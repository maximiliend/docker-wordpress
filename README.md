# Wordpress

A enhanced docker image of WordPress with PHP7 & Security Tools. Based on Official Docker WordPress.

### Wordpress Version

4.4.2

### Advice

The official wordpress Image use a volume for /var/www/html.

We recommend you to use volume for wordpress but only for /var/www/html/wp-content. So you only keep uploaded files, themes and plugins. You are not supposed to change the wordpress core.
Simply choose what you want to do by using -v option.
```
docker run [...] -v /path/to/wp-content:/var/www/html/wp-content [...]
```

For security reason the default wordpress login /wp-login.php is hidden from bots.
> Use http://my-awesome-website/wp-admin-panel/ to access to your login panel

### Security

Embedded security systems in this version provide differents features :
* Block malicious bots
* Reduce comment spam
* Protect sensitive files and pages
* Reduce possible hacks & SQL injections by preventing some insertions in url.
* Hide your admin panel login from bots.

### Why use this version and not the official?

* The official don't use PHP7
* The official don't embeds security tips by default
