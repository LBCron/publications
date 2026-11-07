# 第 1 章　合意を一人に集めれば判断待ちが伸び、各チームに任せれば承認なしに書き換わる

群: チームのあいだの合意と、集中・分散の失敗

<!--
構造: agent-hub-roles-kaz/philosopher/2026-11-07-eaa-textbook-structure.md（55553ae4）。章題と群の札の字は writer-ja/drafts/eaa-toc/titles.md（d21b0d80、@ope-ultp1635 msg 65a67e15）で書き直した。構造は変えない。
出どころ（構造の表のまま）: 素材 0・1（drafts/agentic-agile-materials/explanations/eaa/0-two-exits.html・1-between-two-collapses.html。SAFe・LeSS・Spotify の記述）、core.md:94-96。Core は publications origin/main 0d07f75 の core.md 版 6。
本文: @ope-ultp1635 msg a8d86548（群ごとに 4 回。群一から）。
引用の訳は素材 0 のもの（素材 0 の付記: 一次資料から取得し原文と照合、英文を訳した）。この本では原文に当たり直していない。
「出口」「崩れ方」は比喩なので使わない（titles.md の判断と同じ）。「集める」「任せる」と、失敗の中身（判断待ちが伸びる・承認なしに書き換わる）で書く。
「一人の PO が持てるチームの数が減る」「列が早く伸びる」は推論で実測ではない（素材 0 の付記）。p.8 の注に書いた。
「実行が安くなった」は確定した事実として扱わない（素材 0 の付記）。p.7 の注に書いた。
-->

> 実行の費用が下がるほど、集める側では判断待ちの列が伸び、任せる側では Contract を自分の側だけで改訂できてしまう。どちらのやり方も成り立つ範囲が狭くなる。

```svg
<svg viewBox="0 0 880 300" width="880" height="300">
  <path d="M440,20 V250" class="lt dash"/>
  <text x="220" y="36" class="t" text-anchor="middle" font-weight="700">一人に集める</text>
  <text x="660" y="36" class="t" text-anchor="middle" font-weight="700">各チームに任せる</text>
  <rect x="320" y="90" width="80" height="56" rx="6" class="h"/><text x="360" y="124" class="ts on" text-anchor="middle">一人</text>
  <g><use href="#i-wait" x="50" y="104" width="22" height="30"/><use href="#i-wait" x="80" y="104" width="22" height="30"/><use href="#i-wait" x="110" y="104" width="22" height="30"/><use href="#i-wait" x="140" y="104" width="22" height="30"/><use href="#i-wait" x="170" y="104" width="22" height="30"/><use href="#i-wait" x="200" y="104" width="22" height="30"/><use href="#i-wait" x="230" y="104" width="22" height="30"/><use href="#i-wait" x="260" y="104" width="22" height="30"/></g>
  <path d="M286,118 H314" class="ln" marker-end="url(#arr)"/>
  <text x="200" y="180" class="t" text-anchor="middle" font-weight="700" fill="#777">判断待ちが伸びる</text>
  <rect x="490" y="80" width="80" height="66" rx="8" class="box"/><text x="530" y="118" class="ts" text-anchor="middle">チーム</text>
  <rect x="750" y="80" width="80" height="66" rx="8" class="box"/><text x="790" y="118" class="ts" text-anchor="middle">チーム</text>
  <rect x="610" y="74" width="100" height="78" rx="3" class="xl" style="fill:#fff"/><text x="660" y="104" class="ts xc" text-anchor="middle">取り決め</text><text x="660" y="132" class="ts xc" text-anchor="middle">版 3→版 4</text>
  <path d="M570,113 H606" class="xl" marker-end="url(#arr-x)"/>
  <text x="660" y="180" class="t xc" text-anchor="middle" font-weight="700">承認なしに書き換わる</text>
  <path d="M60,222 H820" class="ln" marker-end="url(#arr)"/>
  <text x="440" y="246" class="ts sub" text-anchor="middle">実行が安くなるほど、どちらも早く起きる</text>
</svg>
```

