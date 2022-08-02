# 第一个爬虫  
* 爬虫：通过编写程序来获取到互联网上的资源  
* 需求：用程序模拟浏览器，输入一个网站，从该网站获取到资源或内容  
```python
from urllib.request import urlopen

url = "http://www.baidu.com"
resp = urlopen(url)

with open("mybaidu.html",mode="w",encoding="utf-8") as f:
    f.write(resp.read().decode("utf-8"))#读取网页源代码
print("over!")
```
