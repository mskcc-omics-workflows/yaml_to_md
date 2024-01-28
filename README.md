# YAML to Markdown

- [YAML to Markdown](#yaml-to-markdown)
  - [requirements](#requirements)
  - [usage](#usage)
    - [validate yaml](#validate-yaml)
    - [convert yaml](#convert-yaml)
    - [validate and convert yaml](#validate-and-convert-yaml)
  - [validate](#validate)
  - [convert](#convert)
  - [all](#all)
  - [read\_yaml](#read_yaml)
  - [convert\_yaml\_to\_markdown](#convert_yaml_to_markdown)

<a id="yaml_to_md"></a>

## requirements

- python==3.10
- jsonschema==4.21.1
- requests==2.31.0
- typer==0.9.0
- PyYaml==6.0.1

## usage

### validate yaml

```bash
python yaml_to_md.py validate -y test.yaml
```

### convert yaml

```bash
python yaml_to_md.py convert -y test.yaml
```

### validate and convert yaml

```bash
python yaml_to_md.py all -y test.yaml
```

<a id="yaml_to_md.validate"></a>

## validate

The `validate` function validates a YAML data against a JSON schema retrieved from a given URL.

**Arguments**:

- `yaml_file` (`Path`): The `yaml_file` parameter is the path to the YAML file that you want to convert to Markdown. It is specified using the `--yaml-file` or `-y` option when running the script. The file should exist and be readable
- `schema_url`: The `schema_url` parameter is a URL that points to a JSON schema file. This schema file defines the structure and validation rules for the YAML data

<a id="yaml_to_md.convert"></a>

## convert

The `convert` function is a Python script that converts a YAML file into a Markdown file.

**Arguments**:

- `yaml_file` (`Path`): The `yaml_file` parameter is the path to the YAML file that you want to convert to Markdown. It is specified using the `--yaml-file` or `-y` option when running the script. The file should exist and be readable
- `output_file` (`str`): The `output_file` parameter is the path to the output Markdown file. It specifies the file where the converted Markdown content will be saved. By default, the value is set to "output.md". However, you can provide a different file path if desired

<a id="yaml_to_md.all"></a>

## all

The `all` function is a Python script that validates and converts a YAML file into a Markdown file based on a specified JSON schema.

**Arguments**:

- `yaml_file` (`Path`): The `yaml_file` parameter is the path to the YAML file that you want to convert to Markdown. It is specified using the `--yaml-file` or `-y` option when running the script. The file should exist and be readable
- `schema_url` (`str`): The `schema_url` parameter is the URL of the JSON schema that will be used to validate the YAML data. In this code, the default value for `schema_url` is set to "<https://raw.githubusercontent.com/mskcc-omics-workflows/yaml_to_md/main/nextflow_schema/meta-schema.json>" derived from "<https://raw.githubusercontent.com/nf-core/modules/master/modules/meta-schema.json>". However, you can provide one as well
- `output_file` (`str`): The `output_file` parameter is the path to the output Markdown file. It specifies the file where the converted Markdown content will be saved. By default, the value is set to "output.md". However, you can provide a different file path if desired

<a id="yaml_to_md.read_yaml"></a>

## read\_yaml

```python
def read_yaml(yaml_file)
```

The function `read_yaml` reads the contents of a YAML file and returns it as a string.

**Arguments**:

- `yaml_file`: The `yaml_file` parameter is a file object that represents a YAML file

**Returns**:

the contents of the YAML file as a string.

<a id="yaml_to_md.convert_yaml_to_markdown"></a>

## convert\_yaml\_to\_markdown

```python
def convert_yaml_to_markdown(data)
```

The `convert_yaml_to_markdown` function takes in a YAML data structure and converts it into a Markdown format.

**Arguments**:

- `data`: The `data` parameter is a dictionary that contains information about a module.

**Returns**:

a Markdown-formatted string that contains information about a module. The string includes the module's name, description, keywords, tools, inputs, outputs, authors, and maintainers.