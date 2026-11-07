# 第 12 章　導入は、作り方を残したまま、つながり方だけを Core に合わせる

群: 規範の承認・採用と導入

<!--
構造: agent-hub-roles-kaz/philosopher/2026-11-07-eaa-textbook-structure.md（55553ae4）。章題と群の札の字は writer-ja/drafts/eaa-toc/titles.md（d21b0d80、@ope-ultp1635 msg 65a67e15）で書き直した。構造は変えない。
出どころ（構造の表のまま）: adoption-guide.md 6・7 節、delivery-guide.md 3・4 節、role-model.md 2 節。Core は publications origin/main 0d07f75 の core.md 版 6。
本文: @ope-ultp1635 msg dfcb091f（群四）。
「Operator の判断は規範に書き直していく」は骨格で題から落とし書き手メモに残したもの（@ope-ultp1635 msg d407be50）。群四の便で必ず入れると指示があった。章の概要の文と、8 ページ目「判断を規範に書き直していく」の文に字のまま入れた。
足した出どころ: delivery-guide.md 2 節（判断の削減と成果・安全性を一緒に観測する）、profiles.md 6 節（Supplier の責務。第 8 章の注と同じ）、各適用例の冒頭の「位置づけ：適用例（非規範）」（最後のページ）。
例は第 6〜11 章の在庫と物流を続けた。在庫は自社の Scrum、物流は委託先の標準工程（第 6 章の例のまま）。あいだを定例会議で合わせていた、は第 1 章「複数社で組んでも同じ二つ」の発注側の定例会議につないだ説明のための仮定。
包含と同じ形の字: adoption-guide.md:296「Domain が自律できる境界を作る」は「Cell が自律できる境界」と書いた。delivery-guide.md:20・35「各 Domain は」は「各 Cell は」と書いた（Domain／Enterprise の組は development-model.md:24 と同じ字の組で、第 9 章の書き手メモと同じ扱い）。role-model.md 5 節「Enterpriseの責務」（全体の目的・制約・資源配分）は出どころの 2 節の外で、使っていない。
adoption-guide.md:270-277 の英語の段は日本語に開いた（Recorded Decision → 記録した判断、Machine-readable Control → 機械で読める制御、Future Autonomy → 次からは任せられる）。Operator Dependency(t) は「Operator への依存」と書いた。
第 2・3 章と重なる所（つながり方の最低限、Profile の数で Cell を決めない）は、ページを立てずに前の章を指した。
絵: Cell はどれもほかの Cell の枠の外に並べる（core.md:43）。
新しく引く外部の文献は無い。
-->

> 既存の Scrum・SAFe・委託先の工程は残し、Evidence を観測して責務を Profile に書き、独立した判断が要る所だけ Cell を分ける。

```svg
<svg viewBox="0 0 880 300" width="880" height="300">
  <text x="200" y="28" class="ts sub" text-anchor="middle">前</text><text x="660" y="28" class="ts sub" text-anchor="middle">導入の後</text>
  <rect x="30" y="44" width="130" height="110" rx="10" class="box"/><text x="95" y="90" class="ts" text-anchor="middle" font-weight="700">在庫</text><text x="95" y="116" class="tx" text-anchor="middle">Scrum</text>
  <rect x="240" y="44" width="130" height="110" rx="10" class="box"/><text x="305" y="90" class="ts" text-anchor="middle" font-weight="700">物流</text><text x="305" y="116" class="tx" text-anchor="middle">委託先の工程</text>
  <path d="M160,99 H240" class="ln dash"/><text x="200" y="186" class="ts" text-anchor="middle">定例会議で合わせる</text>
  <path d="M420,100 H460" class="ln" marker-end="url(#arr)"/>
  <rect x="490" y="44" width="130" height="110" rx="10" class="box"/><text x="555" y="90" class="ts" text-anchor="middle" font-weight="700">在庫</text><text x="555" y="116" class="tx" text-anchor="middle">Scrum</text>
  <rect x="720" y="44" width="130" height="110" rx="10" class="box"/><text x="785" y="90" class="ts" text-anchor="middle" font-weight="700">物流</text><text x="785" y="116" class="tx" text-anchor="middle">委託先の工程</text>
  <rect x="630" y="74" width="80" height="50" rx="3" class="hl" style="fill:#fff"/><text x="670" y="104" class="tx hc" text-anchor="middle">Contract</text>
  <path d="M620,99 H630 M710,99 H720" class="ln"/><text x="670" y="186" class="ts" text-anchor="middle">版付きの文書と Evidence</text>
  <text x="440" y="262" class="t" text-anchor="middle" font-weight="700">中は今のまま。替わるのは、あいだの線だけ</text>
</svg>
```

