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
PhpBench 0.17.0 Running benchmarks.
Using configuration file: /opt/web/bench/phpbench.json.dist

\PhpBench\Benchmarks\Micro\HashingBench

    benchAlgos # 0..........................I9 [μ Mo]/r: 0.255 0.242 (μs) [μSD μRSD]/r: 0.039μs 15.47%
    benchAlgos # 1..........................I9 [μ Mo]/r: 0.460 0.437 (μs) [μSD μRSD]/r: 0.053μs 11.42%

\PhpBench\Micro\Math\KdeBench

    benchKde # ten points...................I9 [μ Mo]/r: 0.0256 0.0248 (ms) [μSD μRSD]/r: 0.002ms 6.13%
    benchKde # twenty points................I9 [μ Mo]/r: 0.0471 0.0461 (ms) [μSD μRSD]/r: 0.003ms 5.70%
    benchKde # forty points.................I9 [μ Mo]/r: 0.0812 0.0811 (ms) [μSD μRSD]/r: 0.001ms 0.89%

\PhpBench\Micro\Math\StatisticsBench

    benchVariance...........................I9 [μ Mo]/r: 0.84 0.81 (μs) [μSD μRSD]/r: 0.094μs 11.20%
    benchStDev..............................I9 [μ Mo]/r: 0.87 0.86 (μs) [μSD μRSD]/r: 0.019μs 2.15%

\PhpBench\Benchmarks\Micro\DependencyInjection\ContainerBench

    benchInitNoExtensions...................I9 [μ Mo]/r: 0.000021 0.000021 (s) [μSD μRSD]/r: 0.000s 2.35%
    benchInitCoreExtension..................I9 [μ Mo]/r: 0.000158 0.000151 (s) [μSD μRSD]/r: 0.000s 5.39%

\PhpBench\Benchmarks\Macro\LogBench

    benchLog................................I9 [μ Mo]/r: 0.012 0.012 (s) [μSD μRSD]/r: 0.000s 0.94%

\PhpBench\Benchmarks\Macro\benchmarks\NothingBench

    benchNothing............................I0 [μ Mo]/r: 2.000 2.000 (μs) [μSD μRSD]/r: 0.000μs 0.00%

\PhpBench\Benchmarks\Macro\RunBench

    benchRun................................I9 [μ Mo]/r: 0.239 0.236 (s) [μSD μRSD]/r: 0.006s 2.61%
    benchRunAndReport.......................I9 [μ Mo]/r: 0.241 0.237 (s) [μSD μRSD]/r: 0.012s 5.14%

\PhpBench\Benchmarks\Macro\ReportBench

    benchAggregate..........................I9 [μ Mo]/r: 0.003 0.002 (s) [μSD μRSD]/r: 0.000s 11.03%
    benchDefault............................I9 [μ Mo]/r: 0.002 0.002 (s) [μSD μRSD]/r: 0.000s 13.11%
    benchEnv................................I9 [μ Mo]/r: 0.002 0.002 (s) [μSD μRSD]/r: 0.000s 2.84%

13 subjects, 151 iterations, 2,527 revs, 0 rejects, 0 failures, 0 warnings
(best [mean mode] worst) = 0.240 [31,228.953 30,751.085] 0.373 (μs)
⅀T: 4,996,614.431μs μSD/r 1,212.840μs μRSD/r: 6.022%
suite: 1343b0df77311386f83e5da28cb3d9c77065e376, date: 2020-02-05, stime: 11:14:54
+-----------------+------------------------+---------------+------+-----+------------+-----------+-----------+-----------+-----------+-----------+--------+-------------+
| benchmark       | subject                | set           | revs | its | mem_peak   | best      | mean      | mode      | worst     | stdev     | rstdev | diff        |
+-----------------+------------------------+---------------+------+-----+------------+-----------+-----------+-----------+-----------+-----------+--------+-------------+
| HashingBench    | benchAlgos             | 0             | 1000 | 10  | 1,117,608b | 0.240μs   | 0.255μs   | 0.242μs   | 0.373μs   | 0.039μs   | 15.47% | 1.00x       |
| HashingBench    | benchAlgos             | 1             | 1000 | 10  | 1,117,608b | 0.434μs   | 0.460μs   | 0.437μs   | 0.602μs   | 0.053μs   | 11.42% | 1.80x       |
| KdeBench        | benchKde               | ten points    | 100  | 10  | 1,178,864b | 0.0244ms  | 0.0256ms  | 0.0248ms  | 0.0295ms  | 0.0016ms  | 6.13%  | 100.27x     |
| KdeBench        | benchKde               | twenty points | 100  | 10  | 1,183,344b | 0.0451ms  | 0.0471ms  | 0.0461ms  | 0.0544ms  | 0.0027ms  | 5.70%  | 184.73x     |
| KdeBench        | benchKde               | forty points  | 100  | 10  | 1,192,304b | 0.0803ms  | 0.0812ms  | 0.0811ms  | 0.0829ms  | 0.0007ms  | 0.89%  | 318.40x     |
| StatisticsBench | benchVariance          | 0             | 100  | 10  | 1,133,024b | 0.79μs    | 0.84μs    | 0.81μs    | 1.12μs    | 0.09μs    | 11.20% | 3.30x       |
| StatisticsBench | benchStDev             | 0             | 100  | 10  | 1,133,024b | 0.85μs    | 0.87μs    | 0.86μs    | 0.91μs    | 0.02μs    | 2.15%  | 3.41x       |
| ContainerBench  | benchInitNoExtensions  | 0             | 10   | 10  | 1,141,448b | 0.000021s | 0.000021s | 0.000021s | 0.000022s | 0.000001s | 2.35%  | 83.58x      |
| ContainerBench  | benchInitCoreExtension | 0             | 10   | 10  | 1,774,256b | 0.000150s | 0.000158s | 0.000151s | 0.000171s | 0.000009s | 5.39%  | 619.64x     |
| LogBench        | benchLog               | 0             | 1    | 10  | 5,095,192b | 0.012s    | 0.012s    | 0.012s    | 0.012s    | 0.000s    | 0.94%  | 46,265.78x  |
| NothingBench    | benchNothing           | 0             | 1    | 1   | 1,117,200b | 2.000μs   | 2.000μs   | 2.000μs   | 2.000μs   | 0.000μs   | 0.00%  | 7.84x       |
| RunBench        | benchRun               | 0             | 1    | 10  | 4,915,952b | 0.231s    | 0.239s    | 0.236s    | 0.249s    | 0.006s    | 2.61%  | 937,317.91x |
| RunBench        | benchRunAndReport      | 0             | 1    | 10  | 5,341,328b | 0.232s    | 0.241s    | 0.237s    | 0.277s    | 0.012s    | 5.14%  | 944,517.05x |
| ReportBench     | benchAggregate         | 0             | 1    | 10  | 3,881,448b | 0.002s    | 0.003s    | 0.002s    | 0.003s    | 0.000s    | 11.03% | 10,122.30x  |
| ReportBench     | benchDefault           | 0             | 1    | 10  | 3,869,632b | 0.002s    | 0.002s    | 0.002s    | 0.003s    | 0.000s    | 13.11% | 9,438.26x   |
| ReportBench     | benchEnv               | 0             | 1    | 10  | 3,678,088b | 0.002s    | 0.002s    | 0.002s    | 0.003s    | 0.000s    | 2.84%  | 9,710.31x   |
+-----------------+------------------------+---------------+------+-----+------------+-----------+-----------+-----------+-----------+-----------+--------+-------------+

```

