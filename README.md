# nG-SetEnvIf
<p align="right"><em>a project of <a href="https://t18d.github.io/">Open Source by Tonkünstler-on-the-Bund</a></em></p>

&nbsp;  
&nbsp;  
&nbsp;  
nG-SetEnvIf was created as a fork of the [nG Firewall](https://perishablepress.com/ng-firewall/) that replicates its functionality in Apache httpd using `mod_setenvif` and tracks upstream release. The trade-off is between the [efficiency gained](https://httpd.apache.org/docs/2.4/rewrite/avoid.html) over `mod_rewrite` and [having to defer](https://www.webmasterworld.com/apache/4572958.htm) to any existing rewrite rules (_eg_ for [permalink settings](https://github.com/t18d/nG-SetEnvIf/wiki/Recipes#disable-mod_rewrite)).

The focus being on performance, no logging facility is provided in addition to httpd's native logs. Backreference support has been removed to minimise memory footprint.

&nbsp;  
> [!NOTE]
> httpd's default behaviour (_eg_ [MergeSlashes](https://httpd.apache.org/docs/2.4/mod/core.html#mergeslashes)) overrides certain rules.

> [!WARNING]
> [Test with mod_rewrite](https://perishablepress.com/ng-firewall-logging/) before deploying nG-SetEnvIf.

&nbsp;  
**Use case:** [httpd.conf](https://httpd.apache.org/docs/trunk/howto/htaccess.html#when)  
**Requires:** `mod_setenvif`, `mod_authz_core`, `mod_log_config`   
**Documentation:** [Apache Module mod_setenvif](https://httpd.apache.org/docs/trunk/mod/mod_setenvif.html) and the discussion [here](https://httpd.apache.org/docs/trunk/rewrite/access.html#blocking-of-robots)  
**Known issues & recipes:** See project [Wiki](https://github.com/t18d/nG-SetEnvIf/wiki/Known-Issues)  
**Upstream:** [8G v1.3](https://perishablepress.com/8g-firewall/), courtesy of Jeff Starr  
**Idea for fork:** Port these rules to Cloudflare's free-tier WAF

&nbsp;  
<hr width="50%">

**Our Sponsor:**

<img src="https://github.com/t18d/nG-SetEnvIf/assets/130416721/8d560367-f84b-478b-a9c9-ef1c1dc6331c" width="200" />

