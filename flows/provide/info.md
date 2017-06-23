# Flow provide

## Description

Provide and install all dependencies and requirements.

## Excluded contexts

All the gitflow contexts are excluded:

* [develop][1]
* [master][2]
* [feature][3]
* [hotfix][4]
* [release][5]
* [merger][6]
* [consolidation][7]

## Steps

These are the steps configured in the [config.json][8] file:

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

[1]: https://github.com/cellsjs/pisco-gitflow-contexts/blob/master/contexts/develop/index.js
[2]: https://github.com/cellsjs/pisco-gitflow-contexts/blob/master/contexts/master/index.js
[3]: https://github.com/cellsjs/pisco-gitflow-contexts/blob/master/contexts/feature/index.js
[4]: https://github.com/cellsjs/pisco-gitflow-contexts/blob/master/contexts/hotfix/index.js
[5]: https://github.com/cellsjs/pisco-gitflow-contexts/blob/master/contexts/release/index.js
[6]: https://github.com/cellsjs/pisco-gitflow-contexts/blob/master/contexts/merger/index.js
[7]: https://github.com/cellsjs/pisco-gitflow-contexts/blob/master/contexts/consolidation/index.js
[8]: ./config.json