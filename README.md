# struts-mini
Security patch for struts 1.3.8

Struts 1 already stop official supporting for many years.
In these years, a few critical security vulnerabilities were found in struts 1.
This project is a security patch for struts 1.3.8, below security vulnerabilities are solved:

CVE-2016-1182
ActionServlet.java in Apache Struts 1 1.x through 1.3.10 does not properly restrict the Validator configuration, 
which allows remote attackers to conduct cross-site scripting (XSS) attacks or cause a denial of service via crafted input, 
a related issue to CVE-2015-0899.

CVE-2016-1181
ActionServlet.java in Apache Struts 1 1.x through 1.3.10 mishandles multithreaded access to an ActionForm instance, 
which allows remote attackers to execute arbitrary code or cause a denial of service (unexpected memory access) via a multipart request, 
a related issue to CVE-2015-0899.

CVE-2015-0899
The MultiPageValidator implementation in Apache Struts 1 1.1 through 1.3.10 allows remote attackers to bypass 
intended access restrictions via a modified page parameter.

CVE-2014-0114
Apache Commons BeanUtils, as distributed in lib/commons-beanutils-1.8.0.jar in Apache Struts 1.x through 1.3.10 and 
in other products requiring commons-beanutils through 1.9.2, does not suppress the class property, 
which allows remote attackers to "manipulate" the ClassLoader and execute arbitrary code via the class parameter, 
as demonstrated by the passing of this parameter to the getClass method of the ActionForm object in Struts 1.

https://www.cvedetails.com/vulnerability-list/vendor_id-45/product_id-6117/version_id-164423/Apache-Struts-1.3.8.html

Usage:
* struts-mini-1.3.8.jar depends on commons-beanutils-1.9.3.jar.
  upgrade commons-beanutils-1.8.0.jar to commons-beanutils-1.9.3.jar
* remove below 5 jar files from class path:
  struts-core-1.3.8.jar
  struts-el-1.3.8.jar
  struts-extras-1.3.8.jar
  struts-taglib-1.3.8.jar
  struts-tiles-1.3.8.jar
* drop struts-mini-1.3.8.jar in class path.

