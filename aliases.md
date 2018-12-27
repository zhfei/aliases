##### 提高效率的 Mac命令别名
```
alias ll='ls -Alh'
alias snip='cd ~/Library/Developer/Xcode/UserData/CodeSnippets'
alias xcodeCC='cd ~/Library/Developer/Xcode/DerivedData'
alias showAll='defaults write com.apple.finder AppleShowAllFiles -bool true;KillAll Finder'
alias showPart='defaults write com.apple.finder AppleShowAllFiles -bool false;KillAll Finder'
#打印IP地址
alias ip='ifconfig en0'
#将OC源码编译成C、C++
alias cc='clang -rewrite-objc'
#将OC源码编译成C、C++
alias cc2='clang -x objective-c -rewrite-objc -isysroot /Applications/Xcode.app/Contents/Developer/Platforms/iPhoneSimulator.platform/Developer/SDKs/iPhoneSimulator.sdk'
```