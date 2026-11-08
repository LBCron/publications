# 第 3 章　責務を先に Profile に書き、Cell は判断の権限を別の責任主体に渡して分ける

群: Cell の分割と自治

<!--
構造: agent-hub-roles-kaz/philosopher/2026-11-07-eaa-textbook-structure.md（55553ae4）。章題と群の札の字は writer-ja/drafts/eaa-toc/titles.md（d21b0d80、@ope-ultp1635 msg 65a67e15）で書き直した。構造は変えない。
出どころ（構造の表のまま）: core.md:47-49、profiles.md 1〜5 節・9 節、development-model.md:18-27、role-model.md:56-63。Core は publications origin/main 0d07f75 の core.md 版 6。
core.md は 49 行に続く 50 行（一つの Cell が複数 Profile を担ってよい・記述だけで権限は発生しない）も使った。リードの字がこの行による。
本文: @ope-ultp1635 msg 18751c19（群二）。
絵: Cell はどれも枠の外に対等に並べ、どの Cell もほかの Cell の枠の中に描かない（同 msg。core.md:43）。
development-model.md:18-27 のうち 24・25 行（Enterprise／Domain は全体と部分という位置の呼び名、同じ Cell が全体として子 Cell を持つ）は包含の字なので使っていない（25 行は同 msg で名指し、24 行は同じ字の組なので合わせて外した）。
「サービスの数から Cell の数を決めず」は working-notes.md:19 による（同ファイルの 13 行ではない）。p.「Profile やサービスの数で決めない」の注に書いた。⑥ でリードからは外した。
判断の責任者を Role Model は Operator（Ope）と呼ぶ。Role Model は適用例で規範ではない。p.「分けるのは、判断を渡すとき」の注に書いた。
新しく引く外部の文献は無い。
⑤（@ope-ultp1635 msg 281e5366、@reviewer 3 回目・4 回目）: p.「Profile は責務の版付きの仕様」の出典欄の「まだ決まっていない」を、未確定としているのは Profiles（profiles.md:5・135）だと書き直した。
⑥（@ope-ultp1635 msg 6fc17eeb、@reviewer 2〜4 回目）: 章題・章の概要の絵の「判断を渡すときだけ分ける」の「だけ」は Core に無く、出どころは Delivery Guide・Role Model（適用例）で、第 0 章の「Core に無い決まりを足さない」とぶつかっていた。章題は core.md:52 の定義（分割は責務と判断権限を別の責任主体へ渡すこと）の字にし、「だけ」を落とした（titles.md に記録）。リードの「Profile やサービスの数から決めず、負荷が増えて渡すときに分ける」は適用例だと書いた。p.「Profile やサービスの数で決めない」の出典に（適用例）を足し、Core が決めている範囲（core.md:50）を書いた。
-->

> Profile は組織図より先に書く。一つの Cell が複数の Profile を担ってよい。いつ分けるかは、適用例が、判断の負荷が続けて増えて別の Operator に渡すときとしている。

```svg
<svg viewBox="0 0 880 300" width="880" height="300">
  <g class="ts" text-anchor="middle">
    <rect x="60" y="20" width="160" height="50" rx="3" class="hl" style="fill:#fff"/><text x="140" y="51" class="hc">Platform</text>
    <rect x="260" y="20" width="160" height="50" rx="3" class="hl" style="fill:#fff"/><text x="340" y="51" class="hc">契約</text>
    <rect x="460" y="20" width="160" height="50" rx="3" class="hl" style="fill:#fff"/><text x="540" y="51" class="hc">受注</text>
    <rect x="660" y="20" width="160" height="50" rx="3" class="hl" style="fill:#fff"/><text x="740" y="51" class="hc">請求</text>
  </g>
  <rect x="40" y="120" width="600" height="110" rx="10" class="box"/><text x="80" y="150" class="ts" font-weight="700">Cell</text>
  <rect x="300" y="138" width="80" height="36" rx="6" class="h"/><text x="340" y="162" class="ts on" text-anchor="middle">責任者</text>
  <rect x="660" y="120" width="180" height="110" rx="10" class="box"/><text x="750" y="142" class="ts" text-anchor="middle" font-weight="700">Cell</text>
  <rect x="710" y="152" width="80" height="32" rx="6" class="h"/><text x="750" y="174" class="ts on" text-anchor="middle">責任者</text>
  <path d="M140,70 V116" class="ln" marker-end="url(#arr)"/><path d="M340,70 V116" class="ln" marker-end="url(#arr)"/><path d="M540,70 V116" class="ln" marker-end="url(#arr)"/><path d="M740,70 V116" class="ln" marker-end="url(#arr)"/>
  <text x="340" y="206" class="tx" text-anchor="middle">一つの Cell が Platform・契約・受注を担う</text>
  <text x="750" y="206" class="tx" text-anchor="middle">判断を渡した所だけ分かれた</text>
  <text x="440" y="274" class="t" text-anchor="middle" font-weight="700">責務を先に書き、判断の権限を渡した所で Cell が分かれる</text>
</svg>
```

