# vagrant-x11
vagrantでGUIつかいたひ。
GUI使わなくても、普通のVMのベースにしても便利。

## 説明
https://tbistr.github.io/posts/tech/vagrant_x11/ に書いてある。

## vscodeでアタッチしに行く。
`vagrant ssh-config >> C:\Users\[user_name]\.ssh\config`とかでssh_configファイルにカキコすると、vscodeのリモートから認証なしにアクセスできる。
