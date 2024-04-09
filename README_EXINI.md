# EXINI AI: Scikit Learn

### Fork of https://github.com/scikit-learn/scikit-learn

This is fork with updates enabling build of 0.23.X in python 3.11
The objcative of this fork is to maintain the performance of the mixed gaussian
estimator used to extract liver reference values in aPROMISE.
Later versions of scikit learn (>1.0.0) have updated parameter initializations using a normal distribution
instead of a uniform, changing the convergent estimate in multiple cases.


## Deployment procedure
Deploy package to aws. 

Build wheel using
```
$ python setup.py bdist_wheel -d dist/
```
from the base folder.

Upload new package version to release to aws. If version is x.y.z, upload wheel to
 
s3://dev-deploy-exiniaws-com/pet-analysis-service/packages/scikit-learn/x.y.z/