## あいだの合意の持ち方は二つ

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <path d="M440,20 V320" class="lt dash"/>
  <text x="220" y="44" class="t" text-anchor="middle" font-weight="700">集める</text>
  <text x="660" y="44" class="t" text-anchor="middle" font-weight="700">任せる</text>
  <rect x="160" y="80" width="120" height="56" rx="6" class="h"/><text x="220" y="105" class="ts on" text-anchor="middle">一人</text><text x="220" y="126" class="tx" text-anchor="middle" style="fill:#fff">または定例の場</text>
  <g class="box"><rect x="50" y="230" width="70" height="50" rx="6"/><rect x="135" y="230" width="70" height="50" rx="6"/><rect x="235" y="230" width="70" height="50" rx="6"/><rect x="320" y="230" width="70" height="50" rx="6"/></g>
  <path d="M85,228 L200,140 M170,228 L212,140 M270,228 L228,140 M355,228 L240,140" class="ln" marker-end="url(#arr)"/>
  <g class="box"><rect x="500" y="90" width="70" height="50" rx="6"/><rect x="750" y="90" width="70" height="50" rx="6"/><rect x="500" y="230" width="70" height="50" rx="6"/><rect x="750" y="230" width="70" height="50" rx="6"/></g>
  <path d="M570,115 H750 M570,255 H750 M535,140 V230 M785,140 V230 M570,140 L750,230" class="ln"/>
  <text x="660" y="108" class="tx" text-anchor="middle">直接合わせる</text>
  <text x="220" y="330" class="ts sub" text-anchor="middle">一人や定例の場が、あいだを決める</text>
  <text x="660" y="330" class="ts sub" text-anchor="middle">関係するチームどうしが、話して合わせる</text>
</svg>
```

大規模開発の手法は、あいだの合意を誰が持つかに、二つの答えを出してきました。一人や定例の場に集めるか、チームどうしに任せるかです。

※ SAFe・LeSS・Spotify の三つを、当事者が書いたもので見ます。三つとも、それぞれの条件の下では機能しています。この本は優劣を判定しません。

## 集める：LeSS は PO の上限を書く

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <text x="160" y="40" class="t" text-anchor="middle" font-weight="700">50 チーム</text>
  <g fill="#fff" stroke="#555" stroke-width="1.5">
    <rect x="40" y="60" width="20" height="20"/><rect x="64" y="60" width="20" height="20"/><rect x="88" y="60" width="20" height="20"/><rect x="112" y="60" width="20" height="20"/><rect x="136" y="60" width="20" height="20"/><rect x="160" y="60" width="20" height="20"/><rect x="184" y="60" width="20" height="20"/><rect x="208" y="60" width="20" height="20"/><rect x="232" y="60" width="20" height="20"/><rect x="256" y="60" width="20" height="20"/>
    <rect x="40" y="84" width="20" height="20"/><rect x="64" y="84" width="20" height="20"/><rect x="88" y="84" width="20" height="20"/><rect x="112" y="84" width="20" height="20"/><rect x="136" y="84" width="20" height="20"/><rect x="160" y="84" width="20" height="20"/><rect x="184" y="84" width="20" height="20"/><rect x="208" y="84" width="20" height="20"/><rect x="232" y="84" width="20" height="20"/><rect x="256" y="84" width="20" height="20"/>
    <rect x="40" y="108" width="20" height="20"/><rect x="64" y="108" width="20" height="20"/><rect x="88" y="108" width="20" height="20"/><rect x="112" y="108" width="20" height="20"/><rect x="136" y="108" width="20" height="20"/><rect x="160" y="108" width="20" height="20"/><rect x="184" y="108" width="20" height="20"/><rect x="208" y="108" width="20" height="20"/><rect x="232" y="108" width="20" height="20"/><rect x="256" y="108" width="20" height="20"/>
    <rect x="40" y="132" width="20" height="20"/><rect x="64" y="132" width="20" height="20"/><rect x="88" y="132" width="20" height="20"/><rect x="112" y="132" width="20" height="20"/><rect x="136" y="132" width="20" height="20"/><rect x="160" y="132" width="20" height="20"/><rect x="184" y="132" width="20" height="20"/><rect x="208" y="132" width="20" height="20"/><rect x="232" y="132" width="20" height="20"/><rect x="256" y="132" width="20" height="20"/>
    <rect x="40" y="156" width="20" height="20"/><rect x="64" y="156" width="20" height="20"/><rect x="88" y="156" width="20" height="20"/><rect x="112" y="156" width="20" height="20"/><rect x="136" y="156" width="20" height="20"/><rect x="160" y="156" width="20" height="20"/><rect x="184" y="156" width="20" height="20"/><rect x="208" y="156" width="20" height="20"/><rect x="232" y="156" width="20" height="20"/><rect x="256" y="156" width="20" height="20"/>
  </g>
  <path d="M290,118 H360" class="ln" marker-end="url(#arr)"/>
  <g><use href="#i-pr" x="380" y="70" width="22" height="28"/><use href="#i-pr" x="406" y="70" width="22" height="28"/><use href="#i-pr" x="432" y="70" width="22" height="28"/><use href="#i-pr" x="458" y="70" width="22" height="28"/><use href="#i-pr" x="484" y="70" width="22" height="28"/><use href="#i-pr" x="380" y="104" width="22" height="28"/><use href="#i-pr" x="406" y="104" width="22" height="28"/><use href="#i-pr" x="432" y="104" width="22" height="28"/><use href="#i-pr" x="458" y="104" width="22" height="28"/><use href="#i-pr" x="484" y="104" width="22" height="28"/><use href="#i-pr" x="380" y="138" width="22" height="28"/><use href="#i-pr" x="406" y="138" width="22" height="28"/><use href="#i-pr" x="432" y="138" width="22" height="28"/><use href="#i-pr" x="458" y="138" width="22" height="28"/><use href="#i-pr" x="484" y="138" width="22" height="28"/></g>
  <text x="443" y="40" class="t" text-anchor="middle" font-weight="700">PBI 200 件</text>
  <text x="443" y="192" class="tx" text-anchor="middle">1 回の iteration で</text>
  <path d="M520,118 H600" class="ln" marker-end="url(#arr)"/>
  <rect x="610" y="90" width="90" height="56" rx="6" class="h"/><text x="655" y="124" class="ts on" text-anchor="middle">PO 一人</text>
  <use href="#i-pile" x="716" y="96" width="40" height="40"/>
  <text x="740" y="176" class="ts xc" text-anchor="middle">一人には多すぎる</text>
  <rect x="40" y="236" width="800" height="110" rx="10" class="lt" style="fill:#fff"/>
  <text x="60" y="270" class="ts sub">LeSS の記述（訳）</text>
  <text x="60" y="302" class="t">50 チームなら、1 iteration だけで PBI は 200 件になる。</text>
  <text x="60" y="332" class="t">200 件の優先順位を付けるのは、一人の PO には多すぎる。</text>
</svg>
```

