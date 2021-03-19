# Minerva-Capstone

The repo contains the code notebooks used to generate results for my Capstone project at Minerva Schools. 
This project is an attempt to distinguish between the two mutational subtypes of the EGFR mutation, exon 19 deletions 
and exon 21 substitution, with tiled whole slide images using deep learning (Inception V3). Since the type and acitivty 
of intracellular signaling differs between the two mutational subtypes, which causes different cell fates, I hypothesized
there might be morphological differences and patterns detectable through CNN.  

patient_list.csv file contains the list of patients with EGFR exon 19 deletions and exon 21 substituions in 
The Cancer Genome Atlas's (TCGA) LUAD project. The images is SVS format assocaited with most of the patients can be downloaded 
from the TCGA website. Two types of the SVS slides are available, but the project used only the frozen SVS slides to prevent
heterogeneity. 

The WSI_tiling notebook contains the code using the OpenSlide library to tile the larger SVS files in smaller JPEG files 
before inputting into the neural network. Tiles with more than 50 percent background were discarded. Two types of magnifications, 
20x and 40x, were used in this project. 

The Inception_classification notebooks contains the setup of the model and the training process. The tiled images are stored in
Google Drive and loaded to Google Colab for training. The model was setup with weights pre-trained on ImageNet. 
