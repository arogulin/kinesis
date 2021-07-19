# kinesis
Kinesis Advantage2 keyboard setup

I got this keyboard on July 17th of 2021 and here I will keep some configuration files and interesting ideas about key remapping and so forth.

An interesting mapping I found on [reddit](https://www.reddit.com/r/kinesisadvantage/comments/o4qeoy/best_qwerty_key_changes/h2ni9pk/?utm_source=reddit&utm_medium=web2x&context=3), huge thank you to redditor [wonderbreadofsin](https://www.reddit.com/user/wonderbreadofsin/):
```
[caps]>[kpshft]
[kp-x]>[1]
[kp-c]>[2]
[kp-v]>[3]
[kp-s]>[4]
[kp-d]>[5]
[kp-f]>[6]
[kp-w]>[7]
[kp-e]>[8]
[kp-r]>[9]
[kp-bspace]>[0]
[kp8]>[up]
[kp4]>[left]
[kp5]>[down]
[kp6]>[right]
{left}>{speed9}{-lctrl}{-lwin}{left}{+lctrl}{+lwin}
{right}>{speed9}{-rctrl}{-lwin}{right}{+rctrl}{+lwin}
{kp7}>{speed9}{-lshift}{obrack}{+lshift}
{kp9}>{speed9}{-lshift}{cbrack}{+lshift}
{kpmin}>{speed9}{-lshift}{=}{+lshift}
[kp-caps]>[kpshft]
{kpplus}>{speed9}{-lshift}{hyphen}{+lshift}
[kp-']>[`]
[kp0]>[space]
{kp1}>{speed9}{-lshift}{9}{+lshift}
{kp3}>{speed9}{-lshift}{0}{+lshift}
[kp2]>[=]
{kp-y}>{speed9}{-lshift}{4}{+lshift}
{kp-h}>{speed9}{-lshift}{1}{+lshift}
{kp-n}>{speed9}{-lshift}{2}{+lshift}
{kpenter1}>{speed9}{-lshift}{`}{+lshift}
[=]>[`]
```

Explanation:

> I remapped Caps Lock to be my layer switch key, then changed all of the keys on my right hand to do something different on the second layer (while I'm holding down Caps Lock).

> I,J,K,L are now my arrow keys on the second layer. The existing arrow keys I've changed to do other things on the default layer, like switch desktops in Windows.

> I moved the number pad to my left hand, since when I use that I toggle layers instead of holding down Caps Lock.

> All of the other keys on my right hand do something useful for programming on the second layer. i.e. U and O are round braces, M and . are curly braces. ' is backtick, , is equals, Y is $, H is !, etc.

> The keyboard has two "layers", the normal layer and the keypad layer. If you haven't remapped anything, the keypad layer just has the number pad, and you switch to the keypad layer by pressing the keypd button. But you can remap everything and make that layer way more useful.

> The keypd button toggles layers, but you can also create a layer shift key, which only keeps the keyboard on the keypad layer while you're holding it down. I made that my Caps Lock button. I then created custom mappings for a bunch of keys. So now I can hold down the caps lock button with my left pinky, and the home row keys in my right hand turn into the arrow keys for navigation. Super useful.

> You can also assign macros, which are sequences and combinations of keys. To the left and right arrow keys, I assigned the key combinations for switching between desktops, for instance.


Some troubleshooting:
```
I added the following to my qwerty.txt:

[caps]>[kpshft]

But it makes for that key to now do both CapsLock and keypad layer. 
Do I need to delete the CapsLock assignment somewhere?

I had forgotten to add [kp-caps]>[kpshft]
```
 
---
Another remapping idea, this one has interesting browser macros: https://github.com/fatih/dotfiles/blob/main/kinesis-layout/qwerty.txt
```
[caps]>[lctrl]
[delete]>[bspace]

[lctrl]>[lwin]
[kp-lctrl]>[lwin]

