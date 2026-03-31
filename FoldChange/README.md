To run the notebook, create a new conda environment, then activate the environment and add all dependencies.
```aiignore
conda create -n star_rosemary python
conda activate star_rosemary
pip install "git+https://github.com/sirius-ms/sirius-client-openAPI@star-protocol#subdirectory=client-api_python/generated"
pip install pandas plotly pubchempy
```

Download SIRIUS from https://github.com/sirius-ms/sirius/releases/tag/v6.5.0-SNAPSHOT, then start it using
```aiignore
sirius rest -s -p <port>
```
If not logged in already, log in before by running the below command and inputting your password to the command line coming up.
```aiignore
sirius login -u <username> -p
```

Download the dataset for the notebook from [MSV000080553](https://massive.ucsd.edu/ProteoSAFe/dataset.jsp?task=9a75f69f0f33460293ee3928361ab836) or use our specifically created cell to do it from Python. Note that this might take a while.

Once the dataset is in the same repository as the notebook, and you are logged in and running the REST service, run the notebook. It should be able to run in one go, however it might take some hours depending on your hardware. 