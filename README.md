# Weather examples

This repository contains sample Python notebooks that show you what you can do with weather data. You can run these notebooks in a local notebook environment or on the Data Science Experience (DSX) in the IBM Cloud.

All notebooks are tested with Python 3, both locally and on DSX. Please let us know if you have any problems by creating an issue in this repository.  

**Notebooks:**

1. [Weather Forecast with matplotlib](https://github.com/MargrietGroenendijk/weather-demos/blob/master/Weather%20Forecast%20with%20Matplotlib.ipynb). Use the Weather Company Data API to get weather forecast json data based on latitude and longitude, convert this json data into a pandas DataFrame and create a weather chart and map with matplotlib.
2. [Weather Forecast PixieApp]().


### Running a notebook locally

The easiest way to install notebooks is by installing [Anaconda](https://www.anaconda.com/download/) and then type `jupyter notebook` in a Terminal. This will open the notebook environment in a browser. 

### Running a notebook in the IBM Cloud

Another option is to run a notebook in the IBM Cloud. Sign up for a [DSX Lite account](https://datascience.ibm.com/), which will give you a 2 Spark executors and 5GB of Object Storage for free. 

To install **Basemap** (needed for the maps in the first notebook) on DSX follow these steps as a temporary work-around:

1. Create a new notebook with a Python 3 kernel

2. Copy the below code into separate cells and run the notebook

3. Restart the kernel

```!wget "https://downloads.sourceforge.net/project/matplotlib/matplotlib-toolkits/basemap-1.0.7/basemap-1.0.7.tar.gz?r=https%3A%2F%2Fsourceforge.net%2Fprojects%2Fmatplotlib%2Ffiles%2Fmatplotlib-toolkits%2Fbasemap-1.0.7%2F&ts=1494445440&use_mirror=netix"```

```!mv basemap-1.0.7.tar.gz\?r\=https\:%2F%2Fsourceforge.net%2Fprojects%2Fmatplotlib%2Ffiles%2Fmatplotlib-toolkits%2Fbasemap-1.0.7%2F\&ts\=1494445440\&use_mirror\=netix basemap-107.tar.gz```

```!tar xzvf basemap-107.tar.gz```

```!(cd basemap-1.0.7/geos-3.3.3/ && export GEOS_DIR=~/ && ./configure --prefix=$GEOS_DIR && make && make install) > progress.out```

```!cd basemap-1.0.7/ && python setup.py install --user```


