# 【設計図】スマートフォン向け「幸せの好循環サイクル」レイアウト＆デザイン仕様書

薄倉さんのホームページ（GitHub Pages）のメインビジュアル直下に配置する、「幸せの好循環サイクル」を直感的に伝えるためのデザイン・レイアウトの設計図です。
若草色（#9bca3e）をメインに据え、高齢者にも現役世代にも一目で「すべての世代が豊かになる循環」が理解できる構成にしています。

---

## 1. 画面全体のデザインコンセプト（若草色テーマ）

| 役割 | カラーコード | デザイン上の役割 |
| :--- | :--- | :--- |
| **メイン（ブランドカラー）** | `#9bca3e` (若草色) | 循環を繋ぐ矢印、各ステップの番号、メインのボタンに使用。 |
| **ベース背景** | `#f4f9eb` (極薄の緑) | カードの背景やセクション全体の背景。目に優しくクリーンな印象。 |
| **テキスト・引き締め** | `#2f5213` (深緑) | タイトル、本文、枠線に使用。黒よりもナチュラルで知的な印象。 |
| **アクセント** | `#f39800` (温かみのあるオレンジ) | 循環の「矢印の先端」や「最重要ボタン」に少量使用。 |

---

## 2. スマホ画面での表示イメージ（ワイヤーフレーム）

スマホの画面を下にスクロールするだけで、循環のストーリーが頭に入る「縦スクロール連動型サイクル」です。

```text
+---------------------------------------------------+
|      【タイトル】世代を超えて寄り添う             |
|        川西を豊かにする「幸せの好循環」           |
+---------------------------------------------------+
|                                                   |
|  [STEP 1: アイコン] 子育て・現役世代の徹底支援    |
|  若い世代に選ばれる活気あるまちへ。               |
|                                                   |
+---------------------------------------------------+
|                        ↓                          |
|                  (若草色の矢印)                   |
+---------------------------------------------------+
|                                                   |
|  [STEP 2: アイコン] 空き家・人口減少への挑戦       |
|  地域の体力を維持し、将来の税収をしっかり確保。   |
|                                                   |
+---------------------------------------------------+
|                        ↓                          |
|                  (若草色の矢印)                   |
+---------------------------------------------------+
|                                                   |
|  [STEP 3: アイコン] 高齢者向け福祉サービスの充実   |
|  生まれた税収でお買い物や通院の足を豊かに。       |
|                                                   |
+---------------------------------------------------+
|                        │                          |
|                        └─ (再びSTEP 1へ繋がるループ)
+---------------------------------------------------+
```

---

## 3. 各ステップの構成詳細とアイコン・ビジュアル案

各ステップは、カード型（背景色：`#ffffff`、角丸、軽い影付き）で配置します。

### ■ STEP 1：子育て・現役世代の徹底支援（未来への投資）
*   **アイコンイメージ:** 「双葉」または「子どもと親が手を繋いでいるイラスト」
*   **アイコン作成用プロンプト案:**
    > *`Minimalist flat vector icon of a seedling with two leaves, cute hand-drawn style, line art, colored in soft green #9bca3e, white background, suitable for a mobile website.`*
*   **掲載テキスト:**
    > **「若い世代に選ばれるまちへ」**
    > 子どもたちへの投資や子育て支援（待機児童保育ステーションの充実など）を徹底して行い、川西を活気あるまちにアップデートします。

### ■ STEP 2：空き家・人口減少への挑戦（地域の体力維持）
*   **アイコンイメージ:** 「家と右肩上がりの矢印」または「街並みと太陽的イラスト」
*   **アイコン作成用プロンプト案:**
    > *`Minimalist flat vector icon of a cozy house with a small rising arrow, hand-drawn style, line art, colored in soft green #9bca3e and gray, white background, mobile UI icon.`*
*   **掲載テキスト:**
    > **「地域経済を回し、税収を確保する」**
    > 人口流入を促して空き家問題を解消へ。地域全体の経済を活性化し、次世代に過度な負担をかけない持続可能な税収基盤を築きます。

