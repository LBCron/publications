# 第 7 章　仕事は Mission で渡し、作業や受け入れだけでは完了にしない

群: Evidence・Mission・Contract と版

<!--
構造: agent-hub-roles-kaz/philosopher/2026-11-07-eaa-textbook-structure.md（55553ae4）。章題と群の札の字は writer-ja/drafts/eaa-toc/titles.md（d21b0d80、@ope-ultp1635 msg 65a67e15）で書き直した。構造は変えない。
出どころ（構造の表のまま）: core.md:32-35・65-67・106-110。Core は publications origin/main 0d07f75 の core.md 版 6。
本文: @ope-ultp1635 msg f202fb67（群三）。
足した出どころ: Mission と Contract の使い分けは素材 3（3-hand-over-versions.html「Contract という語について」）。Mission の例は delivery-guide.md:131-179（Mission Metadata Pattern。説明用の記法で確定スキーマではない、と 178 行）。依存する版は core.md:78。「PR の merge は完了ではない」は delivery-guide.md:214。GitHub での残し方は delivery-guide.md:104-127。
用語を開いた所: Constraints・Authority は Core の概念表に定義が無い（core.md:65 で欄の名前として出るだけ）。本文では英語の欄名を残し、「守る条件」「任せる権限」の説明を添えた。説明は素材 3 の「守る条件・任せる範囲」による。注に書いた。Mission の例の acceptance の値（contract-change-e2e・rollback-tested）は日本語に開いた。
Mission の例の ontology の参照先は、原文では enterprise:// で始まる。Ontology を持つ者が全体の側（Enterprise）になる形に読め、core.md:21「境界の両側が保持する」と食い違うので、（Ontology が一つであることは理由にしていない。二つの Cell が共有する一つの Ontology は全体の側の持ち物ではなく、第 6 章はその形を取る）参照先の名前は出さず「契約・請求プラン・顧客の Ontology」とだけ書いた。注に書いた。
「子Mission」「親Goal」（core.md:67）は Mission の分け方の呼び名で、Cell の親子ではない。絵では Mission を Cell の枠の中に描いていない。
完了を誰が判定するかは core.md:106-107 に名指しが無い。最後のページに書いた。
新しく引く外部の文献は無い。
⑤（@ope-ultp1635 msg 281e5366、@reviewer 3 回目・4 回目）: 最後のページの項目は core.md:11 の既知の不足に無いので「Core に書かれていない」に置き、「まだ」を落とした。
⑥（@ope-ultp1635 msg 6fc17eeb、@reviewer 2〜4 回目）: 章題と章の概要（絵の結び・文）が完了の条件を Outcome と Acceptance Evidence だけにしていた。core.md:106 は Contract 更新・判断記録・権限違反の解消も要る（「完了に要るもの」のページは全部書いていた）。章題は core.md:107 の「作業実施や変更の受入だけでは完了しない」の字にし（titles.md に記録）、概要の文に残りの条件を足した。core.md:107 の「必要な職務分離」の「必要な」を戻した。p.「目的を変えるなら」は core.md:67 の「新Missionまたは改訂として提案する」の「提案する」を落としていたので戻し、見出しも変えた。p.「決めたことは、記録に戻す」の絵の「会話だけに残った決定は正式な決定として扱わない」は delivery-guide.md:127 の字で（そこからも「重要な」が落ちていた）、Core より強い内容なのに最後のページで「Core が決めていること」に入っていた。絵と最後のページを core.md:110 の字にし、Delivery Guide の字は適用例として注に置いた。
2 周目（@ope-ultp1635 msg 8fbac4e5、@reader r2 cea29c1f）: 最後のページの右の小見出しを「既知の不足にも挙がっていない」にした（理由は第 6 章の注と同じ）。
-->

> Mission には Goal・Constraints・Authority・Acceptance Evidence を書く。Task の分け方は受けた Cell が決め、作業したことや受け入れたことだけでは完了にならない。

