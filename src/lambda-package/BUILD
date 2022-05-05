python_sources()

# wheel compatible with all Pythons/platforms: https://pypi.org/project/urllib3/1.26.9/#files
python_requirement(name="urllib3", requirements=["urllib3==1.26.9"])

file(name="complete_platform_lambda", source="./complete_platform_lambda.json")
file(name="complete_platform_mac", source="./complete_platform_mac.json")

python_awslambda(
    name="awslambda",
    handler="lambda.py:handler",
    runtime="python3.9",
    complete_platforms=[":complete_platform_lambda", ":complete_platform_mac"],
)

archive(name="validate_complete_platform_lambda", files=[":complete_platform_lambda", ":complete_platform_mac"], format="zip")
