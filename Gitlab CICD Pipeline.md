# DevSecOps-Pro
Notes for future / Exam

```bash
stages:   # Dictionary
 - build   # this is build stage
 - test    # this is test stage
 - integration # this is an integration stage
 - prod       # this is prod/production stage

build:       # this is job named build, it can be anything, job1, job2, etc.,
  stage: build    # this job belongs to the build stage. Here both job name and stage name is the same i.e., build
  script:
    - echo "This is a build step"  # We are running an echo command, but it can be any command.
    - echo "{\"vulnerability\":\"SQL Injection\"}" > output.json
  artifacts:      # notice a new tag artifacts
    paths: [output.json]   # this is the path to the output.json file

test:
  stage: test
  script:
    - echo "This is a test step."
    - exit 1         # Non zero exit code, fails a job.
  allow_failure: true   #<--- allow the build to fail but don't mark it as such

integration:        # integration job under stage integration.
  stage: integration
  script:
    - echo "This is an integration step."

prod:
  stage: prod
  script:
    - echo "This is a deploy step."
  when: manual   #<-- A human has to click a button (play button in Gitlab) for this task to
 ```