```svg
<svg viewBox="0 0 880 300" width="880" height="300">
  <rect x="30" y="30" width="250" height="200" rx="10" class="box"/><text x="155" y="66" class="t" text-anchor="middle" font-weight="700">頼む Cell</text>
  <rect x="320" y="24" width="240" height="212" rx="3" class="hl" style="fill:#fff"/><text x="440" y="54" class="t hc" text-anchor="middle" font-weight="700">Mission</text>
  <g class="ts"><text x="340" y="88">Goal</text><text x="340" y="120">Constraints</text><text x="340" y="152">Authority</text><text x="340" y="184">Acceptance Evidence</text></g>
  <path d="M280,130 H316" class="ln" marker-end="url(#arr)"/><path d="M564,130 H596" class="ln" marker-end="url(#arr)"/>
  <rect x="600" y="30" width="250" height="200" rx="10" class="box"/><text x="725" y="66" class="t" text-anchor="middle" font-weight="700">受けた Cell</text>
  <rect x="630" y="90" width="190" height="40" rx="6" class="soft"/><text x="725" y="116" class="ts" text-anchor="middle">Task は自分で分ける</text>
  <rect x="630" y="150" width="190" height="56" rx="6" class="soft"/><text x="725" y="174" class="ts" text-anchor="middle">完了に要るものを</text><text x="725" y="196" class="ts" text-anchor="middle">全部揃える</text>
  <text x="440" y="274" class="t" text-anchor="middle" font-weight="700">渡すのは条件。完了は、作業でなく、要るものが揃ったかで決める</text>
</svg>
```

一回の仕事は、目指す状態と条件を書いた Mission で渡します。完了には、成り立った変化と決めた Evidence に加え、要る記録と権限違反の解消が要ります。

## Mission は、今回の変化

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="40" width="800" height="80" rx="10" class="soft"/><text x="70" y="76" class="t" font-weight="700">Profile</text><text x="70" y="102" class="ts sub">Cell が引き受けている責務（続く）</text>
  <path d="M440,120 V150" class="ln" marker-end="url(#arr)"/>
  <rect x="200" y="156" width="480" height="70" rx="3" class="hl" style="fill:#fff"/><text x="230" y="190" class="t hc" font-weight="700">Mission</text><text x="230" y="214" class="ts">責務のもとで、今回実現する変化・成果</text>
  <g class="ts" text-anchor="middle">
    <rect x="120" y="260" width="300" height="80" rx="6" class="box"/><text x="270" y="292" font-weight="700">Goal</text><text x="270" y="318">Mission が目指す状態</text>
    <rect x="460" y="260" width="300" height="80" rx="6" class="box"/><text x="610" y="292" font-weight="700">Outcome</text><text x="610" y="318">実際に成り立たせた変化・成果</text>
  </g>
</svg>
```

Mission は、引き受けた責務のもとで今回実現する変化です。目指す状態を Goal、実際に成り立たせた変化を Outcome と呼びます。

出典: EAA Core 版 6 の概念表「Mission」「Goal」「Outcome」。

## 一回の仕事と、続く取り決め

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <path d="M440,20 V320" class="lt dash"/>
  <text x="220" y="54" class="t" text-anchor="middle" font-weight="700">Mission</text><text x="220" y="80" class="ts sub" text-anchor="middle">一回の仕事</text>
  <text x="660" y="54" class="t" text-anchor="middle" font-weight="700">Contract</text><text x="660" y="80" class="ts sub" text-anchor="middle">続いていく取り決め</text>
  <rect x="80" y="110" width="280" height="150" rx="3" class="hl" style="fill:#fff"/><g class="ts" text-anchor="middle"><text x="220" y="150">出荷指示に</text><text x="220" y="176">希望時間帯の欄を足す</text><text x="220" y="220" class="sub">終わったら完了</text></g>
  <rect x="520" y="110" width="280" height="150" rx="3" class="hl" style="fill:#fff"/><g class="ts" text-anchor="middle"><text x="660" y="150">在庫と物流のあいだの</text><text x="660" y="176">責任・条件・入出力・Evidence</text><text x="660" y="220" class="sub">変えるまで効き続ける</text></g>
  <text x="440" y="350" class="ts sub" text-anchor="middle">Contract は第 8 章で見る</text>
</svg>
```

