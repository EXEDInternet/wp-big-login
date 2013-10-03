wp-big-login
=============
The BIG register contains the official registration of healthcare professionals in The Netherlands, on behalf of the Ministry of Health, Welfare and Sport. More info about the BIG register can be found on the [official website](https://www.bigregister.nl/en/aboutthebigregister/). Technical information can be found at [this address](https://www.bigregister.nl/zoeken/zoeken_eigen_systeem/) - Dutch only.

= About this plugin =
The Big Login Plugin checks the number entered in the BIG register through a SOAP connection and sets a session variable if successful. This session variable can be used to limit access to certain pages to healthcare professionals.
The settings page provides an option to forward the user to another page after a successful login.

Requires WordPress 2.5 and PHP >= 5.1.0 with LibXML and SOAP enabled [see PHP.net](http://nl3.php.net/manual/en/book.soap.php).

Installation
=============

1. Upload the folder `big-login` to the `/wp-content/plugins/` directory  
2. Activate the plugin through the 'Plugins' menu in WordPress  
3. Set the url pointer in case of a successful login   
4. Place the widget on the page where you want to have it.  

Technical information
=====================
* This plugin uses PHP SOAP. SOAP requires LibXML as well.
* The session variable set after successful login is `$_SESSION['professional']`
* The plugin uses the option variable `big-login-url`
* The *RibizSearch class* does not make full use of the BIG register functionality, but only uses the functionality to check the validity of the provided BIG number
* The BIG number consists of 12 digits

