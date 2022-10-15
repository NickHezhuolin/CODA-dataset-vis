# CODA-dataset-vis
CODA可视化工具
# Dataset Download
https://coda-dataset.github.io/download.html#link

The instructions for downloading CODA is listed as follows:

1. Download the CODA dataset files using the link provided below and then decompress.
2. Check the CODA Documentation page and the included README file for specific usages of CODA dataset, especially for the related data of KITTI and nuScenes datasets.

After decompression, the data organization is listed as follows:

```
"CODA": {
    |---base                             
        |---corner_case.json            -- COCO-style annotation
        |---kitti_indices.json          -- KITTI sample indices
        |---nuscenes_sample_tokens.json -- nuScenes sample tokens
    |---sample                          -- Proper subset of validation set 
        |---corner_case.json            
        |---images        
            |---*_*.jpg     
    |---val                             -- CODA2022 validation set 
        |---annotations.json            
        |---images        
            |---*_*.jpg     
    |---test                            -- CODA2022 test set 
        |---annotations.json            
        |---images        
            |---*_*.jpg     
    |---README.md                       -- Detailed instructions about CODA usage
}
```

tips:

1. 第1张图-000001_1616005007200.jpg打不开，而且也没有相应的annotations信息
2. base里的corner_case.json中前100的sample部分annotations是对的，但是在`image_id: 101`中间空了一张图，导致后面的annotations都错了;所以要跳过一张图来处理后续的annotation
