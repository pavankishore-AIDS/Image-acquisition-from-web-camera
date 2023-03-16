# Image-Acquisition-from-Web-Camera
## Aim
 
Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
###Step 1:
Import cv2 and capture the video using cv2.VideoCapture(0)

###Step 2:
Write the captured image using cv2.imwrite("NewPicture.jpg",frame)

###Step 3:
Resize the image using cv2.resize() to get a four-split screen.

###Step 4:
Rotate the image using cv2.rotate(smaller_frame,cv2.cv2.ROTATE_180)

###Step 5:
Display the image until the key to close the window is pressed.

## Program:
``` Python
### Developed By:Pavan Kishore.M
### Register No:212221230076

## i) Write the frame as JPG file
import cv2

import numpy as np

cap=cv2.VideoCapture (0)

while True:

    ret, frame = cap.read()

    width = int(cap.get(3))

    height=int(cap.get(4))

    image = np.zeros(frame. shape, np. uint8)
    
    smaller_frame = cv2.resize(frame, (0,0), fx = 0.5, fy=0.5)

    image[:height//2, :width//2] = cv2.rotate(smaller_frame,cv2.ROTATE_180)

    image[height//2:, :width//2] = smaller_frame

    image[:height//2, width//2:]= smaller_frame
    
    image[height//2:, width//2:]= smaller_frame

    cv2.imshow('myimage', image)

    if cv2.waitKey(1) == ord('q'):

        break

cap.release()

cv2.destroyAllWindows()


## ii) Display the video
VidCap=cv2.VideoCapture(0)
while(True):
    ret,frame=VidCap.read()
    cv2.imshow('video_image',frame)
    if cv2.waitKey(1) == ord('q'):
        break
VidCap.release()
cv2.destroyAllWindows()



## iii) Display the video by resizing the window
README.md
Image-Acquisition-from-Web-Camera
Aim
Aim:

To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.

Write the frame as JPG
Display the video
Display the video by resizing the window
Rotate and display the video
Software Used
Anaconda - Python 3.7

Algorithm
Step 1:
Import cv2 and capture the video using cv2.VideoCapture(0)

Step 2:
Write the captured image using cv2.imwrite("NewPicture.jpg",frame)

Step 3:
Resize the image using cv2.resize() to get a four-split screen.

Step 4:
Rotate the image using cv2.rotate(smaller_frame,cv2.cv2.ROTATE_180)

Step 5:
Display the image until the key to close the window is pressed.

Program:
### Developed By: Kaushika A
### Register No: 212221230048
## i) Write the frame as JPG file
VidCap2 = cv2.VideoCapture(0)
while(True):
    ret,frame = VidCap2.read()
    cv2.imshow('video_image',frame)
    cv2.imwrite("212221230048.jpg",frame)
    if cv2.waitKey(1) == ord('q'):
        break
    result = False
VidCap2.release()
cv2.destroyAllWindows()



## ii) Display the video
VidCap=cv2.VideoCapture(0)
while(True):
    ret,frame=VidCap.read()
    cv2.imshow('video_image',frame)
    if cv2.waitKey(1) == ord('q'):
        break
VidCap.release()
cv2.destroyAllWindows()

 
## iii) Display the video by resizing the window
cap=cv2.VideoCapture(0)
while(True):
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame = cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2,:width//2]=smaller_frame
    image[height//2:,:width//2]=smaller_frame
    image[:height//2,width//2:]=smaller_frame
    image[height//2:,width//2:]=smaller_frame
    
    cv2.imshow('quadrant_screen',image)
    if cv2.waitKey(1) == ord('q'):
        break
VidCap.release()
cv2.destroyAllWindows()




## iv) Rotate and display the video
cap2=cv2.VideoCapture(0)
while(True):
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame = cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2,:width//2]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:,:width//2]=smaller_frame
    image[:height//2,width//2:]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:,width//2:]=smaller_frame
    
    cv2.imshow('quadrant_rotated_screen',image)
    if cv2.waitKey(1) == ord('q'):
        break
cap2.release()
cv2.destroyAllWindows()








```
## Output

### i) Write the frame as JPG image
</br>
</br>![Screenshot 2023-03-15 141104](https://user-images.githubusercontent.com/94154941/225555717-3472f000-57a1-434c-94b2-bb0e5879a8cb.png)



### ii) Display the video
</br>
![Screenshot 2023-03-15 141104](https://user-images.githubusercontent.com/94154941/225555771-39d56167-288f-45d9-aa94-e7e77cff4075.png)

</br>


### iii) Display the video by resizing the window
</br>
![Screenshot 2023-03-15 143709](https://user-images.githubusercontent.com/94154941/225555833-5010e09f-9447-45c3-a2dc-f76445f72bd8.png)

</br>



### iv) Rotate and display the video
</br>![Screenshot 2023-03-15 143709](https://user-images.githubusercontent.com/94154941/225555850-3cc29222-d8e4-4d89-94eb-e8dbe647a441.png)


</br>





## Result:
Thus the image is accessed from webcamera and displayed using openCV.
