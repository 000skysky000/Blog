# 3DGS算法调研

- [GitHub](https://github.com/graphdeco-inria/gaussian-splatting)

- Awesome 3D Gaussian Splatting Resources
  - [GitHub](https://github.com/MrNeRF/awesome-3D-gaussian-splatting?tab=readme-ov-file#reviews)

## 综述论文

首篇综述：A Survey on 3D Gaussian Splatting

第二篇综述：相对比较全面，推荐精读 3D Gaussian as a New Vision Era: A Survey

- [知乎](https://zhuanlan.zhihu.com/p/683723004)
- [arvix](https://arxiv.org/pdf/2402.07181)

第三篇综述：涵盖了更多最新进展

- [Recent Advances in 3D Gaussian Splatting](https://blog.csdn.net/c2a2o2/article/details/137871400)
- [bilibili](https://www.bilibili.com/read/cv33416481/)
- [arvix论文](http://arxiv.org/pdf/2403.11134)

## Colmap

- [调参指南](https://www.bilibili.com/read/cv32336778/)
- [官方文档](https://colmap.github.io/)

    colmap feature_extractor --database_path /data2/songkaiyu/3dgs/pkg_office/database.db2 --image_path /data2/songkaiyu/3dgs/pkg_office/images --SiftExtraction.max_num_features 8000 --ImageReadercamera_model PINHOLE

    colmap feature_extractor \
    --database_path /data2/songkaiyu/3dgs/pkg_office/database.db \
    --image_path /data2/songkaiyu/3dgs/pkg_office/images

    colmap exhaustive_matcher --database_path /data2/songkaiyu/3dgs/pkg_office/database.db2 --SiftMatching.guided_matching 1

    colmap point_triangulator \
    --database_path /data2/songkaiyu/3dgs/pkg_office/database.db2 \
    --image_path /data2/songkaiyu/3dgs/pkg_office/images \
    --input_path /data2/songkaiyu/3dgs/pkg_office/sparse/0 \
    --output_path /data2/songkaiyu/3dgs/pkg_office/sparse/1

## Viewer

- [PlayCanvas glTF Viewer GitHub](https://github.com/playcanvas/model-viewer)

- [https://playcanvas.com/model-viewer](https://playcanvas.com/model-viewer)
  
- [Splat](https://antimatter15.com/splat/)

- [Editor](https://playcanvas.com/supersplat/editor)

# Gaussian Editor

论文：  

中文：[CSDN](https://blog.csdn.net/su_zy_/article/details/134762776)


## 3DGS调参
- 默认
     
    --position_lr_init 0.000016 --scaling_lr 0.001


- 推荐
     
    --position_lr_init 0.000016 --scaling_lr 0.001

- 变电站
  
    python train.py -s ../biandianzhan_3dgs/ -m ../biandianzhan_3dgs/output_r4 --position_lr_init 0.000016 --scaling_lr 0.001 --position_lr_final 0.00000016


## 
