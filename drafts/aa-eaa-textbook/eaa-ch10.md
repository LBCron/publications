# 第 10 章　共有文書の改訂は人間の所有者が承認し、提起した者は承認しない

群: 規範の承認・採用と導入

<!--
構造: agent-hub-roles-kaz/philosopher/2026-11-07-eaa-textbook-structure.md（55553ae4）。章題と群の札の字は writer-ja/drafts/eaa-toc/titles.md（d21b0d80、@ope-ultp1635 msg 65a67e15）で書き直した。構造は変えない。
出どころ（構造の表のまま）: core.md:45・94-97、profiles.md 4 節。Core は publications origin/main 0d07f75 の core.md 版 6。
本文: @ope-ultp1635 msg dfcb091f（群四）。
足した出どころ: core.md:7-12（Core 自身の所有者・観測・準拠先の表。語の意味をここから取った）、core.md:70（権限が足りないときは調整へ戻す）、core.md:93（承認の手続きは各判断に適用される手続きに任せる）、core.md:98（Contract の所有者は 1 人）、core.md:107・109（職務分離の維持と、改訂を追える記録）。編集権の行は profiles.md:73。
例は第 6〜9 章の在庫と物流を続けた。締めの時刻の改訂は第 9 章の「逆向きの変更」のページの続き。所有者本人が提起したときの承認者は、第 8 章の最後のページにも挙げた。ここでは例で見せ、最後のページに Core の字からの帰結として書いた。
publications の #135・#136・#137 と APPROVALS 行 12〜15 を実例として使うかは書き手の判断に任された（@ope-ultp1635 msg dfcb091f）。使っていない。理由: (1) 公開の記録どうしが食い違っている — 行 12・14 の備考は「operator が記入した」と書き、行を入れた commit 383a09c の件名は「下書き・commit は @philosopher、確定は operator の照合」と書く。どちらが事実かを本が決めて書くことはできない。(2) 読み手は自分の案件に Core を当てるエンジニアで、所有者の言葉を operator が中継する形は読み手の案件から遠い。実例から取れる一般の問い（提起した者と承認した者が別だと、記録の上でどう示すか）は、Core が決めていないこととして最後のページに置いた。
④の洗い出し（@ope-ultp1635 msg 02ab9595、@reviewer 2026-11-08 ch10-12 4-1）: 「編集できても、承認ではない」は profiles.md:73 の「共有するProfileの正本の改訂」の文を、文書一般に広げて書いていた。字を Profile の正本に戻した。
包含と同じ形の字: profiles.md 4 節の 51 行「Enterprise Cellが複数Profileをまとめて引き受けてよい」・62 行「EnterpriseがDomain Profileを提供する場合、Enterpriseが正本を管理する」は使っていない。使ったのは 73 行だけ。
絵: Cell はどれもほかの Cell の枠の外に並べる（core.md:43）。人は橙の四角、Agent は青の丸い札（第 0・2 章と同じ）。
新しく引く外部の文献は無い。
準拠先（③、@ope-ultp1635 msg 6ec153b2）: 例の 3 項目は在庫と物流の Contract の欄で、Cell 間で共有する文書の準拠先は core.md:94 で自己改訂規範アーキテクチャ v1・最小構成と決まっている（core.md:12 の Core 自身の準拠先も同じ）。前の版は「EAA Core 版 6」と書いており誤りだったので、第 8 章の例に揃えた。各 Cell の中の規範が Core に準拠する話はこの章では書いていない。
⑥（@ope-ultp1635 msg 6fc17eeb、@reviewer 2〜4 回目）: 章題「改訂は提起した者以外が承認する」と最後のページから「所有者が承認する」（core.md:90）が落ちていた。「以外」だと所有者でない人でも承認できると読める。章題を「改訂は人間の所有者が承認し、提起した者は承認しない」にし（titles.md に記録）、最後のページの左と文に足した。p.「中の改訂の手続き」は、絵の結び・文が「Core の条件は中の規範に及ばない」、注が「緩めない行は中にも及ぶ」で逆だった。core.md:94-95 で中に及ばないのは「所有者・観測・準拠先を持つ」（同アーキテクチャへの準拠）の要求で、core.md:96 は文書を限っていない。絵の結び・文の主語をその要求に絞り、注が指す行を前の 2 ページと書いた。
⑤（@ope-ultp1635 msg 281e5366、@reviewer 3 回目・4 回目）: 最後のページで、所有者本人の改訂の承認者を「決めていないこと」から外し、core.md:90・94・98 からの帰結として左に書いた。例のページの文に core.md:90（改訂を判断するのは所有者）を足した。残りの 2 項目は core.md:11 に無いので「Core に書かれていない」。権限が足りないときの戻し先を core.md:70 の字「正当な判断主体」に揃えた（第 2・4 章と同じ）。
2 周目（@ope-ultp1635 msg 8fbac4e5、@reader r2 cea29c1f）: 最後のページの右の小見出しを「既知の不足にも挙がっていない」にした（理由は第 6 章の注と同じ）。例のページの絵の準拠先の行に「Core 自身の準拠先も同じ」を足した（core.md:12）。
-->

