# ubuntu-18-install-sogou-input
Guide on how to install sogou Chinese input in ubuntu 18.

Main reference: 
https://www.twblogs.net/a/5c160eb4bd9eee5e418429ff

This reference is pretty good already, but I added something here, might help make solution more robust. 

## Completely remove fcitx
```
sudo apt -y remove *fcitx*
sudo apt autoremove
```

## Reinstall fcitx

```
sudo apt -y install fcitx fcitx-bin fcitx-table fcitx-table-all
sudo apt -y install fcitx-config-gtk
```

## Remove ibus
```
sudo apt purge ibus
sudo apt autoremove
```

## Download from official website the .deb file for sogou input and then install:

Download from https://pinyin.sogou.com/linux/?r=pinyin

`sudo dpkg -i <sogouinstallfile.deb>` 

You might saw some log saying dependency missing, don't worry we can solve it later. 

## Solve dependency issues:
`apt-get install -f`

## Go to language and support page to install Chinese language and change input to fcitx

It might tell you there are some packages to install, and might install ibus again.

## Restart computer

Typically now things should work.

Refer to reference pages for more help if things don't work. 
