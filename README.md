# KITTI_GroundTruth

**Description:** Ground Truth of KITTI dataset (odometry benchmark) for loop closure detection or visual place recognition. KITTI odometry benchmark (http://www.cvlibs.net/datasets/kitti/eval_odometry.php) contains 22 sequences and 11 (00-10) of them are provided with metric positions of each image. Among these 11 sequences, 7 sequences contain loop closures. We label the ground truth of loop closure for these sequences based on the metric positions of each images. Specifically, we compare the position of each image to the others in the sequence and regard the one as a loop if it lies within a radius of 6m.

---
### kittiXXGroundTruth.mat
- **kittiXXGroundTruth.mat** is a binary matrix with size of N x N, where N is the number of images. Entry (i,j) of the matrix is 0 if image i and image j were taken at the different places. When entry (i,j) is equal to 1, it indicates that image i and image j are regareded as the same place, i.e. a loop closure. 

### gnd_kittiXX.mat
- **gnd_kittiXX.mat** lists, for each image in a sequence, the indices of images that are regarded as the same place.


## Related Publications
**Please consider citing our work if you want to use this groundtruth.**

  ```
 @article{zhang2019graph,
  title={Graph-Based Place Recognition in Image Sequences with CNN Features},
  author={Zhang, Xiwu and Wang, Lei and Zhao, Yan and Su, Yan},
  journal={Journal of Intelligent \& Robotic Systems},
  volume={95},
  number={2},
  pages={389--403},
  year={2019},
  publisher={Springer}
}
  ```
