## Introduction

Up until the recent COVID-19 pandemic the greatest social/medical crisis in the United States has been the opioid epidemic, taking 128 lives a day per the CDC. 
Two of the high-level BioGears objectives are lowering the barrier to create medical training content and training the military. 
I believe that a clinically relevant comprehensive model of the naloxone reversal of fentanyl-induced respiratory depression could serve both as a training tool for emergency medical personnel as well as a predictive tool for the dose and frequency of nasally administered naloxone. 
Current guidelines for nasal naloxone usage are ambiguous and dependent on a wait-and-see approach instead of a high-fidelity data-driven predictive model, which risks under-usage of the life-saving drug due to basic human error.

## Description of Work

This project was conducted as a part of Google Summer of Code 2020. 
The main addition this project presents to the BioGears Engine is a model for the systemic absorption of substances through a nasal pathway, which can be compared to the currently available intravenous and oral models in the engine. The use of this model is centered around naloxone and its reversal of fentanyl-induced respiratory depression, however, further adjustments of the model can allow for adjustment of the model to work for other nasally administered drugs. The rough methodology used to create the oral administration path was used for this nasal path with some modifications, however, the model itself was entirely different due to a clear need to adapt to different validation data.

## This involved the following:

1. Configuration of BioGears patient action files to include nasal administration (SESubstanceNasalDose.cpp/h, Drugs.h)

2. Incorporation of ElapsedTime variable in PatientActions.xsd

3. Creation of mathematical nasal disposition model using a solution of differential equations in Drugs.cpp

4. Linkage of nasal model output to BioGears systemic circulation in Drugs.cpp

5. Adjustment of model rate constants to non-carrier administered naloxone in Drugs.cpp

6. Creation of test case scenario files to run simulations based on the model (.xml scenario files)

7. Validation of pharmacokinetic curve for naloxone based on literature data

This was accomplished as shown in the following repositories:

[Main Github Repository](https://github.com/rishisdas/core/tree/f/rdas-NasalDrugAdmin)

[Commits](https://github.com/rishisdas/core/commits/f/rdas-NasalDrugAdmin)

[Git Diff Comparison](https://github.com/BioGearsEngine/core/compare/f/rdas-NasalDrugAdmin...rishisdas:f/rdas-NasalDrugAdmin)

[Pull Request](https://github.com/BioGearsEngine/core/pull/48)
