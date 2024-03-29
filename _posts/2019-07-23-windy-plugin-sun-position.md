---
layout: post
title: "Windy Plugin: Sun Position"
tagline: "Inspired py PhotoPills, this Plugin gives you Sun details on Windy.com"
header_bg: "/assets/blog_assets/windy-plugin-sun-position/header.jpg"
header_color: '#010'
header_source: '© OpenStreetMap contributors ; windy.com'
categories:
  - blog
  - project
author: "Jochen Jacobs"
---

This is a plugin for [Windy](https://www.windy.com) that gives shows sun and moon position on the map and gives details about sunset and sunrise times as well as other sun and moon details. It is called ```windy-plugin-sun-position```.

**Unfortunately Plugins do not work in the app currently**

[Open Plugin](http://www.windy.com/plugins/windy-plugin-sun-position) | [View Code on GitHub](https://github.com/jacobsjo/windy-plugin-sun-position)

You can also open the plugin by going to *Menu → Install Windy plugin → Select "Sun position"*.

To open the display, right-click on the map (or tap and hold on mobile), then select "Sun Position". Then open a weather picker to see the sun dial and the details on the left.

### Dial
![Sun dial](https://raw.githubusercontent.com/jacobsjo/windy-plugin-sun-position/master/pictures/sundial.jpg "Sun dial")

The dial displays the current sun and moon azimuth on the map using a black line from the picker position. Additionally, dashed lines show the azimuth of sunrise and sunset and dotted lines show the azimuth of moonrise and moonset. Clicking on the sunrise, sunset, moonrise and moonset lines will set the current time to the respective time.

### Detail pane
![Sun detail pane](https://raw.githubusercontent.com/jacobsjo/windy-plugin-sun-position/master/pictures/sundetail.jpg "Sun detail pane")

The detail pane on the left shows the time of astronomical, nautical, and civil dusk and dawn; start and end of blue and golden hour and solar noon. Moonrise and moonset times are also added to the timeline. Below, a diagram of the sun and moon altitudes over time is displayed. Below that, details about the current sun and moon position are shown.

On the top of the detail pane it is possible to enable and disable individual displays. The telescope toggles visibility of astronomical sun details (astronomical and nautical dawn and dusk). The camera toggles visibility of blue and golden hour times. The moon toggles visibility of moon details.


### Changelog
#### V0.1.0
Original release

#### V0.1.1
Fixed timezone issues:
- Displays times in timezone of position selected (instead of local timezone of user)
- When Windy setting to display all times in UTC is selected, displays all times in UTC

#### V0.2.0
- **The hook has been changed from the Overlay layers menu to the context-menu.**
- Displays only times that exist: If the sun does not go far enough below the horizon, astronomical dawn and dusk might not exist and the entire night is astronomical twilight. In this (and more extreme) cases the non-existent times are hidden
- The plugin now works on mobile (thanks @rittels for the help)
- Fixed some delay issues that resulted from the timezone-lookup

#### V0.3.0
- reworked detail phase
- included details about the moon
- fixed blue hour times
- redesigned current sun position display
- added options to disable moon, astronomical details and photography details separately
- added footnote with links to plugin pages

#### V0.3.1
- desktop sidebar hotfix (broken by change on windy)

#### V0.3.2
- fixed plugin loading issue (broken by change on windy)
- changed timezone lookup to tz-lookup package
- added querry string

#### V0.3.3
- fixed plugin loading issue (broken by change on windy)

#### V0.3.4 and V0.3.5
- fixed issue finding location (broken by change on windy)
