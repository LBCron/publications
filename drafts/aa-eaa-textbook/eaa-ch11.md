# 第 11 章　Core の採用は各 Cell の規範の所有者が決め、拘束と不採用の部分を記録する

群: 規範の承認・採用と導入

<!--
構造: agent-hub-roles-kaz/philosopher/2026-11-07-eaa-textbook-structure.md（55553ae4）。章題と群の札の字は writer-ja/drafts/eaa-toc/titles.md（d21b0d80、@ope-ultp1635 msg 65a67e15）で書き直した。構造は変えない。
出どころ（構造の表のまま）: core.md:112-123。Core は publications origin/main 0d07f75 の core.md 版 6。
本文: @ope-ultp1635 msg dfcb091f（群四）。
足した出どころ: core.md:79（新しい版の公開と採用は別で、自動では追随しない。第 9 章と同じ行）、core.md:93（新しい版の採用は、ふつうの受入の権限だけでは決められない）。
例は第 6〜10 章の在庫と物流を続けた。物流が Contract の所有者なのは第 8 章の例のまま。在庫の不採用の例（所有者が離れたときの規定）と理由は説明のための仮定で、第 8 章の最後のページ（Contract と商取引上の契約書の関係を Core は定めていない）につないだ。
「Core の所有者は承認者にならない」の理由と、「新しい版の採用も同じ承認と記録をする」は Core の行からの読みで、注に書いた。
publications の APPROVALS.md「本書に書かないもの」は他の Cell での採用の承認をその Cell の記録とする旨を書くが、実例を使わない判断（第 10 章の書き手のメモ）に合わせて引いていない。
包含と同じ形の字: 採用の記録を全体の側が一つ持つ形は書いていない（core.md:123 の「記録はそのCellが管理し」のとおり、記録は各 Cell の枠の中に描いた）。
絵: Cell はどれもほかの Cell の枠の外に並べる（core.md:43）。Core の文書は Cell の上に置くが、どの Cell も囲まない。
新しく引く外部の文献は無い。
⑥（@ope-ultp1635 msg 6fc17eeb、@reviewer 2〜4 回目）: p.「採用しない部分は、相手に示す」の例は、同じ Contract について在庫と物流が別々の規定に従う状態を作るのに、最後のページがそれを挙げていなかった。core.md:121 は示すことまでしか求めないので、「Core に書かれていない」に足した。観測欄の「移行中の責任」はこの章では使っていない（⑤で出典欄から外した）。
⑤（@ope-ultp1635 msg 281e5366、@reviewer 3 回目・4 回目）: 最後のページの項目は core.md:11 の既知の不足に無いので「Core に書かれていない」に置いた。出典欄の「移行中の責任は既知の不足」は、3 項目のどれとも Core が結びつけていないので外した。
-->

> 採用を承認するのは Core の所有者ではない人間で、承認者を置けない Cell は採用しない。記録はその Cell が管理し、Core の所有者は書き換えない。

```svg
<svg viewBox="0 0 880 300" width="880" height="300">
  <rect x="200" y="20" width="480" height="250" rx="10" class="box"/>
  <text x="440" y="56" class="t" text-anchor="middle" font-weight="700">採用の記録（物流の Cell が管理する）</text>
  <g class="ts">
    <text x="230" y="104" font-weight="700">承認者と版</text><text x="420" y="104">物流の規範の所有者・Core 版 6</text>
    <text x="230" y="158" font-weight="700">引き受ける拘束</text><text x="420" y="158">所有する共有文書と、その所有者</text>
    <text x="230" y="212" font-weight="700">採用しない部分</text><text x="420" y="212">その部分と理由。無ければ無い</text>
  </g>
  <path d="M220,124 H660 M220,178 H660 M400,76 V240" class="lt"/>
</svg>
```

Core を採用するかは、各 Cell が決めます。決めた者と、引き受ける拘束と、採用しない部分を、その Cell の記録に残します。

## 採用は、Cell ごとに決める

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="300" y="30" width="280" height="60" rx="3" class="hl" style="fill:#fff"/><text x="440" y="66" class="ts hc" text-anchor="middle" font-weight="700">EAA Core　版 6（公開済み）</text>
  <path d="M380,94 L240,130 M500,94 L640,130" class="lt"/>
  <rect x="40" y="130" width="340" height="190" rx="10" class="box"/><text x="210" y="166" class="t" text-anchor="middle" font-weight="700">在庫の Cell</text>
  <text x="210" y="226" class="ts" text-anchor="middle">採用するかを、自分で決める</text>
  <rect x="500" y="130" width="340" height="190" rx="10" class="box"/><text x="670" y="166" class="t" text-anchor="middle" font-weight="700">物流の Cell</text>
  <text x="670" y="226" class="ts" text-anchor="middle">採用するかを、自分で決める</text>
  <text x="440" y="356" class="ts sub" text-anchor="middle">Core を公開しても、どの Cell も自動では従わない</text>
