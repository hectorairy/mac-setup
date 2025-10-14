## My Macbook Setup

This repo contains info of all the apps and settings I use on my Mac for software development and productivity

## OS Settings

These are my preferred settings for `Desktop`, `Finder` and the `Dock`.

### Desktop

Trackpad, Active Tap to click

I don't like the new Desktop, Stage Manager or Widget features in new versions of macOS, so I disable them.

- System Preferences
  - Desktop & Dock
    - Desktop & Stage Manager
      - Show Items
        - On Desktop -> uncheck
        - In Stage Manager -> uncheck
      - Click wallpaper to reveal desktop -> Only in Stage Manager
      - Stage Manager -> uncheck
      - Widgets
        - On Desktop -> uncheck
        - In Stage Manager -> uncheck

### Finder

- Finder -> Preferences
  - General -> Show these on the desktop -> Select None
    - I try to keep my desktop completely clean.
  - General -> New Finder windows show -> Home Folder
    - I prefer to see my home folder in each new finder window instead of recent documents
  - Remove all tags
  - Sidebar show a Home, Downloads, Documents, Applications and Desktop
  - Advanced -> Show all filename extensions -> Yes
  - Advanced -> Show warning before changing an extension -> No
  - Advanced -> When performing a search -> Search the current folder
  - Show as a list
- View
  - Show Status Bar
  - Show Path Bar
  - Show Tab Bar

### Dock

I don't use the Dock at all. It takes up screen space, and I can use RayCast to launch apps and AltTab to switch between apps. I make the dock as small as possible and auto hide it.

- System Preferences
  - Desktop & Dock
    - remove all apps from dock
    - Size -> Small as possible
    - Position on screen -> Left
    - Automatically hide and show the Dock -> Yes
    - Animate opening applications -> No
    - Show suggested and recent apps in the Dock -> No

Menu Bar
Control center
Battery no
Clock option
show date never
Disable AM/PM
Style analog
Spothlight no show

## Quick Launching

The built in spotlight search is a bit slow for me and usually has web search results as the default instead of apps or folders on my machine.

I recently use [RayCast](https://www.raycast.com/). I'm really liking it so far.

I use to replace spotlight shortcut and use it to open raycast:

Sistem preferences
keyboard
keyboad shortcuts
show spotlight seach option space

show raycast in menu bar no

Then I put all my shortcuts in raycast window managment

Open settings -> Extensions 
  Window managment
    Center Three Fourths - ALT + CMD + C
    Left half - ALT + CMD + <-
    Maximize - ALT + CMD + ENTER
    Restore - ALT + CMD + DEL
    Right half - ALT + CMD + ->
  Clipboard History
    Clipboard History - CMD + SHIFT + V

## Homebrew

### Homebrew

[Homebrew](https://brew.sh/) allows us to install tools and apps from the command line.

To install it, open up the built in `Terminal` app and run this command:

```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

This will also install the xcode build tools which is needed by many other developer tools.

After Homebrew is done installing, we will use it (via RayCast) to install everything else we need.

### RayCast Homebrew Plugin

Install the [RayCast Homebrew Plugin](https://www.raycast.com/nhojb/brew) so we can easily install formulae and casks directly from RayCast.

## App Switching

The built in App switcher only shows application icons, and only shows 1 icon per app regardless of how many windows you have open in that app.

I use an app switcher called [AltTab](https://alt-tab-macos.netlify.app/). It shows full window previews, and has an option to show a preview for every open window in all applications (even minimized ones).

I replace the built-in `CMD+TAB` shortcut with AltTab.

Search for `alt-tab` in RayCast `brew search` or:

```sh
brew install alt-tab
```

Then open settings disable show menubar icon and change shortcut to use command tab

## Menu Bar Utilities

### Hidden Bar

If you have several apps running that have menu bar icons, [Hidden Bar](https://github.com/dwarvesf/hidden) will let you choose which ones should be hidden after a timeout. This cleans things up if you have a ton of background apps running.

Search for `hiddenbar` in RayCast `brew search` or:

```sh
brew install hiddenbar
```

Start hidden bar when I log in yes
Show preferences on launch no

### System Stats Widgets

I use [stats](https://github.com/exelban/stats) to see my network traffic, CPU temp / usage and RAM usage at a glance.

In each widget, a key setting to look for is under "widget settings", choose "merge widgets into one".

Search for `stats` in RayCast `brew search` or:

```sh
brew install stats
```

Show ram
Battery (merge icons)
Clock (E d MMMM h:mm a)

# Browser

## Other Apps I Use Daily

- [kap](https://getkap.co/) - Screen recorder / gif maker (Homebrew)
- [Bitwarden](https://bitwarden.com/es-la/) - Password manager (Homebrew)
- [Spotify](https://open.spotify.com/) - Music streaming platform (Homebrew)
- [Boring Notch](https://theboring.name/) - Customizable macOS notch tool
- [AppCleaner](https://freemacsoft.net/appcleaner/) - Uninstall apps completely on macOS (Homebrew)
- [Obsidian](https://obsidian.md/) - Markdown-based note-taking and knowledge management (Homebrew)
- [Notion Calendar](https://www.notion.com/product/calendar) - Calendar app by Notion for scheduling and time-blocking (Homebrew)

### OrbStack (Docker)

```sh
brew install --cask orbstack
```

### Github SSH Setup

- Follow [this guide](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) to setup an ssh key for github
- Follow [this guide](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account) to add the ssh key to your github account

## Node.js

I use nvm to manage the installed versions of Node.js on my machine. This allows me to easily switch between Node.js versions depending on the project I'm working in.

See installation instructions [here](https://github.com/nvm-sh/nvm#installing-and-updating).

OR run this command (make sure v0.39.7 is still the latest)

```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
```

Now that nvm is installed, you can install a specific version of node.js and use it:

```sh
nvm install 22
nvm use 22
node --version
```

Install yarn and upgrade npm

```sh
npm install -g npm
npm install -g yarn
```
