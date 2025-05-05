# 🧠 brain‑vault

あなたの知識とアイデアを蓄えて育てる **Markdown & Obsidian ベース**のパーソナル・ナレッジ倉庫。

---

## 📌 このリポジトリで出来ること

| 機能       | ひと言                            | 備考                  |
| -------- | ------------------------------ | ------------------- |
| **書く**   | Obsidian で Markdown ノートをサクサク作成 | Inbox でまずは書き散らす     |
| **つなげる** | `[[内部リンク]]` + タグで知識をネットワーク化    | Graph View で俯瞰      |
| **育てる**  | MOC (Map Of Content) で体系化      | 小粒メモ → まとめ記事へ       |
| **共有する** | GitHub で履歴管理 & 公開              | Note / Zenn への転用も簡単 |

---

## 🗂 ディレクトリ構成

```text
brain-vault/
├── 00_inbox/            # 思いつきメモの一時置き場
├── _assets/             # 画像・PDF 等の添付ファイル
├── _templates/          # ノート雛形 (YAML front‑matter 付き)
├── knowledge/           # 純粋な“知識”メモ
│   ├── religion/
│   │   ├── MOC_religion.md
│   │   ├── buddhism.md
│   │   └── christianity.md
│   ├── math/
│   │   ├── category-theory/
│   │   │   └── yoneda-lemma.md
│   │   └── topology/
│   │       └── compactness.md
│   └── ...
├── ideas/               # ビジネス・技術アイデア
│   ├── business/
│   └── tech/
├── articles/            # 外部メディア向け原稿
│   ├── note/
│   └── zenn/
├── docs/                # 運用ルール・用語集など
├── .github/             # CI/CD, Issue/PR テンプレート
└── README.md            # ← いま見ているファイル
```

> **ポイント**
>
> * **Inbox → 分類** のループを回して知識をストック。
> * フォルダはあくまで“ゆるく”。横断は `[[リンク]]` とタグで。
> * 添付は `_assets/` に隔離 → Git LFS 推奨。

---

## 🚀 使いはじめガイド

1. **Obsidian をインストール**

   * [https://obsidian.md](https://obsidian.md) からダウンロード（無料）

2. **Vault を開く**

   * 起動 → “Open folder as vault” → `brain-vault` フォルダを指定

3. **必須コアプラグイン**

   * Daily Notes / Templates / Backlinks / Graph view などを有効化

4. **おすすめコミュニティプラグイン**

   | プラグイン            | 目的                      |
   | ---------------- | ----------------------- |
   | **Obsidian Git** | GitHub へ自動バックアップ        |
   | **Dataview**     | タグで一覧表・ダッシュボード生成        |
   | **QuickAdd**     | スラッシュコマンドでメモ作成を高速化      |
   | **Calendar**     | Daily Notes を月間カレンダーで閲覧 |

5. **テンプレを登録**

   * `_templates/note_template.md` を Templates プラグインのデフォルトに

6. **Inbox キャプチャを習慣化**

   * Daily Notes or QuickAdd で 00\_inbox にまず書く → 後から振り分け

---

## 🔄 GitHub 連携（Obsidian Git プラグイン）

1. GitHub で空のリポジトリ `brain-vault` を作成
2. ターミナルで

   ```bash
   cd path/to/brain-vault
   git init
   git remote add origin https://github.com/USER/brain-vault.git
   ```
3. Obsidian → Settings → **Community Plugins** → “Obsidian Git” をインストール & Enable
4. Settings → Obsidian Git

   * **Vault path** は自動入力
   * **Auto pull**: on startup
   * **Auto backup interval**: 10 min など
5. トークンを聞かれたら GitHub の **Personal Access Token** を発行して入力
6. 以降は自動でコミット / プッシュ。手動なら右上 Git アイコン → *Commit & push*

> **母ポイント👩‍🦰**
>
> * 「ノート = テキストファイル」なので、写真のアルバムを USB にコピーする感覚で GitHub にバックアップできる。
> * ボタン 1 つで“保存して雲に送る”と思えば OK。

---

## 🛠 CI/CD（任意）

* `.github/workflows/lint.yaml` → **Markdown lint** & **リンク切れチェック**
* `gh-pages` ブランチに自動デプロイ → **MkDocs** or **Docusaurus** でサイト化

---

## 🙌 コントリビュート

1. `issue` でトピックを提案
2. `git switch -c feat/<topic>` でブランチ作成
3. ノート追加・更新 → `git commit -m "feat: add <topic> note"`
4. PR → Review → Merge 🎉

### コミット規約

* Conventional Commits 準拠（例: `feat(math): add Yoneda lemma note`）

---

## 📜 ライセンス

このリポジトリのノート・記事は **CC BY‑4.0**、スクリプト類は **MIT** とします。

---

> Grow your brain, link your thoughts, and forge new ideas. Happy writing! 📝
