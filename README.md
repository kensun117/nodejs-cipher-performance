# nodejs-cipher-performance

Benchmarks for nodejs `crypto.getCiphers()` or just a wrapper for cipher function

## Installation

Install through NPM

```bash
npm install nodejs-cipher-performance
```
or
```bash
git clone git://github.com/hex7c0/nodejs-cipher-performance.git
```

## API

inside nodejs project
```js
var cipher = require('nodejs-cipher-performance');

cipher('foo', 'aes128', 'ciao', 'base64');
```

### nodejs-cipher-performance(raw,cipher,password,encoding)

#### options

 - `raw` - **String | Buffer** Your Data *(default "required")*
 - `cipher`- **String** Type of Hash *(default "required")*
 - `password` - **String | Buffer** Your Password *(default "required")*
 - `encoding`- **String** Type of Encoding *(default "required")*

### [License GPLv3](LICENSE)

## Benchmark

Look at
[![Linux](https://img.shields.io/travis/hex7c0/nodejs-cipher-performance.svg?label=linux)](https://travis-ci.org/hex7c0/nodejs-cipher-performance)
and
[![Windows](https://img.shields.io/appveyor/ci/hex7c0/nodejs-cipher-performance.svg?label=windows)](https://ci.appveyor.com/project/hex7c0/nodejs-cipher-performance)
for latest run


```bash
$ npm run-script test

> node benchmark/index.js

> node benchmark/body-100.js
  100 body

   buffer-base64-CAST-cbc              x 31,656 ops/sec ±4.41% (122 runs sampled)
   buffer-base64-aes-128-cbc           x 27,695 ops/sec ±4.67% (115 runs sampled)
   buffer-base64-aes-128-cbc-hmac-sha1 x 25,892 ops/sec ±5.39% (111 runs sampled)
   buffer-base64-aes-128-cfb           x 36,025 ops/sec ±4.72% (127 runs sampled)
   buffer-base64-aes-128-cfb1          x 10,879 ops/sec ±1.98% (141 runs sampled)
   buffer-base64-aes-128-cfb8          x 27,727 ops/sec ±4.20% (122 runs sampled)
   buffer-base64-aes-128-ctr           x 38,321 ops/sec ±4.15% (126 runs sampled)
   buffer-base64-aes-128-ecb           x 36,750 ops/sec ±4.54% (127 runs sampled)
   buffer-base64-aes-128-gcm           x 35,114 ops/sec ±4.38% (124 runs sampled)
   buffer-base64-aes-128-ofb           x 37,928 ops/sec ±3.74% (126 runs sampled)
   buffer-base64-aes-128-xts           x 39,193 ops/sec ±4.10% (130 runs sampled)
   buffer-base64-aes-192-cbc           x 38,308 ops/sec ±4.17% (118 runs sampled)
   buffer-base64-aes-192-cfb           x 33,754 ops/sec ±4.42% (124 runs sampled)
   buffer-base64-aes-192-cfb1          x  9,477 ops/sec ±2.84% (128 runs sampled)
   buffer-base64-aes-192-cfb8          x 31,243 ops/sec ±3.77% (133 runs sampled)
   buffer-base64-aes-192-ctr           x 35,400 ops/sec ±4.47% (121 runs sampled)
   buffer-base64-aes-192-ecb           x 33,900 ops/sec ±4.46% (123 runs sampled)
   buffer-base64-aes-192-gcm           x 36,673 ops/sec ±4.11% (129 runs sampled)
   buffer-base64-aes-192-ofb           x 38,558 ops/sec ±3.58% (131 runs sampled)
   buffer-base64-aes-256-cbc           x 34,177 ops/sec ±4.61% (124 runs sampled)
   buffer-base64-aes-256-cbc-hmac-sha1 x 32,281 ops/sec ±4.73% (126 runs sampled)
   buffer-base64-aes-256-cfb           x 39,603 ops/sec ±3.70% (131 runs sampled)
   buffer-base64-aes-256-cfb1          x  8,861 ops/sec ±2.23% (132 runs sampled)
   buffer-base64-aes-256-cfb8          x 27,121 ops/sec ±3.94% (127 runs sampled)
   buffer-base64-aes-256-ctr           x 36,730 ops/sec ±4.09% (129 runs sampled)
   buffer-base64-aes-256-ecb           x 37,818 ops/sec ±3.82% (131 runs sampled)
   buffer-base64-aes-256-gcm           x 32,272 ops/sec ±4.97% (121 runs sampled)
   buffer-base64-aes-256-ofb           x 36,415 ops/sec ±4.24% (129 runs sampled)
   buffer-base64-aes-256-xts           x 37,503 ops/sec ±4.06% (130 runs sampled)
   buffer-base64-aes128                x 35,227 ops/sec ±4.54% (126 runs sampled)
   buffer-base64-aes192                x 36,023 ops/sec ±3.69% (130 runs sampled)
   buffer-base64-aes256                x 35,326 ops/sec ±3.95% (128 runs sampled)
   buffer-base64-bf                    x 11,884 ops/sec ±2.08% (143 runs sampled)
   buffer-base64-bf-cbc                x 11,866 ops/sec ±1.99% (143 runs sampled)
   buffer-base64-bf-cfb                x 11,506 ops/sec ±2.24% (141 runs sampled)
   buffer-base64-bf-ecb                x 11,151 ops/sec ±2.58% (137 runs sampled)
   buffer-base64-bf-ofb                x 11,893 ops/sec ±2.35% (141 runs sampled)
   buffer-base64-blowfish              x 11,733 ops/sec ±2.08% (143 runs sampled)
   buffer-base64-camellia-128-cbc      x 35,415 ops/sec ±3.89% (136 runs sampled)
   buffer-base64-camellia-128-cfb      x 37,982 ops/sec ±3.58% (137 runs sampled)
   buffer-base64-camellia-128-cfb1     x  5,618 ops/sec ±1.35% (144 runs sampled)
   buffer-base64-camellia-128-cfb8     x 21,824 ops/sec ±3.50% (128 runs sampled)
   buffer-base64-camellia-128-ecb      x 34,468 ops/sec ±5.04% (133 runs sampled)
   buffer-base64-camellia-128-ofb      x 36,251 ops/sec ±3.63% (126 runs sampled)
   buffer-base64-camellia-192-cbc      x 35,605 ops/sec ±3.64% (135 runs sampled)
   buffer-base64-camellia-192-cfb      x 35,770 ops/sec ±4.49% (125 runs sampled)
   buffer-base64-camellia-192-cfb1     x  4,653 ops/sec ±1.59% (140 runs sampled)
   buffer-base64-camellia-192-cfb8     x 20,450 ops/sec ±3.47% (135 runs sampled)
   buffer-base64-camellia-192-ecb      x 32,765 ops/sec ±4.35% (128 runs sampled)
   buffer-base64-camellia-192-ofb      x 32,151 ops/sec ±4.88% (123 runs sampled)
   buffer-base64-camellia-256-cbc      x 34,772 ops/sec ±3.77% (135 runs sampled)
   buffer-base64-camellia-256-cfb      x 36,238 ops/sec ±4.07% (132 runs sampled)
   buffer-base64-camellia-256-cfb1     x  4,412 ops/sec ±2.00% (134 runs sampled)
   buffer-base64-camellia-256-cfb8     x 20,809 ops/sec ±3.08% (130 runs sampled)
   buffer-base64-camellia-256-ecb      x 35,285 ops/sec ±3.74% (132 runs sampled)
   buffer-base64-camellia-256-ofb      x 35,609 ops/sec ±3.85% (133 runs sampled)
   buffer-base64-camellia128           x 34,226 ops/sec ±4.04% (130 runs sampled)
   buffer-base64-camellia192           x 35,120 ops/sec ±3.48% (134 runs sampled)
   buffer-base64-camellia256           x 36,341 ops/sec ±3.43% (138 runs sampled)
   buffer-base64-cast                  x 35,407 ops/sec ±3.80% (134 runs sampled)
   buffer-base64-cast-cbc              x 35,438 ops/sec ±3.60% (133 runs sampled)
   buffer-base64-cast5-cbc             x 35,637 ops/sec ±3.46% (134 runs sampled)
   buffer-base64-cast5-cfb             x 34,128 ops/sec ±3.92% (131 runs sampled)
   buffer-base64-cast5-ecb             x 32,005 ops/sec ±4.21% (125 runs sampled)
   buffer-base64-cast5-ofb             x 33,989 ops/sec ±4.17% (130 runs sampled)
   buffer-base64-des                   x 34,203 ops/sec ±3.71% (133 runs sampled)
   buffer-base64-des-cbc               x 34,954 ops/sec ±3.61% (135 runs sampled)
   buffer-base64-des-cfb               x 33,045 ops/sec ±4.42% (125 runs sampled)
   buffer-base64-des-cfb1              x  4,789 ops/sec ±1.51% (140 runs sampled)
   buffer-base64-des-cfb8              x 21,219 ops/sec ±3.33% (141 runs sampled)
   buffer-base64-des-ecb               x 34,543 ops/sec ±3.57% (135 runs sampled)
   buffer-base64-des-ede               x 28,646 ops/sec ±3.78% (132 runs sampled)
   buffer-base64-des-ede-cbc           x 29,158 ops/sec ±3.23% (135 runs sampled)
   buffer-base64-des-ede-cfb           x 28,894 ops/sec ±4.02% (134 runs sampled)
   buffer-base64-des-ede-ofb           x 30,642 ops/sec ±3.52% (133 runs sampled)
   buffer-base64-des-ede3              x 29,730 ops/sec ±3.59% (131 runs sampled)
   buffer-base64-des-ede3-cbc          x 29,441 ops/sec ±3.34% (131 runs sampled)
   buffer-base64-des-ede3-cfb          x 29,998 ops/sec ±3.52% (133 runs sampled)
   buffer-base64-des-ede3-cfb1         x 12,339 ops/sec ±2.65% (136 runs sampled)
   buffer-base64-des-ede3-cfb8         x 12,902 ops/sec ±2.21% (142 runs sampled)
   buffer-base64-des-ede3-ofb          x 29,803 ops/sec ±3.57% (134 runs sampled)
   buffer-base64-des-ofb               x 36,049 ops/sec ±3.95% (131 runs sampled)
   buffer-base64-des3                  x 29,008 ops/sec ±3.76% (136 runs sampled)
   buffer-base64-desx                  x 32,590 ops/sec ±3.90% (133 runs sampled)
   buffer-base64-desx-cbc              x 33,261 ops/sec ±3.67% (133 runs sampled)
   buffer-base64-id-aes128-GCM         x 35,488 ops/sec ±4.10% (127 runs sampled)
   buffer-base64-id-aes192-GCM         x 35,510 ops/sec ±4.06% (128 runs sampled)
   buffer-base64-id-aes256-GCM         x 37,388 ops/sec ±3.61% (136 runs sampled)
   buffer-base64-idea                  x 35,463 ops/sec ±3.42% (135 runs sampled)
   buffer-base64-idea-cbc              x 33,311 ops/sec ±4.33% (128 runs sampled)
   buffer-base64-idea-cfb              x 36,795 ops/sec ±3.62% (134 runs sampled)
   buffer-base64-idea-ecb              x 36,053 ops/sec ±3.76% (133 runs sampled)
   buffer-base64-idea-ofb              x 34,452 ops/sec ±3.79% (128 runs sampled)
   buffer-base64-rc2                   x 30,078 ops/sec ±4.09% (129 runs sampled)
   buffer-base64-rc2-40-cbc            x 29,425 ops/sec ±3.69% (128 runs sampled)
   buffer-base64-rc2-64-cbc            x 29,908 ops/sec ±3.84% (129 runs sampled)
   buffer-base64-rc2-cbc               x 30,959 ops/sec ±3.69% (132 runs sampled)
   buffer-base64-rc2-cfb               x 31,170 ops/sec ±3.81% (128 runs sampled)
   buffer-base64-rc2-ecb               x 31,125 ops/sec ±4.02% (130 runs sampled)
   buffer-base64-rc2-ofb               x 28,366 ops/sec ±5.24% (115 runs sampled)
   buffer-base64-rc4                   x 30,790 ops/sec ±5.25% (112 runs sampled)
   buffer-base64-rc4-40                x 31,383 ops/sec ±6.26% (121 runs sampled)
   buffer-base64-rc4-hmac-md5          x 39,767 ops/sec ±3.23% (135 runs sampled)
   buffer-base64-seed                  x 35,134 ops/sec ±3.18% (133 runs sampled)
   buffer-base64-seed-cbc              x 29,094 ops/sec ±4.48% (124 runs sampled)
   buffer-base64-seed-cfb              x 32,984 ops/sec ±4.22% (126 runs sampled)
   buffer-base64-seed-ecb              x 33,803 ops/sec ±3.71% (133 runs sampled)
   buffer-base64-seed-ofb              x 33,591 ops/sec ±4.12% (124 runs sampled)
Fastest is: buffer-base64-rc4-hmac-md5, buffer-base64-aes-192-ofb, buffer-base64-aes-128-ctr, buffer-base64-aes-128-ofb

> node benchmark/body-1000.js
  1000 body

   buffer-base64-CAST-cbc              x 19,685 ops/sec ±2.29% (130 runs sampled)
   buffer-base64-aes-128-cbc           x 28,793 ops/sec ±2.90% (131 runs sampled)
   buffer-base64-aes-128-cbc-hmac-sha1 x 28,255 ops/sec ±2.45% (133 runs sampled)
   buffer-base64-aes-128-cfb           x 30,009 ops/sec ±2.59% (133 runs sampled)
   buffer-base64-aes-128-cfb1          x  1,407 ops/sec ±1.06% (138 runs sampled)
   buffer-base64-aes-128-cfb8          x 11,500 ops/sec ±1.67% (140 runs sampled)
   buffer-base64-aes-128-ctr           x 33,966 ops/sec ±2.64% (132 runs sampled)
   buffer-base64-aes-128-ecb           x 32,175 ops/sec ±2.70% (132 runs sampled)
   buffer-base64-aes-128-gcm           x 32,838 ops/sec ±2.38% (133 runs sampled)
   buffer-base64-aes-128-ofb           x 29,872 ops/sec ±2.52% (132 runs sampled)
   buffer-base64-aes-128-xts           x 31,620 ops/sec ±2.87% (131 runs sampled)
   buffer-base64-aes-192-cbc           x 29,875 ops/sec ±2.23% (131 runs sampled)
   buffer-base64-aes-192-cfb           x 29,533 ops/sec ±2.72% (128 runs sampled)
   buffer-base64-aes-192-cfb1          x  1,223 ops/sec ±1.27% (133 runs sampled)
   buffer-base64-aes-192-cfb8          x 10,197 ops/sec ±1.81% (140 runs sampled)
   buffer-base64-aes-192-ctr           x 32,674 ops/sec ±2.69% (134 runs sampled)
   buffer-base64-aes-192-ecb           x 29,578 ops/sec ±3.09% (126 runs sampled)
   buffer-base64-aes-192-gcm           x 30,366 ops/sec ±3.05% (128 runs sampled)
   buffer-base64-aes-192-ofb           x 30,549 ops/sec ±2.73% (135 runs sampled)
   buffer-base64-aes-256-cbc           x 26,173 ops/sec ±2.49% (136 runs sampled)
   buffer-base64-aes-256-cbc-hmac-sha1 x 25,116 ops/sec ±2.96% (130 runs sampled)
   buffer-base64-aes-256-cfb           x 26,501 ops/sec ±2.79% (128 runs sampled)
   buffer-base64-aes-256-cfb1          x  1,118 ops/sec ±1.50% (134 runs sampled)
   buffer-base64-aes-256-cfb8          x  8,813 ops/sec ±1.96% (132 runs sampled)
   buffer-base64-aes-256-ctr           x 27,771 ops/sec ±3.54% (129 runs sampled)
   buffer-base64-aes-256-ecb           x 28,240 ops/sec ±3.35% (128 runs sampled)
   buffer-base64-aes-256-gcm           x 28,914 ops/sec ±2.97% (132 runs sampled)
   buffer-base64-aes-256-ofb           x 27,210 ops/sec ±3.25% (131 runs sampled)
   buffer-base64-aes-256-xts           x 29,367 ops/sec ±3.16% (128 runs sampled)
   buffer-base64-aes128                x 26,730 ops/sec ±2.95% (129 runs sampled)
   buffer-base64-aes192                x 27,577 ops/sec ±2.79% (133 runs sampled)
   buffer-base64-aes256                x 27,226 ops/sec ±2.49% (133 runs sampled)
   buffer-base64-bf                    x  9,331 ops/sec ±1.92% (137 runs sampled)
   buffer-base64-bf-cbc                x  9,679 ops/sec ±1.58% (138 runs sampled)
   buffer-base64-bf-cfb                x  9,842 ops/sec ±1.27% (142 runs sampled)
   buffer-base64-bf-ecb                x  9,820 ops/sec ±1.40% (142 runs sampled)
   buffer-base64-bf-ofb                x  9,673 ops/sec ±1.86% (139 runs sampled)
   buffer-base64-blowfish              x  9,623 ops/sec ±1.66% (139 runs sampled)
   buffer-base64-camellia-128-cbc      x 24,217 ops/sec ±2.28% (138 runs sampled)
   buffer-base64-camellia-128-cfb      x 24,831 ops/sec ±2.51% (132 runs sampled)
   buffer-base64-camellia-128-cfb1     x    617 ops/sec ±1.50% (135 runs sampled)
   buffer-base64-camellia-128-cfb8     x  4,497 ops/sec ±2.04% (129 runs sampled)
   buffer-base64-camellia-128-ecb      x 18,594 ops/sec ±3.90% (122 runs sampled)
   buffer-base64-camellia-128-ofb      x 23,199 ops/sec ±3.41% (127 runs sampled)
   buffer-base64-camellia-192-cbc      x 21,068 ops/sec ±2.68% (133 runs sampled)
   buffer-base64-camellia-192-cfb      x 21,519 ops/sec ±2.88% (130 runs sampled)
   buffer-base64-camellia-192-cfb1     x    497 ops/sec ±1.31% (133 runs sampled)
   buffer-base64-camellia-192-cfb8     x  4,105 ops/sec ±1.28% (137 runs sampled)
   buffer-base64-camellia-192-ecb      x 18,945 ops/sec ±2.76% (124 runs sampled)
   buffer-base64-camellia-192-ofb      x 20,016 ops/sec ±3.16% (128 runs sampled)
   buffer-base64-camellia-256-cbc      x 18,492 ops/sec ±2.69% (124 runs sampled)
   buffer-base64-camellia-256-cfb      x 18,069 ops/sec ±3.84% (123 runs sampled)
   buffer-base64-camellia-256-cfb1     x    469 ops/sec ±1.51% (133 runs sampled)
   buffer-base64-camellia-256-cfb8     x  3,728 ops/sec ±1.47% (133 runs sampled)
   buffer-base64-camellia-256-ecb      x 17,943 ops/sec ±2.89% (125 runs sampled)
   buffer-base64-camellia-256-ofb      x 21,609 ops/sec ±2.78% (134 runs sampled)
   buffer-base64-camellia128           x 23,799 ops/sec ±2.16% (140 runs sampled)
   buffer-base64-camellia192           x 21,048 ops/sec ±2.77% (140 runs sampled)
   buffer-base64-camellia256           x 22,170 ops/sec ±2.13% (138 runs sampled)
   buffer-base64-cast                  x 18,218 ops/sec ±3.39% (133 runs sampled)
   buffer-base64-cast-cbc              x 17,437 ops/sec ±2.99% (126 runs sampled)
   buffer-base64-cast5-cbc             x 16,881 ops/sec ±3.39% (124 runs sampled)
   buffer-base64-cast5-cfb             x 18,583 ops/sec ±2.48% (135 runs sampled)
   buffer-base64-cast5-ecb             x 19,701 ops/sec ±2.37% (135 runs sampled)
   buffer-base64-cast5-ofb             x 20,871 ops/sec ±2.56% (135 runs sampled)
   buffer-base64-des                   x 17,389 ops/sec ±2.14% (139 runs sampled)
   buffer-base64-des-cbc               x 17,593 ops/sec ±2.19% (137 runs sampled)
   buffer-base64-des-cfb               x 17,207 ops/sec ±1.94% (137 runs sampled)
   buffer-base64-des-cfb1              x    564 ops/sec ±0.51% (143 runs sampled)
   buffer-base64-des-cfb8              x  4,446 ops/sec ±1.00% (145 runs sampled)
   buffer-base64-des-ecb               x 16,978 ops/sec ±2.22% (134 runs sampled)
   buffer-base64-des-ede               x 10,011 ops/sec ±2.02% (136 runs sampled)
   buffer-base64-des-ede-cbc           x 10,459 ops/sec ±1.52% (139 runs sampled)
   buffer-base64-des-ede-cfb           x 10,483 ops/sec ±2.05% (137 runs sampled)
   buffer-base64-des-ede-ofb           x 10,499 ops/sec ±1.80% (139 runs sampled)
   buffer-base64-des-ede3              x  9,981 ops/sec ±1.69% (135 runs sampled)
   buffer-base64-des-ede3-cbc          x 10,346 ops/sec ±2.05% (138 runs sampled)
   buffer-base64-des-ede3-cfb          x 10,678 ops/sec ±1.83% (142 runs sampled)
   buffer-base64-des-ede3-cfb1         x  1,768 ops/sec ±0.98% (141 runs sampled)
   buffer-base64-des-ede3-cfb8         x  1,847 ops/sec ±0.88% (144 runs sampled)
   buffer-base64-des-ede3-ofb          x 10,925 ops/sec ±1.51% (141 runs sampled)
   buffer-base64-des-ofb               x 18,288 ops/sec ±2.34% (135 runs sampled)
   buffer-base64-des3                  x 10,037 ops/sec ±1.87% (136 runs sampled)
   buffer-base64-desx                  x 16,087 ops/sec ±2.68% (133 runs sampled)
   buffer-base64-desx-cbc              x 16,717 ops/sec ±2.34% (133 runs sampled)
   buffer-base64-id-aes128-GCM         x 27,787 ops/sec ±3.52% (125 runs sampled)
   buffer-base64-id-aes192-GCM         x 29,109 ops/sec ±2.96% (130 runs sampled)
   buffer-base64-id-aes256-GCM         x 28,922 ops/sec ±3.44% (131 runs sampled)
   buffer-base64-idea                  x 17,568 ops/sec ±2.44% (134 runs sampled)
   buffer-base64-idea-cbc              x 19,020 ops/sec ±1.92% (139 runs sampled)
   buffer-base64-idea-cfb              x 19,074 ops/sec ±1.92% (139 runs sampled)
   buffer-base64-idea-ecb              x 19,361 ops/sec ±1.84% (138 runs sampled)
   buffer-base64-idea-ofb              x 19,300 ops/sec ±1.94% (137 runs sampled)
   buffer-base64-rc2                   x 11,594 ops/sec ±2.92% (131 runs sampled)
   buffer-base64-rc2-40-cbc            x 10,896 ops/sec ±2.63% (128 runs sampled)
   buffer-base64-rc2-64-cbc            x 12,155 ops/sec ±2.05% (139 runs sampled)
   buffer-base64-rc2-cbc               x 11,708 ops/sec ±2.43% (135 runs sampled)
   buffer-base64-rc2-cfb               x 12,682 ops/sec ±2.12% (134 runs sampled)
   buffer-base64-rc2-ecb               x 12,927 ops/sec ±1.74% (132 runs sampled)
   buffer-base64-rc2-ofb               x 15,480 ops/sec ±1.65% (140 runs sampled)
   buffer-base64-rc4                   x 30,868 ops/sec ±2.68% (129 runs sampled)
   buffer-base64-rc4-40                x 32,422 ops/sec ±2.03% (130 runs sampled)
   buffer-base64-rc4-hmac-md5          x 29,667 ops/sec ±2.28% (130 runs sampled)
   buffer-base64-seed                  x 18,077 ops/sec ±2.09% (130 runs sampled)
   buffer-base64-seed-cbc              x 17,161 ops/sec ±2.28% (128 runs sampled)
   buffer-base64-seed-cfb              x 18,120 ops/sec ±2.81% (125 runs sampled)
   buffer-base64-seed-ecb              x 16,810 ops/sec ±2.10% (129 runs sampled)
   buffer-base64-seed-ofb              x 18,203 ops/sec ±2.35% (129 runs sampled)
Fastest is: buffer-base64-aes-128-ctr

> node benchmark/body-10000.js
  10000 body

   buffer-base64-CAST-cbc              x  4,434 ops/sec ±0.93% (134 runs sampled)
   buffer-base64-aes-128-cbc           x 11,491 ops/sec ±1.02% (134 runs sampled)
   buffer-base64-aes-128-cbc-hmac-sha1 x 10,694 ops/sec ±1.58% (130 runs sampled)
   buffer-base64-aes-128-cfb           x 10,234 ops/sec ±2.79% (125 runs sampled)
   buffer-base64-aes-128-cfb1          x    153 ops/sec ±0.89% (125 runs sampled)
   buffer-base64-aes-128-cfb8          x  1,568 ops/sec ±1.07% (138 runs sampled)
   buffer-base64-aes-128-ctr           x 17,760 ops/sec ±0.89% (140 runs sampled)
   buffer-base64-aes-128-ecb           x 16,029 ops/sec ±1.13% (138 runs sampled)
   buffer-base64-aes-128-gcm           x 15,190 ops/sec ±0.66% (138 runs sampled)
   buffer-base64-aes-128-ofb           x 12,386 ops/sec ±1.16% (138 runs sampled)
   buffer-base64-aes-128-xts           x 17,290 ops/sec ±0.90% (134 runs sampled)
   buffer-base64-aes-192-cbc           x 11,101 ops/sec ±1.74% (124 runs sampled)
   buffer-base64-aes-192-cfb           x 10,460 ops/sec ±1.60% (129 runs sampled)
   buffer-base64-aes-192-cfb1          x    129 ops/sec ±1.12% (121 runs sampled)
   buffer-base64-aes-192-cfb8          x  1,363 ops/sec ±0.83% (139 runs sampled)
   buffer-base64-aes-192-ctr           x 16,381 ops/sec ±1.61% (137 runs sampled)
   buffer-base64-aes-192-ecb           x 15,521 ops/sec ±1.41% (131 runs sampled)
   buffer-base64-aes-192-gcm           x 14,805 ops/sec ±0.90% (139 runs sampled)
   buffer-base64-aes-192-ofb           x 11,796 ops/sec ±1.00% (137 runs sampled)
   buffer-base64-aes-256-cbc           x 11,112 ops/sec ±1.22% (134 runs sampled)
   buffer-base64-aes-256-cbc-hmac-sha1 x 10,544 ops/sec ±1.21% (133 runs sampled)
   buffer-base64-aes-256-cfb           x 10,700 ops/sec ±1.28% (134 runs sampled)
   buffer-base64-aes-256-cfb1          x    128 ops/sec ±0.93% (121 runs sampled)
   buffer-base64-aes-256-cfb8          x  1,287 ops/sec ±0.69% (134 runs sampled)
   buffer-base64-aes-256-ctr           x 16,989 ops/sec ±0.89% (135 runs sampled)
   buffer-base64-aes-256-ecb           x 16,213 ops/sec ±1.10% (133 runs sampled)
   buffer-base64-aes-256-gcm           x 14,655 ops/sec ±1.39% (136 runs sampled)
   buffer-base64-aes-256-ofb           x 11,205 ops/sec ±0.75% (141 runs sampled)
   buffer-base64-aes-256-xts           x 16,808 ops/sec ±1.03% (134 runs sampled)
   buffer-base64-aes128                x 11,521 ops/sec ±1.77% (123 runs sampled)
   buffer-base64-aes192                x 10,858 ops/sec ±1.43% (134 runs sampled)
   buffer-base64-aes256                x 10,819 ops/sec ±1.05% (140 runs sampled)
   buffer-base64-bf                    x  3,867 ops/sec ±0.81% (139 runs sampled)
   buffer-base64-bf-cbc                x  3,864 ops/sec ±1.43% (141 runs sampled)
   buffer-base64-bf-cfb                x  3,455 ops/sec ±1.09% (140 runs sampled)
   buffer-base64-bf-ecb                x  3,893 ops/sec ±1.19% (141 runs sampled)
   buffer-base64-bf-ofb                x  3,983 ops/sec ±0.78% (142 runs sampled)
   buffer-base64-blowfish              x  4,047 ops/sec ±0.83% (137 runs sampled)
   buffer-base64-camellia-128-cbc      x  6,950 ops/sec ±0.89% (137 runs sampled)
   buffer-base64-camellia-128-cfb      x  6,507 ops/sec ±1.95% (129 runs sampled)
   buffer-base64-camellia-128-cfb1     x  66.60 ops/sec ±1.49% (116 runs sampled)
   buffer-base64-camellia-128-cfb8     x    637 ops/sec ±0.68% (130 runs sampled)
   buffer-base64-camellia-128-ecb      x  6,903 ops/sec ±1.07% (133 runs sampled)
   buffer-base64-camellia-128-ofb      x  7,083 ops/sec ±0.90% (136 runs sampled)
   buffer-base64-camellia-192-cbc      x  5,603 ops/sec ±1.29% (130 runs sampled)
   buffer-base64-camellia-192-cfb      x  5,287 ops/sec ±2.40% (120 runs sampled)
   buffer-base64-camellia-192-cfb1     x  53.22 ops/sec ±0.93% (117 runs sampled)
   buffer-base64-camellia-192-cfb8     x    485 ops/sec ±0.72% (136 runs sampled)
   buffer-base64-camellia-192-ecb      x  5,403 ops/sec ±2.21% (136 runs sampled)
   buffer-base64-camellia-192-ofb      x  5,734 ops/sec ±1.03% (136 runs sampled)
   buffer-base64-camellia-256-cbc      x  5,790 ops/sec ±1.07% (136 runs sampled)
   buffer-base64-camellia-256-cfb      x  5,620 ops/sec ±1.04% (131 runs sampled)
   buffer-base64-camellia-256-cfb1     x  55.21 ops/sec ±1.04% (105 runs sampled)
   buffer-base64-camellia-256-cfb8     x    501 ops/sec ±0.80% (134 runs sampled)
   buffer-base64-camellia-256-ecb      x  5,796 ops/sec ±0.96% (133 runs sampled)
   buffer-base64-camellia-256-ofb      x  5,981 ops/sec ±1.08% (136 runs sampled)
   buffer-base64-camellia128           x  7,050 ops/sec ±1.44% (131 runs sampled)
   buffer-base64-camellia192           x  5,847 ops/sec ±1.05% (129 runs sampled)
   buffer-base64-camellia256           x  5,952 ops/sec ±0.83% (134 runs sampled)
   buffer-base64-cast                  x  4,557 ops/sec ±0.81% (130 runs sampled)
   buffer-base64-cast-cbc              x  4,450 ops/sec ±0.74% (140 runs sampled)
   buffer-base64-cast5-cbc             x  4,446 ops/sec ±0.70% (142 runs sampled)
   buffer-base64-cast5-cfb             x  4,058 ops/sec ±0.79% (139 runs sampled)
   buffer-base64-cast5-ecb             x  4,516 ops/sec ±0.64% (143 runs sampled)
   buffer-base64-cast5-ofb             x  4,830 ops/sec ±0.66% (139 runs sampled)
   buffer-base64-des                   x  3,493 ops/sec ±0.85% (133 runs sampled)
   buffer-base64-des-cbc               x  3,419 ops/sec ±0.65% (143 runs sampled)
   buffer-base64-des-cfb               x  3,200 ops/sec ±0.57% (143 runs sampled)
   buffer-base64-des-cfb1              x  56.96 ops/sec ±0.45% (120 runs sampled)
   buffer-base64-des-cfb8              x    495 ops/sec ±0.49% (138 runs sampled)
   buffer-base64-des-ecb               x  3,448 ops/sec ±0.68% (140 runs sampled)
   buffer-base64-des-ede               x  1,533 ops/sec ±0.85% (139 runs sampled)
   buffer-base64-des-ede-cbc           x  1,532 ops/sec ±0.49% (139 runs sampled)
   buffer-base64-des-ede-cfb           x  1,478 ops/sec ±0.54% (139 runs sampled)
   buffer-base64-des-ede-ofb           x  1,518 ops/sec ±0.47% (136 runs sampled)
   buffer-base64-des-ede3              x  1,479 ops/sec ±1.50% (130 runs sampled)
   buffer-base64-des-ede3-cbc          x  1,488 ops/sec ±1.34% (134 runs sampled)
   buffer-base64-des-ede3-cfb          x  1,433 ops/sec ±1.22% (140 runs sampled)
   buffer-base64-des-ede3-cfb1         x    184 ops/sec ±0.78% (134 runs sampled)
   buffer-base64-des-ede3-cfb8         x    195 ops/sec ±0.40% (131 runs sampled)
   buffer-base64-des-ede3-ofb          x  1,474 ops/sec ±0.96% (138 runs sampled)
   buffer-base64-des-ofb               x  3,381 ops/sec ±1.18% (141 runs sampled)
   buffer-base64-des3                  x  1,463 ops/sec ±1.28% (140 runs sampled)
   buffer-base64-desx                  x  3,200 ops/sec ±1.30% (138 runs sampled)
   buffer-base64-desx-cbc              x  3,255 ops/sec ±0.68% (139 runs sampled)
   buffer-base64-id-aes128-GCM         x 14,061 ops/sec ±1.39% (133 runs sampled)
   buffer-base64-id-aes192-GCM         x 13,780 ops/sec ±1.69% (136 runs sampled)
   buffer-base64-id-aes256-GCM         x 13,342 ops/sec ±1.54% (131 runs sampled)
   buffer-base64-idea                  x  3,741 ops/sec ±0.69% (143 runs sampled)
   buffer-base64-idea-cbc              x  3,737 ops/sec ±0.77% (142 runs sampled)
   buffer-base64-idea-cfb              x  3,251 ops/sec ±1.02% (137 runs sampled)
   buffer-base64-idea-ecb              x  3,444 ops/sec ±1.23% (134 runs sampled)
   buffer-base64-idea-ofb              x  3,499 ops/sec ±1.07% (141 runs sampled)
   buffer-base64-rc2                   x  1,858 ops/sec ±0.65% (141 runs sampled)
   buffer-base64-rc2-40-cbc            x  1,828 ops/sec ±1.09% (141 runs sampled)
   buffer-base64-rc2-64-cbc            x  1,843 ops/sec ±1.34% (138 runs sampled)
   buffer-base64-rc2-cbc               x  1,838 ops/sec ±0.71% (141 runs sampled)
   buffer-base64-rc2-cfb               x  1,858 ops/sec ±0.55% (130 runs sampled)
   buffer-base64-rc2-ecb               x  1,955 ops/sec ±0.57% (141 runs sampled)
   buffer-base64-rc2-ofb               x  2,477 ops/sec ±0.86% (141 runs sampled)
   buffer-base64-rc4                   x 13,403 ops/sec ±1.24% (133 runs sampled)
   buffer-base64-rc4-40                x 13,086 ops/sec ±1.07% (135 runs sampled)
   buffer-base64-rc4-hmac-md5          x 11,419 ops/sec ±0.89% (140 runs sampled)
   buffer-base64-seed                  x  3,336 ops/sec ±0.74% (136 runs sampled)
   buffer-base64-seed-cbc              x  3,341 ops/sec ±1.15% (136 runs sampled)
   buffer-base64-seed-cfb              x  3,474 ops/sec ±0.69% (142 runs sampled)
   buffer-base64-seed-ecb              x  3,638 ops/sec ±0.95% (136 runs sampled)
   buffer-base64-seed-ofb              x  3,696 ops/sec ±0.88% (133 runs sampled)
Fastest is: buffer-base64-aes-128-ctr
```
