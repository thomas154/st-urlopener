# St-urlopener
A script to ease the task of opening url present on st(suckless terminal) using dmenu.

This will only work with patched version of st with external pipe feature enabled.

## Dependency
+ Dmenu
+ Notify-send for notification (optional)

## Demo
+ Grabbing links from Reddit terminal viewer(rtv). 

![demo1](https://raw.githubusercontent.com/thomas154/gifs-for-repositories/master/st-urlopener-gif/demo1.gif)

+ Grabbing links from Newsboat.

![demo2](https://raw.githubusercontent.com/thomas154/gifs-for-repositories/master/st-urlopener-gif/demo2.gif)

Above demo showed some use cases, but this script can be used with any terminal app or to grab links easily present on st without configuring each app individually.... 

## Installation
```
git clone https://github.com/thomas154/st-urlopener.git
cd st-urlopener
chmod +x urlopener extract
```

## Usage 
- Press the key bindings to execute the script on focused terminal.
```
 Alt+u #Mine is binded to this
```

You can use my st patched version from [here](https://github.com/thomas154/st)

## NOTE
 For script to work make sure you  replace
 ```
 ~/scripts/st-urlopener/./urlopener
 ``` 
 at line 203 of config.h of suckless terminal.
 
 with
 ```
 static char *openurl[] = { "/bin/sh", "-c", "sed 's/ssh:\\/\\///g' | pathToTheUrlopenerFile./urlopener", "externalpipe",NULL, NULL   };
 ```
