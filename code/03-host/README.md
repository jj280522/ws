# 架設網站

請用 00-mdServer 來測試您的架設是否成功！

## 架設在本機 localhost

如果你有對外 IP ，只要打入該 IP 就可以看到此網站。

## 用 ngrok 架設臨時測試用網站

* 適合測試時使用，或者你不想花錢時可以用這種模式 (但只能臨時用，不適合永久架站)
* [測試 webhook 不再煩惱：ngrok](https://blog.techbridge.cc/2018/05/24/ngrok/)
* [怎麼將內網的 localhost 讓外面的人都看得到呢？用用 ngrok 吧！](https://tenten.co/blog/how-to-use-ngrok-to-connect-your-localhost/)

老師的使用範例： 執行以下指令

```
ngrok http 3000 
```

完成後會出現下列畫面

```

ngrok by @inconshreveable                                                                                         (Ctrl+C to quit)
Session Status                online
Session Expires               7 hours, 58 minutes
Update                        update available (version 2.3.34, Ctrl-U to update)
Version                       2.2.8
Region                        United States (us)
Web Interface                 http://127.0.0.1:4040
Forwarding                    http://0156480c.ngrok.io -> localhost:3000
Forwarding                    https://0156480c.ngrok.io -> localhost:3000

Connections                   ttl     opn     rt1     rt5     p50     p90     
                              3       0       0.02    0.01    2.06    2.48    
```

然後檢視 http://0156480c.ngrok.io/README.md 就會看到你個網站呈現 README.md 的結果。

就算你用另一台電腦，或者是手機檢視，一樣可以正常運作！

## 架設無 node.js 程式的網站


測試： 使用 live-server 

```
PS D:\ccc\course\ws\code\03-host> live-server
Serving "D:\ccc\course\ws\code\03-host" at http://127.0.0.1:8080
Ready for changes
Change detected D:\ccc\course\ws\code\03-host\mdAjax\mdAjax.html
...
```

然後檢視：

http://127.0.0.1:8080/mdAjax/mdAjax.html#/README.md

上線： 使用 github pages (gh-pages)

