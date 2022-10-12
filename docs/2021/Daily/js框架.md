# pure
auto emit event
	click, key, ...
sub event outside view
pure view: fn: state→view
impure view: mess view/state/event all together
pure aciton: fn: prevState→nextState
event: str: event→action
pure function that doesn't set external state

#
element:
	id, inner(text or child), outer, state, style, component
component:
	name, init(state), event, action(named event), sub(render),
	transformer
	init→state→render→transformer
	event→action→state→render→transformer
	state→render→transformer
# transformer
click
style
p: (v,e)=>e.style.padding = v + 'px'
# app
page state→ view state 
load code → render base → load data → render content
# style
size, margin, color, border
# expander
bcp → style: borderColor: $primary
n-1 → number: 1
still transformer

# 元素
原子 复合元素 关系
s steo s:teo name:ost
div`.ste.ost.steos id:123 width:12 