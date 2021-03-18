# Minerva-Capstone
The repo contains the code notebooks used to generate results for my Capstone project at Minerva Schools. 
This project is an attempt to distinguish between the two mutational subtypes of the EGFR mutation, exon 19 deletions 
and exon 21 substitution, with tiled whole slide images using deep learning (Inception V3). 

The patient_list.csv file contains the list of patients with EGFR exon 19 deletions and exon 21 substituions in 
the Cancer Genome Atlas's LUAD project. The images is SVS format assocaited with the patients can be downloaded 
from the project website. 

The WSI_tiling notebook is the python notebook where I tile the larger SVS files in smaller JPEG files before inputting
into the neural network. The Inception_classification notebooks contains the setup of the model and the training process.
