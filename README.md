# SafeCam
Video anomaly detection app.<br><br>
Referenced paper for the ML model: https://arxiv.org/abs/2004.07941 <br><br>
ShanghaiTech dataset and ped2 dataset: http://download.impersonator.org:8181/dataset/ <br><br>
Avenue dataset: http://www.cse.cuhk.edu.hk/leojia/projects/detectabnormal/dataset.html<br><br>
Current progress=> 
* Used YOLOv4 to detect objects and extract their location (bounding box center coordinates and area) and appearance features (class probabilities). 
* Used the bounding boxes thus extracted as input to optical flow algorithm (optical flow is used to estimate the change or motion between 2 frames. So previous frame and current frame are needed as inputs)
* Stored the training feature vectors in a list
* Downloaded and integrated the dataset
* Made Opencv GPU enabled
* Normalized the dataset
* Completed training
* Tried RAFT deep learning method for optical flow calculation, but still needs fine tuning
* Completed testing on ped2 dataset, results seem accurate
* AUC of 0.82 (approx) on ped2 dataset!<br><br>
* Completed testing on avenue dataset
* AUC Of 0.71  (approx) on avenue dataset
Further work and remarks=>
* Fine tuning and deciding on RAFT usage 
