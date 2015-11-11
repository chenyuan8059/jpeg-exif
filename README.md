# jpeg-exif
Get exif infomation from jpeg format file.


```js
var exif = require("jpeg-exif");
var file = "~/Photo/IMG_0001.JPG";
exif.parse(file, function (err, data) {
    if (err) {
        console.log(err);
    } else {
        console.log(data);
    }
});

```

## Features

* Support More Than 450 Exif Tags
* Support GPSInfo Tags

## Installation

```bash
$ npm install jpeg-exif
```

## Callback Data Format

```js
{
    "Make": "Apple",
    "Model": "Apple",
    //...
    "SubExif": [
        "DateTimeOriginal": "2015:10:06 17:19:36",
        "CreateDate": "2015:10:06 17:19:36",
        //...
    ],
    "GPSInfo":[
        "GPSLatitudeRef": "N",
        "GPSLatitude": [ 35, 39, 40.08 ],
	    //...
    ]
}
```