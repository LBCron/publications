# 第 8 章　Contract は、結ぶ Cell のすべてが同じ版を採用して成立する

群: Evidence・Mission・Contract と版

<!--
構造: agent-hub-roles-kaz/philosopher/2026-11-07-eaa-textbook-structure.md（55553ae4）。章題と群の札の字は writer-ja/drafts/eaa-toc/titles.md（d21b0d80、@ope-ultp1635 msg 65a67e15）で書き直した。構造は変えない。
出どころ（構造の表のまま）: core.md:38・80・98-104、素材 3。Core は publications origin/main 0d07f75 の core.md 版 6。
本文: @ope-ultp1635 msg f202fb67（群三）。
リードの「Contract に何を書くか」は、骨格で題から外してリードに置いた主張（titles.md「短さと中身のどちらを取ったか」）。本文の 2・3 ページ目（書く欄・例）で受けた。
素材 3 は Core 版 2 を定義元にしている。欄と問い・在庫と物流の例・「所有者が片側でも片側だけでは変わらない」・発注側の立ち位置は素材 3 から取り、版 6 の行に当て直した（欄 core.md:38、成立 80、所有者 98、採用 79・91）。素材 3「07 未決」の 4 件のうち「所有者が Cell を抜けたとき」は版 6 の 99-102 行で決まったので、未決には入れていない。「所有者自身の改訂の承認者」は版 6 にも書かれていない（94 行は提起者の承認を禁じ、98 行は所有者を 1 人とするが、所有者が提起した場合の承認者は書いていない）ので、最後のページに残した。
「埋まらない欄は合意していないこと」「所有者が片側でも片側だけでは変わらない」「発注側は結ぶ Cell の一つとして立つ」は素材 3 の読みで、Core の規定ではない。注に書いた。
Core 版 6 は「契約」「検収」の語を使っていない（core.md を grep で確認）。Supplier の責務は profiles.md:94。
core.md:103-104 は空行と「5. 成果と記録」の見出しで、規定の字は無い。
絵: 在庫と物流の Cell は横に並べ、所有者は物流の Cell の枠の中の人として描く。Contract は二つの Cell のあいだに置き、どちらの枠の中にも入れない。
新しく引く外部の文献は無い。
②（@ope-ultp1635 msg 95d31f1b、@reviewer 2026-11-08 ch06-09 三）: 必要な Evidence の問いを core.md:22（受け取った Cell が作った Cell を介さずに確かめられる形）と core.md:39（成果や判断の成立）に合わせて書き直した。問いの他の 3 本は EAA 紹介 3 のまま。core.md:94 の所有者・観測・準拠先を、第 6 章「Evidence の様式も共有する文書」と同じ形のページにして欄のページの次に置き、例の版 1 にも足した。例の所有者・観測は第 10 章の例と同じ値。準拠先は core.md:94 の字（自己改訂規範アーキテクチャ v1・最小構成に準拠する）から取った。観測・準拠先の語の説明は第 10 章と同じく core.md:11-12 の Core 自身の表から取った。
⑤（@ope-ultp1635 msg 281e5366、@reviewer 3 回目・4 回目）: 後任の合意不成立は core.md:101 が合意不成立として扱うと決め、その間に保たれるものも core.md:99・102・71 が決めているので「決めていること」へ移し、未定は詳しい手順だけとした。契約書との関係は core.md:11 に無いので「Core に書かれていない」。所有者本人の改訂の承認者は「未決」から外し、core.md:90・94・98 を合わせた帰結（承認できる者がいない、第 10 章）として絵の下に書いた。
-->

> Contract には相互の責任・提供条件・入出力・Evidence を書き、所有者・観測・準拠先を持たせる。所有者は結ぶ Cell に属する人間 1 人をそれらの Cell の合意で決め、所有者が離れたら後任が決まるまで改訂は承認されない。

