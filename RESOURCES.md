# はじむ言語リソースブックマーク

## 🔗 公式リポジトリ

### コア言語
- **はじむ言語本体**: https://github.com/ReoShiozawa/hajimu
  - 主要な日本語プログラミング言語インタプリタ
  - C99/C11で実装
  - 143個の組み込み関数

### 関連フレームワーク
- **hajimu_web**: https://github.com/ReoShiozawa/hajimu_web
  - ExpressやFlask相当のWebフレームワーク
  - 252個のAPI関数
  - セッション管理、テンプレート、gzip圧縮対応

- **hajimu_discord**: https://github.com/ReoShiozawa/hajimu_discord
  - Discord API完全日本語ラッパー
  - 252個のAPI関数
  -音声サポート、スラッシュコマンド対応

- **hajimu_gui**: https://github.com/ReoShiozawa/hajimu_gui
  - 完全な日本語ファーストなGUIフレームワーク
  - 1,101個の関数
  - クロスプラットフォーム（macOS/Linux/Windows）

- **hajimu-document**: https://github.com/ReoShiozawa/hajimu-document
  - 公式ドキュメント
  - 詳細なAPI仕様

### その他プロジェクト
- **hajimudiscordmusic**: https://github.com/ReoShiozawa/hajimudiscordmusic
  - Discord音楽ボットサンプル
  - YouTube integration

---

## 📚 学習リソース

### インストール方法

```bash
# macOS/Linux (Homebrew)
brew install hajimu

# ソースからのビルド
git clone https://github.com/ReoShiozawa/hajimu.git
cd hajimu
make
make install
```

### コマンドリファレンス

```bash
# プログラム実行
hajimu script.jp

# パッケージ管理
hajimu パッケージ 一覧          # インストール済みパッケージ表示
hajimu パッケージ 追加 [名前]    # パッケージ追加
hajimu パッケージ インストール   # 依存関係インストール
hajimu パッケージ 削除 [名前]    # パッケージ削除

# REPL
hajimu  # 対話型シェル
```

---

## 🎯 キーワード一覧

### 制御フロー
| 日本語 | 説明 |
|-------|------|
| もし...なら...終わり | if文 |
| それ以外...終わり | else文 |
| 繰り返す...終わり | for文 |
| の間...終わり | while文 |
| 抜ける | break |
| 続ける | continue |

### データ型と操作
| 日本語 | 説明 |
|-------|------|
| 変数 | 変数宣言 |
| 関数 | 関数定義 |
| クラス | クラス定義 |
| 新しい | インスタンス化 |
| 初期化 | コンストラクタ |
| 戻す | return |

### よく使う関数
| 日本語 | 説明 |
|-------|------|
| 表示 | 標準出力 |
| 長さ | 文字列/配列長 |
| 分割 | 文字列分割 |
| 追加 | 要素追加 |
| 削除 | 要素削除 |

---

## 💡 トラブルシューティング

### `hajimu: command not found`
```bash
# パスの確認
which hajimu
# /usr/local/bin/hajimu が表示されるはず

# 直接実行
/usr/local/bin/hajimu script.jp
```

### パッケージインストールエラー
```bash
# キャッシュクリア
rm -rf ~/.hajimu/cache

# パッケージリスト再生成
hajimu パッケージ インストール

# デバッグモードで実行
HAJIMU_DEBUG=1 hajimu パッケージ 追加 [パッケージ名]
```

### ポート競合エラー
```
"Address already in use" が出た場合、別のポートを使用してください:
ウェブ.サーバー作成(9000)  # 8080から9000に変更
```

### モジュールが見つからないエラー
```bash
# インストール確認
hajimu パッケージ 一覧

# パッケージの再インストール
hajimu パッケージ 削除 [パッケージ名]
hajimu パッケージ 追加 [パッケージ名]
hajimu パッケージ インストール
```

---

## 🔐 セキュリティのベストプラクティス

### パスワード管理
```hajimu
# 安全なパスワード生成
関数 安全なパスワード():
    # 最小16文字で大文字・小文字・数字・特殊文字を含む
    戻す パスワード生成(16, ["小文字", "大文字", "数字", "特殊文字"])
終わり
```

### 入力検証
```hajimu
# メール検証の例
もし メール検証(ユーザーメール) なら
    # 処理を続行
終わり
```

### API呼び出しのセキュリティ
```hajimu
# トークン管理
変数 API_TOKEN = 環境変数("API_TOKEN")
# 環境変数から読み込む、コードへの埋め込みは避ける
```

---

## 🚀 本番環境デプロイ

### Docker 構成例
```dockerfile
FROM ubuntu:20.04

RUN apt-get update && apt-get install -y \
    build-essential \
    curl

RUN curl https://raw.githubusercontent.com/ReoShiozawa/hajimu/main/install.sh | bash

WORKDIR /app
COPY . .

CMD ["hajimu", "main.jp"]
```

### systemd サービス例
```ini
[Unit]
Description=Hajimu Web Application
After=network.target

[Service]
Type=simple
User=app
WorkingDirectory=/opt/app
ExecStart=/usr/local/bin/hajimu main.jp
Restart=on-failure
RestartSec=10s

[Install]
WantedBy=multi-user.target
```

---

## 📊 パフォーマンス最適化

### メモリ効率
- 大規模配列は配列内包表記より手動ループを検討
- 不要な中間配列の生成を避ける

### 実行速度
- 計算集約的な処理はC拡張プラグインで実装
- 頻繁に呼ぶ関数は事前定義

### I/O最適化
- バッチ処理で複数のファイル操作を集約
- キャッシング機構を活用

---

## 🔗 コミュニティリンク

### GitHub
- Issues・Discussions: バグ報告・質問用
- Pull Requests: コントリビューション受付

### SNS
- (@ReoShiozawa) - メイン開発者

### 関連プロジェクト
- はじむで書かれたクリプロジェクト: https://github.com/ReoShiozawa/hajimu

---

## 📝 useful Commands

### デバッグ
```bash
# エラーの詳細表示
hajimu --debug script.jp

# 構文チェック
hajimu --check script.jp

# パフォーマンスプロファイリング
hajimu --profile script.jp
```

### ファイル操作
```bash
# ディレクトリ内のすべてのファイルを実行
for f in *.jp; do hajimu "$f"; done

# 複数ファイルから一つを実行
hajimu -f filelist.txt main.jp
```

---

**最終更新**: 2026年2月22日  
**バージョン**: 1.0.0
