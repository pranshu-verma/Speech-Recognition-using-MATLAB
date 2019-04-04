# Speech-Recognition-using-MATLAB
In this repository, we will create a Speech Recognition system using Fast Fourier Transform.

### Files in this repository
1. voiceTraining.m ---> It is used to record the user's voice data and store it in the database.
2. voiceFeatures.m ---> It extracts the features of the audio data using FFT (feature is pitch in this example).
3. voiceTesting.m ---> It is compares the test data to the voice data which is already stored in the database.

## How to use
#### Training
1. Open the file "voiceTraining.m" and run the file.
2. Record your voice for 5s.
3. Enter the user number.
4. The features/pitch will be stored in the file named database.mat.

#### Testing
1. Open the file "voiceTesting.m" and run the file.
2. Speak for 5s.
3. Your voice will be compared to other voices in the database.
4. The smallest distance between the test data and the database will be the output class.

for example,
  ```
  user1_pitch = 700
  user2_pitch = 1050
  test_user_pitch = 1000
  d1 = abs(test_user_pitch - user1_pitch) % 1000 - 700 = 300
  d2 = abs(test_user_pitch - user2_pitch) % 1000 - 1050 = 50
  
  ```
  
  Smallest distance is d2 = 50 so the detected class will be User 2.
  
  ### Note_1: I've added comments to every line which indicate their meaning in the MATLAB file.
  ### Note_2: This code only takes a maximum of 2 users. Feel free to update it for as many users you want.
  
  ### Thank You,
  ### Pranshu Verma  
