### 脚本的由来

随着项目的发展，目前我们项目已经有5个target了，一个主target，2个Today Widget的target，2个Apple Watch的target。这些target的版本号必须一模一样才能编译通过，也就是`Info.plist`中的`CFBundleShortVersionString`。每次版本迭代的时候都要手动一个一个改一点，实在太麻烦，而且对于一个程序员，怎么能忍这种很机械的操作！遂，鼓动个脚本一劳永逸~

### 脚本的使用

1. 在脚本中配置你工程的project的名字，还有各渠道的主target的`Bundle Id`。
2. 将脚本放在project所在的文件夹中。
3. 具体的使用：

```
使用说明：
       修改指定target组的版本号
          plist-version -i <index of bundleId array> -v <version num>
       修改全部target的版本号
          plist-version -a -v <version num>

参数说明： 
          -a               指定修改全部target的版本号
          -s               展示配置在脚本中的target
          -h               查看命令的使用
          -v               指定的版本号
          -i               指定build id对应的索引
```

*脚本的实现思路：<http://www.shinancao.cn/2017/07/16/Project-Design-4/>*
