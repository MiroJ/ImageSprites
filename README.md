# Image Sprites
An image sprite is a collection of images stored in a single image. A web page with many images can take a long time to load and generates multiple server requests. Using image sprites will reduce the file size and the number of server requests, thus save bandwidth.

## Features
- Easy to create and update image sprites
- Support for png, jpg, and bmp images
- Configurable vertical or horizontal sprite layouts
- Produce LESS, Sass or CSS file with sprite image locations
- Configurable settings for each sprite file

## Creating Image Sprites

The extension allows several ways to create a sprite image:

### 1. Sprite all images in a folder

Right click on a folder containing images and select *Create Image Sprite*

![Sprite All Image in a Folder](https://github.com/gurayyarar/ImageSprites/raw/master/images/docs/folder-sprite.gif)

### 2. Sprite only selected images

Select the images, right click and select *Create Image Sprite*

![Sprite Only Selected Images](https://github.com/gurayyarar/ImageSprites/raw/master/images/docs/files-sprite.gif)

These two ways will generate a `.sprite` settings file as well as the resulting `image file` and a `.css` file as a default.

![Sprite Result](https://github.com/gurayyarar/ImageSprites/raw/master/images/docs/display-sprite.jpg)


## Configuration File (.sprite)

The configuration file contains settings for the specific image sprite. It uses a standard JSON format with `.sprite` extension and can be modified using VS Code or any text editor. The file is stored in the `output` folder selected during the creation process.

*Example:*
```
{
   "style_name": "images",
   "images": [
      "..\\images\\access_exports.png",
      "..\\images\\access_imports.png",
      "..\\images\\accordion.png",
      "..\\images\\account_balances.png",
      "..\\images\\account_functions.png"
   ],
   "orientation": "vertical",
   "padding": 5,
   "custom_styles": {
      "display": "inline-block"
   },
   "stylesheet": "css",
   "path_prefix": "",
   "output": "png",
   "enable_cache_busting": true,
   "output_image_file": "..\\images\\sprites\\avatar.sprite.png",
}
```

### Configuration Options

The following are options and their default values, configurable via the `.sprite` file.

|Key|Description|Value Type|Values|Default|
|---|-----------|----------|------|-------|
|style_name|Class name `.style_name { /* css codes */ }`|string| | |
|images|An array of relative file paths to the image files|string[]|||
|folder|Relative folder path contains sprited images|string|||
|orientation|The layout of sprited image|string|`vertical` `horizontal`|`vertical`|
|padding|Distance of whitespace inserted around each individual image in the sprite. The value is in pixels.|number||5
|custom_styles|Allows you to inject any css declarations into the generated stylesheets.|object||`{ "display": "inline-block" }`|
|stylesheet|Outputs LESS, Sass or plain CSS files|string|`css` `scss` `less`|`css`|
|path_prefix|Adds a prefix string to the image path in the url(path) value in the stylesheet.|string|||
|output|Sprite image file format|string|`png` `jpg` `bmp`|`png`|
|output_image_file|Relative file path to the sprite image output file|string||
|enable_cache_busting|Enable/Disable cache busting|boolean|`true` `false`|`true`


## Updating Image Sprite

You can update an already-created sprite by:

- Right click on a `.sprite` file and select `Update Image Sprite` or
- Right click on editor when a `.sprite` file opened and select `Update Image Sprite`.

![Update Image Sprite](https://github.com/gurayyarar/ImageSprites/raw/master/images/docs/update-sprite.gif)

## License

**Image Sprites** is an open source project that is licensed under the [MIT license](http://opensource.org/licenses/MIT).


## Donations

Donations are **greatly appreciated!**

**[BUY ME A COFFEE](http://bit.ly/2NCtG3k)**

Special thanks to all contributors!