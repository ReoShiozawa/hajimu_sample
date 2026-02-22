# はじむ言語 サンプルコード集

> **はじむ言語**の学習と実践のための、全ファイル動作確認済みのサンプルコード集です。  
> 基本文法から Web 開発・ゲーム・Discord Bot まで、段階的に学習できます。

## 📋 必要環境

- [はじむ言語](https://github.com/ReoShiozawa/hajimu) がインストール済みであること

```bash
# 動作確認
hajimu --version
```

---

## 📁 ディレクトリ構成

```
jp-examples/
├── 00_シンプルサンプル/              ← まずここから！（10本）
├── 01_基本文法/                      ← 変数・演算・制御構文
├── 02_データ構造/                    ← 配列・辞書・内包表記
├── 03_関数とクラス/                  ← 関数・ラムダ・クラス・継承
├── 04_組み込み関数/                  ← 文字列・配列・数学関数
├── 05_実践的な例/                    ← ファイル・API・例外・電卓・ゲーム
├── 06_Web開発（hajimu_web）/         ← HTTP サーバー・REST API
├── 07_Discord_Bot（hajimu_discord）/ ← Discord Bot デモ
├── 08_GUI開発（hajimu_gui）/         ← GUI アプリデモ
├── 09_実用ツール/                    ← TODO管理・テキスト分析
├── 10_ゲーム開発/                    ← RPG・数当て・迷路・ブラックジャック
├── 11_データ処理/                    ← CSV/JSON 変換・API 連携
├── 12_セキュリティ/                  ← パスワード生成・在庫管理・バリデーション
└── 13_高度な例/                      ← REST API・高度なパターン
```

---

## 🚀 クイックスタート

```bash
# リポジトリをクローン
git clone https://github.com/ReoShiozawa/hajimu_sample.git
cd hajimu_sample

# 最初の1本を実行
hajimu 00_シンプルサンプル/01_hello.jp
```

---

## 📂 各ディレクトリの詳細

### 00_シンプルサンプル — まずここから

| ファイル | 内容 |
|---|---|
| `01_hello.jp` | Hello World |
| `02_variables.jp` | 変数と定数 |
| `03_conditions.jp` | 条件分岐 (if/else) |
| `04_loops.jp` | ループ (for/while) |
| `05_arrays.jp` | 配列の基本 |
| `06_functions.jp` | 関数の定義と呼び出し |
| `07_classes.jp` | クラスの基本 |
| `08_exception_handling.jp` | 例外処理 |
| `09_string_operations.jp` | 文字列操作 |
| `10_math_functions.jp` | 数学関数 |

### 01_基本文法

| ファイル | 内容 |
|---|---|
| `01_hello_world.jp` | 最小構成 |
| `02_variables_and_types.jp` | 変数・定数・型変換 |
| `03_arithmetic_operations.jp` | 算術演算・数学関数・素数判定 |
| `04_control_flow.jp` | if/elseif/else・for・while・break/continue |
| `05_string_basics.jp` | 文字列補間・分割・結合・置換 |

### 02_データ構造

| ファイル | 内容 |
|---|---|
| `01_array_basics.jp` | 配列の作成・アクセス・foreach |
| `02_array_operations.jp` | map/filter/reduce・スライス・重複除去 |
| `03_list_comprehension.jp` | リスト内包表記・範囲関数 |
| `04_dict_basics.jp` | 辞書の作成・更新・キー/値一覧 |
| `05_nested_structures.jp` | ネストした配列・辞書・行列 |

### 03_関数とクラス

| ファイル | 内容 |
|---|---|
| `01_function_definition.jp` | 関数定義・再帰・可変長引数・ラムダ |
| `02_function_advanced.jp` | クロージャ・パイプ演算子・デコレータ |
| `03_class_definition.jp` | クラス・初期化・メソッド・継承 |

### 04_組み込み関数

| ファイル | 内容 |
|---|---|
| `01_string_functions.jp` | 大文字/小文字・検索・置換・正規表現 |
| `02_array_functions.jp` | ソート・スライス・変換・集約・圧縮 |
| `03_math_functions.jp` | 絶対値・平方根・三角関数・素数判定・GCD |

### 05_実践的な例

| ファイル | 内容 |
|---|---|
| `01_file_operations.jp` | ファイル読み書き・追記・JSON保存 |
| `02_api_integration.jp` | HTTP GET・JSON 解析・URL エンコード |
| `03_exception_handling.jp` | try/catch/finally・リトライ処理 |
| `04_calculator.jp` | 四則演算・エラー処理 |
| `05_games.jp` | 数当てゲーム・じゃんけん |

### 06_Web開発（hajimu_web）

> **hajimu_web プラグインが必要です**
> ```bash
> hajimu パッケージ 追加 ReoShiozawa/hajimu_web
> hajimu パッケージ インストール
> ```

| ファイル | 内容 |
|---|---|
| `01_hello_server.jp` | 最小 HTTP サーバー (localhost:8080) |
| `02_json_api.jp` | JSON REST API サーバー (localhost:3000) |
| `03_async_patterns.jp` | 非同期/コールバック/パイプラインパターン |

### 07_Discord_Bot（hajimu_discord）

> **hajimu_discord プラグインと Discord Bot トークンが必要です**

| ファイル | 内容 |
|---|---|
| `01_hello_bot.jp` | トークンなしでも動くデモ + Discord 接続方法の説明 |

### 08_GUI開発（hajimu_gui）

> **hajimu_gui プラグインが必要です**
> ```bash
> hajimu パッケージ 追加 ReoShiozawa/hajimu_gui
> hajimu パッケージ インストール
> ```

| ファイル | 内容 |
|---|---|
| `01_hello_gui.jp` | GUI コンポーネントデモ（コンソールシミュレーター） |
| `02_calculator_gui.jp` | 電卓 GUI ロジック |

### 09_実用ツール

| ファイル | 内容 |
|---|---|
| `01_todo_manager.jp` | TODO リスト管理 (CLI) |
| `02_text_analyzer.jp` | テキスト統計分析 |

### 10_ゲーム開発

| ファイル | 内容 |
|---|---|
| `01_text_rpg.jp` | テキスト RPG バトル |
| `02_number_guessing.jp` | 数当てゲーム |
| `03_maze_game.jp` | 迷路探索 (スタック DFS) |
| `04_blackjack.jp` | ブラックジャック |

### 11_データ処理

| ファイル | 内容 |
|---|---|
| `01_csv_json_conversion.jp` | CSV/JSON 変換 |
| `02_advanced_api.jp` | API 連携・パイプライン処理 |

### 12_セキュリティ

| ファイル | 内容 |
|---|---|
| `01_password_generator.jp` | パスワード生成・強度判定 |
| `02_inventory_system.jp` | 在庫管理システム (クラス設計) |
| `03_validation.jp` | 入力バリデーション |

### 13_高度な例

| ファイル | 内容 |
|---|---|
| `01_rest_api_complete.jp` | REST API クライアント完全版 |
| `02_advanced_patterns.jp` | カリー化・Builder・メモ化・パイプ・デコレータ |

---

## 📚 推奨学習順序

```
Week 1: 00_シンプルサンプル → 01_基本文法 → 02_データ構造
Week 2: 03_関数とクラス → 04_組み込み関数
Week 3: 05_実践的な例 → 09_実用ツール → 10_ゲーム開発
Week 4: 06_Web開発 → 07_Discord_Bot → 08_GUI開発
```

---

## 🔗 公式リソース

- [公式ドキュメント](https://reoshiozawa.github.io/hajimu-document/)
- [リファレンスマニュアル](https://github.com/ReoShiozawa/hajimu/blob/main/docs/REFERENCE.md)
- [GitHub リポジトリ](https://github.com/ReoShiozawa/hajimu)

---

## 🐛 トラブルシューティング

| 症状 | 対処法 |
|---|---|
| `hajimu: command not found` | `which hajimu` でパスを確認 |
| パッケージエラー | `hajimu パッケージ 一覧` で確認後、`hajimu パッケージ インストール` |
| ポート競合 | コード内の `ウェブ.サーバー作成(8080)` の番号を変更 |

---

## 📄 ライセンス

MIT License

---

Happy Hajimu Programming! 🚀
