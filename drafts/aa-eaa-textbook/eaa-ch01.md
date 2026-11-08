# 第 1 章　人間は職能で分業してきたが、職能は Agent にとって分業の軸になるほどの文脈ではない

群: 巨大なシステムの分業という問い

<!--
構造: agent-hub-roles-kaz/writer-ja/drafts/eaa-toc/structure-v5.md（6e3f57bf・dd08b888）の第 1 章。GO: @ope-ultp1635 msg b918626f。
2d0ca30 までの第 1 章（LeSS・SAFe・Spotify の、合意を集める／任せるの二つ）は v5 の付録へ移す。この章には持ってこない。移すとき、旧第 1 章の書き手のメモにある直し（引用は原文に当たり直していないことを本文と絵で見せる・LeSS の URL と参照日・片側改訂を防ぐのは core.md:79・80・91・EAA 紹介 0 の置き場所を本文から外す）を落とさない。旧本文は 2d0ca30 の eaa-ch01.md にある。
所有者の言葉の引用は structure-v5.md「イデア」の逐語。
p.「AA のレビュー分離は別の目的」: AA の本の第 2 章は、レビューを書いた AI から切り離す（作成者の文脈を持たない者に確かめさせる）。この章の「職能で切らない」と食い違って読まれないよう、あれは分業ではなく職務分離（core.md:45「同じ判断について、行う者と、承認または検証する者を別の者にすること」）だと書いた。AA の本の字: aa-ch02.md「判定は残し、レビュアーを文脈から切る」「レビューは回数でなく、文脈を分ける」。
「人間は職能ごとに覚えることが多いので、渡し直しを払っても職能で分けた」は structure-v5.md 第 1 章の行の字。所有者の字は「人間は職能に応じて分業してた」まで。理由の部分は書き手の導出（structure-v5 でそう書いて GO を受けた）。
-->

```svg
<svg viewBox="0 0 880 340" width="880" height="340">
  <text x="215" y="30" class="t" text-anchor="middle" font-weight="700">職能で分ける</text>
  <g class="ts" text-anchor="middle">
    <rect x="30" y="50" width="80" height="200" rx="8" class="box"/><text x="70" y="76">設計</text>
    <rect x="125" y="50" width="80" height="200" rx="8" class="box"/><text x="165" y="76">実装</text>
    <rect x="220" y="50" width="80" height="200" rx="8" class="box"/><text x="260" y="76">テスト</text>
    <rect x="315" y="50" width="80" height="200" rx="8" class="box"/><text x="355" y="76">レビュー</text>
  </g>
  <g class="a"><rect x="40" y="140" width="60" height="30" rx="4"/><rect x="135" y="140" width="60" height="30" rx="4"/><rect x="230" y="140" width="60" height="30" rx="4"/><rect x="325" y="140" width="60" height="30" rx="4"/></g>
  <path d="M100,155 H133 M195,155 H228 M290,155 H323" class="xl" marker-end="url(#arr-x)"/>
  <text x="212" y="276" class="ts xc" text-anchor="middle">一つの機能の文脈を、持ち場ごとに渡し直す</text>
  <text x="212" y="306" class="ts sub" text-anchor="middle">人間には、職能で分ける理由があった</text>
  <rect x="480" y="50" width="370" height="200" rx="10" class="hl" style="fill:#fff"/>
  <text x="665" y="30" class="t hc" text-anchor="middle" font-weight="700">Agent には職能が小さな文脈</text>
  <rect x="555" y="80" width="220" height="44" rx="22" class="a"/><text x="665" y="108" class="ts on" text-anchor="middle">Agent</text>
  <text x="665" y="160" class="ts" text-anchor="middle">設計・実装・テスト・レビュー</text>
  <text x="665" y="190" class="ts" text-anchor="middle">どれも頼める</text>
  <text x="665" y="306" class="ts hc" text-anchor="middle">職能で切ると、渡し直しだけが残る</text>
</svg>
```

