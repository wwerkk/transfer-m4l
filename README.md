# Transfer
Max for Live device for easy, real-time timbre transfer in Ableton Live using [RAVE](https://github.com/acids-ircam/RAVE).
## Requirements
- ``nn~`` external: https://github.com/acids-ircam/nn_tilde/
## Quick start
- Download/clone this repo. For ``transfer.amxd`` to appear in ``Max for Live/Max Audio Effects`` in Ableton, on MacOS you can run:
```
git clone https://github.com/wwerkk/transfer-m4l.git ~/Music/Ableton/User\ Library/Presets/Audio\ Effects/Max\ Audio\ Effect/transfer
```
- Download the nn~ version compatible with your system and put it somewhere in your Max path, ie. the folder of this repository.
- Drop as an audio effect on any channel you like.
- Hit the *Download* button to automatically download [pre-trained models made available by kind people of IRCAM](https://acids-ircam.github.io/rave_models_download).
- After download is finished, the menu on top of the patch should automatically populate with four pre-trained models (note: ``darbouka_onnx`` is not compatible).
- Pick the model you want to use.
- Turn up the Wet gain.
- Use as you would use a regular audio effect.
- Values in each latent dimension can be scaled and offset using the multisliders. The menu below offset controls wavefolding settings in case your latent values go out of ``[-4, 4]`` range.
- Latency of the output can be reduced by changing the *Buffer size* setting to 0. This is pretty CPU heavy, so you might have to trade-off by increasing the global Ableton buffer size.
## Adding your own models
You can add your own models by clicking *Browse* and picking the directory where your models are located, or simply put them into the folder of the repo and hit the *Default* button to automatically re-populate the menu.

A symbolic link to the model directory will also work. On Mac, you can create one by running:
```
ln -s ~/models ~/Music/Ableton/User\ Library/Presets/Audio\ Effects/Max\ Audio\ Effect/transfer/models
```
Afterwards, hit *Default* to update the menu.

## Saving
To set your chosen model folder to load up on start, open the patcher in Max, add the directory as described above and save the patcher.
Multislider settings should save automatically with your Ableton project.


## Note
This is a work in progress, so feel free to open up issues for any bugs encountered or features you'd like to see. Feedback from Windows users is especially appreciated, since I don't have any means of testing on that platform.


## Demo
Coming soon!
