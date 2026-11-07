# 第 6 章　境界を越えるのは Evidence で、語の定義は両側がそれぞれ持つ

群: Evidence・Mission・Contract と版

<!--
構造: agent-hub-roles-kaz/philosopher/2026-11-07-eaa-textbook-structure.md（55553ae4）。章題と群の札の字は writer-ja/drafts/eaa-toc/titles.md（d21b0d80、@ope-ultp1635 msg 65a67e15）で書き直した。構造は変えない。
出どころ（構造の表のまま）: core.md:20-24・36・39-41・75-76。Core は publications origin/main 0d07f75 の core.md 版 6。
本文: @ope-ultp1635 msg f202fb67（群三）。
足した出どころ: 群三の通しの例（在庫と物流）は素材 3（drafts/agentic-agile-materials/explanations/eaa/3-hand-over-versions.html）。素材 3 は Core 版 2 を定義元にしているので、取った箇所は版 6 の行に当て直した。Evidence になる記録の例は delivery-guide.md:203-212（Evidence Graph の node 例）。英語の node 名は日本語に開いた（「production trace」→「本番の実行記録」など）。開いたことは注に書いた。
「出荷日」の意味のずれは、説明のための例で、素材 3 にも Core にも無い。注に書いた。
共有する Ontology・Evidence の様式の所有者をどう決めるかは、core.md:94 が所有者を持つことを求めるだけで、決め方は Contract（core.md:98-102）にしか書いていない。最後のページに書いた。
包含と同じ形の字として、profiles.md:107「EnterpriseのOntology」と development-model.md:45「DomainからEnterpriseへのOntology訂正」は使っていない（Ontology を全体の側が一つ持つ形で、core.md:21「境界の両側が保持する」と食い違う。development-model.md:24 の Enterprise／Domain と同じ字の組）。
絵: Cell はどれもほかの Cell の枠の外に並べる（core.md:43）。
新しく引く外部の文献は無い。
-->

> Evidence は、受け取った Cell が、作った Cell を介さずに確かめられる形にする。意味のずれは Evidence が受け入れられなかったときに見えるので、推測で越えずに照会か変更提案で解く。

```svg
<svg viewBox="0 0 880 300" width="880" height="300">
  <rect x="30" y="30" width="280" height="200" rx="10" class="box"/><text x="170" y="64" class="t" text-anchor="middle" font-weight="700">作った Cell</text>
  <rect x="570" y="30" width="280" height="200" rx="10" class="box"/><text x="710" y="64" class="t" text-anchor="middle" font-weight="700">受け取った Cell</text>
  <rect x="60" y="150" width="220" height="56" rx="6" class="soft"/><text x="170" y="184" class="ts" text-anchor="middle">この Cell の Ontology</text>
  <rect x="600" y="150" width="220" height="56" rx="6" class="soft"/><text x="710" y="184" class="ts" text-anchor="middle">この Cell の Ontology</text>
  <path d="M310,100 H566" class="ln" marker-end="url(#arr)"/><use href="#i-pr" x="425" y="62" width="30" height="38"/><text x="440" y="124" class="ts" text-anchor="middle" font-weight="700">Evidence</text>
  <path d="M310,178 H566" class="xl dash"/><use href="#i-no" x="428" y="166" width="24" height="24"/><text x="440" y="214" class="tx" text-anchor="middle">語の定義は越えない</text>
  <text x="440" y="270" class="t" text-anchor="middle" font-weight="700">越えるのは記録。読むための語は、両側がそれぞれ持つ</text>
</svg>
```

境界を越えるのは、成果や判断の成立を確かめる記録です。読むための語の定義は、両側の Cell がそれぞれ持ちます。

## 越えるのは、確かめる記録

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="240" height="200" rx="10" class="box"/><text x="160" y="96" class="t" text-anchor="middle" font-weight="700">Cell</text>
  <rect x="600" y="60" width="240" height="200" rx="10" class="box"/><text x="720" y="96" class="t" text-anchor="middle" font-weight="700">Cell</text>
  <rect x="80" y="140" width="160" height="44" rx="3" class="hl" style="fill:#fff"/><text x="160" y="168" class="ts hc" text-anchor="middle">成果・判断</text>
  <path d="M280,162 H596" class="ln" marker-end="url(#arr)"/><use href="#i-pr" x="425" y="118" width="30" height="38"/>
  <text x="440" y="186" class="ts" text-anchor="middle" font-weight="700">Evidence</text>
  <text x="440" y="210" class="tx" text-anchor="middle">成立したことを確かめられる記録</text>
  <text x="440" y="320" class="t" text-anchor="middle" font-weight="700">Cell どうしは、この記録で互いの成果の上に積む</text>