まず責務を Profile として書きます。それを担う Cell と判断の責任者を決めるのは、その後です。

出典: EAA Core 版 6「1. 責務と分割」。

## 組織を先に作ると、調整先が増える

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <path d="M440,20 V310" class="lt dash"/>
  <text x="220" y="44" class="t" text-anchor="middle" font-weight="700">能力が要るたびに組織を作る</text>
  <text x="660" y="44" class="t hc" text-anchor="middle" font-weight="700">責務を先に書く</text>
  <g class="box"><rect x="60" y="80" width="80" height="50" rx="6"/><rect x="180" y="80" width="80" height="50" rx="6"/><rect x="300" y="80" width="80" height="50" rx="6"/><rect x="60" y="200" width="80" height="50" rx="6"/><rect x="180" y="200" width="80" height="50" rx="6"/><rect x="300" y="200" width="80" height="50" rx="6"/></g>
  <path d="M140,105 H180 M260,105 H300 M140,225 H180 M260,225 H300 M100,130 V200 M220,130 V200 M340,130 V200 M140,130 L180,200 M260,130 L300,200 M180,130 L140,200 M300,130 L260,200" class="xl"/>
  <text x="220" y="290" class="ts xc" text-anchor="middle">組織が増えるたびに、調整先も増える</text>
  <g class="ts" text-anchor="middle">
    <rect x="490" y="80" width="100" height="40" rx="3" class="hl" style="fill:#fff"/><text x="540" y="106" class="hc">責務</text>
    <rect x="610" y="80" width="100" height="40" rx="3" class="hl" style="fill:#fff"/><text x="660" y="106" class="hc">責務</text>
    <rect x="730" y="80" width="100" height="40" rx="3" class="hl" style="fill:#fff"/><text x="780" y="106" class="hc">責務</text>
  </g>
  <path d="M660,124 V160" class="ln" marker-end="url(#arr)"/>
  <rect x="500" y="170" width="320" height="76" rx="6" class="soft"/>
  <text x="660" y="200" class="ts" text-anchor="middle">同じ Cell で担うか</text><text x="660" y="228" class="ts" text-anchor="middle">別の Cell へ移すかを選べる</text>
</svg>
```

専門の能力が要るたびに専用の組織を作ると、調整先も増えます。先に責務を書けば、同じ Cell で担うか、別の Cell へ移すかを選べます。

出典: EAA 考え方と開発の姿「2. 組織図より先に責務を置く」。

## Profile は責務の版付きの仕様

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="200" y="20" width="480" height="300" rx="4" class="hl" style="fill:#fff"/>
  <text x="230" y="56" class="t hc" font-weight="700">Profile</text><text x="650" y="56" class="t hc" text-anchor="end" font-weight="700">版 2</text>
  <path d="M220,72 H660" class="lt"/>
  <g class="ts"><text x="230" y="104">目的と、責任を負う範囲・負わない範囲</text><text x="230" y="140">業務上の意味と、参照する Ontology</text><text x="230" y="176">要る権限、守る制約と参照する規範</text><text x="230" y="212">提供する能力、依存先、外への保証と Contract</text><text x="230" y="248" class="hc" font-weight="700">成り立ったことを示す Evidence</text><text x="230" y="284">自分で判断できない条件</text></g>
  <text x="440" y="356" class="ts sub" text-anchor="middle">特定の担当者や Agent の製品は書かない</text>
</svg>
```