LeSS は、優先順位の最終決定を一人の Product Owner（PO）に置き、その上限を数で書いています。PO を補う役を置く主な理由も、過負荷を防ぐためです。

出典: LeSS「Area Product Owner」（英文。訳は EAA 紹介 0 による）。PBI は Product Backlog の項目、iteration は開発の 1 周期。

## 集める：SAFe は範囲を限る

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="370" y="30" width="140" height="56" rx="6" class="h"/><text x="440" y="64" class="ts on" text-anchor="middle">中央で決める</text>
  <g class="box"><rect x="60" y="230" width="110" height="50" rx="6"/><rect x="200" y="230" width="110" height="50" rx="6"/><rect x="570" y="230" width="110" height="50" rx="6"/><rect x="710" y="230" width="110" height="50" rx="6"/></g>
  <g class="ts" text-anchor="middle"><text x="115" y="261">チーム</text><text x="255" y="261">チーム</text><text x="625" y="261">チーム</text><text x="765" y="261">チーム</text></g>
  <rect x="330" y="120" width="220" height="60" rx="6" class="hl" style="fill:#fff"/>
  <text x="440" y="144" class="ts hc" text-anchor="middle">頻度が低く、長く効き、</text><text x="440" y="166" class="ts hc" text-anchor="middle">規模の経済が大きい決定</text>
  <path d="M440,118 V92" class="hl" marker-end="url(#arr)"/>
  <g class="tx"><text x="115" y="214" text-anchor="middle">ほかの決定</text><text x="255" y="214" text-anchor="middle">ほかの決定</text><text x="625" y="214" text-anchor="middle">ほかの決定</text><text x="765" y="214" text-anchor="middle">ほかの決定</text></g>
  <rect x="40" y="300" width="800" height="62" rx="10" class="lt" style="fill:#fff"/>
  <text x="60" y="324" class="ts sub">SAFe の記述（訳）</text>
  <text x="60" y="350" class="ts">ほとんどの決定に管理者の関与が必要だと、決定を求める列ができ、進行を止める。</text>
