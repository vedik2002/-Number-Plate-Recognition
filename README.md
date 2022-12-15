# -Number-Plate-Recognition


To run the program install the following dependecies

 pip install opencv-python
 pip install matplotlib
 pip install imutils
 pip install numpy
 pip install easyocr
 
  To make use of easyocr make sure to install pytorch (https://pytorch.org/get-started/locally/)
  
  Program desciption 
  
  For text detection i have used the easyocr library.
  
  To use this I have first filtered the image in order to remove noise from the image after that I have found at the contours associated with the image i have used cv2.RETR_TREE as the mode in order to have an arrangment in the form of tree( making sorting easier) and used cv2.CHAIN_APPROX_SIMPLE as to remove unnecessary coordinates and to get only major coordinates. Next I appplied a for loop to find four coordinates such that it forms square like structure (as the plate is having rectangle structure) Next I created a blank black mask in which i had drawn the area made by finding the coordinates of the contours. Next i created a new_image containing which only containes the license plate. These all steps makes the detection by easyocr easier. After that I used easyocr to get the text and then store it under a text file. 
  
 <img width = "300" src = "https://user-images.githubusercontent.com/91774067/207909302-56cf115c-db93-4364-b3d0-3be0a6334465.png">
 
 
 
 <img width = "300" src = "https://user-images.githubusercontent.com/91774067/207910665-c5d2ab13-1904-4377-8264-8171faeca728.png">

