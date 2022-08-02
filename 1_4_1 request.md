# request 1
###### 安装requests  
> pip install requests  
>
使用request尝试简单发送请求
```python
import requests

query = input("输入你一个喜欢的明星：")

url = f'https://www.sogou.com/web?query={query}'

dic = {"User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/103.0.5060.114 Safari/537.36 Edg/103.0.1264.49"}

resp = requests.get(url,headers=dic)#处理一个小小的反爬

print(resp)
print(resp.text)#拿到页面源代码

resp.close()
```