```svg
<svg viewBox="0 0 880 300" width="880" height="300">
  <rect x="30" y="30" width="250" height="180" rx="10" class="box"/><text x="155" y="66" class="t" text-anchor="middle" font-weight="700">在庫の Cell</text>
  <rect x="600" y="30" width="250" height="180" rx="10" class="box"/><text x="725" y="66" class="t" text-anchor="middle" font-weight="700">物流の Cell</text>
  <rect x="680" y="84" width="90" height="36" rx="6" class="h"/><text x="725" y="108" class="ts on" text-anchor="middle">所有者</text>
  <rect x="330" y="40" width="220" height="80" rx="3" class="hl" style="fill:#fff"/><text x="440" y="74" class="ts hc" text-anchor="middle" font-weight="700">Contract　版 1</text><text x="440" y="100" class="tx" text-anchor="middle">責任・条件・入出力・Evidence</text>
  <path d="M280,80 H326 M554,80 H596" class="ln"/>
  <use href="#i-ok" x="141" y="150" width="28" height="28"/><text x="155" y="200" class="ts okc" text-anchor="middle">版 1 を採用</text>
  <use href="#i-ok" x="711" y="150" width="28" height="28"/><text x="725" y="200" class="ts okc" text-anchor="middle">版 1 を採用</text>
  <text x="440" y="170" class="ts" text-anchor="middle" font-weight="700">両方が採用して、成立</text>
  <text x="440" y="264" class="t" text-anchor="middle" font-weight="700">書くのは所有者 1 人。成り立たせるのは、結ぶ Cell の全部</text>
</svg>
```

Contract は、Cell のあいだの続いていく取り決めです。所有者は 1 人でも、結ぶ Cell のすべてが同じ版を採用したときに初めて成り立ちます。

## Contract は、境界の合意

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="240" height="200" rx="10" class="box"/><text x="160" y="96" class="t" text-anchor="middle" font-weight="700">Cell</text>
  <rect x="600" y="60" width="240" height="200" rx="10" class="box"/><text x="720" y="96" class="t" text-anchor="middle" font-weight="700">Cell</text>
  <rect x="320" y="40" width="240" height="110" rx="3" class="hl" style="fill:#fff"/><text x="440" y="76" class="ts hc" text-anchor="middle" font-weight="700">Contract</text><text x="440" y="104" class="ts" text-anchor="middle">どの Evidence を渡すか</text><text x="440" y="128" class="ts" text-anchor="middle">を定める</text>
  <path d="M280,220 H596" class="ln" marker-end="url(#arr)"/><use href="#i-pr" x="425" y="180" width="30" height="38"/><text x="440" y="242" class="ts" text-anchor="middle">Evidence</text>
  <text x="440" y="320" class="t" text-anchor="middle" font-weight="700">Contract が決めた Evidence が、境界を越える</text>
</svg>
```

Contract は、相互の責任、提供条件、入出力、必要な Evidence を定める、Cell のあいだの合意です。どの Evidence を渡すかを、ここで決めます。

出典: EAA Core 版 6 の概念表「Contract」と「0. 目的と範囲」。

## Contract に書く欄と問い

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="20" width="800" height="300" rx="3" class="hl" style="fill:#fff"/>
  <g class="ts">
    <text x="70" y="64" font-weight="700">相互の責任</text><text x="280" y="64">相手に何を約束し、相手から何を約束してもらうか</text>
    <text x="70" y="134" font-weight="700">提供条件</text><text x="280" y="134">どんな条件の下でなら、その約束を守れるか</text>
    <text x="70" y="204" font-weight="700">入出力</text><text x="280" y="204">何を渡し、何を受け取るか。その形は</text>
    <text x="70" y="264" font-weight="700">必要な Evidence</text><text x="280" y="264">何が残っていたら、成果と判断が成り立ったと、</text><text x="280" y="290" font-weight="700">受け取った側が、作った側を介さずに確かめられるか</text>
  </g>
  <path d="M60,96 H820 M60,166 H820 M60,236 H820" class="lt"/>
  <text x="440" y="356" class="ts sub" text-anchor="middle">左が Core の欄。右は、自分の案件で欄を埋めるときの問い</text>
</svg>
```

Contract には、相互の責任、提供条件、入出力、必要な Evidence を書きます。右の問いに、相手の Cell と一緒に答えれば、欄が埋まります。

出典: EAA Core 版 6 の概念表「Contract」「Evidence」と「0.」。※ 問いは EAA 紹介 3 のもの。Evidence の問いだけ、Core の字に合わせて直しました。

