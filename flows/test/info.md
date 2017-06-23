# Flow test

## Description

Integrated validate: Needs deploy. Once the artifat is deployed we will test in the deployed environment its public API.
We have defined several type of testing in this deployed environment:

* `smoke-testing`
* `functional-testing`
* `performance-testing`
* `security-testing`
* `usability-testing`
* `acceptance-tests`

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
```

[1]: https://github.com/cellsjs/pisco-gitflow-contexts/blob/master/contexts/develop/index.js
[2]: https://github.com/cellsjs/pisco-gitflow-contexts/blob/master/contexts/master/index.js
[3]: https://github.com/cellsjs/pisco-gitflow-contexts/blob/master/contexts/feature/index.js
[4]: https://github.com/cellsjs/pisco-gitflow-contexts/blob/master/contexts/hotfix/index.js
[5]: https://github.com/cellsjs/pisco-gitflow-contexts/blob/master/contexts/release/index.js
[6]: https://github.com/cellsjs/pisco-gitflow-contexts/blob/master/contexts/merger/index.js
[7]: https://github.com/cellsjs/pisco-gitflow-contexts/blob/master/contexts/consolidation/index.js