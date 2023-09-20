<!-- TODO

-->
## Instructions
### Installation
Make sure [conda](https://www.anaconda.com/distribution/) is installed.

    # clone this repository
    git clone https://github.com/VlSomers/bpbreid

    # create conda environment
    cd bpbreid/ # enter project folder
    conda create --name bpbreid python=3.10
    conda activate bpbreid
    # install torch and torchvision (select the proper cuda version to suit your machine)
    conda install pytorch torchvision cudatoolkit=9.0 -c pytorch
    # install dependencies
    # make sure `which python` and `which pip` point to the correct path
    pip install -r requirements.txt
    # install torchreid (don't need to re-build it if you modify the source code)
    python setup.py develop
    

### Download dataset
Download [dataset](https://drive.google.com/drive/folders/1k4SnHuUB4qr3uuDI6RcBu64CrzABSjCs?fbclid=IwAR2qpzrDsMFsNRde6IbtKB9CVPd_zLAgf_7YQJVk_G9o8dQImjZl33nj2Aw&hl=en) then extract downloaded dataset then copy to /home/$USER/datasets/reid

### Download the pre-trained models
Download pretrained model [hrnetv2_w32_imagenet_pretrained](https://drive.google.com/drive/folders/1k4SnHuUB4qr3uuDI6RcBu64CrzABSjCs?fbclid=IwAR2qpzrDsMFsNRde6IbtKB9CVPd_zLAgf_7YQJVk_G9o8dQImjZl33nj2Aw&hl=en) first then copy pretrained model to pretrained_model folder in the project

### Training
    conda activate bpbreid
    python main.py --config-file configs/bpbreid/bpbreid_market1501_train.yaml

