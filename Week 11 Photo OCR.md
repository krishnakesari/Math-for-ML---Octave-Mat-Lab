
# Problem description and pipeline

1. Photo OCR Pipeline (ML pipeline)

i. Understanding context of images (to let algorithm to detect text in image)
a. Text Detection
b. Read text in the regions (character segmentation)
c. Character classification

# Sliding windows

## 1. Pedestrian detection (simpler)
i.  identify pederstrian using fixed aspect ration (Height to width ratio stays same even through the distance varies from camera)
ii. x = pixels in 82x36 image patches
iii. collect large training examples 
      a. positive examples (y = 1) 
      b. negative examples (y = 0)
iv. Run image patches using sliding window detection 
      a. first take small image patch to train
      b. Scale it to large image patch to detect


## 2. Text detection 
i. First Training sample 
   a. Positive examples of text patches (y = 1)
   b. Negative examples of text patches (y = 0)
ii. Test sample using sliding window with one rectangle size
    classifier looks for text 
    a. white color - identified text
    b. gray - identified text with confidence 
    c. black - no text
iii. Apply expansion operator - expanding based on nearby white spaces
iv. Draw boundaries around white regions
v. One dimensional Character segmentation (if only one sentence)
vi. Second training sample
    a. Positive example of images with splitting characters based on space between them (y = 1)
    b. Negative example of images with splitting a character into two (y = 0)
 
# Getting lots of training data
## Artificial data synthesis:

1. Real Data
2. paste a random Font from libraries on radom background
3. Warp data to make character distortions
4. Synthetic data
  
Notes: 
1. use low bias classifier / increasing number of features or hidden neural networks until you have low bias classifier
2. How much work it would be to get 10X as much data as we have ? 
   a. artificial data synthesis
   b. Collect/label it yourself
   c. "Crowd source" data (Eg: Amazon Mechanical Turk System) (have issues with labeller reliability)

# Ceiling Analysis 
## Estimating errors due to each component
1. What parts of the pipeline should you spend the most time trying to improve ? 
2. Which part of process needs more effort ?
3. Where should you allocate scare resources ?

Component | Accuracy
----------| ----------
Overall System | 72 %  
Text detection | 89 %
Character Segmentation | 90 %
Character Recognition | 100 %

Ceiling analysis helps in identifying which parts need more improvement 

Example: Ceiling analysis for image recognition 

Camera Image --> pre-processing (remove background) --> Face detection (1. eyes segmentation 2. nose segmentation 3. mouth segmentation) --> Logistic Regression --> Label



  
  
  







