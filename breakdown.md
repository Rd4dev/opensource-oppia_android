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


## Milestones Table

| ✅   | Task                      | Description of PR / action                                                       | Target date for PR creation | Target date for PR to be merged | Notes |
|-----------|---------------------------|----------------------------------------------------------------------------------|-----------------------------|-----------------------------------| --------|
|    | **MILESTONE 1**           |                                                                                   |                             |                                   |        |
| ⬜  | Milestone 1.1             | Introduce RunCoverage.kt and CoverageRunner.kt to run code coverage for a specific bazel test target, interpret coverage result  | 10-06-2024                  | 15-06-2024                |    Additonal Notes  |
| ⬜  | Sub-milestone 1.1 Task 1 | Implement proto processing                                                       | 15-06-2024                  | 20-06-2024                        |    |
| ⬜  | Milestone 1.2             | Introduce CoverageReporter.kt to generate Coverage Report in desired format      | 25-06-2024                  | 28-06-2024                        |    |
|    |**Internal Evaluation**| Internal evaluation - Milestone 1                                                | 28-06-2024                  |                                   |    |
| ⬜  | Milestone 1.3 Task 1      | Update test exemption script                                                     | 05-07-2024                  | 08-07-2024                        |    |
|    | **Buffer Time** |Buffer time for revision - Phase 1                                               | 01-07-2024                  | 08-07-2024                        |    |
| ⬜  | Milestone 1.3 Task 2      | Update script to accept minimum coverage arg and add tests for Milestone 1       | 10-07-2024                  | 12-07-2024                        |    |
|    | **Midpoint Evaluation** |Midpoint evaluation - Milestone 1                                                              | 08-07-2024                  | 12-07-2024                        |    |
|--|---------|-------------|----------|----------|-------|
|    | **MILESTONE 2**           |                                                                                   |                             |                                   |        |
| ⬜  | Milestone 2.1             | Implement options for single target coverage analysis and report generation       | 20-07-2024                  | 23-07-2024                        | Additonal Notes  |
| ⬜  | Milestone 2.2 Task 1      | Introduce new CI workflow for code coverage                                      | 04-06-2024                  | 07-06-2024                        |        |
|    | **Internal Evaluation**   | Internal evaluation - Milestone 2                                                | 12-08-2024                  |                                   |        |
| ⬜  | Milestone 2.2 Task 2      | Upload report as comment                                                         | 10-08-2024                  | 14-08-2024                        |        |
|    | **Buffer Time**           | Buffer time for revision - Phase 2                                               | 15-08-2024                  | 23-08-2024                        |        |
| ⬜  | Milestone 2.3 Task 1      | Fix/replace cancellation workflow                                                 | 19-08-2024                  | 22-08-2024                        |        |
| ⬜  | Milestone 2.3 Task 2      | Add tests for Milestone 2                                                         | 22-08-2024                  | 24-08-2024                        |        |
|    | **Final Evaluation**      | Final evaluation - Milestone 2                                                    | 19-07-2024                  | 26-07-2024                        |        |
|--|---------|-------------|----------|----------|-------|
| ⬜  | Milestone 2.4       | Create wiki page explaining code coverage usage, limitations, and test writing tips    | 19-08-2024                  | 22-08-2024                        |        |
| ⬜  | Milestone 2.5       | File issues for missed coverage                                                         |                   |                        |        |


