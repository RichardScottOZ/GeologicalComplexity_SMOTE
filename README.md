# Geological Complexity (Fractal Dimension) and SMOTE
Implementation and Data repository for
**Modeling of Cu-Au Prospectivity in the Carajás mineral province (Brazil) through Machine Learning: Dealing with Imbalanced Training Data**
## Authors
[Elias M. G. Prado](mailto:lukas.mosser15@imperial.ac.uk) [Twitter](https://twitter.com/porestar)<sup>1,2</sup>  
[Carlos Roberto de Souza Filho](https://www.imperial.ac.uk/people/o.dubrule)<sup>2</sup>  
[Emmanuel John M. Carranza](https://www.imperial.ac.uk/people/m.blunt)<sup>3</sup>  
[João Gabriel Motta](https://www.imperial.ac.uk/people/m.blunt)<sup>2</sup>  
<sup>1</sup>*Centre for Technological Development, Geological Survey of Brazil - CPRM*  
<sup>2</sup>*Institute of Geosciences, University of Campinas - UNICAMP*  
<sup>3</sup>*Department of Geology, University of KwaZulu-Natal*  

## Results
### Geological Complexity
Geological Complexity Map of Carajás Mineral Province (CMP), Pará, Brazil.    
<img align="left" width="100%" height="100%" src="https://github.com/Eliasmgprado/GeologicalComplexity_SMOTE/blob/master/GeologicalComplexity/imgs/GeolocalComplexity_Results.png"/>    
(a) Map of faults/fractures was produced by interpretation of shaded-relief images derived from the 30 m resolution Shuttle Radar Topographic Mission (SRTM) (b) Geological Complexity map of CMP.

### SMOTE
Mineral Prospectivity Model Flowchart    
<img align="left" width="100%" height="100%" src="https://github.com/Eliasmgprado/GeologicalComplexity_SMOTE/blob/master/SMOTE/imgs/Fig4_flowchart.jpg"/>   


Training F1 scores of SVM models. The scores are arranged by over-sampling/under-sampling rates used to generate the training data points. Models with tendency to over-fit and under-fit are highlighted inside dashed contours. Models trained with same number of mineralized and non-mineralized samples are highlighted in purple.   
<img align="left" width="100%" height="100%" src="https://github.com/Eliasmgprado/GeologicalComplexity_SMOTE/blob/master/SMOTE/imgs/Fig5_SVM_heatmaps_f1_train.jpg"/>   


Testing F1 scores of SVM models. The scores are arranged by over-sampling/under-sampling rates used to generate the training data points. Models with tendency to over-fit and under-fit are highlighted inside dashed contours. Models trained with same number of mineralized and non-mineralized samples are highlighted in purple.  
<img align="left" width="100%" height="100%" src="https://github.com/Eliasmgprado/GeologicalComplexity_SMOTE/blob/master/SMOTE/imgs/Fig6_SVM_heatmaps_f1_test.jpg"/>   


Success-rate curves of SVM-based prospectivity models derived using training data (a) with fixed under-sampling rate of 5% for non-mineralized samples and variable over-sampling rates for mineralized samples ranging from 100-2000%, (b) with fixed over-sampling rate of 100% for mineralized samples and variable under-sampling rates for non-mineralized samples ranging from 5%-100%, and (c) with same number of mineralized and non-mineralized samples. The rate between mineralized and non-mineralized locations for each model is shown in the legend in brackets. 
<img align="left" width="100%" height="100%" src="https://github.com/Eliasmgprado/GeologicalComplexity_SMOTE/blob/master/SMOTE/imgs/Fig7_Models_CAPPs.jpg"/>   


Success-rate and prediction-rate curves of CMP Cu-Au prospectivity models. (a) SVM model trained with 2000% over-sampling rate of mineralized class and 100% under-sampling rate of non-mineralized class (balanced class distribution). (b) SVM model trained without over-sampling of mineralized class (100% over-sampling rate) and without under-sampling non-mineralized class (100% under-sampling rate). (c) SVM model trained without over-sampling of mineralized class (100% over-sampling rate) and 5% under-sampling rate of non-mineralized class (balanced class distribution). (d) WofE model trained with the same input features of the SVM models and the original training mineralized locations. Vertical lines highlight which proportion of Carajás area predicted as prospective for Cu-Au deposits covers 100% of training/test (success-rate/prediction-rate) Cu-Au mineralized locations.
<img align="left" width="100%" height="100%" src="https://github.com/Eliasmgprado/GeologicalComplexity_SMOTE/blob/master/SMOTE/imgs/Fig8_capp.jpg"/>   


Success-rate and prediction-rate curves of CMP Cu-Au prospectivity models.    
<img align="left" width="100%" height="100%" src="https://github.com/Eliasmgprado/GeologicalComplexity_SMOTE/blob/master/SMOTE/imgs/Fig4_flowchart.jpg"/>  
(a) SVM model trained with 2000% over-sampling rate of mineralized class and 100% under-sampling rate of non-mineralized class (balanced class distribution). (b) SVM model trained without over-sampling of mineralized class (100% over-sampling rate) and without under-sampling non-mineralized class (100% under-sampling rate). (c) SVM model trained without over-sampling of mineralized class (100% over-sampling rate) and 5% under-sampling rate of non-mineralized class (balanced class distribution). (d) WofE model trained with the same input features of the SVM models and the original training mineralized locations. Vertical lines highlight which proportion of Carajás area predicted as prospective for Cu-Au deposits covers 100% of training/test (success-rate/prediction-rate) Cu-Au mineralized locations.


## Methodology
### Geological Complexity
![Geological Complexity Methodology](https://github.com/Eliasmgprado/GeologicalComplexity_SMOTE/blob/master/GeologicalComplexity/imgs/Hodkiewicz.png)
#### References
- Ford, A., Blenkinsop, T.G., 2008. Evaluating geological complexity and complexity gradients as controls on copper mineralisation, Mt Isa Inlier. Aust. J. Earth Sci. 55, 13–23.
- Hodkiewicz, P., 2003, The Interplay Between Physical and Chemical Processes in the Formation of World-Class Orogenic Gold Deposits in the Eastern Goldfields Province , Western Australia.
### SMOTE
![SMOTE pseudo-code](https://github.com/Eliasmgprado/GeologicalComplexity_SMOTE/blob/master/SMOTE/imgs/Chawla_SMOTE.png)
#### References
- Chawla, N., Bowyer, K.W., Hall, L.O., Kegelmeyer, W.P., 2002. SMOTE: Synthetic minority over-sampling technique. J. Artif. Intell. Res. 16, 321–357. https://doi.org/10.1613/jair.953
## Instructions
### Pre-requisites
- To run any of the `jupyter` notebooks follow instructions [here](http://jupyter.org/install.html) or install via pip.
```bash
pip install jupyter
```
- In addition we make use of following packages:

    - gdal                      2.3.3  
    - geopandas                 0.4.1  
    - pandas                    0.24.2  
    - matplotlib                3.0.3  
    - rasterio                  1.0.21  
    - numpy                     1.16.3  
    - scipy                     1.2.1  

- We recommend the use of [anaconda](https://www.continuum.io/downloads)
- After installing the packages Clone this repo
```bash
git clone https://github.com/Eliasmgprado/GeologicalComplexity_SMOTE
cd PorousMediaGAN
```
- The codes with instructions and comments are in the `jupyter` notebooks inside the `GeologicalComplexity` and `SMOTE` folders

## Citation
If you use our code for your own research, we would be grateful if you cite our publication
```
@article{EliasPrado2020,
	title={Modeling of Cu-Au Prospectivity in the Carajás mineral province (Brazil) through Machine Learning: Dealing with Imbalanced Training Data},
	author={Prado, E.M.G. and Souza Filho, C.R. and Carranza, E.J.M. and Motta, J.G.},
	journal={Ore Geology Reviews},
	year={2020}
}
```

## Acknowledgement
The code used for Geological Complexity is based on the works [Ford and Blenkinsop (2008)](https://www.tandfonline.com/doi/full/10.1080/08120090701581364) and [Hodkiewicz (2003)](https://research-repository.uwa.edu.au/en/publications/the-interplay-between-physical-and-chemical-processes-in-the-form)    
and the code used for SMOTE is based on the work [Chawla et al. (2002)](https://arxiv.org/pdf/1106.1813.pdf).
