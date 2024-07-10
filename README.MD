This is the code repository accompanying the manuscript: Disease progression strikingly differs in research and real-world Parkinson’s populations (https://www.nature.com/articles/s41531-024-00667-5)

Abstract:
Characterization of Parkinson’s disease (PD) progression using real-world evidence could guide clinical trial design and identify subpopulations. Efforts to curate research populations, the increasing availability of real-world data, and advances in natural language processing, particularly large language models, allow for a more granular comparison of populations than previously possible. This study includes two research populations and two real-world data-derived (RWD) populations. The research populations are the Harvard Biomarkers Study (HBS, N = 935), a longitudinal biomarkers cohort study with in-person structured study visits; and Fox Insights (N = 36,660), an online self-survey-based research study of the Michael J. Fox Foundation. Real-world cohorts are the Optum Integrated Claims-electronic health records (N = 157,475), representing wide-scale linked medical and claims data and de-identified data from Mass General Brigham (MGB, N = 22,949), an academic hospital system. Structured, de-identified electronic health records data at MGB are supplemented using a manually validated natural language processing with a large language model to extract measurements of PD progression. Motor and cognitive progression scores change more rapidly in MGB than HBS (median survival until H&Y 3: 5.6 years vs. >10, p < 0.001; mini-mental state exam median decline 0.28 vs. 0.11, p < 0.001; and clinically recognized cognitive decline, p = 0.001). In real-world populations, patients are diagnosed more than eleven years later (RWD mean of 72.2 vs. research mean of 60.4, p < 0.001). After diagnosis, in real-world cohorts, treatment with PD medications has initiated an average of 2.3 years later (95% CI: [2.1–2.4]; p < 0.001). This study provides a detailed characterization of Parkinson’s progression in diverse populations. It delineates systemic divergences in the patient populations enrolled in research settings vs. patients in the real-world. These divergences are likely due to a combination of selection bias and real population differences, but exact attribution of the causes is challenging. This study emphasizes a need to utilize multiple data sources and to diligently consider potential biases when planning, choosing data sources, and performing downstream tasks and analyses.

There are two main components: 
1. Extraction
  We include a comparison with regex extraction to allow for a comparison with the LLM based extraction technique as orginally developed in prior work: "Zero-shot interpretable phenotyping of postpartum hemorrhage using large language models" (https://www.nature.com/articles/s41746-023-00957-x) and Code: https://github.com/EmilyAlsentzer/PPH-Extract

  Task specific prompts are available in the manuscript: 

  “Q: Answer the following question with a value between 1 and 5 or NA. What is the Hoehn & Yahr score for the patient in the following note? Note: Note Content A: 3 Q: Answer the following question with a value between 1 and 5 or NA. What is the Hoehn & Yahr score for the patient in the following note? Note: Note Content A:”

2. Analyses and population comparisons
  All code to generate figures 1-3 and definitions are available in the labeled files.


Data Access

All data used in this study are secondary use and therefore the authors must direct those interested in using any data involved to their source: Harvard Biomarkers set is accessible through the Accelerating Medicines Partnership program for Parkinson’s disease https://amp-pd.org/unified-cohorts/hbs and through https://www.bwhparkinsoncenter.org/biobank/. Mass General Brigham EMR; https://rc.partners.org/about/who-we-are-risc/research-patient-data-registry. Optum® Integrated Claims-EHR Data46 (https://www.optum.com/content/dam/optum3/optum/en/resources/fact-sheets/Integrated-Data-product-sheet.pdf), Fox Insight45 https://foxinsight.michaeljfox.org/.

Please direct all questions to beaulieujones [at] uchicago.edu