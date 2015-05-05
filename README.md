# Sketch Data Populator

## Installation
1. Download the ZIP file (or clone repository)
2. Move the file ```Sketch Data Populator.sketchplugin``` into your Sketch Plugins folder. In Sketch 3, choose **Plugins › Reveal Plugins Folder…** to open it.

## Testing & Credits

Please report bugs, observations and ideas as [issues](https://github.com/preciousforever/sketch-data-populator/issues). Also, please don't share the plugin at the moment. We're going to release it but we would like to adjust a few things first.

This is another collaboration between [Lukas Ondrej](https://github.com/lukas77me) from Brighton, United Kingdom and [precious design studio](http://precious-forever.com/) in Hamburg, Germany.

## How to use …
 
The **Sketch Data Populator** plugin replaces text and image placeholders with RealMockData™. 

Here's how it works:

1. Create a Layer Group that contains at least one Text Layer. In these Text Layers, use placeholders for you data fields in curly brackets – such as ```{first_name}``` or ```{last_name}```. Within a Text Layer, you can do arbitrary string concatenation such as ```{last_name}, {first_name}```. The plugin's "Populate with Data" command will replace all these placeholders with respective data.

2. In the same Layer Group, create a Rectangle Layer (this is your image placeholder). Give the Rectangle Layer a placeholder name in curly brackets – such as ```{avatar_image}```. The plugin's "Populate with Data" command will replace this placeholders with respective image data.

Check out the _demo.sketch_ and _demo-population.sketch_ files in the _demo_ folder to get an idea.

The data need to be stored in JSON files that can be loaded by the plugin from any folder on your computer. The data in JSON need to be in an array like in this example:

```[
  {
    "id": 1,
    "first_name": "Willie",
    "last_name": "Willis",
    "company_name": "Myworks",
    "job_title": "Marketing Assistant",
    "email": "wwillis0@cdc.gov",
    "phone": "9-(528)011-1428",
    "street_address": "99 Hallows Terrace",
    "city": "Outeiro",
    "country": "Portugal",
    "avatar_image": "assets/1.jpg"
  },
  {
    "id": 2,
    "first_name": "Melissa",
    "last_name": "Flores",
    "company_name": "Tagtune",
    "job_title": "Actuary",
    "email": "mflores1@jigsy.com",
    "phone": "4-(965)937-9250",
    "street_address": "46 Acker Trail",
    "city": "Santiago",
    "country": "Philippines",
    "avatar_image": "assets/2.jpg"
  },
  {
    "id": 3,
    "first_name": "Rachel",
    "last_name": "Hamilton",
    "company_name": "Riffwire",
    "job_title": "Librarian",
    "email": "rhamilton2@tamu.edu",
    "phone": "7-(881)710-0983",
    "street_address": "90833 5th Terrace",
    "city": "Semanding",
    "country": "Indonesia",
    "avatar_image": "assets/3.jpg"
  }, …
```
  
Note that the image files are referenced from a folder called _assets_. This means all your image data must be placed inside a folder that sits on the same level as your JSON file. The images folder as well as your images can be named anything you like, you just need to reference them accordingly within the JSON file.

The mock data in "demo" were created with https://www.mockaroo.com, which is a pretty powerful tool to generate all kinds of data. The "products" images are from apple.com, the "contacts" images are from https://randomuser.me/.