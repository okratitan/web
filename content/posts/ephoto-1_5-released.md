---
title: "Ephoto 1.5 Released"
date: 2017-08-21T11:46:32-05:00
---

![alt text](/images/ephoto.png "Ephoto")

This is a bugfix release that also contains a slight change to the interface of Ephoto.  The main interface is no longer using the translucent overlay panels for file browsing and such.  It is now using standard elementary widgets and no longer hovers over other items hiding your images.  This release also fixes the issues with compiling and running Ephoto with EFL 1.20.  This release will bridge the gap between 1.0 and 2.0.

Here is a log of the changes since the 1.0 Release:

commit 197ef09a0f40ccfdcd66ea07f02ab4a003cc4c39
Author: Stephen ‘Okra’ Houston <smhouston88@gmail.com>
Date: Mon Aug 21 16:05:49 2017 -0500

Ephoto: Don’t use panes in the editor.

commit 01af89d1648de796e598cc4c39c890f27a30c6f9
Author: Stephen ‘Okra’ Houston <smhouston88@gmail.com>
Date: Mon Aug 21 15:59:36 2017 -0500

Ephoto: Bump version to 1.5 – A bugfix Release and Bridge from 1.0 to 2.0.

commit a9ddb8add7352833720a8fb679b1271193265df1
Author: Stephen ‘Okra’ Houston <smhouston88@gmail.com>
Date: Mon Aug 21 15:58:07 2017 -0500

Ephoto: Removed buggy panes.

commit 5ee6630a6cd8a66b1a2861609ece26768662fac5
Author: Marcel Hollerbach <marcel-hollerbach@t-online.de>
Date: Mon Aug 21 13:59:16 2017 +0200

ephoto: remove reminder, this was wrong

fix T5888

commit 47fe2b9ab03c151b0f459b99de0dd52c49b5705c
Author: Marcel Hollerbach <marcel-hollerbach@t-online.de>
Date: Sun Aug 20 09:30:13 2017 +0200

ephoto: make it work again

It turns out that there is some madness when setting a aspect on a
elm.label. This should at first fix this, but its far from a good
solution.

ref T5888

commit b76a54bd3ee93fe9d529e577251a1d5fc6b32d1a
Author: Stephen ‘Okra’ Houston <smhouston88@gmail.com>
Date: Thu Jul 27 12:51:28 2017 -0500

Ephoto: Remove unneccessary header.

This fixes compilation and T5761

commit 4828fe95a4b5065c2d88da1ad1a223843dee23bf
Author: Stephen ‘Okra’ Houston <smhouston88@gmail.com>
Date: Mon Jun 26 12:28:24 2017 -0500

Ephoto: Give the user the option to choose between cropped thumbnails and aspect based thumbnails.

commit 1265151a8324398555ade623c5008cc4db9408e5
Author: Stephen ‘Okra’ Houston <smhouston88@gmail.com>
Date: Wed May 10 14:03:48 2017 -0500

Ephoto: Check that a path exists before running file_file_get on it.

commit 9474ceaa00ccddf020dc5df0ac9f953834cf7b56
Author: Stephen ‘Okra’ Houston <smhouston88@gmail.com>
Date: Mon May 8 16:21:41 2017 -0500

Ephoto: Implement open/closed folder icon changing and clean up some fdo icons.

commit 5759135ad3e064aa33899dd805ec17aad17c1697
Author: Stephen ‘Okra’ Houston <smhouston88@gmail.com>
Date: Fri May 5 11:08:15 2017 -0500

Ephoto: Fix a potential crash when switching directories in single view.

commit e53ee13f3cfaf0b8c1cc4e094587f3a0a633bdeb
Author: Stephen ‘Okra’ Houston <smhouston88@gmail.com>
Date: Wed May 3 09:26:45 2017 -0500

Ephoto: make sure the monitor callback for delete is on the file we are working on.

commit 3480bb44b39a169b8eb052a3a8826452b2265cd8
Author: Stephen ‘Okra’ Houston <smhouston88@gmail.com>
Date: Tue May 2 11:19:43 2017 -0500

Ephoto: Factor out common code, use “start” for Windows based devices instead of xdg-open, improve compiler flags.

commit d8e2df3092f564c0462ba12d7d909da86114e544
Author: Stephen ‘Okra’ Houston <smhouston88@gmail.com>
Date: Mon May 1 22:30:20 2017 -0500

Ephoto: Remove trailing /

commit dc89de84e98cc3749ed8dae1ca5335e8b0cff78a
Author: Stephen ‘Okra’ Houston <smhouston88@gmail.com>
Date: Mon May 1 18:44:56 2017 -0500

Ephoto: Move root/home shortcuts into the context menu and remove min size restrictions that affect window resizing.

commit 31d122f98fb1618705773c4bfa1a1d098486de39
Author: Stephen ‘Okra’ Houston <smhouston88@gmail.com>
Date: Mon May 1 15:28:01 2017 -0500

Ephoto: Quit dumb negative padding.

commit 788863df681ae11397a65095841da1a893078419
Author: Stephen ‘Okra’ Houston <smhouston88@gmail.com>
Date: Mon May 1 15:24:07 2017 -0500

Ephoto: Don’t send unnecessary signals now that we are not showing/hiding panels in edje.

commit 76a02499ab5c51bf170703a851bb03e6090fd3be
Author: Stephen ‘Okra’ Houston <smhouston88@gmail.com>
Date: Mon May 1 13:56:14 2017 -0500

Ephoto: Allow resizeable panels, remove checkerboard so that it functions better with themes, add shortcuts for home and root.

commit 9bdacab76f3f50a988267dd9b0e7b589c99db432
Author: Stephen ‘Okra’ Houston <smhouston88@gmail.com>
Date: Wed Apr 19 10:59:18 2017 -0500

Ephoto: Don’t set a color on the background of the tiling so that the transparency overlays will match any theme’s background.

As always if you have any questions, please let me know.

Thanks!
Stephen
