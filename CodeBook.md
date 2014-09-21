**Codebook**

In order to understand that data set that I have created, I felt it was important to start with the following original overview. I have add text following it that explains the tidy data set.

----
*From the original documentation (in the zip file)*

The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals. These time domain signals were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals using another low pass Butterworth filter with a corner frequency of 0.3 Hz. 

Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals . Also, the magnitude of these three-dimensional signals were calculated using the Euclidean norm. 

Finally a Fast Fourier Transform (FFT) was applied to some of these signals.
 
These signals were used to estimate variables of the feature vector for each pattern.

---
Here are the steps that were followed to create the output tidy data set.

1.    Merged the training and the test sets to create one data set.
2.    Extracted the measurements on the mean and standard deviation for each measurement. 
3.    Used descriptive activity names to name the activities in the data set
4.    Provided descriptive variable names. 
5.    Created a second, independent tidy data set with the average of each variable for each activity and  subject.  This was done by taking the mean of the sample data provided.
More information is available in the "README.md" file.

The following describes the transformed data.

Rows 3 - 81 are:
normalized and ***bounded within [-1,1]***.
mean of the input data samples (calculated by subject id and activity) 

 1. "activity" - String indicating the activity that the subject was undertaking: "WALKING", "WALKING_UPSTAIRS", "WALKING_DOWNSTAIRS", "SITTING", "STANDING" and, "LAYING".
 2.  "subjectID" - Integer subject identifier (There are 30 subjects. i.e. 1 represents person 1).  
 3. "BodyAccelerationMeanX" - mean of volunteer's body motion acceleration along the x-axis.
 4. "BodyAccelerationMeanY" - mean of volunteer's body motion acceleration along the y-axis.
 5. "BodyAccelerationMeanZ" - mean of volunteer's body motion acceleration along the z-axis.
 6. "BodyAccelerationStandardDeviationX" - standard deviation of volunteer's body acceleration along the x-axis.
 7. "BodyAccelerationStandardDeviationY" - standard deviation of volunteer's body acceleration along the y-axis
 8. "BodyAccelerationStandardDeviationZ" - standard deviation of volunteer's body acceleration along the z-axis
 9.  "GravityAccelerationMeanX" - mean of acceleration due to gravity, along the x-axis.
 9.  "GravityAccelerationMeanY" - mean of acceleration due to gravity, along the y-axis.
 9. "GravityAccelerationMeanZ" - mean of acceleration due to gravity, along the z-axis.
 9. "GravityAccelerationStandardDeviationX" - standard deviation of movement along the x-axis, due to gravity.
 9. "GravityAccelerationStandardDeviationY" - standard deviation of movement along the y-axis, due to gravity.
 9. "GravityAccelerationStandardDeviationZ" - standard deviation of movement along the z-axis, due to gravity.
 9. "BodyAccelerationJerkMeanX" - mean volunteer's body Jerk (change in body linear acceleration and angular velocity) along the x-axis.
 9. "BodyAccelerationJerkMeanY" - mean volunteer's body Jerk (change in body linear acceleration and angular velocity) along the y-axis.
 9. "BodyAccelerationJerkMeanZ" - mean volunteer's body Jerk (change in body linear acceleration and angular velocity) along the z-axis.
 9. "BodyAccelerationJerkStandardDeviationX" - standard deviation of volunteer's body Jerk (change in body linear acceleration and angular velocity) along the x-axis.
 9. "BodyAccelerationJerkStandardDeviationY" - standard deviation of volunteer's body Jerk (change in body linear acceleration and angular velocity) along the y-axis.
 9. "BodyAccelerationJerkStandardDeviationZ" - standard deviation of volunteer's body Jerk (change in body linear acceleration and angular velocity) along the z-axis.
 9. "BodyGyroscopeMeanX" - mean gyroscopically measured of the volunteer's body in the x direction.
 9. "BodyGyroscopeMeanY" - mean gyroscopically measured of the volunteer's body in the y direction.
 9. "BodyGyroscopeMeanZ" - mean gyroscopically measured of the volunteer's body in the z direction.
 9. "BodyGyroscopeStandardDeviationX" - standard deviation of gyroscopically measured movement of the volunteer's body in the x direction.
 9. "BodyGyroscopeStandardDeviationY" - standard deviation of gyroscopically measured movementof the volunteer's body in the y direction.
 9. "BodyGyroscopeStandardDeviationZ" - standard deviation of gyroscopically measured movement of the volunteer's body in the z direction.
 9. "BodyGyroscopeJerkMeanX"  - mean volunteer's body gyroscopically measured Jerk (change in body linear acceleration and angular velocity) along the x-axis.
 9. "BodyGyroscopeJerkMeanY" - mean volunteer's body gyroscopically measured Jerk (change in body linear acceleration and angular velocity) along the y-axis.
 9. "BodyGyroscopeJerkMeanZ" - mean volunteer's body gyroscopically measured Jerk (change in body linear acceleration and angular velocity) along the z-axis.
 9. "BodyGyroscopeJerkStandardDeviationX"  - standard deviation of volunteer's body gyroscopically measured Jerk (change in body linear acceleration and angular velocity) along the x-axis.
 9. "BodyGyroscopeJerkStandardDeviationY" - standard deviation of volunteer's body gyroscopically measured Jerk (change in body linear acceleration and angular velocity) along the y-axis.
 9. "BodyGyroscopeJerkStandardDeviationZ" - standard deviation of volunteer's body gyroscopically measured Jerk (change in body linear acceleration and angular velocity) along the z-axis.
 9. "BodyAccelerationMagnitudeMean" - mean magnitude (calculated using three axis data) of volunteer's body acceleration.
 9. "BodyAccelerationMagnitudeStandardDeviation" - standard deviation of magnitude (calculated using three axis data) of volunteer's body acceleration.
 9. "GravityAccelerationMagnitudeMean" - mean magnitude (calculated using three axis data) of acceleration due to Gravity.
 9. "GravityAccelerationMagnitudeStandardDeviation" - standard deviation of magnitude of acceleration due to gravity.
 9. "BodyAccelerationJerkMagnitudeMean" - mean magnitude (calculated using three axis data) of volunteer's body Jerk (change in body linear acceleration and angular velocity).
 9. "BodyAccelerationJerkMagnitudeStandardDeviation" - standard deviation of magnitude (calculated using three axis data) of volunteer's body acceleration Jerk (change in body linear acceleration and angular velocity).
 9. "BodyGyroscopeMagnitudeMean" - mean magnitude (calculated using three axis data) of volunteer's body orientation measured with a gyroscope.
 9. "BodyGyroscopeMagnitudeStandardDeviation" - standard deviation of magnitude of volunteer's body orientation measured with a Gyroscope (calculated using three axis data).
 9. "BodyGyroscopeJerkMagnitudeMean" - mean magnitude (calculated using three axis data) of volunteer's body orientation measured with a Gyroscope Jerk (acceleration rate of change).
 9. "BodyGyroscopeJerkMagnitudeStandardDeviation" - standard deviation of volunteer's body orientation measured with a Gyroscope Jerk (acceleration rate of change).
 9. "FFTBodyAccelerationMeanX" - mean x-axis volunteer's body acceleration with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyAccelerationMeanY" - mean y-axis volunteer's body acceleration with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyAccelerationMeanZ" - mean z-axis volunteer's body acceleration with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyAccelerationStandardDeviationX" - standard deviation x-axis volunteer's body acceleration  with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyAccelerationStandardDeviationY" - standard deviation y-axis volunteer's body acceleration  with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyAccelerationStandardDeviationZ" - standard deviation z-axis volunteer's body acceleration  with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyAccelerationMeanFrequencyX" - x-axis mean frequency volunteer's body acceleration with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyAccelerationMeanFrequencyY" - y-axis mean frequency volunteer's body acceleration with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyAccelerationMeanFrequencyZ" - z-axis mean frequency volunteer's body acceleration with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyAccelerationJerkMeanX" - mean Jerk (change in body linear acceleration and angular velocity) on x-axis of volunteer's body acceleration with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyAccelerationJerkMeanY" - mean Jerk (change in body linear acceleration and angular velocity) on y-axis of volunteer's body acceleration with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyAccelerationJerkMeanZ" - mean Jerk (change in body linear acceleration and angular velocity) on z-axis of volunteer's body acceleration with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyAccelerationJerkStandardDeviationX" - standard deviation of Jerk (change in body linear acceleration and angular velocity) on x-axis of volunteer's body acceleration with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyAccelerationJerkStandardDeviationY" - standard deviation of Jerk (change in body linear acceleration and angular velocity) on y-axis of volunteer's body acceleration with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyAccelerationJerkStandardDeviationZ" - standard deviation of Jerk (change in body linear acceleration and angular velocity) on z-axis of volunteer's body acceleration with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyAccelerationJerkMeanFrequencyX" - mean x-axis frequency of volunteer's body Jerk (change in body linear acceleration and angular velocity) with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyAccelerationJerkMeanFrequencyY" - mean y-axis frequency of volunteer's body Jerk (change in body linear acceleration and angular velocity) with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyAccelerationJerkMeanFrequencyZ" - FFT of of mean z-axis frequency volunteer's body Jerk (change in body linear acceleration and angular velocity) with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyGyroscopeMeanX" - mean x-axis volunteer's body orientation measured with a gyroscope - with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyGyroscopeMeanY" - mean y-axis volunteer's body orientation measured with a gyroscope - with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyGyroscopeMeanZ" - mean z-axis volunteer's body orientation measured with a gyroscope - with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyGyroscopeStandardDeviationX" - standard deviation of x-axis volunteer's body orientation measured with a gyroscope - with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyGyroscopeStandardDeviationY" - standard deviation of y-axis volunteer's body orientation measured with a gyroscope - with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyGyroscopeStandardDeviationZ" - standard deviation of z-axis volunteer's body orientation measured with a gyroscope - with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyGyroscopeMeanFrequencyX" - mean frequency of x-axis volunteer's body orientation measured with a gyroscope - with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyGyroscopeMeanFrequencyY" - mean frequency of y-axis volunteer's body orientation measured with a gyroscope - with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyGyroscopeMeanFrequencyZ" - mean frequency of z-axis volunteer's body orientation measured with a gyroscope - with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyAccelerationMagnitudeMean" - mean magnitude of volunteer's body orientation with frequency domain signals obtained by calculating with FFT on the time domain signal (calculated using three axis data).
 9. "FFTBodyAccelerationMagnitudeStandardDeviation" - standard deviation of magnitude of acceleration of volunteer's body - with frequency domain signals obtained by calculating with FFT on the time domain signal (calculated using three axis data).
 9. "FFTBodyAccelerationMagnitudeMeanFrequency" - mean frequency (weighted average of the frequency components) of acceleration of volunteer's body with frequency domain signals obtained by calculating with FFT on the time domain signal (calculated using three axis data).
 9. "FFTBodyAccelerationJerkMagnitudeMean" - mean magnitude of volunteer's body acceleration Jerk (change in body linear acceleration and angular velocity) (os three axis data).
 9. "FFTBodyAccelerationJerkMagnitudeStandardDeviation" - standard deviation of mean volunteer's body acceleration Jerk (change in body linear acceleration and angular velocity) magnitude (calculated using three axis data).
 9. "FFTBodyAccelerationJerkMagnitudeMeanFrequency" - mean frquency ( weighted average of the frequency components, producing a mean) body acceleration Jerk (change in body linear acceleration and angular velocity) magnitude (calculated using three axis data).
 9. "FFTBodyGyroscopeMagnitudeMean" - mean magnitude (in three axes) of volunteer's body orientation measured with a gyroscope - with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyGyroscopeMagnitudeStandardDeviation" - mean standard deviation of magnitude (in three axes) of volunteer's body orientation measured with a gyroscope - with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyGyroscopeMagnitudeMeanFrequency" - mean frequency of magnitude (in three axes) of volunteer's body orientation measured with a gyroscope - with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyGyroscopeJerkMagnitudeMean" - mean magnitude (in three axes) of Jerk (change in body linear acceleration and angular velocity) of volunteer's body orientation measured with a gyroscope - with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyGyroscopeJerkMagnitudeStandardDeviation" - standard deviation of magnitude (in three axes) of Jerk (change in body linear acceleration and angular velocity) of volunteer's body orientation measured with a gyroscope - with frequency domain signals obtained by calculating with FFT on the time domain signal.
 9. "FFTBodyGyroscopeJerkMagnitudeMeanFrequency" - mean magnitude of frequency (in three axes) of Jerk (change in body linear acceleration and angular velocity) of volunteer's body orientation measured with a gyroscope - with frequency domain signals obtained by calculating with FFT on the time domain signal.