一回の仕事は Mission で渡し、続く取り決めは Contract に書きます。在庫と物流なら、欄を足す仕事が Mission、取り決めが Contract です。

出典: EAA 紹介 3「Contract という語について」、EAA Core 版 6 の概念表。※ 欄を足す仕事は説明のための例です。

## Mission に書く欄

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="30" width="800" height="250" rx="3" class="hl" style="fill:#fff"/>
  <g class="ts">
    <text x="70" y="70" font-weight="700">Goal</text><text x="330" y="70">目指す状態</text>
    <text x="70" y="120" font-weight="700">Constraints</text><text x="330" y="120">守る条件</text>
    <text x="70" y="170" font-weight="700">Authority</text><text x="330" y="170">任せる権限（触ってよい範囲と、触らない範囲）</text>
    <text x="70" y="220" font-weight="700">Acceptance Evidence</text><text x="330" y="220">受け入れの判断に使う Evidence</text>
    <text x="70" y="262" class="sub">そのほか</text><text x="330" y="262" class="sub">背景と、引き受ける条件を共有する</text>
  </g>
  <path d="M60,90 H820 M60,140 H820 M60,190 H820 M60,240 H820" class="lt"/>
  <text x="440" y="330" class="ts sub" text-anchor="middle">左は Core の欄の名前。右の説明は EAA 紹介 3 による</text>
</svg>
```

Mission には、Goal、Constraints、Authority、Acceptance Evidence を書き、背景と引き受ける条件も共有します。

出典: EAA Core 版 6「2. 自治と権限」。※ 欄の説明（守る条件・任せる権限）は EAA 紹介 3 によります。Core は欄の名前だけを挙げます。

## 例：契約プランの変更を渡す

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="20" width="800" height="300" rx="3" class="hl" style="fill:#fff"/>
  <text x="60" y="52" class="t hc" font-weight="700">Mission</text>
  <g class="ts">
    <text x="60" y="92" font-weight="700">Goal</text><text x="300" y="92">契約プランの変更を、すぐに反映できる</text>
    <text x="60" y="136" font-weight="700">Constraints</text><text x="300" y="136">過去の契約を書き換えない</text><text x="300" y="160">確定済みの請求を変えない</text>
    <text x="60" y="204" font-weight="700">Authority</text><text x="300" y="204">書いてよい：契約　　書かない：請求</text>
    <text x="60" y="248" font-weight="700">Acceptance Evidence</text><text x="300" y="248">契約変更の通しのテストの結果</text><text x="300" y="272">切り戻しを試した結果</text>
  </g>
  <path d="M60,112 H820 M60,180 H820 M60,224 H820" class="lt"/>
  <text x="440" y="356" class="ts sub" text-anchor="middle">説明のための記法で、決まった書式ではない</text>
</svg>
```

契約プランの変更をすぐ反映させる Mission の例です。請求に触らないことを、Constraints と Authority の両方に書いています。

出典: EAA Delivery Guide「7.」の Mission の例（適用例）。値は日本語に開いた（contract-change-e2e → 契約変更の通しのテスト）。

## 依存する版も、Mission に書く

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="40" width="360" height="260" rx="3" class="hl" style="fill:#fff"/><text x="220" y="76" class="t hc" text-anchor="middle" font-weight="700">Mission</text>
  <g class="ts"><text x="70" y="120">Goal・Constraints・</text><text x="70" y="146">Authority・Acceptance Evidence</text></g>
  <path d="M70,176 H370" class="lt"/>
  <g class="ts"><text x="70" y="210">依存する Ontology の版</text><text x="70" y="240">依存する Constitution の版</text><text x="70" y="270">依存する Contract の版</text></g>
  <path d="M400,240 H476" class="ln" marker-end="url(#arr)"/>
  <rect x="480" y="160" width="360" height="140" rx="10" class="soft"/>
  <text x="660" y="200" class="ts" text-anchor="middle" font-weight="700">どの版で頼んだかが決まる</text>
  <text x="660" y="232" class="ts" text-anchor="middle">新しい版が出ても、</text><text x="660" y="258" class="ts" text-anchor="middle">自動では移らない（第 9 章）</text>
