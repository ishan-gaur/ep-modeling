# ep-modeling

There are three files in this repository.

main.py houses some scripts to look at the enhancer-promoter contacts at the HBG locus.
The Hi-C data can be found at https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE160425
We used the WT HUDEP2 Hi-C data.

In order to model the promoter activation from acetylated transcription factors, we need to model transcription factor diffusion.
This is done in diffusion.ipynb. There are various options in this file, one of the most important is the HDAC concentration arrangement.
The file also outputs gifs of the diffusion process and exposure.pkl which can be used for further work for a full contact simulation by main.py

free_path.ipynb has scripts to look at the mean free path of the TFs, but this was before I remembered the equations are all for ideal gases :(

For the diffusion simulations, you can look at the git log for a numpy version of the code in case you don't want to use pytorch.
Also you can use the simulation on CPUs by changing the "device" variable to "cpu".
