# Git ワークフロー セキュリティ & 品質テンプレート

## 🛡️ プロジェクト概要

このテンプレートリポジトリは、以下に焦点を当てた堅牢なGitワークフロー設定を提供します：
- ハードコードされたシークレットの防止
- コミットメッセージ規約の強制
- リンティングとフォーマットによるコード品質の確保

## 🚀 主な機能

### 1. Gitleaks: シークレット検出
- ハードコードされたシークレット、APIキー、機密情報を自動スキャン
- 機密データの誤ったコミットを防止
- カスタマイズ可能な秘密情報検出ルール

### 2. Commitlint: 一貫したコミットメッセージ
- 従来型のコミットメッセージ形式を強制
- コードレビューと変更履歴生成の改善
- コミットメッセージ構造の標準化

### 3. Lint-staged: コード品質チェック
- ステージングされたファイルにリンターとフォーマッターを実行
- コミット前のコード一貫性を確保
- TypeScript、JavaScript、CSS、JSONをサポート

## 📦 前提条件

- Homebrew (macOS)
- Node.js と npm
- Git

## 🔧 インストール

1. リポジトリをクローン
```bash
git clone https://github.com/your-username/your-repo.git
cd your-repo
```

2. 依存関係をインストール
```bash
npm install
npx husky init
```

3. プレコミットフックを設定
```bash
npm run prepare
```

## 🛠️ 設定ファイル

- `.gitleaks.toml`: カスタムシークレット検出ルール
- `commitlint.config.js`: コミットメッセージ検証ルール
- `.eslintrc.js`: ESLintの設定
- `.prettierrc`: コードフォーマット設定
- `package.json`: Lint-stagedとスクリプト設定

## 💡 使用方法

### コードのコミット
- 従来型のコミットメッセージを使用：
  - `feat: 新機能の追加`
  - `fix: 認証のバグ修正`
  - `docs: READMEの更新`

### カスタマイズ
- `.gitleaks.toml`を変更してプロジェクト固有の秘密情報パターンを追加
- ESLintとPrettierの設定を必要に応じて調整

## 🚨 トラブルシューティング

- すべての前提条件がインストールされていることを確認
- フックの実行権限を確認
- Node.jsとnpmのバージョンを検証

## 📚 参考資料
- [Gitleaks GitHub](https://github.com/gitleaks/gitleaks)
- [Commitlintドキュメンテーション](https://commitlint.js.org/)
- [Lint-staged GitHub](https://github.com/lint-staged/lint-staged)

## 🤝 コントリビューション
1. リポジトリをフォーク
2. フィーチャーブランチを作成
3. 変更をコミット
4. ブランチにプッシュ
5. プルリクエストを作成

## 📝 ライセンス
-
