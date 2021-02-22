# Ruby rvm 常用指令


```ruby
$ ruby -v # 查看ruby 版本
$ rvm list known # 列出已知的 ruby 版本
$ rvm install 2.3.0 # 选择指定 ruby 版本进行更新
$ rvm get stable # 更新 rvm
$ rvm use 2.2.2 # 切换到指定 ruby 版本
$ rvm use 2.2.2 --default # 设置指定 ruby 版本为默认版本
$ rvm list # 查询已安装的 ruby 版本
$ rvm remove 1.9.2 # 卸载移除 指定 ruby 版本

$ curl -L https://get.rvm.io | bash -s stable # 安装 rvm 环境
$ curl -sSL https://get.rvm.io | bash -s stable --ruby # 默认安装 rvm 最新版本
$ curl -sSL https://get.rvm.io | bash -s stable --ruby=2.3.0 # 安装 rvm 指定版本
$ source ~/.rvm/scripts/rvm # 载入 rvm
```