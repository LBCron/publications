# 第 5 章　Cell の分割と統合では、権限・記録・残件・未履行の保証を引き継ぐ

群: Cell の分割と自治

<!--
構造: agent-hub-roles-kaz/philosopher/2026-11-07-eaa-textbook-structure.md（55553ae4）。章題と群の札の字は writer-ja/drafts/eaa-toc/titles.md（d21b0d80、@ope-ultp1635 msg 65a67e15）で書き直した。構造は変えない。
出どころ（構造の表のまま）: core.md:57-58、profiles.md 5 節、development-model.md:52-64。Core は publications origin/main 0d07f75 の core.md 版 6。
リードの「引継ぎの詳細手順は Profiles が未決として残している」は profiles.md:83・135 による（⑤、@ope-ultp1635 msg 281e5366。以前は「Core でも」と書き、Profiles の字を Core に帰属させていた）。Core の既知の不足（core.md:11）に当たるのは「移行中の責任」だけ。最後のページの注に書いた。同じページの絵の「一方的な強制で埋めない」は core.md:71。
本文: @ope-ultp1635 msg 18751c19（群二）。
絵: 元の Cell と分かれた Cell は横に並べ、どの Cell もほかの Cell の枠の中に描かない（同 msg。core.md:43）。
Platform の分離は development-model.md:55「構成例であり、効果の実証ではない」。例のページの注と、効果のページの注に書いた。
development-model.md:58 にある比喩の語は本文に持ち込まない（root CLAUDE.md「成果物の文章の作法」の語の表）。
新しく引く外部の文献は無い。
⑥（@ope-ultp1635 msg 6fc17eeb、@reviewer 2〜4 回目、項 15）: core.md の「移行」は版の移行（core.md:79・80）の語で、分割の引継ぎ（core.md:57）には「移行」の字が無い。core.md:11 の「移行中の責任」が分割の引継ぎに当たるかは Core の字では決まらないので、最後のページの注にそう書いた。
⑤（@ope-ultp1635 msg 281e5366、@reviewer 3 回目・4 回目）: 最後のページの「決めていないこと」を、Core の既知の不足（core.md:11 の移行中の責任）と、Profiles が未決・未確定とした引継ぎ・移行の手順（profiles.md:83・135）に分けた。
2 周目（@ope-ultp1635 msg 8fbac4e5、@reader r2 cea29c1f）: 最後のページの絵の「既知の不足」の小見出しの下に「詳しい手順は未定。いつ決めるかは書いていない」を足した（文は上限 80 字に余りが無いので絵に持たせた。第 8・9 章も同じ）。core.md:11 は観測欄で「既知の不足として、…は、詳細手順が未定である」と挙げるだけで、後の版で決めるとは書いていない。そのため「決める予定」とは書かず、いつ・どの版で決めるかは書いていない、とした。
-->

> 業務機能と基盤を扱ってきた Cell から、基盤の判断の負荷が増えたので Platform を別の Cell に分ける例で、移すものと再合意が要る場面を示す。引継ぎの詳細手順は、Core ではなく Profiles が未決として残している。

```svg
<svg viewBox="0 0 880 300" width="880" height="300">
  <rect x="30" y="30" width="260" height="190" rx="10" class="box"/><text x="160" y="62" class="t" text-anchor="middle" font-weight="700">元の Cell</text>
  <rect x="590" y="30" width="260" height="190" rx="10" class="box"/><text x="720" y="62" class="t" text-anchor="middle" font-weight="700">分かれた Cell</text>
  <g class="ts" text-anchor="middle">
    <rect x="330" y="30" width="220" height="30" rx="3" class="hl" style="fill:#fff"/><text x="440" y="51">権限・資源</text>
    <rect x="330" y="66" width="220" height="30" rx="3" class="hl" style="fill:#fff"/><text x="440" y="87">管理対象・記録</text>
    <rect x="330" y="102" width="220" height="30" rx="3" class="hl" style="fill:#fff"/><text x="440" y="123">進行中の Mission・残件</text>
    <rect x="330" y="138" width="220" height="30" rx="3" class="xl" style="fill:#fff"/><text x="440" y="159" class="xc" font-weight="700">まだ果たしていない保証</text>
  </g>
  <path d="M290,184 H586" class="ln" marker-end="url(#arr)"/><text x="440" y="206" class="tx" text-anchor="middle">全部を移す</text>
  <text x="440" y="262" class="t" text-anchor="middle" font-weight="700">移した後に、誰も持たない責任を残さない</text>
</svg>
```

