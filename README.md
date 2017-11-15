Magento 2<br />
v. 2.2.1<br />
This module fix the date format bug ( Invalid input datetime format of value ).<br />
When the format is Day, Month and Year. dd\mm\YY .<br />
<br />
Installing:<br />
<br />
Simply paste the FernandoFauth folder on (magento root)/app/code<br />
After installing the module upgrade your store.<br />
<br />
bin/magento setup:upgrade<br />
<br />
Check if your cache is clean.
<br />
Check if the Interface Locale is Português (Brasil) / português (Brasil) or other language that use the dd\mm\YY format
<br />
Certify if you using developer or production mode.<br />
<br />
If using production mode, you need recomplie the store code.<br />
<br />
Follow this steps
<br />
bin/magento setup:upgrade<br />
<br />
bin/magento indexer:reindex<br />
<br />
bin/magento deploy:mode:set production -s<br />
<br />
bin/magento setup:di:compile (Here was the secret, to run the di:compile after production)<br />
<br />
bin/magento setup:static-content:deploy (lang_code) [ ex: bin/magento setup:static-content:deploy pt_BR]<br />
<br />
Other thing you can do is check your folder permissions.