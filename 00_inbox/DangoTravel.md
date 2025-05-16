
https://cloud.google.com/blog/topics/sustainability/new-geospatial-datasets-in-bigquery?hl=en

- google mapとの違い
- ベンチマークとなるアプリは？
	- alltrails
	- japan travel
	- platinum map
- ターゲットは？
	- 複数回来られる方
	- 欧米
	- 中華圏
- インプットはどうやって集める？
- 有名じゃないところをどう訴求する？
- 友達から案内してもらうようなUXにしたら？
- マネタイズ
	- すでに企業や自治体と契約したりしてる？



### 全体
- lambda-apiは今使ってないですか？
	- 使っていないファイルはすぐ消した方が、どんな参画者がきても迷わない
- 使ってないソースコードも結構残っちゃってますかね？？
- コメントの言語はできる限り統一したいです
	- 今は三言語ありそう？
- ER図とかありますか？
	- 結構テーブル多そうなのですが、この辺りの設計は問題ないですかね？データ周りは後から修正するの大変そうです〜
- コメントアウトがとにかく多くて読みにくいかもです…適切な量にしたいです
	- 基本はなくていいかも。説明ないと処理がわからないアルゴリズムだけつければ良い派です！
### Supabase
- Supabaseのキー直打ち込みはやめた方がいいですー
	- https://zenn.dev/koichi_51/articles/2cc5ea540254d1
- RLSは必須にした方がいいです！
	- https://zenn.dev/koichi_51/articles/2cc5ea540254d1
	- https://qiita.com/masakinihirota/items/011c9ee596f6e4bcc78a
### Flutter
- 不要なプラットフォームのディレクトリは削除したいです
	- linux, macos, windowsあたり？
- Riverpodはコード生成の使用を推奨されているのと、コード生成の方が楽なのでおすすめです〜
	- https://riverpod.dev/ja/docs/concepts/about_code_generation
- ライセンスページはあった方が無難です〜
	- https://zenn.dev/mukkun69n/articles/8f366cb6408b7e
- debugPrintはリリースモードでも出力されちゃうのでやめた方がいいです！
	- https://zenn.dev/fastriver/articles/flutter-debug-print
	- logging入れてるみたいなので、それを必ず使うようにしたい
- とにかくlintの警告はすぐ潰すようにした方がいいです〜
	- パフォーマンス悪くなったり、本当のエラーがわからなくなったりする為