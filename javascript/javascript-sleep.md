
```
function sleep(time) {
  const now = Date.now
  const before = now()
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