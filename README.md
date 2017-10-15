# kennan
sasaki

## 参考

https://qiita.com/sayama0402/items/99bbf6d0977c5c6414cb

## githubと接続

* github側にこっちのpubkeyを登録してあげる
* `$ssh -T git@github.com`で確認 
* `git@github.com:akiyoshi-sasaki/kennan.git`


## vagrant環境用意

vagrantとvirtual box入れる

```
$ vagrant init rails-dev-box
```

```
$ git clone https://github.com/rails/rails-dev-box.git
$ cd rails-dev-box
$ vagrant up
```

#### ファイルの同期

ホスト側のVagrant.flieを更新

```
[~/develop/kennan] (setup *)$ vi Vagrantfile

Vagrant.configure('2') do |config|

  ...

  + config.vm.synced_folder "/Users/akiyoshi/develop/kennan", "/home/ubuntu/kennan", owner: "ubuntu"

  ...

```

ホスト側の作業用ディレクリはこれ

```
[~/develop/kennan]
```


***
