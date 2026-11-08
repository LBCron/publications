# 第 2 章　Cell は判断の責任者で数え、作り方では数えない

群: Cell の分割と自治

<!--
構造: agent-hub-roles-kaz/philosopher/2026-11-07-eaa-textbook-structure.md（55553ae4）。章題と群の札の字は writer-ja/drafts/eaa-toc/titles.md（d21b0d80、@ope-ultp1635 msg 65a67e15）で書き直した。構造は変えない。
出どころ（構造の表のまま）: core.md:16-18・28-29、development-model.md:30-41、delivery-guide.md:18-47。Core は publications origin/main 0d07f75 の core.md 版 6。
本文: @ope-ultp1635 msg 18751c19（群二）。
絵: Cell はどれも枠の外に対等に並べ、どの Cell もほかの Cell の枠の中に描かない（同 msg。core.md:43）。骨格にあった「（保留）子 Cell を親 Cell の枠の中に描くか」は、描かないで閉じた。
development-model.md:30-41 のうち 33 行（「外部には一つの責任主体、内部には複数Cell」）は包含の字なので使っていない（同 msg）。表の残りの行（31・32・34）と 36-41 行だけを使った。
「Cell の数え方」は、core.md:28 の Cell の定義（責任・権限・実行能力）と、development-model.md:37（Task を Agent へ配るだけでは分割にならない）から読んだ。数えるのが判断の責任者だと Core が一文で言っている行は無い。「Agent に配っても Cell は増えない」の注に書いた。
Local Delivery Model の表は Delivery Guide の「例」で、規範ではない。p.4 の注に書いた。中の作り方の名前は Delivery Guide のまま。
④（@ope-ultp1635 msg 02ab9595、@reviewer 2026-11-08 ch10-12 1-3）: delivery-guide.md:20「各 Domain は」を「業務ごとに」と書いていたのを「Cell ごとに」に直した。内部方式を決める単位は core.md:62 で Cell、core.md:50 で一つの Cell が複数 Profile を担うので、業務と Cell は 1 対 1 ではない。表の Domain 名は日本語にし、Cell の枠に業務の名前として「Contract」が残らないようにした（「契約」。第 3 章の Domain Profile の例と同じ字）。delivery-guide.md:35 の「Escalation できる」は「上げられる」と書いていたのを、core.md:70 の字（明示し、正当な判断主体との調整へ戻す）に直した。core.md:70 は向きを持たず、core.md:63 は親 Cell も上書きしないとするので、「上げる」は第 4 章と逆の形になる。
新しく引く外部の文献は無い（Scrum・Kanban・SAFe ART は名前を挙げるだけで、記述を引いていない）。
-->

> Federation は Cell の内部方式を指定しない。AA で動く Cell も、Scrum のチームも、委託先の標準工程も同じ形でつながり、全責務を一つの AA が担う構成は Cell が一つの EAA である。

```svg
<svg viewBox="0 0 880 300" width="880" height="300">
  <rect x="30" y="40" width="230" height="150" rx="10" class="box"/><text x="145" y="72" class="t" text-anchor="middle" font-weight="700">Cell</text>
  <rect x="110" y="88" width="70" height="32" rx="6" class="h"/><text x="145" y="110" class="tx" text-anchor="middle" style="fill:#fff">責任者</text>
  <rect x="70" y="134" width="150" height="34" rx="17" class="a"/><text x="145" y="157" class="ts on" text-anchor="middle">AA で動く</text>
  <rect x="325" y="40" width="230" height="150" rx="10" class="box"/><text x="440" y="72" class="t" text-anchor="middle" font-weight="700">Cell</text>
  <rect x="405" y="88" width="70" height="32" rx="6" class="h"/><text x="440" y="110" class="tx" text-anchor="middle" style="fill:#fff">責任者</text>
  <g class="h"><rect x="378" y="134" width="34" height="34" rx="6"/><rect x="423" y="134" width="34" height="34" rx="6"/><rect x="468" y="134" width="34" height="34" rx="6"/></g>
  <rect x="620" y="40" width="230" height="150" rx="10" class="box"/><text x="735" y="72" class="t" text-anchor="middle" font-weight="700">Cell</text>
  <rect x="700" y="88" width="70" height="32" rx="6" class="h"/><text x="735" y="110" class="tx" text-anchor="middle" style="fill:#fff">責任者</text>
  <path d="M660,152 H812" class="ln" marker-end="url(#arr)"/><g class="tx"><text x="668" y="144">要件</text><text x="718" y="144">設計</text><text x="768" y="144">試験</text></g>
  <path d="M260,115 H325 M555,115 H620" class="hl"/>
  <use href="#i-pr" x="282" y="128" width="20" height="26"/><use href="#i-pr" x="578" y="128" width="20" height="26"/>
  <text x="145" y="214" class="ts" text-anchor="middle">AA</text><text x="440" y="214" class="ts" text-anchor="middle">Scrum のチーム</text><text x="735" y="214" class="ts" text-anchor="middle">委託先の標準工程</text>
  <text x="440" y="262" class="t" text-anchor="middle" font-weight="700">中の作り方は違っても、同じ形で横に並んでつながる</text>
</svg>
```