</svg>
```

Core を採用するかは、Cell ごとに決めます。Core が公開されていても、どの Cell も自動では従いません。

出典: EAA Core 版 6「6. 本書の採用」「3. 意味と合意」。公開と採用が別の行為なのは、第 9 章の Contract の版と同じです。

## 承認するのは、その Cell の規範の所有者

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="380" height="240" rx="10" class="box"/><text x="230" y="96" class="t" text-anchor="middle" font-weight="700">物流の Cell</text>
  <rect x="80" y="130" width="300" height="44" rx="6" class="h"/><text x="230" y="158" class="ts on" text-anchor="middle">物流の規範の所有者</text>
  <use href="#i-ok" x="216" y="190" width="28" height="28"/><text x="230" y="246" class="ts okc" text-anchor="middle">Core の採用を承認する</text>
  <rect x="480" y="60" width="360" height="240" rx="10" class="soft"/>
  <text x="660" y="110" class="ts" text-anchor="middle" font-weight="700">これだけでは決められない</text>
  <g class="ts"><use href="#i-no" x="510" y="150" width="22" height="22"/><text x="544" y="167">実装・設定の変更を</text><text x="544" y="191">受け入れる権限</text></g>
</svg>
```

Core の採用を承認するのは、その Cell の規範の正当な所有者です。ふつうの変更を受け入れる権限だけでは決められません。

出典: EAA Core 版 6「6. 本書の採用」「4. 提案と変更」。規範の新しい版の採用と同じ扱いで、第 9 章で見ました。

## Core の所有者は、承認しない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="300" height="220" rx="10" class="soft"/><text x="190" y="100" class="t" text-anchor="middle" font-weight="700">Core の所有者</text>
  <use href="#i-no" x="176" y="140" width="28" height="28"/><text x="190" y="200" class="ts xc" text-anchor="middle">どの Cell の採用も</text><text x="190" y="224" class="ts xc" text-anchor="middle">承認しない</text>
  <rect x="480" y="60" width="360" height="220" rx="10" class="box"/><text x="660" y="96" class="t" text-anchor="middle" font-weight="700">在庫の Cell</text>
  <text x="660" y="140" class="ts" text-anchor="middle">規範の所有者のうち、</text><text x="660" y="164" class="ts" text-anchor="middle">Core の所有者ではない人間</text>
  <use href="#i-ok" x="646" y="186" width="28" height="28"/><text x="660" y="244" class="ts okc" text-anchor="middle">この人が承認する</text>
</svg>
```

承認者は、その Cell の規範の所有者のうち、Core の所有者ではない人間です。Core の所有者が所有者を兼ねていても、その人は承認しません。

出典: EAA Core 版 6「6. 本書の採用」。※ 書いた者が採用の判断を兼ねない点で、第 10 章の職務分離と同じ向きです。Core が書いた理由ではありません。

## 承認者を置けなければ、採用しない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="380" height="230" rx="10" class="box"/><text x="230" y="96" class="t" text-anchor="middle" font-weight="700">ある Cell</text>
  <rect x="90" y="130" width="280" height="44" rx="6" class="h"/><text x="230" y="158" class="ts on" text-anchor="middle">規範の所有者 = Core の所有者</text>
  <text x="230" y="220" class="ts" text-anchor="middle">ほかに規範の所有者がいない</text>
  <path d="M420,175 H496" class="ln" marker-end="url(#arr)"/>
  <rect x="500" y="60" width="340" height="230" rx="10" fill="url(#hatch)"/>
  <use href="#i-no" x="656" y="120" width="28" height="28"/><text x="670" y="190" class="t" text-anchor="middle" font-weight="700">Core を採用しない</text>
</svg>
```

この条件に合う承認者を置けない Cell では、Core を採用しません。たとえば、規範の所有者が Core の所有者 1 人だけの Cell です。

出典: EAA Core 版 6「6. 本書の採用」。※ 例は、同じ節の 2 行から導いた場合の一つです。

