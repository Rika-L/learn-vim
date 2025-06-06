# 如何删除一个函数

前置知识

% 匹配括号

```js
function add (a, b) {
  return a + b
}
```

插件: vim-indent-object

-> 基于缩进的操作


```js
function add (a, b) {
  return a + b
}
```

如果使用 `vai` 选择 会有一些问题 比如最后一个括号选择不上 但是 `vaI` 就没这个问题

该方案的问题是光标位置应该在函数内部 不然选择会有问题

# 删除函数

## 方案1
`dap` 基于段落 text-object
问题是无法处理以下函数
```js
function add(a, b) {
  console.log(a)

  return a + b
}
```
因为选择的是段落 console被截成一段,所以只会删掉一半

## 方案2
`daI` 基于vim-indent-object
缺陷: 光标需要在函数内部 而且 按 I 比较麻烦

优化:使用配置 ai 映射成 aI 反正 i 在我们js里用不太上

## 方案3
`V$%d` 原理 选择一整行 并移动光标至行尾 即 大括号处 使用 % 匹配括号 然后 d 删除
缺陷: 光标需在函数顶 参数缩进不对的话会有问题

优化 使用配置 `<leader> + d + f` 映射成 `V$%d` 
配置解读: leader delete function

总结 可以方案二三结合使用 在函数内部使用daI 在函数顶使用`<leader> d f`