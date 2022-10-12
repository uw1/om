[Search · virtual machine](https://github.com/search?l=JavaScript&o=desc&p=3&q=virtual+machine&s=stars&type=Repositories)
	大部分是具体的实例，没有教程。
	[francisrstokes/16bitjs: 💻 A 16-bit virtual machine, including assembly language with 37 instructions, binary assembler, and a step through debugger](https://github.com/francisrstokes/16bitjs)
# js
[16-Bit VM in javascript – Francis Stokes](https://francisstokes.wordpress.com/2017/07/20/16-bit-vm-in-javascript/)
	instruction codes
[Make your own assembler simulator in JavaScript (Part 1)](https://www.mschweighauser.com/make-your-own-assembler-simulator-in-javascript-part1/)
[Higgs JavaScript Virtual Machine | Hacker News](https://news.ycombinator.com/item?id=8611492)
	peer review is quite broken and it is not quite clear how to fix it.
[Building an In-Browser JavaScript VM and Debugger Using Generators](https://amasad.me/js-debugger)
	call stack information in CPS is held in the lexical scope whereas in this method we need to take full control of the call stack.
[VM (executing JavaScript) | Node.js v15.14.0 Documentation](https://nodejs.org/api/vm.html)
```js
const context = { x: 2 };
vm.createContext(context); 
```
[CodeGuppy Playground](https://codeguppy.com/code.html?t=simple_vm)
```
var program = [11,0,10,42,6,255,30,0,11,0,0,11,1,1,11,3,1,60,1,10,2,0,20,2,1,60,2,10,0,1,10,1,2,11,2,1,20,3,2,31,2,30,2,41,3,2,19,31,0,50];
vm.load(program);
vm.run();
```
[ Building a Powerful Virtual Machine in JavaScript](https://morioh.com/p/6830a72aef28)
	更基础/详细