test environment：macOS 10.15.3, I7-7700K

php-static-7.3.14 
```sh
PhpBench 0.17.0 Running benchmarks.
\PhpBench\Benchmarks\Micro\HashingBench

    benchAlgos # 0..........................I9 [μ Mo]/r: 0.189 0.190 (μs) [μSD μRSD]/r: 0.001μs 0.60%
    benchAlgos # 1..........................I9 [μ Mo]/r: 0.396 0.396 (μs) [μSD μRSD]/r: 0.001μs 0.24%

\PhpBench\Micro\Math\KdeBench

    benchKde # ten points...................I9 [μ Mo]/r: 0.0212 0.0209 (ms) [μSD μRSD]/r: 0.001ms 3.66%
    benchKde # twenty points................I9 [μ Mo]/r: 0.0376 0.0372 (ms) [μSD μRSD]/r: 0.001ms 1.55%
    benchKde # forty points.................I9 [μ Mo]/r: 0.0672 0.0667 (ms) [μSD μRSD]/r: 0.001ms 1.07%

\PhpBench\Micro\Math\StatisticsBench

    benchVariance...........................I9 [μ Mo]/r: 0.70 0.69 (μs) [μSD μRSD]/r: 0.024μs 3.43%
    benchStDev..............................I9 [μ Mo]/r: 0.76 0.75 (μs) [μSD μRSD]/r: 0.019μs 2.56%

\PhpBench\Benchmarks\Micro\DependencyInjection\ContainerBench

    benchInitNoExtensions...................I9 [μ Mo]/r: 0.000013 0.000013 (s) [μSD μRSD]/r: 0.000s 7.03%
    benchInitCoreExtension..................I9 [μ Mo]/r: 0.000123 0.000120 (s) [μSD μRSD]/r: 0.000s 6.00%

\PhpBench\Benchmarks\Macro\LogBench

    benchLog................................I9 [μ Mo]/r: 0.011 0.011 (s) [μSD μRSD]/r: 0.000s 1.59%

\PhpBench\Benchmarks\Macro\benchmarks\NothingBench

    benchNothing............................I0 [μ Mo]/r: 1.000 1.000 (μs) [μSD μRSD]/r: 0.000μs 0.00%

\PhpBench\Benchmarks\Macro\RunBench

    benchRun................................I9 [μ Mo]/r: 0.104 0.103 (s) [μSD μRSD]/r: 0.002s 1.57%
    benchRunAndReport.......................I9 [μ Mo]/r: 0.104 0.103 (s) [μSD μRSD]/r: 0.001s 0.72%

\PhpBench\Benchmarks\Macro\ReportBench

    benchAggregate..........................I9 [μ Mo]/r: 0.002 0.002 (s) [μSD μRSD]/r: 0.000s 5.05%
    benchDefault............................I9 [μ Mo]/r: 0.002 0.002 (s) [μSD μRSD]/r: 0.000s 3.68%
    benchEnv................................I9 [μ Mo]/r: 0.002 0.002 (s) [μSD μRSD]/r: 0.000s 2.61%

13 subjects, 151 iterations, 2,527 revs, 0 rejects, 0 failures, 0 warnings
(best [mean mode] worst) = 0.187 [14,066.545 13,990.617] 0.190 (μs)
⅀T: 2,250,638.140μs μSD/r 175.495μs μRSD/r: 2.586%
suite: 1343b0fa06d60e3095d7e5b526b55d5e9247b685, date: 2020-02-07, stime: 19:08:35
+-----------------+------------------------+---------------+------+-----+------------+-----------+-----------+-----------+-----------+-----------+--------+-------------+
| benchmark       | subject                | set           | revs | its | mem_peak   | best      | mean      | mode      | worst     | stdev     | rstdev | diff        |
+-----------------+------------------------+---------------+------+-----+------------+-----------+-----------+-----------+-----------+-----------+--------+-------------+
| HashingBench    | benchAlgos             | 0             | 1000 | 10  | 2,650,800b | 0.187μs   | 0.189μs   | 0.190μs   | 0.190μs   | 0.001μs   | 0.60%  | 1.00x       |
| HashingBench    | benchAlgos             | 1             | 1000 | 10  | 2,650,800b | 0.394μs   | 0.396μs   | 0.396μs   | 0.398μs   | 0.001μs   | 0.24%  | 2.10x       |
| KdeBench        | benchKde               | ten points    | 100  | 10  | 2,651,080b | 0.0207ms  | 0.0212ms  | 0.0209ms  | 0.0233ms  | 0.0008ms  | 3.66%  | 112.10x     |
| KdeBench        | benchKde               | twenty points | 100  | 10  | 2,651,080b | 0.0369ms  | 0.0376ms  | 0.0372ms  | 0.0388ms  | 0.0006ms  | 1.55%  | 198.85x     |
| KdeBench        | benchKde               | forty points  | 100  | 10  | 2,651,080b | 0.0665ms  | 0.0672ms  | 0.0667ms  | 0.0687ms  | 0.0007ms  | 1.07%  | 355.52x     |
| StatisticsBench | benchVariance          | 0             | 100  | 10  | 2,649,464b | 0.68μs    | 0.70μs    | 0.69μs    | 0.75μs    | 0.02μs    | 3.43%  | 3.73x       |
| StatisticsBench | benchStDev             | 0             | 100  | 10  | 2,649,464b | 0.73μs    | 0.76μs    | 0.75μs    | 0.80μs    | 0.02μs    | 2.56%  | 4.02x       |
| ContainerBench  | benchInitNoExtensions  | 0             | 10   | 10  | 2,649,104b | 0.000013s | 0.000013s | 0.000013s | 0.000016s | 0.000001s | 7.03%  | 69.93x      |
| ContainerBench  | benchInitCoreExtension | 0             | 10   | 10  | 2,936,576b | 0.000118s | 0.000123s | 0.000120s | 0.000143s | 0.000007s | 6.00%  | 651.99x     |
| LogBench        | benchLog               | 0             | 1    | 10  | 6,334,880b | 0.010s    | 0.011s    | 0.011s    | 0.011s    | 0.000s    | 1.59%  | 56,304.92x  |
| NothingBench    | benchNothing           | 0             | 1    | 1   | 2,649,072b | 1.000μs   | 1.000μs   | 1.000μs   | 1.000μs   | 0.000μs   | 0.00%  | 5.29x       |
| RunBench        | benchRun               | 0             | 1    | 10  | 5,925,784b | 0.102s    | 0.104s    | 0.103s    | 0.107s    | 0.002s    | 1.57%  | 548,296.45x |
| RunBench        | benchRunAndReport      | 0             | 1    | 10  | 6,887,392b | 0.103s    | 0.104s    | 0.103s    | 0.106s    | 0.001s    | 0.72%  | 548,955.53x |
| ReportBench     | benchAggregate         | 0             | 1    | 10  | 4,889,032b | 0.002s    | 0.002s    | 0.002s    | 0.003s    | 0.000s    | 5.05%  | 12,394.39x  |
| ReportBench     | benchDefault           | 0             | 1    | 10  | 4,877,088b | 0.002s    | 0.002s    | 0.002s    | 0.002s    | 0.000s    | 3.68%  | 11,632.61x  |
| ReportBench     | benchEnv               | 0             | 1    | 10  | 4,691,608b | 0.002s    | 0.002s    | 0.002s    | 0.002s    | 0.000s    | 2.61%  | 12,460.56x  |
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

