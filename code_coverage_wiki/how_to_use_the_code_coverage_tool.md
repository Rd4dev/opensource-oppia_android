# How to use the code coverage tool

How to Use the Code Coverage Tool in the Oppia Android Codebase
Oppia provides code coverage analysis reports in two ways: through the CI process on PRs and via local CLI tools.

1. Code Coverage in Pull Requests (PRs)
When you push your code, the Continuous Integration (CI) system runs code coverage checks on the changed files. It performs analysis and uploads the code coverage report as a comment on your PR. This report includes:

- Failed Coverage Cases: A table representing the files that failed to meet the minimum coverage threshold.
- Successful Coverage Cases: Listed under a dropdown, these are the files that passed the coverage checks.
- Anomaly Cases: Files that are exempt from having a minimum coverage requirement or files where coverage data retrieval failed.

Your code needs to pass the minimum coverage threshold to pass the coverage check. Note that some files are exempt from this requirement and may still pass even if below the threshold.

2. CLI Tools for Local Coverage Check Analysis
To perform a local coverage analysis, use the CLI command:

```
bazel run //scripts:run_coverage path/to/file1.kt path/to/file2.kt (optional) --processTimeout=10 --format=html

```

- List of Files: Provide the list of files you want to analyze.
- processTimeout: Optional parameter to specify how long the process should wait before ending (depends on your machine performance).
- format: Output format of the coverage report. Oppia Android supports two formats:
md for a quick report (similar to PR comments).
html for a detailed local development report (default).

When you run the coverage script, it generates the report in the specified path, typically coverage_reports/path/to/file/coverage.html.

Opening the HTML report provides a visual representation:

Green Lines: Code covered by tests.
Red Lines: Code not covered by tests.
Top Banner: Displays total lines, lines hit, and overall coverage percentage.
Steps to Use the HTML Report
1. Analyze the red lines in the HTML report to identify untested code.
2. Check if there are existing test cases for those lines. 
3. If not, add the necessary test cases.
4. Run the CLI command again to generate an updated coverage report.
5. Ensure the coverage status report shows as PASS.

By following these steps, you can effectively use the code coverage tools provided by Oppia Android to ensure your code meets the required standards.