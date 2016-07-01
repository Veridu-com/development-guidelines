# Developing the Development Guide for Developers

DONE, noun:

- **Coded to standards**: we have coding standards, follow them as they make life easier to everyone who may deal with your code
> I've used the coding standards, so nobody will waste time figuring out what I meant with `StringBuffer a=new StringBuffer();a.append(loc+"?"+var1+"&param1"+var2+"&param2"+var3+"&param3"+var4+"&param4"+var5+"&param5"+var6+"&param6");return a.toString();`.
- **Unit tested and human tested**: unit tests help spot silly bugs, decreasing effort spent on human testing and bux fixing
> I created unit tests so if I screw up my class X, I'll notice that it affects class Y somewhere else before anybody else has to try it.
- **Successfully built/linted**: compiled projects must be successfully built; interpreted projects must be successfully linted
> I properly built/linted my project, so silly type or syntax errors won't bother anybody else.
- **Reviewed**: all code must be reviewed before being used in production environments
> I've reviewed your code, so we're more sure it's good quality.
- **Committed**: all code must be under a version control system
> I've deleted a really important class, but it's fine, I have it on GIT.

## Guidelines

- Development
    - [First Steps](Development/FirstSteps.md)
    - [GIT](Development/GIT.md)
    - [Coding Standard](Development/Standard.md)
    - [Documentation](Development/Documentation.md)
    - [Unit Tests](Development/UnitTests.md)
    - [Project Boilerplates](Development/Boilerplate.md)
    - Languages
        - [PHP](Development/languages/php)
        - [Javascript](Development/languages/javascript)
        - [Java](Development/languages/java)
        - [Python](Development/languages/python)
    - Editors
        - [Eclipse](Development/editors/eclipse)
        - [SublimeText](Development/editors/sublimetext)
        - [VIM](Development/editors/vim)
    - [Software Version](Development/SoftwareVersion.md)
    - [Optimizations](Development/Optimizations.md)
    - [General Suggestions](Development/Suggestions.md)
    - GUIs for databases
        - [Oracle SQL Developer](Development/guis/OracleSQLDev.md)
        - [Robomongo](Development/guis/Robomongo.md)
- Deployment
    - [Code Review](Deployment/CodeReview.md)
    - [Continuous Integration](Deployment/ContinuousIntegration.md)
    - [Deploy](Deployment/Deploy.md)

## Owners

These are the list of people you should reach out to items related to languages or processes.

- Languages
    - Java: Cássio
    - Javascript: Rafael
    - PHP: Flávio
    - Python: Cássio & Håkan
- Code Review:
    - Front-end: Flávio & Rafael
    - Back-end: Flávio & Rafael
    - Models: Cássio & Håkan
- Deploy: Flávio

Bear in mind that as part of the engineering team, we are all owners of every and each project, so if you spotted anything you think should be different (a bug, a security issue, code not following standards etc), either open an issue, fix it or talk to whoever is responsible for the project.
