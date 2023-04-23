(Android app+Smart bracelet)

# Abstract

This project aim to study learning analytic methods or tools among the group of children with special educational need in an effective and scientific way. This project focuses on students with special education needs (SEN), in particular to children with Attention Deficit Hyperactivity Disorder (ADHD). Furthermore, this project aims to investigate the relationship between Physical status, which can be indicated by different physiological index, such as heartbeat, blood pressure, and Emotion, and how they can affect study performance.

# Develop android app

To obtain the physiological index, e.g. heart rate, blood pressure, motion sensor data, we choose smart bracelet as our measurement device.

![image alt text](image_0.png)

(iii) heart rate measuring

# Connect to smart bracelet

The smart bracelet we obtained from online shop do not exactly provide a list of API which they claimed to provide, in fact, they only provide a documentation of communication protocol between the bracelet and Android device in HEX data and a simple source code about getting the battery level of the smart bracelet. That being the case, there are difficulties in understanding and implement the communication interface.

![image alt text](image_1.png)

## Obtaining the heart rate data

According to the documentation, the procedure of getting the heart rate data are as below:

(i) send packet data 0x 68 06 01 00 01 70 16 to the smart bracelet to open the heart rate monitoring function

(ii) send packet data 0x 68 06 01 00 00 6f 16 to the smart bracelet to receive the heart rate data

(iii) the packet data similar to  0x 68 86 0e 00 46 00 00 00 00 00 00 00 00 01 00 00 00 00 43 16 will be returned, where 0x46=70bpm is the heart rate.![image alt text](image_2.png)

## Developing app interface

According to the app design protocol, bottom navigation bar is used. It will direct user to different page in a faster and smoother way.

![image alt text](image_3.png)

In the measurement page, to represent the data in an informative way, chart is used. **MPAndroidChart** library is being used to represent the chart.

<img src="image_4.jpg" width="280">

In the ‘quest’ page, user can answer to the question and submit to see the results. If the answer is correct, correct page will be shown and points will be added, else, wrong page will be shown.

<img src="image_5.jpg" width="180"> <img src="image_6.jpg" width="180">

<img src="image_7.jpg" width="180"> <img src="image_8.jpg" width="180">

## Cooperate with company to design a quiz on the teaching robot

![image alt text](image_17.png)

![image alt text](image_18.png)

![image alt text](image_19.png)

![image alt text](1.png)

# Storing time-series data to Android SQLite database for further analysis

![image alt text](image_9.jpg)![image alt text](image_10.jpg)

# Time-series data analysis

# Candidate A

*-very patient*


## Traditional paper

avg. HR: 81.4

Quiz score: 2/6

10:40:44 showing frustrated

10:41:56 showing excited![image alt text](image_11.png)

## Robot

avg. HR: 79.0

Quiz score: 6/10

11:17:10 repeatedly speaking the answers to the robot as the robot cannot detect the answers

![image alt text](image_12.png)

# Candidate B

*-very excited on the robot*

## Traditional paper

avg. HR: 78.8

Quiz score: 3/6

10:44:00 seems excited on the bracelet

10:46:10 standing up

![image alt text](image_13.png)

## Robot

Avg. HR: 89.2

Quiz score: 5/10

10:54:20 singing song

10:56:10 shouting

![image alt text](image_14.png)

## Candidate C

*-easy to be tired due to physical condition*

 Traditional paper

Avg HR:  74.8

Quiz score: 2/6

10:50:10 seem bored on calculation

10:50:30 showing tired by resting on the table

![image alt text](image_15.png)

## Robot

Avg HR: 80.5

Quiz score: 7/10

11:00:40 touching robot head

11:01:50 seems excited on the robot

11:02:37 moving the head of the robot

11:03:10 touching the robot again

![image alt text](image_16.png)

# Conclusion

## 1.The heart rate of the candidates doing quiz on a robot is more flucturated than doing on a traditional A4 paper. 

We can see that from the above graph, also something needed to be noticed is that there are many gaps on the heart rate graph of doing robot quiz, meaning that the change of heart rate is very high.

## 2. The abnormal heart rate can be regarded as a leading indicator of physical actions. 

For candidate B, he stand up at 10:46:10, but the heart rate increase at 10:46:09. When he touch the robot head at 11:00:40, his heart rate drop before at 11:00:39. When he try to move the robot head at 11:02:37, his heart rate drop before at 11:02:35.

## 3. The average heart rate when doing a robot quiz seems to be similar compared to doing a traditional quiz.

Although for candidate C, the average. HR is 89.2 when doing a robot quiz which is much higher than when doing a traditional quiz which is 74.8. Also, the heart rate of candidate B when doing a robot quiz is higher than when doing a traditional quiz. This does not apply to candidate A.
