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

arin-get-ns 0.35.in-addr.arpa
dns1.itd.umich.edu
dns2.itd.umich.edu

arin-add-ns 0.35.in-addr.arpa dns3.umich.org
dns1.itd.umich.edu
dns2.itd.umich.edu
dns3.umich.org

arin-delete-ns 0.35.in-addr.arpa dns1.itd.umich.edu
dns2.itd.umich.edu
dns3.umich.org

arin-set-ns 0.35.in-addr.arpa dns1.itd.umich.edu dns2.itd.umich.edu
============== desired:
dns1.itd.umich.edu
dns2.itd.umich.edu
============== existing:
dns2.itd.umich.edu
dns3.umich.org
============== adding:
adding dns1.itd.umich.edu
dns2.itd.umich.edu is already a nameserver
============== deleting:
dns2.itd.umich.edu is still a nameserver
deleting dns3.umich.org
============== new:
dns1.itd.umich.edu
dns2.itd.umich.edu
success
~~~
