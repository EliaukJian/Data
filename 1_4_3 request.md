# request 3
> 简单的反爬操作：通过打开自己的浏览器复制自己的正常访问的header和一些参数来伪装我们的代码请求
>
下面是一个简单的小案例：
```python
import requests

url = "https://movie.douban.com/j/chart/top_list"

#重新封装参数
param = {
    'type': '24',
    'interval_id': '100:90',
    'action': '',
    'start': '0',
    'limit': '20'
}
header = {
    "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/103.0.5060.114 Safari/537.36 Edg/103.0.1264.49"
}

resp = requests.get(url,params=param,headers=header)
print(resp.json())

resp.close() #关掉resp
```