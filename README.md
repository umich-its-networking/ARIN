# ARIN    
ARIN.net API scripts    
    
~~~
Production: reg.arin.net    
Test server: reg.ota.arin.net    
test info at: https://www.arin.net/reference/tools/testing/    

prod overview: https://www.arin.net/resources/manage/regrws/    
Quick start guide: https://www.arin.net/resources/manage/regrws/quickstart/    

arin-get-ns 0.35.in-addr.arpa
dns1.itd.umich.edu
dns2.itd.umich.edu
dns3.umich.org



arin-add-ns 0.35.in-addr.arpa cffw1.dns.umich.com
dns1.itd.umich.edu
dns2.itd.umich.edu
dns3.umich.org
cffw1.dns.umich.com


arin-delete-ns 0.35.in-addr.arpa dns1.itd.umich.edu
cffw1.dns.umich.com
dns2.itd.umich.edu
dns3.umich.org


arin-set-ns 0.35.in-addr.arpa cffw1.dns.umich.com cffw2.dns.umich.net
============== desired:
cffw1.dns.umich.com
cffw2.dns.umich.net
============== existing:
cffw1.dns.umich.com
dns2.itd.umich.edu
dns3.umich.org
============== adding:
cffw1.dns.umich.com is already a nameserver
adding cffw2.dns.umich.net
============== deleting:
cffw1.dns.umich.com is still a nameserver
deleting dns2.itd.umich.edu
deleting dns3.umich.org
============== new:
cffw1.dns.umich.com
cffw2.dns.umich.net
success
~~~