</svg>
```

SAFe は、複数チームの計画を周期ごとの PI Planning でまとめて立て、そのうえで中央に集める決定を、頻度が低く長く効き、規模の経済が大きいものに限ります。

出典: SAFe「Principle #9 Decentralize Decision-Making」（Web Archive の 2022 年 1 月・2023 年 12 月の版。訳は EAA 紹介 0 による）。

## 任せる：LeSS の "just talk"

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="80" y="70" width="180" height="120" rx="10" class="box"/><text x="170" y="136" class="t" text-anchor="middle">チーム</text>
  <rect x="620" y="70" width="180" height="120" rx="10" class="box"/><text x="710" y="136" class="t" text-anchor="middle">チーム</text>
  <path d="M260,110 H614" class="hl" marker-end="url(#arr)"/><path d="M620,150 H266" class="hl" marker-end="url(#arr)"/>
  <text x="440" y="100" class="ts hc" text-anchor="middle">行く・電話する・メール</text>
  <text x="440" y="176" class="ts hc" text-anchor="middle">"just talk"（とにかく話す）</text>
  <rect x="360" y="216" width="160" height="50" rx="6" fill="#b5b5b5" opacity=".7"/><text x="440" y="247" class="ts on" text-anchor="middle">正式な調整の場</text>
  <use href="#i-no" x="510" y="206" width="24" height="24"/><text x="546" y="247" class="tx">要らない</text>
  <rect x="40" y="290" width="800" height="72" rx="10" class="lt" style="fill:#fff"/>
  <text x="60" y="314" class="ts sub">LeSS の記述（訳）</text>
  <text x="60" y="344" class="ts">調整のために、正式で、たいてい遅い仕組みは要らない。</text>
</svg>
```

LeSS は、優先順位は一人の PO に集めつつ、チーム間の調整は任せる側に寄せています。調整が要るなら、相手のチームと直接話して合わせます。

出典: LeSS「Coordination and Integration」（英文。訳は EAA 紹介 0 による）。

## 任せる：Spotify と大きな案件

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <g class="box"><rect x="60" y="40" width="90" height="56" rx="6"/><rect x="180" y="40" width="90" height="56" rx="6"/><rect x="300" y="40" width="90" height="56" rx="6"/><rect x="420" y="40" width="90" height="56" rx="6"/></g>
  <path d="M150,68 H180 M270,68 H300 M390,68 H420" class="ln"/>
  <text x="560" y="64" class="ts">疎結合だが、しっかり揃ったチーム</text>
  <rect x="60" y="120" width="450" height="56" rx="6" class="w"/><text x="285" y="154" class="ts" text-anchor="middle">大きな案件（いくつものチームにまたがる）</text>
  <rect x="40" y="194" width="800" height="66" rx="10" class="lt" style="fill:#fff"/>
  <text x="60" y="218" class="ts sub">Henrik Kniberg（2014）</text>
  <text x="60" y="246" class="ts">大きな案件の進め方は、まだたくさん実験していて、まだうまくない。</text>
  <rect x="40" y="270" width="800" height="92" rx="10" class="lt" style="fill:#fff"/>
  <text x="60" y="294" class="ts sub">Jeremiah Lee（元 Spotify のプロダクトマネージャー、2020）</text>
  <text x="60" y="322" class="ts">エンジニアリングチームの成果に責任を持つ人も、同じ責任の水準で</text>
  <text x="60" y="348" class="ts">作業の優先順位を交渉できる人も、一人もいなかった。</text>
