# c# 中HttpClient访问Https网站

c# 中HttpClient访问Https网站，加入如下代码：

```
handler = new HttpClientHandler() ;
handler.AllowAutoRedirect = true;
handler.UseCookies = true;
handler.CookieContainer = cookies;
```

System.Net.ServicePointManager.SecurityProtocol = SecurityProtocolType.Tls12 | SecurityProtocolType.Tls11 | SecurityProtocolType.Tls;

或者：

```
handler.ClientCertificateOptions = ClientCertificateOption.Automatic;

httpClient = new HttpClient(handler);
```

转载于:https://www.cnblogs.com/94cool/p/10592262.html