Profile は、Cell が引き受ける責務を定める版付きの仕様です。何を成り立たせ、どこまで自分で判断し、外に何を保証し、それをどう確かめるかを書きます。

出典: EAA Profiles「1.」「3. 責務定義と割当」。項目名・記法・必須の欄は、Profiles が詳細スキーマとして未確定にしている。

## Standard と Domain は同じ形

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="30" width="380" height="230" rx="10" class="soft"/>
  <text x="60" y="64" class="t" font-weight="700">Standard Profile</text><text x="60" y="92" class="tx">EAA が使い回せる責務として出す</text>
  <g class="ts"><text x="60" y="130">Platform　Portfolio　Supplier</text><text x="60" y="162">Assurance　Regulated</text><text x="60" y="194">Migration　Cutover</text></g>
  <rect x="460" y="30" width="380" height="230" rx="10" class="soft"/>
  <text x="480" y="64" class="t" font-weight="700">Domain Profile</text><text x="480" y="92" class="tx">業務の意味・不変条件・責任から定める</text>
  <g class="ts"><text x="480" y="130">契約　請求　受注</text></g>
  <rect x="200" y="290" width="480" height="56" rx="6" class="hl" style="fill:#fff"/>
  <text x="440" y="324" class="ts hc" text-anchor="middle">書く形は同じ。Cell の種類を分けるものではない</text>
</svg>
```

使い回せる責務は Standard Profile、業務に固有の責務は Domain Profile に書きます。形は同じで、Cell を二種類に分けるものではありません。

出典: EAA Profiles「2. Standard Profile と Domain Profile」。

## 書いただけでは、権限は生まれない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="200" height="140" rx="4" class="hl" style="fill:#fff"/><text x="140" y="96" class="t hc" text-anchor="middle" font-weight="700">Profile</text><text x="140" y="130" class="ts" text-anchor="middle">要る権限：</text><text x="140" y="156" class="ts" text-anchor="middle">本番の基盤を変える</text>
  <path d="M240,130 H330" class="ln" marker-end="url(#arr)"/><text x="285" y="118" class="tx" text-anchor="middle">引き受ける</text>
  <rect x="340" y="40" width="500" height="200" rx="10" class="box"/><text x="370" y="74" class="t" font-weight="700">Cell</text>
  <g class="ts">
    <rect x="370" y="100" width="140" height="44" rx="6" class="h"/><text x="440" y="128" class="on" text-anchor="middle">権限を得る</text>
    <rect x="525" y="100" width="140" height="44" rx="6" class="h"/><text x="595" y="128" class="on" text-anchor="middle">資源を得る</text>
    <rect x="680" y="100" width="140" height="44" rx="6" class="a"/><text x="750" y="128" class="on" text-anchor="middle">能力を持つ</text>
  </g>
  <text x="595" y="190" class="ts" text-anchor="middle">権限・資源・能力が揃って、引き受けたことになる</text>
  <use href="#i-no" x="128" y="236" width="24" height="24"/><text x="140" y="290" class="ts xc" text-anchor="middle">書いてあるから使える</text><text x="140" y="314" class="ts xc" text-anchor="middle">とはしない</text>
  <text x="595" y="300" class="ts sub" text-anchor="middle">書いた権限と、実際に与えられた権限を分けて扱う</text>
</svg>
```

Profile に権限を書いただけでは、その権限は生まれません。引き受けるときに、要る権限・資源・能力を実際に揃えます。

出典: EAA Core 版 6「1. 責務と分割」、EAA Profiles「3.」「4. ロード・合成・改訂・解除」。

