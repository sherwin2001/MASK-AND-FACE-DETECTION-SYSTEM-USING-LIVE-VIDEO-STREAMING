# MASK-AND-FACE-DETECTION-SYSTEM-USING-LIVE-VIDEO-STREAMING
## An AI and Computer Vision based Intelligent System to scan and ensure that People wear Mask during COVID outbreak.

###### (This is my final year project. Due to certain privacy policies associated with the college project, I am not permitted to share code files. However, I have added all the important slices of code in the [Project Report Book](https://github.com/sherwin2001/MASK-AND-FACE-DETECTION-SYSTEM-USING-LIVE-VIDEO-STREAMING/blob/master/Project_ReportBook.pdf))  
COVID-19 pandemic is the most life-changing event which startled the world since the year 2020 began.
Further, with the reopening of countries from COVID-19 lockdown, Government and Public health agencies are recommending face mask as essential measures to keep us safe when venturing into public.  
A survey shows that 90% of people in India are aware of wearing a mask, but only 44% of them are wearing a face mask. To monitor that people are following this basic safety principle, a strategy should be developed.  
An automated detector system can be implemented to check and ensure that the principle is followed.  

The project uses **MobileNetV2 Neural Network** Model and **FaceNet Deep Learning** Model trained on **Kaggle** and Self-Constructed images dataset.  
Developed using **Python**, **OpenCv** and **Django**.  

Working demonstration of the project:  

https://user-images.githubusercontent.com/64347893/201717801-7c752f6a-3cc3-4530-97e8-2a1c98049dd5.mp4

Project is divided into three sections:
- Mask Detection system
- Face Recognition system
- Data Storage and Analytics

The workflow diagram of the project is as follows:  <br></br>
![image](https://user-images.githubusercontent.com/64347893/201297478-4a6d3d19-8b96-440f-a889-cadeb4d6d6fc.png) 

1. At first, System will take frame(image) as input from the Camera (IP Webcam).  
2. Then system will process this image using some pre-processing technique.  
3. After the pre-processing step it will send this image to face detection model which will classify each person's face present in the input image as “With Mask” (if mask is found on the face) and “Without Mask” (if mask is not found on the face”).  
4. The second step is to recognize the faces of each person which has been classified as “Without Mask”. (Since, face is properly visible in case of “without mask” it becomes easy to recognize them.)  
5. Now these images will be sent to the face recognition model which will recognize the face if it is present in our database else it will show “Unknown”.  
6. Now, from database system will fetch details of the person and accordingly it will send alert message via email system.
7. If face is recognized, then the person is alerted through associated email id and fined if threshold exceeds.  
