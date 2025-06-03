---
title: Fixing macOS Dictation Without Reboot
date: 2017-07-08
categories: software
---
Often when I’m in the middle of a story, macOS’s built in dictation will stop working and I have to reboot the entire machine to fix it. Needless to say, this is incredibly frustrating. After some digging for the hundredth time, I stumbled across a solution.

In Terminal.app run the following command:

```
killall -9 DictationIM com.apple.SpeechRecognitionCore.speechrecognitiond com.apple.SpeechRecognitionCore.brokerd
```

This will restart the process that handles dictation and it should start working again when you use the keyboard shortcut. I use the default: Press Fn (Function) Key Twice.