</svg>
```

Spotify は、任せる側に大きく寄りました。目指したのは、疎結合だがしっかり揃ったチームです。当事者は、大きな案件の進め方はまだうまくない、と話しています。

出典: Kniberg「Spotify Engineering Culture part 2」（2014、動画）、Jeremiah Lee（2020）。訳は EAA 紹介 0。一社の実践の記述です。

## 複数社で組んでも同じ二つ

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <path d="M440,20 V320" class="lt dash"/>
  <text x="220" y="44" class="t" text-anchor="middle" font-weight="700">発注側が集める</text>
  <text x="660" y="44" class="t" text-anchor="middle" font-weight="700">ベンダーに任せる</text>
  <rect x="150" y="70" width="140" height="56" rx="6" class="h"/><text x="220" y="104" class="ts on" text-anchor="middle">発注側の定例会議</text>
  <g class="box"><rect x="60" y="200" width="100" height="50" rx="6"/><rect x="280" y="200" width="100" height="50" rx="6"/></g>
  <g class="ts" text-anchor="middle"><text x="110" y="231">ベンダー</text><text x="330" y="231">ベンダー</text></g>
  <path d="M110,198 L190,130 M330,198 L250,130" class="ln" marker-end="url(#arr)"/>
  <rect x="170" y="150" width="100" height="40" rx="3" class="lt" style="fill:#fff"/><text x="220" y="175" class="tx" text-anchor="middle">契約・検収の条件</text>
  <g class="box"><rect x="500" y="130" width="100" height="50" rx="6"/><rect x="720" y="130" width="100" height="50" rx="6"/></g>
  <g class="ts" text-anchor="middle"><text x="550" y="161">ベンダー</text><text x="770" y="161">ベンダー</text></g>
  <path d="M600,146 H714" class="hl" marker-end="url(#arr)"/><path d="M720,166 H606" class="hl" marker-end="url(#arr)"/>
  <text x="660" y="214" class="ts hc" text-anchor="middle">直接合わせる</text>
  <text x="220" y="300" class="ts sub" text-anchor="middle">一社の中の「集める」と同じ形</text>
  <text x="660" y="300" class="ts sub" text-anchor="middle">一社の中の「任せる」と同じ形</text>
</svg>
```

複数社で組む現場にも、同じ二つのやり方があります。発注側の定例会議で合わせて契約と検収の条件に書くか、ベンダーどうしで直接合わせてもらうかです。

## 実行が安くなり、判断が残る

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <text x="40" y="34" class="ts" font-weight="700">これまで</text>
  <rect x="40" y="44" width="300" height="38" class="a"/><text x="190" y="69" class="ts on" text-anchor="middle">実行</text>
  <rect x="340" y="44" width="200" height="38" class="h"/><text x="440" y="69" class="ts on" text-anchor="middle">判断</text>
  <text x="40" y="114" class="ts" font-weight="700">Agent が実行する</text>
  <rect x="40" y="124" width="60" height="38" class="a"/><text x="70" y="149" class="tx" text-anchor="middle" style="fill:#fff">実行</text>
  <rect x="100" y="124" width="200" height="38" class="h"/><text x="200" y="149" class="ts on" text-anchor="middle">判断</text>
  <text x="40" y="194" class="ts" font-weight="700">実行を 3 倍に増やす</text>
  <rect x="40" y="204" width="180" height="38" class="a"/><text x="130" y="229" class="ts on" text-anchor="middle">実行 × 3</text>
  <rect x="220" y="204" width="600" height="38" class="h"/><text x="520" y="229" class="ts on" text-anchor="middle">判断 × 3</text>
  <text x="440" y="290" class="t" text-anchor="middle" font-weight="700">判断する人と、実行する者が分かれた</text>
  <text x="440" y="324" class="ts sub" text-anchor="middle">実行を増やすほど、全体の速さは判断で決まる</text>
  <text x="440" y="356" class="tx" text-anchor="middle">長さは説明のための目安で、実測ではない</text>
