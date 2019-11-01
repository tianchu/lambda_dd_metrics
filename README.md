This library is no longer supported, please use the [Datadog Lambda Layer](https://github.com/DataDog/datadog-lambda-layer-python) instead. Learn more about [monitoring lambda functions using Datadog](https://docs.datadoghq.com/integrations/amazon_lambda/).

## DataDog Metrics for Lambda Functions (python)

To install: `pip install lambda_dd_metrics`

To use:
```
import lambda_dd_metrics
METRICS = lambda_dd_metrics.DataDogMetrics('metric.name.prefix', 'group.name')
METRICS.incr('record.received', 1, ['tag_name:tag_value'])
```

Make sure that your DataDog account has active AWS and Lambda integrations enabled for this to take effect:
http://docs.datadoghq.com/integrations/awslambda/

## For Contributors
* Bump the version in `setup.py`
* Build the package: `python setup.py sdist`
* Upload using [twine](https://pypi.python.org/pypi/twine): `twine upload dist/*`
* If the above fails, make sure you have `~/.pypirc` with the following contents:
```
[pypi]
username = your_username
password = your_password
```
