[[编程语言设计]]
# lua's semantics
# lisp's syntax (without nonsense parenthesis)
# no nonsense parenthesis
eg. in Clujure you have to write `console.log` as `(get console log)` or `(.log console)`
these kind of nonsense will never seen in LuaLis

[get - clojure.core | ClojureDocs - Community-Powered Clojure Documentation and Examples](https://clojuredocs.org/clojure.core/get)
[Janet Tables](https://janet-lang.org/docs/data_structures/tables.html)
[CLHS: Accessor GETHASH](http://clhs.lisp.se/Body/f_gethas.htm)

# minimal data types 
number: `123`
variable: `abc`, a string that can not be parsed as number.
string: `"abc"` or `'abc` when no spaces
function: `(fa a b (+ a b))` → `(a, b) => a+b`
seq: `[1 2 :a 3 :b 4]` → `{0: 1, 1: 2, a: 3, b:4}`
table: `{a 3 b 4}`
# function
`fn(a, b)` → `(fn a b)`
# sequence
in Lualis, array, object, string are all sequence, so they share the same syntax:
`arr[a][b]` → `(arr a b)`
`obj.a.b` → `(obj a b)`
`str[1]` → `(str 1)`
`str.slice(a,b)` → `(str a b)`
# table vs object
`this` is nonsense, table is a object without `this`
`{.a}` → `{a a}`
`{..a}` → `{...a}`
# defining variable
local: `(d a 1)`
global: `(d _g.a 1)`
parent: `(d _p.a 1)`
this: `_`
# every variable saves in a table

# alias
aliases store in a seperate object, so it's ok to write: `(alias a b b a)`
the same as `(d _a.a 'b _a.b 'a)`
# every api is a function, no nonsense opertators or keywords
if you think set is too long, you can just set it by `(set s set)`
# single control flow api (to beat them all)
# dynamic evaluation for different types
# why not AST
AST is more powerful but more verbose,
easier to read and learn

# no nonsense sponser, let's make money together
so that we don't have to sell our life to profit-orient companies
