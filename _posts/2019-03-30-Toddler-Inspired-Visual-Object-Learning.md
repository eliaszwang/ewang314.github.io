---
title: 'Toddler-Inspired Visual Object Learning'
date: 2019-03-30
collection: posts
categories: 
  - paper review
tags:
  - developmental psych
  - NeurIPS
  - '2018'
---

Summary
------
* Real-world learning systems are limited in the quality and quantity of training datasets they can collect
* Use head-mounted cameras and gaze trackers to collect egocentric images from human child in naturalistic learning contexts
* Child data produces better object models than egocentric adult data
* Child data exhibits unique combination of quality and diversity
* [Paper link](https://papers.nips.cc/paper/7396-toddler-inspired-visual-object-learning)
<!--more-->

Motivation and Related Work
------
* Current machine learning approaches rely on collecting large amounts of data, with generalization ability benefitting from the size
* Human children are very efficient learners, able to recognize roughly 300 object categories by age 2, and generalize to novel instances of newly learned label
* Successful learning in toddlers lies in the qulity of visual data they collect in everyday activities, more coherent and correlated
* Use CNNs to quantify and compare the information content of various datasets

Background and Methods
------
* Toddlers in toy play context (24 toys), learn about objects and names
* Egocentric video and eye tracker for toddler and adult, as well as 3rd person view
* Final dataset of about 200 minutes of video, 30fps, 480 x 640, 70 degree horizontal FOV
* Separate "standard" image dataset of the 24 toy objects with 128 viewpoints per object, 3072 total images - used for test set
* Manually detect object looks using gaze data, average duration was ~1-2 seconds, ~200k frames each for child and parent 
* Used pretrained YOLO to obtain object bounding boxes in each frame
* Simulate foveated vision by prgressively blurring away from center of gaze
* Make datasets with different FOV, between 30-70 degrees in 10 degree increments
* Used pretrained VGG with finetuning for the different datasets, weighting loss based on object frequency
* Test on the "standard" *clean* object dataset

Results
------
* Differences in histogram of object sizes
	* Adult data skewed towards smaller objects (<10% of FOV)
	* Child data has more larger objects (>20% FOV), up to \~50% FOV 
	* ImageNet has much more large objects, up to 100% image size
* Use GIST features to compare low-level visual similarity, toddler has bigger tail of dissimilar instances compared to adults
	* ImageNet is generally more variable since contains instances of different objects
* VGG trained on child data performs better than adult data across various FOV and with or without blurring
* Separated child data into two datasets where objects were smaller or larger than median, based on YOLO bounding boxes 
* Larger object dataset resulted in higher performance
* Create datasets of similar, diverse, and orignal based on GIST features of bounding box cropped objects
	* Similar contained 25% of the instances with minimum total pairwise distance
	* Diverse contained 25% with maximum distance
	* Original contains random subset of original datset
* Original performed best, and diverse better than similar
* Blurring, from simulated foveated vision, generally hurts performance
	* Only helps in adult data with large FOV (>50 degrees)

Conclusion
------
* Data (images) gathered by toddlers during play results in better performance than adult data
* Child data differs from adults in object size and instance diversity, which contribute to performance gain
	* More larger objects
	* More diverse instances
* Toddler dataset contains more information than they have access to
	* Requires (manual) labeling of objects in each frame
* Not clear that better performance of "big objects" isn't just due to the test set generally having large objects too
	* Test performance with original distribution of object size (both big and small) not shown
	* Would having both large and small objects help for a more "realistic" test set
* Would be nice to see results hold with training from scratch
	* Data needed for fine-tuning might be different
* Other task besides object recognition would be interesting
* How well would a "standard" dataset compare to toddler and adult data
	* Can these principles be used to design better "standard" datasets