</svg>
```

Cell の境界を越えるのは、成果や判断が成り立ったことを確かめる記録で、これを Evidence と呼びます。受け取った Cell は、確かめて次の成果を積みます。

出典: EAA Core 版 6「0. 目的と範囲」と概念表「Evidence」。

## Evidence になる記録の例

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <g class="ts" text-anchor="middle">
    <rect x="40" y="50" width="185" height="64" rx="3" class="lt" style="fill:#fff"/><text x="132" y="88">PR</text>
    <rect x="245" y="50" width="185" height="64" rx="3" class="lt" style="fill:#fff"/><text x="337" y="88">実行できるテスト</text>
    <rect x="450" y="50" width="185" height="64" rx="3" class="lt" style="fill:#fff"/><text x="542" y="88">CI の実行結果</text>
    <rect x="655" y="50" width="185" height="64" rx="3" class="lt" style="fill:#fff"/><text x="747" y="88">本番の実行記録</text>
    <rect x="40" y="134" width="185" height="64" rx="3" class="lt" style="fill:#fff"/><text x="132" y="172">突き合わせの結果</text>
    <rect x="245" y="134" width="185" height="64" rx="3" class="lt" style="fill:#fff"/><text x="337" y="172">切り戻しの結果</text>
    <rect x="450" y="134" width="185" height="64" rx="3" class="lt" style="fill:#fff"/><text x="542" y="172">人間の判断の記録</text>
    <rect x="655" y="134" width="185" height="64" rx="3" class="lt" style="fill:#fff"/><text x="747" y="172">外部の確認</text>
  </g>
  <rect x="40" y="236" width="800" height="90" rx="10" class="soft"/>
  <text x="440" y="272" class="t" text-anchor="middle" font-weight="700">どれも、作った側に聞かずに確かめられる形で残す</text>
  <text x="440" y="304" class="ts sub" text-anchor="middle">どれを Evidence にするかは、Cell のあいだで決める</text>
</svg>
```

PR、テスト、CI の実行結果、本番の実行記録、突き合わせや切り戻しの結果、人間の判断の記録などが Evidence になります。

出典: EAA Delivery Guide「8.」の Evidence Graph の例（適用例）。英語の名前は日本語に開いた（Actions・production trace など）。

## 作った Cell を介さずに確かめる

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="70" width="240" height="200" rx="10" class="box"/><text x="160" y="106" class="t" text-anchor="middle" font-weight="700">作った Cell</text>
  <rect x="600" y="70" width="240" height="200" rx="10" class="box"/><text x="720" y="106" class="t" text-anchor="middle" font-weight="700">受け取った Cell</text>
  <path d="M280,150 H596" class="ln" marker-end="url(#arr)"/><use href="#i-pr" x="425" y="110" width="30" height="38"/><text x="440" y="172" class="ts" text-anchor="middle">Evidence</text>
  <use href="#i-ok" x="636" y="140" width="28" height="28"/><text x="750" y="160" class="ts okc" text-anchor="middle">記録だけで確かめる</text>
  <path d="M596,236 H284" class="xl dash" marker-end="url(#arr-x)"/><use href="#i-no" x="428" y="214" width="24" height="24"/><text x="440" y="262" class="ts xc" text-anchor="middle">「本当に合っていますか」と聞かないと分からない</text>
  <text x="440" y="330" class="t" text-anchor="middle" font-weight="700">確かめるのは、受け取った Cell</text>
</svg>
```

ほかの Cell は判断を上書きしないので、確かめるのは受け取った Cell です。だから Evidence は、作った Cell に聞かずに記録だけで確かめられる形にします。

出典: EAA Core 版 6「0. 目的と範囲」。上書きしないことは第 4 章で見ました。

## 例：在庫と物流のあいだ

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="50" width="260" height="210" rx="10" class="box"/><text x="170" y="86" class="t" text-anchor="middle" font-weight="700">在庫の Cell</text><text x="170" y="114" class="tx" text-anchor="middle">中は Scrum（自社のチーム）</text>
  <rect x="580" y="50" width="260" height="210" rx="10" class="box"/><text x="710" y="86" class="t" text-anchor="middle" font-weight="700">物流の Cell</text><text x="710" y="114" class="tx" text-anchor="middle">中は委託先の標準工程</text>
  <path d="M300,150 H576" class="ln" marker-end="url(#arr)"/><text x="440" y="140" class="ts" text-anchor="middle">出荷指示</text>
  <path d="M576,214 H304" class="ln" marker-end="url(#arr)"/><text x="440" y="204" class="ts" text-anchor="middle">出荷結果</text>
  <rect x="200" y="290" width="480" height="60" rx="6" class="soft"/><text x="440" y="316" class="ts" text-anchor="middle" font-weight="700">Evidence：指示と結果を 1 件ずつ突き合わせた記録</text><text x="440" y="340" class="tx" text-anchor="middle">欠品は理由とともに残す</text>
</svg>
```

