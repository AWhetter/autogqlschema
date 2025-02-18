Changelog
=========

Versions follow `Semantic Versioning <https://semver.org/>`_ (``<major>.<minor>.<patch>``).

.. towncrier release notes start

v1.0.0 (2025-02-17)
-------------------

Features
^^^^^^^^

- Add support for Python 3.13


Misc
^^^^

- Drop support for Python 3.8
- Switch from black to ruff
- Update development workflows to use Python 3.13


v0.2.0 (2023-11-12)
-------------------

Features
^^^^^^^^

- Can correctly parse CommonMark syntax in docstrings


Bugfixes
^^^^^^^^

- Can read source files in any order
- Fix indentation issues causing incorrect rendering
- Fix relative root directories always erroring


v0.1.0 (2023-09-30)
-------------------

Features
^^^^^^^^

- Initial implementation
