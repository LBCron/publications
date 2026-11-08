# 第 4 章　分割で渡した判断権限は、親 Cell も上書きしない

群: Cell の分割と自治

<!--
構造: agent-hub-roles-kaz/philosopher/2026-11-07-eaa-textbook-structure.md（55553ae4）。章題と群の札の字は writer-ja/drafts/eaa-toc/titles.md（d21b0d80、@ope-ultp1635 msg 65a67e15）で書き直した。構造は変えない。
出どころ（構造の表のまま）: core.md:43・52-53・62-63・70。Core は publications origin/main 0d07f75 の core.md 版 6。
本文: @ope-ultp1635 msg 18751c19（群二）。
絵: 親 Cell と子 Cell は横に並べ、子を親の枠の中に描かない。親子の線は、ほかの Cell どうしの線と同じ形にした（core.md:43「分割の後の両者の関係は、ほかのCellどうしと同じCellの間の関係である」）。55 行（子Cell群を持つCell）には合わせていない（同 msg）。骨格にあった「（保留）子 Cell を親 Cell の枠の中に描くか」は、描かないで閉じた。
「親・子」の字は、分割の由来を言うときだけ使う。分割の後の関係を言う文では「渡した Cell」「受け取った Cell」と書いた。
最後のページ「上書きを許すと、確かめが効かない」は core.md:22（他 Cell は一方的に上書きしないので、確かめるのは受け取った Cell）による。第 0 章と同じ行。
新しく引く外部の文献は無い。
⑤（@ope-ultp1635 msg 281e5366、@reviewer 3 回目・4 回目）: 「決める権限のある相手」を core.md:70 の字「正当な判断主体」に直した。自分の Cell 側の主体が抜けないため。第 2・10 章と揃う。
-->

> 親・子は分割の由来を示す呼び名で、分割の後はほかの Cell どうしと同じ関係である。親の範囲が後で変わっても子の範囲は子が新しい版を採用するまで変わらず、提案を断っても合意した義務は残る。

```svg
<svg viewBox="0 0 880 300" width="880" height="300">
  <text x="150" y="30" class="ts sub" text-anchor="middle">分割の前</text>
  <rect x="40" y="44" width="220" height="150" rx="10" class="box"/><text x="150" y="78" class="t" text-anchor="middle" font-weight="700">Cell</text>
  <g class="ts" text-anchor="middle"><rect x="62" y="100" width="82" height="40" rx="3" class="hl" style="fill:#fff"/><text x="103" y="126" class="hc">契約</text><rect x="156" y="100" width="82" height="40" rx="3" class="hl" style="fill:#fff"/><text x="197" y="126" class="hc">請求</text></g>
  <path d="M290,120 H340" class="ln" marker-end="url(#arr)"/><text x="315" y="108" class="tx" text-anchor="middle">分割</text>
  <text x="600" y="30" class="ts sub" text-anchor="middle">分割の後</text>
  <rect x="360" y="44" width="220" height="150" rx="10" class="box"/><text x="470" y="78" class="t" text-anchor="middle" font-weight="700">Cell</text><text x="470" y="100" class="tx" text-anchor="middle">親（渡した）</text>
  <rect x="408" y="116" width="124" height="40" rx="3" class="hl" style="fill:#fff"/><text x="470" y="142" class="ts hc" text-anchor="middle">契約　版 4</text>
  <rect x="620" y="44" width="220" height="150" rx="10" class="box"/><text x="730" y="78" class="t" text-anchor="middle" font-weight="700">Cell</text><text x="730" y="100" class="tx" text-anchor="middle">子（受け取った）</text>
  <rect x="668" y="116" width="124" height="40" rx="3" class="hl" style="fill:#fff"/><text x="730" y="142" class="ts hc" text-anchor="middle">請求　版 3</text>
  <path d="M580,120 H620" class="ln"/>
  <text x="730" y="222" class="ts" text-anchor="middle">子が採用するまで版 3 のまま</text>
  <text x="440" y="274" class="t" text-anchor="middle" font-weight="700">分けた後は、ほかの Cell どうしと同じく横に並ぶ</text>
</svg>
```

分割は、責務と判断権限を別の Cell に渡すことです。渡したものは受け取った Cell のものになり、渡した側は、親であっても、その判断を上書きしません。

## 分割は判断権限ごと渡すこと

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="300" height="220" rx="10" class="box"/><text x="190" y="96" class="t" text-anchor="middle" font-weight="700">渡す Cell</text>
  <rect x="540" y="60" width="300" height="220" rx="10" class="box"/><text x="690" y="96" class="t" text-anchor="middle" font-weight="700">受け取る Cell</text>
  <rect x="380" y="110" width="120" height="44" rx="3" class="hl" style="fill:#fff"/><text x="440" y="138" class="ts hc" text-anchor="middle">責務</text>
  <rect x="380" y="176" width="120" height="44" rx="6" class="h"/><text x="440" y="204" class="ts on" text-anchor="middle">判断権限</text>
  <path d="M340,165 H536" class="ln" marker-end="url(#arr)"/>
  <rect x="600" y="136" width="180" height="56" rx="6" class="soft"/><text x="690" y="170" class="ts" text-anchor="middle">自分で判断して実行する</text>
  <text x="440" y="320" class="t" text-anchor="middle" font-weight="700">責務だけ渡して、判断は手元に残す、をしない</text>