人間が職能で分けたのは、職能ごとに覚えることが多いからです。Agent にとって職能は大きな文脈ではないので、職能で切ると渡し直しだけが残ります。

## 所有者の言葉

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="60" y="40" width="760" height="250" rx="10" class="soft"/>
  <text x="90" y="90" class="t hc" font-weight="700">人間は職能に応じて分業してたが、</text>
  <text x="90" y="130" class="t hc" font-weight="700">職能はエージェントにとっては大したコンテキストではない。</text>
  <text x="90" y="190" class="t" font-weight="700">それよりもドメインとか価値とか権限とかで</text>
  <text x="90" y="230" class="t" font-weight="700">分けた方が疎結合になる。</text>
  <text x="440" y="340" class="ts sub" text-anchor="middle">EAA Core の所有者の言葉（原文のまま）。この章は色の付いた前半を扱う</text>
</svg>
```

この章は、この言葉の前半を扱います。人間はなぜ職能で分けてきたのか、それが Agent ではなぜ成り立たないのか、です。後半の切り方は、第 2 章から見ます。

※ 出典: EAA Core の所有者（Kazuhiro）が、この本の構成を決めるときに書いた考え。

## 職能で分けると機能が切れる

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <g class="ts" text-anchor="middle">
    <rect x="40" y="60" width="180" height="220" rx="8" class="box"/><text x="130" y="90" font-weight="700">設計</text>
    <rect x="245" y="60" width="180" height="220" rx="8" class="box"/><text x="335" y="90" font-weight="700">実装</text>
    <rect x="450" y="60" width="180" height="220" rx="8" class="box"/><text x="540" y="90" font-weight="700">テスト</text>
    <rect x="655" y="60" width="180" height="220" rx="8" class="box"/><text x="745" y="90" font-weight="700">レビュー</text>
  </g>
  <rect x="40" y="150" width="795" height="40" rx="4" class="hl" style="fill:none"/>
  <text x="440" y="140" class="ts hc" text-anchor="middle">一つの機能（在庫の引当）</text>
  <path d="M220,170 H245 M425,170 H450 M630,170 H655" class="xl"/>
  <text x="440" y="330" class="t" text-anchor="middle" font-weight="700">持ち場を越えるたび（赤）に、機能の前提を渡し直す</text>
</svg>
```

設計・実装・テスト・レビューで分けると、一つの機能の文脈が持ち場ごとに切られます。持ち場を越えるたびに、その機能の前提を渡し直します。

※ 例の機能は説明のために選んだ。

## 人間は渡し直しを払ってきた

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="380" height="230" rx="10" class="box"/>
  <text x="230" y="96" class="t" text-anchor="middle" font-weight="700">職能で分ける理由</text>
  <g class="ts"><text x="70" y="140">職能ごとに、覚える知識と</text><text x="70" y="166">手の技が多い</text><text x="70" y="210">一人で全部はこなせない</text></g>
  <rect x="460" y="60" width="380" height="230" rx="10" class="box"/>
  <text x="650" y="96" class="t" text-anchor="middle" font-weight="700">職能で分ける手間</text>
  <g class="ts"><text x="490" y="140">持ち場を越えるたびの</text><text x="490" y="166">渡し直し</text></g>
  <path d="M420,175 H456" class="ln" marker-end="url(#arr)"/>
  <text x="440" y="340" class="t hc" text-anchor="middle" font-weight="700">理由が手間を上回るので、人間は職能で分けた</text>
