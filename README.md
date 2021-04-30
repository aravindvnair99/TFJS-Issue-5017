# TFJS-Issue-5017
MCVE for https://github.com/tensorflow/tfjs/issues/5017

## Steps to reproduce (Node.js v14.16.0 with npm v7.11.2):

```console
$ git clone https://github.com/aravindvnair99/TFJS-Issue-5017
$ cd TFJS-Issue-5017/
$ npm i
$ node index.js
node-pre-gyp info This Node instance does not support builds for N-API version 8
node-pre-gyp info This Node instance does not support builds for N-API version 8
2021-05-01 02:54:39.108908: I tensorflow/core/platform/cpu_feature_guard.cc:142] This TensorFlow binary is optimized wit
h oneAPI Deep Neural Network Library (oneDNN) to use the following CPU instructions in performance-critical operations:
 AVX2
To enable them in other operations, rebuild TensorFlow with the appropriate compiler flags.
D:\TFJS-Issue-5017\node_modules\@tensorflow\tfjs-automl\dist\index.js:18
export { ImageClassificationModel, loadImageClassification } from './img_classification';
^^^^^^

SyntaxError: Unexpected token 'export'
    at wrapSafe (internal/modules/cjs/loader.js:979:16)
    at Module._compile (internal/modules/cjs/loader.js:1027:27)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:1092:10)
    at Module.load (internal/modules/cjs/loader.js:928:32)
    at Function.Module._load (internal/modules/cjs/loader.js:769:14)
    at Module.require (internal/modules/cjs/loader.js:952:19)
    at require (internal/modules/cjs/helpers.js:88:18)
    at Object.<anonymous> (D:\TFJS-Issue-5017\index.js:2:11)
    at Module._compile (internal/modules/cjs/loader.js:1063:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:1092:10)
```

## Steps to reproduce (Node.js v14.16.1 with npm v6.14.12):

