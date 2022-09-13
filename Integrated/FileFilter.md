- [基础命令](#基础命令)
- [正则表达式](#正则表达式)
  - [取根域名-1](#取根域名-1)
- [文件批处理](#文件批处理)
  - [删除指定字符串](#删除指定字符串)
  - [替换指定字符串](#替换指定字符串)
  - [添加前缀](#添加前缀)
  - [添加后缀](#添加后缀)
  - [去重合并](#去重合并)

## 基础命令

- 设置系统时间 `tzselect`

## 正则表达式

### 取根域名-1

```
cat result.txt
  http://www.adomain.com/index.html
  http://www.bdomain.com/example.html
  http://www.cdomain.com/urls/123

awk -F '/' '{print $3}' result.txt > domain.txt
cat domain.txt
  www.adomain.com
  www.bdomain.com
  www.cdomain.com

awk -F 'www.' '{print $2}' domain.txt > rootdomain.txt
cat rootdomain.txt
  adomain.com
  bdomain.com
  cdomain.com
```

## 文件批处理

- 相关链接：
  - [rename命令详解](https://wangchujiang.com/linux-command/c/rename.html)
  - [Mac 批量重命名（增加前缀后缀）](https://blog.csdn.net/m0_46728513/article/details/114396779)

### 删除指定字符串

```bash
$ ls
  a_1.txt a_2.txt a_3.txt a_4.txt a_5.txt
$ rename -d a_ *.txt
$ ls
  1.txt 2.txt 3.txt 4.txt 5.txt
```

### 替换指定字符串

```bash
ls
  1.txt 2.txt 3.txt 4.txt 5.txt

rename 's/.txt/.log/' *
ls
  1.log 2.log 3.log 4.log 5.log
```

### 添加前缀

```bash
ls
  1.txt 2.txt 3.txt 4.txt 5.txt

for i in *.txt;do mv "$i" "username_${i%.txt}.txt" ;done
ls
  username_1.txt username_2.txt username_3.txt username_4.txt username_5.txt
```

### 添加后缀

```bash
ls
  1.txt 2.txt 3.txt 4.txt 5.txt

for i in *.txt;do mv "$i" "${i%.txt}_bak.txt" ;done
ls
  1_bak.txt 2_bak.txt 3_bak.txt 4_bak.txt 5_bak.txt
```

### 去重合并

```bash
ls
  1.txt 2.txt
cat 1.txt
  3
  2
  1
cat 2.txt
  2
  3
  4
cat *.txt|sort|uniq
  1
  2
  3
  4
```
