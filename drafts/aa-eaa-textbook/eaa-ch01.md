# 第 1 章　職能は、Agent の仕事を分ける軸にならない

群: 巨大なシステムの分業という問い

<!--
構造: agent-hub-roles-kaz/writer-ja/drafts/eaa-toc/structure-v5.md（6e3f57bf・dd08b888）の第 1 章。GO: @ope-ultp1635 msg b918626f。
2d0ca30 までの第 1 章（LeSS・SAFe・Spotify の、合意を集める／任せるの二つ）は v5 の付録へ移す。この章には持ってこない。移すとき、旧第 1 章の書き手のメモにある直し（引用は原文に当たり直していないことを本文と絵で見せる・LeSS の URL と参照日・片側改訂を防ぐのは core.md:79・80・91・EAA 紹介 0 の置き場所を本文から外す）を落とさない。旧本文は 2d0ca30 の eaa-ch01.md にある。
所有者の言葉の引用は structure-v5.md「イデア」の逐語。
p.「AA のレビュー分離は別の目的」: AA の本の第 2 章は、レビューを書いた AI から切り離す（作成者の文脈を持たない者に確かめさせる）。この章の「職能で切らない」と食い違って読まれないよう、あれは分業ではなく職務分離（core.md:45「同じ判断について、行う者と、承認または検証する者を別の者にすること」）だと書いた。AA の本の字: aa-ch02.md「判定は残し、レビュアーを文脈から切る」「レビューは回数でなく、文脈を分ける」。
「人間は職能ごとに覚えることが多いので、渡し直しを払っても職能で分けた」は structure-v5.md 第 1 章の行の字。所有者の字は「人間は職能に応じて分業してた」まで。理由の部分は書き手の導出（structure-v5 でそう書いて GO を受けた）。
群二で直したこと（@ope-ultp1635 msg 83d1e0ea、@reader 目次 v5 の通読 349c4d63 の桜井）: 章題「人間は職能で分業してきた」は事実として誤り。LeSS・SAFe・Spotify はチームを職能で分けず、要る技能を一つのチームに揃える。原文に当たり直した（2026-11-08、WebFetch）:
- LeSS「Feature Teams」https://less.works/less/structure/feature-teams —「a long-lived, cross-functional, cross-component team that completes many end-to-end customer features」「a component team structure reinforces sequential development」（待ち・仕掛り・多くの handoff を生むと続く）。表で component team は「focus on single specialization」、feature team は「focus on multiple specializations」。
- SAFe「Agile Teams」https://framework.scaledagile.com/agile-teams —「An Agile Team is a cross-functional group of typically ten or fewer individuals with all the skills necessary to define, build, test, and deliver increments of value」。「Agile Release Train」https://framework.scaledagile.com/agile-release-train —「ARTs are cross-functional and contain all the necessary capabilities for the solution they deliver」「Organizing ARTs around value」。
群一の旧第 1 章は EAA 紹介 0 の訳に揃えるため当たり直さなかった。今回の字は紹介 0 に無い（紹介 0 は合意の持ち方を引いた）ので、揃える訳が無く、当たり直した。
直し方: 章題を「職能で分ける理由は人間にあった」にし、人間が必ず職能で分けたとは書かない。p.「LeSS・SAFe は職能で分けない」「枠組みが減らしたのも渡し直し」「チームの中には職能が残る」を足した。枠組みが職能で分けないのはこの章の主張（職能で切ると渡し直しが残る）を人間の側で先に示したもので、主張を弱めない。「チームの中には職能が残る」は書き手の読み（SAFe の all the skills・LeSS の multiple specializations は、技能を持つ人が複数いることを前提にする）で、注に書いた。
Spotify は付録で引くので、この章では名前を挙げない（付録の旧本文は EAA 紹介 0 の訳）。
77a7fc9 の検算と通読を受けて直した（@ope-ultp1635 msg 614590ff。判定の正本 @reviewer 2026-11-08-eaa-textbook-77a7fc9-ch00-04 / ch05-08 / ch09-12-furoku、@reader 2026-11-08-eaa-textbook-v5-215p-6readers-r3）: 第 3 章が SAFe の value stream と別の語だとした「価値」を、SAFe の側で先に使っていた（絵「価値の単位で組む」）。「機能を最後まで作る」「value stream に沿って組む」にした。「枠組みが職能で分けないのも渡し直しを減らすため」は出典が LeSS だけなので、LeSS に限った。「チームの中には職能が残る」は LeSS が直接言っているので「書き手の読み」を出典に替えた（@reviewer 1 便）。
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

人間が職能で分けるのは、職能ごとに覚えることが多いからです。大規模開発の枠組みは、チームを職能で分けなくなりました。LeSS は、その理由に渡しと待ちが増えることを挙げます。Agent にとって職能は大きな文脈ではないので、職能で切ると渡し直しだけが残ります。

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

この章は、この言葉の前半を扱います。人間が職能で分ける理由は何か、それが Agent ではなぜ成り立たないのか、です。後半の切り方は、第 2 章から見ます。

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

## 人間には職能で分ける理由がある

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="380" height="230" rx="10" class="box"/>
  <text x="230" y="96" class="t" text-anchor="middle" font-weight="700">職能で分ける理由</text>
  <g class="ts"><text x="70" y="140">職能ごとに、覚える知識と</text><text x="70" y="166">手の技が多い</text><text x="70" y="210">一人で全部はこなせない</text></g>
  <rect x="460" y="60" width="380" height="230" rx="10" class="box"/>
  <text x="650" y="96" class="t" text-anchor="middle" font-weight="700">職能で分ける手間</text>
  <g class="ts"><text x="490" y="140">持ち場を越えるたびの</text><text x="490" y="166">渡し直し</text></g>
  <path d="M420,175 H456" class="ln" marker-end="url(#arr)"/>
  <text x="440" y="340" class="t hc" text-anchor="middle" font-weight="700">理由が手間を上回るとき、人間は職能で分ける</text>
