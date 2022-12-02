ArgusEyes Demonstration
===

Example project using [ArgusEyes](https://github.com/amsterdata/arguseyes) in an automated CI workflow using GitHub Actions.

**ArgusEyes** is a system which allows data scientists to declaratively specify a variety of pipeline issues that they are concerned about. Subsequently, ArgusEyes can instrument, execute and screen the pipeline for the configured pipeline issues, as part of continuous integration processes. ArgusEyes detects complex issues by tracking record-level provenance and understanding the semantics of operations in ML pipelines. ArgusEyes was presented as an [abstract at CIDR'22](https://ssc.io/pdf/arguseyes.pdf).

We provide three example scenarios (Note that you have to locally install ArgusEyes first to execute them). You can run ArgusEyes to execute the pipeline and screen it for a particular issue issue. Subsequently, you can use an interactive notebook to determine the root cause of the pipeline issue and fix it.

### Label errors: detecting mislabeled image in a computer vision pipeline
 
  * Source code of the ML pipeline [mlinspect-computervision-sneakers.py](pipelines/mlinspect-computervision-sneakers.py)
  * Screening configuration: [mlinspect-computervision-sneakers-labelerrors.yaml](mlinspect-computervision-sneakers-labelerrors.yaml)
  * [Github workflow run detecting the label errors](https://github.com/amsterdata/arguseyes-demo/actions/runs/3602119501/jobs/6068693355)
  * Manual screening: `./eyes mlinspect-computervision-sneakers-labelerrors.yaml`
  * Notebook for retrospective debugging: [retrospective_labelerrors.ipynb](retrospective_labelerrors.ipynb)


### Data leakage: detecting data leakage in a price prediction pipeline
 
  * Source code of the ML pipeline [mlflow-regression-nyctaxifare.py](pipelines/mlflow-regression-nyctaxifare.py)
  * Screening configuration: [mlflow-regression-nyctaxifare-dataleakage.yaml](mlflow-regression-nyctaxifare-dataleakage.yaml)
  * [Github workflow run detecting the leakage](https://github.com/amsterdata/arguseyes-demo/actions/runs/3602119501/jobs/6068693150)
  * Manual screening: `./eyes mlflow-regression-nyctaxifare-dataleakage.yaml`
  * Notebook for retrospective debugging: [retrospective_dataleakage.ipynb](retrospective_dataleakage.ipynb)

### Fairness: detecting fairness violations in a credit scoring pipeline
 
  * Source code of the ML pipeline [openml-classification-incomelevel.py](pipelines/openml-classification-incomelevel.py)
  * Screening configuration: [openml-classification-incomelevel-fairness.yaml](openml-classification-incomelevel-fairness.yaml)
  * [Github workflow run detecting the fairness violation](https://github.com/amsterdata/arguseyes-demo/actions/runs/3602119501/jobs/6068693482)
  * Manual screening: `./eyes openml-classification-incomelevel-fairness.yaml`
  * Notebook for retrospective debugging: [retrospective_fairnessviolation.ipynb](retrospective_fairnessviolation.ipynb)
