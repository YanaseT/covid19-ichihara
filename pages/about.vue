<template>
  <div class="About">
    <page-header class="mb-3">
      {{ $t('当サイトについて') }}
    </page-header>
    <StaticCard>
      <i18n
        tag="p"
        path="当サイトは新型コロナウイルス感染症 (COVID-19) に関する最新情報を提供するために、市原市が提供しているデータを元に{authorWebsite}が開設したものです。"
      >
        <a
          href="https://twitter.com/shelovesnicolas"
          target="_blank"
          rel="noopener"
          place="authorWebsite"
        >
          {{ $t('男子大学生のニコラス') }}
        </a>
      </i18n>
      <br />
      {{
        $t(
          '当サイトは{blogWebsite}を運営する市内在住の大学生により運営される非公式サイトです。'
        )
      }}
      <a
        href="https://ichihara.nicolas.love"
        target="_blank"
        rel="noopener"
        place="blogWebsite"
      >
        {{ $t('地域情報サイト市原市情報センター') }}
      </a>
      <br />
      <br />
      {{
        $t(
          '市原市による公式情報と客観的な数値をわかりやすく伝えることで、市原市にお住まいの方や、市原市内に拠点を持つ企業の方、市原市を訪れる方が、現状を把握して適切な対策を取れるようにすることを目的としています。'
        )
      }}
      <p class="StaticCard-Note">
        <span>
          {{
            $t(
              '※ 当サイトは複製・改変が許されたオープンソースライセンスの下で公開されている、東京都新型コロナウイルス感染症対策サイトの仕組みを利用しています。'
            )
          }}
        </span>
      </p>
    </StaticCard>
    <StaticCard>
      <h3>{{ $t('ブラウザ環境について') }}</h3>
      <p>
        {{ $t('当サイトは以下の環境でご覧いただくことを推奨いたします。') }}
      </p>
      <ul>
        <li>{{ $t('Microsoft Edge 最新版') }}</li>
        <li>{{ $t('Mozilla Firefox 最新版') }}</li>
        <li>
          {{ $t('Google Chrome 最新版（Windows 10以上, Android 8.0以上）') }}
        </li>
        <li>{{ $t('Safari 最新版（macOS, iOS）') }}</li>
        <li>{{ $t('Opera Software ASA Opera 最新版') }}</li>
      </ul>
      <p class="StaticCard-Note">
        <span>{{ $t('※') }}</span>
        <span>
          {{
            $t(
              '※ 推奨環境以外で利用された場合や、推奨環境下でもご利用のブラウザの設定等によっては、正しく表示されない場合がありますのでご了承ください。'
            )
          }}
        </span>
      </p>
    </StaticCard>
    <StaticCard>
      <h3>{{ $t('当サイトへのリンクについて') }}</h3>
      <p>{{ $t('当サイトへのリンクは自由です。') }}</p>
    </StaticCard>
    <StaticCard>
      <h3>{{ $t('JavaScriptについて') }}</h3>
      <p>
        {{ $t('当サイトではJavaScriptを使用しております。') }}<br />
        {{
          $t(
            'JavaScriptを無効にして使用された場合、各ページが正常に動作しない、または、表示されない場合がございます。'
          )
        }}<br />
        {{
          $t(
            '当サイトをご利用の際には、JavaScriptを有効にして頂きますようお願いいたします。'
          )
        }}
      </p>
    </StaticCard>
    <StaticCard>
      <h3>{{ $t('クッキー (Cookie) について') }}</h3>
      <p>
        {{ $t('当サイトの一部ではクッキーを使用しています。') }}<br />
        {{
          $t(
            'クッキーとは、Webコンテンツからの要求で利用者の手元の端末に一時的に保存されるデータのことで、当サイトでは利用状況の把握のためにクッキーを使用する場合があります。'
          )
        }}<br />
      </p>
      <p>
        {{
          $t(
            'ブラウザに関する情報の収集を希望しない場合は、インターネット閲覧ソフト（ブラウザ）をご自身で設定することにより、クッキーの機能が働かないようにすることも可能です。'
          )
        }}
      </p>
      <p>
        {{
          $t(
            'ただし、クッキーを受け入れない設定をされている場合は、当サイトの機能が正常に動作しない場合がございます。'
          )
        }}
      </p>
    </StaticCard>
    <StaticCard>
      <h3>{{ $t('Google Analyticsの利用について') }}</h3>
      <p>
        {{
          $t(
            '当サイトでは、サービス向上やサイトの改善のためにGoogle LLCの提供するアクセス分析のツールであるGoogle Analyticsを利用した計測を行っております。'
          )
        }}<br />
        {{
          $t(
            'Google Analyticsは、当サイトが発行するクッキー (Cookie) を利用して、個人を特定する情報を含まずにWebサイトの利用データ（アクセス状況、トラフィック、閲覧環境など）を収集しております。クッキー (Cookie) の利用に関してはGoogleのプライバシーポリシーと規約に基づいております。'
          )
        }}<br />
        {{
          $t(
            '取得したデータは Webサイト利用状況の分析、サイト運営者へのレポートの作成、その他のサービスの提供に関わる目的に限り、これを使用します。'
          )
        }}<br />
        {{
          $t(
            'Google Analyticsの利用規約及びプライバシーポリシーに関する説明については、Google Analyticsのサイトをご覧ください。'
          )
        }}
      </p>
      <ul>
        <li>
          <a
            :href="
              $t(
                'https://marketingplatform.google.com/about/analytics/terms/jp/'
              )
            "
            target="_blank"
            rel="noopener"
          >
            {{ $t('Google Analytics利用規約') }}
          </a>
        </li>
        <li>
          <a
            :href="$t('https://policies.google.com/privacy?hl=ja')"
            target="_blank"
            rel="noopener"
          >
            {{ $t('Googleのプライバシーポリシー') }}
          </a>
        </li>
        <li>
          <a
            :href="
              $t('https://support.google.com/analytics/answer/6004245?hl=ja')
            "
            target="_blank"
            rel="noopener"
          >
            {{ $t('Google Analyticsに関する詳細情報') }}
          </a>
        </li>
      </ul>
    </StaticCard>
    <StaticCard>
      <h3>{{ $t('免責事項') }}</h3>
      <p>
        {{
          $t(
            '当サイトに掲載されている情報の正確性については万全を期していますが、男子大学生のニコラスは利用者が当サイトの情報を用いて行う一切の行為について責任を負うものではありません。'
          )
        }}
      </p>
      <p>
        {{
          $t(
            'また、利用者が当サイトを利用したことにより発生した利用者の損害及び利用者が第三者に与えた損害に対して、責任を負うものではありません。'
          )
        }}
      </p>
      <p>
        {{
          $t(
            '当サイトに掲載されている情報は、予告なしに変更又は削除することがあります。'
          )
        }}
      </p>
    </StaticCard>
    <StaticCard>
      <h3>{{ $t('データについて') }}</h3>
      <i18n
        tag="p"
        path="当サイトで公表しているデータは、市原市が{catalogWebsite}にて提供しているデータを元にしていますが、必ずしも正確・完全なものとは限りません。当サイトの表示内容について、富山県への直接の問合せは行わないでください。"
      >
        <a
          href="https://www.city.ichihara.chiba.jp/kenko/iryo_kansensyou/kansensyouyobou/covid-19/about/kanja.html"
          target="_blank"
          rel="noopener"
          place="catalogWebsite"
        >
          {{ $t('新型コロナウイルス感染症患者等の発生状況') }}
        </a>
      </i18n>
    </StaticCard>
    <StaticCard>
      <h3>{{ $t('ソースコードについて') }}</h3>
      <p>
        {{
          $t(
            '当サイトのソースコードはMITライセンスで公開されており、誰でも自由に利用することができます。'
          )
        }}
        <i18n path="詳しくは、{githubRepo}をご確認ください。">
          <a
            href="https://github.com/YanaseT/covid19-ichihara"
            target="_blank"
            rel="noopener"
            place="githubRepo"
          >
            {{ $t('GitHub リポジトリ') }}
          </a>
        </i18n>
      </p>
    </StaticCard>
    <StaticCard>
      <h3>{{ $t('お問合わせ') }}</h3>
      <i18n
        tag="p"
        path="当サイトに関するお問合わせは{contactWebsite}にて受け付けています。"
      >
        <a
          href="https://ichihara.nicolas.love/%e3%81%8a%e5%95%8f%e3%81%84%e5%90%88%e3%82%8f%e3%81%9b/"
          target="_blank"
          rel="noopener"
          place="contactWebsite"
        >
          {{ $t('お問い合わせ | 地域情報サイト市原市情報センター') }}
        </a>
      </i18n>
    </StaticCard>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import { MetaInfo } from 'vue-meta'
import PageHeader from '@/components/PageHeader.vue'
import StaticCard from '@/components/StaticCard.vue'

export default Vue.extend({
  components: {
    PageHeader,
    StaticCard
  },
  head(): MetaInfo {
    return {
      title: this.$t('当サイトについて') as string
    }
  }
})
</script>
