# 2017-Summer-Reading-List
My reading list for my Summer 2017 internship at Voyage. Material that I found useful or interesting during work.

Note: reuploaded after github wiped my account.


| Paper Link   | Paper Title | Paper Description |
|----------|:----------------:|:-------------------------:|
| [Link](https://arxiv.org/pdf/1611.07759.pdf) |  Multi-View 3D Object Detection Network for Autonomous Driving | Baidu paper that uses object region proposals followed by ROI pooling to generate feature maps for multiple perspeectives (LiDAR Bird's Eye View, LiDAR Fron View, RGB Front View) and then a deep fusion network to generate 3D bounding boxes and class scores.| 
| [Link](https://pdfs.semanticscholar.org/62a2/b1956166ecd5fd8a6b2928f45765f41b76ed.pdf) |    Real-time Object Classification in 3D Point Clouds Using Point Feature Histograms   |    Uses a 2D occupancy grid and connected components to generate non-overlapping bounding boxes. Then generates feature histrograms for each object proposal to classify each object with an SVM. Operates at 10 hz with good performance  |
| [Link](http://www.mrt.kit.edu/z/publ/download/Moosmann_IV09.pdf) | Segmentation of 3D Lidar Data in non-flat Urban Environments using a Local Convexity Criterion |   Uses a heuristic on LiDAR scanners to generate graph directly from the LiDAR scan (without going to point cloud). This graph is then used to quickly generate a attribute at each point which is an approximation for the surface normal. They use this to estimate object segmentations by considering two points in the same object if they are "[locally convex](http://imgur.com/a/wQmwE)". |
| [Link](https://pdfs.semanticscholar.org/89e4/1b0d7194584c5107c480a38bc52782a3fb7a.pdf) | On the Segmentation of 3D LIDAR Point Clouds | Provides a few different methods for scene segmentation from 3D point clouds. Discusses different representations of 3D point clouds that make segmentation more efficient. Shows that removal of ground points is a good way to improve performance.|
| [Link](https://arxiv.org/pdf/1611.08303.pdf) | Deep Watershed Transform for Instance Segmentation | Trains a network to take in RGB image data and learn two masks. The first mask represents the direction at each pixel to the nearest object boundary and the second mask represents the distance to the nearest object boundary. This distance mask is then used as a representation of watershed energy and object boundaries are inferred. Very good instance segmentation results. |
| [Link](https://arxiv.org/pdf/1311.2524.pdf) | Rich feature hierarchies for accurate object detection and semantic segmentation (R-CNN) | The R-CNN paper. Extracts region proposals and generates class scores for each one.|
| [Link](https://arxiv.org/pdf/1504.08083.pdf) | Fast R-CNN | Speeds up R-CNN by sharing computation on object proposals |
| [Link](https://arxiv.org/pdf/1506.01497.pdf) | Faster R-CNN: Towards Real-Time Object Detection with Region Proposal Networks | Uses k anchors and a sliding window to generate region proposals.   |
| [Link](https://arxiv.org/pdf/1703.06870.pdf) | Mask R-CNN |   Improves the idea further by using aligning the regions of interest before transforming a region of interest into a fixed size region of interest feature map. They call this RoI align and it improves performance.  |
| [Link](https://blog.athelas.com/a-brief-history-of-cnns-in-image-segmentation-from-r-cnn-to-mask-r-cnn-34ea83205de4) | A Brief History of CNNs in Image Segmentation: From R-CNN to Mask R-CNN |   Good review of the history of R-CNN and related papers. |
| [Link](https://arxiv.org/pdf/1612.00593.pdf) | PointNet: Deep Learning on Point Sets for 3D Classification and Segmentation | Generates semantic segmentation from unordered point cloud data.  |
| [Link](https://arxiv.org/pdf/1506.02640.pdf) | You Only Look Once: Unified, Real-Time Object Detection | Convolutional object detection but with a single pass. Uses anchors and fixed grid to generate a fixed number of bounding boxes with class scores and probabilities. Idea is that R-CNN and region proposal networks are over complicated and that just making it a single network is a good simple idea to explore. |
| [Link](https://arxiv.org/pdf/1612.08242.pdf) | YOLO9000: Better, Faster, Stronger | YOLO v2 proposes improvements to their previous work that improve performance. Removes fully connected layers, increases resolution so that their detector network doesnt have to learn a new resolution, bounds offsets with a logistic activation so that the model cant put proposals anywhere in the image but only in the local anchor area this makes the model more stable, changes classification vector to not be 1000 long but 1369 long to represent probabilities of intermediate nodes in imagenet and softmaxes along branching points |
| [Link](https://arxiv.org/pdf/1706.08355.pdf) | Deep Semantic Classification for 3D LiDAR Data | They use both an objectness score and a “dynamicity” score to detect and classify objects. Also some other things going on, good read. |

Also this:

https://github.com/takeitallsource/awesome-autonomous-vehicles
   
