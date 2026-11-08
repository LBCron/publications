# 第 0 章　チームのあいだは、人や会議でなく、版付きの文書と Evidence でつなぐ

群: チームのあいだの合意と、集中・分散の失敗

<!--
構造: agent-hub-roles-kaz/philosopher/2026-11-07-eaa-textbook-structure.md（55553ae4）。章題と群の札の字は writer-ja/drafts/eaa-toc/titles.md（d21b0d80、@ope-ultp1635 msg 65a67e15）で書き直した。構造は変えない。
出どころ（構造の表のまま）: core.md:16-24、素材 0（drafts/agentic-agile-materials/explanations/eaa/0-two-exits.html）。Core は publications origin/main 0d07f75 の core.md 版 6。
本文: @ope-ultp1635 msg a8d86548（群ごとに 4 回。群一から）。骨格の章の概要の後ろに本文のページを足した。
絵: Cell は枠の外に対等に並べ、どの Cell もほかの Cell の枠の中に描かない（同 msg。core.md:43「分割の後の両者の関係は、ほかの Cell どうしと同じ Cell の間の関係である」）。
包含の字のある development-model.md:25・33、working-notes.md:13 は出どころに使っていない（同 msg）。
-->

> この本では、自律して開発する主体を Cell と呼ぶ。Cell を分けて広げる目的は、互いの成果を受け取り、その上に次の成果を積めるようにすることで、そのために境界を越えて流れるのは Evidence である。

```svg
<svg viewBox="0 0 880 300" width="880" height="300">
  <g opacity=".7">
    <rect x="20" y="40" width="70" height="44" rx="6" fill="#b5b5b5"/><text x="55" y="68" class="ts on" text-anchor="middle">一人</text>
    <rect x="20" y="100" width="70" height="44" rx="6" fill="#b5b5b5"/><text x="55" y="128" class="ts on" text-anchor="middle">会議</text>
    <use href="#i-no" x="80" y="30" width="22" height="22"/><use href="#i-no" x="80" y="90" width="22" height="22"/>
    <text x="55" y="170" class="tx" text-anchor="middle">預けない</text>
  </g>
  <rect x="140" y="60" width="170" height="130" rx="10" class="box"/><text x="225" y="92" class="t" text-anchor="middle" font-weight="700">Cell</text><text x="225" y="120" class="ts sub" text-anchor="middle">中は各自の作り方</text>
  <rect x="680" y="60" width="170" height="130" rx="10" class="box"/><text x="765" y="92" class="t" text-anchor="middle" font-weight="700">Cell</text><text x="765" y="120" class="ts sub" text-anchor="middle">中は各自の作り方</text>
  <path d="M495,30 V240" class="lt dash"/>
  <rect x="440" y="36" width="110" height="64" rx="3" class="hl" style="fill:#fff"/><text x="495" y="62" class="ts hc" text-anchor="middle">Contract</text><text x="495" y="86" class="t hc" text-anchor="middle" font-weight="700">版 3</text>
  <path d="M310,150 H672" class="ln" marker-end="url(#arr)"/>
  <use href="#i-pr" x="400" y="128" width="30" height="38"/><text x="415" y="186" class="ts" text-anchor="middle">Evidence</text>
  <use href="#i-ok" x="700" y="140" width="28" height="28"/><text x="790" y="160" class="ts okc" text-anchor="middle">確かめる</text>
  <text x="495" y="282" class="t" text-anchor="middle" font-weight="700">あいだは、版付きの文書に書き、Evidence で確かめる</text>
</svg>
```

先に、この本が勧めるつなぎ方を言います。なぜ今それが要るのかは、第 1 章で見ます。

## チームのあいだに要る合意

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="70" width="200" height="200" rx="10" class="box"/><text x="140" y="110" class="t" text-anchor="middle" font-weight="700">チーム</text>
  <rect x="640" y="70" width="200" height="200" rx="10" class="box"/><text x="740" y="110" class="t" text-anchor="middle" font-weight="700">チーム</text>
  <rect x="260" y="70" width="360" height="200" rx="10" class="soft"/>
  <text x="440" y="56" class="ts sub" text-anchor="middle">あいだ</text>
  <g class="ts" text-anchor="middle">
    <rect x="300" y="96" width="280" height="44" rx="6" class="hl" style="fill:#fff"/><text x="440" y="124">インターフェース</text>
    <rect x="300" y="150" width="280" height="44" rx="6" class="hl" style="fill:#fff"/><text x="440" y="178">依存</text>
    <rect x="300" y="204" width="280" height="44" rx="6" class="hl" style="fill:#fff"/><text x="440" y="232">順序</text>
  </g>
  <path d="M240,170 H296 M584,170 H640" class="ln"/>
  <text x="440" y="320" class="t" text-anchor="middle" font-weight="700">この合意を、誰がどう持つか</text>
  <text x="440" y="350" class="ts sub" text-anchor="middle">何を作るか・何に投資するかは、決める人がこれまでどおり決める</text>
