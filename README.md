# Federated Learning on Medical Data Imaging

I have worked on Federated Learning on Medical Data Imaging in this project. For this, I have used the BraTS-2020 dataset. Doctors use MRI scans to detect tumour size and shape, but doing it manually takes time and effort. So we can automate it so that the machine can detect the size of the tumour by looking at MRI scans. For this, we can train a machine-learning model. We can pool the hospitals' data and train a centralised model.

However, the problem is that hospitals cannot share their sensitive patient data with the centralised server because of guidelines like HIPAA and GDPR. This can also create the problem of data silos - isolated datasets confined to the institution.

Therefore, we use the concept of Federated Learning. It is a decentralised machine learning paradigm where institutions can train their models locally, and then the model updates can be aggregated and used for the centralised model. So, instead of sending the data to the server, we send the ML algorithm to the local institutions.

**Models Used for Training**:- I have used the UNet and Attention UNet architectures to train the models. Both are designed for biomedical image segmentation tasks.

## BraTS 2020 Dataset

It contains 369 brain MRI scans from glioma patients. Each scan has 4 MRI modalities : 

1. T1-weighted (T1)
2. Contrast-enhanced T1-weighted (T1CE)
3. T2-weighted (T2)
4. Fluid-attenuated inversion recovery (FLAIR)
   
Each scan contains a segmentation mask

0. Background
1. Edema
2. Enhancing Tumor
3. Necrotic Core

## Federated Learning

**Federated Learning Workflow** :- 

Step 1 :- The server creates a unet model with random weights. 

Step 2 :- Server sends the global model to all 5 hospitals.

Step 3 :- Each hospital trains the model on their private MRI scans, computes model updates and then sends only the updated weights to the server.

Step 4 :- Server averages the weights from all hospitals.

Step 5 :- Server replaces the old global model with the averaged weights.

We will repeat steps 2-5 for multiple rounds.
