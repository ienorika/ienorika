# 家の理科(ienorika)

電気とお湯のコストを仕組みから解説する静的サイト。WordPressは使わず、HTMLファイルをそのまま配信する。

## 中身
| 場所 | 内容 |
|---|---|
| public/index.html | トップ |
| public/articles/ecocute-denkidai-takai/ | 1本目の記事「エコキュートの電気代が高い」+電気代の計算機 |
| public/tools/mitsumori-check/ | エコキュート交換の見積チェック(試作) |
| public/about/, public/privacy/ | 運営者情報・プライバシーポリシー(運営者名と連絡先は公開前に記入) |
| wrangler.jsonc | Cloudflareに「publicフォルダをそのまま配信する」と伝える設定 |

## 公開の手順(本人の作業)
1. ドメインを Cloudflare で取得(候補:ienorika.com)。
2. GitHub で新しいリポジトリ「ienorika」を作り、このフォルダの中身をアップロード。
3. Cloudflare の「Workers & Pages」→「作成」→「Gitリポジトリをインポート」で ienorika を選ぶ。ビルドコマンドは空欄、デプロイコマンドは `npx wrangler deploy`。
4. できたWorkerの「設定」→「ドメインとルート」で ienorika.com をつなぐ。
5. 「Web Analytics」でサイトを追加(Cookieを使わない計測)。計算機が使われると `?calc=1` `?check=1` のページとして数えられる想定(未確認、公開後に確かめる)。

## 決まり
- 2027年4月1日まで紹介リンク・広告は載せない。載せるときは「PR」「広告」を明記。
- 数字には出典と日付。自分の計算は式と前提を書く。
- 入力は送信しない。個人情報は受け取らない。

## 身元を守るための注意
- GitHubに上げる前に、コミットの作者名とメールアドレスを匿名にする(作者名は ienorika、メールはGitHubの「非公開用アドレス」)。本名が入ると公開される。
- 自宅の検針票を記事に使うときは、地域・契約番号・検針日を消す。
- ドメインの登録者情報が非公開になっているか、取得後に確かめる。
