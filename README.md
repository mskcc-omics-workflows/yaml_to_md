# YAML to Markdown

- [YAML to Markdown](#yaml-to-markdown)
- [yaml\_to\_md](#yaml_to_md)
      - [requirements](#requirements)
      - [usage](#usage)
      - [validate\_yaml](#validate_yaml)
      - [convert\_yaml\_to\_markdown](#convert_yaml_to_markdown)
      - [convert](#convert)

<a id="yaml_to_md"></a>

# yaml\_to\_md

<a id="yaml_to_md.validate_yaml"></a>

#### requirements

- jsonschema
- requests
- typer
- yaml
- tabulate

#### usage

```bash
python yaml_to_md.py -y test.yaml
```

#### validate\_yaml

```python
def validate_yaml(yaml_data, schema_url)
```

The `validate_yaml` function validates a YAML data against a JSON schema retrieved from a given URL.

**Arguments**:

- `yaml_data`: The `yaml_data` parameter is the YAML data that you want to validate. It should be a string containing the YAML content
- `schema_url`: The `schema_url` parameter is a URL that points to a JSON schema file. This schema file defines the structure and validation rules for the YAML data

<a id="yaml_to_md.convert_yaml_to_markdown"></a>

#### convert\_yaml\_to\_markdown

```python
def convert_yaml_to_markdown(data)
```

The `convert_yaml_to_markdown` function takes in a YAML data structure and converts it into a Markdown format.

**Arguments**:

- `data`: The `data` parameter is a dictionary that contains information about a module. It has
the following structure:

**Returns**:

a Markdown-formatted string that contains information about a module. The string includes the module's name, description, keywords, tools, inputs, outputs, authors, and maintainers.

<a id="yaml_to_md.convert"></a>

#### convert

The `convert` function is a Python script that converts a YAML file into a Markdown file based on a specified JSON schema.

**Arguments**:

- `yaml_file` (`Path`): The `yaml_file` parameter is the path to the YAML file that you want to convert to Markdown. It is specified using the `--yaml-file` or `-y` option when running the script. The file should exist and be readable
- `schema_url` (`str`): The `schema_url` parameter is the URL of the JSON schema that will be used to validate the YAML data. In this code, the default value for `schema_url` is set to "https://raw.githubusercontent.com/mskcc-omics-workflows/yaml_to_md/main/nextflow_schema/meta-schema.json" derived from "https://raw.githubusercontent.com/nf-core/modules/master/modules/meta-schema.json>". However, you can provide your own
- `output_file` (`str`): The `output_file` parameter is the path to the output Markdown file. It specifies the file where the converted Markdown content will be saved. By default, the value is set to "output.md". However, you can provide a different file path if desired