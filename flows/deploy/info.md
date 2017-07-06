# Flow deploy

1. [Description](#description)
1. [Steps](#steps)
1. [Excluded Contexts](#excluded-contexts)

## <a name="description"></a>Description

Deploy the artifact. The particular environment (in which the artifact will be deployed) will be calculated in function of several parameters:
                     
* `branch type`: develop, master, feature, hotfix, etc...
* `configuration`: the configuration of the deploy itself.
* `stage in the CI process`: development, preproduction, UAT, production, ...

## <a name="steps"></a>Steps

```json
{
  "deploy": {
    "implementation-check" : false
  }
}
```

* `deploy`: All commands needed to deploy the artifact to an environment provided or configured in order to run the artifact there.

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
