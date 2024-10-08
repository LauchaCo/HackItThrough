## What is File Upload?
__File upload__ is an attack that can be carried out by uploading malicious files that can make a wide variety of things. Some attacks can make the file upload functionality an XSS or CSRF with PDFs, another attacks make the file upload function an OS Command execution entry point, etc.

## Types of attacks by filetypes
- PDF: CSRF, XSS
- ZIP: Zip Bomb, OS Command Execution via 

## Useful extensions to bypass blacklist
- **PHP**: .php, .php2, .php3, .php4, .php5, .php6, .php7, .phps, .phps, .pht, .phtm, .phtml, .pgif, .shtml, .htaccess, .phar, .inc, .hphp, .ctp, .module
	- **Working in PHPv8**: .php, .php4, .php5, .phtml, .module, .inc, .hphp, .ctp
- **ASP**: .asp, .aspx, .config, .ashx, .asmx, .aspq, .axd, .cshtm, .cshtml, .rem, .soap, .vbhtm, .vbhtml, .asa, .cer, .shtml
- **Jsp:** .jsp, .jspx, .jsw, .jsv, .jspf, .wss, .do, .action
- **Coldfusion:** .cfm, .cfml, .cfc, .dbm
- **Flash**: .swf
- **Perl**: .pl, .cgi
- **Erlang Yaws Web Server**: .yaws

## Bypass file extension checks
1. After checking for the previous extensions to discard a blacklist check you can try to test using some uppercase letters eg.: .pHp, .pHp5, .Phar
2. Check adding a valid extension before the actual extension eg.: file.png.php, file.png.Php5
3. Try adding special characters at the end. This can be done by bruteforcing with Burp. An example could be the following:
	1. file.php%20
	2. file.php%0a
	3. file.php%00
	4. file.php%0d%0a
	5. file.php/
	6. file.php.|
	7. file.
	8. file.php ...
	9. file.pHp5 ...
4. 