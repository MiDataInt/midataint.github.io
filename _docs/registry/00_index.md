---
title: Tool Suite Registry
has_children: true
nav_order: 50
---

## {{page.title}}

We are pleased to list public MDI tool suites registered by 
established code providers. 

Providers, please see 
[these instructions](/mdi-suite-template/docs/suite_sharing.html#add-your-public-tools-to-the-mdi-suite-registry)
for getting your suites listed.

### Security notice
Be advised that people with malicious intent
could include dangerous code in their tool suite, as
with any software they provide to you. 

We perform an initial, basic level of code review for appropriateness,
but cannot deeply audit every tool. Tool suites are maintained by providers,
not the MDI team, and will change over time without our knowledge or approval.

You, the user, are 
responsible for deciding whether to trust the people writing
the tools you use and accept all risks and responsibilities for doing so.

To promote transparency and safety, we only list:

- open-source, publicly accessible tool suites, so you can read the
code you are executing.
- tool suites with publicly identified authors, so you
 know who is responsible for the code you use.
- code from providers who agreed in a public pull request to abide
by the Code of Conduct below.

### MDI developer Code of Conduct

Tool suite developers must follow these principles when writing code
to be executed in the Michigan Data Interface.

- Tools will only perform actions on the user's system consistent with
their stated purpose. 
- No attempt will be made to send user data to a third party,
over the internet or by any other means, unless doing so is a stated
purpose of the tool and the third party is clearly identified or chosen
by the user.
- Only files understood to be derived from input options will be 
read from the user's file system; no attempt will be made to mine 
any other files for data.
- All files created by a pipeline will be written to the directory defined by
options `--output-dir` and `--data-name`, `--tmp-dir`, `--tmp-dir-large`, or 
another path as long as it is clearly communicated by other pipeline options. 
- All files created by an app will be written into the directory or subdirectories
known as `mdiDir` or `MDI_DIR`, or paths specified by the user in the `paths` key of configuration file stage2-apps.yml.
- No files created by a pipeline or app will contain executable code unless doing so is a stated purpose of the tool confirmed by the user, and, in that case, execution of that code will not do harm to the user's system.
- All software installed on behalf of a tool, including but not limited to conda
environments and R packages, will abide by the same rules as stated above.
