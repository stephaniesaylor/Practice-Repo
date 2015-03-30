#Marketplace Configurations
##OzoneConfig.js
The `OzoneConfig.js` file contains parameters for adjusting specific parts of the application. This section explains how to make those changes.

## Network Changes
###Change the Public URI
You can make the store publicly accessible using the `marketplace.publicURI` configuration. The URI (uniform resource identifier) can be useful if the ozp-rest backend is behind a load balancer or reverse proxy, and the base URI as calculated by the ozp-rest backend itself is not correct. 

To change the Public URI:

1.	Open `\apache-tomcat-7.0.55\apache-tomcat-7.0.55\lib\MarketplaceConfig.groovy`
2.	Change the value for `marketplace.publicURI`. This value will be used as the base URI in the construction of all URIs within the resources representation returned by the server. If the value is null or not set, the automatically-calculated base URI for each request will be used.


