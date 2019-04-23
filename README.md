# Octave Convolution

### Introduction

Unofficial!

A replication of [Octave Convoltuion](https://arxiv.org/abs/1904.05049).

Require TensorFlow 2.0 to run the code.

Model and layers are from [SUL](https://github.com/ddddwee1/sul).

### Installation

To install, run
```
pip install tf-nightly-gpu-2.0-preview
```

Remember to change registry if using Windows.

```
1. Start the registry editor (regedit.exe)

2. Navigate to HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem

3. Double click LongPathsEnabled, set to 1 and click OK

4. Reboot
```

### How to Run

```
1. Modify the data reader yourself.

2. In 'train.py', modify line 22 to fit your data reader.

3. Modify the network initialization step in line 50 of 'train.py'. The parallel training needs it.

4. There should be no problem. Run 'train.py'
```

### Notes

Different models are/will be implemented in './net_structures/'. 

Currently I am using 'octresnet_half' to train the face recognition model. 

Since the input is 112x112 and cannot be halved in the last ResBlock, I use conventional ResUnits for the last block to form 'octresnet_half'.

I will report the performance once finished.
