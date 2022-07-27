##### silver-nightingale
 
 # **AI Music Generation using RNNs**
 
 ##### Generate musical notes using a simple Recurrent Neural Network (RNN)

In this project, I have implemented this [tutorial](https://www.tensorflow.org/tutorials/audio/music_generation) and generated musical notes using a simple recurrent neural network (RNN).

First I trained a model using a collection of piano MIDI files from the MAESTRO dataset. Given a sequence of notes, the model learned to predict the next note in the sequence. 

### **Setup**

Run the following commands in the terminal in the environment this notebook is being run, to install the main dependencies and packages required:
```console
sudo apt install -y fluidsynth
```

```console
pip install --upgrade pyfluidsynth
```

```console
pip install pretty_midi
```

### **Dataset**

To access the dataset, run the following piece of code in jupyter notebook:
```python
import tensorflow as tf
import pathlib

data_dir = pathlib.Path('data/maestro-v2.0.0')
if not data_dir.exists():
  tf.keras.utils.get_file(
      'maestro-v2.0.0-midi.zip',
      origin='https://storage.googleapis.com/magentadata/datasets/maestro/v2.0.0/maestro-v2.0.0-midi.zip',
      extract=True,
      cache_dir='.', cache_subdir='data',
  )

```
