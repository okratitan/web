---
title: "Fynedesk Features and Improvements"
date: 2019-08-26T11:57:30-05:00
aliases: ["/posts/fynedesk/"]
---


![alt text](/images/fyne.png "Fynedesk") Over the course of the last month I have been putting a lot of time into improving the [Fyne Desktop](https://github.com/fyne.io/desktop).  Fyne Desktop is an X11 desktop environment written in Go.  The project founder Andrew Williams, whom I consider to be a close friend, built a solid base to work from with basic window manager functionality.  After I joined on the [Fyne](http://www.fyne.io) project as a contributor, one of my first areas of interest was the desktop.  I have had nearly two decades of experience working on linux desktops and they have alway been a passion of mine.  So upon initial inspection of the state of the desktop, I determined the immediate needs were an application bar or dock, taskbar, application launcher, and minimize/maximize functionality for the windows.

In order to complete the application bar, taskbar, and launcher, the first requirement was a revisit of the [FDO Icon Theme Specification](https://standards.freedesktop.org/icon-theme-spec/icon-theme-spec-latest.html).  Once I had refamiliarized myself with the spec I began developing an interface that provided this functionality.  Andrew would later follow this up with a Mac OSX interface as well.  The next step was to design the application bar.  Many moons ago Andrew had written an application bar/taskbar for Enlightenment that was called "Engage".  It is still beloved to this day.  It is similar in use and feel to the Mac OSX dock.  So we agreed that it would be neat to revive engage for use in Fyne Desktop.  This satisfied our need for an application bar and taskbar.  Here are some images that show the application bar in action:
![FyneDesk Appbar](/images/fynedesk_appbar.png)

![FyneDesk Appbar Zoom](/images/fynedesk_appbar_zoom.png)

The next step was completing an application launcher so that users could run apps without having to open a terminal and place all of their icons in the application bar.  Using the same underlying application/icon code we wrote for the application bar and taskbar, we created a simple window that auto populates a list of applications that match what you are typing, as you type.  The end result can be seen here:
![Fynedesk App Launcher](/images/fynedesk_applauncher.png)

Now that we had application handling in a solid state, we needed to have the ability to minimize(iconify) windows, as well as maximize them.  In order to do this correctly, it would involve following two specs, the [Inter-Client Communication Conventions Manual](https://tronche.com/gui/x/icccm/) and the [Extended Window Manager Hints Specification](https://specifications.freedesktop.org/wm-spec/wm-spec-latest.html#idm140200472615568).  This would involve creating a client layer for windows that are managed by Fyne Desktop.  This layer exists between the window manager and the window frame and allows for the handling of messaging, properties, and states related to clients of the window manager.  With minimize and maximize in place, the application taskbar was then updated to handle and interact with these features.

With these features now in place, Fyne Desktop is becoming quite usable.  There are still many features and improvements left to go, but a solid foundation has been built and perhaps a release is not too far off.  If you would like to contribute, or just follow along and chat with us as we continue development, feel free to hangout in the #fyne and #fyne-desktop channels on [Gopher's Slack](https://gophers.slack.com)

Here is an updated screenshot of Fyne Desk in action:
![Fyne Desktop Environment](/images/fynedesk_updated.png)

Stephen Houston
