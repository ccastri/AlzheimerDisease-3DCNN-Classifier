# AlzheimerDisease-3DCNN-Classifier
## What is it?
Here is the documentation about the construction and methods used in medical image classification with MRI and 3D convolutional nueral networks. It's important to you'd been prior expirience with neuroscience software as ANTs, SPM12, FREESURFER, FSL or even Nipype among others. As a general view the project has 3 stages: Preprocessing pipeline from Clinica `<T1-linnear>`, just for anatomical images and linnear processing, model construction and trainning with `<deep learning prepare data>` from Clinica too and interpretability analysis. The whole project was coded in python currently we just work with T1-Weighted MRI scans by the ADNI database

# *third-partly software*
First off all we need to set up our environment in such way we run different software plataforms to construct our pipelines and to assess our partial results. So this software resources it's going to be a strong and powerfull help during the nexts developing tasks the table bellow sumarizes the main packages used in neuroscience apllications:

Package name    | Documentation
------------    | -------------
Dcm2nii         | https://nilearn.github.io/
SPM             | https://www.fil.ion.ucl.ac.uk/spm/software/spm12/
ANTs            | https://github.com/ANTsX/ANTs/wiki/Compiling-ANTs-on-Linux-and-Mac-OS
FSL             | https://fsl.fmrib.ox.ac.uk/fsl/fslwiki
FreeSurfer      | https://surfer.nmr.mgh.harvard.edu/fswiki
nilearn         | https://nilearn.github.io/


Previously, we recommend to download the colection images in NIfTI and also you must to download all the .csv tabular data of the participants directly from ADNI page. There is a lot of important information to the pipeline can run without errors. Also, the colection needs to be in a BIDS (Brain Image Data Structure) format. This is a standar format in neuroimaging that allow reasearchers gather the information in a more stetic view by ordering your patients per folders and inside of each folder it's going to be sessions folders containing the particular information per each patient 

``` # ADNI DATASET_DIRECTORY
├── sub-ADNI002S4171
│   ├── SES-M00
│   │   ├── sub-ADNI002S4171_ses-M00_scans.tsv
│   │   └── anat
│   │       └── sub-ADNI002S4171_ses-M00_T1W.nii.gz
│   ├── ...
├── sub-ADNI006S4515
│   ├── ...
├── ...```

In our project the dataset conversion to BIDS was possible thanks to `<adni-2-bids>` from clinica.
