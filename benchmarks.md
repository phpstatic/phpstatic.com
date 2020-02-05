test environment：macOS 10.15.3, I7-7700K

php-static-7.3.14 
```sh
PhpBench 0.17.0 Running benchmarks.
Using configuration file: /opt/web/bench/phpbench.json.dist

\PhpBench\Benchmarks\Micro\HashingBench

    benchAlgos # 0..........................I9 [μ Mo]/r: 0.185 0.186 (μs) [μSD μRSD]/r: 0.002μs 1.00%
    benchAlgos # 1..........................I9 [μ Mo]/r: 0.386 0.377 (μs) [μSD μRSD]/r: 0.025μs 6.42%

\PhpBench\Micro\Math\KdeBench

    benchKde # ten points...................I9 [μ Mo]/r: 0.0222 0.0221 (ms) [μSD μRSD]/r: 0.000ms 0.72%
    benchKde # twenty points................I9 [μ Mo]/r: 0.0393 0.0388 (ms) [μSD μRSD]/r: 0.002ms 4.26%
    benchKde # forty points.................I9 [μ Mo]/r: 0.0675 0.0671 (ms) [μSD μRSD]/r: 0.001ms 1.00%

\PhpBench\Micro\Math\StatisticsBench

    benchVariance...........................I9 [μ Mo]/r: 0.67 0.66 (μs) [μSD μRSD]/r: 0.021μs 3.17%
    benchStDev..............................I9 [μ Mo]/r: 0.72 0.72 (μs) [μSD μRSD]/r: 0.022μs 3.07%

\PhpBench\Benchmarks\Micro\DependencyInjection\ContainerBench

    benchInitNoExtensions...................I9 [μ Mo]/r: 0.000033 0.000032 (s) [μSD μRSD]/r: 0.000s 8.38%
    benchInitCoreExtension..................I9 [μ Mo]/r: 0.000245 0.000242 (s) [μSD μRSD]/r: 0.000s 3.50%

\PhpBench\Benchmarks\Macro\LogBench

    benchLog................................I9 [μ Mo]/r: 0.010 0.010 (s) [μSD μRSD]/r: 0.000s 2.07%

\PhpBench\Benchmarks\Macro\benchmarks\NothingBench

    benchNothing............................I0 [μ Mo]/r: 2.000 2.000 (μs) [μSD μRSD]/r: 0.000μs 0.00%

\PhpBench\Benchmarks\Macro\RunBench

    benchRun................................I9 [μ Mo]/r: 0.110 0.109 (s) [μSD μRSD]/r: 0.002s 1.69%
    benchRunAndReport.......................I9 [μ Mo]/r: 0.110 0.109 (s) [μSD μRSD]/r: 0.002s 1.48%

\PhpBench\Benchmarks\Macro\ReportBench

    benchAggregate..........................I9 [μ Mo]/r: 0.002 0.002 (s) [μSD μRSD]/r: 0.000s 2.97%
    benchDefault............................I9 [μ Mo]/r: 0.002 0.002 (s) [μSD μRSD]/r: 0.000s 6.09%
    benchEnv................................I9 [μ Mo]/r: 0.002 0.002 (s) [μSD μRSD]/r: 0.000s 4.99%

13 subjects, 151 iterations, 2,527 revs, 0 rejects, 0 failures, 0 warnings
(best [mean mode] worst) = 0.181 [14,822.750 14,672.939] 0.187 (μs)
⅀T: 2,371,621.925μs μSD/r 249.760μs μRSD/r: 3.175%
suite: 1343b0df9cb075a428fe80cdc43b6127fdd878e7, date: 2020-02-05, stime: 11:14:35
+-----------------+------------------------+---------------+------+-----+------------+-----------+-----------+-----------+-----------+-----------+--------+-------------+
| benchmark       | subject                | set           | revs | its | mem_peak   | best      | mean      | mode      | worst     | stdev     | rstdev | diff        |
+-----------------+------------------------+---------------+------+-----+------------+-----------+-----------+-----------+-----------+-----------+--------+-------------+
| HashingBench    | benchAlgos             | 0             | 1000 | 10  | 1,466,448b | 0.181μs   | 0.185μs   | 0.186μs   | 0.187μs   | 0.002μs   | 1.00%  | 1.00x       |
| HashingBench    | benchAlgos             | 1             | 1000 | 10  | 1,466,448b | 0.377μs   | 0.386μs   | 0.377μs   | 0.460μs   | 0.025μs   | 6.42%  | 2.09x       |
| KdeBench        | benchKde               | ten points    | 100  | 10  | 1,466,824b | 0.0220ms  | 0.0222ms  | 0.0221ms  | 0.0226ms  | 0.0002ms  | 0.72%  | 119.99x     |
| KdeBench        | benchKde               | twenty points | 100  | 10  | 1,466,824b | 0.0386ms  | 0.0393ms  | 0.0388ms  | 0.0443ms  | 0.0017ms  | 4.26%  | 212.85x     |
| KdeBench        | benchKde               | forty points  | 100  | 10  | 1,466,824b | 0.0670ms  | 0.0675ms  | 0.0671ms  | 0.0689ms  | 0.0007ms  | 1.00%  | 365.65x     |
| StatisticsBench | benchVariance          | 0             | 100  | 10  | 1,466,432b | 0.64μs    | 0.67μs    | 0.66μs    | 0.70μs    | 0.02μs    | 3.17%  | 3.60x       |
| StatisticsBench | benchStDev             | 0             | 100  | 10  | 1,466,432b | 0.68μs    | 0.72μs    | 0.72μs    | 0.75μs    | 0.02μs    | 3.07%  | 3.88x       |
| ContainerBench  | benchInitNoExtensions  | 0             | 10   | 10  | 1,466,104b | 0.000031s | 0.000033s | 0.000032s | 0.000041s | 0.000003s | 8.38%  | 177.59x     |
| ContainerBench  | benchInitCoreExtension | 0             | 10   | 10  | 1,582,512b | 0.000240s | 0.000245s | 0.000242s | 0.000270s | 0.000009s | 3.50%  | 1,325.55x   |
| LogBench        | benchLog               | 0             | 1    | 10  | 4,042,280b | 0.010s    | 0.010s    | 0.010s    | 0.011s    | 0.000s    | 2.07%  | 55,774.23x  |
| NothingBench    | benchNothing           | 0             | 1    | 1   | 1,466,040b | 2.000μs   | 2.000μs   | 2.000μs   | 2.000μs   | 0.000μs   | 0.00%  | 10.83x      |
| RunBench        | benchRun               | 0             | 1    | 10  | 3,100,712b | 0.108s    | 0.110s    | 0.109s    | 0.114s    | 0.002s    | 1.69%  | 595,754.74x |
| RunBench        | benchRunAndReport      | 0             | 1    | 10  | 3,169,488b | 0.108s    | 0.110s    | 0.109s    | 0.113s    | 0.002s    | 1.48%  | 597,476.99x |
| ReportBench     | benchAggregate         | 0             | 1    | 10  | 2,654,696b | 0.002s    | 0.002s    | 0.002s    | 0.002s    | 0.000s    | 2.97%  | 10,747.16x  |
| ReportBench     | benchDefault           | 0             | 1    | 10  | 2,654,696b | 0.002s    | 0.002s    | 0.002s    | 0.002s    | 0.000s    | 6.09%  | 10,644.29x  |
| ReportBench     | benchEnv               | 0             | 1    | 10  | 2,654,696b | 0.002s    | 0.002s    | 0.002s    | 0.002s    | 0.000s    | 4.99%  | 11,429.34x  |
+-----------------+------------------------+---------------+------+-----+------------+-----------+-----------+-----------+-----------+-----------+--------+-------------+

```

