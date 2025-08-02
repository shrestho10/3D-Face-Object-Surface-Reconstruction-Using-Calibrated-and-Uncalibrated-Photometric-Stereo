This folder Shagoto_CS217_Final_Project contains my final project for CS217
All the codes are done by me expect the last part in uncalibrated (mode 3) normal prediction. For this I have enabled the implementation of SDPS paper. Their git repo is: https://github.com/guanyingc/SDPS-Net.git

Details are below:


Since the project has two parts
So:
Part 1 is in Shagoto_CS217_Final_Project/calibrated     Folder
Part 2 is in Shagoto_CS217_Final_Project/uncalibrated   Folder

Now for part1:
In Shagoto_CS217_Final_Project/calibrated 
There are two folders

First--> Yale
Yale Folder is: Shagoto_CS217_Final_Project/calibrated/Yale
This folder contains code for calibrated photomoetric stereo for Yale dataset
Main code is in :  Shagoto_CS217_Final_Project/calibrated/Yale/Final_Yale_Calibrated_Mesh_Generation.ipynb
Dataset in: Shagoto_CS217_Final_Project/calibrated/Yale/yaleB_data
However, the dataset has been removed for large size and project report submission page asked not to add any image or videos
Generated mesh are in: Shagoto_CS217_Final_Project/calibrated/Yale/generated_mesh
However, the meshes have been removed for large size and project report submission page asked not to add any image or videos


Second--> DiliGenT
DiliGenT Folder is: Shagoto_CS217_Final_Project/calibrated/DiliGenT
This folder contains code for calibrated photomoetric stereo for DiliGenT dataset
Main code is in :  Shagoto_CS217_Final_Project/calibrated/DiliGenT/from lights.ipynb
Dataset in: Shagoto_CS217_Final_Project/calibrated/DiliGenT/Diligent
However, the dataset has been removed for large size and project report submission page asked not to add any image or videos

Generated mesh are in: Shagoto_CS217_Final_Project/calibrated/DiliGenT/generated_mesh_from_light
However, the meshes have been removed for large size and project report submission page asked not to add any image or videos



Now for part2:
In Shagoto_CS217_Final_Project/uncalibrated
There is one folder because uncalibrated is done for DiliGenT only as it has ground truth normals
Folder: Shagoto_CS217_Final_Project/uncalibrated/diligent

Now this folder -->   Shagoto_CS217_Final_Project/uncalibrated/diligent  has 3 modes 

First SVD:
main code: Shagoto_CS217_Final_Project/uncalibrated/diligent/SVD_based-final.ipynb
saved mesh: Shagoto_CS217_Final_Project/uncalibrated/diligent/generated_mesh
dataset: Shagoto_CS217_Final_Project/uncalibrated/diligent/Diligent
However, the dataset and meshes have been removed for large size and project report submission page asked not to add any image or videos



Second: Simple Deep learning   --> Folder: Shagoto_CS217_Final_Project/uncalibrated/diligent/simple deep learning
main code: Shagoto_CS217_Final_Project/uncalibrated/diligent/simple deep learning/simple depth learning.ipynb
saved mesh: Shagoto_CS217_Final_Project/uncalibrated/diligent/simple deep learning/generated_mesh
dataset: Shagoto_CS217_Final_Project/uncalibrated/diligent/DiLiGenT
However, the dataset and meshes have been removed for large size and project report submission page asked not to add any image or videos




Third SDPS: Folder  -->  Shagoto_CS217_Final_Project/uncalibrated/diligent/Complex_Deep_Learning

To get predicted normals from this model run: CUDA_VISIBLE_DEVICES=0 python eval/run_stage2.py --retrain data/models/LCNet_CVPR2019.pth.tar --retrain_s2 data/models/NENet_CVPR2019.pth.tar

This code has to be run inside: Shagoto_CS217_Final_Project/uncalibrated/diligent/Complex_Deep_Learning/SDPS/SDPS-Net

After running that the normals will be found at: Shagoto_CS217_Final_Project/uncalibrated/diligent/Complex_Deep_Learning/SDPS/SDPS-Net/shagoto_predicted_normal

Main code to generate mesh from predicted normals: Shagoto_CS217_Final_Project/uncalibrated/diligent/Complex_Deep_Learning/SDPS/SDPS-Net/Shagoto_SDPS PREDICTED NORMAL_and_ MESH.ipynb

The generated meshes will be found at: Shagoto_CS217_Final_Project/uncalibrated/diligent/Complex_Deep_Learning/SDPS/SDPS-Net/shagoto_predicted_mesh


However, the dataset and meshes have been removed for large size and project report submission page asked not to add any image or videos



Lastly, in Shagoto_CS217_Final_Project/Comparison.ipynb  the angular error comparison of all models are there.

Thank you,
Shagoto Rahman
65044968
shagotor@uci.edu


