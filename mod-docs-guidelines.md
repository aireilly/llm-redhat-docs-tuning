# Modular documentation reference guide

# Introduction to modular documentation

This manual provides instructions on how to author modularly structured documentation based on user stories. The manual defines used terminology, describes components that form modular documentation, and instructs writers on how to use provided templates to turn user stories into modular documentation.

**IMPORTANT**
As modular documentation imperatives continue to evolve, the details and recommendations in this guide might be modified.

# Understanding modular documentation

This chapter explains what modular documentation is and what it is not.

# What modular documentation is

Modular documentation is documentation based on _modules_, which the writer combines into _assemblies_. An assembly can also include other assemblies. A module should not contain another module.

**IMPORTANT**
Nesting assemblies too deep can create too much complexity, which might make the documentation difficult to use and maintain. If you are worried this might be the case, consider linking to another assembly as an alternative to direct inclusion.

At Red Hat, we write modular documentation that is based on _user stories_. This means that each assembly documents a user story.


* For definitions of the terms we use, including modules, assemblies, and user stories, see [Modular documentation terms and definitions](#modular-documentation-terms-and-definitions).

# What modular documentation is not

* **Legacy (non-modular) documentation split into small, _meaningless_ pieces**
A module must make sense and provide value on its own, even when read separately from the other modules. The templates included in this manual help ensure this.
* **A collection of modules that have no relationship to one another**
An unorganized set of modules is confusing to users. That is why we combine modules into:
  * Assemblies that are based on user stories
  * Deliverables, like a book or help system, that present a structured view of the body of knowledge represented by a set of modules
* **Always a linear, book-type model**
Modular documentation is designed to enable you to deliver content flexibly. You can combine modules to build lean, article-based content or large, linear books.

# Modular documentation repositories

Due to many factors that determine repository design for individual products, these modular documentation guidelines do not provide a strict documentation repository template.

For a general repository structure used by documentation teams at Red Hat, see the example documentation repository and `README` file in the [`mod-doc-repo-example`](https://github.com/redhat-documentation/modular-docs/tree/mod-doc-repo-example) branch in this repository.

# Writing modular documentation

Assemblies can include various types of modules. Use the instructions in the following sections to create modules and combine them into assemblies.

## Creating modules

Follow these guidelines to create different types of modules:

* [Concept Module](#concept-modules)
* [Procedure Module](#creating-procedure-modules)
* [Reference Module](#reference-module-guidelines)

A module should not contain another module. However a module can contain a text snippet. For information about text snippets, see [Using Text Snippets](#using-text-snippets).

See [Module and assembly examples](#module-and-assembly-examples) for real-world examples of assemblies, modules, and their individual parts.

# Concept modules

This section explains what a concept module is and provides recommended practices for writing concept modules.

# Concept module definition

A concept module is an "understand" module. Concept modules give the user descriptions and explanations needed to understand and use a product.

# Concept module guidelines

The core requirement for a concept module is explaining the idea, or concept.
A concept module requires a short introduction and optionally, can also include additional resources.

When planning a concept module, look at nouns in related procedure modules and assemblies to find the concepts to explain to users.
Explain only things that are visible to users.
Even if a concept is interesting, it probably does not require an explanation if it is not visible to users.

## Concept introduction

The introduction to a concept module is a single, concise paragraph that provides a short overview of the module.
A short description makes the module more usable because users can quickly determine whether the concept is useful without having to read the entire module.

The introduction typically answers the following questions:

* What is the concept?
* Why should the user care about the concept?

For details and examples, see the [Short descriptions](https://redhat-documentation.github.io/supplementary-style-guide/#shortdesc) section in the Red Hat supplementary style guide.

## Concept body

The concept body describes the subject of the concept module.

Apart from paragraphs, you can use other AsciiDoc elements, such as lists, tables, or examples.
Consider including graphics or diagrams to speed up the understanding of the concept.

Avoid including instructions to perform an action. Action items belong in procedure modules. However, in some cases a concept or reference module can include suggested actions when those actions are simple, are highly dependent on the context of the module, and have no place in any procedure module. In such cases, ensure that the heading of the concept or reference remains a noun phrase and not a gerund. For example, see link:https://access.redhat.com/documentation/en-us/red_hat_process_automation_manager/7.9/html-single/developing_decision_services_in_red_hat_process_automation_manager/index#bound_variables_in_patterns_and_constraints[
"Bound variables in patterns and constraints"] and the sections that follow it. These concept and reference modules contain actions that are not suitable for standalone procedure modules but are relevant actions to understand in the context of the concept or reference being described.

See also [The DITA Topic Types](https://informationmapping.com/blogs/news/the-dita-topic-types-square-pegs-and-round-holes?_pos=1&_sid=45011393d&_ss=r) at _informationmapping.com_ for more information about different types of conceptual information: principle, concept, structure, process, and fact.

If the concept module is large and complex, consider splitting the concept module into multiple standalone concept modules. If you cannot split the module into meaningful standalone modules, consider using subheadings in the module to structure the content for improved reader navigation. If you use subheadings in a concept module, you can add the `[discrete]` tag to exclude each subheading from the table of contents, if needed. However, in many cases, subheadings are helpful to include in the table of contents to improve content searchability.

**NOTE**
You can use subheadings in concept or reference modules, but not in procedure modules.

## Concept additional resources

The optional additional resources list links to other material closely related to the contents of the concept module, for example, other documentation resources.

Focus on relevant resources that might interest the user. Do not list resources for completeness.

## Additional resources

* Download the [concept module template (adoc file)](https://raw.githubusercontent.com/redhat-documentation/modular-docs/master/modular-docs-manual/files/TEMPLATE_CONCEPT_concept-explanation.adoc) for new projects.
* For real-world examples of concept modules, see [Concept module examples](#concept-module-examples).

# Procedure modules

Procedure modules explain how to do something. A procedure module contains numbered, step-by-step instructions to help users accomplish a single task. Sometimes those tasks include substeps. Procedure modules must include a title, a brief introduction, and one or more steps in the form of imperative statements. Procedure modules can also contain the following sections:

* [limitations](#limitations)
* [Prerequisites](#prerequisites)
* [Verification](#verification)
* [Troubleshooting](#troubleshooting)
* [Next steps](#next-steps)
* [Additional resources](#additional-resources)

Do not change or embellish these subheadings. Unless absolutely necessary, do not create additional subheadings.

**Schema of a procedure module**

**Procedure title**

The title of a procedure module is a gerund phrase, such as **Deploying OpenShift Container Platform**.

**Procedure introduction**

The procedure introduction is a short paragraph that provides an overview of the module. The introduction includes what the module will help the user do and why it will be beneficial to the user. It includes key words that relate to the module to maximize search engine optimization.

The introduction typically provides context for the procedure, such as:

* Why and where the user performs the procedure
* Special considerations specific to the procedure

For details and examples, see the [Short descriptions](https://redhat-documentation.github.io/supplementary-style-guide/#shortdesc) section in the Red Hat supplementary style guide.

**Prerequisites**

This section is optional. Prerequisites are a bulleted list of conditions that must be satisfied before the user starts the procedure. Use a bulleted list for prerequisites and the plural heading **Prerequisites**, even if your procedure only has a single prerequisite.

Prerequisites can be full sentences or sentence fragments; however, prerequisite list items must be parallel.

Focus on relevant prerequisites that users might not otherwise be aware of. Do not list obvious prerequisites. If a prerequisite applies to all of the procedures in a user story, consider listing the prerequisite in the assembly file. If you do this, consider including the prerequisite in the procedure module as a comment.

**Procedure**

This section is required. The procedure consists of one or more steps required to complete the procedure. Each step describes one action written in the imperative form, for example, 'Do this action'. For single-step procedures, use an unnumbered bullet instead of a numbered list.

**NOTE**
Not all numbered lists in documentation are procedures. You can also use numbered lists in any module type for non-procedural sequences, such as a process flow of system actions.

**Verification**

This section is optional. It provides the user with one or more steps to verify that the procedure provided the intended outcome, for example:

* An example of expected command output or a pop-up window that the user receives when the procedure is successful
* Actions for the user to complete, such as entering a command, to determine the success or failure of the procedure

**Troubleshooting**

This section is optional and not used often. List any actions that can help with troubleshooting the procedure. This subsection should be short. Consider whether the information might be better in a separate troubleshooting procedure or as part of a reference module that contains other troubleshooting sections.

**Next steps**

This section is optional. Provide links to resources that contain instructions that might be useful to the user after they complete this procedure.

**NOTE**
Do not use **Next steps** to provide a second list of instructions.

**Additional resources**

This section is optional. The listed resources link to other material closely related to the contents of the module, such as other documentation resources, instructional videos, or labs.

Focus on relevant resources that might interest the user. Do not list resources for completeness. If a resource applies to all of the modules in a user story, consider listing the resource in the Additional resources section of the assembly file. If you do this, consider including the resource in the procedure module as a comment.

# Reference modules

This section explains what a reference module is and provides recommended practices for writing reference modules.

# Reference module definition

Reference modules provide data that users might want to look up, but do not need to remember.

**Common documentation examples of reference modules**

* A list of commands that users can use with an application
* A table of configuration files with definitions and usage examples
* A list of default settings for a product

**Reference modules explained using a real-life example**

For documentation on how to cross the road, you could create these modules:

* Concept modules:
  * What are roads
  * What are crossings
* Procedure modules:
  * How to put one foot in front of another
  * How to use pedestrian traffic lights
  * How to see if the road is clear for crossing
* Reference modules:
  * Crossing signals
  * Common crosswalk pavement markings
  * Crossing laws by country

# Reference module guidelines

The required part of a reference module is the reference data.
A reference module requires a short introduction.

## Reference introduction

The introduction to a reference module is a single, concise paragraph that provides a short overview of the module. A short description makes the module more usable because users can quickly determine whether the reference is useful without having to read the entire module.

For details and examples, see the [Short descriptions](https://redhat-documentation.github.io/supplementary-style-guide/#shortdesc) section in the Red Hat supplementary style guide.

## Reference body

A reference module has a very strict structure, often in the form of a list or a table. A well-organized reference module enables users to scan it quickly to find the details they want.

To make the reference data easier to scan, organize it in a logical order (such as alphabetically) or as a table. AsciiDoc markup to consider for reference data:

* [Lists](http://asciidoctor.org/docs/asciidoc-syntax-quick-reference/#lists) (unordered, labeled)
* [Tables](http://asciidoctor.org/docs/asciidoc-syntax-quick-reference/#tables)

If you have a large volume of the same type of information to document, use a structure into which the information details can fit, and then document each logical unit of information as one reference module. For example, think of man pages, which document very different information details, but which still use consistent titles and formats to present those details in a uniform information structure.

If the reference module is large and complex, consider splitting the reference module into multiple standalone reference modules. If you cannot split the module into meaningful standalone modules, consider using subheadings in the module to structure the content for improved reader navigation. If you use subheadings in a reference module, you can add the `[discrete]` tag to exclude each subheading from the table of contents, if needed. However, in many cases, subheadings are helpful to include in the table of contents to improve content searchability.

**NOTE**
You can use subheadings in concept or reference modules, but not in procedure modules.

## Additional resources

* Download the [reference module template (adoc file)](https://raw.githubusercontent.com/redhat-documentation/modular-docs/master/modular-docs-manual/files/TEMPLATE_REFERENCE_reference-material.adoc) for new projects.
* For real-world examples of reference modules, see [Reference module examples](#reference-module-examples).
* For advice on when to use lists and when to use tables, see [Let’s bring &lt;table> to the table, again.](https://medium.com/@heyoka/lets-bring-table-to-the-table-again-f1ae751159d5)

# File names and anchors

Create snake-case lower case file names. 

**NOTE**
Do not include special characters in file names. Ensure that all members of your team use the same file naming conventions.

# Forming assemblies

This section explains what an assembly is and provides recommended practices for forming assemblies.

# Assembly definition

An assembly is a collection of modules that describes how to accomplish a user story. See also [Understanding modular documentation](#understanding-modular-documentation).

# Assembly guidelines

The required parts of an assembly are the introduction and modules. Optionally, an assembly can also include prerequisites and additional resources.

## Assembly title

If the assembly describes a task and includes one or more procedure modules, start the title with a verb in the gerund form, such as Creating or Configuring, for example _Encrypting block devices using LUKS_. If the assembly does not include any procedure modules, use a noun phrase, for example _Red Hat Process Automation Manager API reference_.

## Assembly introduction

The introduction explains what the user accomplishes by working through the assembled modules. It typically provides context for the assembly.

Consider rewording the user story to write the assembly introduction, for example:

* User story: As an administrator, I want to provide external identity, authentication and authorization services for my Atomic Host, so that users from external identity sources can access the Atomic Host.
* Assembly introduction: As a system administrator, you can use SSSD in a container to provide external identity, authentication, and authorization services for the Atomic Host system. This enables users from external identity sources to authenticate to the Atomic Host.

For details and examples, see the [Short descriptions](https://redhat-documentation.github.io/supplementary-style-guide/#shortdesc) section in the Red Hat supplementary style guide.

## Assembly prerequisites

Prerequisites are conditions that must be satisfied before the user can start following the assembly and are applicable to all the modules in the assembly.

Use the second level heading syntax for the Prerequisites section in the assembly so that it is displayed in the table of contents and is consistent with the Additional resources or Next steps sections in the assembly.

## Assembly modules

All module and assembly titles must use the H1 heading designation, such as `= My heading`.

## Next steps and Additional resources
These sections are optional. If you use both **Next steps** and **Additional resources**, list **Next steps** first. The listed resources link to other material closely related to the contents of the module, such as other documentation resources, instructional videos, or labs.

Focus on relevant resources that might interest the user. Do not list resources for completeness. If a resource applies to all of the modules in a user story, consider listing the resource in the Additional resources section of the assembly file. If you do this, consider including the resource in the procedure module as a comment.

**NOTE**
If you use **Next steps** or **Additional resources** in an assembly file, check whether the last module in the assembly also has **Next steps** or **Additional resources**. If so, view the rendered HTML and consider rewriting or reorganizing the assembly.
