# 第 9 章　新しい版を公開しても、各 Cell が採用するまで合意は変わらない

群: Evidence・Mission・Contract と版

<!--
構造: agent-hub-roles-kaz/philosopher/2026-11-07-eaa-textbook-structure.md（55553ae4）。章題と群の札の字は writer-ja/drafts/eaa-toc/titles.md（d21b0d80、@ope-ultp1635 msg 65a67e15）で書き直した。構造は変えない。
出どころ（構造の表のまま）: core.md:78-80・84-92、profiles.md 4 節・7 節、素材 3。Core は publications origin/main 0d07f75 の core.md 版 6。
本文: @ope-ultp1635 msg f202fb67（群三）。
リードの「変えたい側は提案する」は、骨格で題から外してリードに置いた主張（titles.md「短さと中身のどちらを取ったか」）。本文の 3〜9 ページ目（提案・例・承認・採用・判断する者・逆向き・どの向きでも）で受けた。
足した出どころ: core.md:93-94（採用は実装の受入権限だけでは判断できない・提起者は承認しない）、core.md:70（義務を一方的に捨てない）、core.md:11・71（未定の調整と、一方的な強制で補わない）。PR での実装例は delivery-guide.md:517-533（20. Profile改訂・採用 Pattern）と 115 行。素材 3 の例（希望時間帯・締めの時刻・採用の進み方の表）は、版 6 の 79・80・84・91・94 行に当て直した。
包含と同じ形の字として、profiles.md:62「EnterpriseがDomain Profileを提供する場合、Enterpriseが正本を管理する」と、profiles.md:107「EnterpriseのOntology」、development-model.md:45「DomainからEnterpriseへのOntology訂正」は使っていない（development-model.md:24 の Enterprise／Domain と同じ字の組）。提供側・引受側の表（profiles.md:65-68）は Enterprise の字を含まないので使った。
提起者が承認しないことの理由と、Core の採用の承認は第 10・11 章が言う。この章では手続きの順序の中で一度だけ触れ、先の章を指した。
絵: Cell はどれもほかの Cell の枠の外に並べる（core.md:43）。
新しく引く外部の文献は無い。
⑥（@ope-ultp1635 msg 6fc17eeb、@reviewer 2〜4 回目）: p.「承認して、新しい版を公開する」は、在庫の側が承認しない理由を「提起した者は承認しない」（core.md:94）にしていた。core.md:94 は人の単位の規定で、Cell の単位の分離ではない。在庫の側が承認しないのは、改訂を判断するのが所有者（core.md:90）で、所有者が物流の側にいる（core.md:98・第 8 章の例）から。理由をそちらに替え、core.md:94 は人の単位で満たしていることを注に書いた。第 1 章の「片側で書き換わる」の注と同じ取り違え。
⑤（@ope-ultp1635 msg 281e5366、@reviewer 3 回目・4 回目）: 最後のページの見出しを「詳しい手順が未定のこと」にし、各項目が core.md:11 の既知の不足であることを書いた。以前は見出しが「決めていないこと」で、扱い全体が未決に読めた（緊急時・合意不成立には core.md:71・101・102 の字がある）。
-->

> 変えたい側は提案し、受け入れるかは対象の Cell が決める。親子・兄弟・横断のどの向きでも同じ手続きで、基盤を担う Cell も CI/CD の変更を PR で提案する。

```svg
<svg viewBox="0 0 880 300" width="880" height="300">
  <path d="M120,236 H840" class="ln" marker-end="url(#arr)"/><text x="840" y="260" class="tx" text-anchor="end">時間</text>
  <text x="70" y="96" class="ts" text-anchor="middle" font-weight="700">在庫</text><text x="70" y="176" class="ts" text-anchor="middle" font-weight="700">物流</text>
  <rect x="120" y="74" width="300" height="40" rx="3" class="lt" style="fill:#fff"/><text x="270" y="100" class="ts" text-anchor="middle">版 1</text>
  <rect x="420" y="74" width="420" height="40" rx="3" class="hl" style="fill:#fff"/><text x="630" y="100" class="ts hc" text-anchor="middle">版 2 を採用</text>
  <rect x="120" y="154" width="520" height="40" rx="3" class="lt" style="fill:#fff"/><text x="380" y="180" class="ts" text-anchor="middle">版 1</text>
  <rect x="640" y="154" width="200" height="40" rx="3" class="hl" style="fill:#fff"/><text x="740" y="180" class="ts hc" text-anchor="middle">版 2 を採用</text>
  <path d="M260,40 V220" class="lt dash"/><text x="260" y="32" class="tx" text-anchor="middle">版 2 を公開</text>
  <path d="M640,40 V220" class="ln"/><text x="640" y="32" class="ts okc" text-anchor="middle">ここで版 2 に移る</text>
  <text x="450" y="284" class="t" text-anchor="middle" font-weight="700">公開から移行までのあいだ、効いているのは版 1</text>
</svg>
```

