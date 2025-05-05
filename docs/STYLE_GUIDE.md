# STYLE_GUIDE

brain-vault のノート/記事を書くときのガイドライン（2025-05-05 時点）

## 1. Markdown 規約
- 見出しは `# H1` から。ファイル先頭はタイトルを H1 で始める
- 箇条書きは `-` を使用（一段階入れ子までは OK）
- コードは ```lang``` ブロック、数式は $...$ または $$...$$

## 2. タイトル命名
- 固有名詞はキャメルケースより半角スペース区切りを推奨
- 日付ID が必要なら `YYYYMMDD_タイトル.md`

## 3. タグ
- フロントマター `tags:` に複数指定可
- ステータス管理タグ例: `#draft #ready #published`

## 4. フロントマター
```yaml
---
title: "Yoneda Lemma"
tags: [math, category-theory]
status: draft
updated: 2025-05-05
---
```

## 5. 添付ファイル
- `_assets/` 配下に置き、ノートから相対パスでリンク
- 大容量 (>2MB) は Git LFS 管理

## 6. Pull Request
- Conventional Commits (`feat(math): add yoneda lemma note`)
- PR テンプレートに「背景・変更点・参考文献」を明記

Happy writing! 📝