## 欄のほかに、所有者・観測・準拠先を持つ

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="70" width="200" height="180" rx="10" class="box"/><text x="140" y="166" class="t" text-anchor="middle" font-weight="700">在庫の Cell</text>
  <rect x="640" y="70" width="200" height="180" rx="10" class="box"/><text x="740" y="166" class="t" text-anchor="middle" font-weight="700">物流の Cell</text>
  <rect x="290" y="40" width="300" height="250" rx="3" class="hl" style="fill:#fff"/>
  <text x="440" y="76" class="t hc" text-anchor="middle" font-weight="700">Contract</text>
  <g class="ts" text-anchor="middle"><text x="440" y="112">相互の責任・提供条件</text><text x="440" y="138">入出力・必要な Evidence</text></g>
  <path d="M310,162 H570" class="lt"/>
  <g class="ts" text-anchor="middle"><text x="440" y="192" font-weight="700">所有者（人間）</text><text x="440" y="220" font-weight="700">観測</text><text x="440" y="248" font-weight="700">準拠先</text></g>
  <g class="tx" text-anchor="middle"><text x="440" y="274">欄だけでは、Contract は揃わない</text></g>
  <path d="M240,160 H286 M594,160 H636" class="ln"/>
  <text x="440" y="330" class="ts sub" text-anchor="middle">Evidence の様式・共有する Profile・共有する Ontology と同じ扱い</text>
</svg>
```

Contract は Cell のあいだで共有する文書なので、欄のほかに所有者・観測・準拠先を持ちます。所有者は人間です。第 6 章の Evidence の様式と同じです。

出典: EAA Core 版 6「4. 提案と変更」。観測・準拠先の意味は第 10 章で見ます。

## 例：在庫と物流の Contract

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="14" width="800" height="352" rx="3" class="hl" style="fill:#fff"/>
  <text x="60" y="42" class="ts hc" font-weight="700">在庫と物流のあいだの Contract　版 1</text>
  <g class="ts">
    <text x="60" y="76" font-weight="700">相互の責任</text><text x="230" y="76">在庫は、引き当て済みの品目だけを指示に載せる</text><text x="230" y="98">物流は、受けた指示を出荷し、結果を返す</text>
    <text x="60" y="134" font-weight="700">提供条件</text><text x="230" y="134">平日 15 時までに受けた指示は、その日のうちに出荷する</text>
    <text x="60" y="170" font-weight="700">入出力</text><text x="230" y="170">渡す：出荷指示（品目・数量・届け先）</text><text x="230" y="192">受け取る：出荷結果（出荷番号・出荷日時・欠品の有無と理由）</text>
    <text x="60" y="228" font-weight="700">必要な Evidence</text><text x="230" y="228">指示と結果を 1 件ずつ突き合わせた記録</text><text x="230" y="250">欠品は理由とともに残す</text>
    <text x="60" y="292" font-weight="700">所有者</text><text x="230" y="292">物流の窓口の責任者</text>
    <text x="60" y="320" font-weight="700">観測</text><text x="230" y="320">受け入れられなかった出荷結果と、その理由</text>
    <text x="60" y="348" font-weight="700">準拠先</text><text x="230" y="348">自己改訂規範アーキテクチャ v1・最小構成</text>
  </g>
  <path d="M60,112 H820 M60,148 H820 M60,206 H820" class="lt"/><path d="M60,266 H820" class="ln"/>
</svg>
```

第 6 章の在庫と物流の例で、欄を埋めた Contract です。相手の中の作り方には触れず、あいだの約束だけを書きます。下の 3 行が所有者・観測・準拠先です。

※ 欄の中身・所有者・観測・版の番号は、EAA 紹介 3 と第 10 章の、説明のための仮定です。準拠先は Core「4. 提案と変更」の字のとおり。

## 埋まらない欄は、まだ合意していない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="40" width="440" height="260" rx="3" class="hl" style="fill:#fff"/>
  <g class="ts"><text x="60" y="84" font-weight="700">相互の責任</text><use href="#i-ok" x="430" y="68" width="22" height="22"/>
  <text x="60" y="144" font-weight="700">提供条件</text>
  <rect x="200" y="122" width="260" height="34" rx="3" fill="url(#hatch-x)"/><text x="330" y="144" class="xc" text-anchor="middle">休日の扱いが決まらない</text>
  <text x="60" y="204" font-weight="700">入出力</text><use href="#i-ok" x="430" y="188" width="22" height="22"/>
  <text x="60" y="264" font-weight="700">必要な Evidence</text><use href="#i-ok" x="430" y="248" width="22" height="22"/></g>
  <path d="M480,140 H556" class="ln" marker-end="url(#arr)"/>
  <rect x="560" y="80" width="280" height="130" rx="10" class="soft"/>
  <text x="700" y="120" class="ts" text-anchor="middle" font-weight="700">まだ合意していないこと</text>
  <text x="700" y="152" class="ts" text-anchor="middle">版 1 を出す前に、</text><text x="700" y="178" class="ts" text-anchor="middle">相手と決める</text>