### ■ STEP 3：高齢者向け福祉・サービスの充実（暮らしの安心）
*   **アイコンイメージ:** 「シニアの笑顔（温かみのあるイラスト）」または「ハートを載せた小さなバス・タクシー」
*   **アイコン作成用プロンプト案:**
    > *`Minimalist flat vector icon of a cute small community bus with a heart on top, hand-drawn style, line art, colored in soft green #9bca3e, white background, mobile UI icon.`*
*   **掲載テキスト:**
    > **「生まれた予算をすべての世代の安心へ」**
    > 確保した税収を地域に分配し、高齢者の皆さまの医療・介護の充実、そして「100円お出かけ支援（乗り合いタクシー）」などの移動の足をしっかり守ります。

---

## 4. 実装用HTML/CSSテンプレートコード

このコードをホームページの該当箇所に挿入するだけで、若草色ベースの美しいスマホ対応3ステップカードが完成します。

### 【HTML】
```html
<section class="virtuous-cycle-section">
  <div class="cycle-container">
    <h2 class="cycle-title">世代を超えて寄り添い、みんなで豊かになる<br><span>「幸せの好循環」</span></h2>
    
    <!-- STEP 1 -->
    <div class="cycle-card">
      <div class="card-step">STEP 1</div>
      <div class="card-icon">🌱</div>
      <h3>子育て・現役世代の徹底支援</h3>
      <p>子どもたちへの投資や送迎支援を充実させ、若い世代に「選ばれる川西」をつくります。</p>
    </div>
    
    <div class="cycle-arrow">↓</div>
    
    <!-- STEP 2 -->
    <div class="cycle-card">
      <div class="card-step">STEP 2</div>
      <div class="card-icon">🏡</div>
      <h3>空き家・人口減少への挑戦</h3>
      <p>現役世代の流入を促すことで空き家を解消し、地域の体力を維持して持続可能な税収を確保します。</p>
    </div>
    
    <div class="cycle-arrow">↓</div>
    
    <!-- STEP 3 -->
    <div class="cycle-card">
      <div class="card-step">STEP 3</div>
      <div class="card-icon">👵👴</div>
      <h3>高齢者向け福祉のさらなる充実</h3>
      <p>生まれた財政的なゆとりを分配し、医療や介護、お買い物や通院を助ける「お出かけの足」をしっかりと守ります。</p>
    </div>
    
    <div class="loop-text">♻ 世代を超えて循環し続ける、持続可能なまちづくりへ</div>
  </div>
</section>
```

### 【CSS】
```css
/* セクション全体のスタイル */
.virtuous-cycle-section {
  background-color: #f4f9eb; /* 薄い緑 */
  padding: 40px 20px;
  font-family: sans-serif;
}
.cycle-container {
  max-width: 500px; /* スマホ向け幅 */
  margin: 0 auto;
  text-align: center;
}
.cycle-title {
  color: #2f5213; /* 深緑 */
  font-size: 1.4rem;
  margin-bottom: 30px;
  line-weight: bold;
}
.cycle-title span {
  color: #9bca3e; /* 若草色 */
}

/* カードのスタイル */
.cycle-card {
  background: #ffffff;
  border: 2px solid #9bca3e;
  border-radius: 12px;
  padding: 20px;
  margin: 10px 0;
  box-shadow: 0 4px 6px rgba(0,0,0,0.05);
  position: relative;
  text-align: left;
}
.card-step {
  position: absolute;
  top: -12px;
  left: 20px;
  background-color: #9bca3e;
  color: #ffffff;
  padding: 2px 10px;
  font-size: 0.8rem;
  font-weight: bold;
  border-radius: 20px;
}
.card-icon {
  font-size: 2rem;
  margin-bottom: 10px;
}
.cycle-card h3 {
  color: #2f5213;
  margin: 5px 0 10px 0;
  font-size: 1.1rem;
}
.cycle-card p {
  color: #555;
  font-size: 0.9rem;
  line-height: 1.5;
  margin: 0;
}

/* 矢印のスタイル */
.cycle-arrow {
  font-size: 1.8rem;
  color: #9bca3e;
  margin: 15px 0;
  font-weight: bold;
}
.loop-text {
  margin-top: 25px;
  font-size: 0.9rem;
  color: #2f5213;
  font-weight: bold;
}
```
