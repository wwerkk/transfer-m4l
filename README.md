# Transfer

Max for Live device meant for making it easier to run timbre transfer in Ableton Live using real-time neural network models.

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
- Hit the *Download* button to download some of the [pre-trained RAVE models made available by kind people of IRCAM](https://acids-ircam.github.io/rave_models_download).
- The menu on top of the patch should automatically populate with available models.
  
## Use

- Pick the model you want to use.
- Turn up the Wet gain (it's all the way down by default for safety reasons!).
- ???
- Profit.

### Hints

- Values in each latent dimension can be scaled, offset and modulated with noise using the multisliders.
- The menu below offset controls wavefolding settings in case your latent values go out of set range.
- Latency is unavoidable, but can be reduced by changing the *Buffer size* setting to 0. This is pretty CPU heavy, so you might have to trade-off by increasing the global buffer size in Ableton Preferences.

## Adding your own models

You can add your own models by dropping them into the ``nn_models`` subdirectory, or replacing it with a symlink to a directory of your choice containing the models. Hit ``Refresh`` to repopulate the umenu.

## Saving state

The current model and slider state should correctly save with the Live Set and device presets.

**Warning:** due to how Max and Ableton interact, opening up the patcher (``Edit in Max``) seems to initialise a new copy with the default state, meaning any edits will also need to be saved as a separate ``.amxd`` file.

## Note

This is a work in progress, so feel free to open up issues for any bugs encountered or features you'd like to see. Feedback from Windows users is especially appreciated, since I don't have any means of testing on that platform.

## Demo

A proper one is due at some point.
A less proper video of simple jamming can be found on [my YouTube](https://www.youtube.com/watch?v=mzVxCmxmQBg).

---

More RAVE models are available from:

- [IRCAM ACIDS](https://acids-ircam.github.io/rave_models_download)
- [Intelligent Instruments Lab](https://huggingface.co/Intelligent-Instruments-Lab/rave-models/tree/main)
