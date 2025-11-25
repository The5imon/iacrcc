
# IACR Communication in Cryptology

This is a [Quarto](https://quarto.org/) template implementing the [IACR Communication in Cryptology document class](https://publish.iacr.org/iacrcc) 

## Creating a New Paper

To create a new paper using this format:

```bash
quarto use template The5imon/iacrcc
```

This will create a new directory with an example document that uses this format.

## Using with an Existing Document

To add this format to an existing document:

```bash
quarto add The5imon/iacrcc
```

Then, add the format to your document options:

```yaml
format:
  iacrcc-pdf: default
```

The ``iacrcc`` paper template currently only supports the `-pdf` format.

## Options

To include additional \LaTeX packages inside this document append them in the YAML header:

```yaml
iacrcc-header-includes:
  - text: |
      \usepackage{eplain}
      \usepackage{easy-todo}
  - file: packages.tex
  - macros.tex 
```

This is a special definition of the header because the default `header-includes` and `include-in-header` directives are not compatible with the `iacrcc` document class, due to [issues](https://github.com/orgs/quarto-dev/discussions/13345) with the AMS theorem environment creation and settings.

## Example

Here is the source code for a minimal sample document: [template.qmd](template.qmd) that also goes over the structure of the template and corresponding Quarto features in more detail. The rendered paper can be found in [template.pdf](template.pdf).

## Resources

Here you can find more resources regarding creating Quarto journal templates:

- https://quarto.org/docs/extensions/creating.html

This template is also based on the standard ones provided by the `quarto-journals` Github repository:

- https://github.com/quarto-journals/
- https://github.com/quarto-journals/article-format-template