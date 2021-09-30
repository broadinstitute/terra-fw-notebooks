# terra-fw-notebooks
A repo for Terra Featured Workspace Notebooks owned and maintained by DSP Customer Delivery

Last update: September 30, 2021

Below are listed the notebooks contained in each of Terra's featured workspaces (FW) that are owned and maintained by Customer Delivery. The list is organized by workspace, and several notebooks appear in multiple workspaces. Each workspace is listed in the format of "billing project/workspace name", as it appears at the top of the page when inside the workspace.

----------------------------------------

### Workspace:
help-gatk/GATK4-Germline-Preprocessing-VariantCalling-JointCalling
#### Notebooks:
1-gatk-germline-variant-discovery-tutorial
2-gatk-hard-filtering-tutorial
Workflow Cost Estimator

### Workspace:
help-gatk/Somatic-SNVs-Indels-GATK4
#### Notebooks:
Somatic-Mutect2-Tutorial

### Workspace:
help-gatk/Somatic-CNVs-GATK4
#### Notebooks:
Somatic-CNA-Tutorial

### Workspace:
help-gatk/cnn-variant-filter
#### Notebooks:
gatk-cnn-tutorial
Archived/gatk-cnn-tutorial

### Workspace:
help-gatk/Reproducibility_Case_Study_Tetralogy_of_Fallot
#### Notebooks:
Cluster_Analysis_Tetralogy_of_Fallot

### Workspace:
help-gatk/GATKTutorials-Germline
#### Notebooks:
3-gatk-cnn-tutorial
2-gatk-hard-filtering-tutorial
1-gatk-germline-variant-discovery-tutorial

### Workspace:
help-gatk/GATKTutorials-Somatic
#### Notebooks:
2-somatic-cna-tutorial
1-somatic-mutect2-tutorial

### Workspace:
fc-product-demo/Terra-Notebooks-Quickstart
#### Notebooks:
1_R_environment_setup
2_BigQuery_cohort_analysis
3_Access_and_plot_public_BigQuery_data
0_Intro_to_Jupyter_Notebooks_OPTIONAL

### Workspace:
terra-outreach/DEMO-Working-with-gnomAD
#### Notebooks:
gnomAD-with-Hail
gnomAD-with-BigQuery

### Workspace:
amp-t2d-op/2019_ASHG_Reproducible_GWAS-V2
#### Notebooks:
GWAS_initial_analysis_blank
GWAS_initial_analysis_completed

------------------------------

## Git Actions

This workspace has a list of Git actions, one for each Terra Featured Workspace. Executing the git actions will copy 1 or more of the notebooks in this repository to the respective Terra workspace bucket. 

## Adding New Notebooks

New noteboks should be placed in the ./notebooks folder. Then a Git Actions YML should be created for the notebook(s) using the .github/workflows/publish.yml as a template. 
Enusre the YML ENV block is updated with the workspace propeities the notebooks should be copied to:
```
env:
  NAMESPACE: ''
  WORKSPACE: ''
  WORKSPACE_BUCKET: ''
```

and which notebook(s) to copy is updated in "Publish the notebooks." step.
```
# Publish the notebooks.
        gsutil -m cp <name>.ipynb "gs://${WORKSPACE_BUCKET}/notebooks/"
```

