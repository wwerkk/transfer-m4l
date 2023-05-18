# Transfer
Max4Live device for real-time timbre transfer using RAVE models.
## Requirements
- ``nn~`` external: https://github.com/acids-ircam/nn_tilde/
- any *RAVE* model, you can download some pre-trained ones here: https://acids-ircam.github.io/rave_models_download
(v1 models without prior training such as ``darbouka_onnx`` do not work for the moment)
## Quick start
- Download the required files from above and add them to your Max path.
If you don't know how to do that: clone the repo as instructed below and simply put all of the necessary files inside of the repo directory.
- For ``transfer.amxd`` to appear in Max for Live/Max Audio Effects in Ableton, on MacOS run:
```
git clone https://github.com/wwerkk/transfer-m4l.git ~/Music/Ableton/User\ Library/Presets/Audio\ Effects/Max\ Audio\ Effect/transfer
```
- Use as an audio effect on any channel you like.
- You can change the loaded model using the menu.
- Turn up the Wet output gain.
- Latent vectors can be offset and scaled using the multisliders, the menu below offset controls wavefolding settings in case your latent values go out of ``-4`` to ``4`` range.
## Adding your own models
Add the directory containing your models by dropping it into the box on left bottom of the patch or using the browse button.
To set your chosen model folder to load up on start, open the patcher in Max, add the directory as described above and save the patcher.

*Default* button resets the path to default Max path, it should display ``wheel.ts`` if you have downloaded it using the ``nn~`` help file.
