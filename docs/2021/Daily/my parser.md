parser是一定要的，evaluator不一定，可以先用JS实现，用起来再说

# seon
sexp object notation
eval(obj)
# dynamic data
(if isLoading (div "loading") (h1 "abc"))

# pair
sPair "
dPair {} ()
# parser generator
[Tree-sitter: an incremental parsing system for programming tools | Hacker News](https://news.ycombinator.com/item?id=26225298)
	str → ast，还需要自己再把ast→data
	
# basic data
number string symbol
string with prefix
pre"str"→ (prefix "str")
preSTR → (prefix "STR")

# complex data
array with prefix

我需要一个统一的可复用的可定制的数据格式
to replace all the shitty data notation like HTML/CSS/JS/JSON/YAML/Markdown...
# special
break | col delimiter
escape
linebreak | row delimiter
# atom parser
# unified notation
instead of writing (+ "!" name) → (! name)
底层更简便&表层更简便

# udn
udn-core
udn-parse
udn-