</svg>
```

Mission には、依存する Ontology・Constitution・Contract の版を書きます。どの版を前提に頼んだかが、受けた側にも後から分かります。

出典: EAA Core 版 6「3. 意味と合意」。※ 例の原文は Ontology の参照先の名前も書くが、ここでは出していない。

## Task は、受けた Cell が分ける

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="260" height="220" rx="10" class="box"/><text x="170" y="96" class="t" text-anchor="middle" font-weight="700">頼む Cell</text>
  <rect x="80" y="150" width="180" height="50" rx="3" class="hl" style="fill:#fff"/><text x="170" y="182" class="ts hc" text-anchor="middle">Mission</text>
  <path d="M300,175 H536" class="ln" marker-end="url(#arr)"/>
  <rect x="540" y="60" width="300" height="220" rx="10" class="box"/><text x="690" y="96" class="t" text-anchor="middle" font-weight="700">受けた Cell</text>
  <g class="ts" text-anchor="middle"><rect x="570" y="124" width="110" height="36" rx="18" class="a"/><text x="625" y="148" class="on">Task</text><rect x="700" y="124" width="110" height="36" rx="18" class="a"/><text x="755" y="148" class="on">Task</text><rect x="570" y="176" width="110" height="36" rx="18" class="a"/><text x="625" y="200" class="on">Task</text><rect x="700" y="176" width="110" height="36" rx="18" class="a"/><text x="755" y="200" class="on">Task</text></g>
  <text x="690" y="250" class="ts" text-anchor="middle">分け方は、この Cell が決める</text>
  <path d="M300,240 C 380,300 480,300 560,240" class="xl dash" marker-end="url(#arr-x)"/><use href="#i-no" x="418" y="278" width="24" height="24"/><text x="430" y="330" class="ts xc" text-anchor="middle">頼む側が Task まで指定する</text>
</svg>
```

Mission を受けた Cell は、それを実現するための作業の単位を Task として自分で分けます。頼む側は、Task の分け方を指定しません。

出典: EAA Core 版 6 の概念表「Task」と「2. 自治と権限」。

## 任せる権限は、自分の持つ範囲まで

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="300" height="220" rx="10" class="box"/><text x="190" y="96" class="t" text-anchor="middle" font-weight="700">頼む Cell</text>
  <rect x="70" y="120" width="240" height="130" rx="6" class="soft"/><text x="190" y="146" class="ts" text-anchor="middle">正当に与えられる権限</text>
  <rect x="110" y="166" width="160" height="60" rx="3" class="hl" style="fill:#fff"/><text x="190" y="202" class="ts hc" text-anchor="middle">Authority に書く</text>
  <path d="M340,196 H536" class="ln" marker-end="url(#arr)"/><use href="#i-ok" x="426" y="160" width="26" height="26"/>
  <rect x="540" y="60" width="300" height="220" rx="10" class="box"/><text x="690" y="96" class="t" text-anchor="middle" font-weight="700">受けた Cell</text>
  <text x="690" y="200" class="ts" text-anchor="middle">書かれた範囲で判断する</text>
  <rect x="40" y="306" width="800" height="50" rx="6" class="xl" style="fill:#fff"/><use href="#i-no" x="60" y="319" width="24" height="24"/><text x="100" y="338" class="ts xc">自分が持っていない権限（たとえば請求への書き込み）は、Authority に書けない</text>