Cell は、判断の責任者ごとに数えます。中が AA でも、人のチームでも、委託先の工程でも、つながり方は変わりません。

## Cell は責任・権限・実行能力の単位

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="250" y="40" width="380" height="250" rx="12" class="box"/>
  <text x="440" y="76" class="t" text-anchor="middle" font-weight="700">Cell</text>
  <rect x="280" y="100" width="100" height="56" rx="6" class="h"/><text x="330" y="134" class="ts on" text-anchor="middle">責任</text>
  <rect x="390" y="100" width="100" height="56" rx="6" class="h"/><text x="440" y="134" class="ts on" text-anchor="middle">権限</text>
  <rect x="500" y="100" width="100" height="56" rx="6" class="a"/><text x="550" y="134" class="ts on" text-anchor="middle">実行能力</text>
  <text x="440" y="196" class="ts" text-anchor="middle">一定の目的に対して、これを持つ</text>
  <rect x="320" y="222" width="240" height="44" rx="6" class="soft"/><text x="440" y="250" class="ts" text-anchor="middle">自律して成果を出す</text>
  <rect x="40" y="200" width="150" height="70" rx="3" class="hl" style="fill:#fff"/><text x="115" y="230" class="ts hc" text-anchor="middle">外との合意</text><text x="115" y="254" class="tx" text-anchor="middle">これに基づいて</text>
  <path d="M190,236 H246" class="ln" marker-end="url(#arr)"/>
  <text x="440" y="340" class="ts sub" text-anchor="middle">責任・権限・実行能力のどれかが欠けると、自律して成果を出せない</text>
</svg>
```

Cell は、一定の目的に対する責任・権限・実行能力を持ち、外との合意に基づいて自律して成果を出す単位です。

出典: EAA Core 版 6 の概念表「Cell」。

## Federation は中を指定しない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="70" width="220" height="200" rx="10" class="box"/><text x="150" y="104" class="t" text-anchor="middle" font-weight="700">Cell</text>
  <rect x="620" y="70" width="220" height="200" rx="10" class="box"/><text x="730" y="104" class="t" text-anchor="middle" font-weight="700">Cell</text>
  <rect x="70" y="130" width="160" height="110" rx="6" fill="url(#hatch)"/><text x="150" y="190" class="ts sub" text-anchor="middle">中の方式</text>
  <rect x="650" y="130" width="160" height="110" rx="6" fill="url(#hatch)"/><text x="730" y="190" class="ts sub" text-anchor="middle">中の方式</text>
  <use href="#i-no" x="218" y="120" width="22" height="22"/><use href="#i-no" x="798" y="120" width="22" height="22"/>
  <rect x="320" y="60" width="240" height="220" rx="6" class="hl" style="fill:#fff"/>
  <text x="440" y="90" class="ts hc" text-anchor="middle" font-weight="700">共有する文書でつなぐ</text>
  <g class="ts" text-anchor="middle"><text x="440" y="130">責任</text><text x="440" y="164">権限</text><text x="440" y="198">合意</text><text x="440" y="232" font-weight="700">Evidence</text></g>
  <path d="M260,170 H316 M564,170 H620" class="ln"/>
  <text x="440" y="330" class="t" text-anchor="middle" font-weight="700">相手の中の方式を、接続の条件にしない</text>
</svg>
```

Cell どうしは互いの中の方式を指定せず、共有する文書を通して責任・権限・合意・Evidence をつなぎます。この関係を Federation と呼びます。

出典: EAA Core 版 6 の概念表「Federation」、同「0. 目的と範囲」。

