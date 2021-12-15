# No keyboard in PWA when other PWA in background

## Summary
The keyboard is not shown in PWA if at least one other PWA is running in the background on the iPad or iPhone.

## Steps to reproduce
1. Install a PWA like https://jamesjohnson280.github.io/hello-pwa
2. Install second PWA https://dstester.github.io/PWAKeyboardNotOpening/
3. Open first PWA
4. Open second PWA
5. Click on the text-input element in the PWA
6. Keyboard does not open (bug)
7. Close alls PWA's
8. Open only second PWA
9. Click on the text-input element in the PWA
10. Keyboard works again

## Description
If an installed PWA is running in the background, the keyboard is not opening if you click on a input (type: text, number, tel and some other) or textarea element in an other installed PWA.
Date-, time- and colorpicker are working like expected.
The value of window.visualViewport.height changes, as if the keyboard was shown and the viewport is scrollable for the height of the keyboard.
On the iPhone it shows the keyboard toolbar in the middle of the screen, but the keyboard is not shown below.
Example sourcecode, videos and screenshots can be found at https://github.com/DSTester/PWAKeyboardNotOpening

This happens also with other installed PWA's like https://mobile.twitter.com or https://web.dev but not in Safari, even not with two instances runing.
From my testing it seems like the bug was introduced in iPadOS 15.1/14.8.1. 

## Tested with
* iPad 8.Gen, MYMH2FD/A, iPadOS 15.1 & 15.2, Webkit/605.1.15 => does happen
* iPad Air, MD791FD/A, iOS 12.5.5 => does not happen
* iPad Air2, iPadOS 14.8.1 (18H107) => does happen
* iPhone SE, MP822DN/A, iOS 15.1 & 15.2, Webkit/605.1.15 => does happen
* Simulator 13.1 (970), SimulatorKit 612, CoreSimulator 776.4
    * iPad Pro 9.7, iOS 15.0, does not happen
    * iPad Air 4th Gen., iOS 15.0, does not happen
* Simulator 13.2 (972.2), SimulatorKit 613.1, CoreSimulator 783.5
    * iPad Pro 9.7, iOS 15.2, does happen
    * iPad Air 4th Gen., iOS 15.2, does happen
* Samsung SM-P600, Android 5.1.1, Webkit/537.36 => does not happen
* Samsung SM-A505FN, Android 11, Webkit/537.36 => does not happen
