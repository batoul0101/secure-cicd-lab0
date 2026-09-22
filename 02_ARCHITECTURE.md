# Secure CI/CD Architecture

## Architecture Diagram

```text
                 DEVELOPER
                     |
                     v
                LOCAL GIT
                     |
                     v
              GITHUB REPOSITORY
                     |
                     v
              GITHUB ACTIONS
                     |
        +------------+------------+
        |            |            |
        v            v            v
   Application   Dependency    Secret
      Test          Scan       Detection
        |            |            |
        +------------+------------+
                     |
                     v
                 CODEQL
                   SAST
                     |
                     v
                DOCKER BUILD
                     |
                     v
              CONTAINER SCAN
                     |
                     v
              SECURITY RESULT