新しい版を公開することと、各 Cell が採用することは別の行為です。結ぶ Cell が全部採用するまで、いま効いている合意は変わりません。

## 公開と採用は、別の行為

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="360" height="220" rx="10" class="soft"/>
  <text x="220" y="100" class="t" text-anchor="middle" font-weight="700">公開する</text>
  <text x="220" y="140" class="ts" text-anchor="middle">規範の所有者が、新しい版を出す</text>
  <text x="220" y="200" class="ts sub" text-anchor="middle">これだけでは、どの Cell の</text><text x="220" y="226" class="ts sub" text-anchor="middle">義務も変わらない</text>
  <rect x="480" y="60" width="360" height="220" rx="10" class="soft"/>
  <text x="660" y="100" class="t" text-anchor="middle" font-weight="700">採用する</text>
  <text x="660" y="140" class="ts" text-anchor="middle">各 Cell が、その版に従うと決める</text>
  <text x="660" y="200" class="ts sub" text-anchor="middle">自動では追随しない</text>
  <path d="M400,170 H476" class="ln" marker-end="url(#arr)"/><text x="440" y="160" class="tx" text-anchor="middle">別の時点</text>
</svg>
```

規範の新しい版を公開することと、各 Cell がそれを採用することは別の行為で、採用は自動では追随しません。採用中の合意は、移行が成り立つまで効きます。

出典: EAA Core 版 6「3. 意味と合意」。

## 採用の進み方と、効いている版

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <g class="ts">
    <text x="60" y="54" font-weight="700">できごと</text><text x="520" y="54" font-weight="700" text-anchor="middle">在庫が採用中</text><text x="650" y="54" font-weight="700" text-anchor="middle">物流が採用中</text><text x="780" y="54" font-weight="700" text-anchor="middle">効いている版</text>
    <text x="60" y="104">両方が版 1 を採用する</text><text x="520" y="104" text-anchor="middle">1</text><text x="650" y="104" text-anchor="middle">1</text><text x="780" y="104" text-anchor="middle">1（成立）</text>
    <text x="60" y="164">所有者が版 2 を公開する</text><text x="520" y="164" text-anchor="middle">1</text><text x="650" y="164" text-anchor="middle">1</text><text x="780" y="164" text-anchor="middle">1</text>
    <text x="60" y="224">在庫が版 2 を採用する</text><text x="520" y="224" text-anchor="middle" class="hc" font-weight="700">2</text><text x="650" y="224" text-anchor="middle">1</text><text x="780" y="224" text-anchor="middle" font-weight="700">1</text>
    <text x="60" y="284">物流が版 2 を採用する</text><text x="520" y="284" text-anchor="middle" class="hc" font-weight="700">2</text><text x="650" y="284" text-anchor="middle" class="hc" font-weight="700">2</text><text x="780" y="284" text-anchor="middle" class="okc" font-weight="700">2（移行）</text>
  </g>
  <path d="M40,72 H840 M40,132 H840 M40,192 H840 M40,252 H840" class="lt"/>
  <text x="440" y="342" class="ts sub" text-anchor="middle">3 行目、在庫は版 2 を採用しているが、効いているのは版 1</text>
</svg>
```

在庫が版 2 を採用しても、物流が採用するまでは版 1 が効いています。在庫は、物流に版 2 に従えとは言えません。物流が採用しなければ、版 1 のままです。

出典: EAA Core 版 6「3. 意味と合意」。※ 表は EAA 紹介 3 のもので、版の番号は説明のための仮定です。