導入では、各チームの中の作り方を変えません。変えるのはチームのあいだのつながり方で、Operator の判断は規範に書き直していきます。

## 中の作り方は、そのまま残す

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <g class="ts" text-anchor="middle">
    <rect x="20" y="80" width="150" height="120" rx="10" class="box"/><text x="95" y="134">Scrum</text>
    <rect x="195" y="80" width="150" height="120" rx="10" class="box"/><text x="270" y="134">SAFe の ART</text>
    <rect x="370" y="80" width="150" height="120" rx="10" class="box"/><text x="445" y="134">計画型の工程</text>
    <rect x="545" y="80" width="150" height="120" rx="10" class="box"/><text x="620" y="134">委託先の工程</text>
    <rect x="720" y="80" width="150" height="120" rx="10" class="box"/><text x="795" y="134">パッケージ導入</text>
    <text x="95" y="170" class="tx">Cell の中</text><text x="270" y="170" class="tx">Cell の中</text><text x="445" y="170" class="tx">Cell の中</text><text x="620" y="170" class="tx">Cell の中</text><text x="795" y="170" class="tx">Cell の中</text>
  </g>
  <rect x="40" y="250" width="800" height="70" rx="10" class="soft"/>
  <text x="440" y="292" class="t" text-anchor="middle" font-weight="700">今の仕事をやめさせず、今の専門性を残る形に変える</text>
</svg>
```

Scrum、SAFe の ART、計画型の工程、委託先の工程、パッケージの導入は、どれもその Cell の中の作り方として残せます。

出典: EAA Adoption Guide「7.」（適用例）。Predictive を計画型と書いた。ART は第 2 章で見ました。

## 導入の順序

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <g class="ts">
    <rect x="60" y="20" width="560" height="40" rx="6" class="soft"/><text x="80" y="46">1　Core でつなぐ</text>
    <rect x="60" y="70" width="560" height="40" rx="6" class="soft"/><text x="80" y="96">2　中の作り方を残す</text>
    <rect x="60" y="120" width="560" height="40" rx="6" class="soft"/><text x="80" y="146">3　Evidence を観測する</text>
    <rect x="60" y="170" width="560" height="40" rx="6" class="soft"/><text x="80" y="196">4　責務を Profile に書き、割り当てる</text>
    <rect x="60" y="220" width="560" height="40" rx="6" class="soft"/><text x="80" y="246">5　独立した判断が要る所だけ Cell を分ける</text>
    <rect x="60" y="270" width="560" height="40" rx="6" class="soft"/><text x="80" y="296">6　要らないと確かめた制約だけ外す</text>
  </g>
  <path d="M650,40 V290" class="ln" marker-end="url(#arr)"/>
  <g class="tx"><text x="670" y="146">第 6 章</text><text x="670" y="196">第 3 章</text><text x="670" y="246">第 3・5 章</text></g>
</svg>
```

Core でつなぎ、中の作り方を残し、Evidence を観測し、責務を Profile に書き、独立した判断が要る所だけを分け、要らない制約だけを外します。

出典: EAA Adoption Guide「7.」（適用例。英語の段を日本語に開いた）。右の章で、それぞれの段の決まりを見ました。

## 例：在庫と物流を Core でつなぐ

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="50" width="260" height="210" rx="10" class="box"/><text x="170" y="86" class="t" text-anchor="middle" font-weight="700">在庫の Cell</text><text x="170" y="114" class="tx" text-anchor="middle">中は Scrum（自社のチーム）のまま</text>
  <rect x="580" y="50" width="260" height="210" rx="10" class="box"/><text x="710" y="86" class="t" text-anchor="middle" font-weight="700">物流の Cell</text><text x="710" y="114" class="tx" text-anchor="middle">中は委託先の標準工程のまま</text>
  <rect x="330" y="100" width="220" height="70" rx="3" class="hl" style="fill:#fff"/><text x="440" y="132" class="ts hc" text-anchor="middle" font-weight="700">Contract　版 1</text><text x="440" y="156" class="tx" text-anchor="middle">所有者は物流の窓口の責任者</text>
  <path d="M300,135 H326 M554,135 H576" class="ln"/>
  <path d="M576,214 H304" class="ln" marker-end="url(#arr)"/><text x="440" y="204" class="ts" text-anchor="middle">出荷結果と、突き合わせの記録</text>
  <rect x="120" y="296" width="640" height="54" rx="6" class="soft"/><text x="440" y="329" class="ts" text-anchor="middle">定例会議で合わせていた中身を、Contract に書く</text>
