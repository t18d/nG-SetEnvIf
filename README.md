<div align="center">

# nG-SetEnvIf
[![](https://custom-icon-badges.demolab.com/badge/freenginx-1.29.2-009639?logo=freenginx&logoColor=white)](https://freenginx.org/en/)
![](https://img.shields.io/badge/Apache-2.4.65-D22128?logo=Apache&logoColor=white)
[![ReDoS detector](https://github.com/t18d/nG-SetEnvIf/actions/workflows/redos-detector.yml/badge.svg?branch=staging)](https://github.com/t18d/nG-SetEnvIf/actions/workflows/redos-detector.yml)
&nbsp;  
[![](https://custom-icon-badges.demolab.com/badge/Perishable%20Press-8G%20v1.5-dd6d0b.svg?logo=perishable-press)](https://perishablepress.com/8g-firewall/)
<p align="right"><em>a project of <a href="https://t18d.github.io/">Open Source by Tonkünstler-on-the-Bund</a></em></p>

&nbsp;  
&nbsp;  
&nbsp;  
nG-SetEnvIf is an [nG Firewall](https://perishablepress.com/ng-firewall/) fork that focusses on performance.

It can be used with both nginx and Apache httpd.

[Installation](#installation) •
[Configuration](#configuration) •
[Recipes](#recipes)

</div>

## Installation

### nginx

In `http` context, add

```Nginx
include /path/to/8g-firewall.conf;
```

In the relevant `server` context, add
```Nginx
include /path/to/8g.conf;
```

### Apache

In the relevant `<Directory>` section, add
```ApacheConf
Include /path/to/8G-SetEnvIf
```

## Configuration

### nginx

To enable logging, add `$ng_reason` to the relevant `log_format` directive.

For best performance, add to the main context

```Nginx
pcre_jit on;
```
and place the `include` directive before any `if`, `rewrite` or `set` within the same context.

### Apache

The eponymous module, mod_setenvif, is required, as is mod_authz_core. This is [more efficient](https://httpd.apache.org/docs/trunk/rewrite/avoid.html) than using mod_rewrite.

For best performance, `httpd.conf` [should be used](https://httpd.apache.org/docs/trunk/howto/htaccess.html#when) in preference to `.htaccess`.

> [!WARNING]
> Test with [Starr's logging suite](https://perishablepress.com/ng-firewall-logging/) and mod_rewrite before deploying in production.

## Recipes

If even nG-SetEnvIf fails to satisfy your passion for performance, read on.

- [Maxim Dounin’s Q&A](https://github.com/t18d/nG-SetEnvIf/wiki/Maxim-Dounin’s-Q&A) (nginx)
- [Replace mod_rewrite](https://github.com/t18d/nG-SetEnvIf/wiki/Recipes#disable-mod_rewrite-altogether) (Apache)
- [Calculate `pm.max_children`](https://devcenter.heroku.com/articles/php-concurrency#web_concurrency-defaults-by-dyno-type) (PHP)
- [OPcache tuning](https://tideways.com/profiler/blog/fine-tune-your-opcache-configuration-to-avoid-caching-suprises) (PHP)
- [Percona's environment for MySQL](https://www.percona.com/blog/innodb-performance-optimization-basics-updated/#:~:text=Operating%20system)
- [Post-quantum KEM](https://github.com/t18d/nG-SetEnvIf/wiki/Recipes#post-quantum-kem)
- [URL normalisation](https://github.com/t18d/nG-SetEnvIf/wiki/Recipes#url-normalisation)
- [Block AI crawlers](https://github.com/t18d/nG-SetEnvIf/wiki/Recipes#ai-crawlers)
- [Block spam emails](https://github.com/t18d/nG-SetEnvIf/wiki/Recipes#spam-emails)
- [Rate-limiting](https://github.com/t18d/nG-SetEnvIf/wiki/Recipes#rate-limit-404s) (WP)
- [Integration with Cloudflare](https://github.com/t18d/nG-SetEnvIf/wiki/Recipes#cloudflare)

&nbsp;  
<hr width="50%">

**Our Sponsor:**

<a href="https://tuta.com"><img src="https://github.com/t18d/nG-SetEnvIf/assets/130416721/8d560367-f84b-478b-a9c9-ef1c1dc6331c" width="200"></a>

