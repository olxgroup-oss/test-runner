<p align="center">
<img src="https://github.com/olxgroup-oss/olx-test-runner/blob/main/assets/logos/logo_big.png?raw=true" height="100" alt="OLX Test Runner Logo" />
</p>

<p align="center">
<a href="https://github.com/olxgroup-oss/olx-test-runner/actions/"><img src="https://github.com/olxgroup-oss/olx-test-runner/actions/workflows/quality-gate.yml/badge.svg" alt="Quality gate"></a>
<a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/license-MIT-purple.svg" alt="License: MIT"></a>
</p>

# OLX Test runner

The OLX Test Runner library is an solution designed to speed up unit tests on slow machines. For
developers working on Flutter projects, running tests can often become a time-consuming task,
especially when working with diverse environments that may not have optimal performance.
This library addresses the issue by combining individual tests into test groups, boosting the
efficiency and reducing the execution time of your test suite. By leveraging smarter grouping and
execution, OLX Test Runner ensures your testing workflow is streamlined and faster, allowing you to
focus on development and iteration rather than waiting for slow tests to complete.

### Key Features:

- Improved testing speed: combines tests into groups, minimizing overhead and speeding up execution
  even on low-performing machines.
- Command-Line Interface (CLI): a robust CLI tool specially tailored for Flutter projects, enabling
  seamless integration and easy usage.
- Optimized workflows: focuses on providing a productive and efficient testing experience, crucial
  for teams working with large codebases or in challenging environments.

This library solves an ongoing problem in the Flutter community, as outlined
in [the issue](https://github.com/flutter/flutter/issues/69429). It is your go-to tool for ensuring
unit tests run swiftly.

### Documentation:

Documentation can be found [here](https://olxgroup-oss.github.io/olx-test-runner/)

## How to use:

To activate locally, go to the path with `olx_test_runner` directory and then run this
command:

```shell
dart pub global activate olx_test_runner --source path
```

This will hook package from local directory into dart runtime.

To activate (not locally) latest released version, run this command:

```shell
dart pub global activate olx_test_runner
```

## Commands:

### Generate Command :dart:

The Test Group Generation is a core feature of the OLX Test Runner library that helps you generate
optimized test groups for your Flutter project. This functionality is designed to make it easy to
structure and execute your tests efficiently.

#### Command Overview

The command can be executed with the following syntax:

```
dart pub global run olx_test_runner generate <options>
```

This command allows you to customize the test grouping process using various options to best fit the
needs of your test environment.
Running this command will generate test groups file inside your `test-path` directory.
More about this command can be found in
the [documentation](https://olxgroup-oss.github.io/olx-test-runner/guides/generate/).

### Test Command :test_tube:

The Test Command is an all-in-one solution for generating, running, and displaying the results of
test groups within your Flutter project's test suite. It simplifies and optimizes the entire testing
process, ensuring a smooth and efficient workflow.

#### Command Overview

You can launch the test command using the following syntax:

```
dart pub global run olx_test_runner test <options>
```

The test command handles three key tasks:

1. Generating Test Groups: Automatically organizes tests into logical groups for efficient
   execution.
2. Executing tests: Runs the grouped tests while offering support for additional features like
   coverage collection.
3. Result reporting: Displays the results of the tests and optionally saves them in specified file
   paths.
   More about this command can be found in
   the [documentation](https://olxgroup-oss.github.io/olx-test-runner/guides/test/).

### Validate Command :white_check_mark:

The Validate Command is a powerful utility designed to ensure your tests are properly set up and
conform to best practices. This command analyzes your test suite for common issues and provides a
detailed report highlighting any problems. It’s an essential tool to maintain the quality and
organization of your tests.

#### Command Overview

You can run the validate command using the following syntax:

```
dart pub global run olx_test_runner validate <options>
```

After execution, the command will analyze test files and provide verbose output indicating any
issues or confirming that the test files are valid.
More about this command can be found in
the [documentation](https://olxgroup-oss.github.io/olx-test-runner/guides/validate/).

## Example usage

Generate test groups:

```bash
dart pub global activate olx_test_runner
dart pub global run olx_test_runner generate --test-path ./test --seed 54382123 --shard-count 3
```

Run tests:

```bash
dart pub global activate olx_test_runner
dart pub global run olx_test_runner test --test-path ./test --seed 54382123 --shard-count 3 --result-path . --coverage
```

Validate test groups:

```bash
dart pub global activate olx_test_runner
dart pub global run olx_test_runner validate --test-path ./test 

```

## Support

Feel free to report any issue or feature
request [here](https://github.com/olxgroup-oss/olx-test-runner/issues).
