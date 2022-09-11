
> 功能强大的子域收集工具 <https://github.com/shmilylty/OneForAll>

**下载安装**

```bash
git clone https://gitee.com/shmilylty/OneForAll.git
cd OneForAll/
python3 -m pip install -U pip setuptools wheel -i https://mirrors.aliyun.com/pypi/simple/
pip3 install -r requirements.txt -i https://mirrors.aliyun.com/pypi/simple/
# Linux创建软链接（可选）
echo 'alias oneforall="python3 [OneForAll路径]/oneforall.py"' >> ~/.zshrc
```

## 常用命令

python3 oneforall.py --target example.com run

python3 oneforall.py --targets ./example.txt run
