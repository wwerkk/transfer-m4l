# Transfer
Max4Live device for real-time timbre transfer using RAVE models.
## Requirements
- nn~ tilde: https://github.com/acids-ircam/nn_tilde/
- any RAVE model, you can download some pre-trained ones here (darbouka_onnx does not work for the moment): https://acids-ircam.github.io/rave_models_download
## Quick start
- Download the required files from above and add them to your Max path.
If you don't know how to do that: clone the repo as instructed below and simply put all of the necessary files inside of the repo directory.
- For ``transfer.amxd`` to appear in Max for Live/Max Audio Effects in Ableton, on MacOS run:
```
git clone https://github.com/wwerkk/transfer-m4l.git ~/Music/Ableton/User\ Library/Presets/Audio\ Effects/Max\ Audio\ Effect/transfer
```
- Use as an audio effect on any channel you like.
- You can change the loaded model using the umenu.
- Turn up the Wet gain.
- Latent vectors can be offset and scaled using the multisliders.
- You can save the multislider settings by clicking on the ``preset`` object on the far right while holding *Shift*.
## Adding your own models
To add your own model and enable loading it dynamically:
1. In the ``transfer.amxd`` patch, add your model name as an item to the ``live.menu`` object.
2. That's it!