> 実行者は、自分を縛る規範を緩める変更も、自分の権限を広げる変更も自己承認できない。行う者と、承認・検証する者を分ける。

```svg
<svg viewBox="0 0 880 300" width="880" height="300">
  <rect x="40" y="40" width="240" height="170" rx="10" class="box"/><text x="160" y="76" class="t" text-anchor="middle" font-weight="700">提起する者</text>
  <use href="#i-no" x="146" y="110" width="28" height="28"/><text x="160" y="170" class="ts xc" text-anchor="middle">自分では承認しない</text>
  <rect x="330" y="70" width="220" height="80" rx="3" class="hl" style="fill:#fff"/><text x="440" y="104" class="ts hc" text-anchor="middle" font-weight="700">共有する文書</text><text x="440" y="130" class="tx" text-anchor="middle">改訂の案</text>
  <path d="M280,110 H326" class="ln" marker-end="url(#arr)"/><path d="M554,110 H596" class="ln" marker-end="url(#arr)"/>
  <rect x="600" y="40" width="240" height="170" rx="10" class="box"/><text x="720" y="76" class="t" text-anchor="middle" font-weight="700">承認する者</text>
  <rect x="660" y="94" width="120" height="36" rx="6" class="h"/><text x="720" y="118" class="ts on" text-anchor="middle">所有者・人間</text>
  <use href="#i-ok" x="706" y="144" width="28" height="28"/><text x="720" y="196" class="ts okc" text-anchor="middle">承認する</text>
  <text x="440" y="264" class="t" text-anchor="middle" font-weight="700">同じ改訂を、出す者と認める者が別の人</text>
</svg>
```

共有する文書の改訂は、その文書の所有者が承認します。所有者は人間で、改訂を提起した者は、その改訂を承認しません。

## 共有する文書は、所有者を持つ

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <g class="ts" text-anchor="middle">
    <rect x="30" y="50" width="150" height="70" rx="3" class="hl" style="fill:#fff"/><text x="105" y="91">Contract</text>
    <rect x="200" y="50" width="150" height="70" rx="3" class="hl" style="fill:#fff"/><text x="275" y="80">共有する</text><text x="275" y="104">Profile</text>
    <rect x="370" y="50" width="150" height="70" rx="3" class="hl" style="fill:#fff"/><text x="445" y="80">共有する</text><text x="445" y="104">Ontology</text>
    <rect x="540" y="50" width="150" height="70" rx="3" class="hl" style="fill:#fff"/><text x="615" y="80">Evidence の</text><text x="615" y="104">様式</text>
    <rect x="710" y="50" width="150" height="70" rx="3" class="hl" style="fill:#fff"/><text x="785" y="91">EAA Core</text>
  </g>
  <path d="M105,124 V168 M275,124 V168 M445,124 V168 M615,124 V168 M785,124 V168 M105,168 H785 M445,168 V196" class="lt"/>
  <rect x="200" y="200" width="490" height="130" rx="10" class="soft"/>
  <text x="445" y="236" class="t" text-anchor="middle" font-weight="700">どれも、次の 3 項目を持つ</text>
  <g class="ts" text-anchor="middle"><text x="290" y="290">所有者</text><text x="445" y="290">観測</text><text x="600" y="290">準拠先</text></g>
</svg>
```

Contract、共有する Profile・Ontology、Evidence の様式と Core は、どれも所有者・観測・準拠先を持ちます。

出典: EAA Core 版 6「4. 提案と変更」。

## 例：在庫と物流の Contract の 3 項目

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <text x="60" y="50" class="ts hc" font-weight="700">在庫と物流のあいだの Contract　版 1</text>
  <g class="ts">
    <text x="60" y="110" font-weight="700">所有者</text><text x="220" y="110">物流の窓口の責任者</text><text x="560" y="110" class="tx">変更を承認する人</text>
    <text x="60" y="180" font-weight="700">観測</text><text x="220" y="180">受け入れられなかった出荷結果と、</text><text x="220" y="204">その理由</text><text x="560" y="180" class="tx">見直しの根拠に残す記録</text>
    <text x="60" y="274" font-weight="700">準拠先</text><text x="220" y="262">自己改訂規範アーキテクチャ</text><text x="220" y="286">v1・最小構成</text><text x="560" y="262" class="tx">従う上位の規範と、その版</text><text x="560" y="286" class="tx">Core 自身の準拠先も同じ</text>
  </g>
  <path d="M40,70 H840 M40,140 H840 M40,234 H840 M40,304 H840" class="lt"/>
</svg>
```