## 中の作り方は Cell ごとに選ぶ

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <g class="ts">
    <rect x="40" y="30" width="250" height="90" rx="10" class="box"/><text x="60" y="64" font-weight="700">連携の Cell</text><text x="60" y="94" class="ac">Full Agentic</text>
    <rect x="315" y="30" width="250" height="90" rx="10" class="box"/><text x="335" y="64" font-weight="700">契約の Cell</text><text x="335" y="94">Scrum + Coding Agent</text>
    <rect x="590" y="30" width="250" height="90" rx="10" class="box"/><text x="610" y="64" font-weight="700">請求の Cell</text><text x="610" y="94">Kanban + Agent</text>
    <rect x="40" y="140" width="250" height="90" rx="10" class="box"/><text x="60" y="174" font-weight="700">旧マスタの Cell</text><text x="60" y="204" class="hc">Predictive / Vendor</text>
    <rect x="315" y="140" width="250" height="90" rx="10" class="box"/><text x="335" y="174" font-weight="700">パッケージの Cell</text><text x="335" y="204">Package implementation</text>
    <rect x="590" y="140" width="250" height="90" rx="10" class="box"/><text x="610" y="174" font-weight="700">大規模製品の Cell</text><text x="610" y="204">SAFe ART</text>
  </g>
  <path d="M290,75 H315 M565,75 H590 M290,185 H315 M565,185 H590 M165,120 V140 M440,120 V140 M715,120 V140" class="hl"/>
  <text x="440" y="282" class="t" text-anchor="middle" font-weight="700">Cell ごとに、中の作り方が違ってよい</text>
  <text x="440" y="316" class="ts sub" text-anchor="middle">各枠の上は Cell が担う業務、下はその Cell の中の作り方</text>
</svg>
```

Cell ごとに、中の作り方は違ってかまいません。全部を Agent に任せる Cell の横に、委託先が従来の工程で作る Cell が並んでも、つながれます。

出典: EAA Delivery Guide「3.」の表（適用例）。原文の Domain を Cell と書いた（単位は Core 版 6「2. 自治と権限」）。Contract は「契約」と書いた。

## 揃えるのは外とのつながり方

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="230" height="250" rx="10" class="box"/><text x="155" y="96" class="t" text-anchor="middle" font-weight="700">Cell</text>
  <rect x="70" y="120" width="170" height="160" rx="6" fill="url(#hatch)"/><text x="155" y="206" class="ts sub" text-anchor="middle">中は揃えない</text>
  <path d="M270,185 H326" class="ln" marker-end="url(#arr)"/>
  <rect x="330" y="40" width="510" height="290" rx="6" class="hl" style="fill:#fff"/>
  <text x="360" y="74" class="ts hc" font-weight="700">どの Cell も最低限できること</text>
  <g class="t"><text x="380" y="118">Mission を受け取る</text><text x="380" y="160">Ontology と Contract を読む</text><text x="380" y="202">与えられた権限を越えない</text><text x="380" y="244" font-weight="700">Evidence を返す</text><text x="380" y="286">判断できない問題を示し、調整に戻せる</text></g>
  <g><use href="#i-ok" x="346" y="100" width="22" height="22"/><use href="#i-ok" x="346" y="142" width="22" height="22"/><use href="#i-ok" x="346" y="184" width="22" height="22"/><use href="#i-ok" x="346" y="226" width="22" height="22"/><use href="#i-ok" x="346" y="268" width="22" height="22"/></g>
</svg>
```

EAA が揃えるのは、中の作り方ではなく外とのつながり方です。絵に並べたことを、中がどう作られていても、どの Cell にもできるようにします。

出典: EAA Delivery Guide「3.」。「Escalation できる」は、向きを持たない Core 版 6「2. 自治と権限」の字（正当な判断主体との調整へ戻す）で書いた。

## 全部を担う AA は、Cell が一つの EAA

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="300" height="230" rx="10" class="box"/><text x="190" y="96" class="t" text-anchor="middle" font-weight="700">Cell</text>
  <rect x="150" y="112" width="80" height="40" rx="6" class="h"/><text x="190" y="138" class="ts on" text-anchor="middle">責任者</text>
  <rect x="80" y="176" width="220" height="44" rx="22" class="a"/><text x="190" y="204" class="ts on" text-anchor="middle">AA が全責務を担う</text>
  <text x="190" y="262" class="ts sub" text-anchor="middle">これだけで開発は進む</text>
  <path d="M370,175 H450" class="ln" marker-end="url(#arr)"/><text x="410" y="164" class="tx" text-anchor="middle">分けると</text>
  <rect x="470" y="60" width="170" height="230" rx="10" class="box"/><text x="555" y="96" class="t" text-anchor="middle" font-weight="700">Cell</text>
  <rect x="670" y="60" width="170" height="230" rx="10" class="box"/><text x="755" y="96" class="t" text-anchor="middle" font-weight="700">Cell</text>
  <rect x="515" y="112" width="80" height="40" rx="6" class="h"/><text x="555" y="138" class="ts on" text-anchor="middle">責任者</text>
  <rect x="715" y="112" width="80" height="40" rx="6" class="h"/><text x="755" y="138" class="ts on" text-anchor="middle">責任者</text>
  <rect x="495" y="176" width="120" height="44" rx="22" class="a"/><text x="555" y="204" class="ts on" text-anchor="middle">AA</text>
  <rect x="695" y="176" width="120" height="44" rx="22" class="a"/><text x="755" y="204" class="ts on" text-anchor="middle">AA</text>
  <path d="M640,175 H670" class="hl"/>
  <text x="655" y="316" class="ts sub" text-anchor="middle">どちらの AA も、同じ AA</text>
  <text x="440" y="356" class="t" text-anchor="middle" font-weight="700">AA の原則は、分けても書き直さない</text>
