# 更高效的移动
## 使用插件 vim-easymotion

默认的<leader>是反斜杠`\` 按起来不是很方便 故改键为 空格 `<Space>`

Start of word forwards : `<leader><leader>w`
start of word backwards : `<leader><leader>b`
end of word forwards : `<leader><leader>e`
end of word backwards : `<leader><leader>ge`

这一部分可以用前面单词的操作来理解

matches beginning & ending of word, camelCase,after _, and after # forwards : `<leader><leader>l`
matches beginning & ending of word, camelCase,after _, and after # backwards : `<leader><leader>h`
功能非常的强大 但是需要的快捷键太多了 实用性不佳

start of line forwards : `<leader><leader>j`
start of line backwards : `<leader><leader>k`
基于行跳转 很方便

jump to anywhere motion; default behavior matches beginning & ending og  word,camelCase, after _ and after # : `<leader><leader><leader>j`
太多键了 不常用吧

## 使用插件 vim-sneak
sneak基于两个字符的匹配来快速移动
语法 s+字符

本身s的位置很常用 所以把原本f的功能改成vim-sneak 并还原原本s的功能
在operator-pending模式下使用本来使用z匹配，现在改到f