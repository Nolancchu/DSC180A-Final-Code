# DSC180A-Final-Code
Final code repository for group 1 in capstone group B05 for DSC180A

Unfortunately, all of our initial unproccessed output data is stored on the National Ceter for Atmospheric Research's (NCAR) jupyterhub server, which we've used throughout all of our capstone project. Because of this, our code is not reproducible without access to the server, as output_data_processing.ipynb relies on that original data, and baseline_models.ipynb relies on the output data produced by output_data_processing.ipynb.   

However, if we assume that you're on the NCAR jupyterhub server, these are the steps to replicating our results:

1. For EDA purposes, run all of the cells within explore_CMIP6_data.ipynb
2. In order to process the output data, run all of the cells within output_data_processing, this file may take a lot of time to run, as each Dask dataframe must be loaded before it is written, and there's a lot of data contained within the Dask dataframes. 
3. Store the processed output data within folders named pr_means, pr_perc, and tas_means respectively.
4. Download the preprocessed input data from https://zenodo.org/records/7064308m namely the files CMIP6.zip and test.tar.gz, and store them in input_data and test_data respectively.
5. Now that you have all the data in place, run all of the cells within baseline_models in order to get the model outputs. 