# St-urlopener
A script to ease the task of opening url present on st(suckless terminal) using dmenu.

This will only work with patched version of st with external pipe feature enabled.

## Dependency
+ Dmenu
+ Notify-send for notification (optional)

# Demo
+ Grabbing links from Reddit terminal viewer(rtv). 

![demo1](/gifs/demo1.gif)

+ Grabbing links from Newsboat.

![demo2](/gifs/demo2.gif)

Above demo showed some use cases, but this script can be used with any terminal app or to grab links easily present on st without configuring each app individually.... 

# Note
Make sure the location in urlopener script points to the location of extract script.

```
url=`~/scripts/st-urlopener/./extract|dmenu -i -l 10 -p Urls -fn 'roboto mono nerd font:bold:size=11'` 
```
change the location as per required.

In my case it is present at ~/scripts/st-urlopener/

