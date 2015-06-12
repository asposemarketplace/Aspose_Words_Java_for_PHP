# Aspose.Words Java for PHP

Aspose Words Java for PHP is a PHP project that demonstrates / provides the Aspose.Words for Java API usage examples in PHP by using PHP/JAVA Bridge.

You will need to configure PHP/Java Bridge before using any of the Aspose provided Java APIs in PHP e.g Aspose.Words, Aspose.Cells and Aspose.Slides etc.

## Installation and Configuration of PHP/JavaBridge
### Install Tomcat Server

To install tomcat server, issue following command on the linux console. This will successfully install tomcat server. 
```sh
$ sudo apt-get install tomcat8
```
### Download and Configure PHP/JavaBridge
In order to download the PHP/JavaBridge binaries, issue following command on the linux console. 
```sh
$ wget http://citylan.dl.sourceforge.net/project/php-java-bridge/Binary%20package/php-java-bridge_6.2.1/php-java-bridge_6.2.1_documentation.zip 
```
Unzip the PHP/JavaBridge binaries by issuing the following command on linux console. 
```sh
$ unzip -d php-java-bridge_6.2.1_documentation.zip 
```
This will extract JavaBridge.war file. Copy it to tomcat88 webapps folder by issuing the following command on Linux console. 
```sh
$ sudo cp JavaBridge.war /var/lib/tomcat8/webapps/JavaBridge.war
```
By copying, tomcat8 will automatically create a new folder "JavaBridge" in webapps. Once the folder is created, make sure your tomcat8 is running and then check http://localhost:8080/JavaBridge in browser, it should open a default page of JavaBridge. 

If any error message appears then install  FastCGI by issuing the following command on Linux console.
```sh
$ sudo apt-get install php55-cgi
``` 
After installing php5.5 cgi, restart tomcat8 server and check http://localhost:8080/JavaBridge again in the browser.

If JAVA_HOME error is displayed, then open /etc/default/tomcat8 file and uncomment the line that sets the JAVA_HOME. Check http://localhost:8080/JavaBridge in browser again, it should come with PHP/JavaBridge Examples page. 
###Example using Aspose.Words For Java in PHP/JavaBridge
First of all copy aspose-words-15.4.0-jdk16.jar file into /var/lib/tomcat/webapps/JavaBridge/WEB-INF/lib folder, then you can use below sample code. To download Aspose.Words for Java API to be used with these examples through PHP/Java Bridge Please navigate to:

http://www.aspose.com/community/files/72/java-components/aspose.words-for-java/
```php
require_once("java/Java.inc");
$filename = ''; // put filename with full path
$infoObj = new Java('com.aspose.words.FileFormatUtil');
$info = $infoObj->detectFileFormat($fileName);
$file_format = java_values($info->getLoadFormat());
```
In $file_format variable, you will have result of the file format.
