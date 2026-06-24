# UPDATES
I do NOT need to beat it in preview! Beta works for preview!

Beat it in stable! If it helps here is vulkan info for stable:

(deck@steamdeck ~)$ vulkaninfo | grep -i "apiVersion"
        apiVersion        = 1.3.296 (4206888)
(deck@steamdeck ~)$ 

beta:

(deck@steamdeck ~)$ vulkaninfo | grep -i "apiVersion"
        apiVersion        = 1.4.330 (4211018)
(deck@steamdeck ~)$ 

Maybe THAT'S why it wasn't working...

# Luigi-s-Mansion-2-Dark-Moon-Azahar-Emulator-Vulkan-Shader-Cache
I am not affiliated with Azahar or Nintendo. You need the orginal game to use this. Luigi's Mansion 2 Dark Moon is very difficult to emulate, because it has to render tens of thousands of shaders *per room*. Therefore, I beat the game on vulkan and copied the full cache files!! On steam deck but it might work on Windows or android I don't know. 

I beat the game using Vulkan, but I plan to beat the game 4 times, twice on Vulkan, and twice on OpenGL. Then the cache will have both.

Download here:

[Vulkan 1.3](https://github.com/PhoenixStormJr/Luigi-s-Mansion-2-Dark-Moon-Azahar-Emulator-Vulkan-Shader-Cache/releases/download/release2/Luigi.s.Mansion.2.Azahar.Vulkan.Shaders.Cache.Stable.zip)

[OpenGL_Stable](https://github.com/PhoenixStormJr/Luigi-s-Mansion-2-Dark-Moon-Azahar-Emulator-Vulkan-Shader-Cache/releases/download/opengl1/Luigi.s.Mansion.2.Dark.Moon.Open.GL.shaders.zip) (Probably doesn't work)

(WARNING for Beta you need to CHECK the disable optimize spirv cache, because I was an idiot the first time around and didn't know any better, now it's stuck. I won't do it again until Beta moves into Stable. I'm moving into Open GL.)

# DISCLAIMER:
I am not affiliated with Azahar, not a developer. You MUST have the original legally dumped from YOUR OWN 3DS game to use this! (Literally this won't work without the ROM, it's just the cache to speed up the LEGALLY DUMPED GAME!! It will NOT run by itself!!!)

# Setup:

I dumped my game Luigi's Mansion Dark Moon (USA) (En, Fr, Es).cci. I can't make the shaders for the 3ds file because I didn't buy it. I don't know if these will work for the 3ds file or not. I am not buying another copy of the game in a different format, JUST FOR SHADERS.

(This is how I made the shaders. You might be able to ignore some of these for speed, I'm not sure. Try whatever, experiment.)

Right click the game -> properties

Under System:

CHECK "Enable New 3DS mode". Makes it faster, doesn't affect cache

UNCHECK "Use LLE applets" Again, specific to your device, but not to mine. You can check it if you need online, but it may not work. I dunno.

Under Enhancements:

Internal Resolution: (set to whatever) but I set mine to 3x and then tried lowering it, still used the old shaders.

UNCHECK Use Integer Scaling. It doesn't matter at all.

CHECK "Enable Linear Filtering". It's very fast, and standard.

Texture Filter: NONE. Faster and doesn't change shaders.

CHECK Disable Right Eye Rendering. Eye to render, Left Eye (default) Makes it faster. Barely affects shaders.

Swap Eyes OFF. It does nothing that I can tell...

(nothing under utility matters.)

Layout: My layout is X position: 0, Y position: 0, Width: 1280, Height: 650, X position: 565. Y position: 650, Width: 150, Height: 150. But you can do whatever.

Under Graphics:

Graphics API: Set to Vulkan. (Eventually I'll make OpenGL shaders, but until then, Vulkan)

CHECK SPIR-V shader generation. (THE MOST IMPORTANT LITERALLY!!!)

UNCHECK Disable GLSL -> SPIR-V optimizer. This makes the shaders compile "faster" BUT makes them specific to YOUR device, not generic. (This is how I messed up the first time.) They also probably won't work without this unchecked. Also after compiled, they run the same speed.

CHECK Enable hardware shader. Just do it. DO. IT. Or don't, and see what happens...

UNCHECK "Accurate multiplication". This doesn't even affect shaders at all. It just slows the game down.

CHECK "enable async shader compilation". I UNCHECKED it, because it makes shaders more accurate, but you should CHECK it for faster gameplay.

CHECK "enable async presentation". Makes it faster and I noticed no input lag.

Texture Sampling: Application controlled. Default.

DEFINITELY CHECK "use disk shader cache" BECAUSE THIS IS HOW IT LOADS THE FILES I UPLOADED!!!

CHECK "Enable VSync". It increases performance but doesn't affect shaders.

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

UNCHECK Force deterministic async operations. I DON'T know what I'm doing so it's staying off cuz it told me to.

I have no idea about cheats.




I use a steam deck LCD. I got the files from here:

Vulkan:

/home/deck/.local/share/azaharplus-emu/shaders/vulkan/pipeline/0004000000055F00-1002163F.bin

/home/deck/.local/share/azaharplus-emu/shaders/vulkan/transferable/0004000000055F00_fs.vkch

/home/deck/.local/share/azaharplus-emu/shaders/vulkan/transferable/0004000000055F00_gs.vkch

/home/deck/.local/share/azaharplus-emu/shaders/vulkan/transferable/0004000000055F00_pl.vkch

/home/deck/.local/share/azaharplus-emu/shaders/vulkan/transferable/0004000000055F00_vs.vkch

OpenGL:

/home/deck/.local/share/azaharplus-emu/shaders/opengl/precompiled/separable/0004000000055F00.bin

/home/deck/.local/share/azaharplus-emu/shaders/opengl/transferable/0004000000055F00.bin

version of emulator Azahar 2125.1.1
