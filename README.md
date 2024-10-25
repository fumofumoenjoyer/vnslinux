# vnslinux

Original reddit post [Here](https://www.reddit.com/r/visualnovels/comments/mga4d6/tutorial_how_to_run_any_visual_novel_on_linux/) i created this repo for safekeeping purposes, credits to the original writer.

 [tutorial] How to run any visual novel on Linux (pretty much)

In this mini post I'll try to explain how you can run almost any visual novel in Linux with a native Japanese locale, since this topic is hard to find newbie-friendly on Google.If you already know how to play windows games on Linux, about Vulkan and stuff, and you're looking up for Japanese locale on Linux then jump to the second section.
The basics - Setting the environment [Vulkan/Wine/Lutris]

If you're new in this Linux world, then you must know that we'll be playing this VN by emulating them in Wine. This is not a tutorial of how to install Wine and it depends on your distro, search on YouTube if the case. However, Wine is not enough by itself to run any VN you like. Yeah, you'll be able to run some VN, but some others will just crash or have poor emulation. You need to install dependencies to make it compatible, and this post teach you how to do that: WineDependencies at master - lutris/docs - GitHub Follow the steps depending on your distro

Make sure to have installed the drivers for your graphic card to get a real better performance on heavy VN. I recommend to install Vulkan (it's a 3D graphics and compute API) if your computer is compatible. Again, here you have the steps to follow, but keep in mind that packages changes on Intel, NVIDIA or AMD. InstallingDrivers at master - lutris/docs -GitHub

Last but not least, I recommend to install Lutris to have all your VN beautifully placed in one single hub. Also, it allows you to add cool stuff as environment variables much easier than launching from terminal (like gamemode, or changing the locale for an specific process).About this gamemode thing, is not necessary to install it at all. But if you have a low-end PC like me, then it'll definitely make a difference on performance in games like Nekopara (well, at least for me). Here a YouTube Video explaining what it is and how to install it: How to use Gamemode in Linux - Chris Titus Tech on YouTube. Extra tip: first run winecfg before trying to run any game. That will set it up all from once.
Setting your Linux to have native Japanese locale

Beside some Japanese fonts, we don't have to install anything on this step. As I said, it's natively.

Let's go to the point: open a terminal, type sudo nano /etc/locale.gen and uncomment the line jp_JP-UTF-8 and save and exit. Then regenerate your locales typing sudo locale-gen.(I think you can do this on GUI if you like KDE, Gnome or so, but I've never tried from there)

Now that you have Japanese locale active on your system, you're able to run programs with a Japanese coding by just adding LANG="ja_JP.UTF-8" before typing the program's name on terminal.Ex. LANG="ja_JP.UTF-8" wine clannad.exe will Launch Clannad running in a Japanese coded wine.
Extra tips and notes

   I could be a lil bit annoying to be launching your games from terminal and having to copy/paste this env variable of JP locale. So that's why I recommended Lutris. When you add your game to library, just go to System Options tab and scroll down to Environment Variables. There you can add LANG and ja_JP.UTF-8 to the game which need it.

   Before launching any game check if you have to install any custom fonts. If so, then don't install it on your Linux (lol), but simply copy it to ~/.wine/drive_c/windows/Fonts/. Or use winetricks.

   Some novels doesn't need the JP locale added to run, so try launching the game normally and if crashes or doesn't load well, then try with locale. I'll add two examples at the end of this post.


