## Frequently-used-Commands

- `conda env list` or `conda info --envs`: List all conda envs
- `conda list -n <my_env>` : List all packages installed in the env my_env
- `pip list`: List all packeges in current env. Need to run this when the env is activated.

## Google Cloud
- Typical steps:
  - Start an instance: `gcloud compute instances start pytorch-event-detector-vm `
  - Connecting to the instance: `gcloud compute ssh muyang@pytorch-event-detector-vm` 
  - Stop instances `gcloud compute instances stop pytorch-event-detector-vm --zone us-west1-b`
- check instance status: `gcloud compute instances list`. Note that you have to make sure the status is TERMINATED. Otherwise Google will charge you.

## Tensorflow
- Check visiable device to TF 
```
import tensorflow as tf
sess = tf.Session(config=tf.ConfigProto(log_device_placement=True))
```
- Force TF to use CPU, ignoring GPU. (This might be useful for some RNN cases, where it might be even slower to train RNNs on GPU than CPU)
```
os.environ['CUDA_VISIBLE_DEVICES'] = ''
```

## Vim
- I used [amix/vimrc](https://github.com/amix/vimrc)
- `\<leader\>nn` to open NerdTree panel, `\<C-ww\>` to switch between code and NerdTree panel. `\<leader-te\>` to select path buffer and select files to open in a new tab. `gt` goes to next tab, `gT` goes to prev tab.
- Maybe good to check [this](https://www.freecodecamp.org/news/learn-linux-vim-basic-features-19134461ab85/) out

## Terminal
- Check GPU cards and CPUs: `lspci`

## Awesome tutorials
- [Some very common Linux commands](https://linuxtools-rst.readthedocs.io/zh_CN/latest/base/01_use_man.html)
