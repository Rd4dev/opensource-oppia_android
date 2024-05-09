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

