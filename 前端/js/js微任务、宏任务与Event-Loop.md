#### 微任务，宏任务以及event-loop

JavaScript是一个单线程的脚本语言，用回调函数的概念，引入了异步事件的概念。

###### 微任务 && 宏任务

当前执行栈（主线程）执行完毕时会立刻先处理所有微任务队列中的事件，然后再去宏任务队列中取出一个事件，同一次事件循环中，微任务永远在宏任务之前完成。如果在执行 microtask（微任务） 的过程中，又产生了microtask，那么会加入到队列的末尾，也会在这个周期被调用执行。

- 宏任务：setTimeout，setInterval，setImmediate，requestAnimationFrame
- 微任务：process.nextTick，MutationObserver，Promise.then catch finally

###### Event Loop是javascript的执行机制，称为事件轮询在微任务与宏任务之间轮询切换执行。

###### javascript 同步 && 异步 && 任务队列

- 同步任务：在主线程上排队执行的任务，只有前一个任务执行完毕，才能执行后一个任务。
- 异步任务：不进入主线程、而进入`任务队列`（Task Queue）的任务。
- 任务队列：是一个事件的队列（也可以理解成消息的队列），IO设备完成一项任务，就在"任务队列"中添加一个事件，表示相关的异步任务可以进入"执行栈"了。主线程读取"任务队列"，就是读取里面有哪些事件。











