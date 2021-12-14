# No keyboard in PWA when other PWA in background 

## Webkit bug?
TODO: Test on Android
 
## Summary
The Keyboard does not open in PWA if at least one other PWA is running in the background on the iPad or iPhone.

## Steps to reproduce
1. Install a PWA like web.dev
2. Install second PWA like mobile.twitter.com
3. Open one PWA
4. Open other PWA
5. Click on any input element in the PWA
6. Keyboard does not open (bug)
7. Close all PWA's
8. Open one PWA
9. Click on any input element in the PWA
10. Keyboard opens as expected

## Description
May be connected to this webkit bugs:
* https://bugs.webkit.org/show_bug.cgi?id=223431
* https://bugs.webkit.org/show_bug.cgi?id=226848


## Tested with
* iPad 8.Gen, MYMH2FD/A, iPadOS 15.1 => does happen
* iPad Air, MD791FD/A, iOS 12.5.5 => does not happen
* iPhone SE, MP822DN/A, iOS 15.1 => ?
* iPad Air 4, iOS 15.2 Beta 3 (19C5044b) => ?
* iOS-Simulator, iPad 9. Gen., iOS 15.0 ?

