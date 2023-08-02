# Quick Overview of apache proxypass
---
## Terminologies:
- Reverse Proxy - enable requests that come from public internet to acces resource that reside on your private subnet (INBOUND - just like your BIGIP load balancer sitting in front of your web servers).
- Forward Proxy - enable users on a private subnet access the public internet (OUTBOUND).
---
## Requirements:
```
       <Location ~ "^((?!(/public|Shibboleth)).)*$">
          AuthType shibboleth
          ShibRequestSetting requireSession 1
          Require valid-user
          RequestHeader set "REMOTE_USER" "%{uid}e"
          ProxyPass http://tomcatapp:8080/
          ProxyPassReverse http://tomcatapp:8080/
       </Location>
```

---
