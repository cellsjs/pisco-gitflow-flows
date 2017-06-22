### Flow Validate

This is the main flow for Continuous Integration. It has defined several steps needed for almost every software context.
It doesn't apply for version control contexts like `master`, `develop`, `feature`, `hotfix`, etc... 

The steps of the flow are the following. The definition of the flow is in the [config.json][1] file.

```json
  {
    "provide": {
      "type": "flow"
    },
    "build": {
      "type": "flow"
    },
    "check": {
      "type": "flow"
    }, 
    "package": {
      "type": "flow"
    },
    "publish": {
      "type": "flow"
    },
    "deploy": {
      "type": "flow"
    },
    "test": {
      "type": "flow"
    }
  }
```

#### Flow provide

Provide and install all dependencies and requirements. This flow doesn't apply for the version control contexts (master, develop, feature, ...).

* Steps
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

#### Flow build



#### Flow check



#### Flow package



#### Flow publish



#### Flow deploy



#### Flow test




[1]: ./config.json
