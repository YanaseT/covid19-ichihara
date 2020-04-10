<template>
  <v-col cols="12" md="6" class="DataCard">
    <data-table
      :title="$t('陽性患者の属性')"
      :title-id="'attributes-of-confirmed-cases'"
      :chart-data="patientsTable"
      :chart-option="{}"
      :date="Data.patients.date"
      :info="sumInfoOfPatients"
      :url="
        'https://www.city.ichihara.chiba.jp/kenko/iryo_kansensyou/kansensyouyobou/covid-19/about/kanja.html'
      "
    />
  </v-col>
</template>

<script>
import Data from '@/data/data.json'
import formatGraph from '@/utils/formatGraph'
import formatTable from '@/utils/formatTable'
import DataTable from '@/components/DataTable.vue'

export default {
  components: {
    DataTable
  },
  data() {
    // 感染者数グラフ
    const patientsGraph = formatGraph(Data.patients_summary.data)
    // 感染者数
    const patientsTable = formatTable(Data.patients.data)

    const sumInfoOfPatients = {
      lText: patientsGraph[
        patientsGraph.length - 1
      ].cumulative.toLocaleString(),
      sText: this.$t('{date}の累計', {
        date: patientsGraph[patientsGraph.length - 1].label
      }),
      unit: this.$t('人')
    }
    /* const sumInfoOfPatients = {
      lText: Data['patients']['data'].length,
      sText: this.$t('{date} までの累計', {
        date: Data['patients']['date']
      }),
      unit: this.$t('人')
    } */

    // 陽性患者の属性 ヘッダー翻訳
    for (const header of patientsTable.headers) {
      header.text =
        header.value === '退院' ? this.$t('退院※') : this.$t(header.value)
    }
    // 陽性患者の属性 中身の翻訳
    for (const row of patientsTable.datasets) {
      row['居住地'] = this.$t(row['居住地'])
      row['年代'] = this.$t(row['年代'])
      row['性別'] = this.$t(row['性別'])
      // row['退院'] = this.$t(row['退院'])
      row['職業'] = this.$t(row['職業'])
    }

    const data = {
      Data,
      patientsTable,
      sumInfoOfPatients
    }
    return data
  }
}
</script>
