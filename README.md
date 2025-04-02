# Funkin' Replay Mod

An FNF Mod that Records your Inputs during gameplay and stores them in a Replay File.

## How does the mod work?

Upon loading the mod, a new `replays` folder is created, if one wasn't provided already. This is where the replay files will be stored.

> [!NOTE]
> If you had used this mod in its initial version, all your replay files (suffixed with `.rep`) will be converted to the newer format (suffixed with `.fnfr`).

Every keyboard input that you make during the gameplay after the countdown start will be stored in a .json file. Additionally, at random point during your gameplay, a screenshot will be taken to serve as a preview image for your replay in the replay viewer menu.

> [!IMPORTANT]
> Any keyboard inputs happening before or after initial gameplay, such as pressing the `ACCEPT` keybind during Dialogue, will **NOT** be saved!
> Replays also may not be fully accurate due to lag spikes or rounding errors, as the inputs are registered based on Conductor's `songPosition` variable.

Once the song ends, your replay data and your replay preview image will be saved in the `replays` folder with a file with a `.fnfr` file extension. These files are similar to the `.fnfc` or `.fnfs` files, in a sense that they are essentially renamed `.zip` files. You can later view this replay, alongside your previous ones in the Replay Viewer menu, which could be accessed by pressing `G` in the Main Menu.

> [!NOTE]
> This works with modded songs as well! 

## What about the Replay Viewer Menu?

The Replay Viewer Menu is similar design-wise to the Debug Menu, you know, the one where you choose the editors? Yeah, that one.
There are a couple of differences though, namely the background is orange, the text font is different and additionally there is some information about the gameplay from the replay as well as the corresponding replay preview image displayed to the right. The aforementioned information features the full song name and its difficulty, when the replay was taken as well as some tallies like score, total notes hit etc.

> [!NOTE]
> Putting replay files directly in the `replays` folder will **NOT** make them be listed in the menu, as currently there isn't a way to read a folder's content using hscript.

To navigate through the menu, use the `UP` and `DOWN` arrows or your mouse's scroll wheel.

Some additional keybinds that could be used in the menu:
* `F2` - Pressing this allows you to rename the currently selected replay to whatever you wish for. Duplicate names are accounted for!
* `Del` - One may think this deletes the replay. However, hscript currently doesn't allow for file deletion, so instead this takes you to the exact location of the replay file. Delete it yourself and pretend the `Del` keybind did it lol
* `Enter` - Aside from viewing replay, if you're currently typing a replay's name, this stops the typing process and saves the custom name for the replay.

> [!IMPORTANT]
> The replay will not play if the song could not be found, which could happen if the modded song from the replay gets its mod disabled. This is an *input* recording mod, not a *video* recording mod, after all!

# Closing

Thank you for downloading the mod! If you encounter any issues or have a suggestion, do not hesitate reporting to the [GitHub Page](https://github.com/KoloInDaCrib/ReplayModVSlice)! 