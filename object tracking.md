
# Optical flow(SDE)
** workflow **
coner points extraction -> predict the next location by optical flow
## conor points extraction
harris matrix
![algo](https://github.com/zzskyy0301/ReadPapers/blob/main/figures/e5e45cbad219e7592831fba6db7f12f.png)
## optical flow method
[pyramidal tracking algorithm](http://robots.stanford.edu/cs223b04/algo_tracking.pdf): Good at track large objects using optical flow
![algorithm](https://github.com/zzskyy0301/ReadPapers/blob/main/figures/Screen%20Shot%202021-02-01%20at%203.43.17%20PM.png)
![lucas func](https://github.com/zzskyy0301/ReadPapers/blob/main/figures/Screen%20Shot%202021-02-01%20at%203.43.35%20PM.png)

# DeepSORT(SDE)
[codes + notes](https://zhuanlan.zhihu.com/p/90835266)
**workflow**
bbox by YOLO → detections → prediction by  Kalman Filter → match tracks and detections by Hugarian Algo → update Kalman Filter by new detection
## Hungarian Algorithm
** cost matrix**
appearance information & Mahalanobis distance
** function**
## Kalman Filter (Constant Velocity Model)
基于传感器的测量值来更新预测值，以达到更精确的估计。
**predict**
![formla](https://www.zhihu.com/equation?tex=+x%27%3DFx+%5Cqquad%281%29)
![formula](https://www.zhihu.com/equation?tex=P%27+%3D+FPF%5E%7BT%7D%2BQ%5Cqquad%282%29)
(P: covariance matrix at time t; F: state-transfer matrix, Q:system noise,describe reliablities)
**update**
![update](https://github.com/zzskyy0301/ReadPapers/blob/main/figures/%E5%BE%AE%E4%BF%A1%E5%9B%BE%E7%89%87_20210202110040.png)


# CenterTrack
# Real-time JDE
[PAPER](https://arxiv.org/pdf/1909.12605.pdf)

