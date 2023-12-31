# nG-SetEnvIf
_a project of [Open Source by Tonkünstler-on-the-Bund](https://t18d.github.io/)_

&nbsp;  
&nbsp;  
nG-SetEnvIf was created as an [nG Firewall](https://perishablepress.com/ng-firewall/) fork that replicates its functionality in httpd using mod_setenvif and tracks upstream release. The trade-off is between the efficiency [gained](https://httpd.apache.org/docs/2.4/rewrite/avoid.html) over mod_rewrite and having to [defer](https://www.webmasterworld.com/apache/4572958.htm) to any existing rewrite rules (eg for [permalink](https://glennmessersmith.com/pages/wphtaccess.html) settings).

The focus being on performance, no logging facility is provided in addition to httpd's native logs. Backreference support has been removed to minimise memory footprint.

&nbsp;  
> [!NOTE]
> Use mod_rewrite for [testing](https://perishablepress.com/ng-firewall-logging/) before deploying nG-SetEnvIf.

&nbsp;  
**Use case:** [httpd.conf](https://httpd.apache.org/docs/2.4/howto/htaccess.html#when)  
**Requires:** mod_setenvif, mod_authz_core, mod_log_config   
**Documentation:** See discussions in [Using mod_rewrite to control access](https://httpd.apache.org/docs/2.4/rewrite/access.html)  
**Known issues & recipes:** See project [Wiki](https://github.com/t18d/nG-SetEnvIf/wiki/Known-Issues)  
**Upstream:** [8G v1.2](https://perishablepress.com/8g-firewall/), courtesy of Jeff Starr  
**Idea for fork:** Port these rules to Cloudflare's free-tier WAF

&nbsp;  
<hr width="50%">

**Our Sponsor:** &nbsp;&nbsp;&nbsp;&nbsp;<img src="https://github.com/t18d/nG-SetEnvIf/assets/130416721/574fa0d4-7f08-466d-a277-d3cd67e60ad1" width="200" />