## 理解ではなく、記録で成り立つ

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="340" height="220" rx="10" fill="url(#hatch)"/>
  <text x="210" y="130" class="t" text-anchor="middle" font-weight="700">理解しているか</text>
  <text x="210" y="190" class="ts" text-anchor="middle">Core は検査しない</text>
  <rect x="500" y="60" width="340" height="220" rx="10" class="box"/>
  <text x="670" y="110" class="t" text-anchor="middle" font-weight="700">記録したか</text>
  <text x="670" y="160" class="ts" text-anchor="middle">決めた項目を、自分の Cell に</text><text x="670" y="184" class="ts" text-anchor="middle">当てて記録する</text>
  <use href="#i-ok" x="656" y="210" width="28" height="28"/>
  <text x="440" y="330" class="t" text-anchor="middle" font-weight="700">承認は、記録したときに成り立つ</text>
</svg>
```

承認者が Core を理解しているかを、Core は検査しません。承認は、承認者が決められた項目を自分の Cell に当てて記録したときに成り立ちます。

出典: EAA Core 版 6「6. 本書の採用」。

## 記録に書くこと

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <g class="ts">
    <text x="60" y="60" font-weight="700">項目</text><text x="330" y="60" font-weight="700">書くこと</text>
    <text x="60" y="120">承認者と版</text><text x="330" y="120">承認者の名前と、採用する Core の版</text>
    <text x="60" y="190">引き受ける拘束</text><text x="330" y="190">少なくとも、その Cell が所有する共有文書と、</text><text x="330" y="214">その所有者</text>
    <text x="60" y="284">採用しない部分</text><text x="330" y="284">その部分と理由。無ければ、無いこと</text>
  </g>
  <path d="M40,80 H840 M40,150 H840 M40,244 H840 M40,314 H840 M310,30 V314" class="lt"/>
</svg>
```

記録には、承認者の名前と採用する版、引き受ける拘束、採用しない部分とその理由を書きます。採用しない部分が無ければ、無いと書きます。

出典: EAA Core 版 6「6. 本書の採用」。

## 例：物流の採用の記録

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="30" width="800" height="300" rx="10" class="box"/>
  <text x="60" y="66" class="t" font-weight="700">物流の Cell　Core の採用の記録</text>
  <g class="ts">
    <text x="60" y="120" font-weight="700">承認者と版</text><text x="270" y="120">物流の規範の所有者（名前）・Core 版 6</text>
    <text x="60" y="184" font-weight="700">引き受ける拘束</text><text x="270" y="184">所有する共有文書：在庫と物流のあいだの Contract</text><text x="270" y="208">その所有者：物流の窓口の責任者</text>
    <text x="60" y="278" font-weight="700">採用しない部分</text><text x="270" y="278">無い</text>
  </g>
  <path d="M50,90 H830 M50,150 H830 M50,240 H830" class="lt"/>
</svg>
```

物流は、在庫との Contract を所有しているので、それを拘束に書きます。採用しない部分は無いので、無いと書きます。

※ 記録の中身は説明のための仮定です。Contract の所有者が物流の窓口の責任者なのは、第 8 章の例のままです。

## 採用しない部分は、相手に示す

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="40" width="340" height="250" rx="10" class="box"/><text x="210" y="76" class="t" text-anchor="middle" font-weight="700">在庫の Cell</text>
  <g class="ts"><text x="70" y="124" font-weight="700">採用しない部分</text><text x="70" y="156">Contract の所有者が離れたときの規定</text><text x="70" y="200" font-weight="700">理由</text><text x="70" y="232">所有者の交代を、取引先との</text><text x="70" y="256">契約書で決めているため</text></g>
  <path d="M380,165 H536" class="ln" marker-end="url(#arr)"/><text x="458" y="152" class="ts" text-anchor="middle">示す</text>
  <rect x="540" y="40" width="300" height="250" rx="10" class="box"/><text x="690" y="76" class="t" text-anchor="middle" font-weight="700">物流の Cell</text>
  <text x="690" y="160" class="ts" text-anchor="middle">Contract を共有する相手</text>
</svg>
```

採用しない部分のうち、共有する文書にかかるものは、その文書を共有する Cell に示します。在庫が Contract にかかる部分を外すなら、物流に示します。

出典: EAA Core 版 6「6. 本書の採用」。※ 外す部分と理由は説明のための仮定です。Contract と契約書の関係は第 8 章の最後のページで見ました。

