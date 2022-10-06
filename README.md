# 3D_SCENEGRAPH

### Requirements:
- PyTorch >= 1.4
- torchvision >= 0.4
- cocoapi
- yacs
- matplotlib
- GCC >= 4.9
- OpenCV

### DATASET
The following is exactly the same as [3DSSG](https://github.com/ShunChengWu/3DSSG/blob/master/data_processing/README.md).

### Data preparation

Alternatively, you can download the files from this [link](https://drive.google.com/file/d/1V_QIDvu1fZqKkjP2Kg41HNCjX8TPfH6u/view?usp=sharing)

Download data from 3RScan
* To download the 3RScan 3D data, visit their [project page](https://waldjohannau.github.io/RIO).
* After receiving the download script, run:
```
python download.py -o /path/to/3RScan/ --type semseg.v2.json
python download.py -o /path/to/3RScan/ --type labels.instances.annotated.v2.ply
``` 

* change DATA_PATH in `./utils/define.py` to your path to the 3RScan directory and ROOT_PATH to the path of this repository.

* Run `transform_ply.py` under `./data_processing/` to generate `labels.instances.align.annotated.ply`

### Generate training/evaluation data with GT segmentations
Use `gen_data_gt.py` to generate the training data in the 3DSSG paper.


[3rscan]: https://waldjohannau.github.io/RIO/