</svg>
```

一つの AA が全責務を担う構成は、Cell が一つの EAA です。分けた後の各 Cell を担う AA も、同じ AA です。分けても AA の原則は書き直しません。

出典: EAA Core 版 6「0. 目的と範囲」、EAA 考え方と開発の姿「3. 分割しても開発原則は変わらない」。

## Agent に配っても Cell は増えない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="40" width="380" height="250" rx="10" class="box"/><text x="230" y="76" class="t" text-anchor="middle" font-weight="700">Cell は一つ</text>
  <rect x="190" y="94" width="80" height="40" rx="6" class="h"/><text x="230" y="120" class="ts on" text-anchor="middle">責任者</text>
  <g class="a"><rect x="66" y="180" width="56" height="40" rx="20"/><rect x="132" y="180" width="56" height="40" rx="20"/><rect x="198" y="180" width="56" height="40" rx="20"/><rect x="264" y="180" width="56" height="40" rx="20"/><rect x="330" y="180" width="56" height="40" rx="20"/></g>
  <path d="M230,134 V160 M94,160 H358 M94,160 V178 M160,160 V178 M226,160 V178 M292,160 V178 M358,160 V178" class="ln"/>
  <text x="230" y="250" class="ts sub" text-anchor="middle">Task を何体もの Agent に配った</text>
  <rect x="470" y="40" width="170" height="250" rx="10" class="box"/><text x="555" y="76" class="t" text-anchor="middle" font-weight="700">Cell</text>
  <rect x="670" y="40" width="170" height="250" rx="10" class="box"/><text x="755" y="76" class="t" text-anchor="middle" font-weight="700">Cell</text>
  <rect x="515" y="94" width="80" height="40" rx="6" class="h"/><text x="555" y="120" class="ts on" text-anchor="middle">責任者</text>
  <rect x="715" y="94" width="80" height="40" rx="6" class="h"/><text x="755" y="120" class="ts on" text-anchor="middle">責任者</text>
  <rect x="527" y="180" width="56" height="40" rx="20" class="a"/><rect x="727" y="180" width="56" height="40" rx="20" class="a"/>
  <path d="M640,114 H670" class="hl"/>
  <text x="655" y="316" class="ts sub" text-anchor="middle">判断を別の責任者に渡した</text>
  <text x="440" y="356" class="t" text-anchor="middle" font-weight="700">Cell の数は、判断の責任者の数</text>
</svg>
```

一人の責任者が Task を何体の Agent に配っても、Cell は一つのままです。Cell が増えるのは、判断を別の責任者に渡したときです。

出典: EAA 考え方と開発の姿「3.」。※「Cell の数は判断の責任者の数」は、この行と Core の Cell の定義からの読みで、Core の規定ではない。

## つないでも、相手は AA にならない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="260" height="220" rx="10" class="box"/><text x="170" y="96" class="t" text-anchor="middle" font-weight="700">Cell</text>
  <rect x="70" y="120" width="200" height="44" rx="22" class="a"/><text x="170" y="148" class="ts on" text-anchor="middle">AA で動く</text>
  <rect x="580" y="60" width="260" height="220" rx="10" class="box"/><text x="710" y="96" class="t" text-anchor="middle" font-weight="700">Cell</text>
  <g class="h"><rect x="620" y="120" width="50" height="44" rx="6"/><rect x="685" y="120" width="50" height="44" rx="6"/><rect x="750" y="120" width="50" height="44" rx="6"/></g>
  <text x="710" y="200" class="ts" text-anchor="middle">既存の人のチーム</text>
  <text x="710" y="226" class="ts sub" text-anchor="middle">Agent を使わない</text>
  <path d="M300,170 H580" class="hl"/><use href="#i-pr" x="428" y="138" width="24" height="30"/><text x="440" y="196" class="ts" text-anchor="middle">Evidence</text>
  <rect x="330" y="216" width="220" height="44" rx="6" class="soft"/><text x="440" y="244" class="ts" text-anchor="middle">内部方式の異なる Cell の Federation</text>
  <text x="710" y="262" class="tx" text-anchor="middle">つないでも、AA にはならない</text>
  <text x="440" y="330" class="t" text-anchor="middle" font-weight="700">相手が Agent を使うかを、つなぐ条件にしない</text>
</svg>
```

AA の Cell と既存のチームは、内部方式の異なる Cell としてつながります。相手が Agent を使うかは条件にせず、つないでも相手の中は AA になりません。

出典: EAA 考え方と開発の姿「3. 分割しても開発原則は変わらない」の表と本文。
