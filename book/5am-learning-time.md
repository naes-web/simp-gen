# First Attempt at Personal Blog Engine with Scala (*Never Done Either Thing...*) 

So, it is currently 0230, I can't sleep and I've stumbled across a blog post (https://www.lihaoyi.com/post/ScalaScriptingandthe15MinuteBlogEngine.html) from 2016... 
![[Pasted image 20231120023934.png]]

I have little idea what Scala is, beyond it's a language used for stuff above my head. But what got me hooked was the first subtitle of the blog post, "Serious Business". I'm all about business time, so lets give this a go.

I'll be writing this in bits and pieces as I work through the instructions in the blog post, until either:
1) The sun rises
2) I finish it
3) I break
4) I fall asleep (least likely)

## Serious Business Time

So. It would seem Scala is used for very large complex systems, Like Apache Spark and Kafka. I know nothing about either of these things, as I just use Nginx to serve static HTML like all serious business professionals. Regardless, Scala is used for distributed systems, ML, "**Serious Business**". Some remarks from Mr Haoyi regarding Scala and why it's so damn good at serious business include quote:

- "Relatively high-performance on the high-performance JVM runtime makes your web-scale or big-data Serious Business complete faster."  
- "Type-safety makes sure you don't make careless mistakes when doing your very-important Serious Business."
- "Good tools for abstractions (inline-functions, implicits, typeclasses) means you can manage the complexity of your Serious Business and keep it from getting out of hand."

![[Pasted image 20231120025850.png]]

After that, the author of the blog post explains the pitfalls in a few other solutions to running Scala scripts and tells us to *use his tool instead*. Not that I am in any position to argue! (I will note, all the links on the blog 404, here take this! https://ammonite.io/ + https://github.com/com-lihaoyi/Ammonite).

## Hurdle 1 - Installing JVM for Ammonite

So we are going to need a JVM (Java Virtual Machine) in order to get Ammonite running. I haven't got that on my system right now, so I'll document my process following the Arch Wiki page for Java.

Arch seems to officially support OpenJDK in 3 different flavours:
1) Headless JRE - (*Halloween Special Episode?*)
2) Full JRE
3) JDK
- *Along with docs and source code*

They seem to depend on each other bottom to top, so I'm going to install the full JDK with:
	`pacman -S jdk-openjdk`
It comes out around 1138MB installed

If you use Arch too (btw), the packages I just installed came with a cool command for switching between different JVM called `archlinux-java`, so now if we pass the argument `get` to that command, it'll print our JVM!:
	```
```
	archlinux-java get
	java-21-openjdk
```

## Futile Effort 

I only know Scala by name, so I didn't have it installed. Checked it out and it's got a package on the AUR. So I start building it, only to realise it's got JVMs as dependencies. Ah well, maybe it was a good thing to install them first? I'm not versed enough to say either way. I will likely have to change the JVM I'm running after I build Scala, we shall see. Let's continue to follow this nearly decade old set of instructions! 

## Installing Ammonite - Calm, Relaxed, Unbothered, Moisturised 

Looks like a lot of the URL specific commands listed in that tutorial arent going to cut it, 404. I still want to see how far I can go with it and I've managed to piece some bits together from the authors newer stuff. For example, this (https://ammonite.io/#ScalaScripts) is the new site with all the stuff about his Ammonite tool, including the updated command to install it for the latest version of Scala (or something like that, its 0415. I got sidetracked trying to make screenshots work on Wayland).

According to the ancient texts, all we need to do is write our Scala script, save it as `.sc` and then run it with `amm <ur-script>.sc`. Let's give it try with something really unique!!!![[20231120_04h28m38s_grim.png]]

# **SO WHAT HAVE WE LEARNED**
1) Do not follow piecemeal instructions from 9 years ago.
2) Especially do not start the above at 0230
3) I just realised Scala Scripts are build into Scala now (or something? (at least I know something about Scala now!))

I will maybe come back and revisit this, if I remember about it. If not at least I learned a few things from the experience like, How to install and configure my JVM on Arch and a little bit more about Scala than just the name. 

Ultimately. It's fun for me to do stuff like this, bang my head off something and type it out "stream of consciousness" style. I think I'll try and keep doing it, maybe I'll learn something of value someday (lol).
