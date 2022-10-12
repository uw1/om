[[lia]]
思路被JS这种垃圾语言影响了
call: init scope
exec(scope)
atom function, list function

# HN
Lia.js is the JS implementation(interpreter) of Lia.
Lia is **not** yet another prgramming language, because other PL is fundamentally gabbage, they bund their syntax&semantics&APIs all together, and force you to use them.
Lia, on the other hand, separates the syntax&semantic&API, and has only one API that let you load other API, having the freedom to decide which API you use.
I'm the author, AMA.

# folder structure
parse.js
	parsers4char.js
eval.js
	evaluators4arr.js each fn seq
	evaluators4str.js : ,
readme.md

# eval fn
可提前返回，可暂停继续

# paresr generator
[Home - nearley.js - JS Parsing Toolkit](https://nearley.js.org/)
	比传统peg要好。

# parse
comment ;
linebreak \n
string ""
brackets ()[]{}
whitespace \s\t

# interpreter
变量 字符 函数 数组 数字
变量并不是数据类型，底层还是用字符表示
字符默认是变量，数组默认是函数

# api
number
string
array
function
logic
# evaluator
eval arr(s-exp)
eval str(token)
bind str
bind arr
env
	bind
# error message
env scope
fn name
native test api
# return

# 类型变量
值可以变，类型不能变