この群では一つの例を使い続けます。在庫の Cell が物流の Cell に出荷を指示し、物流は出荷して結果を返します。二つの Cell の中の作り方は違います。

※ 在庫・物流の例と Evidence の中身は、EAA 紹介 3 の、説明のための仮定です。第 7〜12 章でも使います。

## 語の定義は、両側がそれぞれ持つ

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="50" width="300" height="230" rx="10" class="box"/><text x="190" y="86" class="t" text-anchor="middle" font-weight="700">在庫の Cell</text>
  <rect x="540" y="50" width="300" height="230" rx="10" class="box"/><text x="690" y="86" class="t" text-anchor="middle" font-weight="700">物流の Cell</text>
  <rect x="70" y="110" width="240" height="140" rx="6" class="soft"/><text x="190" y="140" class="ts" text-anchor="middle" font-weight="700">在庫の Ontology</text>
  <g class="ts"><text x="90" y="174">品目：</text><text x="90" y="200">数量：</text><text x="90" y="226">出荷日：</text></g>
  <rect x="570" y="110" width="240" height="140" rx="6" class="soft"/><text x="690" y="140" class="ts" text-anchor="middle" font-weight="700">物流の Ontology</text>
  <g class="ts"><text x="590" y="174">品目：</text><text x="590" y="200">数量：</text><text x="590" y="226">出荷日：</text></g>
  <path d="M340,170 H536" class="xl dash"/><use href="#i-no" x="426" y="158" width="28" height="28"/>
  <text x="440" y="326" class="t" text-anchor="middle" font-weight="700">Ontology は境界を越えて流れない</text>
</svg>
```

語の意味を定めた共通語の定義を Ontology と呼びます。Ontology は境界を越えず、両側の Cell がそれぞれ持ちます。Evidence はそれで読みます。

出典: EAA Core 版 6「0. 目的と範囲」と概念表「Ontology」。

## ずれは、受け入れなかったときに見える

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="240" height="190" rx="10" class="box"/><text x="160" y="96" class="t" text-anchor="middle" font-weight="700">物流の Cell</text>
  <text x="160" y="146" class="ts" text-anchor="middle">出荷日 ＝</text><text x="160" y="172" class="ts" text-anchor="middle">配送業者に渡した日</text>
  <rect x="600" y="60" width="240" height="190" rx="10" class="box"/><text x="720" y="96" class="t" text-anchor="middle" font-weight="700">在庫の Cell</text>
  <text x="720" y="146" class="ts" text-anchor="middle">出荷日 ＝</text><text x="720" y="172" class="ts" text-anchor="middle">倉庫を出た日</text>
  <path d="M280,124 H596" class="ln" marker-end="url(#arr)"/><use href="#i-pr" x="425" y="86" width="26" height="32"/><text x="440" y="148" class="tx" text-anchor="middle">出荷結果の Evidence</text>
  <use href="#i-no" x="706" y="200" width="28" height="28"/><text x="720" y="282" class="ts xc" text-anchor="middle">突き合わせが合わない</text>
  <text x="440" y="336" class="t" text-anchor="middle" font-weight="700">意味のずれは、ここで初めて見える</text>
</svg>
```

同じ語でも、両側の Ontology で意味が違うことがあります。そのずれは、Evidence が受け入れられなかったときに見えるようになります。

※ 「出荷日」のずれは説明のための例で、Core にも EAA 紹介 3 にもありません。出典: EAA Core 版 6「0. 目的と範囲」。

## 推測で越えず、照会か変更提案で解く

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="40" width="800" height="70" rx="10" class="xl" style="fill:#fff"/>
  <use href="#i-no" x="60" y="62" width="26" height="26"/><text x="100" y="82" class="ts">「たぶん倉庫を出た日のことだろう」と読み替えて受け入れる</text>
  <rect x="40" y="140" width="390" height="180" rx="10" class="soft"/>
  <text x="235" y="178" class="t" text-anchor="middle" font-weight="700">照会する</text>
  <text x="235" y="216" class="ts" text-anchor="middle">「この出荷日は何の日か」を</text><text x="235" y="242" class="ts" text-anchor="middle">相手に聞く</text>
  <rect x="450" y="140" width="390" height="180" rx="10" class="soft"/>
  <text x="645" y="178" class="t" text-anchor="middle" font-weight="700">変更を提案する</text>
  <text x="645" y="216" class="ts" text-anchor="middle">Contract の入出力に</text><text x="645" y="242" class="ts" text-anchor="middle">「倉庫を出た日」の欄を足す</text>
  <text x="440" y="358" class="ts sub" text-anchor="middle">どちらでも、違いと、どう対応させたかを残す</text>