</svg>
```

分割は、責務と、自分で判断する権限を、別の責任主体に渡すことです。責務だけを渡し、判断を手元に残すのは分割ではありません。

出典: EAA Core 版 6「1. 責務と分割」。

## 親・子は、由来の呼び名

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="70" width="220" height="150" rx="10" class="box"/><text x="150" y="110" class="t" text-anchor="middle" font-weight="700">Cell</text><text x="150" y="140" class="ts sub" text-anchor="middle">親（渡した）</text>
  <rect x="330" y="70" width="220" height="150" rx="10" class="box"/><text x="440" y="110" class="t" text-anchor="middle" font-weight="700">Cell</text><text x="440" y="140" class="ts sub" text-anchor="middle">子（受け取った）</text>
  <rect x="620" y="70" width="220" height="150" rx="10" class="box"/><text x="730" y="110" class="t" text-anchor="middle" font-weight="700">Cell</text><text x="730" y="140" class="ts sub" text-anchor="middle">分割と関係のない Cell</text>
  <path d="M260,170 H330 M550,170 H620" class="hl"/>
  <use href="#i-pr" x="284" y="178" width="20" height="26"/><use href="#i-pr" x="574" y="178" width="20" height="26"/>
  <text x="295" y="246" class="tx" text-anchor="middle">Contract と Evidence</text><text x="585" y="246" class="tx" text-anchor="middle">Contract と Evidence</text>
  <rect x="40" y="276" width="800" height="76" rx="10" class="lt" style="fill:#fff"/>
  <text x="440" y="308" class="t" text-anchor="middle" font-weight="700">どちらの線も同じ。親子の間だけ、特別な線は引かない</text>
  <text x="440" y="336" class="ts sub" text-anchor="middle">子も、親の枠の中には入らない</text>
</svg>
```

渡した Cell を親、受け取った Cell を子と呼びます。呼び名は分割の由来を示すだけで、分割の後の両者の関係は、ほかの Cell どうしと同じです。

出典: EAA Core 版 6 の概念表「親 Cell・子 Cell」。

## 親の範囲が変わっても、子は変わらない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <path d="M120,320 H820" class="ln" marker-end="url(#arr)"/><text x="830" y="346" class="tx" text-anchor="end">時間</text>
  <text x="60" y="110" class="ts" text-anchor="middle" font-weight="700">親</text><text x="60" y="230" class="ts" text-anchor="middle" font-weight="700">子</text>
  <rect x="120" y="86" width="240" height="44" rx="3" class="hl" style="fill:#fff"/><text x="240" y="114" class="ts hc" text-anchor="middle">版 3</text>
  <rect x="380" y="86" width="440" height="44" rx="3" class="hl" style="fill:#fff"/><text x="600" y="114" class="ts hc" text-anchor="middle">版 4（親の範囲が変わった）</text>
  <rect x="120" y="206" width="480" height="44" rx="3" class="hl" style="fill:#fff"/><text x="360" y="234" class="ts hc" text-anchor="middle">版 3 のまま</text>
  <rect x="620" y="206" width="200" height="44" rx="3" class="hl" style="fill:#fff"/><text x="720" y="234" class="ts hc" text-anchor="middle">版 4</text>
  <path d="M380,134 L380,200" class="xl dash"/><use href="#i-no" x="368" y="156" width="24" height="24"/><text x="400" y="174" class="tx">自動では移らない</text>
  <path d="M610,196 V262" class="ln"/><use href="#i-ok" x="598" y="268" width="24" height="24"/><text x="610" y="306" class="ts okc" text-anchor="middle">子が採用した</text>
