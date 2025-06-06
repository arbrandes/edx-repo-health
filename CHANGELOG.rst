Change Log
##########

..
   All enhancements and patches to edx-repo-health will be documented
   in this file.  It adheres to the structure of http://keepachangelog.com/ ,
   but in reStructuredText instead of Markdown (for ease of incorporation into
   Sphinx documentation and the PyPI description).

   This project adheres to Semantic Versioning (http://semver.org/).

.. There should always be an "Unreleased" section for changes pending release.

Unreleased
**********


[2.0.0] - 2025-05-07
********************

Added
=====
* Added support for ``Python 3.11`` and dropped support for ``Python 3.8``


[1.1.0] - 2024-03-06
********************

Added
=====
* Added support for ``Python 3.12``


[1.1.0] - 2023-04-14
********************

Fixed
=====

* Use repo's actual org name in GitHub calls, rather than hardcoded "edx"
* Remove codecov dependency.
* Check for PyPI name will no longer fail if it finds too many or too few names.
* Use NULL for empty values in SQLite, not the string "None"
* Annotate async checks so that they aren't skipped any more

Added
=====

* Added a check to determine the amount of dependabot alerts per repo
* Added a check to determine is dependabot.yml exists in repo
* Added a check to determine is github-action, pip and npm ecosystem exists in dependabot.yml
* Added scripts/console_dashboard.py to display a selection of recommended maintenance tasks on the console in rough order of estimated priority
* Added scripts/streamlit_dashboard.py as a tool for exploring the generated SQLite file content (and experiment to explore suitability as another dashboard option)

[1.0.0] - 2023-01-02
********************

Added
=====

* Added code to generate sqlite database for repo health data.
* Added a check for the url= and project_urls= settings in setup.py and setup.cfg.
* Read yaml files for both orgs while creating dashboard

* Added a check for repos that indicate inclusion in Open edX in their openedx.yaml file, but aren't in the openedx GitHub organization.

[0.2.4] - 2022-05-23
********************

Added
=====

* Added a check to validate that pip.txt requirements are installed immediately after upgrading pip.txt in Makefile's upgrade target

[0.2.3] - 2022-04-12
********************

Changed
=======

* Removed gspread constraint to pick up fix in gspread 5.2.3.

[0.2.2] - 2022-03-11
********************

Fixed
=====

* Check the response status code when fetching from ReadTheDocs.
* Only fetch the project list once from ReadTheDocs, since it's a constant.

[0.2.1] - 2022-03-07
********************

Fixed
=====

* Fix to not have checks blow up on an uninitialized repo.
* Temporary fix for check_ownership by constraining gspread<5.2.0. See constraints.txt for details, and information on how this constraint could be removed.

[0.2.0] - 2021-11-19
********************

Fixed
=====

* Fixed code for defining version.


[0.1.8] - 2021-10-27
********************

Added
=====

* Added a check for commitlint.yaml, the GitHub Action check for conformance to
  conventional commits.

[0.1.7] - 2021-06-25
********************

Added
=====

* Added check to parse ubuntu packages from anisble playbooks.

[0.1.6] - 2021-05-19
********************

Added
=====

* Added docker file parsing check. Picking apt-get install or update packages.

[0.1.5] - 2021-05-18
********************

Fixed
=====

* Fixed package-lock.json not found error.

[0.1.4] - 2021-05-18
********************

Refactor
========

* pypi_all will show all dependencies in requirements folder.
* pypi will only show production or development related dependencies.

[0.1.3] - 2021-05-18
********************

Changed
=======

* Added all JS dependencies from package-lock.json. Updated tests.

Added
=====

* Added new column for frontend repos to track what npm package name they publish.

[0.1.2] - 2021-05-05
********************

Changed
=======

* Added development.txt and dev.txt for picking dependencies. Updated tests.

[0.1.1] - 2021-05-04
********************

Added
=====

* Added testing dependencies as separate column.

[0.1.0] - 2020-03-16
********************

First release.
