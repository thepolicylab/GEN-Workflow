---
title: Starting a Project
date: 2018-09-15 07:42:34
slug: starting-a-project
---

## Project Structure

Having a clear structure for projects makes it easier to organize, manage, and search for information. While there are no strict rules regarding how a Python project directory should be structured, there are [guidelines](https://docs.python-guide.org/writing/structure/) and even packages (see [the `Cookiecutter` package](https://cookiecutter.readthedocs.io/en/latest/README.html#a-pantry-full-of-cookiecutters)) designed for this purpose. For us at The Policy Lab, we follow most of the guidelines in [this article](https://docs.python-guide.org/writing/structure/) with a few adaptations. Below is what a Python project directory usually looks like:

```
Project Directory

/package_name   # the name of the package
/data           # stores the data used in the project, will not be pushed to Github
    /raw        # stores raw data
    /processed  # stores processed data
/models         # stores models trained during the model building process
/tests          # for tests
    /fixtures   # stores fixtures for tests
/docs           # stores documentation for the project, if applicable
setup.py
conftest.py
README.md
requirements.txt
.gitignore
```

[This Github repo](https://github.com/thepolicylab/GEN-ProjectTemplate) is an example of this structure. It also serves as a template for new projects. Feel free to clone or fork this repo to start a new project.

When creating a new project, name the root directory and the Github repo following The Policy Lab project naming convention: Name of the agency that the project is for in all-caps (e.g. EOHHS), followed by a dash and the name of the project in CamelCase.  For example, if you are working with RIDE on a project called "Early Warning System", then the name of the project directory and the Github repo should be `RIDE-EarlyWarningSystem`.