## 記録は、その Cell が持つ

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="380" height="240" rx="10" class="box"/><text x="230" y="96" class="t" text-anchor="middle" font-weight="700">在庫の Cell</text>
  <rect x="100" y="130" width="260" height="70" rx="3" class="hl" style="fill:#fff"/><text x="230" y="172" class="ts hc" text-anchor="middle" font-weight="700">在庫の採用の記録</text>
  <text x="230" y="250" class="ts" text-anchor="middle">在庫が管理する</text>
  <rect x="540" y="60" width="300" height="240" rx="10" class="soft"/><text x="690" y="100" class="t" text-anchor="middle" font-weight="700">Core の所有者</text>
  <path d="M536,165 H364" class="xl dash"/><use href="#i-no" x="436" y="137" width="28" height="28"/><text x="450" y="200" class="ts xc" text-anchor="middle">書き換えない</text>
</svg>
```

採用の記録は、採用した Cell が管理します。Core の所有者は、その記録を書き換えません。

出典: EAA Core 版 6「6. 本書の採用」。

## Core の新しい版も、採用して移る

```svg
<svg viewBox="0 0 880 300" width="880" height="300">
  <path d="M120,236 H840" class="ln" marker-end="url(#arr)"/><text x="840" y="260" class="tx" text-anchor="end">時間</text>
  <text x="70" y="96" class="ts" text-anchor="middle" font-weight="700">在庫</text><text x="70" y="176" class="ts" text-anchor="middle" font-weight="700">物流</text>
  <rect x="120" y="74" width="380" height="40" rx="3" class="lt" style="fill:#fff"/><text x="310" y="100" class="ts" text-anchor="middle">Core 版 6</text>
  <rect x="500" y="74" width="340" height="40" rx="3" class="hl" style="fill:#fff"/><text x="670" y="100" class="ts hc" text-anchor="middle">版 7 を採用（承認と記録）</text>
  <rect x="120" y="154" width="720" height="40" rx="3" class="lt" style="fill:#fff"/><text x="480" y="180" class="ts" text-anchor="middle">Core 版 6 のまま</text>
  <path d="M300,40 V220" class="lt dash"/><text x="300" y="32" class="tx" text-anchor="middle">版 7 を公開</text>
</svg>
```

Core に新しい版が出ても、採用した Cell は自動では移りません。移るときも、承認者が新しい版を自分の Cell に当てて記録します。

出典: EAA Core 版 6「3. 意味と合意」「6.」。※ 版の番号は説明のための仮定です。移るときに同じ記録をするのは、記録に版を書くことからの読みです。

## Core はここまでしか決めていない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="30" width="380" height="290" rx="10" class="soft"/>
  <text x="60" y="64" class="t" font-weight="700">Core が決めていること</text>
  <g class="ts"><use href="#i-ok" x="60" y="88" width="22" height="22"/><text x="92" y="105">承認者の条件</text>
  <use href="#i-ok" x="60" y="128" width="22" height="22"/><text x="92" y="145">置けなければ採用しない</text>
  <use href="#i-ok" x="60" y="168" width="22" height="22"/><text x="92" y="185">記録に書く項目</text>
  <use href="#i-ok" x="60" y="208" width="22" height="22"/><text x="92" y="225">記録は採用した Cell が持つ</text></g>
  <rect x="460" y="30" width="380" height="290" rx="10" fill="url(#hatch)"/>
  <text x="480" y="64" class="t" font-weight="700">決めていないこと</text>
  <g class="ts"><text x="480" y="102" class="ts" font-weight="700">Core に書かれていない</text><text x="480" y="126" class="tx">既知の不足にも、決める予定にも無い</text><text x="480" y="162" class="ts">記録の書式と置き場所</text><text x="480" y="194" class="ts">採用をやめるときの手続き</text><text x="480" y="226" class="ts">Core の版が違う Cell どうしの</text><text x="480" y="250" class="ts">あいだの扱い</text><text x="480" y="282" class="ts">不採用を示した後、同じ Contract で</text><text x="480" y="306" class="ts">両側が別の規定に従う状態の扱い</text></g>
  <text x="440" y="356" class="ts sub" text-anchor="middle">理解しているかは、Core では検査しない</text>
</svg>
```

記録の書式と置き場所、採用をやめる手続き、Core の版が違う Cell どうしの扱い、不採用を示した後の同じ Contract の扱いは、Core に書かれていません。

出典: EAA Core 版 6「6.」と冒頭の観測欄（右はどれも既知の不足に無い）。※ 最後の項目は「相手に示す」の例が作る状態。Core が求めるのは示すことまで。
