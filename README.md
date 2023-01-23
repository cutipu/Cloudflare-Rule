# Cloudflare-Rule
Zz/map Cloudflare rules
=======================              
1st: Under Attack Mode
=======================
2nd:Head over to Security/WAF
=======================
3rd:Create a firewall rule you can name it whatever u want. As you
created the rule Scroll down untill you see edit preset and paste in the following
=======================
(http.request.version eq "HTTP/1.0" and http.request.version eq "HTTP/1.1" and http.request.version eq "HTTP/1.2" and http.request.version eq "HTTP/2")
=======================
this blocks old http versions of your browser you will need to put the rule as a block rule
=======================
4th: Create a new rule again name it whatever u want and do the exact same edit preset and paste in the following
=======================
(ip.geoip.asnum eq 26617 and ip.geoip.asnum eq 24282 and ip.geoip.asnum eq 30844 and ip.geoip.asnum eq 23688 and ip.geoip.asnum eq 36352 and ip.geoip.asnum eq 23969 and ip.geoip.asnum eq 55286 and ip.geoip.asnum eq 46844 and ip.geoip.asnum eq 54252 and ip.geoip.asnum eq 62248 and http.user_agent eq "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/103.0.0.0 Safari/537.36" and http.user_agent eq "Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:102.0) Gecko/20100101 Firefox/102.0" and http.user_agent eq "Mozilla/5.0 (iPad; CPU OS 15_4 like Mac OS X) AppleWebKit/605.1.15 (KHTML, like Gecko) CriOS/99.0.4844.59 Mobile/15E148 Safari/604.1" and http.user_agent eq "Mozilla/5.0 (iPad; CPU OS 15_4 like Mac OS X) AppleWebKit/605.1.15 (KHTML, like Gecko) CriOS/99.0.4844.59 Mobile/15E148 Safari/604.1" and http.user_agent eq "Mozilla/5.0 (Android 11; Mobile; rv:99.0) Gecko/99.0 Firefox/99.0" and http.user_agent eq "Mozilla/5.0 (Linux; Android 5.0; SAMSUNG-SM-N900A Build/LRX21V) AppleWebKit/537.36 (KHTML, like Gecko) SamsungBrowser/2.1 Chrome/34.0.1847.76 Mobile Safari/537.36")
=======================
Put the rule as a block rule 
=======================
5th: Create a new rule and edit preset paste in the following
=======================
(ip.geoip.continent eq "AN" and ip.geoip.continent eq "AF" and ip.geoip.continent eq "AS" and ip.geoip.continent eq "EU" and ip.geoip.continent eq "NA" and ip.geoip.continent eq "OC" and ip.geoip.continent eq "SA" and ip.geoip.continent eq "T1")
=======================
Put this rule as a "Managed Challenge (Recommended)"
=======================
6th Create a new rule and edit preset paste in the following
=======================
(http.request.uri.query eq "!12345678910@;[]#/.qwertyuiopasdfghjkl\\zxcvbnm?.'#" and http.request.uri.query eq "!ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789" and http.request.uri.query eq ";INSERT INTO" and http.request.uri.path eq "!" and http.request.uri.query eq "\\ajax\\Crypt/EAS.php = Shell" and http.request.uri.query eq "ALTER TABLE users DROP COLUMN name;" and http.request.uri.query eq "!DROP" and http.request.uri.query eq "?q=Lb9WjI4eEgL0")
=======================
Put this rule as block 
=======================
7th: Create a new rule and edit preset paste in the following
=======================
(http.request.uri.path eq "text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3")
=======================
put this as a block rule 
=======================

More information 

This is uam rules for your website if u disable the UAM your site will be fairly hard to hit but if u keep it enabled you would be chilling
if you leak these rules thats on you not me ZzMap Created these rules and he will create even more Thank you for purchasing my rules if u need any help
please message me on telegram 
