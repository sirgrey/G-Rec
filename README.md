----------------
# What is G-Rec?
----------------

G-Rec is a simple 2 button system for recording demos that uses the built-in scripting system for TF2. Unlike p-rec, this is just a set of scripts, so it won't be broken by Valve updates.

Whenever you think you've been recording for long enough and want to start a new recording, you can either use the key you've bound to keep to keep the demo, or the key to dump the demo.

My personal recommendation is that you dump every life that you don't do anything interesting in. G-Rec automatically writes over the previously recorded demo when you dump a file.

By dumping every life that is boring, you keep your demo files short and only keep the most interesting lives, making finding the interesting stuff you did significantly easier as you will only have to search through one life.

Alternatively, you can simple type the word dump into your default.cfg and this will automatically dump the file when you respawn and you simply need to press the "keep" key when you do something interesting, similar to how the p-rec mark system works.

**WARNING** - Auto-dumping every life will interfere with p-rec as it will stop whatever p-rec is recording and start its own file instead. I do NOT recommend using this method if you use p-rec. 
**WARNING** - TF2 will also sometimes re-execute default.cfg when you lag out, so if you have issues with latency, this may cause you to over-write files you wanted to keep when you lag out.

Use your own discretion when deciding how to use G-Rec.

----------------
# Simple vs Full
----------------

The "Simple" installation is slightly simpler and shorter and all demos will start with grec_ which can be slightly more difficult to search through.

The "Full" installation will take a small amount of extra time and effort, however it will prepend your files with the class that you were playing when you STARTED recording, which can make searching for your demos easier. 

It is worth noting that the full installation will number things in a continuous manner, so if you record sniper_001a and keep that file and then switch to soldier, the next file will be called soldier_001b rather than soldier_001a. 

This is to do with limitations in the scripting engine and cannot be fixed.

----------------
# Labelling system
---------------- 

The G-Rec system labels using numbers and letters. I personally find that remembering where I am in a sequence, letters are easier to remember than numbers so I designed this accordingly.

You will start with grec_01a then grec_01b, grec_01c, grec_01d etc.

After grec_01z it will roll over to grec_02a. 

If you ever wonder what your most recent recording number/letter is - just type grec into console and it will tell you.

The G-Rec system is only set up to record up to 500 demo files. When you hit grec_20a, I recommend archiving all your old grec files as it will rollover and start from the beginning again.

----------------
# WARNING
----------------

If you have ever MANUALLY written stuff into config.cfg, there is a chance this will mess with that stuff (it definitely will if you have written the "alias" command or if you have written the "exec" command into config.cfg).

If you have put stuff into config.cfg, I recommend moving it to default.cfg.

If you have NOT written into config.cfg, or do not HAVE config.cfg then this does not apply to you.

If you have unbindall written into your config anywhere that it gets executed - this will screw up g-rec.

Use the keep/dump key whenever you have a map change or you change server to not be disappointed when things are missing.

You have been warned.

----------------
# INSTALLATION
----------------

Pre-installation:
1. Choose whether you're going to use the simple or full version of G-Rec.
2. Choose which keys you want to bind the "Keep" and "Dump" commands to.

a) Simple installation:

1. Copy g_rec_simple.cfg to your cfg folder
2. Open default.cfg - if this does not exist, you can create it by making a new document in notepad++ and saving it as default.cfg instead of default.txt
3. Paste exec g_rec_simple
4. Save default.cfg
5. Open g_rec_simple.cfg
6. Find and replace keepkey and replace it with the key you want to bind it to to KEEP the demo you just recorded.
7. Find and replace dumpkeyand replace it with the key you want to bind it to to DELETE AND RECORD OVER the demo you just recorded.
8. Open TF2 and type start_grec into console. (Note: you only need to do this the FIRST time you open 
9. Join a server. Start recording by pressing your keep key. Congrats, you are now using g-rec!
10. If you want to simply stop recording, you can just type stop into console. You can then use the dump or keep keys to 

You can now use G-rec.

a) Full installation:

1. Copy g_rec.cfg & the g_rec folder to your cfg folder.
2. Open default.cfg - if this does not exist, you can create it by making a new document in notepad++ and saving it as default.cfg instead of default.txt
3. Paste exec g_rec
4. Save default.cfg
5. Open the g_rec folder.
6. Open every .cfg file in turn and follow steps 7 & 8, using the same keep and dump keys.
7. Find and replace keepkey and replace it with the key you want to bind it to to KEEP the demo you just recorded.
8. Find and replace dumpkeyand replace it with the key you want to bind it to to DELETE AND RECORD OVER the demo you just recorded.
9. Open all the different class .cfg files in the cfg folder and paste in their respective g_class names listed here:

g_scout
g_soldier
g_pyro
g_demo
g_heavy
g_engineer
g_medic
g_sniper
g_spy

10. Open TF2 and type start_grec into console.
11. Join a server. Start recording by pressing your keep key. Congrats, you are now using g-rec!