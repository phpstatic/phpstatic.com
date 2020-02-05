# macOS 10.15.3, I7-7700K

[phpbench](https://github.com/phpbench/phpbench.git) 

php-static-7.3.14 without opcache
```sh
PhpBench 0.8.0. Running benchmarks.

\PhpBench\Tests\Functional\benchmarks\ArrayKeysBench

    benchArrayKeyExists           I3 P0 	μ/r: 0.070μs	μSD/r 0.001μs	μRSD/r: 2.11%
    benchArrayKeyExists           I3 P1 	μ/r: 0.070μs	μSD/r 0.001μs	μRSD/r: 1.43%
    benchArrayKeyExists           I3 P2 	μ/r: 0.073μs	μSD/r 0.004μs	μRSD/r: 6.05%
    benchArrayKeyExists           I3 P3 	μ/r: 0.075μs	μSD/r 0.010μs	μRSD/r: 12.93%
    benchIsset                    I3 P0 	μ/r: 0.058μs	μSD/r 0.001μs	μRSD/r: 1.44%
    benchIsset                    I3 P1 	μ/r: 0.057μs	μSD/r 0.001μs	μRSD/r: 2.27%
    benchIsset                    I3 P2 	μ/r: 0.058μs	μSD/r 0.002μs	μRSD/r: 2.61%
    benchIsset                    I3 P3 	μ/r: 0.058μs	μSD/r 0.001μs	μRSD/r: 1.51%
    benchInArray                  I3 P0 	μ/r: 0.081μs	μSD/r 0.001μs	μRSD/r: 1.75%
    benchInArray                  I3 P1 	μ/r: 0.215μs	μSD/r 0.001μs	μRSD/r: 0.60%
    benchInArray                  I3 P2 	μ/r: 0.809μs	μSD/r 0.001μs	μRSD/r: 0.11%
    benchInArray                  I3 P3 	μ/r: 0.809μs	μSD/r 0.001μs	μRSD/r: 0.15%

\CostOfCalling

    benchCallWithoutParams        I9 P0 	μ/r: 0.046μs	μSD/r 0.000μs	μRSD/r: 0.76%
    benchCallWithParams           I9 P0 	μ/r: 0.052μs	μSD/r 0.003μs	μRSD/r: 4.94%
    benchUserFuncWithoutParams    I9 P0 	μ/r: 0.117μs	μSD/r 0.006μs	μRSD/r: 4.71%
    benchUserFuncParams           I9 P0 	μ/r: 0.125μs	μSD/r 0.002μs	μRSD/r: 1.85%
    benchReflectionCall           I9 P0 	μ/r: 0.088μs	μSD/r 0.004μs	μRSD/r: 4.40%
    benchReflectionCallWithParams I9 P0 	μ/r: 0.131μs	μSD/r 0.006μs	μRSD/r: 4.82%

\HashingBenchmark

    benchMd5                      I9 P0 	μ/r: 0.238μs	μSD/r 0.012μs	μRSD/r: 5.02%
    benchSha256                   I9 P0 	μ/r: 0.436μs	μSD/r 0.005μs	μRSD/r: 1.22%
    benchSha1                     I9 P0 	μ/r: 0.301μs	μSD/r 0.066μs	μRSD/r: 21.91%

\StringSplitting

    benchStrStrSubstr             I7 P0 	μ/r: 0.116μs	μSD/r 0.004μs	μRSD/r: 3.51%
    benchPregMatch                I7 P0 	μ/r: 0.484μs	μSD/r 0.046μs	μRSD/r: 9.47%
    benchExplode                  I7 P0 	μ/r: 0.123μs	μSD/r 0.002μs	μRSD/r: 1.98%

\CostOfReflectionBench

    benchMethodSet                I3 P0 	μ/r: 0.052μs	μSD/r 0.000μs	μRSD/r: 0.90%
    benchPublicProperty           I3 P0 	μ/r: 0.051μs	μSD/r 0.007μs	μRSD/r: 13.44%
    benchPublicReflection         I3 P0 	μ/r: 0.088μs	μSD/r 0.001μs	μRSD/r: 1.51%
    benchPrivateReflection        I3 P0 	μ/r: 0.088μs	μSD/r 0.002μs	μRSD/r: 2.68%
    benchNewClass                 I3 P0 	μ/r: 0.057μs	μSD/r 0.000μs	μRSD/r: 0.15%
    benchReflectionNewInstance    I3 P0 	μ/r: 0.084μs	μSD/r 0.009μs	μRSD/r: 10.99%

21 subjects, 186 iterations, 942000 revs, 0 rejects
min mean max: 0.044 0.104 0.810 (μs/r)
⅀T: 97,783.000μs μSD/r 0.007μs μRSD/r: 4.240%

+-----------------------+-------------------------------+---------------------------+-------------------------+--------+-----+------------+----------+----------+----------+----------+--------+
| benchmark             | subject                       | group                     | params                  | revs   | its | mem        | min      | mean     | max      | stdev    | rstdev |
+-----------------------+-------------------------------+---------------------------+-------------------------+--------+-----+------------+----------+----------+----------+----------+--------+
| ArrayKeysBench        | benchArrayKeyExists           | array_keys                | {"nb_elements":"10"}    | 4000   | 4   | 1,180,944b | 0.0680μs | 0.0703μs | 0.0720μs | 0.0015μs | 2.11%  |
| ArrayKeysBench        | benchArrayKeyExists           | array_keys                | {"nb_elements":"100"}   | 4000   | 4   | 1,180,944b | 0.0690μs | 0.0700μs | 0.0710μs | 0.0010μs | 1.43%  |
| ArrayKeysBench        | benchArrayKeyExists           | array_keys                | {"nb_elements":"1000"}  | 4000   | 4   | 1,180,944b | 0.0690μs | 0.0725μs | 0.0800μs | 0.0044μs | 6.05%  |
| ArrayKeysBench        | benchArrayKeyExists           | array_keys                | {"nb_elements":"10000"} | 4000   | 4   | 3,054,592b | 0.0680μs | 0.0753μs | 0.0920μs | 0.0097μs | 12.93% |
| ArrayKeysBench        | benchIsset                    | array_keys                | {"nb_elements":"10"}    | 4000   | 4   | 1,180,936b | 0.0570μs | 0.0578μs | 0.0590μs | 0.0008μs | 1.44%  |
| ArrayKeysBench        | benchIsset                    | array_keys                | {"nb_elements":"100"}   | 4000   | 4   | 1,180,936b | 0.0550μs | 0.0573μs | 0.0580μs | 0.0013μs | 2.27%  |
| ArrayKeysBench        | benchIsset                    | array_keys                | {"nb_elements":"1000"}  | 4000   | 4   | 1,180,936b | 0.0560μs | 0.0575μs | 0.0590μs | 0.0015μs | 2.61%  |
| ArrayKeysBench        | benchIsset                    | array_keys                | {"nb_elements":"10000"} | 4000   | 4   | 3,054,584b | 0.0560μs | 0.0575μs | 0.0580μs | 0.0009μs | 1.51%  |
| ArrayKeysBench        | benchInArray                  | array_keys                | {"nb_elements":"10"}    | 4000   | 4   | 1,180,936b | 0.0790μs | 0.0810μs | 0.0830μs | 0.0014μs | 1.75%  |
| ArrayKeysBench        | benchInArray                  | array_keys                | {"nb_elements":"100"}   | 4000   | 4   | 1,180,936b | 0.2130μs | 0.2148μs | 0.2160μs | 0.0013μs | 0.60%  |
| ArrayKeysBench        | benchInArray                  | array_keys                | {"nb_elements":"1000"}  | 4000   | 4   | 1,180,936b | 0.8080μs | 0.8085μs | 0.8100μs | 0.0009μs | 0.11%  |
| ArrayKeysBench        | benchInArray                  | array_keys                | {"nb_elements":"10000"} | 4000   | 4   | 3,054,584b | 0.8070μs | 0.8090μs | 0.8100μs | 0.0012μs | 0.15%  |
| CostOfCalling         | benchCallWithoutParams        | cost_of_calling,group_two | []                      | 100000 | 10  | 1,178,408b | 0.0451μs | 0.0456μs | 0.0462μs | 0.0003μs | 0.76%  |
| CostOfCalling         | benchCallWithParams           | cost_of_calling,group_two | []                      | 100000 | 10  | 1,178,408b | 0.0503μs | 0.0516μs | 0.0587μs | 0.0025μs | 4.94%  |
| CostOfCalling         | benchUserFuncWithoutParams    | cost_of_calling,group_two | []                      | 100000 | 10  | 1,178,416b | 0.1140μs | 0.1168μs | 0.1331μs | 0.0055μs | 4.71%  |
| CostOfCalling         | benchUserFuncParams           | cost_of_calling,group_two | []                      | 100000 | 10  | 1,178,408b | 0.1235μs | 0.1247μs | 0.1316μs | 0.0023μs | 1.85%  |
| CostOfCalling         | benchReflectionCall           | cost_of_calling,group_two | []                      | 100000 | 10  | 1,178,824b | 0.0864μs | 0.0880μs | 0.0996μs | 0.0039μs | 4.40%  |
| CostOfCalling         | benchReflectionCallWithParams | cost_of_calling,group_two | []                      | 100000 | 10  | 1,178,848b | 0.1274μs | 0.1308μs | 0.1439μs | 0.0063μs | 4.82%  |
| HashingBenchmark      | benchMd5                      | hashing                   | []                      | 10000  | 10  | 1,173,000b | 0.2320μs | 0.2383μs | 0.2740μs | 0.0120μs | 5.02%  |
| HashingBenchmark      | benchSha256                   | hashing                   | []                      | 10000  | 10  | 1,173,000b | 0.4330μs | 0.4364μs | 0.4520μs | 0.0053μs | 1.22%  |
| HashingBenchmark      | benchSha1                     | hashing                   | []                      | 10000  | 10  | 1,173,000b | 0.2730μs | 0.3006μs | 0.4980μs | 0.0659μs | 21.91% |
| StringSplitting       | benchStrStrSubstr             | string_extraction         | []                      | 8000   | 8   | 1,175,896b | 0.1140μs | 0.1163μs | 0.1270μs | 0.0041μs | 3.51%  |
| StringSplitting       | benchPregMatch                | string_extraction         | []                      | 8000   | 8   | 1,175,888b | 0.4640μs | 0.4839μs | 0.6050μs | 0.0458μs | 9.47%  |
| StringSplitting       | benchExplode                  | string_extraction         | []                      | 8000   | 8   | 1,175,888b | 0.1210μs | 0.1234μs | 0.1280μs | 0.0024μs | 1.98%  |
| CostOfReflectionBench | benchMethodSet                | cost_of_setting           | []                      | 40000  | 4   | 1,180,440b | 0.0514μs | 0.0519μs | 0.0526μs | 0.0005μs | 0.90%  |
| CostOfReflectionBench | benchPublicProperty           | cost_of_setting           | []                      | 40000  | 4   | 1,180,448b | 0.0439μs | 0.0512μs | 0.0593μs | 0.0069μs | 13.44% |
| CostOfReflectionBench | benchPublicReflection         | cost_of_setting           | []                      | 40000  | 4   | 1,180,448b | 0.0863μs | 0.0877μs | 0.0895μs | 0.0013μs | 1.51%  |
| CostOfReflectionBench | benchPrivateReflection        | cost_of_setting           | []                      | 40000  | 4   | 1,180,448b | 0.0854μs | 0.0876μs | 0.0912μs | 0.0023μs | 2.68%  |
| CostOfReflectionBench | benchNewClass                 | cost_of_instantiation     | []                      | 40000  | 4   | 1,180,440b | 0.0570μs | 0.0571μs | 0.0572μs | 0.0001μs | 0.15%  |
| CostOfReflectionBench | benchReflectionNewInstance    | cost_of_instantiation     | []                      | 40000  | 4   | 1,180,456b | 0.0745μs | 0.0838μs | 0.0961μs | 0.0092μs | 10.99% |
+-----------------------+-------------------------------+---------------------------+-------------------------+--------+-----+------------+----------+----------+----------+----------+--------+

```

apple default php 7.3.11 
```sh
PhpBench 0.8.0. Running benchmarks.

\PhpBench\Tests\Functional\benchmarks\ArrayKeysBench

    benchArrayKeyExists           I3 P0 	μ/r: 0.105μs	μSD/r 0.009μs	μRSD/r: 8.41%
    benchArrayKeyExists           I3 P1 	μ/r: 0.100μs	μSD/r 0.001μs	μRSD/r: 0.71%
    benchArrayKeyExists           I3 P2 	μ/r: 0.112μs	μSD/r 0.020μs	μRSD/r: 17.70%
    benchArrayKeyExists           I3 P3 	μ/r: 0.099μs	μSD/r 0.001μs	μRSD/r: 0.84%
    benchIsset                    I3 P0 	μ/r: 0.078μs	μSD/r 0.001μs	μRSD/r: 1.44%
    benchIsset                    I3 P1 	μ/r: 0.078μs	μSD/r 0.000μs	μRSD/r: 0.55%
    benchIsset                    I3 P2 	μ/r: 0.077μs	μSD/r 0.001μs	μRSD/r: 1.07%
    benchIsset                    I3 P3 	μ/r: 0.087μs	μSD/r 0.016μs	μRSD/r: 18.36%
    benchInArray                  I3 P0 	μ/r: 0.098μs	μSD/r 0.001μs	μRSD/r: 1.11%
    benchInArray                  I3 P1 	μ/r: 0.159μs	μSD/r 0.001μs	μRSD/r: 0.71%
    benchInArray                  I3 P2 	μ/r: 0.423μs	μSD/r 0.001μs	μRSD/r: 0.35%
    benchInArray                  I3 P3 	μ/r: 0.422μs	μSD/r 0.001μs	μRSD/r: 0.17%

\CostOfCalling

    benchCallWithoutParams        I9 P0 	μ/r: 0.074μs	μSD/r 0.001μs	μRSD/r: 1.91%
    benchCallWithParams           I9 P0 	μ/r: 0.081μs	μSD/r 0.003μs	μRSD/r: 3.27%
    benchUserFuncWithoutParams    I9 P0 	μ/r: 0.166μs	μSD/r 0.019μs	μRSD/r: 11.33%
    benchUserFuncParams           I9 P0 	μ/r: 0.167μs	μSD/r 0.006μs	μRSD/r: 3.81%
    benchReflectionCall           I9 P0 	μ/r: 0.125μs	μSD/r 0.008μs	μRSD/r: 6.16%
    benchReflectionCallWithParams I9 P0 	μ/r: 0.176μs	μSD/r 0.005μs	μRSD/r: 3.02%

\HashingBenchmark

    benchMd5                      I9 P0 	μ/r: 0.306μs	μSD/r 0.001μs	μRSD/r: 0.48%
    benchSha256                   I9 P0 	μ/r: 0.509μs	μSD/r 0.007μs	μRSD/r: 1.41%
    benchSha1                     I9 P0 	μ/r: 0.327μs	μSD/r 0.003μs	μRSD/r: 1.04%

\StringSplitting

    benchStrStrSubstr             I7 P0 	μ/r: 0.173μs	μSD/r 0.001μs	μRSD/r: 0.73%
    benchPregMatch                I7 P0 	μ/r: 0.481μs	μSD/r 0.006μs	μRSD/r: 1.25%
    benchExplode                  I7 P0 	μ/r: 0.186μs	μSD/r 0.007μs	μRSD/r: 3.72%

\CostOfReflectionBench

    benchMethodSet                I3 P0 	μ/r: 0.076μs	μSD/r 0.004μs	μRSD/r: 5.65%
    benchPublicProperty           I3 P0 	μ/r: 0.065μs	μSD/r 0.000μs	μRSD/r: 0.35%
    benchPublicReflection         I3 P0 	μ/r: 0.119μs	μSD/r 0.005μs	μRSD/r: 4.51%
    benchPrivateReflection        I3 P0 	μ/r: 0.120μs	μSD/r 0.007μs	μRSD/r: 5.76%
    benchNewClass                 I3 P0 	μ/r: 0.077μs	μSD/r 0.000μs	μRSD/r: 0.19%
    benchReflectionNewInstance    I3 P0 	μ/r: 0.106μs	μSD/r 0.000μs	μRSD/r: 0.23%

21 subjects, 186 iterations, 942000 revs, 0 rejects
min mean max: 0.065 0.135 0.529 (μs/r)
⅀T: 126,924.000μs μSD/r 0.005μs μRSD/r: 3.542%

+-----------------------+-------------------------------+---------------------------+-------------------------+--------+-----+------------+----------+----------+----------+----------+--------+
| benchmark             | subject                       | group                     | params                  | revs   | its | mem        | min      | mean     | max      | stdev    | rstdev |
+-----------------------+-------------------------------+---------------------------+-------------------------+--------+-----+------------+----------+----------+----------+----------+--------+
| ArrayKeysBench        | benchArrayKeyExists           | array_keys                | {"nb_elements":"10"}    | 4000   | 4   | 464,264b   | 0.0990μs | 0.1048μs | 0.1200μs | 0.0088μs | 8.41%  |
| ArrayKeysBench        | benchArrayKeyExists           | array_keys                | {"nb_elements":"100"}   | 4000   | 4   | 464,264b   | 0.0990μs | 0.1000μs | 0.1010μs | 0.0007μs | 0.71%  |
| ArrayKeysBench        | benchArrayKeyExists           | array_keys                | {"nb_elements":"1000"}  | 4000   | 4   | 572,136b   | 0.1000μs | 0.1118μs | 0.1460μs | 0.0198μs | 17.70% |
| ArrayKeysBench        | benchArrayKeyExists           | array_keys                | {"nb_elements":"10000"} | 4000   | 4   | 2,538,216b | 0.0980μs | 0.0993μs | 0.1000μs | 0.0008μs | 0.84%  |
| ArrayKeysBench        | benchIsset                    | array_keys                | {"nb_elements":"10"}    | 4000   | 4   | 464,256b   | 0.0760μs | 0.0775μs | 0.0790μs | 0.0011μs | 1.44%  |
| ArrayKeysBench        | benchIsset                    | array_keys                | {"nb_elements":"100"}   | 4000   | 4   | 464,256b   | 0.0780μs | 0.0783μs | 0.0790μs | 0.0004μs | 0.55%  |
| ArrayKeysBench        | benchIsset                    | array_keys                | {"nb_elements":"1000"}  | 4000   | 4   | 572,128b   | 0.0760μs | 0.0773μs | 0.0780μs | 0.0008μs | 1.07%  |
| ArrayKeysBench        | benchIsset                    | array_keys                | {"nb_elements":"10000"} | 4000   | 4   | 2,538,208b | 0.0780μs | 0.0873μs | 0.1150μs | 0.0160μs | 18.36% |
| ArrayKeysBench        | benchInArray                  | array_keys                | {"nb_elements":"10"}    | 4000   | 4   | 464,256b   | 0.0960μs | 0.0978μs | 0.0990μs | 0.0011μs | 1.11%  |
| ArrayKeysBench        | benchInArray                  | array_keys                | {"nb_elements":"100"}   | 4000   | 4   | 464,256b   | 0.1570μs | 0.1585μs | 0.1600μs | 0.0011μs | 0.71%  |
| ArrayKeysBench        | benchInArray                  | array_keys                | {"nb_elements":"1000"}  | 4000   | 4   | 572,128b   | 0.4210μs | 0.4228μs | 0.4250μs | 0.0015μs | 0.35%  |
| ArrayKeysBench        | benchInArray                  | array_keys                | {"nb_elements":"10000"} | 4000   | 4   | 2,538,208b | 0.4210μs | 0.4220μs | 0.4230μs | 0.0007μs | 0.17%  |
| CostOfCalling         | benchCallWithoutParams        | cost_of_calling,group_two | []                      | 100000 | 10  | 462,584b   | 0.0730μs | 0.0740μs | 0.0782μs | 0.0014μs | 1.91%  |
| CostOfCalling         | benchCallWithParams           | cost_of_calling,group_two | []                      | 100000 | 10  | 462,584b   | 0.0789μs | 0.0807μs | 0.0868μs | 0.0026μs | 3.27%  |
| CostOfCalling         | benchUserFuncWithoutParams    | cost_of_calling,group_two | []                      | 100000 | 10  | 462,592b   | 0.1595μs | 0.1662μs | 0.2227μs | 0.0188μs | 11.33% |
| CostOfCalling         | benchUserFuncParams           | cost_of_calling,group_two | []                      | 100000 | 10  | 462,584b   | 0.1637μs | 0.1670μs | 0.1832μs | 0.0064μs | 3.81%  |
| CostOfCalling         | benchReflectionCall           | cost_of_calling,group_two | []                      | 100000 | 10  | 463,000b   | 0.1192μs | 0.1248μs | 0.1415μs | 0.0077μs | 6.16%  |
| CostOfCalling         | benchReflectionCallWithParams | cost_of_calling,group_two | []                      | 100000 | 10  | 463,024b   | 0.1742μs | 0.1765μs | 0.1924μs | 0.0053μs | 3.02%  |
| HashingBenchmark      | benchMd5                      | hashing                   | []                      | 10000  | 10  | 456,736b   | 0.3040μs | 0.3058μs | 0.3090μs | 0.0015μs | 0.48%  |
| HashingBenchmark      | benchSha256                   | hashing                   | []                      | 10000  | 10  | 456,736b   | 0.5040μs | 0.5089μs | 0.5290μs | 0.0072μs | 1.41%  |
| HashingBenchmark      | benchSha1                     | hashing                   | []                      | 10000  | 10  | 456,736b   | 0.3240μs | 0.3267μs | 0.3360μs | 0.0034μs | 1.04%  |
| StringSplitting       | benchStrStrSubstr             | string_extraction         | []                      | 8000   | 8   | 460,200b   | 0.1720μs | 0.1731μs | 0.1750μs | 0.0013μs | 0.73%  |
| StringSplitting       | benchPregMatch                | string_extraction         | []                      | 8000   | 8   | 460,192b   | 0.4750μs | 0.4809μs | 0.4920μs | 0.0060μs | 1.25%  |
| StringSplitting       | benchExplode                  | string_extraction         | []                      | 8000   | 8   | 460,192b   | 0.1810μs | 0.1860μs | 0.2040μs | 0.0069μs | 3.72%  |
| CostOfReflectionBench | benchMethodSet                | cost_of_setting           | []                      | 40000  | 4   | 464,008b   | 0.0725μs | 0.0763μs | 0.0830μs | 0.0043μs | 5.65%  |
| CostOfReflectionBench | benchPublicProperty           | cost_of_setting           | []                      | 40000  | 4   | 464,016b   | 0.0650μs | 0.0652μs | 0.0655μs | 0.0002μs | 0.35%  |
| CostOfReflectionBench | benchPublicReflection         | cost_of_setting           | []                      | 40000  | 4   | 464,016b   | 0.1160μs | 0.1193μs | 0.1286μs | 0.0054μs | 4.51%  |
| CostOfReflectionBench | benchPrivateReflection        | cost_of_setting           | []                      | 40000  | 4   | 464,016b   | 0.1156μs | 0.1198μs | 0.1317μs | 0.0069μs | 5.76%  |
| CostOfReflectionBench | benchNewClass                 | cost_of_instantiation     | []                      | 40000  | 4   | 464,008b   | 0.0765μs | 0.0767μs | 0.0769μs | 0.0001μs | 0.19%  |
| CostOfReflectionBench | benchReflectionNewInstance    | cost_of_instantiation     | []                      | 40000  | 4   | 464,024b   | 0.1059μs | 0.1061μs | 0.1065μs | 0.0002μs | 0.23%  |
+-----------------------+-------------------------------+---------------------------+-------------------------+--------+-----+------------+----------+----------+----------+----------+--------+
```