</svg>
```

埋まらない欄があれば、それは両側でまだ合意していないことです。版を出して採用する前に、相手の Cell と決めます。

※ この読みは EAA 紹介 3 のもので、Core の規定ではありません。休日の扱いは説明のための例です。

## 結ぶ Cell が全部採用して、成立する

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <path d="M120,300 H820" class="ln" marker-end="url(#arr)"/><text x="830" y="326" class="tx" text-anchor="end">時間</text>
  <text x="70" y="110" class="ts" text-anchor="middle" font-weight="700">在庫</text><text x="70" y="190" class="ts" text-anchor="middle" font-weight="700">物流</text>
  <rect x="300" y="86" width="520" height="40" rx="3" class="hl" style="fill:#fff"/><text x="560" y="112" class="ts hc" text-anchor="middle">版 1 を採用中</text>
  <rect x="500" y="166" width="320" height="40" rx="3" class="hl" style="fill:#fff"/><text x="660" y="192" class="ts hc" text-anchor="middle">版 1 を採用中</text>
  <path d="M300,60 V280" class="lt dash"/><text x="300" y="50" class="tx" text-anchor="middle">在庫が採用</text>
  <path d="M500,60 V280" class="ln"/><use href="#i-ok" x="488" y="228" width="24" height="24"/><text x="500" y="274" class="ts okc" text-anchor="middle">ここで成立</text>
  <text x="400" y="150" class="tx" text-anchor="middle">片側だけでは、まだ成り立たない</text>
</svg>
```

Contract は、結ぶ Cell のすべてが同じ版を採用中になったときに、その版で成り立ちます。片方だけが採用しても、まだ効いていません。

出典: EAA Core 版 6「3. 意味と合意」。採用するかを決めるのは、各 Cell の規範の所有者（同「4.」）。

## 所有者は、結ぶ Cell の中の 1 人

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="50" width="260" height="210" rx="10" class="box"/><text x="170" y="86" class="t" text-anchor="middle" font-weight="700">在庫の Cell</text>
  <rect x="580" y="50" width="260" height="210" rx="10" class="box"/><text x="710" y="86" class="t" text-anchor="middle" font-weight="700">物流の Cell</text>
  <rect x="630" y="110" width="160" height="56" rx="6" class="h"/><text x="710" y="134" class="ts on" text-anchor="middle">所有者</text><text x="710" y="156" class="tx on" text-anchor="middle" style="fill:#fff">窓口の責任者</text>
  <rect x="330" y="110" width="220" height="56" rx="3" class="hl" style="fill:#fff"/><text x="440" y="144" class="ts hc" text-anchor="middle">Contract</text>
  <path d="M300,138 H326 M554,138 H576" class="ln"/>
  <rect x="140" y="290" width="600" height="60" rx="10" class="soft"/>
  <text x="440" y="326" class="ts" text-anchor="middle">誰にするかは、作るときに、結ぶ Cell が合意して決める</text>
</svg>
```

Contract の所有者は、Contract を結ぶ Cell に属する人間 1 人です。誰にするかは、Contract を作るときに、それらの Cell が合意して決めます。

出典: EAA Core 版 6「4. 提案と変更」。※ 物流の窓口の責任者を所有者にしたのは、EAA 紹介 3 の例です。

## 所有者が片側でも、片側だけでは変わらない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="40" width="360" height="140" rx="10" class="box"/><text x="220" y="76" class="t" text-anchor="middle" font-weight="700">所有者が決められること</text>
  <text x="220" y="116" class="ts" text-anchor="middle">Contract の本文と版</text><text x="220" y="144" class="ts" text-anchor="middle">（改訂の承認）</text>
  <rect x="480" y="40" width="360" height="140" rx="10" class="box"/><text x="660" y="76" class="t" text-anchor="middle" font-weight="700">各 Cell が決めること</text>
  <text x="660" y="116" class="ts" text-anchor="middle">その版を採用するか</text>
  <path d="M400,110 H476" class="ln" marker-end="url(#arr)"/>
  <rect x="40" y="220" width="800" height="110" rx="10" class="soft"/>
  <text x="440" y="258" class="ts" text-anchor="middle">在庫が新しい版を採用しなければ、前の版のまま</text>
  <text x="440" y="292" class="t" text-anchor="middle" font-weight="700">採用が、両側の同意になっている</text>
</svg>
```

