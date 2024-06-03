# Breakdown

# Milestones Table

## Milestone 1

### PR 1.1
**Introduce RunCoverage and CoverageRunner utilities to run code coverage for a specific bazel test target.**

| Starting Date | Creation Date | Merge Date |
| ------------- | ------------- | ---------- |
| 27-05-2024    | 01-05-2024    | 03-06-2024 |

### Tasks

| Task | Due Date |
| ---- | -------- |
| ⬜ Setup the workspace with bazel 6.2.0. | 27-05-2024 |
| ⬜ Introduce RunCoverage script. | 27-05-2024 |
| ⬜ Introduce CoverageRunner utility to call Bazel command. | 28-05-2024 |
| ⬜ Add implementation in BazelClient to execute Bazel coverage command. | 29-05-2024 |
| ⬜ Add tests for execution of Bazel coverage command through RunCoverage script. | 01-05-2024 |

### PR 1.2
**Updating the test exemption script.**

| Starting Date | Creation Date | Merge Date |
| ------------- | ------------- | ---------- |
| 01-06-2024    | 03-06-2024    | 05-06-2024 |

### Tasks

| Task | Due Date |
| ---- | -------- |
| ⬜ Update the test exemption check script proto. | 01-06-2024 |
| ⬜ Update the exemption_type data. | 02-06-2024 |
| ⬜ Add / Update tests for TestFileCheckTest scripts as required. | 03-06-2024 |

### PR 1.3
**Update / Implement script to run code coverage for a specific file replacing test target argument.**

| Starting Date | Creation Date | Merge Date |
| ------------- | ------------- | ---------- |
| 03-06-2024    | 08-06-2024    | 10-06-2024 |

### Tasks

| Task | Due Date |
| ---- | -------- |
| ⬜ Update the script to take in a file as argument instead of target. | 03-05-2024 |
| ⬜ Check with the exempted test file list to log the coverage ratio to 0%. | 03-06-2024 |
| ⬜ Add functionality to map the file name to related test targets. | 04-06-2024 |
| ⬜ Include execution for related Test and LocalTest Targets. | 06-06-2024 |
| ⬜ Add tests for execution of Bazel coverage command with filename. | 08-06-2024 |

### PR 1.4
**Interpreting the results and building proto for data processing.**

| Starting Date | Creation Date | Merge Date |
| ------------- | ------------- | ---------- |
| 08-06-2024    | 13-06-2024    | 15-06-2024 |

### Tasks

| Task | Due Date |
| ---- | -------- |
| ⬜ Extract the coverage data path from the results. | 08-06-2024 |
| ⬜ Introduce coverage.proto to store the produced coverage data. | 08-06-2024 |
| ⬜ Parse the coverage data and store them to the proto. | 10-06-2024 |
| ⬜ Isolate the coverage data to only contain the target coverage data. | 11-06-2024 |
| ⬜ Include coverage data to proto for any related tests - 'LocalTest'. | 12-06-2024 |
| ⬜ Add tests to validate acquired coverage data stored in the proto. | 13-06-2024 |

### PR 1.5
**Introduce CoverageReporter utility and generate the code coverage report.**

| Starting Date | Creation Date | Merge Date |
| ------------- | ------------- | ---------- |
| 13-06-2024    | 20-06-2024    | 22-06-2024 |

### Tasks

| Task | Due Date |
| ---- | -------- |
| ⬜ Introduce CoverageReporter utility to generate the code coverage report. | 13-06-2024 |
| ⬜ Compute the coverage Ratio. | 13-06-2024 |
| ⬜ Generate Markdown report with proto. | 15-06-2024 |
| ⬜ Generate HTML report with proto. | 18-06-2024 |
| ⬜ Add tests to validate the Markdown and HTML report generation and coverage ratios. | 20-06-2024 |

### Buffer Time
**To work on reviews and code changes.**

| Starting Date | Creation Date | Merge Date |
| ------------- | ------------- | ---------- |
| 22-06-2024    | 26-06-2024    | 28-07-2024 |

### Midpoint Evaluation
**Code Reviews and Evaluations**

| Starting Date | Creation Date | Merge Date |
| ------------- | ------------- | ---------- |
| 28-06-2024    | 08-07-2024    | 12-07-2024 |


## Milestone 2

### PR 2.1
**Introduce new CI workflow for code coverage**

| Starting Date | Creation Date | Merge Date |
| ------------- | ------------- | ---------- |
| 12-07-2024    | 22-07-2024    | 24-07-2024 |

### Tasks

| Task | Due Date |
| ---- | -------- |
| ⬜ Introduce a new CI workflow that utilizes the coverage script. | 13-07-2024 |
| ⬜ Configure it to run it with and without cache. | 15-07-2024 |
| ⬜ Configure it to run as a series of buckets. | 18-07-2024 |
| ⬜ Configure it to fail if it's below the threshold. | 20-07-2024 |
| ⬜ Configure it to generate markdown reports. | 22-07-2024 |
| ⬜ Analyze the new runs. | 22-07-2024 |

### PR 2.2
**Upload generated markdown report as comment**

| Starting Date | Creation Date | Merge Date |
| ------------- | ------------- | ---------- |
| 22-07-2024    | 26-07-2024    | 28-07-2024 |

### Tasks

| Task | Due Date |
| ---- | -------- |
| ⬜ Modify the workflow to upload markdown report as a comment. | 24-07-2024 |
| ⬜ Test markdown report upload feature. | 25-07-2024 |
| ⬜ Review and refine markdown upload implementation. | 26-07-2024 |

### PR 2.3
**Fix/replace cancellation workflow**

| Starting Date | Creation Date | Merge Date |
| ------------- | ------------- | ---------- |
| 26-07-2024    | 01-08-2024    | 03-08-2024 |

### Tasks

| Task | Due Date |
| ---- | -------- |
| ⬜ Identify issues with the current cancellation workflow. | 26-07-2024 |
| ⬜ Execute and analyze cancellation with styfle - PR #2890. | 28-07-2024 |
| ⬜ Develop replacement or fix for the cancellation workflow. | 30-08-2024 |
| ⬜ Validate the new cancellation workflow. | 01-08-2024 |

### PR 2.4
**Create wiki page explaining code coverage usage, limitations, file issues for coverage gaps, and test writing tips**

| Starting Date | Creation Date | Merge Date |
| ------------- | ------------- | ---------- |
| 01-08-2024    | 04-08-2024    | 06-08-2024 |

### Tasks

| Task | Due Date |
| ---- | -------- |
| ⬜ Introduce new wiki page for "how to use the code coverage tool". | 01-08-2024 |
| ⬜ Introduce new wiki page for "how to write tests with good behavioral coverage". | 02-08-2024 |
| ⬜ Introduce new wiki page for "Limitations of the code coverage tool". | 03-08-2024 |
| ⬜ File issues for missing / incorrect code coverages. | 04-08-2024 |

### Buffer Time
**To work on reviews and code changes.**

| Starting Date | Creation Date | Merge Date |
| ------------- | ------------- | ---------- |
| 06-08-2024    | 10-08-2024    | 12-08-2024 |

### Final Evaluation
**Code Reviews and Evaluations**

| Starting Date | Creation Date | Merge Date |
| ------------- | ------------- | ---------- |
| 12-08-2024    | 26-08-2024    | 03-09-2024 |

### Spare Intervals
**Spare intervals to fix any further issues.**

| Starting Date | Creation Date | Merge Date |
| ------------- | ------------- | ---------- |
| 03-09-2024    | N/A           | End of GSoC period |
