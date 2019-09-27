##### 提高效率的 Mac命令别名

```
#########################
#普通打印类型
#详细打印
alias ll='ls -Alh'
#打印当前目录下的目录结构
alias tree="find . -print | sed -e 's;[^/]*/;|____;g;s;____|; |;g'"
#########################
#########################
#常用目录类型
#代码片段目录
alias snip='cd ~/Library/Developer/Xcode/UserData/CodeSnippets'
#XCode代码缓存目录
alias xcodeCC='cd ~/Library/Developer/Xcode/DerivedData'
#########################
#########################
#网络配置类型
#打印IP地址
alias ip='ifconfig en0'
#########################
#########################
#显示/隐藏系统文件类型
#显示隐藏文件
alias showAll='defaults write com.apple.finder AppleShowAllFiles -bool true;KillAll Finder'
#关闭隐藏文件
alias showPart='defaults write com.apple.finder AppleShowAllFiles -bool false;KillAll Finder'
#########################
#########################
#XCode编译器类型
#将OC源码编译成C、C++
alias cc='clang -rewrite-objc'
#将OC源码编译成C、C++
alias cc2='clang -x objective-c -rewrite-objc -isysroot /Applications/Xcode.app/Contents/Developer/Platforms/iPhoneSimulator.platform/Developer/SDKs/iPhoneSimulator.sdk'
#########################
#########################
#压缩/解压缩类型
#-q:不显示进度；-r:当前目录下的目录递归压缩；-e:加密压缩；-m:压缩完删除原文件；-o:压缩后的文件修改时间改为当前压缩时间
#zip -q -r -e -m -o zipfileName.zip originalFileName
alias myzip='zip -q -r -o myZip.zip'
#-d:解压到新目录；-n:不覆盖已有文件
alias myunzip='unzip -d tmp -n'
#########################
#########################
#CocoPods类型
#pod update不更新索引源
alias podup='pod update --no-repo-update'
#########################
#########################
#统计类型
#grep "^-":文件类型；wc -l：前面输出的条目个数；ls -l：按照每个数据一行输出
alias lsfcount='ls -l|grep "^-"| wc -l'
#grep "^d":目录类型；wc -l：前面输出的条目个数；ls -l：按照每个数据一行输出
alias lsdcount='ls -l|grep "^d"| wc -l'
#########################
#########################
#唤出模拟器
#查看模拟器列表
alias simlist='xcrun simctl list'
#调出模拟器
alias simshow='/Applications/Xcode.app/Contents/Developer/Applications/Simulator.app/Contents/MacOS/Simulator -CurrentDeviceUDID'
#调出模拟器6s
alias simshow6s='/Applications/Xcode.app/Contents/Developer/Applications/Simulator.app/Contents/MacOS/Simulator -CurrentDeviceUDID 0EEEC72D-DEE8-42FE-8192-35772A3F7365'
#########################


#########################
#模版说明类型
#########################
```
可以将行框内的命令别名直接copy到文件`~/.bash_profile`内，
添加后执行生效命令`source ~/.bash_profile`