```console
$ git clone https://github.com/aravindvnair99/TFJS-Issue-5017
$ cd TFJS-Issue-5017/
$ npm i
npm WARN read-shrinkwrap This version of npm is compatible with lockfileVersion@1, but package-lock.json was generated for lockfileVersion@2. I'll try to do my best with it!

> @tensorflow/tfjs-node@3.6.1 install D:\TFJS-Issue-5017\node_modules\@tensorflow\tfjs-node
> node scripts/install.js

CPU-windows-3.6.1.zip
* Downloading libtensorflow
[==============================] 12485785/bps 100% 0.0s
* Building TensorFlow Node.js bindings

> core-js@3.11.1 postinstall D:\TFJS-Issue-5017\node_modules\core-js
> node -e "try{require('./postinstall')}catch(e){}"

Thank you for using core-js ( https://github.com/zloirock/core-js ) for polyfilling JavaScript standard library!

The project needs your help! Please consider supporting of core-js on Open Collective or Patreon:
> https://opencollective.com/core-js
> https://www.patreon.com/zloirock

Also, the author of core-js ( https://github.com/zloirock ) is looking for a good job -)

added 129 packages from 109 contributors and audited 129 packages in 122.815s

5 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
$ node index.js
node-pre-gyp info This Node instance does not support builds for N-API version 8
node-pre-gyp info This Node instance does not support builds for N-API version 8
2021-05-01 03:17:40.305468: I tensorflow/core/platform/cpu_feature_guard.cc:142] This TensorFlow binary is optimized wit
h oneAPI Deep Neural Network Library (oneDNN) to use the following CPU instructions in performance-critical operations:
 AVX2
To enable them in other operations, rebuild TensorFlow with the appropriate compiler flags.
D:\TFJS-Issue-5017\node_modules\@tensorflow\tfjs-automl\dist\index.js:18
export { ImageClassificationModel, loadImageClassification } from './img_classification';
^^^^^^

SyntaxError: Unexpected token 'export'
    at wrapSafe (internal/modules/cjs/loader.js:979:16)
    at Module._compile (internal/modules/cjs/loader.js:1027:27)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:1092:10)
    at Module.load (internal/modules/cjs/loader.js:928:32)
    at Function.Module._load (internal/modules/cjs/loader.js:769:14)
    at Module.require (internal/modules/cjs/loader.js:952:19)
    at require (internal/modules/cjs/helpers.js:88:18)
    at Object.<anonymous> (D:\TFJS-Issue-5017\index.js:2:11)
    at Module._compile (internal/modules/cjs/loader.js:1063:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:1092:10)
$ rm -rf node_modules/ package-lock.json
$ npm i
npm WARN deprecated node-pre-gyp@0.14.0: Please upgrade to @mapbox/node-pre-gyp: the non-scoped node-pre-gyp package is deprecated and only the @mapbox scoped package will recieve updates in the future

> @tensorflow/tfjs-node@3.6.1 install D:\TFJS-Issue-5017\node_modules\@tensorflow\tfjs-node
> node scripts/install.js

CPU-windows-3.6.1.zip
* Downloading libtensorflow
[==============================] 13627475/bps 100% 0.0s
* Building TensorFlow Node.js bindings

> core-js@3.11.1 postinstall D:\TFJS-Issue-5017\node_modules\core-js
> node -e "try{require('./postinstall')}catch(e){}"

Thank you for using core-js ( https://github.com/zloirock/core-js ) for polyfilling JavaScript standard library!

The project needs your help! Please consider supporting of core-js on Open Collective or Patreon:
> https://opencollective.com/core-js
> https://www.patreon.com/zloirock

Also, the author of core-js ( https://github.com/zloirock ) is looking for a good job -)

npm notice created a lockfile as package-lock.json. You should commit this file.
npm WARN @tensorflow/tfjs-automl@1.1.0 requires a peer of @tensorflow/tfjs-converter@~3.3.0 but none is installed. You must install peer dependencies yourself.
npm WARN @tensorflow/tfjs-automl@1.1.0 requires a peer of @tensorflow/tfjs-core@~3.3.0 but none is installed. You must install peer dependencies yourself.
npm WARN @tensorflow/tfjs-automl@1.1.0 requires a peer of @tensorflow/tfjs-backend-webgl@3.3.0 but none is installed. You must install peer dependencies yourself.

added 123 packages from 109 contributors and audited 123 packages in 98.274s

5 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
$ node index.js
node-pre-gyp info This Node instance does not support builds for N-API version 8
node-pre-gyp info This Node instance does not support builds for N-API version 8
2021-05-01 03:22:16.203809: I tensorflow/core/platform/cpu_feature_guard.cc:142] This TensorFlow binary is optimized wit
h oneAPI Deep Neural Network Library (oneDNN) to use the following CPU instructions in performance-critical operations:
 AVX2
To enable them in other operations, rebuild TensorFlow with the appropriate compiler flags.
D:\TFJS-Issue-5017\node_modules\@tensorflow\tfjs-automl\dist\index.js:18
export { ImageClassificationModel, loadImageClassification } from './img_classification';
^^^^^^

SyntaxError: Unexpected token 'export'
    at wrapSafe (internal/modules/cjs/loader.js:979:16)
    at Module._compile (internal/modules/cjs/loader.js:1027:27)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:1092:10)
    at Module.load (internal/modules/cjs/loader.js:928:32)
    at Function.Module._load (internal/modules/cjs/loader.js:769:14)
    at Module.require (internal/modules/cjs/loader.js:952:19)
    at require (internal/modules/cjs/helpers.js:88:18)
    at Object.<anonymous> (D:\TFJS-Issue-5017\index.js:2:11)
    at Module._compile (internal/modules/cjs/loader.js:1063:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:1092:10)
$ npm i @tensorflow/tfjs-converter@~3.3.0 @tensorflow/tfjs-core@~3.3.0 @tensorflow/tfjs-backend-webgl@3.3.0
npm WARN @tensorflow/tfjs-backend-cpu@3.6.0 requires a peer of @tensorflow/tfjs-core@3.6.0 but none is installed. You must install peer dependencies yourself.
npm WARN @tensorflow/tfjs-data@3.6.0 requires a peer of @tensorflow/tfjs-core@3.6.0 but none is installed. You must install peer dependencies yourself.
npm WARN @tensorflow/tfjs-layers@3.6.0 requires a peer of @tensorflow/tfjs-core@3.6.0 but none is installed. You must install peer dependencies yourself.

+ @tensorflow/tfjs-core@3.3.0
+ @tensorflow/tfjs-backend-webgl@3.3.0
+ @tensorflow/tfjs-converter@3.3.0
added 4 packages, updated 3 packages and audited 127 packages in 63.434s

5 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
$ node index.js
Platform node has already been set. Overwriting the platform with [object Object].
The kernel 'undefined' for backend 'cpu' is already registered
The kernel 'undefined' for backend 'cpu' is already registered
node-pre-gyp info This Node instance does not support builds for N-API version 8
node-pre-gyp info This Node instance does not support builds for N-API version 8
2021-05-01 03:24:26.947528: I tensorflow/core/platform/cpu_feature_guard.cc:142] This TensorFlow binary is optimized wit
h oneAPI Deep Neural Network Library (oneDNN) to use the following CPU instructions in performance-critical operations:
 AVX2
To enable them in other operations, rebuild TensorFlow with the appropriate compiler flags.
D:\TFJS-Issue-5017\node_modules\@tensorflow\tfjs-automl\dist\index.js:18
export { ImageClassificationModel, loadImageClassification } from './img_classification';
^^^^^^

SyntaxError: Unexpected token 'export'
    at wrapSafe (internal/modules/cjs/loader.js:979:16)
    at Module._compile (internal/modules/cjs/loader.js:1027:27)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:1092:10)
    at Module.load (internal/modules/cjs/loader.js:928:32)
    at Function.Module._load (internal/modules/cjs/loader.js:769:14)
    at Module.require (internal/modules/cjs/loader.js:952:19)
    at require (internal/modules/cjs/helpers.js:88:18)
    at Object.<anonymous> (D:\TFJS-Issue-5017\index.js:2:11)
    at Module._compile (internal/modules/cjs/loader.js:1063:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:1092:10)
```
