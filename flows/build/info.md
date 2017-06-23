# Flow build

## Description

In this section we will build the software unit.
We will resolve all the software **dependencies** of the 
software and we will **compile** the code and detect all the 
compilation-time errors.

## Excluded contexts

All the gitflow contexts are excluded:

* [develop][1]
* [master][2]
* [feature][3]
* [hotfix][4]
* [release][5]
* [merger][6]
* [consolidation][7]

## Steps:


```json
{
  "resolve-deps": {},
  "build": {}
}
```
    
* `resolve-deps`: Resolve all the dependencies in compilation time defined. Check for the bower.json dependencies, or the maven dependecies, or the package.json dependencies.
* `build`: Execute the build process with the tool configured for the software unit.


[1]: https://github.com/cellsjs/pisco-gitflow-contexts/blob/master/contexts/develop/index.js
[2]: https://github.com/cellsjs/pisco-gitflow-contexts/blob/master/contexts/master/index.js
[3]: https://github.com/cellsjs/pisco-gitflow-contexts/blob/master/contexts/feature/index.js
[4]: https://github.com/cellsjs/pisco-gitflow-contexts/blob/master/contexts/hotfix/index.js
[5]: https://github.com/cellsjs/pisco-gitflow-contexts/blob/master/contexts/release/index.js
[6]: https://github.com/cellsjs/pisco-gitflow-contexts/blob/master/contexts/merger/index.js
[7]: https://github.com/cellsjs/pisco-gitflow-contexts/blob/master/contexts/consolidation/index.js