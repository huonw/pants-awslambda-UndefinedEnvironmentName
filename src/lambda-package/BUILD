python_sources()

# wheel compatible with all Pythons/platforms: https://pypi.org/project/urllib3/1.26.9/#files
python_requirement(name="urllib3", requirements=["urllib3==1.26.9"])
python_requirement(name="mypy", requirements=["mypy==0.910"])
python_requirement(name="types-urllib3", requirements=["types-urllib3==1.26.9"], dependencies=[":mypy"])

file(name="complete_platform_lambda", source="./complete_platform_lambda.json")

python_awslambda(
    name="awslambda",
    handler="lambda.py:handler",
    complete_platforms=[":complete_platform_lambda"],
)
