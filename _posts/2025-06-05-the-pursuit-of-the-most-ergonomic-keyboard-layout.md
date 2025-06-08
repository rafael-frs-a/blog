---
layout: post
title: "The pursuit of the most ergonomic keyboard layout"
date: 2025-06-05
author: rafael-frs-a
---
## The main story

The year was 2017, and I started to feel a constant ache in my right-hand pinky finger while coding. I figured it was due to stretching it too much when pressing "P" on my keyboard, so I thought I could solve it by adjusting the resting position of my right hand. No success. I then recalled something a friend had told me a couple of years earlier about moving from [QWERTY](https://en.wikipedia.org/wiki/QWERTY) to a different keyboard layout called [Dvorak](https://en.wikipedia.org/wiki/Dvorak_keyboard_layout). That QWERTY was made to purposefully have the frequently used keys far from each other, because, back in the day, pressing two nearby keys on a typewriter too fast could cause them to stick (I have a vague memory of that happening to me as a child when I had the opportunity to play with one), which made it anti-ergonomic. Since modern keyboards don't have that problem, ergonomic layouts are actually usable now.

I naturally followed the programmer's spirit of spending ten hours to automate a ten-minute task and decided to start a whole project to solve my pinky discomfort. In my Windows environment, I switched from ABNT2 (a QWERTY-based Brazilian keyboard layout) to Dvorak and began relearning how to touch-type on it. After a whole week, I came to the conclusion that I hated it. It was too different, and the position of some keys I used the most didn't feel optimal to me.

I then thought that maybe that wasn't the best layout for me, so I decided to search for alternatives. I found [this](https://www.patrick-wied.at/projects/heatmap-keyboard/) website, which generates a heatmap of the most-used keys on a selected layout given a text input, supporting many options, including QWERTY and Dvorak. I just wasn't exactly sure which keys I used the most, both at home and at work.

I spent more time creating a keylogger app. It captured everything I typed and appended it to a `.txt` file. I then copied the captured text and fed it as input to the keyboard heatmap website. In case you're thinking, "Hmm, they could get passwords from this," the heatmap feature works offline; it is [open-source](https://github.com/pa7/Keyboard-Heatmap), and there are other ways to prevent that from happening. I'm not saying I thought about that at the time.

After a week of experimenting, I found two keyboard layouts where my most-used keys/characters were centered and grouped together: Colemak and Asset. [Colemak](https://en.wikipedia.org/wiki/Colemak) is more popular, with many operating systems already including it as an option, but it still seemed too different. [Asset](https://millikeys.sourceforge.net/asset/) was more obscure, but one thing caught my attention: it looked much more similar to QWERTY, so I decided to give it a try. There was just one issue: it wasn't a built-in option on Windows.

I searched for a way to install it on Windows and found about Microsoft Keyboard Layout Creator (MSKLC). It allows you to define the characters you want on each physical key, generating a `.klc` text file. You can also manually modify that file to include keys not present in its UI, like `ABNT_C1`. Then you can generate a `setup.exe` installer from it, install, and select the layout in your keyboard configuration.

My most used characters were finally centered; the "P," even though not centered, was moved to a stronger finger, and the pain in my pinky was gone.

## Further improvements

After a few days, I started nitpicking Asset. It moved "P" from the pinky finger to the index finger and "U" from the index finger to the middle one. I used both letters equally and both fingers are relatively strong, so I thought I could swap "P" and "U," moving the latter to its original position and making it even closer to QWERTY. I also had a similar thought about "J" and "K," where I could swap them to move "J" back to its original finger, even though it was not centered. After a few iterations, I ended up with the following layout that I use to this date.

![keyboard](https://github.com/user-attachments/assets/ccebbef8-6033-49b3-804c-f396092a084f)

## Experiences with other OSes

I had a short experience with macOS and Linux after I started using my custom layout. To be able to use it on those OSes as well, I had to search for different ways to install it. For macOS, I found an app similar to MSKLC called [Ukulele](https://software.sil.org/ukelele/). Linux was a bit more complicated, and I had to create a script to run at startup and swap the key mapping to match the keys' positions.

## Takeaways

I believe changing to a more ergonomic keyboard layout was definitely a good thing. It clearly solved the issue with my finger, and it also improves overall quality of life. My typing speed didn't change, though; it's still about the same WPM as when I used QWERTY, with the difference that I have to move my fingers less now.

One funny finding is that having a custom keyboard layout installed on your computer discourages other people from using it, even experienced programmers who know how to switch that. Whether that's a good thing or not is entirely personal and contextual.

This also doesn't come without downsides. If you don't keep practicing QWERTY, you eventually forget how to touch-type on it, so using someone else's computer, which will probably have that configuration, might be an issue. Fortunately for me, I've rarely needed to type on a computer without my custom layout over these years, so I still think it was worth it.

## Assets

You can find the `.klc` file I used [here]({{ "/assets/assetp.klc" | absolute_url }}).
