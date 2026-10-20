# Description
This repository uses the BoltzGen universal binder design repository to generate binders to the Human Leukocyte Antigen I (HLA I) expressing the peptide NY-ESO-1 (pMHC) found on tumor cells. The generated designs are meant to mimic T Cell Receptors (TCRm). All credit for the designs go to BoltzGen.


This is mainly an exercise in protein design on an interesting target and due to this nature, not focused on being novel research. In case of any mistakes in this repository, please reach out.

# Background
T cells recognize antigens presenting different peptides on major histocompatibility complexes (MHCs).[2] The peptide NY-ESO-1 that is presented by MHCs has been linked to cancer.[3] Attempts to recognize this peptide presenting MHC (pMHC) has been a goal for computational biology and has been attempted using RFDiffusion.[4] This repo shows work attempting to generate binder designs for NY-ESO-1 presenting human MHCs (HLA I) using the BoltzGen universal binder design library.[1] The generated protein designs are then to be checked for binding to the target, compared to previous results by the RFDiffusion paper [4] and discussed. 


# Setup
The target for the binder was the HLA-peptide complex in "pMHC target.cif".[5] The input for the BoltzGen run is laid out in "TCRm.yaml". It specifies the target to be the heavy alpha chain of the HLA, while excluding the beta-microglobulin, as it that doesn't appear to be involved in binding. [2] Also marked as non-binding is the region 181 - 274, as that appears visually to be the part involved in membrane binding. Because the T cell needs to be able to bind cancerous cells specifically, differentiating between healthy peptides and cancer peptides presented by the HLA, NY-ESO-1 was included in the binding region. Specifically, the bulge formed by Met<sup>4</sup> and Trp<sup>5</sup> as well as the amino acids Thr<sup>7</sup> and Gln<sup>8</sup> are used as targets, as these have the most exposed residues in the cleft.[4]

The work was done on kaggle notebooks's free NVIDIA T4 GPUs. 
# Design
The script for using BoltzGen's binder design on this target is laid out in "boltzgen-TCRm-design.ipynb". For any other use case, turn to the BoltzGen github repository.[1]

# Results
BoltzGen generated 60 binder designs, out of which 10 passed the internal filters. The top 3 designs based on its internal metrics are laid out in "Rank 1-3 TRCm.cif". The designs bound to the target are also laid out in "Rank 1-3 TRCm with target.cif".
<table>
  <tr>
    <td align="center">
      <img src="images/Rank%201%20design.png" width="250">
      <br>Rank 1
    </td>
    <td align="center">
      <img src="images/Rank%202%20design.png" width="250">
      <br>Rank 2
    </td>
    <td align="center">
      <img src="images/Rank%203%20design.png" width="250">
      <br>Rank 3
    </td>
  </tr>
</table>
# Analysis

# Ethical Considerations

# Sources and Licenses
## [1] BoltzGen
This project uses BoltzGen for computational protein binder design.

BoltzGen was developed by Hannes Stärk and colleagues. The software was used to generate and evaluate candidate protein designs using the configuration and workflow documented in this repository.

Software: HannesStark/boltzgen

Paper: Stark et al., BoltzGen: Toward Universal Binder Design (2025).

License: The BoltzGen source code is distributed under the MIT License. See the original repository for its license and applicable notices.


The projecT specific contribution consists of the target selection, configuration, execution, and analysis documented here. The underlying BoltzGen software and its design methodology are credited to their original authors.

Repo: https://github.com/HannesStark/boltzgen/tree/main

## Literature

[2] Damian, D. (2026). Human leukocyte antigen (HLA) and tumor immunity: A critical link in cancer immunotherapy. Immunity, Inflammation and Disease, 14(2), e70363. https://doi.org/10.1002/iid3.70363

[3] Webb, A. I., Dunstone, M. A., Chen, W., Aguilar, M.-I., Chen, Q., Jackson, H., Chang, L., Kjer-Nielsen, L., Beddoe, T., McCluskey, J., Rossjohn, J., & Purcell, A. W. (2004). Functional and structural characteristics of NY-ESO-1-related HLA A2-restricted epitopes and the design of a novel immunogenic analogue. *Journal of Biological Chemistry, 279*(22), 23438–23446. https://doi.org/10.1074/jbc.M314066200

[4] Householder, K. D., Xiang, X., Jude, K. M., Deng, A., Obenaus, M., Zhao, Y., Wilson, S. C., Chen, X., Wang, N., & Garcia, K. C. (2025). De novo design and structure of a peptide-centric TCR mimic binding module. *Science, 389*(6758), 375–379. https://doi.org/10.1126/science.adv3813

[5] Webb, A. I., Dunstone, M. A., Chen, W., Aguilar, M. I., Chen, Q., Jackson, H., Chang, L., Kjer-Nielsen, L., Beddoe, T., McCluskey, J., Rossjohn, J., & Purcell, A. W. (2004). Functional and structural characteristics of NY-ESO-1-related HLA A2-restricted epitopes and the design of a novel immunogenic analogue. Journal of Biological Chemistry, 279(22), 23438–23446. https://doi.org/10.1074/jbc.M314066200

PDB ID: pdb_00001s9w

