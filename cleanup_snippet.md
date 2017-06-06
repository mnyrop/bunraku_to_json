## POST-PANDAS PROCESSING

IF NEEDED:

`replace "[OLD STRING]" "[NEWSTRING]" -- [FILENAME]`

<sup>(e.g. pesky `NaN`s to `null`s)</sub>

DROP NULLS:

`jq 'del(.[][] | nulls)' [FILENAME]`

CONVERT TO YAML

`python -c 'import sys, yaml, json; yaml.safe_dump(json.load(sys.stdin), sys.stdout, default_flow_style=False)' < [JSONFILE] > [YAMLFILE]`