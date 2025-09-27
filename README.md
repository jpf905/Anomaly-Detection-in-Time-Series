# Anomaly-Detection-in-Time-Series

##**Anomaly Dection in Time Series**


### **Description**
I utilize an anomaly detection algorithn to analyze a time series data set that contains anomalies. The data set is "ambient_temperature_system_failure.csv" from the Numenta Anomaly Benchmark (NAB) dataset, which contains time-series data of ambient temperature readings from a system that experienced a failure. 

###**Background**
Anomaly detection in time series involves identifying unusual patterns, deviations, or unexpected behaviors that do not conform to the normal dynamics of the data. Traditional statistical methods often struggle with complex, nonlinear patterns, making deep learning approaches more effective.

An **autoencoder** is a type of neural network designed to learn compressed representations of data. It consists of two main parts:

*   **Encoder**: compresses the input into a lower-dimensional latent representation.
*   **Decoder**: reconstructs the original input from this compressed form.

For time series anomaly detection, the autoencoder is trained on sequences of “normal” behavior. The model learns to reconstruct these sequences accurately. When the autoencoder encounters anomalous data, it fails to reconstruct it well, resulting in a higher reconstruction error. By setting a threshold on the reconstruction error, we can classify whether a time step (or sequence window) is normal or anomalous.


###**Libraries Used**
*   Pandas
*   Numpy
*   Matplotlib
*   Seaborn
*   Sklearn
*   TensorFlow

###**Procedure**
1.  Preprocess and normalize the time series.
2.  Segment the data into windows of fixed length.
3.  Train the autoencoder on normal data only.
4.  Compute reconstruction error for test sequences.
5.  Flag sequences with errors above a chosen threshold as anomalies.

This approach is powerful for detecting rare events such as fraud, equipment failures, or cybersecurity breaches, where normal behavior is predictable but anomalies are critical to catch.
