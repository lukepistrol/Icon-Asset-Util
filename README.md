# Remove Alpha Channel from PNGs
This script will remove the alpha channel of every PNG in a specific directory. 

This is especially useful for iOS App Icon Assets which require the alpha channel to be removed in order to be accepted by App Store Connect. Many applications like Figma export PNGs with alpha channel by default with no easy way to disable it. 

The workaround would be to open each exported PNG in Preview and export it again with the "Alpha Channel" option unchecked.

# Usage
First of all make the script executable
```bash
$ chmod u+x remove-alpha-channel.sh
```

## Install permanently (recommended)
To install this script permanently just put it in your */usr/local/bin/* directory.

```bash
$ sudo cp remove-alpha-channel.sh /usr/local/bin/remove-alpha-channel
```

To use the script just navigate to your asset directory (where all the PNGs are) and call the script.

```bash
$ cd path-to-your-directory
$ remove-alpha-channel .
```

Optionally you can simply pass the path to your directory as an argument.

```bash
$ remove-alpha-channel path-to-your-directory
```

## Use in your own location
You can also put it wherever you want and use it like this:

```bash
$ cd path-to-script
$ ./remove-alpha-channel.sh path-to-your-directory
```