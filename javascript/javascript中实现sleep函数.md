
```
function sleep(time) {
  var now = Date.now
  var before = now()
  while (now() - before < time) {}
}

console.log('Before: ' + (new Date()).toString())
sleep(3000)
console.log('after ' + (new Date()).toString())
```

# es7
```
async function run(time) {
  return new window.Promise(resolve => setTimeout(resolve, time))
}

async function sleep(time) {
  console.log('Before: ' + (new Date()).toString())
  await run(time)
  console.log('after ' + (new Date()).toString())
}

sleep(3000);
```

◆ 扩展阅读
* [javascript如何能简短优雅地实现sleep函数](https://www.zhihu.com/question/31636244)
* [What is the JavaScript version of sleep()?]()