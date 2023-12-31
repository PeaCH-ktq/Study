# WSLをインストールしよう
WSLの操作は基本的に「ターミナル」を使って行います。Windowsマークを右クリックすると出てくるメニューから開きましょう。  

## 1.WSLのバージョン確認
もしかすると何らかのタイミングでWSLがインストールされているかもしれないので以下のコマンドで確認します。（WSLにインストールされているディストリビューションとWSLバージョンを確認するコマンドです）  
```bash
wsl -l -v
```
↓このように表示されているなら既にインストールは完了しているのでこの章は飛ばしてください。  
```bash
  NAME                    STATE           VERSION
* Ubuntu                  Stopped         2
```
## 2.WSLバージョンを設定する  
WSL自体にWSL1とWSL2の2種類があります。デフォルトでWSL2が指定されているはずですが念のため設定しなおします。
```bash
wsl --set-default-version 2
```
## 3.WSLとディストリビューション(Linux系OS)のインストール
ここまで準備ができたら実際にWSLとディストリビューションをインストールしていきましょう。以下のコマンドでWSLとディストリビューションを同時にインストールできます。今回はUbuntuというディストリビューションをインストールします。
```bash
wsl --install -d Ubuntu
```
インストールが終わると初期設定が始まります。インストールしたディストリビューション用のユーザ名とパスワードを適当に入力してください。大抵のLinux系OSはパスワードの入力中に何も表示されませんが裏で処理は進んでいるので気にせず入力してEnterを押してください。  

## 参照  
[WSLの基本的なコマンド Microsoft](https://learn.microsoft.com/ja-jp/windows/wsl/basic-commands)
