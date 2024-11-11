# pyEDA Feature Extraction

This code demonstrates how to use the pyEDA toolkit for pre-processing and feature extraction of electrodermal activity (EDA) data.

## What is pyEDA?

pyEDA is an open-source Python toolkit that provides a range of functions for processing and analyzing EDA signals. It includes tools for:

- **Preprocessing:** Filtering, smoothing, and artifact removal.
- **Feature Extraction:** Extracting statistical and time-domain features.
- **Automatic Feature Extraction:** Using an autoencoder to extract latent features.

This code utilizes the pyEDA toolkit to extract features from EDA data using both statistical and automatic methods.

## How to Run the Code

Prepare your EDA data: Ensure your EDA data is in a suitable format (e.g., CSV, NumPy array).
The code assumes the data is stored in a dictionary called data_All under the key 'data' and subkey 'EDA'.

The code will first perform statistical feature extraction using the process_statistical function.
Then, it will train an autoencoder and extract features using the prepare_automatic and process_automatic functions.

Statistical Feature Extraction

The process_statistical function extracts features such as: Number of peaks, Mean GSR, Maximum peak amplitude, Phasic and tonic components

Automatic Feature Extraction
  The prepare_automatic function preprocesses the EDA data and trains an autoencoder.
  The process_automatic function uses the trained autoencoder to extract latent features.

Notes
The code includes an example of reshaping and segmenting EDA data.
The autoencoder architecture consists of 14 layers (7 encoder layers and 7 decoder layers).
You can adjust parameters such as sample_rate, new_sample_rate, segment_width, and epochs to optimize the feature extraction process.
