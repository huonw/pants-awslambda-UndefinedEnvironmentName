python_sources()

# wheel compatible with all Pythons/platforms: https://pypi.org/project/urllib3/1.26.9/#files
python_requirement(name="urllib3", requirements=["urllib3==1.26.9"])

python_awslambda(
    name="awslambda",
    handler="lambda.py:handler",
    runtime="python3.9",
)
