# An Entropy-Based Assessment of Cloud Mask Algorithms for Satellite Image Segmentation

## Sentinel-2 Masks compared
|Title|Code|TYPE|
|:---:|:---:|:---:|
[s2cloudless](https://developers.google.com/earth-engine/tutorials/community/sentinel-2-s2cloudless)|[Code](https://developers.google.com/earth-engine/tutorials/community/sentinel-2-s2cloudless)|CNN|GEE|
[S2 SCORE+](https://developers.google.com/earth-engine/datasets/catalog/GOOGLE_CLOUD_SCORE_PLUS_V1_S2_HARMONIZED)|[Code](https://developers.google.com/earth-engine/datasets/catalog/GOOGLE_CLOUD_SCORE_PLUS_V1_S2_HARMONIZED)|CNN|GEE|
[Fmask](https://www.sciencedirect.com/science/article/pii/S0034425719302172)|[Code](https://github.com/ubarsc/python-fmask)|physical-rule-based|MATLAB|
[sen2cor](https://step.esa.int/main/snap-supported-plugins/sen2cor/)|[Code](hhttps://github.com/c-core-labs/sen2cor)|physical-rule-based|C++|
[SEnSeIv2](https://ieeexplore.ieee.org/document/10505181)|[Code](https://github.com/aliFrancis/SEnSeIv2)|CNN|PYTORCH|
[Unetmobv2](https://huggingface.co/datasets/tacofoundation/SEN2NAIPv2)|[Code](https://huggingface.co/datasets/tacofoundation/SEN2NAIPv2)|CNN|PYTORCH|
[kappamask]()|[Code]()|CNN|TENSORFLOW|

## How to use
Add SAM model in Checkpoints.

in ```/code``` repository you have two jupyter notebooks:
* ```CloudPlast.ipynb```
  * Follow the instructions and run the code with the data inside each csv file.
  * You can also select custom rois and generate the results.
* ```CloudSEN12+.ipynb```
  * Follow the instructions and run the code with the data inside each csv file.
  * To Generate the results 
    * Download the CLOUDSEN12 dataset images on https://www.scidb.cn/en/detail?dataSetId=f72d622ff4ea4fa18070456a98222b1a descomprise the tar files and add them inside ```CloudSEN12+```. 
    * OPTIONAL but Recommended: Download CLOUDSEN12+ metadata files from https://huggingface.co/datasets/tacofoundation/cloudsen12/tree/main and add them on ```CloudSEN12+```. This step will speed up the processes of processing the images.

## SAM model

To configure the SAM model you can acess ```plastic sniffer``` repository.

Click the links below to download the checkpoint for the corresponding model type.
- **`default` or `vit_h`: [ViT-H SAM model.](https://dl.fbaipublicfiles.com/segment_anything/sam_vit_h_4b8939.pth)**
- `vit_l`: [ViT-L SAM model.](https://dl.fbaipublicfiles.com/segment_anything/sam_vit_l_0b3195.pth)
- `vit_b`: [ViT-B SAM model.](https://dl.fbaipublicfiles.com/segment_anything/sam_vit_b_01ec64.pth)


Then add the model to the `Checkpoints` directory.