</svg>
```

開発が一つのチームに収まらなくなると、チームのあいだに合意が要ります。インターフェース、依存、順序です。この本は、この合意の持ち方を扱います。

※ 複数社で組むなら、これは契約・検収・責任分界の問いでもあります。

## Cell：判断の責任者ごとの単位

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <g>
    <rect x="40" y="50" width="240" height="230" rx="10" class="box"/>
    <rect x="125" y="70" width="70" height="40" rx="6" class="h"/><text x="160" y="96" class="ts on" text-anchor="middle">責任者</text>
    <rect x="70" y="140" width="180" height="44" rx="22" class="a"/><text x="160" y="168" class="ts on" text-anchor="middle">AI エージェントが作る</text>
    <text x="160" y="240" class="ts" text-anchor="middle">AA で動く Cell</text>
  </g>
  <g>
    <rect x="320" y="50" width="240" height="230" rx="10" class="box"/>
    <rect x="405" y="70" width="70" height="40" rx="6" class="h"/><text x="440" y="96" class="ts on" text-anchor="middle">責任者</text>
    <g class="h"><rect x="356" y="140" width="40" height="44" rx="6"/><rect x="420" y="140" width="40" height="44" rx="6"/><rect x="484" y="140" width="40" height="44" rx="6"/></g>
    <text x="440" y="240" class="ts" text-anchor="middle">Scrum のチーム</text>
  </g>
  <g>
    <rect x="600" y="50" width="240" height="230" rx="10" class="box"/>
    <rect x="685" y="70" width="70" height="40" rx="6" class="h"/><text x="720" y="96" class="ts on" text-anchor="middle">責任者</text>
    <path d="M640,162 H800" class="ln" marker-end="url(#arr)"/><g class="tx"><text x="650" y="150">要件</text><text x="700" y="150">設計</text><text x="750" y="150">試験</text></g>
    <text x="720" y="240" class="ts" text-anchor="middle">委託先の標準工程</text>
  </g>
  <text x="440" y="324" class="t" text-anchor="middle" font-weight="700">中の作り方は問わない。どれも同じ形でつながる</text>
  <text x="440" y="356" class="ts sub" text-anchor="middle">Cell はどれも対等に並ぶ。ほかの Cell の中には入らない</text>
</svg>
```

この本では、目的に対する責任・権限・実行能力を持ち、外との合意に基づいて自律して成果を出す単位を Cell と呼びます。中の作り方は問いません。

※ Cell の数え方は第 2 章、分け方は第 3 章。AA は、一つの Cell の中で AI エージェントに開発を任せるやり方で、同じ組の AA の本が扱います。

## 広げる目的：受け取り、上に積む

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="200" width="200" height="110" rx="10" class="box"/><text x="140" y="290" class="ts" text-anchor="middle">Cell</text>
  <rect x="340" y="200" width="200" height="110" rx="10" class="box"/><text x="440" y="290" class="ts" text-anchor="middle">Cell</text>
  <rect x="640" y="200" width="200" height="110" rx="10" class="box"/><text x="740" y="290" class="ts" text-anchor="middle">Cell</text>
  <rect x="90" y="216" width="100" height="36" rx="4" class="a"/><text x="140" y="240" class="ts on" text-anchor="middle">成果 1</text>
  <rect x="390" y="216" width="100" height="36" rx="4" class="a"/><text x="440" y="240" class="ts on" text-anchor="middle">成果 1</text>
  <rect x="390" y="174" width="100" height="36" rx="4" class="ok"/><text x="440" y="198" class="ts on" text-anchor="middle">成果 2</text>
  <rect x="690" y="216" width="100" height="36" rx="4" class="a"/><text x="740" y="240" class="ts on" text-anchor="middle">成果 1</text>
  <rect x="690" y="174" width="100" height="36" rx="4" class="ok"/><text x="740" y="198" class="ts on" text-anchor="middle">成果 2</text>
  <rect x="690" y="132" width="100" height="36" rx="4" class="h"/><text x="740" y="156" class="ts on" text-anchor="middle">成果 3</text>
  <path d="M240,234 H334" class="ln" marker-end="url(#arr)"/><text x="287" y="224" class="tx" text-anchor="middle">受け取る</text>
  <path d="M540,214 H634" class="ln" marker-end="url(#arr)"/><text x="587" y="204" class="tx" text-anchor="middle">受け取る</text>
  <text x="440" y="70" class="t" text-anchor="middle" font-weight="700">互いの成果を受け取り、その上に次の成果を積む</text>
  <text x="440" y="100" class="ts sub" text-anchor="middle">分けて広げるのは、このため</text>
  <text x="440" y="350" class="ts sub" text-anchor="middle">受け取るたびに、相手の中を作り直さない</text>