</svg>
```

在庫は自社の Scrum、物流は委託先の標準工程のままです。変えるのは、あいだの取り決めを Contract に書き、Evidence で確かめることだけです。

※ 第 6〜11 章の在庫と物流の例の続きで、説明のための仮定です。定例会議は第 1 章の「複数社で組んでも同じ二つ」の左側です。

## まず、流れている記録を見る

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <g class="ts">
    <text x="60" y="60" font-weight="700">あいだを今流れている記録</text><text x="560" y="60" font-weight="700">受け取った側だけで確かめられるか</text>
    <text x="60" y="120">出荷指示</text><use href="#i-ok" x="640" y="102" width="24" height="24"/>
    <text x="60" y="180">出荷結果</text><use href="#i-ok" x="640" y="162" width="24" height="24"/>
    <text x="60" y="240">欠品の理由</text><use href="#i-no" x="640" y="222" width="24" height="24"/><text x="680" y="240" class="tx">電話で聞いている</text>
  </g>
  <path d="M40,80 H840 M40,140 H840 M40,200 H840 M40,260 H840" class="lt"/>
  <text x="440" y="320" class="ts sub" text-anchor="middle">確かめられないものが、Contract に書く Evidence の候補になる</text>
</svg>
```

最初に、あいだを今どんな記録が流れているかを観測します。見るのは、受け取った側が作った側に聞かずに確かめられるかです。

出典: EAA Adoption Guide「7.」。※ 見る観点は第 6 章の Evidence の条件です。表の中身は説明のための仮定です。

## 案件に要る Profile を並べる

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <g class="ts">
    <text x="60" y="60" font-weight="700">種類</text><text x="260" y="60" font-weight="700">Profile</text><text x="480" y="60" font-weight="700">書くこと</text>
    <text x="60" y="120">Domain Profile</text><text x="260" y="120">在庫・物流</text><text x="480" y="120">責任の範囲・権限・保証</text>
    <text x="60" y="190">Standard Profile</text><text x="260" y="190">Supplier</text><text x="480" y="190">契約主体をまたぐ責任と受入</text>
    <text x="260" y="250">Platform など</text><text x="480" y="250">要るものだけ</text>
  </g>
  <path d="M40,80 H840 M40,150 H840 M40,280 H840" class="lt"/>
  <text x="440" y="330" class="ts sub" text-anchor="middle">並べた Profile ごとに Cell を作るのではない（第 3 章）</text>
</svg>
```

案件に要る Domain Profile と Standard Profile を並べ、責任の範囲・権限・保証を書きます。委託先が担うなら、Supplier も要ります。

出典: EAA Delivery Guide「4. Profile Selection」（適用例）、EAA Profiles「6.」。※ 在庫・物流の行は説明のための仮定です。

## 外すのは、要らないと確かめた制約だけ

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <g class="ts">
    <text x="60" y="60" font-weight="700">今の手順にある制約</text><text x="500" y="60" font-weight="700">観測した結果</text>
    <text x="60" y="120">週 1 回の定例で出荷指示の変更を承認</text><text x="500" y="120">Contract と Evidence で足りた</text><use href="#i-ok" x="790" y="102" width="24" height="24"/>
    <text x="60" y="180">委託先の工程の中の出荷前の検品</text><text x="500" y="180">要らないと確かめていない</text><text x="790" y="180" class="tx">残す</text>
  </g>
  <path d="M40,80 H840 M40,140 H840 M40,200 H840" class="lt"/>
  <rect x="40" y="240" width="800" height="70" rx="10" class="soft"/>
  <text x="440" y="282" class="t" text-anchor="middle" font-weight="700">一度に置き換えず、少しずつ置き換える</text>
</svg>
```

今の手順にある制約は、要らないと確かめられたものだけを外します。置き換えは一度にせず、少しずつ進めます。

出典: EAA Adoption Guide「7.」（gradual substitution を「少しずつ置き換える」と書いた）。※ 表の中身は説明のための仮定です。

## Operator は、逐一承認しない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="360" height="230" rx="10" fill="url(#hatch)"/>
  <text x="220" y="100" class="t" text-anchor="middle" font-weight="700">しない</text>
  <text x="220" y="160" class="ts" text-anchor="middle">ふつうの成果物を</text><text x="220" y="184" class="ts" text-anchor="middle">一つずつ承認する</text>
  <rect x="480" y="60" width="360" height="230" rx="10" class="box"/>
  <text x="660" y="100" class="t" text-anchor="middle" font-weight="700">する</text>
  <g class="ts"><text x="510" y="150">業務の意味と守る条件を、</text><text x="510" y="174">規範・環境・判定の条件に落とす</text><text x="510" y="220">実行と検証を任せる</text></g>