</svg>
```

権限を任せるときは、任せる側が正当に与えられる範囲を越えません。自分が持っていない権限を、Mission に書いて渡すことはできません。

出典: EAA Core 版 6「2. 自治と権限」。※ 請求の例は説明のためのものです。

## 目的を変えるなら、提案する

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="40" width="300" height="100" rx="3" class="hl" style="fill:#fff"/><text x="190" y="80" class="ts hc" text-anchor="middle" font-weight="700">Mission の Goal</text><text x="190" y="110" class="ts" text-anchor="middle">契約プランの変更を、すぐに反映</text>
  <rect x="540" y="40" width="300" height="100" rx="3" class="lt" style="fill:#fff"/><text x="690" y="80" class="ts" text-anchor="middle" font-weight="700">分けた Mission</text><text x="690" y="110" class="ts" text-anchor="middle">Goal への寄与を説明できる</text>
  <path d="M340,90 H536" class="ln" marker-end="url(#arr)"/>
  <rect x="40" y="190" width="800" height="150" rx="10" class="soft"/>
  <text x="70" y="226" class="ts" font-weight="700">途中で目的そのものを変えたくなったら</text>
  <use href="#i-no" x="70" y="246" width="22" height="22"/><text x="102" y="263" class="ts">いまの Mission の中で、黙って目的を変える</text>
  <use href="#i-ok" x="70" y="286" width="22" height="22"/><text x="102" y="303" class="ts">新しい Mission として、または改訂として提案する</text>
</svg>
```

分けた先の Mission は、元の Goal にどう寄与するかを説明できるようにします。目的を変えるなら、新しい Mission として、または改訂として提案します。

出典: EAA Core 版 6「2. 自治と権限」。Core は分けた先を子 Mission、元を親 Goal と呼ぶ。Cell の親子とは別の呼び名。

## 完了に要るもの

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <g class="ts">
    <rect x="40" y="40" width="390" height="110" rx="6" class="h"/><text x="235" y="86" class="on" text-anchor="middle" font-weight="700">Outcome の達成</text><text x="235" y="114" class="on" text-anchor="middle">変化が実際に成り立った</text>
    <rect x="450" y="40" width="390" height="110" rx="6" class="h"/><text x="645" y="86" class="on" text-anchor="middle" font-weight="700">Acceptance Evidence の充足</text><text x="645" y="114" class="on" text-anchor="middle">決めた Evidence が揃った</text>
    <rect x="40" y="170" width="390" height="110" rx="6" class="box"/><text x="235" y="216" text-anchor="middle" font-weight="700">Contract の更新と判断の記録</text><text x="235" y="244" text-anchor="middle">必要なものが済んだ</text>
    <rect x="450" y="170" width="390" height="110" rx="6" class="box"/><text x="645" y="216" text-anchor="middle" font-weight="700">権限違反の解消</text><text x="645" y="244" text-anchor="middle">違反が残っていない</text>
  </g>
  <text x="440" y="330" class="t" text-anchor="middle" font-weight="700">全部が揃って、Mission は完了する</text>
</svg>
```

完了には、Outcome の達成、Acceptance Evidence の充足、必要な Contract の更新と判断の記録、権限違反の解消のすべてが要ります。

出典: EAA Core 版 6「5. 成果と記録」。

## 作業や受け入れだけでは完了しない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <g class="ts" text-anchor="middle">
    <rect x="40" y="60" width="240" height="70" rx="6" class="soft"/><text x="160" y="102">作業をやり終えた</text>
    <rect x="320" y="60" width="240" height="70" rx="6" class="soft"/><text x="440" y="102">変更を受け入れた</text>
    <rect x="600" y="60" width="240" height="70" rx="6" class="soft"/><text x="720" y="102">PR を merge した</text>
  </g>
  <use href="#i-no" x="146" y="146" width="28" height="28"/><use href="#i-no" x="426" y="146" width="28" height="28"/><use href="#i-no" x="706" y="146" width="28" height="28"/>
  <text x="440" y="214" class="t" text-anchor="middle" font-weight="700">どれも、それだけでは完了ではない</text>
  <rect x="140" y="246" width="600" height="80" rx="10" class="box"/>
  <text x="440" y="280" class="ts" text-anchor="middle">合意した確かめの条件と、必要な職務分離（行う者と確かめる者を分ける）を</text>
  <text x="440" y="306" class="ts" text-anchor="middle">完了の判定まで保つ</text>
</svg>
```