apple default php 7.3.11 
```sh
PhpBench @git_tag@. Running benchmarks.
Using configuration file: /opt/web/bench/phpbench.json.dist

\PhpBench\Benchmarks\Micro\HashingBench

    benchAlgos # 0..........................I9 [μ Mo]/r: 0.246 0.242 (μs) [μSD μRSD]/r: 0.013μs 5.18%
    benchAlgos # 1..........................I9 [μ Mo]/r: 0.455 0.436 (μs) [μSD μRSD]/r: 0.055μs 12.13%

\PhpBench\Micro\Math\KdeBench

    benchKde # ten points...................I9 [μ Mo]/r: 0.0250 0.0246 (ms) [μSD μRSD]/r: 0.001ms 2.36%
    benchKde # twenty points................I9 [μ Mo]/r: 0.0474 0.0464 (ms) [μSD μRSD]/r: 0.002ms 4.83%
    benchKde # forty points.................I9 [μ Mo]/r: 0.0834 0.0822 (ms) [μSD μRSD]/r: 0.003ms 3.22%

\PhpBench\Micro\Math\StatisticsBench

    benchVariance...........................I9 [μ Mo]/r: 0.83 0.82 (μs) [μSD μRSD]/r: 0.038μs 4.59%
    benchStDev..............................I9 [μ Mo]/r: 0.88 0.89 (μs) [μSD μRSD]/r: 0.014μs 1.53%

\PhpBench\Benchmarks\Micro\DependencyInjection\ContainerBench

    benchInitNoExtensions...................I9 [μ Mo]/r: 0.000024 0.000022 (s) [μSD μRSD]/r: 0.000s 30.15%
    benchInitCoreExtension..................I9 [μ Mo]/r: 0.000160 0.000155 (s) [μSD μRSD]/r: 0.000s 8.28%

\PhpBench\Benchmarks\Macro\LogBench

    benchLog................................I9 [μ Mo]/r: 0.012 0.012 (s) [μSD μRSD]/r: 0.000s 2.25%

\PhpBench\Benchmarks\Macro\benchmarks\NothingBench

    benchNothing............................I0 [μ Mo]/r: 3.000 3.000 (μs) [μSD μRSD]/r: 0.000μs 0.00%

\PhpBench\Benchmarks\Macro\RunBench

    benchRun................................I9 [μ Mo]/r: 0.236 0.236 (s) [μSD μRSD]/r: 0.002s 0.71%
    benchRunAndReport.......................I9 [μ Mo]/r: 0.237 0.236 (s) [μSD μRSD]/r: 0.003s 1.17%

\PhpBench\Benchmarks\Macro\ReportBench

    benchAggregate..........................I9 [μ Mo]/r: 0.003 0.002 (s) [μSD μRSD]/r: 0.000s 8.43%
    benchDefault............................I9 [μ Mo]/r: 0.002 0.002 (s) [μSD μRSD]/r: 0.000s 9.81%
    benchEnv................................I9 [μ Mo]/r: 0.003 0.002 (s) [μSD μRSD]/r: 0.000s 5.41%

13 subjects, 151 iterations, 2,527 revs, 0 rejects, 0 failures, 0 warnings
(best [mean mode] worst) = 0.240 [30,825.592 30,746.039] 0.284 (μs)
⅀T: 4,932,067.766μs μSD/r 333.671μs μRSD/r: 6.253%
suite: 1343b0d7d652e51424545531c8deab97c162832b, date: 2020-02-05, stime: 13:52:49
+-----------------+------------------------+---------------+------+-----+------------+-----------+-----------+-----------+-----------+-----------+--------+-------------+
| benchmark       | subject                | set           | revs | its | mem_peak   | best      | mean      | mode      | worst     | stdev     | rstdev | diff        |
+-----------------+------------------------+---------------+------+-----+------------+-----------+-----------+-----------+-----------+-----------+--------+-------------+
| HashingBench    | benchAlgos             | 0             | 1000 | 10  | 1,115,264b | 0.240μs   | 0.246μs   | 0.242μs   | 0.284μs   | 0.013μs   | 5.18%  | 1.00x       |
| HashingBench    | benchAlgos             | 1             | 1000 | 10  | 1,115,264b | 0.433μs   | 0.455μs   | 0.436μs   | 0.620μs   | 0.055μs   | 12.13% | 1.85x       |
| KdeBench        | benchKde               | ten points    | 100  | 10  | 1,176,520b | 0.0244ms  | 0.0250ms  | 0.0246ms  | 0.0260ms  | 0.0006ms  | 2.36%  | 101.55x     |
| KdeBench        | benchKde               | twenty points | 100  | 10  | 1,181,000b | 0.0449ms  | 0.0474ms  | 0.0464ms  | 0.0526ms  | 0.0023ms  | 4.83%  | 192.61x     |
| KdeBench        | benchKde               | forty points  | 100  | 10  | 1,189,960b | 0.0801ms  | 0.0834ms  | 0.0822ms  | 0.0884ms  | 0.0027ms  | 3.22%  | 339.28x     |
| StatisticsBench | benchVariance          | 0             | 100  | 10  | 1,130,680b | 0.80μs    | 0.83μs    | 0.82μs    | 0.94μs    | 0.04μs    | 4.59%  | 3.37x       |
| StatisticsBench | benchStDev             | 0             | 100  | 10  | 1,130,680b | 0.86μs    | 0.88μs    | 0.89μs    | 0.90μs    | 0.01μs    | 1.53%  | 3.59x       |
| ContainerBench  | benchInitNoExtensions  | 0             | 10   | 10  | 1,139,104b | 0.000021s | 0.000024s | 0.000022s | 0.000047s | 0.000007s | 30.15% | 99.51x      |
| ContainerBench  | benchInitCoreExtension | 0             | 10   | 10  | 1,771,912b | 0.000153s | 0.000160s | 0.000155s | 0.000198s | 0.000013s | 8.28%  | 651.20x     |
| LogBench        | benchLog               | 0             | 1    | 10  | 5,092,536b | 0.012s    | 0.012s    | 0.012s    | 0.013s    | 0.000s    | 2.25%  | 50,005.69x  |
| NothingBench    | benchNothing           | 0             | 1    | 1   | 1,114,856b | 3.000μs   | 3.000μs   | 3.000μs   | 3.000μs   | 0.000μs   | 0.00%  | 12.20x      |
| RunBench        | benchRun               | 0             | 1    | 10  | 4,913,160b | 0.233s    | 0.236s    | 0.236s    | 0.239s    | 0.002s    | 0.71%  | 960,387.96x |
| RunBench        | benchRunAndReport      | 0             | 1    | 10  | 5,338,536b | 0.234s    | 0.237s    | 0.236s    | 0.243s    | 0.003s    | 1.17%  | 963,246.85x |
| ReportBench     | benchAggregate         | 0             | 1    | 10  | 3,878,936b | 0.002s    | 0.003s    | 0.002s    | 0.003s    | 0.000s    | 8.43%  | 10,305.00x  |
| ReportBench     | benchDefault           | 0             | 1    | 10  | 3,867,120b | 0.002s    | 0.002s    | 0.002s    | 0.003s    | 0.000s    | 9.81%  | 9,976.41x   |
| ReportBench     | benchEnv               | 0             | 1    | 10  | 3,675,576b | 0.002s    | 0.003s    | 0.002s    | 0.003s    | 0.000s    | 5.41%  | 10,403.82x  |
+-----------------+------------------------+---------------+------+-----+------------+-----------+-----------+-----------+-----------+-----------+--------+-------------+

```

