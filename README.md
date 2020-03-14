# Maven-Issues

Problem faced 

1. sun.security.validator.ValidatorException: PKIX path building failed: sun.security.provider.certpath.SunCertPathBuilderException: unable to find valid 
	 certification path to requested target
   
   Repository URL
   https://https://repo.maven.apache.org/maven2/
   http://insecure.repo1.maven.org/maven2/
   
   Solution 1 
   
   a) disable SSL certificate checking
   
   -Dmaven.wagon.http.ssl.insecure=true -Dmaven.wagon.http.ssl.allowall=true -Dmaven.wagon.http.ssl.ignore.validity.dates=true
   
   Solution 2 
   
   a) created a truststore jks and pointed maven to this jks file
   
