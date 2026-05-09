# UPDATES
hm... this might only work on Beta branch. I'll make another on stable. I was only on Beta to get a feature I really wanted THEN but now it's on stable. I'll also try to make the shaders more "portable" this time.

# Luigi-s-Mansion-2-Dark-Moon-Azahar-Emulator-Vulkan-Shader-Cache
I am not affiliated with Azahar or Nintendo. You need the orginal game to use this. Luigi's Mansion 2 Dark Moon is very difficult to emulate, because it has to render tens of thousands of shaders *per room*. Therefore, I beat the game on vulkan and copied the full cache files!! On steam deck but it might work on Windows or android I don't know. 

I beat the game using Vulkan, but I plan to beat the game 4 times, twice on Vulkan, and twice on OpenGL. Then the cache will have both.

Download here:

https://github.com/PhoenixStormJr/Luigi-s-Mansion-2-Dark-Moon-Azahar-Emulator-Vulkan-Shader-Cache/releases/tag/release

# DISCLAIMER:
I am not affiliated with Azahar, not a developer. You MUST have the original legally dumped from YOUR OWN 3DS game to use this! (Literally this won't work without the ROM, it's just the cache to speed up the LEGALLY DUMPED GAME!! It will NOT run by itself!!!)

# Setup:

I dumped my game Luigi's Mansion Dark Moon (USA) (En, Fr, Es).cci. I can't make the shaders for the 3ds file because I didn't buy it. I don't know if these will work for the 3ds file or not. I am not buying another copy of the game in a different format, JUST FOR SHADERS.

(This is how I made the shaders. You might be able to ignore some of these for speed, I'm not sure. Try whatever, experiment.)

Right click the game -> properties

Under System:

UNCHECK "Enable New 3DS mode". Although this option speeds it up, it makes the shaders LESS "generic" meaning they're specific to YOUR device, not mine.

UNCHECK "Use LLE applets" Again, specific to your device, but not to mine. You can check it if you need online, but it may not work. I dunno.

Under Enhancements:

Internal Resolution: (set to whatever) but I set mine to 3x and then tried lowering it, still used the old shaders.

UNCHECK Use Integer Scaling. It doesn't matter at all.

CHECK "Enable Linear Filtering". It's very fast, and standard.

Texture Filter: NONE. Faster and doesn't change shaders.

UNCHECK Disable Right Eye Rendering. For shaders of right and left eyes. Again, this makes it more "standard" but slower. More likely to be compatible.

Swap Eyes OFF.

(nothing under utility matters.)

Layout: My layout is X position: 0, Y position: 0, Width: 1280, Height: 650, X position: 565. Y position: 650, Width: 150, Height: 150. But you can do whatever.

Under Graphics:

Graphics API: Set to Vulkan. (Eventually I'll make OpenGL shaders, but until then, Vulkan)

CHECK SPIR-V shader generation. (THE MOST IMPORTANT LITERALLY!!!)

UNCHECK Disable GLSL -> SPIR-V optimizer. This makes the shaders work "faster" BUT makes them specific to YOUR device, not generic. (This is how I messed up the first time.) They also probably won't work without this unchecked.

CHECK Enable hardware shader. Just do it. DO. IT. Or don't, and see what happens...

UNCHECK "Accurate multiplication". This doesn't even affect shaders at all. It just slows the game down.

UNCHECK "enable async shader compilation". Because we want as many shaders as possible, and this sometimes skips them! Also... I have all the shaders here so this is literally useless.

UNCHECK "enable async presentation". Maybe?... It makes it slower but I don't know if it breaks it.

Texture Sampling: Linear. This is the "standard" option and pretty fast!

DEFINITELY CHECK "use disk shader cache" BECAUSE THIS IS HOW IT LOADS THE FILES I UPLOADED!!!

UNCHECK "Enable VSync". It increases performance and makes the shader generation smoother. 

Delay application render thread: around 2 ms is best for speed for me.

Audio:

CHECK enable audio stretching

UNCHECK Enable realtime audio

Anything else besides that for audio, and the game will literally scream at you.

Debug:

CPU set clock speed 100% default

UNCHECK "Enable debug renderer" no extra information!!!

UNCHECK "Dump command buffers" it doesn't affect shaders at all

UNCHECK "Delay app start for LLE module initialization" it doesn't affect shaders at all.

CHECK Force deterministic async operations. Meaning if we perform the same action (like catching a ghost) it should give us the SAME shader. This is the only async thing that should be clicked.

I have no idea about cheats.




I use a steam deck LCD. I got the files from here:

/home/deck/.local/share/azaharplus-emu/shaders/vulkan/pipeline/0004000000055F00-1002163F.bin

/home/deck/.local/share/azaharplus-emu/shaders/vulkan/transferable/0004000000055F00_fs.vkch

/home/deck/.local/share/azaharplus-emu/shaders/vulkan/transferable/0004000000055F00_gs.vkch

/home/deck/.local/share/azaharplus-emu/shaders/vulkan/transferable/0004000000055F00_pl.vkch

/home/deck/.local/share/azaharplus-emu/shaders/vulkan/transferable/0004000000055F00_vs.vkch

version of emulator Azahar 2125.1.1
