# Python Development Practices for High-Quality Projects

This guide outlines essential practices for enhancing the quality, maintainability, and efficiency of Python projects.

## Clean Machine Learning Code
Software engineering principles for Clean Machine Learning Code (CMLC) are based on the idea that **all ML software we build is software after all**. By adapting the principles of “Clean Code” to the domain of machine learning, we can improve the quality and maintainability of our ML pipelines. Some of the fundamental principles include:

**At the component level:**

* **Loose coupling:** ML components should know as little as possible about each other, making changing or replacing them more accessible.
* **High cohesion:** Elements of an ML component should belong together logically, resulting in a more straightforward and understandable code structure.
* **Local change:** Code changes should be limited to specific components to reduce associated costs and risks.
* **Easy to remove:** ML components should be easy to remove and replace with simpler alternatives.
* **Mentally sized components:** Break your ML system into components you can easily understand, making it easier to predict the consequences of changes.

**SOLID principles:**

* **Single Responsibility Principle (SRP):** An ML component should only have one reason to change.

* If a component has to change for multiple reasons, it likely has more than one responsibility and should be split.

* **Open/Closed Principle (OCP):** You should be able to extend the behavior of an ML component without modifying it.

* This can be achieved by using interfaces and abstractions, allowing new functionality to be added without changing existing code.

* **Liskov Substitution Principle (LSP):** This principle is still under development in the context of CMLC.

* **Interface Segregation Principle (ISP):** Create customer-specific ML component interfaces instead of one large generic interface. * This prevents clients from depending on the functionality they don't need and reduces the impact of changes to unrelated components.
* **Dependency Inversion Principle (DIP) and Dependency Injection Method:** Depend on abstractions instead of concreteness in your ML pipeline.
* Use dependency injection to connect components at runtime, allowing for a plugin architecture and making testing easier.

**Benefits of CMLC:**

* Reduces the cost of changes to ML pipelines.
* Increases optimal responsiveness to changes.
* Facilitates testing in isolation.

**ML Technical Debt:**

Technical debt in ML relates to violating clean code principles, leading to issues such as:

* **Entanglement:** Intertwined ML code and data violate the SRP principle.
* **Hidden feedback loops:** Deployed models change future training distributions, violating the OCP principle.
* **Undeclared consumers:** Generic interfaces allow undifferentiated access, which goes against the ISP principle.
* **Pipeline jungles:** Rigid, concrete pipelines that violate the OCP, ISP, and DIP principles.

Following CMLC principles can help avoid these problems and create more robust, maintainable, and scalable ML pipelines.


## Dependency Management
- **Use `pyproject.toml` Instead of `requirements.txt`**  
  Manage dependencies with `pyproject.toml` for increased flexibility and to avoid additional files like `dev-requirements.txt`.

- **Adopt a Version and Project Manager**  
  Tools like **Poetry** or **UV** simplify:
  - Dependency management.
  - Virtual environment creation.
  - Running applications in isolated environments.

## Code Quality and Readability
- **Incorporate Type Hints**  
  Use type hints to:
  - Improve code readability.
  - Enable static analysis tools like `ruff` and `mypy` to detect potential errors.
  - Simplify long-term code maintenance by making function parameters and return types explicit.

- **Add a "Raises" Section to Docstrings**  
  Document all possible exceptions a function may raise in the **Raises** section of its docstring. This:
  - Helps developers anticipate potential issues.
  - Simplifies code debugging and maintenance.

- **Use Pydantic Models for Data Handling**  
  Replace dictionaries and numerous function parameters with **Pydantic models** to:
  - Validate data types.
  - Handle errors efficiently.
  - Simplify data passing between functions.

## Code Analysis and Formatting
- **Implement a Linter and Formatter**  
  Use tools like **Ruff** for:
  - Enforcing `Black` formatting standards.
  - Detecting common code issues.
  - Configuring additional rules in `pyproject.toml` to ensure consistent code quality.

## Testing Practices
- **Use Pytest Instead of Unittest**  
  **Pytest** offers:
  - A concise and flexible syntax.
  - Advanced testing features, including fixtures.

## Additional Suggestions (Hot Takes)
These practices may not suit every project but are worth considering:
- **Use `orjson` Instead of `json`**  
  Gain better performance for JSON serialization and deserialization.
  
- **Prefer f-Strings Over String Concatenation**  
  Simplify string formatting with the cleaner and faster syntax of f-strings.

- **Leverage `pathlib` Instead of `os.path`**  
  Modernize file and directory manipulation with the more intuitive `pathlib` module.

- **Use `click` Instead of `argparse` or `sys.argv`**  
  Simplify CLI creation with `click`'s declarative syntax and robust features.

- **Upgrade to Python 3.8+**  
  Take advantage of newer Python features, such as:
  - Assignment expressions (walrus operator `:=`).
  - Positional-only parameters.
  - Improved typing and performance enhancements.

## Conclusion
These best practices will help you maintain a high-quality standard for your Python projects, improve collaboration, and future-proof your codebase.

## References:
- [Stop making your python projects like it was 15 years ago…](https://levelup.gitconnected.com/stop-making-your-python-projects-like-it-was-15-years-ago-125436b470a5)
- [Clean Machine Learning Code - Book](https://leanpub.com/cleanmachinelearningcode)
- [Clean ML Code - Medium](https://towardsdatascience.com/clean-machine-learning-code-bd32bd0e9212)
- [Clean Architecture: How to Structure Your ML Projects to Reduce Technical Debt by Laszlo Sragner](https://youtu.be/IXML9CVDszo)

