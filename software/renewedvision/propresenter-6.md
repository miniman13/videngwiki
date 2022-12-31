---
title: ProPresenter 6
description: Legacy ProPresenter Information
published: true
date: 2022-12-31T05:17:56.188Z
tags: propresenter, lyrics, renewedvision
editor: markdown
dateCreated: 2022-10-19T03:00:40.799Z
---

# ProPresenter 6

> ProPresenter has announced effective January 31, 2023, ProPresenter 6 will be no longer supported or updated and the ProPresenter 7 upgrade discount will no longer be available. See [ProPresenter 6 End of Life FAQs](https://support.renewedvision.com/hc/en-us/articles/10589582923027-ProPresenter6-End-of-Life-Frequently-Asked-Questions) for more information.
{.is-warning}



## Tips and Tricks

### Changing Underline Font Color

Sometimes ProPresenter will do funky things when setting a highlighted portion of text that includes an underline. When this occurs, ProPresenter will display an underline that is not the same color as the text highlighted. To fix this, you must manually set the underline color in the	`Text Style` dialog.

Edit the slide, and go to the `Text Properties` tab. Click the 'Edit Text Style' option. (The button with an 'A' on it), then from the underline option select `color` and set the underline color.

### Managing Media Automatically.

ProPresenter by default is set to manage media automatically. This means ProPresenter will copy all media imported into ProPresenter in a folder (called 'Renewed Vision') and will sort the media into subfolders so the application knows where each file is. This is very helpful if you are importing things from external drives, or don't want to physically manage media locations manually.

## Configuration and Media Transfer

Below are the files that need to be transferred to copy a machine's configuration over to another Mac.

ProPresenter Library Documents

`~/Documents/ProPresenter6/`(entire folder)

ProPresenter Managed Media

`~/Renewed Vision Media/`(entire folder)

ProPresenter Support Files (Cache, Clocks, Templates, Stage Display, Playlists, etc)

`~/Library/Application Support/RenewedVision/ProPresenter6/`(entire folder)

ProPresenter Preferences

`~/Library/Preferences/com.renewedvision.ProPresenter6/` (entire folder)

`~/Library/Preferences/com.renewedvision.ProPresenter6.plist`