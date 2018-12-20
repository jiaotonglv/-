import urllib.request
import urllib.parse
    
def denglv():
    name={
        'username':'18351815556',
        'domain':'CMCC',
        'password':'MTk5ODA3',
        'enablemacauth':'0'
        }
    name=urllib.parse.urlencode(name).encode('utf-8')
    



    headers1={
       'Accept': 'application/json, text/javascript, */*; q=0.01',
	'Accept-Encoding': 'gzip, deflate',
	'Accept-Language': 'zh-CN',
	'Connection': 'Keep-Alive',
	'Host': 'a.nuist.edu.cn',
	'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; WOW64; Trident/7.0; rv:11.0) like Gecko Core/1.63.6788.400 QQBrowser/10.3.2767.400'
       }
    req=urllib.request.Request('http://a.nuist.edu.cn/index.php/index/login',data=name,headers=headers1)
    response=urllib.request.urlopen(req)
    html=response.read().decode('unicode-escape')
    print(html)

denglv()
        

