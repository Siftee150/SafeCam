# SafeCam
Video anomaly detection app.<br><br>
Referenced paper for the ML model: https://arxiv.org/abs/2004.07941 <br><br>
ShanghaiTech dataset and ped2 dataset: http://download.impersonator.org:8181/dataset/ <br><br>
Avenue dataset: http://www.cse.cuhk.edu.hk/leojia/projects/detectabnormal/dataset.html<br><br>
Current progress=> 
* Used YOLOv4 to detect objects and extract their location (bounding box center coordinates and area) and appearance features (class probabilities). 
* Used the bounding boxes thus extracted as input to optical flow algorithm (optical flow is used to estimate the change or motion between 2 frames. So previous frame and current frame are needed as inputs)
* Stored the training feature vectors in a list
* Downloaded and integrated the dataset <br><br>
Further evaluation criterias=>
* Should we store feature vectors from training dataset in list or in a file? 
* Try implementing another optical flow algorithm provided by openCV like DeepFlow or Dense RLOF as they are regarded as better than Gunnar FarneBack model 
