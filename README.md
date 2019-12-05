# htaccess

Block IPs with .htaccess
Order Deny,Allow
Deny from 192.168.1.56


RewriteEngine On

RewriteCond %{HTTP_HOST} ^wp\.sales.tmweb\.ru$ [NC]
RewriteCond %{REQUEST_URI} !^/wp.*$ [NC]
RewriteRule ^(.*)$ /wp/$1 [L,NS]

RewriteCond %{HTTP_HOST} ^hh\.sales.tmweb\.ru$ [NC]
RewriteCond %{REQUEST_URI} !^/hh.*$ [NC]
RewriteRule ^(.*)$ /hh/$1 [L,NS]