</svg>
```

Agent が実装を担えるようになり、実行が安くなりました。判断する人と実行する者が分かれ、実行を増やすほど、全体の速さは判断で決まるようになります。

※ Agent は、計画し、道具を使い、結果を確かめて直す AI。「実行が安くなった」の裏づけは売り手側の調査が多く、逆向きの実測もあります。

## 集める側：判断待ちの列が伸びる

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <text x="60" y="50" class="ts" font-weight="700">これまで</text>
  <g class="box"><rect x="60" y="66" width="44" height="36" rx="4"/><rect x="112" y="66" width="44" height="36" rx="4"/><rect x="164" y="66" width="44" height="36" rx="4"/><rect x="216" y="66" width="44" height="36" rx="4"/><rect x="268" y="66" width="44" height="36" rx="4"/><rect x="320" y="66" width="44" height="36" rx="4"/></g>
  <use href="#i-wait" x="440" y="70" width="20" height="28"/><use href="#i-wait" x="466" y="70" width="20" height="28"/>
  <path d="M370,84 H430" class="ln" marker-end="url(#arr)"/>
  <rect x="740" y="62" width="80" height="44" rx="6" class="h"/><text x="780" y="90" class="ts on" text-anchor="middle">一人</text>
  <path d="M494,84 H734" class="ln" marker-end="url(#arr)"/>
  <text x="60" y="170" class="ts" font-weight="700">1 チームが出すものが増える</text>
  <g class="box"><rect x="60" y="186" width="44" height="36" rx="4"/><rect x="112" y="186" width="44" height="36" rx="4"/><rect x="164" y="186" width="44" height="36" rx="4"/><rect x="216" y="186" width="44" height="36" rx="4"/><rect x="268" y="186" width="44" height="36" rx="4"/><rect x="320" y="186" width="44" height="36" rx="4"/></g>
  <path d="M370,204 H430" class="ln" marker-end="url(#arr)"/>
  <g><use href="#i-wait" x="440" y="190" width="20" height="28"/><use href="#i-wait" x="466" y="190" width="20" height="28"/><use href="#i-wait" x="492" y="190" width="20" height="28"/><use href="#i-wait" x="518" y="190" width="20" height="28"/><use href="#i-wait" x="544" y="190" width="20" height="28"/><use href="#i-wait" x="570" y="190" width="20" height="28"/><use href="#i-wait" x="596" y="190" width="20" height="28"/><use href="#i-wait" x="622" y="190" width="20" height="28"/><use href="#i-wait" x="648" y="190" width="20" height="28"/><use href="#i-wait" x="674" y="190" width="20" height="28"/><use href="#i-wait" x="700" y="190" width="20" height="28"/></g>
  <rect x="740" y="182" width="80" height="44" rx="6" class="h"/><text x="780" y="210" class="ts on" text-anchor="middle">一人</text>
  <text x="440" y="290" class="t" text-anchor="middle" font-weight="700">同じ一人が持てるチームの数が減る</text>
  <text x="440" y="324" class="ts sub" text-anchor="middle">決定を求める列も、同じ理由で早く伸びる</text>
</svg>
```

実行が安くなると、一つのチームが 1 回の iteration で出すものが増えます。同じ一人の PO が持てるチームの数が減り、決定を求める列も早く伸びます。

※ LeSS と SAFe が書いたことに、前のページの前提を当てた推論です。実測ではありません。

## 任せる側：合わせた中身が書かれない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <text x="60" y="44" class="ts" font-weight="700">これまで</text>
  <rect x="60" y="60" width="70" height="48" rx="6" class="h"/><text x="95" y="90" class="ts on" text-anchor="middle">人</text>
  <rect x="300" y="60" width="70" height="48" rx="6" class="h"/><text x="335" y="90" class="ts on" text-anchor="middle">人</text>
  <path d="M130,84 H294" class="hl"/><text x="215" y="76" class="tx hc" text-anchor="middle">話して合わせる</text>
  <path d="M335,110 V150" class="hl" marker-end="url(#arr)"/>
  <rect x="270" y="156" width="130" height="40" rx="4" class="h"/><text x="335" y="182" class="ts on" text-anchor="middle">同じ人が作る</text>
  <text x="215" y="236" class="ts sub" text-anchor="middle">書かなくても、作る所まで届いた</text>
  <path d="M440,20 V260" class="lt dash"/>
  <text x="500" y="44" class="ts" font-weight="700">Agent が実行</text>
  <rect x="500" y="60" width="70" height="48" rx="6" class="h"/><text x="535" y="90" class="ts on" text-anchor="middle">人</text>
  <rect x="740" y="60" width="70" height="48" rx="6" class="h"/><text x="775" y="90" class="ts on" text-anchor="middle">人</text>
  <path d="M570,84 H734" class="hl"/><text x="655" y="76" class="tx hc" text-anchor="middle">話して合わせる</text>
  <path d="M775,110 V150" class="lt dash" marker-end="url(#arr)"/><text x="790" y="136" class="tx xc">書かれていない</text>
  <rect x="720" y="156" width="110" height="40" rx="4" class="a"/><text x="775" y="182" class="ts on" text-anchor="middle">Agent が作る</text>
  <g class="ts xc" text-anchor="middle"><text x="660" y="236">欠けた所を、毎回違う形で埋める</text></g>
  <text x="440" y="300" class="t" text-anchor="middle" font-weight="700">合わせた人と、実行する者が分かれた</text>