Cell を分ける・まとめる・責務を外すときは、権限から、まだ果たしていない保証までを引き継ぎます。誰も持たない責任と、重なって決める権限を残しません。

## 移すものは、権限から残件まで

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="40" width="200" height="260" rx="10" class="box"/><text x="140" y="76" class="t" text-anchor="middle" font-weight="700">元の Cell</text>
  <rect x="640" y="40" width="200" height="260" rx="10" class="box"/><text x="740" y="76" class="t" text-anchor="middle" font-weight="700">引き継ぐ Cell</text>
  <g class="ts" text-anchor="middle">
    <rect x="300" y="40" width="280" height="34" rx="6" class="h"/><text x="440" y="63" class="on">権限</text>
    <rect x="300" y="84" width="280" height="34" rx="6" class="h"/><text x="440" y="107" class="on">資源</text>
    <rect x="300" y="128" width="280" height="34" rx="6" class="a"/><text x="440" y="151" class="on">管理している対象</text>
    <rect x="300" y="172" width="280" height="34" rx="3" class="lt" style="fill:#fff"/><text x="440" y="195">記録</text>
    <rect x="300" y="216" width="280" height="34" rx="3" class="lt" style="fill:#fff"/><text x="440" y="239">進行中の Mission</text>
    <rect x="300" y="260" width="280" height="34" rx="3" class="lt" style="fill:#fff"/><text x="440" y="283">残件</text>
  </g>
  <path d="M240,170 H296 M584,170 H636" class="ln" marker-end="url(#arr)"/>
  <text x="440" y="340" class="ts sub" text-anchor="middle">分ける・まとめ直す・責務を外す、のどれでも同じ</text>
</svg>
```

分ける・まとめ直す・責務を外す、のどれでも、権限・資源・管理している対象・記録・進行中の Mission・残件を引き継ぎます。

出典: EAA Core 版 6「1. 責務と分割」、EAA Profiles「5. 分離可能な責務」。

## 責任の空白と、決定権の重なり

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <path d="M440,20 V310" class="lt dash"/>
  <text x="220" y="44" class="t xc" text-anchor="middle" font-weight="700">空白</text>
  <text x="660" y="44" class="t xc" text-anchor="middle" font-weight="700">重なり</text>
  <rect x="40" y="80" width="150" height="120" rx="10" class="box"/><text x="115" y="146" class="ts" text-anchor="middle">元の Cell</text>
  <rect x="250" y="80" width="150" height="120" rx="10" class="box"/><text x="325" y="146" class="ts" text-anchor="middle">引き継ぐ Cell</text>
  <rect x="150" y="226" width="140" height="44" rx="3" class="xl" style="fill:#fff"/><text x="220" y="254" class="ts xc" text-anchor="middle">障害の対応</text>
  <text x="220" y="296" class="ts" text-anchor="middle">どちらも自分の担当と思っていない</text>
  <rect x="480" y="80" width="150" height="120" rx="10" class="box"/><text x="555" y="146" class="ts" text-anchor="middle">元の Cell</text>
  <rect x="690" y="80" width="150" height="120" rx="10" class="box"/><text x="765" y="146" class="ts" text-anchor="middle">引き継ぐ Cell</text>
  <rect x="590" y="226" width="140" height="44" rx="3" class="xl" style="fill:#fff"/><text x="660" y="254" class="ts xc" text-anchor="middle">本番への反映</text>
  <path d="M555,200 L630,224 M765,200 L690,224" class="xl"/>
  <text x="660" y="296" class="ts" text-anchor="middle">両方が決めて、食い違う</text>
  <text x="440" y="346" class="ts sub" text-anchor="middle">項目は説明のための例</text>
</svg>
```

