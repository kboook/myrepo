import requests
url = 'https://www.youtube.com/results?search_query=python'
r = requests.get(url)
r.encoding = 'utf8'
data = str(r.text).split('"')
data1 = []
data2 = {}
for k in data:
    if '게시자' in k:
        data1.append(k)
        
for k in data1:
    a = k[:k.rfind('게시자')-1]
    b = k[k.rfind('조회수')+4:-1]
    b = b.replace(',','')
    data2[a] = int(b)
