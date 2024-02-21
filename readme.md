# 0. Prerequisites
Install Docker Desktop

# 1. Docker Build
    docker build -f Dockerfile.local . -t gx/gxdemo:local

# 2. Docker Run 

    docker run -p 8888:8888 -it -v ${pwd}:/app --name gx_demo gx/gxdemo:local

# 3. Run Great Expectations Init
Go to Docker Desktop. Find your container. Go to "Exec". Run:
    great_expectations init
<img src="images\run_great_expectations_init.jpg"/>

# 4. Open Jupyter Notebook
Find the link in the terminal that you ran Docker Run in
<img src="images\open_jupyter_notebook.jpg"/>
Navigate to the Jupyter Notebook tab and open the Notebook
<img src="images\navigate_to_jn.jpg"/>

# 5. Step Through Jupyter Notebook (Yellow Taxi - Manual Expectations)
#### Load one Parquet File (Yellow Taxi)
<img src="images\load_parquet_file1.jpg"/>

#### Create Expectations & Suite Manually
<img src="images\create_expectations_manually1.jpg"/>

#### Import Next Parquet File - validation fails
<img src="images\validate_yt2.jpg"/>

#### Adjust Expectations - validation succeeds
<img src="images\adjust_expectations_yt.jpg"/>

# 6. Step Through Jupyter Notebook (Green Taxi - User Configurable Profiling)
#### Import New Parquet File (Green Taxi)
<img src="images\gt_first_file.jpg"/>

#### Import Next Parquet - Validate Expectations - validation fails
<img src="images\gt_second_file.jpg"/>

#### Configure Green Taxi Dataset (All Parquet Files) & Auto-Profile over Batched Dataset
<img src="images\batch_dataset_profile.jpg"/>

#### Validate Expectations on second Green Taxi file - validation now succeeds
<img src="images\gt_second_file_validation.jpg"/>
