# aliases

**在Mac使用中，合理的设置命令别名可以提高开发效率
**

==在mac中设置命令别名的方法如下==

1.进入到当前用户主目录，创建并编辑文件.bash_profile。`~/.bash_profile`

2.在文件中添加命令,**注意：'='两边不要加空格**
```
#详细打印
alias ll='ls -Alh'
#代码片段目录
alias snip='cd ~/Library/Developer/Xcode/UserData/CodeSnippets'
#XCode代码缓存目录
alias xcodeCC='cd ~/Library/Developer/Xcode/DerivedData'
#显示隐藏文件
alias showAll='defaults write com.apple.finder AppleShowAllFiles -bool true;KillAll Finder'
#关闭隐藏文件
alias showPart='defaults write com.apple.finder AppleShowAllFiles -bool false;KillAll Finder'

```
3.编辑完成后，重启终端，或者执行命令`source ~/.bash_profile`

4.接着就可以正常使用了。若要查询可用的命令别名，可以用`alias`命令查询