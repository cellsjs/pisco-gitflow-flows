# Flow check

1. [Description](#description)
1. [Steps](#steps)
1. [Excluded Contexts](#excluded-contexts)

## <a name="description"></a>Description

Static Check: Do not need deploy

In this step, the flow validate will check all the qualities of the software unit than can be measured without any deploy of the software unit.
For example we can measure the bugs in the code, run the unit tests and check for the coverage, ...

## <a name="steps"></a>Steps


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
```

* `unit-testing`: Run all unit tests present in the source code of the contexts. Those that don’t need to be deployed.
* `static-analysis`: execute and static analysis of the code. It can relay in external tools liken [Sonarqube][8], [eslint][9], etc...
* `structural-testing`: checks that the code satisfies certain structural restrictions. For example, we can need a pom.xml in the root directory, or a package.json, etc...

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
[8]: https://www.sonarqube.org/
[9]: http://eslint.org/

