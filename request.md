request方法是一个有用的工具，能模拟浏览器，向目标地址传递数据。
以下均为python方法

url: https://docs.python-requests.org/en/master/index.html

# 请求方法
|方法|
|---------------------------|
|get(url, args)|
|head(url, params, args)|
|patch(url, data, args)|
|post(url, data, json,args)|
|put(url, data, args)|
|request(method, url, args)|


## post

requests.post(url, data={key: value}, json={key: value}, args)
