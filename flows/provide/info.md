# Flow provide

## Description

Provide and install all dependencies and requirements.

## Excluded contexts

All the gitflow contexts are excluded:

* develop
* master
* feature
* hotfix
* release
* merger
* consolidation

## Steps

These are the steps configured in the [config.json][1] file:

    ```json
      {
        "provide-env": {
          "implementation-check" : false
        },
        "configure-env": {
          "implementation-check" : false
        },
        "check-install": {
          "implementation-check" : false
        }
      }
    ```

* `provide-env`: Provide the environment needed for the validate process.
* `configure-env`: Here we configure all the tools needed in the environment.
* `check-install`: Checking that all the requirements over the system have been fulfilled.
    
As defined, those are not steps required in order to execute correctly the flow.

[1]: ./config.json