</svg>
```

話して合わせた中身は、書かれていませんでした。合わせた本人が実行していたので、書かなくても実行に届きました。Agent が実行すると、そうはいきません。

※ Agent は書かれていない前提を持たず、欠けた所をもっともらしく、毎回違う形で埋めます。AA の本の前提「書かれたものだけが効く」と同じです。

## 書かれなければ、全部見るしかない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="140" width="200" height="70" rx="6" class="lt" style="fill:#fff"/><text x="140" y="170" class="ts" text-anchor="middle">合わせた中身が</text><text x="140" y="194" class="ts" text-anchor="middle">書かれていない</text>
  <path d="M240,160 L400,90" class="ln" marker-end="url(#arr)"/><path d="M240,190 L400,260" class="ln" marker-end="url(#arr)"/>
  <rect x="410" y="56" width="200" height="64" rx="6" class="h"/><text x="510" y="94" class="ts on" text-anchor="middle">合わせた人が全部見る</text>
  <rect x="410" y="228" width="200" height="64" rx="6" class="a"/><text x="510" y="266" class="ts on" text-anchor="middle">見ずに進める</text>
  <path d="M610,88 H660" class="ln" marker-end="url(#arr)"/><path d="M610,260 H660" class="ln" marker-end="url(#arr)"/>
  <use href="#i-wait" x="672" y="70" width="24" height="34"/><text x="710" y="94" class="ts">判断待ち</text>
  <use href="#i-pile" x="670" y="240" width="34" height="34"/><text x="714" y="264" class="ts xc">揃わない</text>
  <text x="710" y="124" class="tx">集める側と同じ</text>
  <text x="440" y="350" class="t" text-anchor="middle" font-weight="700">揃ったかどうかが、書いたもので確かめられない</text>
</svg>
```

書かれていないと、揃ったかどうかが分かりません。確かめるには合わせた人が全部を見るしかなく、それは集める側と同じ判断待ちです。見なければ揃わないまま進みます。

## 書いても、片側で書き換わる

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="70" width="200" height="160" rx="10" class="box"/><text x="140" y="104" class="t" text-anchor="middle" font-weight="700">チーム</text>
  <rect x="640" y="70" width="200" height="160" rx="10" class="box"/><text x="740" y="104" class="t" text-anchor="middle" font-weight="700">チーム</text>
  <rect x="340" y="50" width="200" height="70" rx="3" class="lt" style="fill:#fff"/><text x="440" y="80" class="ts" text-anchor="middle">取り決め 版 3</text><text x="440" y="106" class="tx" text-anchor="middle">インターフェース・受入の条件</text>
  <rect x="340" y="160" width="200" height="70" rx="3" class="xw"/><text x="440" y="190" class="ts xc" text-anchor="middle" font-weight="700">取り決め 版 4</text><text x="440" y="214" class="tx xc" text-anchor="middle">自分の側だけで改訂</text>
  <path d="M240,190 H334" class="xl" marker-end="url(#arr-x)"/><text x="287" y="180" class="tx xc" text-anchor="middle">書き換える</text>
  <path d="M440,122 V156" class="xl" marker-end="url(#arr-x)"/>
  <path d="M546,85 H640" class="ln"/><text x="740" y="160" class="ts" text-anchor="middle">まだ版 3 のつもり</text>
  <use href="#i-no" x="728" y="176" width="24" height="24"/>
  <text x="440" y="290" class="t xc" text-anchor="middle" font-weight="700">相手の承認なしに変わり、取り決めでなくなる</text>
  <text x="440" y="326" class="ts sub" text-anchor="middle">インターフェースも受入の条件も、相手の都合でいつでも変わりうる</text>