</svg>
```

判断の責任者である Operator は、ふつうの成果物を一つずつ承認する役ではありません。繰り返す判断を規範に変え、実行と検証を任せます。

出典: EAA Role Model「2. Operator」（適用例）。判断の責任者を Operator と呼ぶのは第 3 章の注で見ました。

## 判断を規範に書き直していく

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <g class="ts" text-anchor="middle">
    <rect x="20" y="40" width="130" height="80" rx="6" class="h"/><text x="85" y="76" class="on">Operator の</text><text x="85" y="100" class="on">判断</text>
    <rect x="170" y="40" width="130" height="80" rx="6" class="soft"/><text x="235" y="76">記録した</text><text x="235" y="100">判断</text>
    <rect x="320" y="40" width="250" height="80" rx="6" class="soft"/><text x="445" y="76">提案して、正当な承認と</text><text x="445" y="100">対象の Cell の受入を得る</text>
    <rect x="590" y="40" width="270" height="80" rx="3" class="hl" style="fill:#fff"/><text x="725" y="76" class="hc">規則・Constitution・</text><text x="725" y="100" class="hc">Contract</text>
    <rect x="320" y="200" width="250" height="80" rx="6" class="soft"/><text x="445" y="246">機械で読める制御</text>
    <rect x="610" y="200" width="250" height="80" rx="22" class="a"/><text x="735" y="246" class="on">次からは任せられる</text>
  </g>
  <path d="M150,80 H166 M300,80 H316 M570,80 H586" class="ln"/>
  <path d="M725,124 V160 H445 V196" class="ln" marker-end="url(#arr)"/><path d="M570,240 H606" class="ln" marker-end="url(#arr)"/>
  <text x="440" y="336" class="t" text-anchor="middle" font-weight="700">同じ判断を、毎回 Operator がしなくてよくなる</text>
</svg>
```

Operator の判断は規範に書き直していきます。判断を記録し、提案して承認と受入を得て規則や Contract にし、機械で読める形にします。

出典: EAA Adoption Guide「6.」（適用例。英語の段を日本語に開いた）。

## ほかの Cell にかかる規範は、提案で

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="300" height="220" rx="10" class="box"/><text x="190" y="96" class="t" text-anchor="middle" font-weight="700">在庫の Cell</text>
  <rect x="110" y="126" width="160" height="40" rx="6" class="h"/><text x="190" y="152" class="ts on" text-anchor="middle">Operator</text>
  <text x="190" y="206" class="ts" text-anchor="middle">繰り返す判断を</text><text x="190" y="230" class="ts" text-anchor="middle">Contract に書きたい</text>
  <path d="M340,170 H536" class="ln" marker-end="url(#arr)"/><use href="#i-pr" x="425" y="128" width="30" height="38"/><text x="440" y="196" class="ts" text-anchor="middle">提案</text>
  <rect x="540" y="60" width="300" height="220" rx="10" class="box"/><text x="690" y="96" class="t" text-anchor="middle" font-weight="700">物流の Cell</text>
  <text x="690" y="160" class="ts" text-anchor="middle">所有者が承認し、</text><text x="690" y="184" class="ts" text-anchor="middle">両方が採用して移る</text>
</svg>
```

ほかの Cell にかかる規範にするときは、提案として出し、正当な所有者の承認と、対象の Cell の採用を得ます。

出典: EAA Adoption Guide「6.」（適用例）。承認は第 10 章、採用は第 9 章で見ました。

## 機械化は、権限を緩めることではない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="360" height="220" rx="10" class="box"/>
  <text x="220" y="100" class="t" text-anchor="middle" font-weight="700">繰り返す判断の機械化</text>
  <text x="220" y="160" class="ts" text-anchor="middle">承認と採用を経た規範を、</text><text x="220" y="184" class="ts" text-anchor="middle">機械が読める形にする</text>
  <use href="#i-ok" x="206" y="214" width="28" height="28"/>
  <rect x="480" y="60" width="360" height="220" rx="10" fill="url(#hatch)"/>
  <text x="660" y="100" class="t" text-anchor="middle" font-weight="700">Agent による自己権限の緩和</text>
  <text x="660" y="160" class="ts" text-anchor="middle">自分を縛る規範を、</text><text x="660" y="184" class="ts" text-anchor="middle">自分で承認して緩める</text>
  <use href="#i-no" x="646" y="214" width="28" height="28"/>
</svg>
```

繰り返す判断を機械化することは、Agent が自分の権限を緩めることとは別です。規範にする段で、承認と採用を経ています。

