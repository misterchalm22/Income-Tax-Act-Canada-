# Canadian Tax Law: Excluded Entity

This project provides an implementation of the definition of an "excluded entity" from Canadian tax legislation, written in the [Catala](https://catala-lang.org/) programming language.

Catala is a domain-specific language for translating law into code, and this project uses its literate programming features to create an implementation that is highly faithful to the original legal text.

## Project Structure

*   `src/excluded_entity.catala_en`: The main Catala file containing the legal text and the implementation.
*   `tests/test_excluded_entity.catala_en`: The test suite for the implementation.
*   `clerk.toml`: The configuration file for the Catala build system, `clerk`.

## Setup

To work with this project, you need to install the Catala compiler and its dependencies.

1.  **Install opam:**
    Follow the instructions on the [opam website](https://opam.ocaml.org/doc/Install.html) to install the OCaml package manager. For example, on Debian-based systems:
    ```bash
    sudo apt-get update
    sudo apt-get install -y opam
    ```

2.  **Initialize opam:**
    ```bash
    opam init -c 4.14.2 --disable-sandboxing -y
    eval $(opam env)
    ```

3.  **Install Catala:**
    You will also need to install the system dependencies `default-jdk` and `libgmp-dev`.
    ```bash
    sudo apt-get install -y default-jdk libgmp-dev
    opam pin catala.dev git+https://github.com/CatalaLang/catala -y
    ```

4.  **Verify the installation:**
    ```bash
    catala --version
    ```

## Building and Testing

This project uses the `clerk` build system, which is included with Catala.

To build the project and run the tests, navigate to the project's root directory (`canadian-tax-law`) and run the following command:

```bash
clerk test
```

This command will discover the build target and the associated tests defined in `clerk.toml`, compile the code, and run the test suite.
