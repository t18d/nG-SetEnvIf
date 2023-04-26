# nG-SetEnvIf
An [nG Firewall](https://perishablepress.com/ng-firewall/) fork that replicates its functionality in httpd using mod_setenvif and tracks the upstream release. The trade-off is between the efficiency gained over [mod_rewrite](https://httpd.apache.org/docs/2.4/rewrite/avoid.html) and having to [defer](https://www.webmasterworld.com/apache/4572958.htm) to any existing rewrite rules (eg for [permalink settings](https://glennmessersmith.com/pages/wphtaccess.html)).

\***

**Use case:** [httpd.conf](https://httpd.apache.org/docs/2.4/howto/htaccess.html#when)  
**Documentation:** See discussions in [Using mod_rewrite to control access](https://httpd.apache.org/docs/2.4/rewrite/access.html)  
**Upstream version:** [8G](https://perishablepress.com/8g-firewall/), courtesy of Jeff Starr  
**Desideratum:** Porting to Cloudflare's free-tier WAF
