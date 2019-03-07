# Задание №5
Написать регулярное выражение для выборки строк из ниже приведённого лога, содержащих следующие сигнатуры атак
(*or*,*1=1*,*script*,*select*,*union*,*alert*,*sleep*). Регулярное выражение должно выводить в групах **ТОЛЬКО** следующую информацию:

* IP (*66.249.65.159*)
* Время и дата (*06/Nov/2014:19:10:38 +0600*)
* Имя параметра (*kekpek*)
* Значения параметра (*53f8d72920ba2744fe873ebc*)

Пример лога:
```
66.249.65.159 - - [06/Nov/2014:19:10:38 +0600] "GET /?kekpek=53f8d72920ba2744fe873ebc HTTP/1.1" 404 177 "-" "Mozilla/5.0 (iPhone; CPU iPhone OS 6_0 like Mac OS X) AppleWebKit/536.26 (KHTML, like Gecko) Version/6.0 Mobile/10A5376e Safari/8536.25 (compatible; Googlebot/2.1; +http://www.google.com/bot.html)"
66.249.65.3 - - [06/Nov/2014:19:11:24 +0600] "GET /?q=%E0%A6%AB%E0%A6' or 1=1'%BE%E0%A7%9F%E0%A6%BE%E0%A6%B0 HTTP/1.1" 200 4223 "-" "Mozilla/5.0 (compatible; Googlebot/2.1; +http://www.google.com/bot.html)"
66.249.65.62 - - [06/Nov/2014:19:12:14 +0600] "GET /?q=%E0%A6%A6%E0%A7%8B%<script>alert(1)</script>E0%A7%9F%E0%A6%BE HTTP/1.1" 200 4356 "-" "Mozilla/5.0 (compatible; Googlebot/2.1; +http://www.google.com/bot.html)"
```