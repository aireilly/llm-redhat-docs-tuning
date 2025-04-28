# Red Hat style guide for product documentation

## About this guide

The style and language guidance in this guide overrides or supplements some guidance provided by the [_IBM Style_](https://www.ibm.com/docs/en/ibm-style) guide, which is the primary source of style guidance for [Red Hat](https://www.redhat.com/) product and cross-product solution documentation.

The Red Hat Customer Content Services team has created this guide to help ensure that Red Hat product documentation is clear, consistent, and cohesive. Upstream communities who want to align more closely with the standards used by Red Hat product documentation can also use this guide. However, some links in this guide might not be accessible for non-Red Hat associates.

**NOTE**
Other Red Hat technical documentation, including Red Hat training and exam content by Global Learning Services (GLS), follows the [_Red Hat Technical Writing Style Guide_](https://stylepedia.net/) instead of the _Red Hat supplementary style guide for product documentation_.

## Using style guides for Red Hat product documentation

Red Hat product documentation adheres to the style guidance provided in the _IBM Style_ guide, the _Red Hat supplementary style guide for product documentation_, and documentation style guidelines specific to Red Hat products, such as Red Hat Enterprise Linux or Red Hat OpenShift Container Platform.

# Grammar and language

## Conscious language

The Conscious Language Group supports the Red Hat commitment to remove problematic language from our code, documentation, websites, and open source projects with which Red Hat is involved.
For more information about the Conscious Language Group, see https://github.com/conscious-lang/conscious-lang-docs.

**IMPORTANT**
To ensure consistency and success, it is imperative for product team stakeholders to align internally. For example, documentation teams should engage in discussions with their engineering leadership to reach an agreement on replacement terms. This ensures that the product documentation matches the code.

### Blacklist and whitelist

When possible, rewrite documentation to avoid these terms.
When it is not possible to remove the terms _blacklist_ and _whitelist_, replace them with one of the following alternatives:

* Blocklist / allowlist: This combination is recommended by the _IBM Style_ guide. Use this combination unless your product area has another specific replacement that is agreed between engineering leadership and your documentation team.
* Denylist / allowlist
* Blocklist / passlist
* You can also use a term that has been agreed by your product team stakeholders.

### Master and slave

When possible, rewrite documentation to avoid these terms. When it is not possible to rewrite, you can use the following alternatives for _master_ / _slave_:

* Primary / secondary
* Source / replica
* Initiator, requester / responder
* Controller, host / device, worker, proxy
* Director / performer
* Controller / port interface (in networking)
* You can also use a term that has been agreed by your product team stakeholders.

## Contractions

Avoid contractions in product documentation to leave no ambiguity and to make it easier for translation and international audiences.

If you are writing quick start or other content that uses a more informal [conversational style](#conversational-style) (_fairly conversational_ or _more conversational_), you may use contractions. In this case, follow the guidance in the _IBM Style_ guide on using contractions.

## Conversational style

Follow the _IBM Style_ guide advice of _less conversational_ style in most cases.

Red Hat Enterprise Linux 8 delivers a stable, secure, and consistent foundation across hybrid cloud deployments with the tools needed to deliver workloads faster with less effort.

As needed, adjust the conversational to _fairly conversational_ for an audience of new users or _least conversational_ for API documentation and other very experienced audiences.

**NOTE**
Documentation for cloud services follows the _IBM Style_ guide for _fairly conversational_ tone. When using _fairly conversational_ tone, use contractions where appropriate.

## Homographs
A homograph is a word that is spelled the same as another word but has a different meaning.
Using homographs close together in a sentence or paragraph might confuse readers.
Therefore, be aware of this potential issue, and, when possible, avoid writing sentences that use homographs close to one another provided that you can do so without changing the technical meaning.

The following list includes homographs that might commonly appear in technical documentation:

* Application
* Attribute
* Block
* Coordinates
* Number
* Object
* Project

## Minimalism
Minimalism is a methodology for creating targeted documentation focused on your readers' needs. If you understand your customers' needs, you can write shorter and simpler documentation specific to what customers want to do.

Minimalism has five principles:

### Principle 1: Customer focus and action orientation
Know what your users do, what their goals are, and why they perform these actions. Minimize how much content customers must wade through to get to something they recognize as real work. Separate conceptual and background information from procedural tasks.

### Principle 2: Findability
Findability covers two areas:

* Ensure your content is findable through Google search and access.redhat.com site searches.
* Ensure your content is scannable. Use short paragraphs and sentences and bulleted lists where appropriate.

### Principle 3: Titles and headings
Use clear titles with familiar keywords for customers. Keep titles and headings between 3 to 11 words. Headings that are too short lack clarity and don’t help customers know what’s in a section. Headings that are too long are less visible in Google searches and harder for customers to understand.

### Principle 4: Elimination of fluff
Avoid long introductions and unnecessary context. Shorten unnecessarily long sentences.

### Principle 5: Error recovery, verification, and troubleshooting
Recognize that people make mistakes and need to verify that they have completed a task. Be sure to include troubleshooting, error recovery, and verification steps.

## Users
In most cases, the word "user" refers to a person or a person’s user account, and therefore would be considered animate. In these cases, use animate personal pronouns such as "who".

In certain technical cases, these users are not persons but instead system accounts or more abstract concepts (inanimate). For example, Linux `root` and `guest` users do not relate to any person. Applications and services might run as specific Linux users with no person controlling them. SELinux users such as `user_u` or `sysadm_u` are identifiers of one or multiple Linux users for access control purposes. In these specific cases, refer to these inanimate users with inanimate personal pronouns such as "that".

In these specific cases, and only if you cannot write around it, you can refer to these inanimate users with inanimate personal pronouns such as "that".

# Formatting

## Commands in code blocks

Use a single command per code block for each procedure step. This approach helps with readability and makes it possible for the copy button in code blocks to work correctly.

## Date formats

Follow the _IBM Style_ guide advice of _day Month year_ for date formats, for example, 3 October 2019.

When the format _day Month year_ causes a presentation or clarity issue, use _Month day, year_ (for example, October 3, 2019) instead.

## Man page references

When referencing a man page in an "Additional resources" section, use the following format:

* `_<man_page_name>_(_<section_number>_)` man page on your system

Do not link to a website that contains the man page information. The contents of a man page might vary between systems or package versions, so users must run the `man` command on the target system to view the system-specific information for the named command or utility.

* `sudoers(5)` man page on your system

* `nmcli(1)`, `nm-settings(5)`, and `sudoers(5)` man pages on your system

## Product names and version references

Use attributes instead of hard-coded references when you refer to the name of your product in full, to its abbreviated form, or to its major or minor version.
Only use hard-coded version references if the version that you are referring to in a particular case never changes.

## Single-step procedures

When a procedure contains only one step, use an unnumbered bullet.

For example:
* Install the `dnf-automatic` package.

## Titles and headings

Write all titles and headings, including the titles of product documentation guides and Knowledgebase articles, in sentence-style capitalization. Do not use headline-style capitalization.

**Examples**

* _Composing a customized RHEL system image_
* _Configuring the node port service range_
* _How to perform an unsupported conversion from a RHEL-derived Linux distribution to RHEL_

## User-replaced values

A _user-replaced value_, also known as a replaceable or variable value, is a placeholder that the user replaces with a value that is relevant for their situation. User-replaced values are often found in places such as code blocks, file paths, and commands.

Use descriptive names for user-replaced values and follow this general format: _&lt;value_name>_.

**NOTE**
For XML code blocks, see the guidance on [user-replaced values for XML](#user-replaced-values-for-xml).

Ensure that user-replaced values have the following characteristics:

* Surrounded by angle brackets (`< >`)
* Separated by underscores (`_`) for multi-word values
* Lowercase, unless the rest of the related text is uppercase or another capitalization scheme
* Italicized
* If the user-replaced value is referencing a value in code or in a command that is normally monospace, also use monospace for the user-replaced value
* If you want to use a user-replaced value in example output, format the replaceable value with italics and in angle brackets. Alternatively, if you choose to use an example value instead, do not italicize the example value and do not place it in angle brackets.

# Structure

## Admonitions

Admonitions should draw the reader’s attention to certain information. Keep admonitions to a minimum, and avoid placing multiple admonitions close to one another. If multiple admonitions are necessary, restructure the information by moving the less-important statements into the flow of the main content.

Admonitions should be short and concise. Do not include procedures in an admonition.

## Lead-in sentences

A lead-in sentence in this context is the text that directly follows a `Prerequisites` or `Procedure` heading in a task-based module. It is distinct from the module abstract, which describes the goals of the user for the module.

Do not use a lead-in sentence in the `Prerequisites` or `Procedure` sections of a module unless it is necessary to aid navigation or add clarity.

The following examples demonstrate when a lead-in sentence might add value.

* Your module has a long list of prerequisites, and you want to group the prerequisites in sections to make it easier for users to understand what tasks must be performed to complete a procedure.
* Your module has a complex procedure or set of prerequisites, and you want to emphasize that all steps or prerequisites must be completed.

Use a complete sentence for the lead-in sentence to reduce ambiguity and support translation.

## Prerequisites

When writing prerequisites, be as clear and concise as possible. You can use the passive voice, _if necessary_, to achieve that end.

Write prerequisites as checks that are true or that the user must have completed before they begin a procedure. They can be actions that the user, another person, or piece of technology has completed. Prerequisites can also include items that the user must have ready before beginning the procedure.

* The passive voice might be appropriate for a prerequisite that is not completed by the current user. For example, having a configuration enabled by a system admin.
* Avoid using imperative formations.
* Use parallel language when you write prerequisites. For example, if one bullet is a complete sentence, write the other bullets as complete sentences. But one bullet can be passive voice and another active voice.

* JDK 11 or later is installed.

  Passive voice: the agent is unknown or unimportant.
* A running Kafka instance in {product}.

  Not a complete sentence: This prerequisite is acceptable if all the other prerequisites in your list are also not complete sentences.
* You are logged in to the Administration Portal.
* You have validated Thing 1.

## Short descriptions

To help readers find the information that they need or to confirm that they are in the right place, every module and assembly must include a _short description_, also called an _abstract_.

**IMPORTANT**
Do not start a module with an admonition, even when adding the Technology Preview admonition. Always include a short description before including an admonition.

This description is usually at least 2-3 sentences long, and you can scan it in a few seconds. It exists between the title and the main content, connecting them and providing context and disambiguation.

Follow these guidelines when writing short descriptions:

* Include user intent:
  * **What** users must do. This content is similar to what is in the title but should not just repeat the same information.
  * **Why** users must complete an action. You must build from the information in the title. This content helps users understand why completing an action is important or beneficial to them.
* Make modules findable and reusable. Ensure that the product name is either in the title or the short description of a module or assembly.
* If you are documenting two or more ways of completing the same procedure, explain why users would want to choose one or the other. If possible, link to the other ways.
* For complex procedures, include some of the key tasks that a customer must complete.
* Write in plain English and use simple sentences. You can test the reading level of your sentences by using a readability scoring tool.
* Use active voice and present tense.
* Avoid self-referential language, such as "This topic covers..." or "Use this procedure to...".
* Avoid feature-focused language. Focus on what users can accomplish with a product, not on what a product does. For example, avoid phrases such as "This product allows you to...".
* Use customer-centric language, such as "You can... by..." or "To..., configure...".

# Technical examples

## Commands requiring root privileges

Some commands require root privileges to run. Users without root privileges must first do one of the following to run such a command:

* Preface the command with `sudo` to temporarily change their current privileges.
* Run `su -` to switch to the root user account.

Use the following guidelines when you document commands that require root privileges:

* If a command requires a temporary switch to root privileges, use the `sudo` command at the beginning of the sample command syntax rather than the `su -` command.
* If you include a shell prompt in a sample command, always show the correct prompt for a regular user (`$`) or a user with root privileges (`#`).

  **NOTE**

  Do not rely solely on a shell prompt in a sample command to indicate the required privilege level to run a command.
  If you include a shell prompt to indicate that a user with root privileges must run the command, also include a statement about this requirement in the step text, the introductory text, or the prerequisites.


* When a sample command includes `sudo`, use the `$` prompt, not `#`, as shown in the following example:

  ```terminal
  $ sudo systemctl start firewalld
  ```

* If multiple commands in a procedure require root privileges, add introductory content to tell the user about the requirement.
The following example shows one way that you could integrate a requirement for root access into the introduction for a procedure:

## Ellipses in YAML code blocks

Use the number sign (`#`) to comment out an ellipsis in YAML code blocks.
YAML reserves `...` to indicate the end of a document without starting a new document.

```yaml
apiVersion: operator.openshift.io/v1alpha1
kind: CertManager
metadata:
  name: cluster
# ...
```

## IP addresses and MAC addresses

Use the IP and MAC address ranges that are reserved for documentation purposes to avoid the likelihood of conflicts and confusion.

### Reserved IP addresses

Reserved IPv4 addresses for documentation are defined in [RFC 5737](https://www.rfc-editor.org/rfc/rfc5737.html):

Reserved IPv6 addresses for documentation are defined in [RFC 3849](https://www.rfc-editor.org/rfc/rfc3849.html):

See the _IBM Style_ guide for additional guidance on using IP addresses in documentation.

### Reserved MAC addresses

Reserved MAC addresses for documentation are defined in [RFC 7042](https://www.rfc-editor.org/rfc/rfc7042.html#section-2.1.2):

* For unicast: 00:00:5E:00:53:00 - 00:00:5E:00:53:FF
* For multicast: 01:00:5E:90:10:00 - 01:00:5E:90:10:FF

## Long code examples

All code blocks (regardless of length) must be necessary, accurate, and helpful. Code blocks must be as copy-and-paste friendly as possible, with the exception of variables and callouts. The length of the block is irrelevant, within reason, if the code block follows these guidelines.

## Syntax highlighting

Provide the source language if it is supported by the Red Hat Customer Portal toolchain.

# Graphical interfaces

For more detailed guidance on how to document user interface (UI) elements, see [PatternFly](https://www.patternfly.org/ux-writing/about).

## Microcopy

The words in a user interface, commonly referred to as "UX copy" or "microcopy", are just as important as the components or layouts. Microcopy is another element of design, and it can drive better UX decisions and guide users to succeed. Red Hat cloud services are based on PatternFly, an open source design system created to enable consistency and usability across a wide range of applications and use cases.

See [UX writing](https://www.patternfly.org/ux-writing/about) in the PatternFly content style guide for comprehensive guidelines about documenting user interfaces.

## Screenshots

Avoid screenshots for both accessibility and localization reasons. If you must use screenshots, use them as judiciously as possible and ensure alt text is unique and descriptive. For more information about proper use of images in user interface documentation, see [Accessibility](#accessibility).

## Text entry

To indicate that a user should input text, use "enter" as opposed to "type" or "input". The text to enter should be in monospace.

## User interface elements

Use bold text for all graphical user interface (GUI) element names, including menus, menu items, buttons, dialog boxes, and windows. Use bold text for the element name if the name appears in the GUI, even if the element is not clickable.

If an element is not labeled in the GUI, refer to the element by a generic description and do not use bold text. For example, if a search field is not labeled in the GUI, write it as "the search field", not "the **Search** field".

# Legal

## Cost references

Avoid all references to the costs and charges of Red Hat products. Although the _IBM Style_ guide recommends against using the term "free", also avoid any references to cost in product documentation because they can confuse users and cause legal concerns. Any cost information is best referenced in marketing materials.

* "at no initial cost" - Avoid this phrase in documentation because, although it implies there are further costs, it can also be construed to mean that the product is free when it is not.

## Future releases or plans

When possible, avoid making statements that predict future releases or plans.

However, some circumstances, such as release notes or deprecation notices, might dictate that you refer to a future release, plan, or event.
In these situations, follow these guidelines:

* When discussing future plans, use words such as "anticipate", "expect", or "plan".
* Do not promise that a feature or a fix for a known issue will be included in an upcoming release or according to a specific timeline.
* Do not refer to a specific future release. For example, do not mention a particular release number or a specific release date.

  **NOTE**

  One exception to this rule applies to deprecation and removal notices, which might have to specify a future release in which a feature or functions will be deprecated and removed.

  See [Deprecated and removed features](#deprecated-and-removed-features) for guidelines about deprecation and removal notices.

# Links

## Cross-references

Follow these guidelines when adding cross-references within your documentation:

* Include cross-references only when necessary.
* If the information is critical, consider including it instead of cross-referencing.

## External links

Follow these guidelines when linking externally:

* Avoid unnecessary links to external sites not owned and operated by Red Hat or IBM.
Links to external sites can change or be unreliable.
In addition, customers might infer that Red Hat endorses or supports the linked content, even if that is not the intent.

  **NOTE**
  Links to upstream sites, such as GitHub, are considered to be external links.

* When possible, link to a top-level page and avoid deep links to a specific page or image.
Deep links can break more frequently and can inadvertently bypass a site’s legal notices.
* Do not use bare URLs for links.
Bare URLs are unhelpful because they do not provide adequate context about the link target.
* Do not use URL shorteners to replace full URLs.
* Always include meaningful link text.
Meaningful link text describes to users what content they will see if they click the link.
* Use hyperlinks unless the URL is an example URL or is otherwise inaccessible to users.
* By default, links are followable and crawlable. Do not use the `nofollow` link option unless absolutely necessary.

For information about links and web addresses, including using URLs in examples, see the _IBM Style_ guide.

## Link text

Follow these guidelines when specifying link text:

* Contextually describe what the user will find at the target location so that they can decide if they want to leave their current location.
* Use a concise sentence or sentence fragment as the link text.
* Avoid irrelevant link text.

## Links to Red Hat Knowledgebase articles

* Use the title of the Knowledgebase article for the link text, or use descriptive running text.
* When not using running text, call out that this is a Knowledgebase article.
* When the link appears in **Additional resources**, put the article title first, followed by `(Red Hat Knowledgebase)`.

For a non-cloud environment, you can resize the disk and file system. For more information, see the Red Hat Knowledgebase solution [Does RHEL 7 support online resize of disk partitions?](https://access.redhat.com/solutions/199573).

If your Apache web server configuration enables SSL security, verify that you enable only the TLSv1 protocol and disable SSLv2 and SSLv3. This is because of the [POODLE SSL vulnerability (CVE-2014-3566)](https://access.redhat.com/solutions/1232413).

* [Does RHEL 7 support online resize of disk partitions?](https://access.redhat.com/solutions/199573) (Red Hat Knowledgebase)

# Accessibility

For full information about writing accessible content at Red Hat, see [_Getting started with accessibility for writers_](https://redhat-documentation.github.io/accessibility-guide/).

## Colors and other visual information

Color should not be used as the only visual means of conveying information, indicating an action, prompting a response, or distinguishing a visual element. The documentation interface must provide at least one visual mode of operation that does not require user perception of color.
Avoid indicating direction, such as left, right, above and below, since these have no meaning to a screen reader. Instructions provided for understanding and operating the product must not rely solely on sensory characteristics such as shape, size, visual location, or orientation.

* Avoid instructions that rely solely on sensory characteristics.
* Information that is conveyed by color differences must also be provided in text form.
* For images or diagrams in your document, ensure sufficient contrast between foreground and background text or graphical elements. Graphics and diagrams in your document produced by a CCS graphic designer must meet contrast ratio requirements. If you created a graphic or diagram yourself, use the WCAG reference for [Contrast](https://www.w3.org/TR/WCAG21/#contrast-minimum), and the [Contrast Checker](https://webaim.org/resources/contrastchecker/) to evaluate contrast compliance.
* Avoid directional indicators such as left, right, above and below when providing navigational instruction in the user interface.

## Images

Use text equivalents for every diagram, image, or other non-text element. Avoid using images of text instead of actual text.

Evaluation:

* All icons, images, diagrams, and non-text elements that convey information must have meaningful alternative-text descriptions.
  * For icons, use alternative text that describes what the icon does rather than what it looks like. For example, the alt text for a `+` icon is "Add" rather than "Plus Sign".
* The document is free from images of text; for example, a screen capture image of an informational table. Make sure that actual text is used to convey information, rather than images of text.

## Links and hypertext

The purpose of each link can be determined from the link text alone, or from the link text together with the link context. Links must lead to the correct target locations within the document, or to a valid external web page location. Ensure that all links work as expected.

* All link URLs and cross-reference links must provide descriptive text that conveys information about the content of the target linked page prior to clicking the link. Do not use a generic phrase like “click here”.

Examples:

* A link to a different section in the same document shows the section title.
* An external link provides the site name or title of the target web page.
* URLs must link to correct and valid web destinations.

## Tables

When working with tables, accessibility tools such as a screen reader can programmatically determine the location of the content in each row and column. Screen readers interact with a data table based on the number of columns and rows, and provide table navigation to the user by reading row and column headers in the order they occur.

* All tables must have a simple, logical reading order from left to right, top to bottom.
* Avoid tables with irregular headers. Tables with multi-level headers, or spanned rows and cells, do not provide a clear horizontal or vertical association between header and data cells, and are too complex for accessibility tools to interpret.
  * See the example in [Tables with irregular headers](https://www.w3.org/WAI/tutorials/tables/irregular/).
* Avoid blank header cells. Older screen readers often do not handle blank header cells correctly. Simplify tables to remove empty header cells, or add row and column text to each header cell.

## Well-formed HTML and meaningful sequence

The meaning of content relies on the order in which you present it. For example, English content is arranged from left to right and readers usually look at a left-hand column before a right-hand column. Users who rely on assistive technology (such as a screen reader) to interpret content need the content to be presented in a meaningful order. If content is presented out of sequence, readers might become disoriented and unable to understand the content.

* Correctly nest headings from H1 to H2, H3 and so forth to indicate relative importance. Do not skip heading levels.
* Use correct AsciiDoc tags to produce the intended HTML.

* Understanding WCAG 2.0
  * [Text Alternatives](https://www.w3.org/TR/UNDERSTANDING-WCAG20/text-equiv.html)
  * [Images of Text](https://www.w3.org/TR/UNDERSTANDING-WCAG20/visual-audio-contrast-text-presentation.html)
  * [Link Purpose (In Context)](https://www.w3.org/TR/UNDERSTANDING-WCAG20/navigation-mechanisms-refs.html)
  * [Sensory Characteristics](https://www.w3.org/TR/UNDERSTANDING-WCAG20/content-structure-separation-understanding.html)
  * [Use of Color](https://www.w3.org/TR/UNDERSTANDING-WCAG20/visual-audio-contrast-without-color.html)
  * [Meaningful Sequence](https://www.w3.org/TR/UNDERSTANDING-WCAG20/content-structure-separation-sequence.html)
* [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/)

## Modular documentation reference guidelines

This section provides instructions on how to author modularly structured documentation based on user stories. The manual defines used terminology, describes components that form modular documentation, and instructs writers on how to use provided templates to turn user stories into modular documentation.

**IMPORTANT**
As modular documentation imperatives continue to evolve, the details and recommendations in this guide might be modified.

### Understanding modular documentation

This chapter explains what modular documentation is and what it is not.

### What modular documentation is

Modular documentation is documentation based on _modules_, which the writer combines into _assemblies_. An assembly can also include other assemblies. A module should not contain another module.

**IMPORTANT**
Nesting assemblies too deep can create too much complexity, which might make the documentation difficult to use and maintain. If you are worried this might be the case, consider linking to another assembly as an alternative to direct inclusion.

At Red Hat, we write modular documentation that is based on _user stories_. This means that each assembly documents a user story.


* For definitions of the terms we use, including modules, assemblies, and user stories, see [Modular documentation terms and definitions](#modular-documentation-terms-and-definitions).

### What modular documentation is not

* **Legacy (non-modular) documentation split into small, _meaningless_ pieces**
A module must make sense and provide value on its own, even when read separately from the other modules. The templates included in this manual help ensure this.
* **A collection of modules that have no relationship to one another**
An unorganized set of modules is confusing to users. That is why we combine modules into:
  * Assemblies that are based on user stories
  * Deliverables, like a book or help system, that present a structured view of the body of knowledge represented by a set of modules
* **Always a linear, book-type model**
Modular documentation is designed to enable you to deliver content flexibly. You can combine modules to build lean, article-based content or large, linear books.

### Modular documentation repositories

Due to many factors that determine repository design for individual products, these modular documentation guidelines do not provide a strict documentation repository template.

For a general repository structure used by documentation teams at Red Hat, see the example documentation repository and `README` file in the [`mod-doc-repo-example`](https://github.com/redhat-documentation/modular-docs/tree/mod-doc-repo-example) branch in this repository.

### Writing modular documentation

Assemblies can include various types of modules. Use the instructions in the following sections to create modules and combine them into assemblies.

#### Creating modules

Follow these guidelines to create different types of modules:

* [Concept Module](#concept-modules)
* [Procedure Module](#creating-procedure-modules)
* [Reference Module](#reference-module-guidelines)

A module should not contain another module. However a module can contain a text snippet. For information about text snippets, see [Using Text Snippets](#using-text-snippets).

See [Module and assembly examples](#module-and-assembly-examples) for real-world examples of assemblies, modules, and their individual parts.

### Concept modules

This section explains what a concept module is and provides recommended practices for writing concept modules.

### Concept module definition

A concept module is an "understand" module. Concept modules give the user descriptions and explanations needed to understand and use a product.

### Concept module guidelines

The core requirement for a concept module is explaining the idea, or concept.
A concept module requires a short introduction and optionally, can also include additional resources.

When planning a concept module, look at nouns in related procedure modules and assemblies to find the concepts to explain to users.
Explain only things that are visible to users.
Even if a concept is interesting, it probably does not require an explanation if it is not visible to users.

#### Concept introduction

The introduction to a concept module is a single, concise paragraph that provides a short overview of the module.
A short description makes the module more usable because users can quickly determine whether the concept is useful without having to read the entire module.

The introduction typically answers the following questions:

* What is the concept?
* Why should the user care about the concept?

For details and examples, see the [Short descriptions](https://redhat-documentation.github.io/supplementary-style-guide/#shortdesc) section in the Red Hat supplementary style guide.

#### Concept body

The concept body describes the subject of the concept module.

Apart from paragraphs, you can use other AsciiDoc elements, such as lists, tables, or examples.
Consider including graphics or diagrams to speed up the understanding of the concept.

Avoid including instructions to perform an action. Action items belong in procedure modules. However, in some cases a concept or reference module can include suggested actions when those actions are simple, are highly dependent on the context of the module, and have no place in any procedure module. In such cases, ensure that the heading of the concept or reference remains a noun phrase and not a gerund. For example, see link:https://access.redhat.com/documentation/en-us/red_hat_process_automation_manager/7.9/html-single/developing_decision_services_in_red_hat_process_automation_manager/index#bound_variables_in_patterns_and_constraints[
"Bound variables in patterns and constraints"] and the sections that follow it. These concept and reference modules contain actions that are not suitable for standalone procedure modules but are relevant actions to understand in the context of the concept or reference being described.

See also [The DITA Topic Types](https://informationmapping.com/blogs/news/the-dita-topic-types-square-pegs-and-round-holes?_pos=1&_sid=45011393d&_ss=r) at _informationmapping.com_ for more information about different types of conceptual information: principle, concept, structure, process, and fact.

If the concept module is large and complex, consider splitting the concept module into multiple standalone concept modules. If you cannot split the module into meaningful standalone modules, consider using subheadings in the module to structure the content for improved reader navigation. If you use subheadings in a concept module, you can add the `[discrete]` tag to exclude each subheading from the table of contents, if needed. However, in many cases, subheadings are helpful to include in the table of contents to improve content searchability.

**NOTE**
You can use subheadings in concept or reference modules, but not in procedure modules.

#### Concept additional resources

The optional additional resources list links to other material closely related to the contents of the concept module, for example, other documentation resources.

Focus on relevant resources that might interest the user. Do not list resources for completeness.

#### Additional resources

* Download the [concept module template (adoc file)](https://raw.githubusercontent.com/redhat-documentation/modular-docs/master/modular-docs-manual/files/TEMPLATE_CONCEPT_concept-explanation.adoc) for new projects.
* For real-world examples of concept modules, see [Concept module examples](#concept-module-examples).

### Procedure modules

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

### Reference modules

This section explains what a reference module is and provides recommended practices for writing reference modules.

### Reference module definition

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

### Reference module guidelines

The required part of a reference module is the reference data.
A reference module requires a short introduction.

#### Reference introduction

The introduction to a reference module is a single, concise paragraph that provides a short overview of the module. A short description makes the module more usable because users can quickly determine whether the reference is useful without having to read the entire module.

For details and examples, see the [Short descriptions](https://redhat-documentation.github.io/supplementary-style-guide/#shortdesc) section in the Red Hat supplementary style guide.

#### Reference body

A reference module has a very strict structure, often in the form of a list or a table. A well-organized reference module enables users to scan it quickly to find the details they want.

To make the reference data easier to scan, organize it in a logical order (such as alphabetically) or as a table. AsciiDoc markup to consider for reference data:

* [Lists](http://asciidoctor.org/docs/asciidoc-syntax-quick-reference/#lists) (unordered, labeled)
* [Tables](http://asciidoctor.org/docs/asciidoc-syntax-quick-reference/#tables)

If you have a large volume of the same type of information to document, use a structure into which the information details can fit, and then document each logical unit of information as one reference module. For example, think of man pages, which document very different information details, but which still use consistent titles and formats to present those details in a uniform information structure.

If the reference module is large and complex, consider splitting the reference module into multiple standalone reference modules. If you cannot split the module into meaningful standalone modules, consider using subheadings in the module to structure the content for improved reader navigation. If you use subheadings in a reference module, you can add the `[discrete]` tag to exclude each subheading from the table of contents, if needed. However, in many cases, subheadings are helpful to include in the table of contents to improve content searchability.

**NOTE**
You can use subheadings in concept or reference modules, but not in procedure modules.

#### Additional resources

* Download the [reference module template (adoc file)](https://raw.githubusercontent.com/redhat-documentation/modular-docs/master/modular-docs-manual/files/TEMPLATE_REFERENCE_reference-material.adoc) for new projects.
* For real-world examples of reference modules, see [Reference module examples](#reference-module-examples).
* For advice on when to use lists and when to use tables, see [Let’s bring &lt;table> to the table, again.](https://medium.com/@heyoka/lets-bring-table-to-the-table-again-f1ae751159d5)

### File names and anchors

Create snake-case lower case file names. 

**NOTE**
Do not include special characters in file names. Ensure that all members of your team use the same file naming conventions.

### Forming assemblies

This section explains what an assembly is and provides recommended practices for forming assemblies.

### Assembly definition

An assembly is a collection of modules that describes how to accomplish a user story. See also [Understanding modular documentation](#understanding-modular-documentation).

### Assembly guidelines

The required parts of an assembly are the introduction and modules. Optionally, an assembly can also include prerequisites and additional resources.

#### Assembly title

If the assembly describes a task and includes one or more procedure modules, start the title with a verb in the gerund form, such as Creating or Configuring, for example _Encrypting block devices using LUKS_. If the assembly does not include any procedure modules, use a noun phrase, for example _Red Hat Process Automation Manager API reference_.

#### Assembly introduction

The introduction explains what the user accomplishes by working through the assembled modules. It typically provides context for the assembly.

Consider rewording the user story to write the assembly introduction, for example:

* User story: As an administrator, I want to provide external identity, authentication and authorization services for my Atomic Host, so that users from external identity sources can access the Atomic Host.
* Assembly introduction: As a system administrator, you can use SSSD in a container to provide external identity, authentication, and authorization services for the Atomic Host system. This enables users from external identity sources to authenticate to the Atomic Host.

For details and examples, see the [Short descriptions](https://redhat-documentation.github.io/supplementary-style-guide/#shortdesc) section in the Red Hat supplementary style guide.

#### Assembly prerequisites

Prerequisites are conditions that must be satisfied before the user can start following the assembly and are applicable to all the modules in the assembly.

Use the second level heading syntax for the Prerequisites section in the assembly so that it is displayed in the table of contents and is consistent with the Additional resources or Next steps sections in the assembly.

#### Assembly modules

All module and assembly titles must use the H1 heading designation, such as `= My heading`.

#### Next steps and Additional resources
These sections are optional. If you use both **Next steps** and **Additional resources**, list **Next steps** first. The listed resources link to other material closely related to the contents of the module, such as other documentation resources, instructional videos, or labs.

Focus on relevant resources that might interest the user. Do not list resources for completeness. If a resource applies to all of the modules in a user story, consider listing the resource in the Additional resources section of the assembly file. If you do this, consider including the resource in the procedure module as a comment.

**NOTE**
If you use **Next steps** or **Additional resources** in an assembly file, check whether the last module in the assembly also has **Next steps** or **Additional resources**. If so, view the rendered HTML and consider rewriting or reorganizing the assembly.
