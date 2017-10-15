# kennan
sasaki

## 参考

https://qiita.com/sayama0402/items/99bbf6d0977c5c6414cb

## githubと接続

* github側にこっちのpubkeyを登録してあげる
* `$ ssh -T git@github.com`で確認 
* 作業用ディレクトリ作成、`~/develop`に移動してから`$ git clone git@github.com:akiyoshi-sasaki/kennan.git`


## vagrant環境用意

vagrantとvirtualboxは公式サイトから入れる

```
$ vagrant init rails-dev-box
```

```
$ cd ~/Vagrant
$ git clone https://github.com/rails/rails-dev-box.git
$ cd rails-dev-box
$ vagrant up
```

#### ファイルの同期

ホスト側のVagrant.flieを更新、一行追加するだけ

```
[~/Vagrant/rails-dev-box] (master *)$ vi Vagrantfile

Vagrant.configure('2') do |config|

  ...

  + config.vm.synced_folder "/Users/akiyoshi/develop/kennan", "/home/ubuntu/kennan", owner: "ubuntu"

  ...

```

ホスト側の作業用ディレクリはこれ

```
[~/develop/kennan]
```

Vagrant.flieを更新したら常にreload必須



***
