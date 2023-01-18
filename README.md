# hubitat_imageServer

This is a companion app for a few different camera integrations that I have written for Hubitat.  It is currently compatible with [hubitat_unifiProtect](https://community.hubitat.com/t/ubiquiti-unifi-protect-cameras/17624/37) and [hubitat_dahua](https://community.hubitat.com/t/dahua-and-amcrest-integration-for-cameras-and-doorbells/109047).
<br><br>
The app makes it possible to use and manipulate images saved using the `take` command with these integrations.  For example, it allows the saved images to be used on dashboard tiles and as Pushover notifications.


# Manual Installation instructions:

Installing with Hubitat Package Manager (HPM) is recommended.  Search for keyword "imageserver".

If you must install manually, follow these steps:

* In the *Apps Code* section of hubitat, create a new app and insert the *imageServerApp* code.

# Usage instructions:

**Install the app**
* In the *Apps* section of Hubitat, click *Add User App* to actually install the *Image Server* app.

**Create image URLs**

* In the section labeled **Select devices...for dashboards and webpages.**, select devices with the `image` attribute.
    * For cameras this is usually the only device.
    * For doorbells, this is usually the main device and usually isn't a "doorbell" or "button" device.
* Note the URLs to access images from specific cameras.
    * You can use these anywhere that is accessible from Hubitat on your local network, like a dashboard image tile, web browser, etc.
    * They will not render through cloud access due to Hubitat limitations.

**Configure Pushover notifications**

* In the section labeled **Select devices...for Pushover notifications.**, 
    * Enter your Pushover User Key and API Token
        * This information is found in the "Create an Application/API Token" section of the Pushover web portal.
    * Select devices with the `image` attribute.
        * For cameras this is usually the only device.
        * For doorbells, this is usually the main device and usually isn't a "doorbell" or "button" device.
* A Pushover notification with the image will be sent any time a new image is captured on any of the selected devices.

# Disclaimer

I have no affiliation with any of the companies mentioned in this readme or in the code.
