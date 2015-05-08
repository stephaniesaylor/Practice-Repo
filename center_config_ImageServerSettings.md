

##Image Servers
###Configure Image Server backend location and file type
This section explains how to change the location where images are stores and change the types of images that are accepted on the Listing Create/Edit Form.

Listings include several icons and screenshots as part of their metadata. Listing owners upload these images on the Listing Create/Edit Form. By default, the images are stored on the OZONE REST server backend file system, this setting is configured in the following file:
`\apache-tomcat-7.0.55\apache-tomcat-7.0.55\lib\MarketplaceConfig.groovy`
To change the location where images are stored, use the following property which is commented out by default in `MarketplaceConfig.groovy`:
`marketplace.imageStoragePath = "${System.properties['catalina.home']}/images"`


- This property should contain an absolute path to a directory where the images are stored.  
- The OZONE REST server must have read and write permissions in this directory, including the ability to create sub-directories.  
- To use a path relative to the running server's working directory, the appropriate system properties can be inserted into the path.  
For example: 
The default value of the `marketplace.imageStoragePath` property is `${System.properties['catalina.home']}/images`.  
For Tomcat servers, this will result in images being placed in an "images" directory within the main Tomcat directory.
*Note: To cluster, you must configure an external mechanism (like a shared network drive) to allow all servers in the cluster to use the image storage directory.*
###Purging the system of unnecessary images
When you create or edit a listing, the system uploads its images to the server in separate calls. If someone removes images from a listing or deletes a listing, the unused images will be deleted by a daily OZONE REST server job.  The job deletes unused images that are at least one day old.
###Acceptable types of images
To configure the types of images that the server accepts:

1. Open `\apache-tomcat-7.0.55\apache-tomcat-7.0.55\lib\MarketplaceConfig.groovy`
2. Use the `marketplace.acceptableImageTypes` configuration to add or delete file types.  The values must be strings that are used as the file extension for the stored image files. 
*Note: This option must be a map object where the keys are Internet Media Type strings that the server can accept. Internet Media Types that do not start with "image/" will be rejected regardless of this setting.*
3.	Save the file and restart `\apache-tomcat-7.0.55\apache-tomcat-7.0.55\bin\startup.bat` (or `startup.sh`)

As an example, the default value of marketplace.acceptableImageTypes is as follows:

    marketplace.acceptableImageTypes = [
    'image/png': 'png',
    'image/jpeg': 'jpg',
    'image/webp': 'webp',
    'image/svg+xml': 'svg'
    ]

 This configuration accepts PNG, JPEG, WebP and SVG images that will be saved with the file extensions .png, .jpg, .webp and .svg, respectfully.  