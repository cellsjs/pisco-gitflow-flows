### Flow Validate

This is the main flow for Continuous Integration. 
It has defined several steps needed for almost every software
context (maven library, cells app, gradle library, J2EE web application, etc...).

It doesn't apply for version control contexts 
(only applies for software contexts) like `master`, `develop`, `feature`, `hotfix`, etc..

The steps of the flow are the following. 
The definition of the flow is in the [config.json][1] file.

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

Provide and install all dependencies and requirements.

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

    * `provide-env`: Provide the environment needed for the validate process.
    * `configure-env`: Here we configure all the tools needed in the environment.
    * `check-install`: Checking that all the requirements over the system have been fulfilled.
    
    As defined, those are not steps required in order to execute correctly the flow.

#### Flow build

In this section we will build the software unit.
We will resolve all the software **dependencies** of the 
software and we will **compile** the code and detect all the 
compilation-time errors.

* Steps:
    ```json
    {
        "resolve-deps": {},
        "build": {}
    }
    ```
    
    * `resolve-deps`: Resolve all the dependencies in compilation time defined. Check for the bower.json dependencies, or the maven dependecies, or the package.json dependencies.
    * `build`: Execute the build process with the tool configured for the software unit.

#### Flow check

In this step, the flow validate will check all the qualities of the software unit than can be measured without any deploy of the software unit.
For example we can measure the bugs in the code, run the unit tests and check for the coverage, ...

* Steps:
    ```json
    {    
      "unit-testing": {
        "implementation-check" : false
      },
      "static-analysis": {
        "type" : "flow"
      },
      "structural-testing": {
        "type" : "flow"
      }
    }


#### Flow package

The validate flow will generate the **artifact** software for this software unit. Usually it involves compress the result of the build process, but it depends on the **build tool** that we have used for our software unit.

* Steps:
    ```json
    {
      "package": {}
    }
    ```
    

#### Flow publish

The validate flow will publish (as configured) the artifacts generated in the previous package step.

* Steps:
    ```json
    {
      "publish": {}
    }
    ```


#### Flow deploy

Once the software has been packaged and published in the correspondent platform, we have to deploy it in order to be able to test this particular artifact in his environment.

The particular environment will be calculated in function of several parameters:

* `branch type`: develop, master, feature, hotfix, etc...
* `configuration`: the configuration of the deploy itself.
* `stage in the CI process`: development, preproduction, UAT, production, ...

#### Flow test

In this step of the flow we hace to test the behaviour of the software unit once it has been deployed in the specific environment.

We have several types of test in this stage, and we have defined it as steps of this flow:

* Steps:
    ```json
    {
        "smoke-testing": {
          "implementation-check" : false
        },
        "functional-testing": {
          "implementation-check" : false
        },
        "performance-testing": {
          "implementation-check" : false
        },
        "security-testing": {
          "implementation-check" : false
        },
        "usability-testing": {
          "implementation-check" : false
        },
        "acceptance-tests": {
          "type" : "flow"
        }
    }



[1]: ./config.json