## 一つの Cell が複数を担ってよい

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <g class="ts" text-anchor="middle">
    <rect x="120" y="30" width="180" height="50" rx="3" class="hl" style="fill:#fff"/><text x="210" y="61" class="hc">Platform</text>
    <rect x="350" y="30" width="180" height="50" rx="3" class="hl" style="fill:#fff"/><text x="440" y="61" class="hc">契約</text>
    <rect x="580" y="30" width="180" height="50" rx="3" class="hl" style="fill:#fff"/><text x="670" y="61" class="hc">請求</text>
  </g>
  <path d="M210,80 V142" class="ln" marker-end="url(#arr)"/><path d="M440,80 V142" class="ln" marker-end="url(#arr)"/><path d="M670,80 V142" class="ln" marker-end="url(#arr)"/>
  <rect x="100" y="146" width="680" height="90" rx="10" class="box"/><text x="130" y="178" class="ts" font-weight="700">Cell</text>
  <rect x="400" y="164" width="80" height="40" rx="6" class="h"/><text x="440" y="190" class="ts on" text-anchor="middle">責任者</text>
  <rect x="100" y="262" width="680" height="96" rx="6" class="soft"/>
  <text x="130" y="290" class="ts" font-weight="700">まとめて担うときに確かめること</text>
  <g class="ts"><text x="130" y="320">誰も持たない責任が無いか</text><text x="450" y="320">同じことを別々に決めていないか</text><text x="130" y="346">両立しない保証を出していないか</text></g>
</svg>
```

一つの Cell が複数の Profile を担ってかまいません。Profile 一つに Cell 一つとは求めません。まとめて担うときは、絵の下に並べたことを確かめます。

出典: EAA Core 版 6「1.」、EAA Profiles「4.」「5. 分離可能な責務」。

## Profile やサービスの数で決めない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <g opacity=".75">
    <text x="210" y="40" class="t" text-anchor="middle" font-weight="700">数から決める</text>
    <g class="lt" style="fill:#fff"><rect x="60" y="64" width="60" height="34" rx="3"/><rect x="130" y="64" width="60" height="34" rx="3"/><rect x="200" y="64" width="60" height="34" rx="3"/><rect x="270" y="64" width="60" height="34" rx="3"/></g>
    <text x="210" y="122" class="tx" text-anchor="middle">Profile やサービスの数だけ</text>
    <path d="M210,130 V158" class="ln" marker-end="url(#arr)"/>
    <g class="box"><rect x="60" y="166" width="60" height="50" rx="6"/><rect x="130" y="166" width="60" height="50" rx="6"/><rect x="200" y="166" width="60" height="50" rx="6"/><rect x="270" y="166" width="60" height="50" rx="6"/></g>
    <text x="210" y="240" class="tx" text-anchor="middle">同じ数の Cell を置く</text>
  </g>
  <use href="#i-no" x="320" y="26" width="24" height="24"/>
  <path d="M440,20 V260" class="lt dash"/>
  <text x="660" y="40" class="t hc" text-anchor="middle" font-weight="700">判断を渡すかで決める</text>
  <g class="hl" style="fill:#fff"><rect x="500" y="64" width="60" height="34" rx="3"/><rect x="570" y="64" width="60" height="34" rx="3"/><rect x="640" y="64" width="60" height="34" rx="3"/><rect x="740" y="64" width="60" height="34" rx="3"/></g>
  <path d="M600,98 V162" class="ln" marker-end="url(#arr)"/><path d="M770,98 V162" class="ln" marker-end="url(#arr)"/>
  <rect x="500" y="166" width="200" height="50" rx="6" class="box"/><rect x="730" y="166" width="80" height="50" rx="6" class="box"/>
  <text x="600" y="240" class="tx" text-anchor="middle">一人の責任者が担う</text><text x="770" y="240" class="tx" text-anchor="middle">別の責任者</text>
  <rect x="40" y="280" width="800" height="70" rx="10" class="lt" style="fill:#fff"/>
  <text x="440" y="322" class="t" text-anchor="middle" font-weight="700">Cell の数は、独立した判断の責任をいくつに分けるかで決まる</text>
</svg>
```

Profile の数からも、既存のサービスの数からも、Cell の数は決めません。決めるのは、独立した判断の責任をいくつに分けるかです。

出典: EAA Role Model「4.」（適用例）、EAA Profiles「5.」、EAA Working Notes 冒頭。Core が決めるのは一つの Cell が複数を担ってよいことまで。