</svg>
```

書いても、その取り決めを自分の側だけで改訂できれば、相手の承認なしに書き換わります。インターフェースも受入の条件も、いつでも変わりうるものになります。

※ EAA は、共有する文書の所有者を人間とし、改訂を出した者がその改訂を承認しないと決めて防ぎます（第 10 章）。出典: EAA Core 版 6「4. 提案と変更」。

## 相手の中は、こちらから選べない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="70" width="240" height="180" rx="10" class="box"/><text x="160" y="104" class="t" text-anchor="middle" font-weight="700">自分たち</text>
  <rect x="125" y="140" width="70" height="48" rx="6" class="h"/><text x="160" y="170" class="ts on" text-anchor="middle">人</text>
  <rect x="600" y="70" width="240" height="180" rx="10" class="box"/><text x="720" y="104" class="t" text-anchor="middle" font-weight="700">組んでいる一社</text>
  <rect x="620" y="140" width="70" height="48" rx="6" class="h" opacity=".45"/><text x="655" y="170" class="ts on" text-anchor="middle">人</text>
  <path d="M694,164 H732" class="ln" marker-end="url(#arr)"/>
  <rect x="740" y="140" width="80" height="48" rx="6" class="a"/><text x="780" y="170" class="ts on" text-anchor="middle">Agent</text>
  <text x="720" y="226" class="tx" text-anchor="middle">相手が自分で決める</text>
  <path d="M280,130 H594" class="ln"/><rect x="380" y="108" width="120" height="44" rx="3" class="lt" style="fill:#fff"/><text x="440" y="136" class="ts" text-anchor="middle">あいだの合意</text>
  <text x="440" y="304" class="t" text-anchor="middle" font-weight="700">相手が実行を Agent に移せば、</text>
  <text x="440" y="338" class="t" text-anchor="middle" font-weight="700">あいだの合意にも同じことが起きる</text>
</svg>
```

相手の中が Agent で動くかどうかは、こちらからは選べません。組んでいる一社が実行を Agent に移せば、その一社とのあいだの合意に同じことが起きます。

※ 自分のチームや組んでいるベンダーにまだ Agent が入っていなくても、入った時点でこうなります。

## 二つのやり方が、どちらも狭くなる

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <path d="M440,20 V200" class="lt dash"/>
  <text x="220" y="44" class="t" text-anchor="middle" font-weight="700">集める</text>
  <text x="660" y="44" class="t" text-anchor="middle" font-weight="700">任せる</text>
  <rect x="110" y="66" width="220" height="56" rx="6" class="lt" style="fill:#fff"/><text x="220" y="100" class="ts" text-anchor="middle">判断待ちの列が伸びる</text>
  <rect x="550" y="66" width="220" height="56" rx="6" class="lt" style="fill:#fff"/><text x="660" y="90" class="ts" text-anchor="middle">書かなければ全部見るか、</text><text x="660" y="112" class="ts" text-anchor="middle">見ずに揃わない</text>
  <rect x="550" y="132" width="220" height="56" rx="6" class="xl" style="fill:#fff"/><text x="660" y="156" class="ts xc" text-anchor="middle">書いても、片側で</text><text x="660" y="178" class="ts xc" text-anchor="middle">承認なしに書き換わる</text>
  <rect x="40" y="226" width="800" height="136" rx="10" class="hl" style="fill:#fff"/>
  <text x="440" y="266" class="tl hc" text-anchor="middle">あいだの合意を、一人にも会議にも預けず、</text>
  <text x="440" y="302" class="tl hc" text-anchor="middle">誰がどう持つか</text>
  <a href="#ch2"><text x="440" y="342" class="ts" text-anchor="middle">答えは第 2 章から組み立てる</text></a>
</svg>
```

集めれば判断待ちが伸び、任せれば承認なしに書き換わります。あいだの合意を一人にも会議にも預けず、誰がどう持つか。その答えを、第 2 章から組み立てます。

※ AA の本の第 1 章で見た、人が全部見るか外すかの板挟みが、チームのあいだに出た形です。