</svg>
```

ずれを見つけても、推測で読み替えて受け入れません。照会するか変更を提案して解き、意味の違いと対応を残します。

出典: EAA Core 版 6「0. 目的と範囲」「3. 意味と合意」。提案の手続きは第 9 章で見ます。

## Ontology の対応は、ずれから足す

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <path d="M100,300 H800" class="ln" marker-end="url(#arr)"/><text x="810" y="326" class="tx" text-anchor="end">時間</text>
  <g class="ts" text-anchor="middle">
    <rect x="80" y="180" width="180" height="60" rx="6" class="soft"/><text x="170" y="216">受け入れられない</text>
    <rect x="350" y="180" width="180" height="60" rx="6" class="soft"/><text x="440" y="216">照会・変更提案</text>
    <rect x="620" y="180" width="180" height="60" rx="3" class="hl" style="fill:#fff"/><text x="710" y="216" class="hc">対応を足す</text>
  </g>
  <path d="M260,210 H346" class="ln" marker-end="url(#arr)"/><path d="M530,210 H616" class="ln" marker-end="url(#arr)"/>
  <rect x="560" y="60" width="300" height="90" rx="6" class="box"/><text x="710" y="94" class="ts" text-anchor="middle">物流の「出荷日」＝ 配送業者に渡した日</text><text x="710" y="122" class="ts" text-anchor="middle">在庫の「出荷日」＝ 倉庫を出た日</text>
  <path d="M710,176 V154" class="ln" marker-end="url(#arr)"/>
  <text x="250" y="110" class="ts sub" text-anchor="middle">初めから全部の語をそろえない</text>
</svg>
```

Ontology の対応は、ずれが見えたところから足していきます。始める前に、全部の語の意味をそろえておくことは求めていません。

出典: EAA Core 版 6「0. 目的と範囲」。※「始める前にそろえることは求めていない」は、この行からの読みです。

## Evidence の様式も共有する文書

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="70" width="220" height="180" rx="10" class="box"/><text x="150" y="166" class="t" text-anchor="middle" font-weight="700">在庫の Cell</text>
  <rect x="620" y="70" width="220" height="180" rx="10" class="box"/><text x="730" y="166" class="t" text-anchor="middle" font-weight="700">物流の Cell</text>
  <rect x="310" y="60" width="260" height="200" rx="3" class="hl" style="fill:#fff"/>
  <text x="440" y="96" class="t hc" text-anchor="middle" font-weight="700">Evidence の様式</text>
  <g class="ts" text-anchor="middle"><text x="440" y="136">何を残すか</text><text x="440" y="164">どの形で残すか</text></g>
  <path d="M330,196 H550" class="lt"/>
  <g class="tx" text-anchor="middle"><text x="440" y="220">所有者（人間）・観測・準拠先</text></g>
  <path d="M260,160 H306 M574,160 H616" class="ln"/>
  <text x="440" y="320" class="ts sub" text-anchor="middle">Contract・共有する Profile・共有する Ontology と同じ扱い</text>
</svg>
```

何を Evidence とし、どの形で残すかは、Evidence の様式として Cell のあいだで共有する文書に書きます。所有者は人間で、観測と準拠先も持ちます。

出典: EAA Core 版 6 の概念表「Evidence の様式」と「4. 提案と変更」。

## Core はここまでしか決めていない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="30" width="380" height="290" rx="10" class="soft"/>
  <text x="60" y="64" class="t" font-weight="700">Core が決めていること</text>
  <g class="ts"><use href="#i-ok" x="60" y="88" width="22" height="22"/><text x="92" y="105">境界を越えるのは Evidence</text>
  <use href="#i-ok" x="60" y="128" width="22" height="22"/><text x="92" y="145">作った側を介さずに確かめられる形</text>
  <use href="#i-ok" x="60" y="168" width="22" height="22"/><text x="92" y="185">ずれは照会か変更提案で解く</text>
  <use href="#i-ok" x="60" y="208" width="22" height="22"/><text x="92" y="225">様式と Ontology も所有者を持つ</text></g>
  <rect x="460" y="30" width="380" height="290" rx="10" fill="url(#hatch)"/>
  <text x="480" y="64" class="t" font-weight="700">決めていないこと</text>
  <g class="ts"><text x="480" y="105">Evidence の様式に書く項目</text><text x="480" y="145">共有する Ontology の所有者の決め方</text><text x="480" y="185">Evidence の様式の所有者の決め方</text></g>
  <text x="440" y="356" class="ts sub" text-anchor="middle">所有者の決め方を書いているのは、Contract だけ</text>
</svg>
```

Evidence の様式に何の項目を書くかを、Core は決めていません。共有する Ontology と様式の所有者をどう決めるかも、まだ書いていません。

出典: EAA Core 版 6「4. 提案と変更」。所有者の決め方は、Contract についてだけ書いている（第 8 章）。
