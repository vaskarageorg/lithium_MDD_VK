# lithium_MDD_VK
The code analyses patients prescribed lithium, identifying commonly co-prescribed drugs, unique patient counts, and time gaps between prescriptions. It categorizes depression diagnoses by severity, visualises severity proportions in Li/Other groups, and finds coprescribed drug.

1. Summary table for drugs given to PPL:
Empty data frame (interacting_Drugs_DF) listing each drug and filling it in with:
-Number of prescriptions for each drug given to PPL.
-Number of unique PPL individuals.

2. It flags if PPL were seen by a psychiatrist or neurologist-psychiatrist or other specialty, then table is created showing how many were seen by each.

3. Prescription timing differences:
For each drug prescribed along with lithium, it checks the timing between lithium and that drug’s prescriptions.
Calculates, for each patient, the shortest time difference between lithium prescriptions and prescriptions of that drug, then saves those time differences and calculates the median difference in days.

4. Grouping by severity.
ICD-10 codes are used to group by severity (mild, moderate, severe, and specifiers).
This information is joined with Li status and a table is generated to show proportions and confidence intervals.

5. For each analysis, relevant plotting code that generated the submitted Figures is presented (ggplot package).

6. Find common co-prescribed drugs:
For each lithium patient, it lists all other drugs they were prescribed (except lithium itself).
Counts how frequently each other drug is co-prescribed with lithium.
Finds the most common pairs and trios of drugs that appear together.
