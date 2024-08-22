# qReadRaman
DESCRIPTION
The qREAD-Raman program is a software tool designed for analyzing and interpreting Raman spectral datasets using machine learning. This automated software operates in two phases: preprocessing and analysis. During the preprocessing stage, noise reduction and spectral normalization are performed. The second stage focuses on assessing the health of tomato plants, specifically for the early detection of two bacterial diseases: bacterial canker of tomato, caused by Clavibacter michiganensis subsp. michiganensis (Cmm), and tomato vein-greening associated with Candidatus Liberibacter solanacearum (CLso).

INSTALLATION
The software was developed using Node.js version 21.4.0, Express version 4.18.2, and the Synaptic package version 1.1.4.
This code enables qReadRaman service on a Linux platform with node.js capabilities.
To run it, download the latest release from the link provided on this page and unzip it to a local folder. In a terminal, with the current directory set to the unzipped local folder, execute the following command:
node server.js
Optionally, if you have a KDE environment installed, you can execute the install.sh file.
The user graphical interface of qReadRaman will be displayed from port 3100. Once the server is running locally, you can access the GUI from a web browser at the URL:
http://localhost:3100

USAGE

The informatics tool is divided into two visualization stages. 
1.	The first stage was designed to preprocess Raman spectral datasets, involving noise reduction by applying mathematical methods such as outlier removal, baseline correction, fluorescence removal, smoothing, and spectral normalization. Only after the datasets have been normalized can the second stage, focused on disease prediagnosis, be correctly activated. 
2.	The second stage is designed for the early detection of two tomato diseases: Cmm and CLso. Preprocessed and normalized spectral datasets are used to train classifiers. The process begins by selecting either a binary model (Cmm-Healthy or CLso-Healthy) or the available three-class model (CLso-Cmm-Healthy). It then proceeds with dimensionality reduction of the datasets through Principal Component Analysis. Finally, the classification is performed using a consensus approach that incorporates five different classifiers: Multilayer Perceptron, Partial Least Squares-Discriminant Analysis, Linear Discriminant Analysis, Long Short-Term Memory, and K-nearest neighbors.
