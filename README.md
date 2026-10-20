# Description
This repository uses the BoltzGen universal binder design repository to generate binders to the Human Leukocyte Antigen I (HLA I) expressing the peptide NY-ESO-1 (pMHC) found on tumor cells. The generated designs are meant to mimic T Cell Receptors (TCRm). All credit for the designs go to BoltzGen.

# Background
T-cells recognize antigens presenting different peptides on major histocompatibility complexes (MHCs).[2] The peptide NY-ESO-1 that is presented by MHCs has been linked to cancer.[3] Attempts to recognize this peptide presenting MHC (pMHC) has been a goal for computational biology and has been attempted using RFDiffusion.[4] This repo shows work attempting to generate binder designs for NY-ESO-1 presenting human MHCs (HLA I) using the BoltzGen universal binder design library.[1] The generated protein designs are then to be checked for binding to the target, compared to previous results by the RFDiffusion paper [4] and discussed. 

This is mainly an exercise in protein design on an interesting target and due to this nature, not focused on being novel research. In case of any mistakes in this repository, please reach out.

# Setup


# Design

# Results

# Analysis

# Sources and Licenses
## [1] BoltzGen
This project uses BoltzGen for computational protein binder design.

BoltzGen was developed by Hannes Stärk and colleagues. The software was used to generate and evaluate candidate protein designs using the configuration and workflow documented in this repository.

Software: HannesStark/boltzgen

Paper: Stark et al., BoltzGen: Toward Universal Binder Design (2025).

License: The BoltzGen source code is distributed under the MIT License. See the original repository for its license and applicable notices.

The project-specific contribution consists of the target selection, configuration, execution, and analysis documented here. The underlying BoltzGen software and its design methodology are credited to their original authors.

Repo: https://github.com/HannesStark/boltzgen/tree/main

## Literature

[2] Damian, D. (2026). Human leukocyte antigen (HLA) and tumor immunity: A critical link in cancer immunotherapy. Immunity, Inflammation and Disease, 14(2), e70363. https://doi.org/10.1002/iid3.70363

[3] Webb, A. I., Dunstone, M. A., Chen, W., Aguilar, M.-I., Chen, Q., Jackson, H., Chang, L., Kjer-Nielsen, L., Beddoe, T., McCluskey, J., Rossjohn, J., & Purcell, A. W. (2004). Functional and structural characteristics of NY-ESO-1-related HLA A2-restricted epitopes and the design of a novel immunogenic analogue. *Journal of Biological Chemistry, 279*(22), 23438–23446. https://doi.org/10.1074/jbc.M314066200

[4] Householder, K. D., Xiang, X., Jude, K. M., Deng, A., Obenaus, M., Zhao, Y., Wilson, S. C., Chen, X., Wang, N., & Garcia, K. C. (2025). De novo design and structure of a peptide-centric TCR mimic binding module. *Science, 389*(6758), 375–379. https://doi.org/10.1126/science.adv3813