引き継ぎでは、どちらの Cell も持っていない責任が残るか、同じことを両方の Cell が決めて食い違うかの失敗が起きます。どちらも残しません。

出典: EAA Core 版 6「1. 責務と分割」。絵の項目は説明のための例で、Core の字ではない。

## まだ果たしていない保証を消さない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="200" height="160" rx="10" class="box"/><text x="140" y="96" class="t" text-anchor="middle" font-weight="700">元の Cell</text>
  <rect x="340" y="60" width="200" height="160" rx="10" class="box"/><text x="440" y="96" class="t" text-anchor="middle" font-weight="700">引き継ぐ Cell</text>
  <rect x="640" y="60" width="200" height="160" rx="10" class="box"/><text x="740" y="96" class="t" text-anchor="middle" font-weight="700">保証を受ける側</text>
  <rect x="80" y="140" width="120" height="44" rx="3" class="hl" style="fill:#fff"/><text x="140" y="168" class="ts hc" text-anchor="middle">約束した保証</text>
  <path d="M200,162 H376" class="ln" marker-end="url(#arr)"/>
  <rect x="380" y="140" width="120" height="44" rx="3" class="hl" style="fill:#fff"/><text x="440" y="168" class="ts hc" text-anchor="middle">約束した保証</text>
  <path d="M540,162 H636" class="hl"/>
  <rect x="200" y="256" width="480" height="86" rx="10" class="soft"/>
  <text x="440" y="290" class="ts" text-anchor="middle" font-weight="700">保証の中身を変えるなら</text>
  <text x="440" y="320" class="ts" text-anchor="middle">保証を受ける側と、合意し直す</text>
</svg>
```

まだ果たしていない保証は、分けても消しません。引き継ぐ Cell に移します。外に約束した保証を変えるなら、関係する相手と合意し直します。

出典: EAA Core 版 6「1. 責務と分割」、EAA Profiles「5.」。

## 例：業務と基盤を一つの Cell で扱う

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="140" y="30" width="600" height="280" rx="10" class="box"/><text x="170" y="64" class="t" font-weight="700">Cell</text>
  <rect x="400" y="46" width="80" height="40" rx="6" class="h"/><text x="440" y="72" class="ts on" text-anchor="middle">責任者</text>
  <rect x="180" y="116" width="240" height="70" rx="3" class="hl" style="fill:#fff"/><text x="300" y="158" class="ts hc" text-anchor="middle">業務機能</text>
  <rect x="460" y="116" width="240" height="70" rx="3" class="hl" style="fill:#fff"/><text x="580" y="158" class="ts hc" text-anchor="middle">基盤</text>
  <rect x="200" y="220" width="200" height="44" rx="22" class="a"/><text x="300" y="248" class="ts on" text-anchor="middle">Agent が作る</text>
  <rect x="480" y="220" width="200" height="44" rx="22" class="a"/><text x="580" y="248" class="ts on" text-anchor="middle">Agent が作る</text>
  <text x="440" y="350" class="ts sub" text-anchor="middle">判断は、どちらも同じ責任者がする</text>
</svg>
```

ここから、一つの例で追います。最初は一つの Cell が、業務の機能と基盤の両方を扱っています。判断は一人の責任者がしています。

出典: EAA 考え方と開発の姿「5. IaC 化から Platform を分離する例」。構成の例で、効果を実証したものではない。