所有者が決められるのは本文と版までで、版が相手を縛るのは、相手がその版を採用したときだけです。所有者の Cell の都合だけでは、取り決めは変わりません。

※ これは EAA 紹介 3 の読みで、Core の「3. 意味と合意」「4. 提案と変更」の行から導いたものです。Core が書いた理由ではありません。

## 結んでいない者は、所有者にならない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="40" width="240" height="160" rx="10" class="box"/><text x="160" y="126" class="t" text-anchor="middle" font-weight="700">在庫の Cell</text>
  <rect x="600" y="40" width="240" height="160" rx="10" class="box"/><text x="720" y="126" class="t" text-anchor="middle" font-weight="700">物流の Cell</text>
  <rect x="330" y="92" width="220" height="56" rx="3" class="hl" style="fill:#fff"/><text x="440" y="126" class="ts hc" text-anchor="middle">Contract</text>
  <path d="M280,120 H326 M554,120 H596" class="ln"/>
  <rect x="330" y="250" width="220" height="70" rx="10" class="box"/><text x="440" y="282" class="ts" text-anchor="middle">発注側の部門</text><text x="440" y="306" class="tx" text-anchor="middle">この Contract を結んでいない</text>
  <path d="M440,246 V154" class="xl dash" marker-end="url(#arr-x)"/><use href="#i-no" x="452" y="190" width="24" height="24"/>
  <text x="680" y="290" class="ts" text-anchor="middle">持つなら、結ぶ Cell の</text><text x="680" y="316" class="ts" text-anchor="middle">一つとして立つ</text>
</svg>
```

所有者になれるのは、その Contract を結ぶ Cell に属する人だけです。結んでいない部門が、外からあいだの取り決めを持つことはありません。

出典: EAA Core 版 6「4. 提案と変更」。※ 発注側の立ち位置は EAA 紹介 3 の読みで、Core は発注側について書いていません。

## 所有者が離れたら、改訂は止まる

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <path d="M60,250 H820" class="ln" marker-end="url(#arr)"/><text x="830" y="276" class="tx" text-anchor="end">時間</text>
  <rect x="60" y="150" width="260" height="60" rx="6" class="h"/><text x="190" y="186" class="ts on" text-anchor="middle">所有者がいる</text>
  <path d="M330,120 V260" class="xl"/><text x="330" y="110" class="ts xc" text-anchor="middle">結ぶ Cell のどれにも属さなくなった</text>
  <rect x="340" y="150" width="260" height="60" rx="6" fill="url(#hatch)"/><text x="470" y="186" class="ts" text-anchor="middle">改訂は承認されない</text>
  <rect x="610" y="150" width="210" height="60" rx="6" class="h"/><text x="715" y="186" class="ts on" text-anchor="middle">後任が決まった</text>
  <rect x="60" y="294" width="760" height="56" rx="10" class="soft"/><text x="440" y="328" class="ts" text-anchor="middle">成立している版と、承認済みの版の採用は、これで変わらない</text>
</svg>
```

所有者が、結ぶ Cell のどれにも属さなくなったら、その人は以後の改訂を承認しません。後任が決まるまで改訂は承認されませんが、成立している版は効き続けます。

出典: EAA Core 版 6「4. 提案と変更」。

## 後任も、結ぶ Cell の合意で決める

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="30" width="800" height="80" rx="10" class="soft"/><use href="#i-ok" x="60" y="56" width="26" height="26"/>
  <text x="100" y="76" class="t" font-weight="700">作るときと同じく、Contract を結ぶ Cell が合意して決める</text>
  <text x="60" y="150" class="ts" font-weight="700">次のどれも、それだけでは後任の根拠にならない</text>
  <g class="ts">
    <use href="#i-no" x="60" y="172" width="22" height="22"/><text x="92" y="189">離れた所有者が指名した</text>
    <use href="#i-no" x="460" y="172" width="22" height="22"/><text x="492" y="189">所有者が属していた Cell だけで決めた</text>
    <use href="#i-no" x="60" y="222" width="22" height="22"/><text x="92" y="239">Cell の親子関係</text>
    <use href="#i-no" x="460" y="222" width="22" height="22"/><text x="492" y="239">Agent が申告した</text>
  </g>
  <rect x="40" y="280" width="800" height="60" rx="10" class="box"/><text x="440" y="316" class="ts" text-anchor="middle">後任が決まっても、承認されていなかった改訂が承認されたことにはならない</text>
