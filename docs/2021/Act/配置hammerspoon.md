代码复用不了，可以复用统一的配置文件
# modifier
[GitHub - jasonrudolph/ControlEscape.spoon: ⌨ Supercharge your Control key: Tap it for Escape. Hold it for Control.](https://github.com/jasonrudolph/ControlEscape.spoon)
[GitHub - jasonrudolph/keyboard: ⌨ Toward a more useful keyboard](https://github.com/jasonrudolph/keyboard)

# 功能丰富
[GitHub - KURANADO2/hammerspoon-kuranado: Hammerspoon 配置](https://github.com/KURANADO2/hammerspoon-kuranado)
[modules · sugood/hammerspoon - 码云 - 开源中国](https://gitee.com/sugood/hammerspoon/tree/master/modules)

# learn
[mac系统下有像windows下的autohotkey一樣的软件，几个热键就可以到某个网页吗？ @Coston](https://www.zhihu.com/question/22392769/answer/1767766592)

# mod modifier
劫持keydown
如果在keyup之前按下了其他的键。就发送mod+other
而如果没有 则是这发送key
when mod down
	set isDown.mod true
when mod up
	set isDown.mod false
when otherkey down & isDown.mod
args: key toMod toKey
state: isDown, toKeyMap
[ControlEscape.spoon/init.lua at main · jasonrudolph/ControlEscape.spoon · GitHub](https://github.com/jasonrudolph/ControlEscape.spoon/blob/main/init.lua)