## 例：基盤の判断が続けて増える

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="30" width="460" height="280" rx="10" class="box"/><text x="70" y="64" class="t" font-weight="700">Cell</text>
  <rect x="230" y="46" width="80" height="40" rx="6" class="h"/><text x="270" y="72" class="ts on" text-anchor="middle">責任者</text>
  <g><use href="#i-wait" x="80" y="120" width="22" height="30"/><use href="#i-wait" x="110" y="120" width="22" height="30"/><use href="#i-wait" x="140" y="120" width="22" height="30"/><use href="#i-wait" x="170" y="120" width="22" height="30"/><use href="#i-wait" x="200" y="120" width="22" height="30"/><use href="#i-wait" x="230" y="120" width="22" height="30"/></g>
  <text x="170" y="180" class="ts" text-anchor="middle">基盤の判断待ち</text>
  <rect x="300" y="116" width="170" height="40" rx="3" class="hl" style="fill:#fff"/><text x="385" y="142" class="ts hc" text-anchor="middle">業務機能</text>
  <rect x="80" y="220" width="380" height="60" rx="3" class="hl" style="fill:#fff"/><text x="270" y="256" class="ts hc" text-anchor="middle">Platform の責務を Profile に書く</text>
  <path d="M500,250 H560" class="ln" marker-end="url(#arr)"/>
  <rect x="570" y="190" width="270" height="120" rx="10" class="soft"/>
  <rect x="650" y="206" width="110" height="40" rx="6" class="h"/><text x="705" y="232" class="ts on" text-anchor="middle">別の責任者</text>
  <text x="705" y="276" class="ts" text-anchor="middle">引き受けることを合意する</text>
</svg>
```

基盤についての判断が、続けて増えてきました。そこで Platform の責務を Profile に書き、別の責任者がそれを引き受けることを合意します。

出典: EAA 考え方と開発の姿「5.」。Role Model の呼び名では、ここで別の Operator が引き受ける。

## 例：移してから、独立させる

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="40" width="260" height="240" rx="10" class="box"/><text x="170" y="76" class="t" text-anchor="middle" font-weight="700">元の Cell</text>
  <rect x="130" y="94" width="80" height="40" rx="6" class="h"/><text x="170" y="120" class="ts on" text-anchor="middle">責任者</text>
  <rect x="80" y="160" width="180" height="44" rx="3" class="hl" style="fill:#fff"/><text x="170" y="188" class="ts hc" text-anchor="middle">業務機能</text>
  <rect x="580" y="40" width="260" height="240" rx="10" class="box"/><text x="710" y="76" class="t" text-anchor="middle" font-weight="700">Platform の Cell</text>
  <rect x="670" y="94" width="80" height="40" rx="6" class="h"/><text x="710" y="120" class="ts on" text-anchor="middle">責任者</text>
  <rect x="620" y="160" width="180" height="44" rx="3" class="hl" style="fill:#fff"/><text x="710" y="188" class="ts hc" text-anchor="middle">基盤</text>
  <g class="ts" text-anchor="middle"><text x="440" y="70">権限</text><text x="440" y="100">資源</text><text x="440" y="130">資産</text><text x="440" y="160">記録</text><text x="440" y="190">残件</text></g>
  <path d="M300,216 H576" class="ln" marker-end="url(#arr)"/><text x="440" y="240" class="tx" text-anchor="middle">移す</text>
  <text x="440" y="330" class="t" text-anchor="middle" font-weight="700">分かれた後は、横に並ぶ別の Cell</text>
</svg>
```

権限・資源・資産・記録・残件を移し、Platform の Cell を独立させます。分かれた後は、どちらも横に並ぶ別の Cell です。

出典: EAA 考え方と開発の姿「5.」。

## 例：以後の変更は、提案と受入で

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="260" height="220" rx="10" class="box"/><text x="170" y="96" class="t" text-anchor="middle" font-weight="700">Platform の Cell</text>
  <rect x="580" y="60" width="260" height="220" rx="10" class="box"/><text x="710" y="96" class="t" text-anchor="middle" font-weight="700">業務の Cell</text>
  <path d="M300,140 H576" class="ln" marker-end="url(#arr)"/><use href="#i-pr" x="425" y="100" width="30" height="38"/><text x="440" y="164" class="ts" text-anchor="middle">CI/CD の変更を PR で提案</text>
  <use href="#i-ok" x="616" y="126" width="28" height="28"/><text x="730" y="146" class="ts okc" text-anchor="middle">受け入れるか決める</text>
  <path d="M576,230 H304" class="ln" marker-end="url(#arr)"/><text x="440" y="220" class="ts" text-anchor="middle">提供の条件を変えてほしい</text>
  <use href="#i-ok" x="92" y="140" width="26" height="26"/><text x="200" y="159" class="ts okc" text-anchor="middle">受け入れるか決める</text>
  <text x="440" y="330" class="t" text-anchor="middle" font-weight="700">どちらの向きでも、相手の中を直接変えない</text>