</svg>
```

後任も、作るときと同じく、結ぶ Cell が合意して決めます。前の所有者の指名や、片側の Cell だけの決定、親子関係、Agent の申告は、単独では根拠になりません。

出典: EAA Core 版 6「4. 提案と変更」。

## 所有者がいない間も、止めることはできる

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="40" width="390" height="230" rx="10" class="soft"/>
  <text x="235" y="78" class="t" text-anchor="middle" font-weight="700">使える</text>
  <use href="#i-ok" x="221" y="96" width="28" height="28"/>
  <text x="235" y="156" class="ts" text-anchor="middle">Contract と各 Cell の規範で</text><text x="235" y="182" class="ts" text-anchor="middle">すでに認められている</text><text x="235" y="208" class="ts" text-anchor="middle" font-weight="700">停止・取消</text>
  <rect x="450" y="40" width="390" height="230" rx="10" class="xl" style="fill:#fff"/>
  <text x="645" y="78" class="t xc" text-anchor="middle" font-weight="700">根拠にしない</text>
  <use href="#i-no" x="631" y="96" width="28" height="28"/>
  <text x="645" y="156" class="ts" text-anchor="middle">「緊急だから」「元に戻せるから」を</text><text x="645" y="182" class="ts" text-anchor="middle">改訂の承認や</text><text x="645" y="208" class="ts" text-anchor="middle">新しい権限の理由にする</text>
  <text x="440" y="320" class="ts sub" text-anchor="middle">所有者がいない間、Contract は所有者を持たない（後任までの例外）</text>
</svg>
```

所有者がいない間も、すでに認められている停止・取消は使えます。ただ、緊急であることや元に戻せることを、改訂の承認や新しい権限の理由にはしません。

出典: EAA Core 版 6「4. 提案と変更」。

## Core はここまでしか決めていない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="30" width="380" height="290" rx="10" class="soft"/>
  <text x="60" y="64" class="t" font-weight="700">Core が決めていること</text>
  <g class="ts"><use href="#i-ok" x="60" y="88" width="22" height="22"/><text x="92" y="105">Contract に書く欄</text>
  <use href="#i-ok" x="60" y="128" width="22" height="22"/><text x="92" y="145">全部が採用して成立</text>
  <use href="#i-ok" x="60" y="168" width="22" height="22"/><text x="92" y="185">所有者の決め方と、後任の決め方</text>
  <use href="#i-ok" x="60" y="208" width="22" height="22"/><text x="92" y="225">所有者がいない間の扱い</text>
  <use href="#i-ok" x="60" y="248" width="22" height="22"/><text x="92" y="265">後任の合意不成立は、合意不成立</text>
  <use href="#i-ok" x="60" y="288" width="22" height="22"/><text x="92" y="305">所有者・観測・準拠先を持つ</text></g>
  <rect x="460" y="30" width="380" height="290" rx="10" fill="url(#hatch)"/>
  <text x="480" y="64" class="t" font-weight="700">決めていないこと</text>
  <g class="ts"><text x="480" y="102" class="ts" font-weight="700">既知の不足（Core の冒頭が挙げた）</text><text x="480" y="132" class="ts">合意不成立の詳しい手順</text><text x="480" y="182" class="ts" font-weight="700">Core に書かれていない</text><text x="480" y="206" class="tx">既知の不足にも、決める予定にも無い</text><text x="480" y="242" class="ts">商取引上の契約書との関係</text></g>
  <text x="440" y="356" class="ts sub" text-anchor="middle">所有者本人が提起した改訂は、Core の字の範囲では承認できる者がいない（第 10 章）</text>
</svg>
```

後任の合意が成り立たなければ、合意不成立として扱います。未定なのは、その詳しい手順です。商取引上の契約書との関係は、Core に書かれていません。

出典: EAA Core 版 6 冒頭の観測欄（合意不成立）と「2.」「4.」。契約主体をまたぐ責任と受入は EAA Profiles「6.」の Supplier の責務。
