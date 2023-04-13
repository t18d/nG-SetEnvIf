# nG-SetEnvIf
This project maintains an [nG Firewall](https://perishablepress.com/ng-firewall/) fork which aims to replicate its functionality in httpd using mod_setenvif, and tracks the latest upstream release. The trade-off is between the efficiency gained over [mod_rewrite](https://httpd.apache.org/docs/2.4/rewrite/avoid.html) and having to [defer](https://www.webmasterworld.com/apache/4572958.htm) to any existing rewrite rules (eg for [permalink settings](https://glennmessersmith.com/pages/wphtaccess.html)).

\***

**Use case:** [httpd.conf](https://httpd.apache.org/docs/2.4/howto/htaccess.html)  
**Documentation:** See discussions in [Using mod_rewrite to control access](https://httpd.apache.org/docs/2.4/rewrite/access.html)  
**Stable upstream version:** [7G](https://perishablepress.com/7g-firewall/), courtesy of Jeff Starr
