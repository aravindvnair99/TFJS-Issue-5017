# TFJS-Issue-5017
MCVE for https://github.com/tensorflow/tfjs/issues/5017

## Environment information:

Node.js: v14.16.0
npm: 7.11.2

## Steps to reproduce:

```console
$ git clone https://github.com/aravindvnair99/TFJS-Issue-5017
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
