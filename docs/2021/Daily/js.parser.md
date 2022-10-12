[[parser]]
[[JS]]
[[js.evaluator]]
# object parser
specific to minimal object
combine other parser(array, string)

# string parser
handle escape
['unraw' a string in JavaScript - Stack Overflow](https://stackoverflow.com/questions/57330203/unraw-a-string-in-javascript)

# performance
[Benchmark: charCodeAt vs [] - MeasureThat.net](https://measurethat.net/Benchmarks/Show/6427/0/charcodeat-vs)
# eg
WASM [guybedford/es-module-lexer: Low-overhead lexer dedicated to ES module parsing for fast analysis](https://github.com/guybedford/es-module-lexer)
# regex based
[Chevrotain/chevrotain: Parser Building Toolkit for JavaScript](https://github.com/Chevrotain/chevrotain)
# generator
[lark-parser/Lark.js: Live port of Lark's standalone parser to Javascript](https://github.com/lark-parser/Lark.js)
	start: word+
	word: WORD ["," | "!"]
	%import common.WORD  
	%ignore " "    
# algorithm
[Devorein/fauton: An ecosystem of packages to work with automaton and parsers (dfa/nfa/e-nfa/regex/cfg/pda)](https://github.com/Devorein/fauton#algorithm-sources)
