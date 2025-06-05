# 处理包裹字符的符号

使用插件 **vim-surround**

change existing surround to desired -- `c s <existing> <desired>` 还挺好记的 c -> change s 插件名 将替换的字符 要替换成的字符

add desired surround around text defined bg -- `y s <motion> <desired>` y s 范围 要包围的字符

delete existing surround -- `d s <existing>` 删除包裹的字符

surround when in visual modes(surrounds full selection) -- `S <desired>` 在可视化模式中

```js
import { add } from './add'

const str = `my name is ${name}`
```