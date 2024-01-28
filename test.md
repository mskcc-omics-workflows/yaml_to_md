# Table of Contents

* [yaml\_to\_md](#yaml_to_md)
  * [validate](#yaml_to_md.validate)
  * [convert](#yaml_to_md.convert)
  * [all](#yaml_to_md.all)
  * [read\_yaml](#yaml_to_md.read_yaml)
  * [convert\_yaml\_to\_markdown](#yaml_to_md.convert_yaml_to_markdown)

<a id="yaml_to_md"></a>

# yaml\_to\_md

<a id="yaml_to_md.validate"></a>

#### validate

```python
@app.command()
def validate(yaml_file: Path = typer.Option(...,"-y", "--yaml-file", exists=True, file_okay=True, dir_okay=False, readable=True, resolve_path=True, help="Path to the YAML file."), schema_url: str = typer.Option(
        "https://raw.githubusercontent.com/mskcc-omics-workflows/yaml_to_md/main/nextflow_schema/meta-schema.json",
        "--schema-url",
        "-s",
        help="URL of the JSON schema.",
    ))
```

The `validate` function validates a YAML data against a JSON schema retrieved from a given URL.

**Arguments**:

- `yaml_file` (`Path`): The `yaml_file` parameter is the path to the YAML file that you want to convert to
Markdown. It is specified using the `--yaml-file` or `-y` option when running the script. The file
should exist and be readable
- `schema_url`: The `schema_url` parameter is a URL that points to a JSON schema file. This
schema file defines the structure and validation rules for the YAML data

<a id="yaml_to_md.convert"></a>

#### convert

```python
@app.command()
def convert(yaml_file: Path = typer.Option(...,"-y", "--yaml-file", exists=True, file_okay=True, dir_okay=False, readable=True, resolve_path=True, help="Path to the YAML file."), output_file: str = typer.Option(
        "output.md",
        "--output-file",
        "-o",
        help="Path to the output Markdown file.",
    ))
```

The `convert` function is a Python script that converts a YAML file into a Markdown file.

**Arguments**:

- `yaml_file` (`Path`): The `yaml_file` parameter is the path to the YAML file that you want to convert to
Markdown. It is specified using the `--yaml-file` or `-y` option when running the script. The file
should exist and be readable
- `output_file` (`str`): The `output_file` parameter is the path to the output Markdown file. It
specifies the file where the converted Markdown content will be saved. By default, the value is set
to "output.md". However, you can provide a different file path if desired

<a id="yaml_to_md.all"></a>

#### all

```python
@app.command()
def all(yaml_file: Path = typer.Option(...,"-y", "--yaml-file", exists=True, file_okay=True, dir_okay=False, readable=True, resolve_path=True, help="Path to the YAML file."), schema_url: str = typer.Option(
        "https://raw.githubusercontent.com/mskcc-omics-workflows/yaml_to_md/main/nextflow_schema/meta-schema.json",
        "--schema-url",
        "-s",
        help="URL of the JSON schema.",
    ), output_file: str = typer.Option(
        "output.md",
        "--output-file",
        "-o",
        help="Path to the output Markdown file.",
    ))
```

The `all` function is a Python script that validates and converts a YAML file into a Markdown file based on a

specified JSON schema.

**Arguments**:

- `yaml_file` (`Path`): The `yaml_file` parameter is the path to the YAML file that you want to convert to
Markdown. It is specified using the `--yaml-file` or `-y` option when running the script. The file
should exist and be readable
- `schema_url` (`str`): The `schema_url` parameter is the URL of the JSON schema that will be used to
validate the YAML data. In this code, the default value for `schema_url` is set to "https://raw.githubusercontent.com/mskcc-omics-workflows/yaml_to_md/main/nextflow_schema/meta-schema.json" derived from
"https://raw.githubusercontent.com/nf-core/modules/master/modules/meta-schema.json". However, you
can provide one as well
- `output_file` (`str`): The `output_file` parameter is the path to the output Markdown file. It
specifies the file where the converted Markdown content will be saved. By default, the value is set
to "output.md". However, you can provide a different file path if desired

<a id="yaml_to_md.read_yaml"></a>

#### read\_yaml

```python
def read_yaml(yaml_file)
```

The function `read_yaml` reads the contents of a YAML file and returns it as a string.

**Arguments**:

- `yaml_file`: The `yaml_file` parameter is a file object that represents a YAML file

**Returns**:

the contents of the YAML file as a string.

<a id="yaml_to_md.convert_yaml_to_markdown"></a>

#### convert\_yaml\_to\_markdown

```python
def convert_yaml_to_markdown(data)
```

The `convert_yaml_to_markdown` function takes in a YAML data structure and converts it into a

Markdown format.

**Arguments**:

- `data`: The `data` parameter is a dictionary that contains information about a module. It has
the following structure:

**Returns**:

a Markdown-formatted string that contains information about a module. The string includes
the module's name, description, keywords, tools, inputs, outputs, authors, and maintainers.

