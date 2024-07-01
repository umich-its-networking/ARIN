# ARIN    
ARIN.net API scripts    
    
~~~
Production: reg.arin.net    
Test server: reg.ota.arin.net    
test info at: https://www.arin.net/reference/tools/testing/    

prod overview: https://www.arin.net/resources/manage/regrws/    
Quick start guide: https://www.arin.net/resources/manage/regrws/quickstart/    

Put URL and API key in a file to add to the environment:
export ARIN_API_PREFIX=https://reg.arin.net/rest
export ARIN_API_KEY=API-XXXX-YYYY-...

source ~/.ssh/arin.env

## 10.in-addr.arpa is not a real zone at ARIN, just an example
arin-get-ns 0.10.in-addr.arpa
dns1.example.com
dns2.example.com

arin-add-ns 0.10.in-addr.arpa dns3.example.com
dns1.example.com
dns2.example.com
dns3.example.com

arin-delete-ns 0.10.in-addr.arpa dns1.example.com
dns2.example.com
dns3.example.com

arin-set-ns 0.10.in-addr.arpa dns1.example.com dns2.example.com
============== desired:
dns1.example.com
dns2.example.com
============== existing:
dns2.example.com
dns3.example.com
============== adding:
adding dns1.example.com
dns2.example.com is already a nameserver
============== deleting:
dns2.example.com is still a nameserver
deleting dns3.example.com
============== new:
dns1.example.com
dns2.example.com
success
~~~
