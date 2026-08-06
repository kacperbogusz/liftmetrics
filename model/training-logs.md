# model training logs

```
Platform: View model at https://platform.ultralytics.com/kacper-bogusz/gym-plates/exp-5
Downloading https://storage.googleapis.com/alpha-ultralytics-eu/exports/6a688e959937b624d71b30a6/gym-plates.ndjson to 'kacper-bogusz/datasets/gym-plates/gym-plates.ndjson': 100% ━━━━━━━━━━━━ 57.9KB 1.1MB/s 0.1s
Converting gym-plates.ndjson → /datasets/gym-plates-13d69683 (197 images): 100% ━━━━━━━━━━━━ 197/197 272.3it/s 0.7s
Downloading https://ultralytics.com/assets/Arial.ttf to '/tmp/Ultralytics/Arial.ttf': 100% ━━━━━━━━━━━━ 755.1KB 8.0MB/s 0.1s
Overriding model.yaml nc=80 with nc=1

                   from  n    params  module                                       arguments
  0                  -1  1       464  ultralytics.nn.modules.conv.Conv             [3, 16, 3, 2]
  1                  -1  1      4672  ultralytics.nn.modules.conv.Conv             [16, 32, 3, 2]
  2                  -1  1      6640  ultralytics.nn.modules.block.C3k2            [32, 64, 1, False, 0.25]
  3                  -1  1     36992  ultralytics.nn.modules.conv.Conv             [64, 64, 3, 2]
  4                  -1  1     26080  ultralytics.nn.modules.block.C3k2            [64, 128, 1, False, 0.25]
  5                  -1  1    147712  ultralytics.nn.modules.conv.Conv             [128, 128, 3, 2]
  6                  -1  1     87040  ultralytics.nn.modules.block.C3k2            [128, 128, 1, True]
  7                  -1  1    295424  ultralytics.nn.modules.conv.Conv             [128, 256, 3, 2]
  8                  -1  1    346112  ultralytics.nn.modules.block.C3k2            [256, 256, 1, True]
  9                  -1  1    164608  ultralytics.nn.modules.block.SPPF            [256, 256, 5, 3, True]
 10                  -1  1    249728  ultralytics.nn.modules.block.C2PSA           [256, 256, 1]
 11                  -1  1         0  torch.nn.modules.upsampling.Upsample         [None, 2, 'nearest']
 12             [-1, 6]  1         0  ultralytics.nn.modules.conv.Concat           [1]
 13                  -1  1    119808  ultralytics.nn.modules.block.C3k2            [384, 128, 1, True]
 14                  -1  1         0  torch.nn.modules.upsampling.Upsample         [None, 2, 'nearest']
 15             [-1, 4]  1         0  ultralytics.nn.modules.conv.Concat           [1]
 16                  -1  1     34304  ultralytics.nn.modules.block.C3k2            [256, 64, 1, True]
 17                  -1  1     36992  ultralytics.nn.modules.conv.Conv             [64, 64, 3, 2]
 18            [-1, 13]  1         0  ultralytics.nn.modules.conv.Concat           [1]
 19                  -1  1     95232  ultralytics.nn.modules.block.C3k2            [192, 128, 1, True]
 20                  -1  1    147712  ultralytics.nn.modules.conv.Conv             [128, 128, 3, 2]
 21            [-1, 10]  1         0  ultralytics.nn.modules.conv.Concat           [1]
 22                  -1  1    463104  ultralytics.nn.modules.block.C3k2            [384, 256, 1, True, 0.5, True]
 23        [16, 19, 22]  1    241566  ultralytics.nn.modules.head.Detect           [1, 1, True, [64, 128, 256]]
YOLO26n summary: 260 layers, 2,504,190 parameters, 2,504,190 gradients, 5.8 GFLOPs

Transferred 606/708 items from pretrained weights
AMP: running Automatic Mixed Precision (AMP) checks...
Downloading https://github.com/ultralytics/assets/releases/download/v8.4.0/yolo26n.pt to 'yolo26n.pt': 100% ━━━━━━━━━━━━ 5.3MB 29.3MB/s 0.2s
AMP: checks passed ✅
train: Fast image access ✅ (ping: 0.0±0.0 ms, read: 1953.2±1423.4 MB/s, size: 134.3 KB)
train: Scanning /datasets/gym-plates-13d69683/labels/train... 150 images, 0 backgrounds, 0 corrupt: 100% ━━━━━━━━━━━━ 150/150 1.1Kit/s 0.1s
train: New cache created: /datasets/gym-plates-13d69683/labels/train.cache
val: Fast image access ✅ (ping: 0.0±0.0 ms, read: 1913.0±1247.6 MB/s, size: 127.3 KB)
val: Scanning /datasets/gym-plates-13d69683/labels/val... 38 images, 0 backgrounds, 0 corrupt: 100% ━━━━━━━━━━━━ 38/38 1.4Kit/s 0.0s
val: New cache created: /datasets/gym-plates-13d69683/labels/val.cache
optimizer: 'optimizer=auto' found, ignoring 'lr0=0.001' and 'momentum=0.937' and determining best 'optimizer', 'lr0' and 'momentum' automatically...
optimizer: AdamW(lr=0.002, momentum=0.9) with parameter groups 114 weight(decay=0.0), 126 weight(decay=0.0005), 126 bias(decay=0.0)
Plotting labels to /runs/detect/kacper-bogusz/gym-plates/exp-5/labels.jpg...
Image sizes 640 train, 640 val
Using 8 dataloader workers
Logging results to /runs/detect/kacper-bogusz/gym-plates/exp-5
Starting training for 100 epochs...

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
      1/100      1.34G     0.9359       5.65   0.006359         11        640: 100% ━━━━━━━━━━━━ 19/19 1.1s/it 20.5s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 1.8s/it 5.3s
                   all         38         55    0.00482          1      0.227      0.168

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
      2/100      1.36G     0.8667      4.278   0.005424         28        640: 100% ━━━━━━━━━━━━ 19/19 11.4it/s 1.7s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.4it/s 0.1s
                   all         38         55      0.189      0.309       0.21      0.131

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
      3/100      1.37G     0.8812      3.712   0.005491         23        640: 100% ━━━━━━━━━━━━ 19/19 11.6it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.5it/s 0.1s
                   all         38         55      0.242      0.273      0.334      0.228

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
      4/100      1.39G     0.8768      3.474   0.005919         20        640: 100% ━━━━━━━━━━━━ 19/19 11.6it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.1it/s 0.1s
                   all         38         55       0.37      0.236      0.387      0.276

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
      5/100      1.41G     0.9671       3.22   0.006183         16        640: 100% ━━━━━━━━━━━━ 19/19 11.7it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.2it/s 0.1s
                   all         38         55      0.725      0.691      0.825      0.682

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
      6/100      1.43G     0.9757      3.365   0.007183         12        640: 100% ━━━━━━━━━━━━ 19/19 11.8it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.7it/s 0.1s
                   all         38         55      0.844      0.691      0.844      0.583

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
      7/100      1.45G      0.956      3.001    0.00625         18        640: 100% ━━━━━━━━━━━━ 19/19 11.7it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.8it/s 0.1s
                   all         38         55      0.754      0.894      0.906      0.741

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
      8/100      1.46G     0.9884      2.687   0.006847         19        640: 100% ━━━━━━━━━━━━ 19/19 11.5it/s 1.7s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.5it/s 0.1s
                   all         38         55      0.648      0.945      0.738      0.557

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
      9/100      1.48G     0.9559      2.608   0.006114         19        640: 100% ━━━━━━━━━━━━ 19/19 11.8it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.2it/s 0.1s
                   all         38         55      0.752      0.945       0.87      0.724

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     10/100       1.5G     0.8946      2.598    0.00633         15        640: 100% ━━━━━━━━━━━━ 19/19 11.7it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.4it/s 0.1s
                   all         38         55       0.76       0.98      0.926      0.716

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     11/100      1.52G     0.9127      2.207   0.006369         19        640: 100% ━━━━━━━━━━━━ 19/19 11.8it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.6it/s 0.1s
                   all         38         55      0.846      0.901      0.935      0.745

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     12/100      1.53G     0.9231      2.066   0.006505         12        640: 100% ━━━━━━━━━━━━ 19/19 11.8it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.0it/s 0.1s
                   all         38         55      0.776      0.945      0.902      0.671

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     13/100      1.55G     0.8121      1.925   0.005442         20        640: 100% ━━━━━━━━━━━━ 19/19 11.8it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.6it/s 0.1s
                   all         38         55      0.873      0.873      0.942      0.727

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     14/100      1.57G     0.8051      1.776   0.005225         17        640: 100% ━━━━━━━━━━━━ 19/19 11.9it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.4it/s 0.1s
                   all         38         55       0.91      0.918      0.959      0.841

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     15/100      1.59G     0.8659      1.607   0.005583         24        640: 100% ━━━━━━━━━━━━ 19/19 11.8it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.0it/s 0.1s
                   all         38         55      0.842      0.966      0.954      0.706

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     16/100      1.61G      0.974      1.621   0.005775         13        640: 100% ━━━━━━━━━━━━ 19/19 11.8it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.6it/s 0.1s
                   all         38         55      0.894      0.918      0.969      0.798

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     17/100      1.62G     0.8159       1.55   0.005633         18        640: 100% ━━━━━━━━━━━━ 19/19 11.8it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.4it/s 0.1s
                   all         38         55      0.918      0.855      0.962      0.753

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     18/100      1.64G     0.7742      1.488   0.005569         11        640: 100% ━━━━━━━━━━━━ 19/19 11.7it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.5it/s 0.1s
                   all         38         55      0.923          1      0.975      0.799

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     19/100      1.66G     0.7487       1.39   0.004573         14        640: 100% ━━━━━━━━━━━━ 19/19 11.9it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.9it/s 0.1s
                   all         38         55      0.948      0.909      0.977      0.757

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     20/100      1.68G     0.7391      1.357   0.005226         17        640: 100% ━━━━━━━━━━━━ 19/19 11.8it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.4it/s 0.1s
                   all         38         55       0.96      0.869      0.972      0.799

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     21/100       1.7G     0.7635      1.257   0.005099         15        640: 100% ━━━━━━━━━━━━ 19/19 11.8it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.6it/s 0.1s
                   all         38         55      0.931      0.975      0.968      0.812

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     22/100      1.72G     0.7511      1.166   0.004718         18        640: 100% ━━━━━━━━━━━━ 19/19 11.5it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.3it/s 0.1s
                   all         38         55       0.85      0.909      0.946      0.812

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     23/100      1.74G     0.7462      1.167   0.004925         18        640: 100% ━━━━━━━━━━━━ 19/19 11.5it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 20.8it/s 0.1s
                   all         38         55      0.842      0.945      0.961      0.812

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     24/100      1.75G     0.7569      1.104   0.004969         23        640: 100% ━━━━━━━━━━━━ 19/19 11.7it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.6it/s 0.1s
                   all         38         55      0.876      0.891      0.957      0.745

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     25/100      1.77G     0.7656      1.087   0.005264         19        640: 100% ━━━━━━━━━━━━ 19/19 11.8it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.5it/s 0.1s
                   all         38         55      0.854      0.945      0.934      0.747

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     26/100      1.79G     0.7397     0.9633   0.004964         19        640: 100% ━━━━━━━━━━━━ 19/19 11.7it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.8it/s 0.1s
                   all         38         55      0.889      0.836      0.888       0.69

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     27/100       1.8G     0.7028     0.9574   0.004777         10        640: 100% ━━━━━━━━━━━━ 19/19 11.8it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.5it/s 0.1s
                   all         38         55       0.84      0.955      0.935       0.79

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     28/100      1.82G     0.7545     0.8728   0.004855         25        640: 100% ━━━━━━━━━━━━ 19/19 11.8it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.2it/s 0.1s
                   all         38         55      0.884      0.927       0.95        0.8

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     29/100      1.84G     0.7342     0.9141    0.00468         11        640: 100% ━━━━━━━━━━━━ 19/19 11.7it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.7it/s 0.1s
                   all         38         55      0.868          1      0.955      0.771

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     30/100      1.86G     0.7392     0.8295   0.004743         22        640: 100% ━━━━━━━━━━━━ 19/19 11.7it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.6it/s 0.1s
                   all         38         55       0.88      0.934      0.944      0.809

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     31/100      1.88G     0.7573     0.8106   0.004959         23        640: 100% ━━━━━━━━━━━━ 19/19 11.7it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 20.4it/s 0.1s
                   all         38         55      0.883      0.982      0.964      0.816

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     32/100       1.9G     0.7277     0.8532   0.005001         20        640: 100% ━━━━━━━━━━━━ 19/19 11.5it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.6it/s 0.1s
                   all         38         55      0.943      0.909      0.972      0.765

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     33/100      1.91G     0.7663     0.7708    0.00507         13        640: 100% ━━━━━━━━━━━━ 19/19 11.7it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.3it/s 0.1s
                   all         38         55      0.856      0.972      0.976      0.861

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     34/100      1.93G     0.7385     0.7419   0.004919         23        640: 100% ━━━━━━━━━━━━ 19/19 11.6it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.7it/s 0.1s
                   all         38         55      0.914      0.966      0.984      0.841

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     35/100      1.95G     0.7439     0.7543   0.004644         21        640: 100% ━━━━━━━━━━━━ 19/19 11.8it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.7it/s 0.1s
                   all         38         55      0.935      0.909       0.98      0.811

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     36/100      1.96G     0.7388     0.7166    0.00502         20        640: 100% ━━━━━━━━━━━━ 19/19 11.7it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.6it/s 0.1s
                   all         38         55      0.943      0.898      0.975      0.767

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     37/100      1.98G     0.7526     0.6858    0.00488         21        640: 100% ━━━━━━━━━━━━ 19/19 11.6it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.0it/s 0.1s
                   all         38         55      0.885       0.98      0.965      0.858

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     38/100      2.01G     0.7014     0.6456    0.00458         16        640: 100% ━━━━━━━━━━━━ 19/19 11.7it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.8it/s 0.1s
                   all         38         55      0.825          1      0.965      0.756

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     39/100      2.02G     0.7115     0.6355   0.004603         31        640: 100% ━━━━━━━━━━━━ 19/19 11.7it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.1it/s 0.1s
                   all         38         55      0.853      0.964      0.968      0.815

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     40/100      2.04G     0.7384      0.674   0.005051         19        640: 100% ━━━━━━━━━━━━ 19/19 11.6it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.1it/s 0.1s
                   all         38         55      0.925      0.945      0.971      0.788

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     41/100      2.06G     0.7214     0.5995   0.004688         25        640: 100% ━━━━━━━━━━━━ 19/19 11.6it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.8it/s 0.1s
                   all         38         55      0.907      0.883      0.954      0.762

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     42/100      2.08G     0.7204     0.6468   0.005011         13        640: 100% ━━━━━━━━━━━━ 19/19 11.6it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.6it/s 0.1s
                   all         38         55      0.908      0.927       0.97      0.866

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     43/100      2.09G     0.7702     0.6641    0.00528         24        640: 100% ━━━━━━━━━━━━ 19/19 11.7it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.6it/s 0.1s
                   all         38         55       0.94      0.859      0.968      0.783

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     44/100      2.11G     0.6728     0.5689   0.004605         13        640: 100% ━━━━━━━━━━━━ 19/19 11.7it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.0it/s 0.1s
                   all         38         55      0.859      0.927      0.956      0.831

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     45/100      2.13G      0.741     0.6173   0.004916          8        640: 100% ━━━━━━━━━━━━ 19/19 11.6it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.4it/s 0.1s
                   all         38         55      0.911      0.945      0.969      0.799

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     46/100      2.15G     0.7181     0.5731    0.00473         17        640: 100% ━━━━━━━━━━━━ 19/19 11.8it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.6it/s 0.1s
                   all         38         55      0.914      0.962      0.984      0.755

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     47/100      2.17G     0.6764     0.5455   0.004398         21        640: 100% ━━━━━━━━━━━━ 19/19 11.6it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.7it/s 0.1s
                   all         38         55      0.953      0.982      0.986      0.843

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     48/100      2.18G     0.8099     0.6299   0.005331         21        640: 100% ━━━━━━━━━━━━ 19/19 11.6it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.6it/s 0.1s
                   all         38         55      0.907      0.964      0.976      0.827

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     49/100       2.2G     0.7254     0.5603   0.005278         23        640: 100% ━━━━━━━━━━━━ 19/19 11.6it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.6it/s 0.1s
                   all         38         55       0.93      0.962       0.98      0.758

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     50/100      2.22G     0.7459     0.5563   0.005339         20        640: 100% ━━━━━━━━━━━━ 19/19 11.6it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.8it/s 0.1s
                   all         38         55      0.928      0.943      0.984      0.883

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     51/100      2.24G     0.6926     0.5472   0.004369         22        640: 100% ━━━━━━━━━━━━ 19/19 11.8it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.0it/s 0.1s
                   all         38         55      0.879      0.982       0.98      0.897

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     52/100      2.26G     0.6735     0.6012   0.004748         17        640: 100% ━━━━━━━━━━━━ 19/19 11.7it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.0it/s 0.1s
                   all         38         55      0.888      0.964      0.978      0.807

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     53/100      2.27G     0.6324     0.4588   0.004044         12        640: 100% ━━━━━━━━━━━━ 19/19 11.6it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.8it/s 0.1s
                   all         38         55      0.863      0.982      0.975      0.831

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     54/100      2.29G     0.6542     0.5327   0.004235         19        640: 100% ━━━━━━━━━━━━ 19/19 11.7it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.0it/s 0.1s
                   all         38         55      0.941      0.945      0.983      0.859

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     55/100      2.31G     0.6488     0.5418   0.004395         21        640: 100% ━━━━━━━━━━━━ 19/19 11.7it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.3it/s 0.1s
                   all         38         55      0.981      0.938      0.988      0.821

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     56/100      2.33G     0.6368     0.5238   0.004128         19        640: 100% ━━━━━━━━━━━━ 19/19 11.5it/s 1.7s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.4it/s 0.1s
                   all         38         55      0.962      0.933      0.987       0.85

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     57/100      2.34G     0.6216     0.4411   0.003734         26        640: 100% ━━━━━━━━━━━━ 19/19 11.6it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.0it/s 0.1s
                   all         38         55      0.925      0.902      0.977       0.78

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     58/100      2.36G     0.5915     0.4434   0.004078         17        640: 100% ━━━━━━━━━━━━ 19/19 11.6it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.1it/s 0.1s
                   all         38         55      0.895      0.964      0.975      0.858

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     59/100      2.38G      0.659     0.4809    0.00399         23        640: 100% ━━━━━━━━━━━━ 19/19 11.4it/s 1.7s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.1it/s 0.1s
                   all         38         55      0.929      0.955       0.98      0.869

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     60/100       2.4G     0.6041     0.4547   0.003923         17        640: 100% ━━━━━━━━━━━━ 19/19 11.5it/s 1.7s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.6it/s 0.1s
                   all         38         55      0.878      0.964       0.98      0.849

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     61/100      2.42G     0.6624     0.5389   0.004576         19        640: 100% ━━━━━━━━━━━━ 19/19 11.4it/s 1.7s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.4it/s 0.1s
                   all         38         55      0.937      0.909       0.98      0.798

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     62/100      2.43G     0.6113     0.4733   0.003871         12        640: 100% ━━━━━━━━━━━━ 19/19 11.7it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 20.8it/s 0.1s
                   all         38         55      0.883      0.959      0.979      0.793

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     63/100      2.45G     0.5907     0.4313   0.003929         13        640: 100% ━━━━━━━━━━━━ 19/19 11.5it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.1it/s 0.1s
                   all         38         55      0.885      0.964      0.976      0.823

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     64/100      2.47G     0.6431     0.4759    0.00414         18        640: 100% ━━━━━━━━━━━━ 19/19 11.5it/s 1.7s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.4it/s 0.1s
                   all         38         55      0.901      0.982      0.979      0.857

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     65/100      2.49G     0.6207     0.4788   0.003997         21        640: 100% ━━━━━━━━━━━━ 19/19 11.6it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.0it/s 0.1s
                   all         38         55      0.931      0.983      0.983      0.802

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     66/100      2.51G     0.6352      0.478    0.00434         18        640: 100% ━━━━━━━━━━━━ 19/19 11.5it/s 1.7s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.3it/s 0.1s
                   all         38         55      0.881      0.982      0.977      0.819

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     67/100      2.52G     0.6301     0.4562   0.004307         13        640: 100% ━━━━━━━━━━━━ 19/19 11.6it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.2it/s 0.1s
                   all         38         55      0.901      0.991      0.978      0.848

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     68/100      2.54G     0.6121     0.5034   0.003961         34        640: 100% ━━━━━━━━━━━━ 19/19 11.6it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.3it/s 0.1s
                   all         38         55      0.913      0.959      0.982      0.863

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     69/100      2.56G     0.5974     0.4409   0.003764         16        640: 100% ━━━━━━━━━━━━ 19/19 11.6it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.9it/s 0.1s
                   all         38         55      0.943          1      0.986      0.872

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     70/100      2.58G     0.6579     0.4405   0.004053         22        640: 100% ━━━━━━━━━━━━ 19/19 11.5it/s 1.7s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.0it/s 0.1s
                   all         38         55      0.931          1      0.988      0.857

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     71/100       2.6G     0.6185     0.4587   0.003744         17        640: 100% ━━━━━━━━━━━━ 19/19 11.6it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 20.2it/s 0.1s
                   all         38         55      0.944          1      0.989      0.844

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     72/100      2.62G     0.6464     0.4193   0.004093         22        640: 100% ━━━━━━━━━━━━ 19/19 11.5it/s 1.7s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.4it/s 0.1s
                   all         38         55       0.93          1      0.989      0.851

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     73/100      2.63G     0.5894     0.4242   0.003893         22        640: 100% ━━━━━━━━━━━━ 19/19 11.6it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.9it/s 0.1s
                   all         38         55      0.931          1      0.989      0.852

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     74/100      2.65G     0.5892     0.4322   0.003823         18        640: 100% ━━━━━━━━━━━━ 19/19 11.5it/s 1.7s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.5it/s 0.1s
                   all         38         55      0.925          1       0.99      0.863

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     75/100      2.67G     0.6416     0.4283   0.004193         12        640: 100% ━━━━━━━━━━━━ 19/19 11.5it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.0it/s 0.1s
                   all         38         55      0.968      0.945      0.991      0.869

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     76/100      2.69G     0.6212     0.4354   0.004061         11        640: 100% ━━━━━━━━━━━━ 19/19 11.1it/s 1.7s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.4it/s 0.1s
                   all         38         55      0.981      0.919      0.989      0.848

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     77/100       2.7G     0.5967     0.4489    0.00392         10        640: 100% ━━━━━━━━━━━━ 19/19 11.1it/s 1.7s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.6it/s 0.1s
                   all         38         55      0.899      0.982      0.985      0.852

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     78/100      2.72G     0.5835     0.4592   0.003938         17        640: 100% ━━━━━━━━━━━━ 19/19 11.3it/s 1.7s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.8it/s 0.1s
                   all         38         55      0.895      0.982      0.982        0.9

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     79/100      2.74G     0.5716     0.4376    0.00377         19        640: 100% ━━━━━━━━━━━━ 19/19 11.6it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.9it/s 0.1s
                   all         38         55        0.9      0.981      0.982      0.899

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     80/100      2.76G     0.5789     0.3978   0.003895         17        640: 100% ━━━━━━━━━━━━ 19/19 11.4it/s 1.7s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.8it/s 0.1s
                   all         38         55      0.902      0.999      0.985      0.868

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     81/100      2.78G      0.543     0.3887   0.003627         13        640: 100% ━━━━━━━━━━━━ 19/19 11.3it/s 1.7s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 20.4it/s 0.1s
                   all         38         55      0.944      0.945      0.989      0.858

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     82/100      2.79G     0.5332     0.4049   0.003503         21        640: 100% ━━━━━━━━━━━━ 19/19 11.2it/s 1.7s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.1it/s 0.1s
                   all         38         55      0.947      0.971      0.988      0.863

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     83/100      2.81G     0.5339     0.3974   0.003788         16        640: 100% ━━━━━━━━━━━━ 19/19 11.5it/s 1.7s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.7it/s 0.1s
                   all         38         55      0.916      0.995      0.987      0.885

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     84/100      2.83G     0.5567     0.4298   0.003605         19        640: 100% ━━━━━━━━━━━━ 19/19 11.4it/s 1.7s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.8it/s 0.1s
                   all         38         55      0.916       0.99      0.986      0.882

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     85/100      2.85G     0.5538     0.4095   0.003461         14        640: 100% ━━━━━━━━━━━━ 19/19 11.9it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.8it/s 0.1s
                   all         38         55      0.943      0.982      0.987      0.888

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     86/100      2.87G     0.5239     0.3866   0.003356         18        640: 100% ━━━━━━━━━━━━ 19/19 12.1it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.9it/s 0.1s
                   all         38         55      0.937      0.982      0.987      0.884

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     87/100       2.9G      0.594       0.46   0.003451         23        640: 100% ━━━━━━━━━━━━ 19/19 11.9it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.1it/s 0.1s
                   all         38         55       0.93          1      0.987      0.872

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     88/100      2.92G     0.4784     0.3671   0.003114         10        640: 100% ━━━━━━━━━━━━ 19/19 11.3it/s 1.7s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.2it/s 0.1s
                   all         38         55      0.915      0.981      0.985      0.898

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     89/100      2.94G      0.493     0.3509   0.003275         12        640: 100% ━━━━━━━━━━━━ 19/19 11.5it/s 1.7s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.2it/s 0.1s
                   all         38         55      0.945      0.936      0.984      0.914

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     90/100      2.96G     0.5561     0.4347   0.003703         20        640: 100% ━━━━━━━━━━━━ 19/19 11.4it/s 1.7s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.4it/s 0.1s
                   all         38         55      0.901      0.992      0.982      0.914
Closing dataloader mosaic

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     91/100      2.98G     0.4387     0.3808   0.003604          9        640: 100% ━━━━━━━━━━━━ 19/19 9.3it/s 2.1s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.7it/s 0.1s
                   all         38         55      0.901      0.998      0.982      0.889

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     92/100         3G     0.4123     0.3619   0.003198          9        640: 100% ━━━━━━━━━━━━ 19/19 11.7it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.6it/s 0.1s
                   all         38         55      0.899          1      0.983      0.866

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     93/100      3.01G     0.4374     0.3281   0.003311         10        640: 100% ━━━━━━━━━━━━ 19/19 11.6it/s 1.6s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.5it/s 0.1s
                   all         38         55      0.929      0.949      0.987       0.86

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     94/100      3.03G     0.4252      0.336   0.003542          8        640: 100% ━━━━━━━━━━━━ 19/19 11.5it/s 1.7s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.8it/s 0.1s
                   all         38         55      0.955      0.964      0.988      0.866

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     95/100      3.05G     0.4505     0.3831   0.003523          6        640: 100% ━━━━━━━━━━━━ 19/19 11.5it/s 1.7s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.1it/s 0.1s
                   all         38         55      0.958      0.964      0.988      0.887

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     96/100      3.07G     0.4153     0.3188   0.003556          8        640: 100% ━━━━━━━━━━━━ 19/19 11.4it/s 1.7s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 20.9it/s 0.1s
                   all         38         55      0.927      0.964      0.987      0.898

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     97/100      3.09G     0.4108     0.2932   0.003281         12        640: 100% ━━━━━━━━━━━━ 19/19 11.5it/s 1.7s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.3it/s 0.1s
                   all         38         55      0.925      0.964      0.985      0.907

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     98/100       3.1G     0.4294     0.3369   0.003411         10        640: 100% ━━━━━━━━━━━━ 19/19 11.4it/s 1.7s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.9it/s 0.1s
                   all         38         55      0.945      0.931      0.983      0.904

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
     99/100      3.12G     0.4033     0.2863   0.003361          7        640: 100% ━━━━━━━━━━━━ 19/19 11.5it/s 1.7s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 22.1it/s 0.1s
                   all         38         55      0.947      0.927      0.982      0.893

      Epoch    GPU_mem   box_loss   cls_loss    l1_loss  Instances       Size
    100/100      3.14G     0.4012     0.3056   0.003226          9        640: 100% ━━━━━━━━━━━━ 19/19 11.4it/s 1.7s
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100% ━━━━━━━━━━━━ 3/3 21.8it/s 0.1s
                   all         38         55      0.962      0.918      0.981      0.885

100 epochs completed in 0.066 hours.
Optimizer stripped from /runs/detect/kacper-bogusz/gym-plates/exp-5/weights/last.pt, 5.4MB
Optimizer stripped from /runs/detect/kacper-bogusz/gym-plates/exp-5/weights/best.pt, 5.4MB

Validating /runs/detect/kacper-bogusz/gym-plates/exp-5/weights/best.pt...
Ultralytics 8.4.108 🚀 Python-3.12.3 torch-2.8.0+cu128 CUDA:0 (NVIDIA RTX PRO 4500 Blackwell, 32125MiB)
YOLO26n summary (fused): 122 layers, 2,375,031 parameters, 0 gradients, 5.2 GFLOPs

                   all         38         55      0.901       0.99      0.982      0.914
Speed: 0.1ms preprocess, 0.9ms inference, 0.0ms loss, 0.1ms postprocess per image
Results saved to /runs/detect/kacper-bogusz/gym-plates/exp-5
```