</svg>
```

人間は、職能ごとに覚える知識と手の技が多く、一人で全部はこなせません。だから職能で分ける組織は、渡し直しの手間を払ってきました。

## LeSS・SAFe は職能で分けない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <g opacity=".6">
    <text x="200" y="40" class="ts sub" text-anchor="middle">職能で分けたチーム</text>
    <g class="tx" text-anchor="middle">
      <rect x="40" y="60" width="70" height="40" rx="6" class="soft"/><text x="75" y="85">設計</text>
      <rect x="120" y="60" width="70" height="40" rx="6" class="soft"/><text x="155" y="85">実装</text>
      <rect x="200" y="60" width="70" height="40" rx="6" class="soft"/><text x="235" y="85">テスト</text>
      <rect x="280" y="60" width="80" height="40" rx="6" class="soft"/><text x="320" y="85">レビュー</text>
    </g>
  </g>
  <path d="M200,112 V150" class="ln" marker-end="url(#arr)"/>
  <rect x="40" y="160" width="320" height="120" rx="10" class="hl" style="fill:#fff"/>
  <text x="200" y="190" class="ts hc" text-anchor="middle" font-weight="700">一つのチームに技能を揃える</text>
  <g class="tx" text-anchor="middle"><text x="200" y="222">設計・実装・テスト・レビュー</text><text x="200" y="250">顧客に届ける機能を最後まで作る</text></g>
  <g class="ts">
    <text x="420" y="110" font-weight="700">LeSS</text><text x="420" y="136" class="tx">cross-functional なフィーチャーチーム</text>
    <text x="420" y="196" font-weight="700">SAFe</text><text x="420" y="222" class="tx">cross-functional なチームと ART</text><text x="420" y="246" class="tx">ART は value stream に沿って組む</text>
  </g>
  <text x="440" y="336" class="ts sub" text-anchor="middle">英文は LeSS「Feature Teams」、SAFe「Agile Teams」「Agile Release Train」（2026-11-08 参照）</text>
</svg>
```

大規模開発の枠組みのうち LeSS と SAFe は、チームを職能で分けません。どちらも、作るのに要る技能を一つのチームに揃えます。

出典: LeSS「Feature Teams」、SAFe「Agile Teams」「Agile Release Train」。この本で原文に当たった。ART は SAFe の、チームを束ねた単位。

## LeSS が減らしたのも渡し直し

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="380" height="220" rx="10" class="box"/>
  <text x="230" y="94" class="t" text-anchor="middle" font-weight="700">一つの専門に寄せたチーム</text>
  <g class="tx" text-anchor="middle">
    <rect x="70" y="140" width="80" height="40" rx="4" class="soft"/><rect x="190" y="140" width="80" height="40" rx="4" class="soft"/><rect x="310" y="140" width="80" height="40" rx="4" class="soft"/>
  </g>
  <path d="M150,160 H188 M270,160 H308" class="xl" marker-end="url(#arr-x)"/>
  <text x="230" y="230" class="ts xc" text-anchor="middle">順に渡す・待つ・渡しが増える</text>
  <rect x="460" y="60" width="380" height="220" rx="10" class="hl" style="fill:#fff"/>
  <text x="650" y="94" class="t hc" text-anchor="middle" font-weight="700">フィーチャーチーム</text>
  <rect x="500" y="140" width="300" height="40" rx="4" class="soft"/>
  <text x="650" y="166" class="tx" text-anchor="middle">一つの機能を、一つのチームで最後まで</text>
  <text x="650" y="230" class="ts" text-anchor="middle">チームのあいだの渡しが減る</text>
  <text x="440" y="336" class="ts sub" text-anchor="middle">LeSS「Feature Teams」の対比を、この章の語で書いた</text>
</svg>
```

LeSS は、一つの専門や部品に寄せたチームは順に渡す開発を強め、渡しと待ちを増やすと書いています。LeSS が職能で分けないのも、渡し直しを減らすためです。

出典: LeSS「Feature Teams」の component team と feature team の対比。

## チームの中には職能が残る

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="200" y="50" width="480" height="230" rx="10" class="hl" style="fill:#fff"/>
  <text x="440" y="84" class="t hc" text-anchor="middle" font-weight="700">技能を揃えたチーム</text>
  <g class="ts" text-anchor="middle">
    <rect x="230" y="120" width="90" height="44" rx="6" class="h"/><text x="275" y="148" class="on">設計の人</text>
    <rect x="335" y="120" width="90" height="44" rx="6" class="h"/><text x="380" y="148" class="on">実装の人</text>
    <rect x="440" y="120" width="100" height="44" rx="6" class="h"/><text x="490" y="148" class="on">テストの人</text>
    <rect x="555" y="120" width="100" height="44" rx="6" class="h"/><text x="605" y="148" class="on">レビューの人</text>
  </g>
  <text x="440" y="220" class="ts" text-anchor="middle">人は、得意な職能を持ったまま一つのチームにいる</text>
  <text x="440" y="336" class="t" text-anchor="middle" font-weight="700">人間に職能ごとに覚えることが多いのは、変わらない</text>
</svg>
```

枠組みは、技能をチームの中に揃えました。チームの中では、人は今も得意な職能を持ちます。

出典: LeSS「Feature Teams」（people still specialize）。SAFe の all the skills も同じ形と読んだ。

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

人の役割を設計担当・実装担当のように Agent に割り当てる形は、職能の分業の写しです。枠組みがチームのあいだから外した切り方を、Agent のあいだに戻します。

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