</svg>
```

渡した Cell の範囲が後で変わっても、受け取った Cell の範囲は、受け取った Cell が新しい版を採用するまで変わりません。

出典: EAA Core 版 6「1. 責務と分割」。版の採用は第 9 章で見ます。

## 親も、横断の Cell も上書きしない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="320" y="110" width="240" height="160" rx="10" class="box"/><text x="440" y="146" class="t" text-anchor="middle" font-weight="700">Cell</text>
  <rect x="350" y="170" width="180" height="70" rx="6" class="soft"/><text x="440" y="200" class="ts" text-anchor="middle">中の方式と実行を</text><text x="440" y="224" class="ts" text-anchor="middle">自分で決める</text>
  <rect x="40" y="40" width="200" height="90" rx="10" class="box"/><text x="140" y="80" class="ts" text-anchor="middle" font-weight="700">親の Cell</text>
  <rect x="640" y="40" width="200" height="90" rx="10" class="box"/><text x="740" y="74" class="ts" text-anchor="middle" font-weight="700">横断の責務を</text><text x="740" y="98" class="ts" text-anchor="middle" font-weight="700">担う Cell</text>
  <rect x="40" y="250" width="200" height="90" rx="10" class="box"/><text x="140" y="300" class="ts" text-anchor="middle" font-weight="700">ほかの Cell</text>
  <path d="M240,100 L316,150" class="xl dash" marker-end="url(#arr-x)"/><path d="M640,100 L564,150" class="xl dash" marker-end="url(#arr-x)"/><path d="M240,290 L316,240" class="xl dash" marker-end="url(#arr-x)"/>
  <use href="#i-no" x="266" y="104" width="22" height="22"/><use href="#i-no" x="592" y="104" width="22" height="22"/><use href="#i-no" x="266" y="244" width="22" height="22"/>
  <text x="440" y="310" class="ts" text-anchor="middle">合意して採用した規範と Contract の範囲で</text>
  <text x="740" y="300" class="ts xc" text-anchor="middle">どれも、一方的に書き換えない</text>
</svg>
```

各 Cell は、採用した規範と Contract の範囲で、中の方式と実行を決めます。親の Cell も横断の責務を担う Cell も、その判断を一方的に上書きしません。

出典: EAA Core 版 6「2. 自治と権限」。

## 断ることと、義務を捨てることは別

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <path d="M440,20 V310" class="lt dash"/>
  <text x="220" y="44" class="t" text-anchor="middle" font-weight="700">新しい提案</text>
  <text x="660" y="44" class="t" text-anchor="middle" font-weight="700">合意済みの義務</text>
  <rect x="120" y="80" width="200" height="56" rx="3" class="hl" style="fill:#fff"/><text x="220" y="114" class="ts hc" text-anchor="middle">版 5 にしたい</text>
  <use href="#i-no" x="206" y="150" width="28" height="28"/><text x="220" y="208" class="ts" text-anchor="middle">受け入れない、と判断してよい</text>
  <rect x="560" y="80" width="200" height="56" rx="3" class="hl" style="fill:#fff"/><text x="660" y="114" class="ts hc" text-anchor="middle">版 4 で約束した保証</text>
  <use href="#i-ok" x="646" y="150" width="28" height="28"/><text x="660" y="208" class="ts" text-anchor="middle">断っても、残る</text>
  <rect x="40" y="236" width="800" height="116" rx="10" class="soft"/>
  <text x="60" y="268" class="ts" font-weight="700">果たせない・自分の権限で決められないとき</text>
  <text x="60" y="300" class="ts">黙って捨てない。果たせないことをはっきり示し、</text>
  <text x="60" y="328" class="ts">正当な判断主体との調整に戻す</text>
</svg>
```

新しい提案を受け入れないことと、合意した義務を一方的に捨てることは別です。果たせないときは、それを示して、正当な判断主体との調整に戻します。

出典: EAA Core 版 6「2. 自治と権限」。

## 上書きを許すと、確かめが効かない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="70" width="240" height="200" rx="10" class="box"/><text x="160" y="106" class="t" text-anchor="middle" font-weight="700">作った Cell</text>
  <rect x="600" y="70" width="240" height="200" rx="10" class="box"/><text x="720" y="106" class="t" text-anchor="middle" font-weight="700">受け取った Cell</text>
  <path d="M280,160 H596" class="ln" marker-end="url(#arr)"/><use href="#i-pr" x="425" y="124" width="30" height="38"/><text x="440" y="186" class="ts" text-anchor="middle">Evidence</text>
  <use href="#i-ok" x="636" y="140" width="28" height="28"/><text x="750" y="160" class="ts okc" text-anchor="middle">確かめて受け入れる</text>
  <rect x="600" y="210" width="240" height="44" rx="6" class="soft"/><text x="720" y="238" class="ts" text-anchor="middle">判断は受け取った Cell のもの</text>
  <path d="M440,330 C 560,330 680,310 700,262" class="xl dash" marker-end="url(#arr-x)"/><text x="300" y="336" class="ts xc" text-anchor="middle">別の Cell が判断を書き換える</text>
  <use href="#i-no" x="560" y="306" width="24" height="24"/>
</svg>
```

成果を確かめるのは、受け取った Cell です。その判断をほかの Cell が書き換えられるなら、確かめた意味がなくなります。だから、親であっても上書きしません。

出典: EAA Core 版 6「0. 目的と範囲」（第 0 章と同じ行）。※「確かめた意味がなくなる」は、この行からの読みで、Core が書いた理由ではない。