</svg>
```

Cell を分けて広げる目的は、Cell どうしが互いの成果を受け取り、その上に次の成果を積めるようにすることです。

出典: EAA Core 版 6「0. 目的と範囲」。EAA Core は、この本の決まりを定める規範案です。

## 境界を越えるのは Evidence

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="70" width="240" height="200" rx="10" class="box"/><text x="160" y="104" class="t" text-anchor="middle" font-weight="700">作った Cell</text>
  <rect x="600" y="70" width="240" height="200" rx="10" class="box"/><text x="720" y="104" class="t" text-anchor="middle" font-weight="700">受け取る Cell</text>
  <path d="M440,40 V300" class="lt dash"/><text x="440" y="30" class="tx" text-anchor="middle">境界</text>
  <rect x="100" y="140" width="120" height="44" rx="4" class="a"/><text x="160" y="168" class="ts on" text-anchor="middle">成果</text>
  <path d="M220,162 H594" class="ln" marker-end="url(#arr)"/>
  <use href="#i-pr" x="350" y="122" width="30" height="38"/><text x="440" y="150" class="ts" text-anchor="middle" font-weight="700">Evidence</text>
  <rect x="350" y="182" width="180" height="20" style="fill:#fff"/><text x="440" y="197" class="tx" text-anchor="middle">成り立ったことを確かめる記録</text>
  <use href="#i-ok" x="626" y="146" width="30" height="30"/><text x="740" y="168" class="ts okc" text-anchor="middle">自分で確かめる</text>
  <path d="M700,220 C 600,300 300,300 200,226" fill="none" stroke="#c62828" stroke-width="2" class="dash" marker-end="url(#arr-x)"/>
  <use href="#i-no" x="428" y="276" width="24" height="24"/><text x="440" y="324" class="ts xc" text-anchor="middle">作った側に聞かないと確かめられない形にしない</text>
</svg>
```

境界を越えて流れるのは、成果が成り立ったことを確かめる記録、Evidence です。受け取った Cell が、作った Cell を介さずに確かめられる形にします。

※ 確かめるのが受け取った側なのは、どの Cell の判断も、ほかの Cell が一方的に上書きしないから。上書きの決まりは第 4 章、Evidence は第 6 章。

## つなぐのは版の付いた共有文書

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <rect x="40" y="80" width="200" height="190" rx="10" class="box"/><text x="140" y="116" class="t" text-anchor="middle" font-weight="700">Cell</text>
  <rect x="640" y="80" width="200" height="190" rx="10" class="box"/><text x="740" y="116" class="t" text-anchor="middle" font-weight="700">Cell</text>
  <rect x="330" y="40" width="220" height="150" rx="4" class="hl" style="fill:#fff"/>
  <text x="350" y="72" class="t hc" font-weight="700">Contract</text><text x="530" y="72" class="t hc" text-anchor="end" font-weight="700">版 3</text>
  <g class="ts"><text x="350" y="104">相互の責任・提供条件</text><text x="350" y="130">入出力</text><text x="350" y="156" class="hc" font-weight="700">渡す Evidence</text></g>
  <path d="M240,150 H326 M554,150 H640" class="ln"/>
  <path d="M240,236 H634" class="ln" marker-end="url(#arr)"/><use href="#i-pr" x="425" y="214" width="26" height="34"/><text x="474" y="230" class="ts">Evidence</text>
  <g class="tx" text-anchor="middle">
    <rect x="200" y="300" width="140" height="32" rx="4" class="lt" style="fill:#fff"/><text x="270" y="321">共有する Profile</text>
    <rect x="370" y="300" width="140" height="32" rx="4" class="lt" style="fill:#fff"/><text x="440" y="321">共有する Ontology</text>
    <rect x="540" y="300" width="140" height="32" rx="4" class="lt" style="fill:#fff"/><text x="610" y="321">Evidence の様式</text>
  </g>
  <text x="440" y="362" class="ts sub" text-anchor="middle">ほかの共有文書にも版が付く。どの版に従うかは各 Cell が決める</text>
