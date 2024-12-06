# Testing Python Scripts with `pytest`

Testing is a critical part of the software development process. It ensures your Python scripts function correctly and meet your expected requirements. This tutorial explains how to use `pytest` for unit tests and integration tests, how to automate testing with a Makefile, and how to integrate `pytest` into a pre-commit workflow.

---

## **What is `pytest`?**

`pytest` is a robust testing framework for Python. It supports:
- **Unit tests**: Testing individual components (e.g., functions, methods) in isolation.
- **Integration tests**: Testing how components work together in a system.
- **Fixtures**: Managing setup and teardown of test environments.

---

## **Installing `pytest`**

Install `pytest` using `pip`:

```bash
pip install pytest
```

## Project Structure

Here's an example project structure for this tutorial:
```
my_project/
├── src/
│   ├── calculator.py
├── tests/
│   ├── test_calculator.py
├── Makefile
├── requirements.txt
├── .pre-commit-config.yaml

```