</svg>
```

分かれた後は、CI/CD の変更も基盤の改善も、互いに提案し、相手が受け入れるかを決めます。Platform の Cell も、業務の Cell の中を直接は変えません。

出典: EAA 考え方と開発の姿「5.」。提案と受入の手続きは第 9 章で見ます。

## 例：効果は判断の集中と保証で見る

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="40" width="800" height="70" rx="10" class="soft"/>
  <text x="440" y="84" class="t" text-anchor="middle" font-weight="700">分けて変わるのは、責務を担う主体と、つなぎ方</text>
  <text x="440" y="160" class="ts sub" text-anchor="middle">分けた効果を、次の項目で確かめる</text>
  <rect x="80" y="186" width="340" height="110" rx="10" class="box"/><text x="250" y="226" class="ts" text-anchor="middle" font-weight="700">元の責任者への判断の集中</text><text x="250" y="262" class="ts" text-anchor="middle">減ったか</text>
  <rect x="460" y="186" width="340" height="110" rx="10" class="box"/><text x="630" y="226" class="ts" text-anchor="middle" font-weight="700">成果と外への保証</text><text x="630" y="262" class="ts" text-anchor="middle">保てたか</text>
  <text x="440" y="344" class="ts sub" text-anchor="middle">どちらも、確かめる項目で、確かめた結果ではない</text>
</svg>
```

分けて変わるのは、責務を担う主体とつなぎ方です。元の責任者への判断の集中が減ったか、成果と外への保証を保てたかで、分けた効果を確かめます。

※ 確かめる項目を挙げたもので、この例で効果が出たという実測ではありません。出典: EAA 考え方と開発の姿「5.」。

## Core はここまでしか決めていない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="30" width="380" height="290" rx="10" class="soft"/>
  <text x="60" y="64" class="t" font-weight="700">Core が決めていること</text>
  <g class="ts"><use href="#i-ok" x="60" y="88" width="22" height="22"/><text x="92" y="105">移すもの</text>
  <use href="#i-ok" x="60" y="128" width="22" height="22"/><text x="92" y="145">空白と重なりを残さない</text>
  <use href="#i-ok" x="60" y="168" width="22" height="22"/><text x="92" y="185">まだ果たしていない保証を消さない</text>
  <use href="#i-ok" x="60" y="208" width="22" height="22"/><text x="92" y="225">保証を変えるなら合意し直す</text></g>
  <rect x="460" y="30" width="380" height="290" rx="10" fill="url(#hatch)"/>
  <text x="480" y="64" class="t" font-weight="700">決めていないこと</text>
  <g class="ts"><text x="480" y="102" class="ts" font-weight="700">既知の不足（Core の冒頭が挙げた）</text><text x="480" y="126" class="tx">詳しい手順は未定。いつ決めるかは書いていない</text><text x="480" y="156" class="ts">移行中の責任（分割に当たるかは未定）</text><text x="480" y="202" class="ts" font-weight="700">Profiles が未決・未確定とした</text><text x="480" y="232" class="ts">引き継ぎの細かい手順</text><text x="480" y="262" class="ts">分離・再統合の移行の手順</text></g>
  <text x="440" y="356" class="ts sub" text-anchor="middle">手順が未定の調整を、ほかの Cell からの一方的な強制で埋めない</text>
</svg>
```

何を移し、何を残してはいけないかは Core が決めています。引き継ぎと移行の手順は Profiles が未確定としています。

出典: EAA Core 版 6 冒頭の観測欄・「2.」、EAA Profiles「5.」「10.」。※ Core の「移行」は版の移行（「3.」）の語で、分割の引き継ぎに当たるかは決まらない。
