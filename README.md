# 環境構築手順
## 前提項目
+ 最新版のVartualBoxのインストール  http://www.oracle.com/technetwork/server-storage/virtualbox/downloads/index.html?ssSourceSiteId=otnjp
+ 最新版のVagrantのインストール https://www.vagrantup.com/

## 以下のVagrantのエラーが発生するため
http://javabayashi.hatenablog.com/entry/2017/02/10/135852
以下のコマンドを実行する。
 + vagrant plugin install vagrant-vbguest
 + vagrant vbguest

## 手順
```
cd (任意のフォルダ)
git clone git@github.com:i-standard1/at-enginner_rails_server.git
vagrant up
vagrant ssh
```

+ mysql初期パスワード確認方法
  $ sudo cat /var/log/mysqld.log
   A temporary password is generated for root@localhost: (パスワード)

+ ansible実行コマンド(本番サーバーに反映する場合):
```
$ ansible-playbook site.yml -i production
```

# create_gaiki

デプロイコマンド
```
bundle exec cap production deploy:initial
```
