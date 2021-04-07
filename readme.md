# Automated Recyclable Detection
This work is part of a larger research project conducted at [The Machine Perception & Cognitive Robotics Lab](https://mpcrlab.com/). The full academic paper can be found [here](https://drive.google.com/file/d/1kiH28ICswPOceoBOHHWpyreT4L5OH55Q/view?usp=sharing). 

### Abstract
Waste production per capita has been consistently increasing, generating more municipal solid waste every year. Processing plants can help address this abundance by repurposing recyclables into raw materials through the use of specialized machinery and human sorters. New contamination policies, however, call for cleaner raw materials, thereby requiring additional processing, making it more challenging for facilities to recycle profitably [1]. Items that previously could have been recycled are now being directly sent to landfills, exacerbating the global landfill crisis. Additionally, there are concerns for the human sorters with respect to operating efficiency and health care (pathogen exposure and hearing loss). To address these issues, several companies have begun exploring the implementation of robotics in the recycling process. This report aims to evaluate the potential efficacy of deep-learning-based approaches through a system capable of real-time segmentation and contamination detection. In order to build a dataset, conveyor belt streams containing a variety of recyclables were recorded directly overhead at sixty frames per second. Using the VGG Image Annotation tool, each item present in a given frame was segmented and classified as contamination or non-contamination [2]. A pretrained Mask-RCNN, a convolutional neural network optimized for instance segmentation tasks, was finetuned over this footage for 1000 iterations [3]. In early-stage testing with a smaller-line containing only high-density polyethylene (HDPE), the model was capable of identifying and segmenting items in ∼780 milliseconds with a 95.8% accuracy. These results indicate that with further development the system has the potential to beneficially assist active processing plants. 

**References**
1.  United States Environmental Protection Agency. (2017). National Overview: Facts and Figures on Materials, Wastes, and Recycling. Retrieved from https://www.epa.gov/facts-and-figures-about-materials-waste-and-recycling/national-overview-facts-and-figures-materials#main-content.

2.  Russell, B. C., Torralba, A., Murphy, K. P., & Freeman, W. T. (2008). LabelMe: a database and web-based tool for image annotation. International journal of computer vision, 77(1-3), 157-173.

3.  He, K., Gkioxari, G., Dollár, P., & Girshick, R. (2017). Mask r-cnn. In Proceedings of the IEEE international conference on computer vision (pp. 2961-2969).

### Model Output Instances
![image](https://imgur.com/jnCMISF.png)
![image](https://imgur.com/4TQqxyF.png)


