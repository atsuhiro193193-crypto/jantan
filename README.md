# 雀鍛（じゃくたん）

勝つための麻雀トレーニングプラットフォーム

## 🎮 機能

- **何切るAI**: 麻雀の局面から最適な牌を切る判断をトレーニング
- **XPシステム**: 正解することでXPを獲得してレベルアップ
- **複数問題セット**: 初級から上級まで段階的に学習可能
- **AIによる解説**: なぜその牌を切るべきなのか、AIが詳しく解説

## 🚀 クイックスタート

### 必要な環境
- Node.js 18+
- npm または yarn

### インストール

```bash
git clone https://github.com/atsuhiro193193-crypto/jantan.git
cd jantan
npm install
```

### 開発サーバーの起動

```bash
npm run dev
```

ブラウザで `http://localhost:3000` を開いてください。

### 本番ビルド

```bash
npm run build
npm start
```

## 📁 プロジェクト構成

```
jantan/
├── README.md
├── package.json
├── package-lock.json
├── .gitignore
├── public/
│   └── index.html
├── src/
│   ├── index.js
│   ├── components/
│   │   ├── GameBoard.jsx
│   │   ├── TileSelector.jsx
│   │   ├── ResultDisplay.jsx
│   │   └── UserStats.jsx
│   ├── utils/
│   │   ├── tileConverter.js
│   │   ├── problemGenerator.js
│   │   └── aiEvaluator.js
│   ├── data/
│   │   └── problems.json
│   └── styles/
│       └── main.css
└── tests/
    ├── tileConverter.test.js
    ├── problemGenerator.test.js
    └── aiEvaluator.test.js
```

## 🛠️ 開発者向けコマンド

| コマンド | 説明 |
|---------|------|
| `npm run dev` | 開発サーバーを起動（ホットリロード有効） |
| `npm run build` | 本番ビルドを実行 |
| `npm start` | ビルド済みアプリを実行 |
| `npm test` | ユニットテストを実行 |
| `npm run lint` | ESLintでコード品質をチェック |
| `npm run format` | Prettierでコードをフォーマット |
| `npm run analyze` | バンドルサイズを分析 |

## 📊 機能詳細

### 何切るAI

局面に応じた最適な牌の切り方を学習します。

**使い方:**
1. 画面に13枚の手牌が表示されます
2. 「ツモ」で14枚になった状態です
3. 4つの選択肢から1つを選んでクリック
4. AIが正答と解説を表示します

### XPシステム

- 正解：**+50 XP**
- 不正解：**+10 XP**（学習ボーナス）
- レベルは100 XPで上昇

### 難易度レベル

| レベル | 説明 | 推奨XP |
|-------|------|--------|
| 初級 | 基本的な牌効率の学習 | 0-500 |
| 中級 | 複雑な局面判断 | 500-2000 |
| 上級 | リスク管理を含めた判断 | 2000+ |

## 🤖 AIエンジン

本アプリケーションは以下の麻雀AIアルゴリズムを採用：

- **牌効率評価**: 各牌の切り方による期待値計算
- **リスク評価**: 放銃率の低い切り方を優先
- **状況判断**: 現在の点数状況、他家の危険度を考慮

## 🔐 プライバシー

- ローカルストレージにのみデータを保存
- サーバーへの個人情報送信なし
- 完全にオフライン動作可能

## 🐛 バグ報告・機能リクエスト

[Issues](https://github.com/atsuhiro193193-crypto/jantan/issues) から報告してください。

## 📝 ライセンス

MIT License - 詳細は [LICENSE](./LICENSE) を参照

## 🙏 謝辞

麻雀AI開発の参考資料：
- 天鳳（Tenhou）の思考エンジン
- 雀魂（じゃんたま）の評価関数

## 📮 お問い合わせ

質問や提案は、GitHubの [Discussions](https://github.com/atsuhiro193193-crypto/jantan/discussions) にお願いします。
