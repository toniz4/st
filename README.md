# Yet another St build

this build of st aims to be minimal, but totaly usable. 

## Patches

- bold is not bright, to not make bold colors bright
- clipboad, making it possible to copy to the clipboad
- font2, so we can use fallback fonts, and fontconfig fonts (read note below)
- osc, for escaping the background color
- solarized theme
- xresources, for setting up fonts and colors in the Xresources file

## St is crashing 

 this is happening because of a bug within the xft library that happens when trying
to render colored emojis, if you are on arch or derivatives you can use
lixft-brga and you should not have this problem. But for that reason i'm
choosing to use non colored emojis, and if you want to render colored emojis,
make sure to delete the Noto Emojis line in the config.def.h. And if st still is
crashing with Noto Emojis in the configs, probably fontconfig is setted up to
prefer colored emojis over uncolored ones.