## 変えたい側は、提案する

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="260" height="220" rx="10" class="box"/><text x="170" y="96" class="t" text-anchor="middle" font-weight="700">提案する Cell</text>
  <g class="ts"><text x="80" y="150">内容</text><text x="80" y="186">理由</text><text x="80" y="222">根拠</text></g>
  <path d="M300,170 H536" class="ln" marker-end="url(#arr)"/><use href="#i-pr" x="405" y="128" width="30" height="38"/><text x="420" y="196" class="ts" text-anchor="middle">提案</text>
  <rect x="540" y="60" width="300" height="220" rx="10" class="box"/><text x="690" y="96" class="t" text-anchor="middle" font-weight="700">対象の Cell</text>
  <text x="690" y="132" class="ts" text-anchor="middle">検証して、どれかに決める</text>
  <g class="ts" text-anchor="middle"><rect x="570" y="150" width="240" height="32" rx="3" class="lt" style="fill:#fff"/><text x="690" y="172">受け入れる</text><rect x="570" y="190" width="240" height="32" rx="3" class="lt" style="fill:#fff"/><text x="690" y="212">直してもらう</text><rect x="570" y="230" width="240" height="32" rx="3" class="lt" style="fill:#fff"/><text x="690" y="252">受け入れない</text></g>
</svg>
```

Cell のあいだの変更は、提案する側が内容・理由・根拠を示します。対象の Cell が検証して、受け入れる・直してもらう・受け入れない、のどれかに決めます。

出典: EAA Core 版 6「4. 提案と変更」。

## 例：出荷指示に希望時間帯を足したい

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="260" height="220" rx="10" class="box"/><text x="170" y="96" class="t" text-anchor="middle" font-weight="700">在庫の Cell</text>
  <rect x="580" y="60" width="260" height="220" rx="10" class="box"/><text x="710" y="96" class="t" text-anchor="middle" font-weight="700">物流の Cell</text>
  <rect x="650" y="116" width="120" height="40" rx="6" class="h"/><text x="710" y="142" class="ts on" text-anchor="middle">所有者</text>
  <path d="M300,140 H646" class="ln" marker-end="url(#arr)"/><use href="#i-pr" x="425" y="98" width="30" height="38"/>
  <rect x="60" y="300" width="760" height="60" rx="10" class="soft"/>
  <g class="ts"><text x="80" y="326">内容：出荷指示に、配送の希望時間帯の欄を足したい</text><text x="80" y="350">理由・根拠：店舗からの要望が増えている</text></g>
  <text x="710" y="200" class="ts" text-anchor="middle">検証して決める</text>
</svg>
```

在庫の Cell が、出荷指示に希望時間帯の欄を足したいと、Contract の所有者に提案します。内容と理由・根拠を付け、所有者が検証して決めます。

※ 例は EAA 紹介 3 の、説明のための仮定です。出典: EAA Core 版 6「4. 提案と変更」。

## 承認して、新しい版を公開する

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="300" height="200" rx="10" class="box"/><text x="190" y="96" class="t" text-anchor="middle" font-weight="700">在庫の Cell</text>
  <text x="190" y="150" class="ts" text-anchor="middle">改訂を提起した</text>
  <use href="#i-no" x="176" y="172" width="28" height="28"/><text x="190" y="226" class="ts xc" text-anchor="middle">所有者がいないので承認しない</text>
  <rect x="540" y="60" width="300" height="200" rx="10" class="box"/><text x="690" y="96" class="t" text-anchor="middle" font-weight="700">物流の Cell</text>
  <rect x="630" y="116" width="120" height="40" rx="6" class="h"/><text x="690" y="142" class="ts on" text-anchor="middle">所有者</text>
  <use href="#i-ok" x="676" y="172" width="28" height="28"/><text x="690" y="226" class="ts okc" text-anchor="middle">承認して版 2 を公開</text>
  <text x="440" y="320" class="t" text-anchor="middle" font-weight="700">承認するのは Contract の所有者で、物流の側にいる</text>
</svg>
```

所有者が承認すると、版 2 が公開されます。承認する所有者は、この例では物流の側にいます。在庫の側が承認しないのは、在庫の側に所有者がいないからです。

出典: EAA Core 版 6「4.」、規定は第 10 章。※「提起した者は承認しない」は人の単位の決まりで、Cell の単位ではない。この例では提起した人と所有者が別の人。

## 採用するかは、各 Cell が決める

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="300" y="30" width="280" height="60" rx="3" class="hl" style="fill:#fff"/><text x="440" y="66" class="ts hc" text-anchor="middle" font-weight="700">Contract　版 2（公開済み）</text>
  <rect x="40" y="130" width="340" height="190" rx="10" class="box"/><text x="210" y="166" class="t" text-anchor="middle" font-weight="700">在庫の Cell</text>
  <text x="210" y="216" class="ts" text-anchor="middle">在庫の規範の所有者が、</text><text x="210" y="242" class="ts" text-anchor="middle">採用するかを決める</text>
  <rect x="500" y="130" width="340" height="190" rx="10" class="box"/><text x="670" y="166" class="t" text-anchor="middle" font-weight="700">物流の Cell</text>
  <text x="670" y="216" class="ts" text-anchor="middle">物流の規範の所有者が、</text><text x="670" y="242" class="ts" text-anchor="middle">採用するかを決める</text>
  <text x="670" y="290" class="tx" text-anchor="middle">Contract の所有者がいる側も、自動では従わない</text>
  <path d="M380,94 L300,130 M500,94 L580,130" class="lt"/>
</svg>
```