[lalt]>[hyper]
[kp-alt]>[hyper]

[rwin]>[lalt]
[kp-rwin]>[lalt]

[rctrl]>[rwin]
[kp-rctrl]>[rwin]


*******************
** embedded layer *
*******************

[bspace]>[kpshift]
[kp-bspace]>[kpshift]

** left side **
****************

{kp-Q}>{speed9}{-lshift}{1}{+lshift}
{kp-W}>{speed9}{-lshift}{2}{+lshift}
{kp-E}>{speed9}{-lshift}{obrack}{+lshift}
{kp-R}>{speed9}{-lshift}{cbrack}{+lshift}
{kp-T}>{speed9}{-lshift}{\}{+lshift}

{kp-A}>{speed9}{-lshift}{7}{+lshift}
{kp-S}>{speed9}{-lshift}{4}{+lshift}
{kp-D}>{speed9}{-lshift}{9}{+lshift}
{kp-F}>{speed9}{-lshift}{0}{+lshift}
[kp-G]>[`]

{kp-Z}>{speed9}{-lshift}{3}{+lshift}
{kp-X}>{speed9}{-lshift}{6}{+lshift}
[kp-C]>[obrack]
[kp-V]>[cbrack]
{kp-B}>{speed9}{-lshift}{`}{+lshift}
 

** right side **
****************

{kpmin}>{speed9}{-lshift}{8}{+lshift}

[kp-H]>[left]
[kp4]>[down]
[kp5]>[up]
[kp6]>[right]

{kp-N}>{speed9}{-lshift}{hyphen}{+lshift}
[kp1]>[hyphen]
[kp2]>[=]
{kp3}>{speed9}{-lshift}{5}{+lshift}

******************
** browser mode **
******************

** previous tab
{kp-Y}>{speed9}{-lwin}{-lalt}{left}{+lwin}{+lalt}

** close tab
{kp7}>{speed9}{-lwin}{w}{+lwin}

** new tab
{kp8}>{speed9}{-lwin}{t}{+lwin}

** next tab
{kp9}>{speed9}{-lwin}{-lalt}{right}{+lwin}{+lalt}

** search
{kp-\}>{speed9}{-lwin}{f}{+lwin}

** copy url
{f9}>{speed9}{-lwin}{l}{+lwin}{-lwin}{c}{+lwin}{escape}

*****************
** misc & apps **
*****************
** somehow the hyper token doesn't work, so we have to manually type the hyper combination

** terminal
{numlk}>{speed9}{-lwin}{-lctrl}{-lalt}{-lshift}{1}{+lwin}{+lctrl}{+lalt}{+lshift}

** browser
{kp=}>{speed9}{-lwin}{-lctrl}{-lalt}{-lshift}{2}{+lwin}{+lctrl}{+lalt}{+lshift}

** slack
{kpdiv}>{speed9}{-lwin}{-lctrl}{-lalt}{-lshift}{3}{+lwin}{+lctrl}{+lalt}{+lshift}

** lock
{scroll}>{speed9}{-lwin}{-lctrl}{-lalt}{-lshift}{4}{+lwin}{+lctrl}{+lalt}{+lshift}

** screenshot
{end}>{speed9}{-lwin}{-lctrl}{-lalt}{-lshift}{5}{+lwin}{+lctrl}{+lalt}{+lshift}

** alfred
{home}>{speed9}{-rwin}{-space}{+rwin}{+space}

** dash
{pdown}>{speed9}{-lwin}{-lctrl}{-lalt}{-lshift}{6}{+lwin}{+lctrl}{+lalt}{+lshift}
```

How to change qwerty.txt:
```
Mount the v-drive with progm + F1
Make changes to the qwerty.txt file (don't forget to save it)
Reload file with progm + F3, check if everything works fine
Unmount file with diskutil unmount /Volumes/ADVANTAGE2/
Disconnect from v-drive by pressing progm + 1 again.
```