</svg>
```

どの Evidence を渡すかは、Cell のあいだで共有する文書の Contract に書きます。共有する文書には版が付き、どの版に従うかは各 Cell が決めます。

※ 共有する文書の所有者は人間で、改訂を提起した者はその改訂を承認しない（第 10 章）。Contract は第 8 章、版の採用は第 9 章。

## 一人にも会議にも預けない

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <path d="M295,20 V250 M585,20 V250" class="lt dash"/>
  <g class="t" text-anchor="middle" font-weight="700"><text x="150" y="40">一人や会議に集める</text><text x="440" y="40">各チームに任せきる</text><text x="730" y="40" class="hc">EAA：文書と Evidence</text></g>
  <rect x="115" y="70" width="70" height="44" rx="6" class="h"/><text x="150" y="98" class="ts on" text-anchor="middle">一人</text>
  <use href="#i-wait" x="74" y="130" width="22" height="30"/><use href="#i-wait" x="104" y="130" width="22" height="30"/><use href="#i-wait" x="134" y="130" width="22" height="30"/><use href="#i-wait" x="164" y="130" width="22" height="30"/><use href="#i-wait" x="194" y="130" width="22" height="30"/>
  <text x="150" y="200" class="ts sub" text-anchor="middle">判断待ちが伸びる</text>
  <rect x="380" y="70" width="120" height="70" rx="3" class="xl" style="fill:#fff"/><text x="440" y="100" class="ts xc" text-anchor="middle">取り決め</text><text x="440" y="126" class="ts xc" text-anchor="middle">版 3 → 版 4</text>
  <text x="440" y="174" class="ts xc" text-anchor="middle">片側だけで書き換える</text>
  <text x="440" y="200" class="ts sub" text-anchor="middle">承認なしに変わる</text>
  <rect x="610" y="70" width="70" height="56" rx="8" class="box"/><rect x="780" y="70" width="70" height="56" rx="8" class="box"/>
  <rect x="696" y="60" width="68" height="44" rx="3" class="hl" style="fill:#fff"/><text x="730" y="88" class="ts hc" text-anchor="middle">版 3</text>
  <path d="M680,116 H774" class="ln" marker-end="url(#arr)"/><use href="#i-ok" x="716" y="130" width="28" height="28"/>
  <text x="730" y="200" class="ts hc" text-anchor="middle">書いて、受け取る側が確かめる</text>
  <rect x="40" y="262" width="800" height="100" rx="10" class="hl" style="fill:#fff"/>
  <text x="440" y="302" class="tl hc" text-anchor="middle">集めるのでも、任せきるのでもない。</text>
  <text x="440" y="340" class="tl hc" text-anchor="middle">あいだは版付きの文書に書き、Evidence で確かめる</text>
</svg>
```

あいだの合意を、一人や定例の会議に集めるのでも、各チームに任せきるのでもなく、版付きの文書に書き、Evidence で確かめます。

※ 左と中のやり方が、なぜ今うまくいかないかは第 1 章で見ます。

## この本の構成：流れを守る決まり

```svg
<svg viewBox="0 0 880 380" width="880" height="380">
  <g class="ts">
    <rect x="40" y="20" width="800" height="62" rx="6" class="soft"/>
    <text x="60" y="47" font-weight="700">チームのあいだの合意と、集中・分散の失敗</text>
    <text x="60" y="71" class="sub">いまの章と第 1 章。なぜ文書と Evidence でつなぐのか</text>
    <a href="#ch1"><text x="820" y="47" text-anchor="end">第 1 章</text></a>
    <rect x="40" y="96" width="800" height="62" rx="6" class="lt" style="fill:#fff"/>
    <text x="60" y="123" font-weight="700">Cell の分割と自治</text>
    <text x="60" y="147" class="sub">Cell の数え方・分け方と、分けた後に上書きしないこと</text>
    <a href="#ch2"><text x="820" y="123" text-anchor="end">第 2 章から</text></a>
    <rect x="40" y="172" width="800" height="62" rx="6" class="lt" style="fill:#fff"/>
    <text x="60" y="199" font-weight="700">Evidence・Mission・Contract と版</text>
    <text x="60" y="223" class="sub">境界に流すもの、仕事の渡し方、取り決めとその版</text>
    <a href="#ch6"><text x="820" y="199" text-anchor="end">第 6 章から</text></a>
    <rect x="40" y="248" width="800" height="62" rx="6" class="lt" style="fill:#fff"/>
    <text x="60" y="275" font-weight="700">規範の承認・採用と導入</text>
    <text x="60" y="299" class="sub">誰が文書の改訂を承認し、誰が採用を決め、どう始めるか</text>
    <a href="#ch10"><text x="820" y="275" text-anchor="end">第 10 章から</text></a>
  </g>
  <text x="440" y="350" class="t" text-anchor="middle" font-weight="700">第 2 章から先は、受け取って積む流れを守る決まり</text>
</svg>
```

第 2 章から先は、受け取って上に積む流れを守るための決まりです。Cell の分け方と自治、境界に流すものと取り決め、文書の承認と採用、導入の順に見ます。

出典: EAA Core 版 6「0. 目的と範囲」。この本は、Core に無い決まりを足しません。
