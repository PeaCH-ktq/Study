Progate Pathは学校のメールアドレス `ac.jp`で登録すると全コンテンツ無料で使えます！  
[Progate公式サイト](https://app.path.progate.com/)  

環境構築タスク
Progate CLIのインストール
「ローカルで環境を構築」を選択

~~Progate Path公式サイトに沿ってインストールするとパス（環境変数）が上手く通らないことがあるので上手くいったときの方法をメモしておきます。~~ 恐らく僕のtypoで別のコマンドを実行していただけです。公式サイトの手順で正常に動くことのほうが多いと思われ。  
※パスの設定を間違えると標準コマンドがそのままでは動かなくなって復旧が面倒なので慎重に設定してください
```bash
#Progate CLI のインストール
#1. ターミナルを開き、以下のコマンドを実行しますの手順(Ubuntuで！)↓
bash <(curl -sSfL https://assets.path.progate.com/cli-installer/out/setup.sh)

exit

progate -v
ここで「progate: command not found」みたいなエラーが出た場合は下の手順を実行してください

sudo vim ~/.bash_profile #root(sudo)じゃなくても良いかも
#パスワード入力（Ubuntuの仕様で入力内容は表示されません）
i押して挿入モードへ
#↓追記 元から書いてあるコードは消さない
PATH="$PATH:$HOME/.progate/bin"

ESC押して挿入モードを終了
Shift+z２回で保存して終了
source ~/.bash_profile #反映

progate -v #インストールできているか確認
~~~ 公式サイトの手順に戻る ~~~
#5. progate コマンドでログインします
progate login
...
```
