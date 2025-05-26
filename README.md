In this project, I have worked on Federated Learning on Medical Data Imaging. For this, I have used the BraTS-2020 dataset. Doctors use MRI scans to detect tumour size and shape, but doing it manually takes time and efforts. So we can automate it so that the machine can detect the size of the tumour by looking at MRI scans. For this, we can train a machine learning model. We can pool the data from the hospitals and can train a centralised model. 

But here comes the problem :- Hospitals can't share their sensitive patitent data to the centralised server because of guidelines like HIPAA and GDPA. This can also create the problem of data silos - isolated datasets confined to the institution.

Therefore, we use the concept of Federated Learning. It is a decentralised machine learning paradigm where institutions can train their models locally and then the model updates can be aggregated and can be used for the centralised model. So instead of sending the data to the server, we are sending the ML algorithm to the local institutions. 

**Models Used for Training** :- I have used the UNet and Attention UNet architectures to train the models. Both are designed for biomedical image segmentation tasks. 


