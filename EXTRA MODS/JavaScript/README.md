JavaScript files are used to further extend/modify the capabilities of Firefox.

There are many JS autoloaders out there, the one I use is: https://github.com/MrOtherGuy/fx-autoconfig
Check the repo and follow the steps there to install the autoloader.

There are many sources for JS to customize Firefox on the Internet, the scripts in use are taken from: https://github.com/aminomancer/uc.css.js
These repos are added as submodules, so to make sure that you have these when cloning this repo:
```bash
git clone --recursive-submodules -j8 https://github.com/Domiragi/FFox-MB.git
```
where `-j8` is an optional performance optimization that became available in version 2.8, and fetches up to 8 submodules at a time in parallel — see `man git-clone`.

To clone the repos with the submodule ***and*** also update the submodules to the latest version:
```bash
git clone --recursive-submodules --remote-submodules -j8 https://github.com/Domiragi/FFox-MB.git
```

To fetch the latest version of all the submodules at a later time:
```bash
git submodule update --remote --merge
```

After following the steps to install fx-autoconfig into your Firefox folders, put the JS files you want to use into the `JS` folder in `chrome` folder in your Firefox profile folder.
Most scripts can be used as is, but some might require to make changes to CSS (your `userChrome.css` file), so make sure to read each file before use.

The scripts I'm using are:
- [Let Ctrl+W close pinned tabs](/EXTRA MODS/JavaScript/uc.css.js/JS/letCtrlWClosePinnedTabs.uc.js)
- [Findbar mod](/EXTRA MODS/JavaScript/uc.css.js/JS/findbarMods.uc.js)
- [Misc mods](/EXTRA MODS/JavaScript/uc.css.js/JS/miscMods.uc.js): a collection of several small mods
