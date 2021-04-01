# Track 3: Automatic Bridge Detection in Optical Satellite Images

In Track 3 the goal is to locate the bridge in the largescale optical satellite images. The coordinates of the bridge are horizontal bounding box.

## Baseline Algorithm
Two-stage object detection method Faster RCNN based on ResNet-50 is developed for object detection tracks.

### Introduction
It is modified from [mmdetection](https://github.com/open-mmlab/mmdetection). The master branch works with **PyTorch 1.1** or higher.

- Linux
- Python 3.5+ ([Say goodbye to Python2](https://python3statement.org/))
- PyTorch 1.1
- CUDA 9.0+
- NCCL 2+
- GCC 4.9+
- [mmcv](https://github.com/open-mmlab/mmcv)

### Quick Run
The following instructions are for running the baseline solution.

#### Training
Command line arguments are used to determine train mode for object detection tracks of Gaofen Challenge. 

Distributed training and non-distributed training use `MMDistributedDataParallel` and `MMDataParallel` respectively. All outputs (log files and checkpoints) will be saved to the working directory, which is specified by `work_dir` in the config file.

* Train with a single GPU

```shell
python tools/train.py ${CONFIG_FILE}
```

If you want to specify the working directory in the command, you can add an argument `--work_dir ${YOUR_WORK_DIR}`.

* Train with multiple GPUs

```shell
./tools/dist_train.sh ${CONFIG_FILE} ${GPU_NUM} [optional arguments]
```

Optional arguments are:

`--validate` (recommended): Perform evaluation at every k (default=1) epochs during the training.

`--work_dir ${WORK_DIR}`: Override the working directory specified in the config file.

`--resume_from ${CHECKPOINT_FILE}`: Resume from a previous checkpoint file.



#### Testing

* Object Detection single-gpu test
 ```
 python tools/test.py ${CONFIG_FILE} ${CHECKPOINT_FILE} [--out ${RESULT_FILE}]
 ```
* Object Detection multi-gpu test
```
./tools/dist_test.sh ${CONFIG_FILE} ${CHECKPOINT_FILE} ${GPU_NUM} [--out ${RESULT_FILE}]
```

Optional arguments:
- `RESULT_FILE`: Filename of the output results in pickle format. If not specified, the results will not be saved to a file.

For methods with only OBB Head, set the type OBB.
```
python tools/parse_results.py --config ${CONFIG_FILE} --type OBB
```
For methods with only HBB Head, se the type HBB
```
python tools/parse_results.py --config ${CONFIG_FILE} --type HBB
```

### Result

|    Method   | Result (mAP) |
| ----------- | ----------- |
| Faster RCNN | 0.00 |