在庫と物流の Contract なら、所有者は物流の窓口の責任者、観測は受け入れられなかった出荷結果、準拠先は自己改訂規範アーキテクチャ v1・最小構成です。

※ 観測の中身は説明のための仮定です。3 項目の意味は Core 版 6 の冒頭にある Core 自身の表から取り、準拠先は Core「4. 提案と変更」の字のとおり（第 8 章と同じ）です。

## 所有者は人間

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="340" height="230" rx="10" class="box"/><text x="210" y="96" class="t" text-anchor="middle" font-weight="700">物流の Cell</text>
  <rect x="80" y="130" width="120" height="44" rx="22" class="a"/><text x="140" y="158" class="ts on" text-anchor="middle">Agent</text>
  <text x="140" y="206" class="ts" text-anchor="middle">改訂の文面を書く</text>
  <rect x="230" y="130" width="120" height="44" rx="6" class="h"/><text x="290" y="158" class="ts on" text-anchor="middle">所有者</text>
  <text x="290" y="206" class="ts" text-anchor="middle">人間</text>
  <path d="M380,170 H496" class="ln" marker-end="url(#arr)"/>
  <rect x="500" y="110" width="340" height="120" rx="3" class="hl" style="fill:#fff"/><text x="670" y="150" class="ts hc" text-anchor="middle" font-weight="700">承認するのは、人間の所有者</text>
  <text x="670" y="190" class="ts" text-anchor="middle">Agent は所有者にならない</text>
</svg>
```

共有する文書の所有者は人間です。改訂の文面を Agent が書いても、承認するのは人間の所有者です。

出典: EAA Core 版 6「4. 提案と変更」。

## 提起した者は、承認しない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="300" height="220" rx="10" class="box"/><text x="190" y="96" class="t" text-anchor="middle" font-weight="700">改訂を提起した者</text>
  <use href="#i-no" x="176" y="140" width="28" height="28"/><text x="190" y="200" class="ts xc" text-anchor="middle">その改訂は承認しない</text>
  <text x="190" y="236" class="tx" text-anchor="middle">提供する側に属していても</text>
  <path d="M340,170 H536" class="ln" marker-end="url(#arr)"/><use href="#i-pr" x="425" y="128" width="30" height="38"/>
  <rect x="540" y="60" width="300" height="220" rx="10" class="box"/><text x="690" y="96" class="t" text-anchor="middle" font-weight="700">ほかの、所有者</text>
  <use href="#i-ok" x="676" y="140" width="28" height="28"/><text x="690" y="200" class="ts okc" text-anchor="middle">承認する</text>
</svg>
```

改訂を提起した者は、その改訂を承認しません。文書を提供する側に属していても同じです。

出典: EAA Core 版 6「4. 提案と変更」、EAA Profiles「4.」の「改訂元と採用先を分ける」。第 9 章の希望時間帯の例は、この形でした。

## 職務分離の一つ

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <g class="ts">
    <text x="60" y="60" font-weight="700">判断</text><text x="330" y="60" font-weight="700">行う者</text><text x="600" y="60" font-weight="700">承認・検証する者</text>
    <text x="60" y="130">共有する文書の改訂</text><text x="330" y="130">提起する者</text><text x="600" y="130">提起していない所有者</text>
    <text x="60" y="200">Mission の完了</text><text x="330" y="200">作業する者</text><text x="600" y="200">確かめる者</text>
  </g>
  <path d="M40,80 H840 M40,160 H840 M40,230 H840 M560,30 V230" class="lt"/>
  <rect x="40" y="270" width="800" height="70" rx="10" class="soft"/>
  <text x="440" y="312" class="t" text-anchor="middle" font-weight="700">同じ判断を、別の者に分ける</text>
