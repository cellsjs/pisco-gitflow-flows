# Flow test

1. [Description](#description)
1. [Steps](#steps)
1. [Excluded Contexts](#excluded-contexts)

## <a name="description"></a>Description

Integrated validate: Needs deploy. Once the artifat is deployed we will test in the deployed environment its public API.
We have defined several type of testing in this deployed environment:

* `smoke-testing`
* `functional-testing`
* `performance-testing`
* `security-testing`
* `usability-testing`
* `acceptance-tests`

## <a name="steps"></a>Steps

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

* `smoke-testing`: Run all smoke tests present in the source code of the contexts. This tests must be properly tagged.
* `functional-testing`: Run all functional tests present in the source code of the contexts. This tests must be properly tagged.
* `performance-testing`: Run all performance tests present in the source code of the contexts. This tests must be properly tagged.
* `security-testing`:  Run all security tests present in the source code of the contexts. This tests must be properly tagged.
* `usability-testing`: Run all usability tests present in the source code of the contexts. This tests must be properly tagged.
* `acceptance-testing`: Run all acceptance tests present in the source code of the contexts. This tests must be properly tagged

## <a name="excluded-contexts"></a>Excluded contexts

All the gitflow contexts are excluded:

* [develop][1]
* [master][2]
* [feature][3]
* [hotfix][4]
* [release][5]
* [merger][6]
* [consolidation][7]


[1]: https://github.com/cellsjs/pisco-gitflow-contexts/blob/master/contexts/develop/index.js
[2]: https://github.com/cellsjs/pisco-gitflow-contexts/blob/master/contexts/master/index.js
[3]: https://github.com/cellsjs/pisco-gitflow-contexts/blob/master/contexts/feature/index.js
[4]: https://github.com/cellsjs/pisco-gitflow-contexts/blob/master/contexts/hotfix/index.js
[5]: https://github.com/cellsjs/pisco-gitflow-contexts/blob/master/contexts/release/index.js
[6]: https://github.com/cellsjs/pisco-gitflow-contexts/blob/master/contexts/merger/index.js
[7]: https://github.com/cellsjs/pisco-gitflow-contexts/blob/master/contexts/consolidation/index.js
