# Breakdown

## Milestone 1: 
Introduce a new script to compute a per-unit code coverage percentage for a single file.
 ### Deliverable 1:
  - [ ] Setup the workspace with bazel 6.2.0 once the source code is updated and confirm the migration works seamlessly.
  - [ ] Introduce RunCoverage.kt and CoverageRunner.kt to run code coverage for a specific bazel test target, interpret coverage result.
  - [ ] Implement proto processing to interpret the results as proto for data processing.
 
 ### Deliverable 2:
  - [ ] Introduce CoverageReporter.kt to generate Coverage Report in desired format.
  - - [ ] Markdown
  - - [ ] HTML
   
### Deliverable 3:
  - [ ] Update test exemption script
  - [ ] Update script to accept minimum coverage arg
  - [ ] Add tests for Milestone1

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
| 27-05-2024    | 30-05-2024    | 02-06-2024 |

### Tasks

| Task | Due Date |
| ---- | -------- |
| ⬜ Setup the workspace with bazel 6.2.0. | 27-05-2024 |
| ⬜ Introduce RunCoverage script. | 27-05-2024 |
| ⬜ Introduce CoverageRunner utility to call Bazel command. | 28-05-2024 |
| ⬜ Add implementation in BazelClient to execute Bazel coverage command. | 30-05-2024 |

### PR 1.2
**Interpreting the results and building proto for data processing.**

| Starting Date | Creation Date | Merge Date |
| ------------- | ------------- | ---------- |
| 02-06-2024    | 09-06-2024    | 11-06-2024 |

### Tasks

| Task | Due Date |
| ---- | -------- |
| ⬜ Extract the coverage data path from the results. | 02-05-2024 |
| ⬜ Introduce coverage.proto to store the produced coverage data. | 03-06-2024 |
| ⬜ Parse the coverage data and store them to the proto. | 05-06-2024 |
| ⬜ Isolate the coverage data to only contain the target coverage data. | 07-06-2024 |
| ⬜ Include coverage data for any related tests - 'LocalTest'. | 09-06-2024 |

### PR 1.3
**Introduce CoverageReporter utility and generate the code coverage report.**

| Starting Date | Creation Date | Merge Date |
| ------------- | ------------- | ---------- |
| 11-06-2024    | 20-06-2024    | 22-06-2024 |

### Tasks

| Task | Due Date |
| ---- | -------- |
| ⬜ Introduce CoverageReporter utility to generate the code coverage report. | 12-06-2024 |
| ⬜ Compute the coverage Ratio. | 13-06-2024 |
| ⬜ Generate Markdown report with proto. | 16-05-2024 |
| ⬜ Generate HTML report with proto. | 20-05-2024 |

### PR 1.4
**Updating the test exemption script.**

| Starting Date | Creation Date | Merge Date |
| ------------- | ------------- | ---------- |
| 22-06-2024    | 26-06-2024    | 28-06-2024 |

### Tasks

| Task | Due Date |
| ---- | -------- |
| ⬜ Update the test exemption check script proto. | 24-06-2024 |
| ⬜ Update the exemption_type data. | 26-06-2024 |

### Buffer Time
**To work on reviews and code changes.**

| Starting Date | Creation Date | Merge Date |
| ------------- | ------------- | ---------- |
| 28-06-2024    | 01-07-2024    | 03-07-2024 |

### Midpoint Evaluation
**Code Reviews and Evaluations**

| Starting Date | Creation Date | Merge Date |
| ------------- | ------------- | ---------- |
| 04-07-2024    | 06-07-2024    | 08-07-2024 |
