# Icon Asset Utility
This script allows you to create iOS App Icon Assets which can be dragged directly into Xcode.

Additionally you can remove the alpha channel of every PNG in a specific directory. 

This is especially useful for iOS App Icon Assets which require the alpha channel to be removed in order to be accepted by App Store Connect. Many applications like Figma export PNGs with alpha channel by default with no easy way to disable it. 

The workaround would be to open each exported PNG in Preview and export it again with the "Alpha Channel" option unchecked.

# 1. Installation
## 1.1 Install permanently (recommended)
To install this script permanently just put it in your ```/usr/local/bin/``` directory.

```bash
$ sudo cp icon-asset-util /usr/local/bin/icon-asset-util
```

Now it can be used globally just by calling
```bash
$ icon-asset-util [options]
```

## 1.2 Use in your own location
You can also put it wherever you want and use it like this:

```bash
$ path-to-script/icon-asset-util [options]
```

# 2. Usage
## 2.1 Create App Icon Set
To create an Asset Catalog simply put any input PNG in a convenient location and from there call

```bash 
$ icon-asset-util -a your-icon.png
```
This will create an 'AppIcon.appiconset' folder with all the required sizes inside. It also creates a 'Content.json' file so you can just drag the whole folder into your Xcode projects Assets Catalog.

## 2.2 Remove Alpha Channel
If you already have your icons in all the required sizes, but you encounter an error when uploading to App Store Connect, that the App Icon must not have an alpha channel, navigate to your asset folder inside your Xcode project and run the following command

```bash 
$ icon-asset-util -r .
```

Or provide the path to the asset folder as an argument

```bash 
$ icon-asset-util -r path-to-directory
```

# 3. Changelog
## Version 2.0
* **Important:** Script was renamed to ```icon-asset-util```
* **Important:** Syntax changed (see current Syntax above)
* Create App Icon Sets

## Version 1.2
* Ommitted ```.sh``` file extension

## Version 1.1
* Show status when converting
* Display success message on completion

## Version 1.0
* Remove the alpha channel of all PNGs in a folder
