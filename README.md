<div align="center">
  <a href="http://mit.edu/sparklab/">
    <img align="left" src="docs/media/sparklab_logo.png" width="80" alt="sparklab">
  </a>
  <a href="https://www.mit.edu/~arosinol/">
    <img align="center" src="docs/media/kimeravio_logo.png" width="150" alt="kimera">
  </a>
  <a href="https://mit.edu">
    <img align="right" src="docs/media/mit.png" width="100" alt="mit">
  </a>
</div>

# Kimera

Kimera is a C++ library for real-time metric-semantic simultaneous localization and mapping, which uses camera images and inertial data to build a semantically annotated 3D mesh of the environment. Kimera is modular, ROS-enabled, and runs on a CPU.

Kimera comprises four **modules**:
- A fast and accurate Visual Inertial Odometry (VIO) pipeline ([Kimera-VIO](https://github.com/MIT-SPARK/Kimera-VIO))
- A full SLAM implementation based on Robust Pose Graph Optimization ([Kimera-RPGO](https://github.com/MIT-SPARK/Kimera-RPGO))
- A per-frame and multi-frame 3D mesh generator ([Kimera-Mesher](https://github.com/MIT-SPARK/Kimera-VIO))
- And a generator of semantically annotated 3D meshes ([Kimera-Semantics](https://github.com/MIT-SPARK/Kimera-Semantics))

<p align="center">
    <a href="https://www.youtube.com/watch?v=-5XxXRABXJs">
    <img src="docs/media/kimera_thumbnail.png" alt="Kimera">
    </a>
</p>

Click on the following links to install Kimera's modules and get started! It is very easy to install!

### [Kimera-VIO & Kimera-Mesher](https://github.com/MIT-SPARK/Kimera-VIO)

<div align="center">
    <a href="https://github.com/MIT-SPARK/Kimera-VIO">
      <img src="docs/media/kimeravio_ROS_mesh.gif" alt="Kimera-VIO">
   </a>
</div>

### [Kimera-RPGO](https://github.com/MIT-SPARK/Kimera-RPGO)

<div align="center">
  <a href="https://github.com/MIT-SPARK/Kimera-RPGO">
    <img src="docs/media/RPGO.png" width="700" alt="Kimera-RPGO">
  </a>
</div>

### [Kimera-Semantics](https://github.com/MIT-SPARK/Kimera-Semantics)

<div align="center">
  <a href="https://github.com/MIT-SPARK/Kimera-Semantics">
    <img src="docs/media/kimera_semantics.gif" alt="Kimera-Semantics">
  </a>
</div>

### Chart

![overall_chart](./docs/media/kimera_chart_23.jpeg)

## Citation

If you found any of the above modules useful, we would really appreciate if you could cite our work:

- [1] A. Rosinol, T. Sattler, M. Pollefeys, L. Carlone. [**Incremental Visual-Inertial 3D Mesh Generation with Structural Regularities**](https://arxiv.org/abs/1903.01067). IEEE Int. Conf. on Robotics and Automation (ICRA), 2019. [arXiv:1903.01067](https://arxiv.org/abs/1903.01067)

```bibtex
@InProceedings{Rosinol19icra-incremental,
  title = {Incremental visual-inertial 3d mesh generation with structural regularities},
  author = {Rosinol, Antoni and Sattler, Torsten and Pollefeys, Marc and Carlone, Luca},
  year = {2019},
  booktitle = {2019 International Conference on Robotics and Automation (ICRA)},
  pdf = {https://arxiv.org/pdf/1903.01067.pdf}
}
```

- [2] A. Rosinol, M. Abate, Y. Chang, L. Carlone, [**Kimera: an Open-Source Library for Real-Time Metric-Semantic Localization and Mapping**](https://arxiv.org/abs/1910.02490). IEEE Intl. Conf. on Robotics and Automation (ICRA), 2020. [arXiv:1910.02490](https://arxiv.org/abs/1910.02490).
 
 ```bibtex
 @InProceedings{Rosinol20icra-Kimera,
   title = {Kimera: an Open-Source Library for Real-Time Metric-Semantic Localization and Mapping},
   author = {Rosinol, Antoni and Abate, Marcus and Chang, Yun and Carlone, Luca},
   year = {2020},
   booktitle = {IEEE Intl. Conf. on Robotics and Automation (ICRA)},
   url = {https://github.com/MIT-SPARK/Kimera},
   pdf = {https://arxiv.org/pdf/1910.02490.pdf}
 }
```

- [3] A. Rosinol, A. Gupta, M. Abate, J. Shi, L. Carlone. [**3D Dynamic Scene Graphs: Actionable Spatial Perception with Places, Objects, and Humans**](https://arxiv.org/abs/2002.06289). Robotics: Science and Systems (RSS), 2020. [arXiv:2002.06289](https://arxiv.org/abs/2002.06289).

```bibtex
@InProceedings{Rosinol20rss-dynamicSceneGraphs,
  title = {{3D} Dynamic Scene Graphs: Actionable Spatial Perception with Places, Objects, and Humans},
  author = {A. Rosinol and A. Gupta and M. Abate and J. Shi and L. Carlone},
  year = {2020},
  booktitle = {Robotics: Science and Systems (RSS)},
  pdf = {https://arxiv.org/pdf/2002.06289.pdf}
}
```

- [4] A. Rosinol, A. Gupta, M. Abate, J. Shi, L. Carlone. [**
Kimera: from SLAM to Spatial Perception with 3D Dynamic Scene Graphs
**](https://arxiv.org/abs/2101.06894). [arXiv:2101.06894](https://arxiv.org/abs/2101.06894).

```bibtex
@InProceedings{Rosinol21arxiv-Kimera,
  title = {{K}imera: from {SLAM} to Spatial Perception with {3D} Dynamic Scene Graphs},
  author = {A. Rosinol, A. Violette, M. Abate, N. Hughes, Y. Chang, J. Shi, A. Gupta, L. Carlone},
  year = {2021},
  booktitle = {arxiv},
  pdf = {https://arxiv.org/pdf/2101.06894.pdf}
}
```

## Open-Source Datasets

We use a photo-realistic Unity-based simulator to test Kimera.
The simulator provides:
- RGB Stereo camera (/tesse/left_cam, /tesse/right_cam)
- Depth camera (/tesse/depth_cam)
- Ground-truth 2D Semantic Segmentation (/tesse/seg_cam)
- IMU data (/tesse/imu)
- Ground-Truth Odometry (/tesse/odom)
- 2D Lidar (/tesse/front_lidar/scan)
- TF (ground-truth odometry of robots, and agents) (/tf)
- Static TF (ground-truth poses of static objects) (/tf_static)

Using this simulator, we created several large visual-inertial datasets which feature scenes with and without dynamic agents (humans), as well as a large variety of environments (indoors and outdoors, small and large).
These are ideal to test your Metric-Semantic SLAM and/or other Spatial-AI systems!

- [uHumans](http://web.mit.edu/sparklab/datasets/uHumans/) (released with [3])
- [uHumans2](http://web.mit.edu/sparklab/datasets/uHumans2/) (released with [4])

## Acknowledgments

Kimera is partially funded by ARL [DCIST](https://www.dcist.org/), [ONR RAIDER](https://www.onr.navy.mil/), [MIT Lincoln Laboratory](https://www.ll.mit.edu/), and
[“la Caixa” Foundation](https://becarioslacaixa.net/en/antoni-rosinol-vidal-B004789) (ID 100010434), LCF/BQ/AA18/11680088 (A. Rosinol).

## License

[BSD License](LICENSE.BSD)
