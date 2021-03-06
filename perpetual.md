#Perpetual
This morning I saw an interesting tweet from [Bryan Veloso](http://avalonstar.com):

>Say hi to my first @dribbble in a -very- long time. Introducing Perpetual (a music app idea): 
[http://t.co/e3YNNoop](http://t.co/e3YNNoop)

The idea was awesome, the UI gorgeous and the app something I really would want to use myself. That didn't seem likely to happen soon, since the dribbble post ended with:

> Sigh, one day I'll build this... or get somebody to help me build it. (o^_^)b

Lately I've been looking for motivations to sit down and learn some more Objective-C/Cocoa. When you want to learn a new language it really helps to have a real goal to work against instead of just following yet another tutorial. So I thought, "why not?" and fired up XCode.

During my lunch break I hacked together a quick prototype and this evening I finished up this basic version:

![Perpetual.app](http://i.imgur.com/xNpY8.png)

You basically load up a song, set the start and end markers and press play. The player will start at the beginning of the sond and when it reaches the end marker it will start over at the start marker.

The positive response made me really excited about this and I can't wait to continue working on it.

The next step is to figure out how to extract metadata from the music file and hopefully find a way to show some sort of cover image. After that, I'll try to implement the sweet-looking UI Bryan made.

You'll find the repo at [https://github.com/revyver/perpetual](https://github.com/revyver/perpetual) 