在庫も物流も、それぞれの規範の所有者が、版 2 を採用するかを決めます。Contract の所有者がいる物流の側も、自分の所有者が出した版に自動では従いません。

出典: EAA Core 版 6「3. 意味と合意」「4. 提案と変更」。

## 何を、誰が判断するか

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <g class="ts">
    <text x="60" y="60" font-weight="700">対象</text><text x="400" y="60" font-weight="700">判断する者</text>
    <text x="60" y="120">実装・設定の変更</text><text x="400" y="120">対象の Cell の規範と権限で定めた受入の担当</text>
    <text x="60" y="180">規範の改訂</text><text x="400" y="180">その規範の正当な所有者</text>
    <text x="60" y="240">規範の新しい版の採用</text><text x="400" y="240">採用する側の規範の正当な所有者</text>
  </g>
  <path d="M40,80 H840 M40,140 H840 M40,200 H840" class="lt"/>
  <rect x="40" y="276" width="800" height="70" rx="10" class="xl" style="fill:#fff"/>
  <text x="440" y="318" class="ts xc" text-anchor="middle">新しい版の採用は、ふつうの実装・設定の変更を受け入れる権限だけでは決められない</text>
</svg>
```

実装・設定の変更、規範の改訂、新しい版の採用は、判断する者が違います。新しい版の採用は、ふつうの変更を受け入れる権限だけでは決められません。

出典: EAA Core 版 6「4. 提案と変更」の表と本文。

## 逆向きの変更も、同じ順序で

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="260" height="200" rx="10" class="box"/><text x="170" y="96" class="t" text-anchor="middle" font-weight="700">在庫の Cell</text>
  <rect x="580" y="60" width="260" height="200" rx="10" class="box"/><text x="710" y="96" class="t" text-anchor="middle" font-weight="700">物流の Cell</text>
  <rect x="650" y="116" width="120" height="40" rx="6" class="h"/><text x="710" y="142" class="ts on" text-anchor="middle">所有者</text>
  <text x="710" y="200" class="ts" text-anchor="middle">締めを 15 時から 14 時に</text><text x="710" y="224" class="ts" text-anchor="middle">早めた版 3 を公開</text>
  <path d="M576,170 H304" class="ln" marker-end="url(#arr)"/>
  <use href="#i-no" x="156" y="150" width="28" height="28"/><text x="170" y="210" class="ts" text-anchor="middle">採用しない</text>
  <rect x="40" y="290" width="800" height="60" rx="10" class="soft"/><text x="440" y="326" class="t" text-anchor="middle" font-weight="700">在庫が採用しなければ、15 時のまま</text>
</svg>
```

物流の側が締めの時刻を早めたい場合も同じです。所有者が承認して版を出しても、在庫が採用しなければ前の時刻のままで、物流は合意した義務を一方的に捨てられません。

出典: EAA Core 版 6「2. 自治と権限」「3. 意味と合意」。※ 例は EAA 紹介 3 の、説明のための仮定です。

## どの向きでも、同じ手続き

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <g class="ts" text-anchor="middle">
    <rect x="20" y="60" width="110" height="90" rx="10" class="box"/><text x="75" y="100">Cell</text><text x="75" y="126" class="tx">親（由来）</text>
    <rect x="170" y="60" width="110" height="90" rx="10" class="box"/><text x="225" y="100">Cell</text><text x="225" y="126" class="tx">子（由来）</text>
    <rect x="310" y="60" width="110" height="90" rx="10" class="box"/><text x="365" y="100">Cell</text><text x="365" y="126" class="tx">兄弟</text>
    <rect x="460" y="60" width="110" height="90" rx="10" class="box"/><text x="515" y="100">Cell</text><text x="515" y="126" class="tx">兄弟</text>
    <rect x="600" y="60" width="110" height="90" rx="10" class="box"/><text x="655" y="100">Cell</text><text x="655" y="126" class="tx">横断の責務</text>
    <rect x="750" y="60" width="110" height="90" rx="10" class="box"/><text x="805" y="100">Cell</text><text x="805" y="126" class="tx">ほか</text>
  </g>
  <path d="M132,105 H168" class="ln" marker-start="url(#arr)" marker-end="url(#arr)"/><path d="M422,105 H458" class="ln" marker-start="url(#arr)" marker-end="url(#arr)"/><path d="M712,105 H748" class="ln" marker-start="url(#arr)" marker-end="url(#arr)"/>
  <g class="ts" text-anchor="middle"><text x="150" y="196">提案と受入</text><text x="440" y="196">提案と受入</text><text x="730" y="196">提案と受入</text></g>
  <rect x="40" y="250" width="800" height="80" rx="10" class="soft"/>
  <text x="440" y="296" class="t" text-anchor="middle" font-weight="700">どの組み合わせにも、相手の中を直接変える権限は作らない</text>
