ColorCheckerProfileGenerator
============================

ColorCheckerProfileGenerator is a standalone Bash script which reads a TIFF
file containing a photo of the ColorChecker Passport and creates an ICC profile.
This profile can then be used by software like AfterShot Pro.

It offers a minimalist GUI using Zenity.

Requirements
------------

This script has been developped and tested on Ubuntu 14.

It requires the following packages to be installed prior to its execution:

- gnome-color-manager (this will also install Argyll CMS)
- Image Magick
- Zenity

Installation
------------

The script should be placed in a directory accessible by the PATH variable. For
example, it can be placed in you ~/bin directory as it does not require special
rights to run.

AfterShot Pro configuration
---------------------------

If you use this script with AfterShot Pro, you can enhance your experience by
creating a new batch output based on the standard "16-bit TIFF" one.

It should have the following settings:

- Image type: TIFF(16 bit)
- Resize width/height: 800/1200
- Output color space: LinearRGB
- Metadata: none
- Postprocessing: open with ColorCheckerProfileGenerator

How to use it
-------------

You should have done a photo of the ColorChecker Passport.

Open the photo:

- crop it on the marks
- Make sure there is no correction (no saturation, vibration, contrast,
  sharpening etc.)
- choose Linear as color management

Use the ColorChecker batch output profile

Enter the following values:

- Camera name
- Description
- Copyright (the author)
- ICC profile name

You can use accents or special characters. 

Notes
-----

I’ve not been able to make scanin automatically recognize the ColorChecker
position in the photo, this is why you have to crop it.

I cannot make Zenity remember the previous values for each field, you have to
type all the values every time you use it (in order to do it, this project
would be more complex than it is today).

