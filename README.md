# The new training/testing protocol for CUHK03 (CUHK03-NP)

The new protocol splits the CUHK03 dataset into training set and testing set similar to that of Market-1501, which consist of 767 identities and 700 identities respectively. 

In testing, we randomly select one image from each camera as the query for each identity and use the rest of images to construct the gallery set. We make sure that each query identity is selected by both two cameras, so that cross-camera search can be performed.

In evaluation, true matched images captured in the same camera as the query are viewed as “junk”.  Meaning that junk images is of zero influence to re-id accuracy (CMC/mAP).

The new training/testing protocol split for CUHK03 in our paper is in the "root/evaluation/data/CUHK03/" folder.
- cuhk03_new_protocol_config_detected.mat
- cuhk03_new_protocol_config_labeled.mat


| |  Labeled | detected|
| -------| -----  | ----  |
|#Training |  7,368 | 7,365|  
|#Query      | 1,400 | 1,400|
|#Gallery      | 5,328 | 5,332|

 



- Directory Structure

Followings are the directory structure for CUHK03-NP. 
> cuhk03-np
>> detected/labeled
>>> bounding_box_train/bounding_box_test/query


## [CUHK03-NP-Mask] 
You can also obtain the person mask of CUHK03-NP from [CUHK03-NP-Mask](https://github.com/developfeng/MGCAM/tree/master/data).




 
