ArgusEyes Demonstration
===

Example project using [ArgusEyes](https://github.com/amsterdata/arguseyes) in an automated CI workflow using GitHub Actions.


### Label errors: detecting mislabeled image in a computer vision pipeline
 
  * Source code of the ML pipeline [mlinspect-computervision-sneakers.py](pipelines/mlinspect-computervision-sneakers.py)
  * Screening configuration: [mlinspect-computervision-sneakers-labelerrors.yaml](mlinspect-computervision-sneakers-labelerrors.yaml)
  * [Github workflow run detecting the label errors](https://github.com/amsterdata/arguseyes-demo/actions/runs/3602119501/jobs/6068693150)
  * Manual screening: `./eyes arguseyes/example_pipelines/mlinspect-computervision-sneakers-labelerrors.yaml`
  * Notebook for retrospective debugging: [retrospective_labelerrors.ipynb](retrospective_labelerrors.ipynb)