</svg>
```

同じ判断を、行う者と、承認または検証する者に分けることを職務分離と呼びます。提起した者が承認しないのは、その一つです。

出典: EAA Core 版 6 の概念表「職務分離」と「5. 成果と記録」。Mission の完了の分離は第 7 章で見ました。

## 自分を縛る規範を、自分で緩めない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="340" height="230" rx="10" class="box"/><text x="210" y="96" class="t" text-anchor="middle" font-weight="700">物流の Cell</text>
  <rect x="80" y="126" width="260" height="44" rx="22" class="a"/><text x="210" y="154" class="ts on" text-anchor="middle">出荷を担う Agent</text>
  <text x="210" y="210" class="ts" text-anchor="middle">「欠品の理由を残す手順を</text><text x="210" y="236" class="ts" text-anchor="middle">外したい」</text>
  <path d="M380,170 H496" class="ln" marker-end="url(#arr)"/>
  <rect x="500" y="60" width="340" height="230" rx="10" class="soft"/>
  <use href="#i-no" x="526" y="100" width="24" height="24"/><text x="562" y="118" class="ts">自分では承認しない</text>
  <use href="#i-ok" x="526" y="160" width="24" height="24"/><text x="562" y="178" class="ts">緩めるかは、正当な所有者が</text><text x="562" y="202" class="ts">承認して決める</text>
</svg>
```

実行者は、自分を縛る規範を緩める変更を、自分で承認してはいけません。緩めてよいかは、正当な所有者が承認して決めます。

出典: EAA Core 版 6「4. 提案と変更」。※ 例は説明のための仮定です。

## 自分の権限を、自分で広げない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="300" height="220" rx="10" class="box"/><text x="190" y="96" class="t" text-anchor="middle" font-weight="700">物流の Cell</text>
  <rect x="70" y="126" width="240" height="44" rx="22" class="a"/><text x="190" y="154" class="ts on" text-anchor="middle">出荷を担う Agent</text>
  <text x="190" y="214" class="ts" text-anchor="middle">在庫の引き当てを、</text><text x="190" y="240" class="ts" text-anchor="middle">直接書き換えたい</text>
  <rect x="540" y="60" width="300" height="220" rx="10" class="box"/><text x="690" y="96" class="t" text-anchor="middle" font-weight="700">在庫の Cell</text>
  <path d="M340,140 H536" class="xl dash"/><use href="#i-no" x="424" y="112" width="28" height="28"/><text x="440" y="170" class="ts xc" text-anchor="middle">自分で権限を足さない</text>
  <path d="M340,230 H536" class="ln" marker-end="url(#arr)"/><text x="440" y="222" class="ts" text-anchor="middle">足りないと示して、提案する</text>
</svg>
```

実行者は、自ら権限を広げてはいけません。権限が足りないときは、それを示し、正当な判断主体との調整に戻します。

出典: EAA Core 版 6「4. 提案と変更」「2. 自治と権限」。※ 例は説明のための仮定です。

## 編集できても、承認ではない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="340" height="220" rx="10" class="soft"/>
  <text x="210" y="100" class="t" text-anchor="middle" font-weight="700">Profile の正本を編集できる</text>
  <use href="#i-pr" x="195" y="130" width="30" height="38"/>
  <text x="210" y="210" class="ts" text-anchor="middle">GitHub に書き込める</text><text x="210" y="236" class="ts" text-anchor="middle">権限も、これに当たる</text>
  <path d="M380,170 H496" class="xl dash"/><use href="#i-no" x="424" y="142" width="28" height="28"/>
  <rect x="500" y="60" width="340" height="220" rx="10" class="box"/>
  <g class="ts"><text x="530" y="110">これだけでは、できないこと</text><text x="530" y="160">・合意した義務を消す</text><text x="530" y="196">・合意した義務を緩める</text><text x="530" y="232">・権限を足す</text></g>
</svg>
```

Profile の正本を編集できる権限だけでは、合意した義務を消したり緩めたり、権限を足したりできません。リポジトリに書き込めることも、承認ではありません。

出典: EAA Profiles「4.」の「改訂元と採用先を分ける」（共有する Profile の正本の改訂の行）。※ 書き込みの権限を文書の編集権に当てたのは、この本の読みです。

