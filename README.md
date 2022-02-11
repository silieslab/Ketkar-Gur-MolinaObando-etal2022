# Ketkar-Gur-MolinaObando-etal2022
README for the source code 
Ketkar, Gür, Molina-Obando et al 2022

Behavioral Experiments
All files were generated with Matlab (.m files). 
1.	The function ‘plot_raw_traces_mk’ is used to create figures with turning velocity time traces throughout the manuscript.
2.	The function ‘calculate_peak_velocities_mk’ extracts peak turning velocities per fly per stimulus and mean and SEM statistics over flies. It requires two inputs – an input data structure such as the structures ‘data’ from the behavioural assessment files published with Zenodo (doi: ___) and a desired output file name. Output files extracted for each genotype are also available in this published dataset.
3.	The function ‘plot_peakVelocities_mk’ creates figures that compare peak velocities between genotypes and stimuli.
4.	The script ‘compare_ONslopes_behaviorVsLum’ calculates and plots the slopes of the linear fits to the peak velocity graphs of each genotype.
5.	The script ‘L1_L2_rescue_efficiencies_PermutationTest’ calculates rescue efficiencies and compares them between L1 rescue and L3 rescue using a permutation test.


In vivo two-photon calcium imaging
1.	L1 imaging with ON edges (Figure 1)
L1 imaging data consist of ROI data recorded from individual flies in the form of .pickle files. Each .pickle file contains a list of a self-written class: "ROI" which is defined in the script "Ketkar_Gur_Obando_code_PyROI.py".  Running "Ketkar_Gur_Obando_code_L1_main.py" will implement the required analysis on the .pickle data to quantify L1 responses to ON edges of different luminances. It will also generate plots that were used for creating Figure 1 panels D and E.
In order to run the script, you need additional packages (numpy, matplotlib etc.) to be available in your python environment.

2.	 L1-L2-L3 imaging (Figure 2)
L1, L2 and L3 imaging data consists of ROIs recorded from individual flies in the form of .mat files (example: "180612bg_fly3_Image 4_pData.mat"). Each .mat file contains stimulus and response traces and some meta data. For the random luminance steps stimuilus, the data are processed using "random_luminance_steps_trace_analysis.m" and saved as .mat files ("L1_5steps_BurakData.mat", "L2_5steps_BurakData.mat", "L3_5steps_BurakData.mat"). Then statistical analysis is done and plots are generated using "random_luminances_post_analysis.m". Genotypes are stored and read by the scripts from the file: "MASTER_foldersummary_Burak.txt" Mutual information calculations are done with the package from Ross BC. 2014. Mutual information between discrete and continuous data sets. PLoS ONE 893 9:e87357–e87357. doi:10.1371/journal.pone.0087357.

For the staircase stimulus, the data are processed and plots are generated using "staircase_stim_analysis.m". "staircase_stim_contrast_analysis.m" was used for comparing the contrast properties of L1 and L2.