作業をやり終えたことや変更を受け入れたことだけでは、完了しません。PR の merge も同じです。合意した確かめの条件と、必要な職務分離を保ちます。

出典: EAA Core 版 6「5. 成果と記録」、EAA Delivery Guide「8.」（PR merge は Mission の完了と同義ではない）。

## 決めたことは、記録に戻す

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="30" width="420" height="300" rx="10" class="soft"/>
  <text x="60" y="64" class="ts" font-weight="700">GitHub で残す例</text>
  <g class="ts"><text x="60" y="104">Issue</text><text x="200" y="104">Mission</text>
  <text x="60" y="140">Sub-issue</text><text x="200" y="140">分けた Mission</text>
  <text x="60" y="176">PR</text><text x="200" y="176">変更の提案と成果物</text>
  <text x="60" y="212">Actions</text><text x="200" y="212">確かめた Evidence</text>
  <text x="60" y="248">Comment</text><text x="200" y="248">判断と Evidence</text>
  <text x="60" y="284">Close</text><text x="200" y="284">Evidence による完了の記録</text></g>
  <rect x="500" y="80" width="340" height="80" rx="6" class="box"/><text x="670" y="116" class="ts" text-anchor="middle">チャット・会議</text><text x="670" y="142" class="tx" text-anchor="middle">その場の連絡</text>
  <path d="M670,160 V210 H464" class="ln" marker-end="url(#arr)"/><text x="680" y="196" class="ts" font-weight="700">決まったら戻す</text>
  <text x="670" y="290" class="ts xc" text-anchor="middle">重要な決定を、</text><text x="670" y="314" class="ts xc" text-anchor="middle">その場の会話だけに残さない</text>
</svg>
```

Mission、実行、Evidence、受け入れ、改訂、引き継ぎを、後から追える形で残します。重要な決定を、その場の会話だけに残しません。

出典: EAA Core 版 6「5.」、EAA Delivery Guide「6.」（適用例）。※ 同ガイドは、記録に戻らない重要な決定を正式な決定と扱わない、とまで書く。Core より強い。

## Core はここまでしか決めていない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="30" width="380" height="290" rx="10" class="soft"/>
  <text x="60" y="64" class="t" font-weight="700">Core が決めていること</text>
  <g class="ts"><use href="#i-ok" x="60" y="88" width="22" height="22"/><text x="92" y="105">Mission に書く欄の名前</text>
  <use href="#i-ok" x="60" y="128" width="22" height="22"/><text x="92" y="145">Task は受けた Cell が分ける</text>
  <use href="#i-ok" x="60" y="168" width="22" height="22"/><text x="92" y="185">完了に要るもの</text>
  <use href="#i-ok" x="60" y="208" width="22" height="22"/><text x="92" y="225">重要な決定を会話だけに残さない</text></g>
  <rect x="460" y="30" width="380" height="290" rx="10" fill="url(#hatch)"/>
  <text x="480" y="64" class="t" font-weight="700">決めていないこと</text>
  <g class="ts"><text x="480" y="102" class="ts" font-weight="700">Core に書かれていない</text><text x="480" y="126" class="tx">既知の不足にも挙がっていない</text><text x="480" y="166" class="ts">Mission の書式（項目名・記法）</text><text x="480" y="206" class="ts">欄ごとに何をどこまで書くか</text><text x="480" y="246" class="ts">完了を判定する者の名指し</text></g>
  <text x="440" y="356" class="ts sub" text-anchor="middle">例の記法は、自分の案件で書き始めるための例</text>
</svg>
```

Mission の書式は Core に書かれていません。完了を判定する者も Core は名指しせず、合意した確かめの条件と必要な職務分離を保つことを求めています。

出典: EAA Core 版 6「5. 成果と記録」、EAA Delivery Guide「7.」（説明用の記法で、確定した書式ではない）。
