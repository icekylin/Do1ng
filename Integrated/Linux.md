- [正则表达式](#正则表达式)


## 正则表达式

从字符串中找出数字
```
# 实例
var str = "abc123def";
var patt1 = /[0-9]+/;
document.write(str.match(patt1))
# 结果
123
# Linux 中 awk 实例
echo "abc123def"|awk 
```