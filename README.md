![image](https://user-images.githubusercontent.com/100893176/161677642-df3129f0-5aec-4e52-a213-78cb28703c7e.png)


# Title
Applying Machine Learning Algorithms to Classify Upper Extremity Actions Using Wrist-Worn Sensors: A Proof-of-Concept Study

[![Background](https://user-images.githubusercontent.com/100893176/161676167-cfe3ac2a-a1ee-4265-b9e2-52719b444a3d.png)](https://www.youtube.com/watch?v=6VEuGwl6hnc&t=1s)

# Purpose
Using a within-subject design, we developed machine learning algorithms to:

- Detect sensor-based upper extremity movements on a repeat functional assessment, the Capabilities of Upper Extremity Test 

- Estimate real-world upper extremity performance during a 24-hour continuous wear period

# Methods: Motor Activity
- 3 right-handed participants without UE deficits wore an ActiGraph GT9x Link watch on their dominant wrist 
- Performed 10 tasks from an spinal cord injury-specific assessment, Capabilities of Upper Extremity Test (CUE-T)
- - Baseline 
- - Following a 24-hour IMU 

# Methods: Classification Process  
We used a 2-level classification process to: 

- Differentiate UE activity from idle (no UE) activity 
- Differentiate gross versus fine motor actions
- Differentiate period versus non-period actions
- Differentiate amongst functional tasks

![image](https://user-images.githubusercontent.com/100893176/161676589-89c49069-89a7-4fe1-bc05-f790dce82de7.png)

# Methods: Annotation Process 
We annotated all accelerometry data (pre and post) to indicate tasks (e.g., Reach Class) using a Python-based annotation tool

![image](https://user-images.githubusercontent.com/100893176/161676788-379ce5f5-fe6a-4052-ac9b-e26a02df3304.png)

# Machine Learning Approach and Algorithm Performance  
- Multiple ML algorithms were trained on baseline CUE-T data (80-20 train-test split; 10-fold cross-validation) with pre-identified sensor-extracted features to classify post-CUE-T data
- A randomized decision trees algorithm using accelerometry features (min, max, mean, and standard deviation) best classified upper extremity activities
- We applied the 2-level classification process to estimate real-world UE performance

![image](https://user-images.githubusercontent.com/100893176/161677036-60b1e350-828d-419a-b0b5-41a1bc3d3f99.png)

# Results: 1st-Level Classification  
- 1st-level classification accuracy was 95.6% for detecting UE versus idle activity 
- On average, participants moved their arm 15.2% of the time during the 24-hour wear period 

# Results: 2nd-Level (Binary) Classification  
- Gross versus fine (overall) = 90.8% 
- Participants performed gross movements more often (91.8%) than fine (8.2%) during the 24-hour wear period

![image](https://user-images.githubusercontent.com/100893176/161677282-6151a1ae-276c-4e27-9556-f6f2d0d733f6.png)
- Periodic versus nonperiodic (overall) = 90.7%
- Participants performed non-periodic movements more often (97.4%) than periodic (2.6%) during the 24-hour wear period 

![image](https://user-images.githubusercontent.com/100893176/161677347-b546224c-8ebb-4a40-bf2a-b5dcfc2a8984.png)

# Results: 2nd-Level (Task-Based) Classification 
- Task-Based (overall) = 82.2% 
- Participants performed lifting (79.7%) tasks most often and isometric (0.3%) tasks least often 

![image](https://user-images.githubusercontent.com/100893176/161677453-043e8a05-5624-4293-974e-4bb93198aa60.png)







