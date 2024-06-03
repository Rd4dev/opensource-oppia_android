# Breakdown

## Milestone 1: 
Introduce a new script to compute a per-unit code coverage percentage for a single file.
 ### Deliverable 1:
  - [ ] Setup the workspace with bazel 6.2.0 once the source code is updated and confirm the migration works seamlessly.
  - [ ] Introduce RunCoverage.kt and CoverageRunner.kt to run code coverage for a specific bazel test target, interpret coverage result.
  - [ ] Add tests for execution Bazel coverage command.
  - [ ] Implement proto processing to interpret the results as proto for data processing.
  - [ ] Add tests to validate stored coverage proto.
 
 ### Deliverable 2:
  - [ ] Introduce CoverageReporter.kt to generate Coverage Report in desired format.
  - - [ ] Markdown
  - - [ ] HTML
  - [ ] Add tests to validate generated reports
   
### Deliverable 3:
  - [ ] Update test exemption script
  - [ ] Update script to accept minimum coverage arg
  - [ ] Add tests for test exemption

## Milestone 2: 
 Integrate code coverage checking.
 ### Deliverable 1:
  - [ ] Implement options for single target coverage analysis and report generation.
  - [ ] Set configuration option to fail if it's below a specified threshold.
 
 ### Deliverable 2:
  - [ ] Introduce new CI workflow for code coverage
  - [ ] Run code coverage only after tests are passing
  - [ ] Reports uploaded as comments to the pr
   
 ### Deliverable 3:
  - [ ] Fix/replace the cancellation workflow to ensure re-runs of CI correctly and quickly terminate all existing workflows.
  - [ ] Add tests for Milestone2 

 ### Deliverable 4:
  - [ ] Introduce a wiki page explaining how to use the code coverage tool, provide advice on how to write tests with good behavioral coverage, and explain the limitations of the code coverage tool (i.e. all the cases it does not correctly count coverage for a specific line).

 ### Deliverable 5:
  - [ ] File issues for all cases where the code coverage tool misses or incorrectly counts code coverage for future work.

<br>

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