</svg>
```

人間は、職能ごとに覚える知識と手の技が多く、一人で全部はこなせません。だから渡し直しの手間を払っても、職能で分けてきました。

## Agent には持ち場を問わず頼める

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="330" y="140" width="220" height="60" rx="30" class="a"/><text x="440" y="178" class="t on" text-anchor="middle">Agent</text>
  <g class="ts" text-anchor="middle">
    <rect x="60" y="50" width="160" height="44" rx="6" class="soft"/><text x="140" y="78">設計</text>
    <rect x="660" y="50" width="160" height="44" rx="6" class="soft"/><text x="740" y="78">実装</text>
    <rect x="60" y="250" width="160" height="44" rx="6" class="soft"/><text x="140" y="278">テスト</text>
    <rect x="660" y="250" width="160" height="44" rx="6" class="soft"/><text x="740" y="278">レビュー</text>
  </g>
  <path d="M220,72 L330,150 M660,72 L550,150 M220,272 L330,192 M660,272 L550,192" class="ln"/>
  <text x="440" y="340" class="t" text-anchor="middle" font-weight="700">職能ごとの覚えることの多さは、分ける理由にならない</text>
</svg>
```

Agent には、設計・実装・テスト・レビューのどれも頼めます。職能ごとに覚えることが多いという理由は、Agent を分ける理由になりません。

※ AA の本の第 2 章は、作る役と判定する役を、どちらも Agent に頼む形を扱った。

## 職能で切ると渡し直しだけ残る

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <g>
    <text x="220" y="50" class="t" text-anchor="middle" font-weight="700">人間</text>
    <rect x="60" y="80" width="150" height="120" rx="6" class="ok"/><text x="135" y="146" class="ts on" text-anchor="middle">分ける理由</text>
    <rect x="230" y="80" width="150" height="120" rx="6" class="xl" style="fill:#fff"/><text x="305" y="146" class="ts xc" text-anchor="middle">渡し直し</text>
  </g>
  <path d="M440,40 V260" class="lt dash"/>
  <g>
    <text x="660" y="50" class="t" text-anchor="middle" font-weight="700">Agent</text>
    <rect x="500" y="80" width="150" height="120" rx="6" class="lt dash" style="fill:#fff"/><text x="575" y="146" class="ts sub" text-anchor="middle">理由は無い</text>
    <rect x="670" y="80" width="150" height="120" rx="6" class="xl" style="fill:#fff"/><text x="745" y="146" class="ts xc" text-anchor="middle">渡し直し</text>
  </g>
  <text x="440" y="320" class="t xc" text-anchor="middle" font-weight="700">理由が消えても、手間は消えない</text>
</svg>
```

Agent を職能で分けると、人間が職能で分けた理由は無いまま、機能の文脈を持ち場ごとに渡し直す手間だけが残ります。

## 人の役割の割り当ても職能

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <g class="ts" text-anchor="middle">
    <rect x="40" y="60" width="180" height="50" rx="6" class="h"/><text x="130" y="91" class="on">設計担当の人</text>
    <rect x="40" y="140" width="180" height="50" rx="6" class="h"/><text x="130" y="171" class="on">実装担当の人</text>
    <rect x="40" y="220" width="180" height="50" rx="6" class="h"/><text x="130" y="251" class="on">テスト担当の人</text>
    <rect x="660" y="60" width="180" height="50" rx="25" class="a"/><text x="750" y="91" class="on">設計担当の Agent</text>
    <rect x="660" y="140" width="180" height="50" rx="25" class="a"/><text x="750" y="171" class="on">実装担当の Agent</text>
    <rect x="660" y="220" width="180" height="50" rx="25" class="a"/><text x="750" y="251" class="on">テスト担当の Agent</text>
  </g>
  <path d="M220,85 H654 M220,165 H654 M220,245 H654" class="lt dash" marker-end="url(#arr)"/>
  <text x="440" y="330" class="t xc" text-anchor="middle" font-weight="700">切る軸は、人の職能のまま</text>
</svg>
```

設計担当・実装担当・テスト担当のように、人の役割を Agent に割り当てる形は、職能の分業を写したものです。何で分けるかという問いには答えていません。