## 分けるのは、判断を渡すとき

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="320" height="200" rx="10" class="box"/><text x="70" y="94" class="ts" font-weight="700">Cell</text>
  <rect x="160" y="80" width="80" height="40" rx="6" class="h"/><text x="200" y="106" class="ts on" text-anchor="middle">責任者</text>
  <g class="ts" text-anchor="middle"><rect x="70" y="150" width="120" height="40" rx="3" class="hl" style="fill:#fff"/><text x="130" y="176" class="hc">契約</text><rect x="210" y="150" width="120" height="40" rx="3" class="hl" style="fill:#fff"/><text x="270" y="176" class="hc">Platform</text></g>
  <use href="#i-wait" x="300" y="200" width="20" height="28"/><use href="#i-wait" x="324" y="200" width="20" height="28"/><use href="#i-wait" x="276" y="200" width="20" height="28"/>
  <text x="200" y="290" class="ts sub" text-anchor="middle">基盤の判断が続けて増える</text>
  <path d="M360,160 H500" class="ln" marker-end="url(#arr)"/><text x="430" y="148" class="tx" text-anchor="middle">判断を渡す</text>
  <rect x="520" y="60" width="320" height="200" rx="10" class="box"/><text x="550" y="94" class="ts" font-weight="700">Cell</text>
  <rect x="640" y="80" width="80" height="40" rx="6" class="h"/><text x="680" y="106" class="ts on" text-anchor="middle">責任者</text>
  <g class="ts" text-anchor="middle"><rect x="620" y="150" width="120" height="40" rx="3" class="hl" style="fill:#fff"/><text x="680" y="176" class="hc">Platform</text></g>
  <text x="680" y="290" class="ts sub" text-anchor="middle">別の責任者が自分で判断する</text>
  <text x="440" y="346" class="t" text-anchor="middle" font-weight="700">横に並ぶ、別の Cell になる</text>
</svg>
```

初めから全部の Profile を専用の Cell にはしません。判断の負荷が続けて増えたら、責務を別の責任者に渡し、その人が判断します。そこで Cell が分かれます。

出典: EAA Delivery Guide「4.」、EAA Role Model「4.」（適用例。責任者を Operator と呼ぶ）。分割が判断の権限を渡すことなのは Core「1.」の定義。

## 最初の Mission に要る範囲から書く

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="20" width="420" height="300" rx="4" class="hl" style="fill:#fff"/>
  <text x="70" y="56" class="t hc" font-weight="700">Billing Profile の例</text>
  <path d="M60,72 H440" class="lt"/>
  <g class="ts"><text x="70" y="106">請求・入金・返金が合っていること</text><text x="70" y="140">請求する主体の意味</text><text x="70" y="174">確定した請求の扱い</text><text x="70" y="208">契約の側との責任の境</text><text x="70" y="242" class="hc" font-weight="700">照合の Evidence</text></g>
  <rect x="60" y="262" width="380" height="40" rx="3" fill="url(#hatch)"/><text x="250" y="288" class="ts sub" text-anchor="middle">まだ書かない範囲</text>
  <path d="M460,170 H520" class="ln" marker-end="url(#arr)"/>
  <rect x="530" y="40" width="310" height="110" rx="10" class="box"/><text x="685" y="80" class="ts" text-anchor="middle">元の Cell が担う</text><text x="685" y="110" class="tx" text-anchor="middle">または</text>
  <rect x="530" y="180" width="310" height="110" rx="10" class="box"/><text x="685" y="220" class="ts" text-anchor="middle">別の責任者に移して</text><text x="685" y="248" class="ts" text-anchor="middle">Billing の Cell を作る</text>
  <text x="440" y="356" class="ts xc" text-anchor="middle">書いていない範囲を、黙って持っている権限として扱わない</text>
</svg>
```

全部の業務を初日から書きません。最初の Mission に要る範囲を書き、まだ決まっていない所を、黙って持っている権限にしません。誰が担うかは、書いた後に決めます。

出典: EAA Profiles「9. Domain Profile の定義」。
