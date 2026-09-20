**🧬 Cancer Classification Model Using Gene Expression Data**

**📌 Overview**
In this project, I will explore whether gene expression data can be used to help detect cancer by building a machine learning model. My goal is to build a simple proof of concept model that uses gene expression data collected from next-generation sequencing to predict whether cancer is present. The dataset contains expression levels for many genes along with a cancer label indicating whether cancer is present. I use this data to train and develop a classification model that estimates cancer risk from genetic patterns. My goal in this report is not to create a finished medical tool but to assess whether gene expression data contains enough signal to support early cancer detection and justify further development.

**🗂 Project Structure**
├── data/                                  # data source and information
├── README.md                              # this file
├── cancer-classification.ipynb            # analysis and machine learning workflow
├── index.html                             # rendered notebook (open in browser)

## 📊 Dataset**
In this project, I use a gene expression dataset collected from next-generation sequencing experiments. Each observation represents a single biological sample and the features correspond to measured gene expression levels such as “gene_####”. The target variable “cancer” indicates whether the sample is associated with cancer. This dataset allows me to study how patterns in gene expression differ between cancer and non-cancer samples. To support unbiased model evaluation, I split the data into training and test sets while making sure the class proportions stay the same in both.

The goal of my analysis is to use these gene expression profiles to predict whether a biological sample is associated with cancer so understanding the available variables is important. A full description of the features used in this model is provided in the data dictionary below.

**Data Dictionary:**
- Target variable (object):
 - cancer: the clinically determined cancer type associated with the tissue sample, possible values include:
 - BRCA: Breast Invasive Carcinoma
 - PRAD: Prostate Adenocarcinoma
 - KIRC: Kidney Renal Clear Cell Carcinoma
 - LUAD: Lung Adenocarcinoma
 - COAD: Colon Adenocarcinoma
- Features (float64):
 - gene_####: continuous gene expression measurement for gene number #### in the dataset. These values represent quantified  -  - expression levels obtained using an Illumina HiSeq next-generation sequencing platform.

**🔬 Methods**
- Performed exploratory data analysis on the gene expression data
- Split the data into stratified training and test sets
- Used median imputation to handle missing values
- Built a gradient boosted tree classification model using scikit-learn
- Used GridSearchCV with 5-fold cross-validation for hyperparameter tuning
- Evaluated the final model using test accuracy and a confusion matrix

**🛠️ Tools**
- Python
- pandas
- scikit-learn






