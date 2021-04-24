# Drupal-collectionspace

A Drupal plugin for CollectionSpace.

This plugin embeds a CollectionSpace collection browser into your Drupal site. To use this plugin, you must have a CollectionSpace 6.0 (or above) installation that has been configured to index records into an Elasticsearch cluster.

The min required version of drupal for this plugin to run is 8+.

## Installing the Plugin

To install the plugin, create a zip file containing this source code, and upload it to your Drupal server. Following are instructions to do this on a Mac OS or Linux system:

1.Download the plugin source code.

```bash
git clone https://github.com/collectionspace/drupal8-collectionspace.git
```
2. Create a zip file named cspace.zip.
```
zip -r cspace.zip drupal8-collectionspace/ -x '*.git*'
```
3. In the Drupal menu, click Extend, click the **Install new module**, then click the **Browse** button. Select the cspace.zip file that you just created.
4. When the plugin installation completes, click the "Enable newly added modules" Option.
5. Search For your module with the name of **Collection Space** in extensions list click the checkbox beside it and hit save.

## Configuring the Plugin

The following instructions describe how to configure the plugin using the Drupal admin area.

### Adding a CollectionSpace Browser
1. After successfully installing the Module you need to go to **Content** -> **Add Content** in drupal Admin Sidebar
2. You should see a content type **CollectionSpace Browsers** Click on it, if you dont see it you missed something follow the above steps.
3. You will need to add three values **Title** , **Script Location** and **config** all of these values are required
4. script location: The URL to the CollectionSpace browser JavaScript application. Your CollectionSpace administrator should be able to provide the correct value for your CollectionSpace installation.
```
https://unpkg.com/cspace-public-browser@1.1.0/dist/cspacePublicBrowser.min.js
```
5. config: Configuration settings for the CollectionSpace browser application, in JavaScript object notation (not restricted to JSON).
```
{
     "gatewayUrl": "https://core.dev.collectionspace.org/gateway/core"
}
```
6. Click Save and you should be redirected to a new page with the browser up and running.

