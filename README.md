# Transfer

Max for Live device for easy, real-time timbre transfer in Ableton Live using [RAVE](https://github.com/acids-ircam/RAVE).

## Requirements

- ``nn~ v.1.5.6`` external: <https://github.com/acids-ircam/nn_tilde/releases/tag/v1.5.6>

**Note: most recent ``nn~ v.1.6.0`` release is not supported!**

## Quick start

- Download/clone this repo. For ``transfer.amxd`` to appear in ``Max for Live/Max Audio Effects`` in Ableton, on MacOS you can run:

```bash
git clone https://github.com/wwerkk/transfer-m4l.git ~/Music/Ableton/User\ Library/Presets/Audio\ Effects/Max\ Audio\ Effect/transfer
```

- Add the repo directory to the Max Path via ``Options/File Preferences``.
- Download the nn~ Max MSP release appropriate for your system and put it somewhere in your Max path, ie. this repository.
- Drop the M4L device as an audio effect on any channel you like.
- Hit the *Download* button to automatically download some of the [pre-trained models made available by kind people of IRCAM](https://acids-ircam.github.io/rave_models_download).
- After download is finished, the menu on top of the patch should automatically populate with four models.
- Pick the model you want to use.
- Turn up the Wet gain.
- Use as you would use a regular audio effect.
- Values in each latent dimension can be scaled and offset using the multisliders. The menu below offset controls wavefolding settings in case your latent values go out of set range.
- Latency of the output can be reduced by changing the *Buffer size* setting to 0. This is pretty CPU heavy, so you might have to trade-off by increasing the global buffer size in Ableton Preferences.

## Adding your own models

You can add your own models by dropping them into the ``nn_models`` subdirectory, or replacing it with a symlink to a directory of your choice containing the models.
Hit ``Refresh`` to repopulate the umenu.

## Saving

To set your chosen model folder to load up on start, open the patcher in Max, add the directory as described above and save the patcher.
Multislider settings should save automatically with your Ableton project.

## Note

This is a work in progress, so feel free to open up issues for any bugs encountered or features you'd like to see. Feedback from Windows users is especially appreciated, since I don't have any means of testing on that platform.

## Demo

Coming soon!