</svg>
```

提案と受入の手続きは、親子・兄弟・横断のどの向きにも同じように当てます。どの組み合わせにも、相手の中を直接変える特別な権限はありません。

出典: EAA Core 版 6「4. 提案と変更」、EAA Profiles「7. 横断責務の実行」。

## 基盤の Cell も、PR で提案する

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="260" height="220" rx="10" class="box"/><text x="170" y="96" class="t" text-anchor="middle" font-weight="700">Platform の Cell</text>
  <rect x="580" y="60" width="260" height="220" rx="10" class="box"/><text x="710" y="96" class="t" text-anchor="middle" font-weight="700">業務の Cell</text>
  <path d="M300,140 H576" class="ln" marker-end="url(#arr)"/><use href="#i-pr" x="425" y="100" width="30" height="38"/><text x="440" y="164" class="ts" text-anchor="middle">CI/CD の変更の PR</text>
  <text x="710" y="150" class="ts" text-anchor="middle">自分の規範と Contract に</text><text x="710" y="174" class="ts" text-anchor="middle">合うかを確かめて</text>
  <use href="#i-ok" x="696" y="190" width="28" height="28"/><text x="710" y="240" class="ts okc" text-anchor="middle">受け入れる</text>
  <path d="M576,240 H304" class="ln" marker-end="url(#arr)"/><text x="440" y="232" class="ts" text-anchor="middle">提供条件への変更提案</text>
  <text x="440" y="330" class="t" text-anchor="middle" font-weight="700">基盤を担っていても、相手の中を直接は変えない</text>
</svg>
```

Platform を担う Cell も、CI/CD の変更は PR で提案します。受け取った Cell が、規範と Contract に合うかを確かめて受け入れます。

出典: EAA Profiles「7. 横断責務の実行」。第 5 章の Platform を分けた例の続きです。

## 導入は、PR を出しても終わらない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <path d="M80,200 H820" class="ln" marker-end="url(#arr)"/>
  <g class="ts" text-anchor="middle">
    <rect x="80" y="160" width="180" height="80" rx="6" class="soft"/><text x="170" y="206">PR を出した</text>
    <rect x="340" y="160" width="180" height="80" rx="6" class="soft"/><text x="430" y="206">受け入れられた</text>
    <rect x="600" y="160" width="200" height="80" rx="6" class="h"/><text x="700" y="196" class="on">導入後に成り立った</text><text x="700" y="222" class="on">ことを Evidence で確認</text>
  </g>
  <use href="#i-no" x="156" y="110" width="28" height="28"/><use href="#i-no" x="416" y="110" width="28" height="28"/><use href="#i-ok" x="686" y="110" width="28" height="28"/>
  <text x="440" y="300" class="t" text-anchor="middle" font-weight="700">完了するのは、右端だけ</text>
</svg>
```

ほかの Cell への導入を目的とする Mission は、提案を出しただけでは完了しません。導入した後に成り立ったことを、Evidence で確かめます。

出典: EAA Profiles「7. 横断責務の実行」。完了の条件は第 7 章で見ました。

## 正本の改訂と、採用版の変更を分ける

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <g class="ts">
    <text x="60" y="56" font-weight="700">起点</text><text x="260" y="56" font-weight="700">正本の改訂</text><text x="570" y="56" font-weight="700">採用している版の変更</text>
    <text x="60" y="120">提供する側が</text><text x="60" y="144">変えたい</text>
    <text x="260" y="120">提起した者以外の正本の所有者が</text><text x="260" y="144">承認し、新しい版を公開する</text>
    <text x="570" y="120">引き受けた側へ採用を提案し、</text><text x="570" y="144">引き受けた側が決める</text>
    <text x="60" y="210">引き受けた側が</text><text x="60" y="234">変えたい</text>
    <text x="260" y="210">提供する側へ提案し、提供する側が</text><text x="260" y="234">承認して新しい版を公開する</text>
    <text x="570" y="210">引き受けた側が中身を確かめ、</text><text x="570" y="234">採用するかを決める</text>
  </g>
  <path d="M40,76 H840 M40,170 H840 M240,30 V260 M550,30 V260" class="lt"/>
  <text x="440" y="316" class="ts sub" text-anchor="middle">承認済みの古い版は上書きしない。採用する版と中身を固定する</text>
</svg>
```

