[[mac键盘输入]]

为什么在电脑上也需要使用语音输入，以及如何在MAC下实现高效地语音输入。

# audio
[terminal - Any way to change sound output device via Applescript or shell? - Ask Different](https://apple.stackexchange.com/questions/213011/any-way-to-change-sound-output-device-via-applescript-or-shell)

# 讯飞输入法
不支持Mac电脑。在windows下似乎也有识别慢的问题。

# 苹果自带输入法。
识别效果太垃圾。

# 搜狗输入法
识别效果不如讯飞。但是还可以接受。
打字时可以一直开着，不影响打字。
一段时间不说话还是会停止识别。并不能够一直打开。
随着近几年人工智能技术的进步，现在的识别效果已经不错。不再像是之前那样错字连篇。
会在按Esc键的时候。或者输入一段时间以后。退出语音输入。无法一直开着。

# 讯飞API
需要自己去申请语音识别服务。初始配置比较麻烦。

# 手机输入
识别效果最好。但是需要额外使用手机，使用起来比较麻烦。

# Google API
浏览器原生就支持, 可以直接调用。但识别效果不如讯飞。

# Windows
可以使用讯飞输入法。

# 开箱即用的
只能使用它提供的功能，没法自己做配置。甚至想改快捷键都改不了。

# 自己编程
现有的API使用起来并不是很方便，也没有好用的第三方库。需要自己花很多时间去写代码。
# xunfei
[语音听写_语音识别-讯飞开放平台](https://www.xfyun.cn/services/voicedictation)
	可以测试效果。整句效果很好。字词的效果一般。
[语音听写（流式版）WebAPI 文档 | 讯飞开放平台文档中心](https://www.xfyun.cn/doc/asr/voicedictation/API.html)
![[Pasted image 20220327025910.png]]

# python
[GitHub - Uberi/speech_recognition: Speech recognition module for Python, supporting several engines and APIs, online and offline.](https://github.com/Uberi/speech_recognition)
	有点麻烦。

# uTools
底层调用的是讯飞的API，但是识别效果没那么好
通过鼠标快捷键激发好处是用鼠标的时候方便，坏处是用键盘的时候不方便。
输入时需要一直按着鼠标快捷键。
使用的是Web API。识别的时间有一定的延迟。
可以通过karabiner设置成快捷键?
字词，需要等一秒钟，并不是很方便

# 语音输入法的问题。
没法完全替代键盘输入。在单质单词上。识别效果不足。自动的标点符号输入不准确。
只要能够准确识别就不得不使用。至少在输入录入的时候，否则就会非常影响输入。用键盘输入法得不偿失。