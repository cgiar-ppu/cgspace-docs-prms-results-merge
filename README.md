# Merging the CGSpace Attachments Data with PRMS Exported Results
This repo will merge the cgspace metadata and attachments text with the results exported from PRMS. The final output file will list all the PRMS results, and the contents of the documents which are attached to PRMS results as evidence.

- A full-scale extraction of metadata and attachments text from CGSPace items were done. These extracted file contains the metadata associated with each item and most importantly, the text of the documents attached with the items on CGSpace. This was done in another repo (https://github.com/cgiar-ppu/CGSpace-extraction), and final processed output files were upload to CGIAR Sharepoint:

https://cgiar.sharepoint.com/:f:/r/sites/PPUInterim/Shared%20Documents/PPU%20Data%20Team%20-%20dev/Digital%20Products/SNAP/Data%20Sources/CGSpace_Metadata_Attachments_By_Year?csf=1&web=1&e=hbjcsF

These files need to be put into the folder `cgspace_data` and will be used as one of the input

- PRMS Results were exported from Results Dashboard by Julia Utomo in form of an excel file (Results AI.xlsx). This excel file contains multiple tabs.
    - `fact_results` is the main table which contain all result from PRMS, including Non QAed results. It conatins common fields which are common across different result_types i.e., Knowledge Products, Innovation Development. This main sheet can be combined with supporting information from other result types using `result_id` as the primary key
        -  For each result type, we have different tables containing supporting information for that specific result type. For example, innovation readiness level is only applicable to result_type = innovation development.
    - `result_kp` shows the supporting information for result_type = Knowledge Products
    - `result_innovation_dev` shows the supporting informaiton for result_type = Innovation Development
    - `result_main_evidences` contains links of evidences for result types which is available in the `Evidence` tab for each result in the PRMS

https://cgiar-my.sharepoint.com/:x:/r/personal/j_utomo_cgiar_org/Documents/Microsoft%20Teams%20Chat%20Files/Result%20AI.xlsx?d=wbeb1eb06a920499fafe3fb9130891c91&csf=1&web=1&e=6gbYaE

This file need to be put into the folder `prms_results` and will be used as one of the input