Profile の正本は提供する側が持ち、引き受けた側は採用した版を特定します。どちらが変えたい場合も、正本の改訂と採用している版の変更を別に扱います。

出典: EAA Profiles「4.」の「改訂元と採用先を分ける」。

## PR では、正本と採用版を別の PR に

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="40" width="340" height="220" rx="10" class="box"/><text x="210" y="76" class="t" text-anchor="middle" font-weight="700">提供する側の repo</text>
  <use href="#i-pr" x="110" y="104" width="26" height="32"/><text x="150" y="126" class="ts">正本を改訂する PR</text>
  <rect x="80" y="170" width="260" height="56" rx="3" class="hl" style="fill:#fff"/><text x="210" y="204" class="ts hc" text-anchor="middle">Profile　版 2（固定）</text>
  <rect x="500" y="40" width="340" height="220" rx="10" class="box"/><text x="670" y="76" class="t" text-anchor="middle" font-weight="700">引き受けた側の repo</text>
  <use href="#i-pr" x="560" y="104" width="26" height="32"/><text x="600" y="126" class="ts">採用版を更新する PR</text>
  <rect x="540" y="170" width="260" height="56" rx="6" class="soft"/><text x="670" y="196" class="ts" text-anchor="middle">CLAUDE.md から</text><text x="670" y="218" class="ts" text-anchor="middle">版 2 を参照する</text>
  <path d="M540,198 H344" class="ln" marker-end="url(#arr)"/>
  <text x="440" y="300" class="ts" text-anchor="middle">参照は latest ではなく、承認済みの中身を特定できる固定版</text>
  <text x="440" y="334" class="ts sub" text-anchor="middle">正本の PR・採用版の PR・採用の結果を関連づけ、実際の採用版を追えるようにする</text>
</svg>
```

GitHub では、正本を改訂する PR と採用版を更新する PR を分けます。それぞれの文書の所有者が判断でき、参照先は固定した版にします。

出典: EAA Delivery Guide「20. Profile 改訂・採用 Pattern」（適用例）。

## Core はここまでしか決めていない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="30" width="380" height="290" rx="10" class="soft"/>
  <text x="60" y="64" class="t" font-weight="700">Core が決めていること</text>
  <g class="ts"><use href="#i-ok" x="60" y="88" width="22" height="22"/><text x="92" y="105">公開と採用は別</text>
  <use href="#i-ok" x="60" y="128" width="22" height="22"/><text x="92" y="145">全部が採用して移る</text>
  <use href="#i-ok" x="60" y="168" width="22" height="22"/><text x="92" y="185">提案と受入、判断する者</text>
  <use href="#i-ok" x="60" y="208" width="22" height="22"/><text x="92" y="225">どの向きでも同じ手続き</text></g>
  <rect x="460" y="30" width="380" height="290" rx="10" fill="url(#hatch)"/>
  <text x="480" y="64" class="t" font-weight="700">詳しい手順が未定のこと</text>
  <g class="ts"><text x="480" y="102" class="ts" font-weight="700">既知の不足（Core の冒頭が挙げた）</text><text x="480" y="138" class="ts">移行中の責任</text><text x="480" y="174" class="ts">複数の Cell にまたがる変更の</text><text x="480" y="198" class="ts">互換性・適用順・部分失敗からの復旧</text><text x="480" y="234" class="ts">合意不成立の調整</text><text x="480" y="270" class="ts">外部の制約の変化・緊急時の調整</text></g>
  <text x="440" y="356" class="ts sub" text-anchor="middle">手順が未定の調整を、ほかの Cell からの一方的な強制で埋めない</text>
</svg>
```

右の項目は、どれも Core が冒頭で既知の不足として挙げたものです。扱いが無いのではなく、未定なのは詳しい手順です。

出典: EAA Core 版 6 冒頭の観測欄（既知の不足）と「2. 自治と権限」。
