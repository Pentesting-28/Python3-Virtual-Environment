## Managing Virtual Environments with `venv`

Using virtual environments in Python is essential to keep your project's dependencies isolated, avoiding conflicts between libraries. Here's how to create, activate, and manage a virtual environment.

### 1. Create a Virtual Environment

```sh
python -m venv venv
```

This command creates a virtual environment in a directory called `venv`. A virtual environment is an isolated copy of Python that allows you to install packages without affecting the global environment.

### 2. Activate the Virtual Environment

- **Windows:**

  ```sh
  venv\Scripts\activate
  ```

- **Unix/MacOS:**

  ```sh
  source venv/bin/activate
  ```

Once activated, all packages installed using `pip` will be added to the virtual environment.

### 3. Save Dependencies

```sh
pip freeze > requirements.txt
```

This command saves all libraries installed in the virtual environment to a `requirements.txt` file, allowing you to replicate the environment on other machines.

### 4. Install Dependencies from `requirements.txt`

```sh
pip install -r requirements.txt
```

This installs all libraries listed in `requirements.txt`, ensuring the environment has the same dependencies.

### 5. Complete Workflow

1. Create the virtual environment:

   ```sh
   python -m venv venv
   ```

2. Activate the virtual environment:

   - **Windows:** `venv\Scripts\activate`
   - **Unix/MacOS:** `source venv/bin/activate`

3. Install dependencies:

   ```sh
   pip install <package-name>
   ```

4. Save dependencies to `requirements.txt`:

   ```sh
   pip freeze > requirements.txt
   ```

5. To share your environment, others can install the same dependencies by running:

   ```sh
   pip install -r requirements.txt
   ```

---

This process ensures that all developers are working with the same library versions, avoiding compatibility issues and providing a consistent environment across different machines.