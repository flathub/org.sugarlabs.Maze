# Maze Activity Flatpak

A simple maze game for the Sugar learning environment.

To Know more about sugar, Please refer to;

* [How to Get Sugar on sugarlabs.org](https://sugarlabs.org/)
* [How to use Sugar](https://help.sugarlabs.org/)

## How To Build

```
git clone https://github.com/flathub/org.sugarlabs.Maze.git
cd org.sugarlabs.Maze
flatpak -y --user install flathub org.gnome.{Platform,Sdk}//46
flatpak -y --user install org.sugarlabs.BaseApp//24.04
flatpak-builder --user --force-clean --install build org.sugarlabs.Maze.json
```

## Check For Updates

Install the flatpak external data checker
```
flatpak --user install org.flathub.flatpak-external-data-checker
```

Now to update every single module to the latest stable version use
```
cd org.sugarlabs.Maze
flatpak run --filesystem=$PWD org.flathub.flatpak-external-data-checker org.sugarlabs.Maze.json
```