出典: EAA Adoption Guide「6.」（適用例）。自分を縛る規範を緩めないことは第 10 章で見ました。

## 依存が減っていくことを成熟と見る

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <path d="M100,40 V290 H820" class="ln"/>
  <text x="90" y="56" class="tx" text-anchor="end">多い</text><text x="90" y="286" class="tx" text-anchor="end">少ない</text><text x="820" y="316" class="tx" text-anchor="end">時間</text>
  <path d="M110,70 C300,90 420,200 800,250" class="hl"/>
  <text x="600" y="186" class="ts hc">Operator への依存</text>
  <text x="140" y="56" class="ts">初めは強い Operator が要る</text>
  <text x="460" y="346" class="ts sub" text-anchor="middle">Operator がずっと全部を判断し続ける状態は、成功ではない</text>
</svg>
```

初めのうちは強い Operator が要りますが、その人がずっと全部を判断し続ける状態は成功ではありません。依存が減っていくことを成熟の目安にします。

出典: EAA Adoption Guide「6.」（適用例。Operator Dependency(t) ↓ を「Operator への依存が減る」と書いた）。

## Operator は、任せる境界を作る

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <g class="ts">
    <text x="60" y="60" font-weight="700">Operator の仕事</text>
    <text x="60" y="120">統治の曖昧さを、Authority・Constraint・例外に訳す</text>
    <text x="60" y="180">例外を分類する</text>
    <text x="60" y="240">繰り返す判断を規則にする</text>
    <text x="60" y="300">Cell が自律できる境界を作る</text>
  </g>
  <path d="M40,80 H840 M40,140 H840 M40,200 H840 M40,260 H840 M40,320 H840" class="lt"/>
  <text x="640" y="200" class="ts sub" text-anchor="middle">判断の件数の多さではない</text>
</svg>
```

Operator の価値は、判断の件数ではありません。曖昧な所を権限・制約・例外に訳し、Cell が自律できる境界を作ることです。

出典: EAA Adoption Guide「6.」（適用例。原文の Domain を Cell と書いた）。

## 判断を減らしても、成果と安全は保つ

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="360" height="210" rx="10" class="box"/><text x="220" y="100" class="t" text-anchor="middle" font-weight="700">人の判断の件数</text>
  <text x="220" y="180" class="tl" text-anchor="middle">↓</text><text x="220" y="230" class="ts" text-anchor="middle">減らしていく</text>
  <rect x="480" y="60" width="360" height="210" rx="10" class="box"/><text x="660" y="100" class="t" text-anchor="middle" font-weight="700">成果と安全</text>
  <text x="660" y="180" class="tl" text-anchor="middle">＝</text><text x="660" y="230" class="ts" text-anchor="middle">保てているか</text>
  <text x="440" y="320" class="t" text-anchor="middle" font-weight="700">両方を、一緒に観測する</text>
</svg>
```

人の判断を減らすことと、成果と安全を保てているかを、一緒に観測します。人が中心の作り方の Cell に、同じ運営を求めるものではありません。

出典: EAA Delivery Guide「2. 判断と役割の配置」（適用例）。

## Core はここまでしか決めていない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="30" width="380" height="290" rx="10" class="soft"/>
  <text x="60" y="64" class="t" font-weight="700">Core が決めていること</text>
  <g class="ts"><use href="#i-ok" x="60" y="88" width="22" height="22"/><text x="92" y="105">責務と分割、自治と権限</text>
  <use href="#i-ok" x="60" y="128" width="22" height="22"/><text x="92" y="145">境界に流す Evidence と意味</text>
  <use href="#i-ok" x="60" y="168" width="22" height="22"/><text x="92" y="185">版と採用、提案と変更</text>
  <use href="#i-ok" x="60" y="208" width="22" height="22"/><text x="92" y="225">成果と記録、Core の採用</text></g>
  <rect x="460" y="30" width="380" height="290" rx="10" fill="url(#hatch)"/>
  <text x="480" y="64" class="t" font-weight="700">自分の案件で決めること</text>
  <g class="ts"><text x="480" y="105">導入の順序と進める速さ</text><text x="480" y="145">Operator の置き方</text><text x="480" y="185">成熟の測り方</text><text x="480" y="225">各 Cell の中の作り方</text></g>
  <text x="440" y="356" class="ts sub" text-anchor="middle">この章の手順は、どれも適用例で、Core の規範ではない</text>
</svg>
```

この章の導入の順序、Operator の置き方、成熟の測り方は、どれも適用例で、Core の規範ではありません。自分の案件の条件で決めます。

出典: EAA Adoption Guide・Role Model・Delivery Guide の冒頭「位置づけ：適用例（非規範）」。
