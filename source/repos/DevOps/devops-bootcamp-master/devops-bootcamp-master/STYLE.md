# Liatrio's DevOps Bootcamp

## Style Guide

### Front-Matter

The bootcamp uses front-matter on each exercise section to generate stats on the bootcamp. Please adhere to this template for the section metadata.

```yaml
---
<relative-path>:
  category: <Fundamentals|Virtualization|Containerization|Container Orchestration|Cloud Computing|Agile Development|CI/CD|Infrastructure as Code|Version Control| Code Quality & Testing>
  estReadingMinutes: 10
  exercises:
    -
      name: Hello EC2
      description: Create EC2 VMs and configure one as a Jenkins server and the other as a Jenkins agent registered to the server.
      estMinutes: 240
      technologies:
      - AWS
      - EC2
      - Jenkins
---
```
Please be consistent with the names of technologies and categories selected. These are used by the front-end in the generation of visualizations like word clouds and graphs.

Modifying or adding front-matter will automatically get added to the 'master record' which is located in the front matter of [`./docs/README.md`](./docs/README.md). Please do not edit this section unless you know what you are doing as it is auto-generated by a [pre-commit hook](./.husky/front-matter-condenser.js)

### HTML

Docsify and some Markdown viewers supports mixing HTML and Markdown elements in the same document. There must be a blank line between the two formats.

```html
<center>

  ![](../../img/goals.png)

</center>
```

Note the blank line between the `<center>` HTML tag and the `![](../img/goals.png)` Markdown tag.

### Multi Column Layout

Multi column layouts can be created using HTML div tags with following CSS classes:

- `grid2`, `grid3`, `grid4`: Define a section with 2, 3 or 4 columns
- `col`: Define a column inside of a grid section

Here is an example of a 3 column layout

```html
<div class="grid3"><div class="col">
<center>

**Column 1**

</center>

1. one
2. two
3. three

</div><div class="col">
<center>

**Column 2**

</center>

* one
* two
* three

</div><div class="col">
<center>

**Column 3**

</center>

>blaa blaa blaa

</div></div>
```