## AA のレビュー分離は別の目的

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="50" width="380" height="240" rx="10" class="box"/>
  <text x="230" y="84" class="t" text-anchor="middle" font-weight="700">AA の本：レビューの切り離し</text>
  <rect x="70" y="120" width="140" height="44" rx="22" class="a"/><text x="140" y="148" class="ts on" text-anchor="middle">作る Agent</text>
  <rect x="250" y="120" width="140" height="44" rx="22" class="a"/><text x="320" y="148" class="ts on" text-anchor="middle">判定する Agent</text>
  <path d="M230,110 V180" class="xl dash"/>
  <text x="230" y="220" class="ts" text-anchor="middle">作った文脈を持たない者が確かめる</text>
  <text x="230" y="250" class="tx" text-anchor="middle">職務分離</text>
  <rect x="460" y="50" width="380" height="240" rx="10" class="hl" style="fill:#fff"/>
  <text x="650" y="84" class="t hc" text-anchor="middle" font-weight="700">この本：分業の軸</text>
  <text x="650" y="150" class="ts" text-anchor="middle">各主体が、自分の仕事の文脈を</text>
  <text x="650" y="176" class="ts" text-anchor="middle">切り替えずに持てるように分ける</text>
  <text x="650" y="250" class="tx" text-anchor="middle">価値・ドメイン・権限</text>
  <text x="440" y="340" class="ts sub" text-anchor="middle">左は確かめを独立させる決まりで、右は仕事を分ける軸。どちらも要る</text>
</svg>
```

AA の本は、レビューを書いた AI から切り離しました。これは仕事を分けるためではなく、作った文脈を持たない者に確かめさせるためです。

※ EAA Core の職務分離（同じ判断について、行う者と、承認または検証する者を別の者にすること）に当たる。出典: EAA Core 版 6「0.」の用語表。

## Agent の文脈は扱う対象の側にある

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="200" y="50" width="480" height="240" rx="10" class="hl" style="fill:#fff"/>
  <text x="440" y="86" class="t hc" text-anchor="middle" font-weight="700">Agent が判断に使う文脈</text>
  <g class="ts" text-anchor="middle">
    <rect x="230" y="116" width="420" height="40" rx="4" class="soft"/><text x="440" y="142">扱う対象の語と記録（ドメイン）</text>
    <rect x="230" y="166" width="420" height="40" rx="4" class="soft"/><text x="440" y="192">何を優先するか（価値）</text>
    <rect x="230" y="216" width="420" height="40" rx="4" class="soft"/><text x="440" y="242">何を決められるか（権限）</text>
  </g>
  <g opacity=".6"><rect x="30" y="140" width="130" height="60" rx="6" class="lt dash" style="fill:#fff"/><text x="95" y="176" class="ts sub" text-anchor="middle">職能</text></g>
  <text x="440" y="340" class="t" text-anchor="middle" font-weight="700">この側で切れば、主体の中で文脈を切り替えずに済む</text>
</svg>
```

Agent が判断に使う文脈は、職能ではなく、扱う対象の語と記録、優先する価値、判断の権限の側にあります。この側で切れば、主体の中で文脈を切り替えずに済みます。

## 次章へ：切り方の判定

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="140" y="70" width="600" height="160" rx="10" class="hl" style="fill:#fff"/>
  <text x="440" y="120" class="t hc" text-anchor="middle" font-weight="700">判定は一つ</text>
  <text x="440" y="164" class="t" text-anchor="middle">その主体の中で、コンテキストスイッチが起きないか</text>
  <text x="440" y="200" class="ts sub" text-anchor="middle">価値・ドメイン・権限は、この判定に通る切り方の例</text>
  <text x="440" y="300" class="ts" text-anchor="middle">第 2 章</text>
</svg>
```

では、どこで切れば文脈が疎結合になるか。第 2 章で、切り方の判定を一つに定めます。その主体の中で、コンテキストスイッチが起きないかです。