## 中の改訂の手続きは、各 Cell が決める

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="50" width="260" height="200" rx="10" class="box"/><text x="170" y="86" class="t" text-anchor="middle" font-weight="700">在庫の Cell</text><text x="170" y="150" class="ts" text-anchor="middle">中の規範の改訂は</text><text x="170" y="176" class="ts" text-anchor="middle">在庫が決めた手続き</text>
  <rect x="580" y="50" width="260" height="200" rx="10" class="box"/><text x="710" y="86" class="t" text-anchor="middle" font-weight="700">物流の Cell</text><text x="710" y="150" class="ts" text-anchor="middle">中の規範の改訂は</text><text x="710" y="176" class="ts" text-anchor="middle">物流が決めた手続き</text>
  <rect x="330" y="110" width="220" height="80" rx="3" class="hl" style="fill:#fff"/><text x="440" y="144" class="ts hc" text-anchor="middle" font-weight="700">Contract</text><text x="440" y="170" class="tx" text-anchor="middle">所有者・観測・準拠先を持つ</text>
  <path d="M300,150 H326 M554,150 H576" class="ln"/>
  <text x="440" y="310" class="t" text-anchor="middle" font-weight="700">所有者・観測・準拠先の要求が及ぶのは、共有する文書</text>
</svg>
```

所有者・観測・準拠先を持つという要求は、Cell の中の規範には及びません。中の改訂の手続きは各 Cell が決めます。

出典: EAA Core 版 6「4. 提案と変更」。※ 前の 2 ページ（自分を縛る規範を緩めない・自分で権限を広げない）の行は共有する文書に限っていないので、中の規範にも当たる、と読みました。

## 例：所有者本人が提起したら

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="60" width="300" height="220" rx="10" class="box"/><text x="190" y="96" class="t" text-anchor="middle" font-weight="700">物流の Cell</text>
  <rect x="120" y="120" width="140" height="40" rx="6" class="h"/><text x="190" y="146" class="ts on" text-anchor="middle">所有者</text>
  <text x="190" y="200" class="ts" text-anchor="middle">締めを 15 時から 14 時に</text><text x="190" y="224" class="ts" text-anchor="middle">早める改訂を提起</text>
  <path d="M340,170 H536" class="ln" marker-end="url(#arr)"/>
  <rect x="540" y="60" width="300" height="220" rx="10" fill="url(#hatch)"/><text x="690" y="130" class="t" text-anchor="middle" font-weight="700">承認する者</text>
  <text x="690" y="180" class="tl" text-anchor="middle">？</text>
  <text x="690" y="236" class="ts" text-anchor="middle">所有者は 1 人で、提起した本人</text>
</svg>
```

第 9 章の締めの時刻の改訂を、所有者本人が提起したとします。改訂を判断するのは所有者、提起した者は承認せず、所有者は 1 人なので、承認できる者がいません。

※ 例は説明のための仮定です。出典: EAA Core 版 6「4. 提案と変更」。この場合の承認者は、第 8 章の最後のページでも挙げました。

## Core はここまでしか決めていない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="30" width="380" height="290" rx="10" class="soft"/>
  <text x="60" y="64" class="t" font-weight="700">Core が決めていること</text>
  <g class="ts"><use href="#i-ok" x="60" y="88" width="22" height="22"/><text x="92" y="105">改訂は人間の所有者が承認する</text>
  <use href="#i-ok" x="60" y="128" width="22" height="22"/><text x="92" y="145">提起した者は承認しない</text>
  <use href="#i-ok" x="60" y="168" width="22" height="22"/><text x="92" y="185">自分を縛る規範を緩めない</text>
  <use href="#i-ok" x="60" y="208" width="22" height="22"/><text x="92" y="225">自分の権限を広げない</text>
  <use href="#i-ok" x="60" y="248" width="22" height="22"/><text x="92" y="265">中の改訂の手続きは各 Cell</text></g>
  <text x="60" y="304" class="ts" font-weight="700">→ 所有者本人の改訂は、承認できる者がいない</text>
  <rect x="460" y="30" width="380" height="290" rx="10" fill="url(#hatch)"/>
  <text x="480" y="64" class="t" font-weight="700">決めていないこと</text>
  <g class="ts"><text x="480" y="102" class="ts" font-weight="700">Core に書かれていない</text><text x="480" y="126" class="tx">既知の不足にも挙がっていない</text><text x="480" y="166" class="ts">提起した者と承認した者が別だと、</text><text x="480" y="190" class="ts">記録の上でどう示すか</text><text x="480" y="230" class="ts">承認の手続きの細部</text></g>
  <text x="440" y="356" class="ts sub" text-anchor="middle">承認の手続きは、それぞれの判断に当てる手続きに任せている</text>
</svg>
```

改訂は人間の所有者が承認し、提起した者は承認しないので、所有者本人の改訂は承認できる者がいません。二者が別だと記録でどう示すかは、Core に書かれていません。

出典: EAA Core 版 6「4. 提案と変更」「5. 成果と記録」。Core は職務分離を保つことと、改訂を後から追える記録に残すことだけを求めています。
