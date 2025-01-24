---
title: Sample Datasets
---

# Sample Datasets

Should this be removed? It was created with an older version of icechunk as I got an error trying to open it with xarray.

## Native Datasets

## Virtual Datasets

### NOAA [OISST](https://www.ncei.noaa.gov/products/optimum-interpolation-sst) Data

> The NOAA 1/4° Daily Optimum Interpolation Sea Surface Temperature (OISST) is a long term Climate Data Record that incorporates observations from different platforms (satellites, ships, buoys and Argo floats) into a regular global grid

Check out an example dataset built using all virtual references pointing to daily Sea Surface Temperature data from 2020 to 2024 on NOAA's S3 bucket using python:

```python
import icechunk

storage = icechunk.s3_storage(
    bucket='earthmover-sample-data',
    prefix='icechunk/oisst.2020-2024/',
    region='us-east-1',
    anon=True,
)

repo = icechunk.Repository.open(storage=storage)
```

![oisst](./assets/datasets/oisst.png)
