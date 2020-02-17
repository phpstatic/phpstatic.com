https://github.com/phpbench/phpbench.git macOS 10.15.3

php-static-7.3.14
```sh
PhpBench @git_tag@. Running benchmarks.
Using configuration file: /opt/web/bench/phpbench.json.dist

\PhpBench\Benchmarks\Micro\HashingBench

    benchAlgos # 0..........................I9 [μ Mo]/r: 0.200 0.200 (μs) [μSD μRSD]/r: 0.003μs 1.67%
    benchAlgos # 1..........................I9 [μ Mo]/r: 0.413 0.411 (μs) [μSD μRSD]/r: 0.005μs 1.21%

\PhpBench\Micro\Math\KdeBench

    benchKde # ten points...................I9 [μ Mo]/r: 0.0230 0.0229 (ms) [μSD μRSD]/r: 0.000ms 1.61%
    benchKde # twenty points................I9 [μ Mo]/r: 0.0417 0.0416 (ms) [μSD μRSD]/r: 0.000ms 0.83%
    benchKde # forty points.................I9 [μ Mo]/r: 0.0742 0.0738 (ms) [μSD μRSD]/r: 0.001ms 1.09%

\PhpBench\Micro\Math\StatisticsBench

    benchVariance...........................I9 [μ Mo]/r: 0.74 0.73 (μs) [μSD μRSD]/r: 0.033μs 4.48%
    benchStDev..............................I9 [μ Mo]/r: 0.76 0.76 (μs) [μSD μRSD]/r: 0.014μs 1.89%

\PhpBench\Benchmarks\Micro\DependencyInjection\ContainerBench

    benchInitNoExtensions...................I9 [μ Mo]/r: 0.000013 0.000013 (s) [μSD μRSD]/r: 0.000s 2.41%
    benchInitCoreExtension..................I9 [μ Mo]/r: 0.000121 0.000119 (s) [μSD μRSD]/r: 0.000s 4.70%

\PhpBench\Benchmarks\Macro\LogBench

    benchLog................................I9 [μ Mo]/r: 0.012 0.012 (s) [μSD μRSD]/r: 0.000s 1.67%

\PhpBench\Benchmarks\Macro\benchmarks\NothingBench

    benchNothing............................I0 [μ Mo]/r: 0.010 0.010 (μs) [μSD μRSD]/r: 0.000μs 0.00%

\PhpBench\Benchmarks\Macro\RunBench

    benchRun................................I9 [μ Mo]/r: 0.108 0.108 (s) [μSD μRSD]/r: 0.002s 1.48%
    benchRunAndReport.......................I9 [μ Mo]/r: 0.110 0.110 (s) [μSD μRSD]/r: 0.001s 0.86%

\PhpBench\Benchmarks\Macro\ReportBench

    benchAggregate..........................I9 [μ Mo]/r: 0.002 0.002 (s) [μSD μRSD]/r: 0.000s 3.27%
    benchDefault............................I9 [μ Mo]/r: 0.002 0.002 (s) [μSD μRSD]/r: 0.000s 5.18%
    benchEnv................................I9 [μ Mo]/r: 0.002 0.002 (s) [μSD μRSD]/r: 0.000s 3.13%

13 subjects, 151 iterations, 2,726 revs, 0 rejects, 0 failures, 0 warnings
(best [mean mode] worst) = 0.010 [14,820.096 14,818.586] 0.010 (μs)
⅀T: 2,371,215.311μs μSD/r 188.375μs μRSD/r: 2.218%
suite: 1343b1920edd6b59813440dabbb3a7973a26bf55, date: 2020-02-17, stime: 00:38:45
+-----------------+------------------------+---------------+------+-----+------------+-----------+-----------+-----------+-----------+-----------+--------+----------------+
| benchmark       | subject                | set           | revs | its | mem_peak   | best      | mean      | mode      | worst     | stdev     | rstdev | diff           |
+-----------------+------------------------+---------------+------+-----+------------+-----------+-----------+-----------+-----------+-----------+--------+----------------+
| HashingBench    | benchAlgos             | 0             | 1000 | 10  | 3,049,864b | 0.194μs   | 0.200μs   | 0.200μs   | 0.206μs   | 0.003μs   | 1.67%  | 19.98x         |
| HashingBench    | benchAlgos             | 1             | 1000 | 10  | 3,049,864b | 0.407μs   | 0.413μs   | 0.411μs   | 0.422μs   | 0.005μs   | 1.21%  | 41.33x         |
| KdeBench        | benchKde               | ten points    | 100  | 10  | 3,050,144b | 0.0227ms  | 0.0230ms  | 0.0229ms  | 0.0240ms  | 0.0004ms  | 1.61%  | 2,299.20x      |
| KdeBench        | benchKde               | twenty points | 100  | 10  | 3,050,144b | 0.0412ms  | 0.0417ms  | 0.0416ms  | 0.0424ms  | 0.0003ms  | 0.83%  | 4,172.50x      |
| KdeBench        | benchKde               | forty points  | 100  | 10  | 3,050,144b | 0.0736ms  | 0.0742ms  | 0.0738ms  | 0.0763ms  | 0.0008ms  | 1.09%  | 7,415.40x      |
| StatisticsBench | benchVariance          | 0             | 100  | 10  | 3,048,528b | 0.69μs    | 0.74μs    | 0.73μs    | 0.82μs    | 0.03μs    | 4.48%  | 74.00x         |
| StatisticsBench | benchStDev             | 0             | 100  | 10  | 3,048,528b | 0.72μs    | 0.76μs    | 0.76μs    | 0.77μs    | 0.01μs    | 1.89%  | 75.60x         |
| ContainerBench  | benchInitNoExtensions  | 0             | 10   | 10  | 3,048,168b | 0.000012s | 0.000013s | 0.000013s | 0.000013s | 0.000000s | 2.41%  | 1,289.00x      |
| ContainerBench  | benchInitCoreExtension | 0             | 10   | 10  | 3,048,168b | 0.000115s | 0.000121s | 0.000119s | 0.000136s | 0.000006s | 4.70%  | 12,056.00x     |
| LogBench        | benchLog               | 0             | 1    | 10  | 6,340,856b | 0.011s    | 0.012s    | 0.012s    | 0.012s    | 0.000s    | 1.67%  | 1,175,570.00x  |
| NothingBench    | benchNothing           | 0             | 200  | 1   | 3,048,136b | 0.010μs   | 0.010μs   | 0.010μs   | 0.010μs   | 0.000μs   | 0.00%  | 1.00x          |
| RunBench        | benchRun               | 0             | 1    | 10  | 6,037,928b | 0.105s    | 0.108s    | 0.108s    | 0.111s    | 0.002s    | 1.48%  | 10,828,110.00x |
| RunBench        | benchRunAndReport      | 0             | 1    | 10  | 6,393,576b | 0.108s    | 0.110s    | 0.110s    | 0.111s    | 0.001s    | 0.86%  | 10,986,440.00x |
| ReportBench     | benchAggregate         | 0             | 1    | 10  | 4,893,464b | 0.002s    | 0.002s    | 0.002s    | 0.003s    | 0.000s    | 3.27%  | 231,720.00x    |
| ReportBench     | benchDefault           | 0             | 1    | 10  | 4,883,024b | 0.002s    | 0.002s    | 0.002s    | 0.002s    | 0.000s    | 5.18%  | 221,650.00x    |
| ReportBench     | benchEnv               | 0             | 1    | 10  | 4,765,312b | 0.002s    | 0.002s    | 0.002s    | 0.003s    | 0.000s    | 3.13%  | 241,220.00x    |
+-----------------+------------------------+---------------+------+-----+------------+-----------+-----------+-----------+-----------+-----------+--------+----------------+
```

apple php PHP 7.3.11 

```sh
./run.sh /usr/bin/php
PhpBench @git_tag@. Running benchmarks.
Using configuration file: /opt/web/bench/phpbench.json.dist

\PhpBench\Benchmarks\Micro\HashingBench

    benchAlgos # 0..........................I9 [μ Mo]/r: 0.257 0.256 (μs) [μSD μRSD]/r: 0.002μs 0.92%
    benchAlgos # 1..........................I9 [μ Mo]/r: 0.468 0.464 (μs) [μSD μRSD]/r: 0.009μs 1.86%

\PhpBench\Micro\Math\KdeBench

    benchKde # ten points...................I9 [μ Mo]/r: 0.0268 0.0268 (ms) [μSD μRSD]/r: 0.000ms 0.45%
    benchKde # twenty points................I9 [μ Mo]/r: 0.0494 0.0496 (ms) [μSD μRSD]/r: 0.001ms 1.14%
    benchKde # forty points.................I9 [μ Mo]/r: 0.0900 0.0877 (ms) [μSD μRSD]/r: 0.007ms 7.47%

\PhpBench\Micro\Math\StatisticsBench

    benchVariance...........................I9 [μ Mo]/r: 0.88 0.88 (μs) [μSD μRSD]/r: 0.016μs 1.81%
    benchStDev..............................I9 [μ Mo]/r: 0.98 0.95 (μs) [μSD μRSD]/r: 0.084μs 8.61%

\PhpBench\Benchmarks\Micro\DependencyInjection\ContainerBench

    benchInitNoExtensions...................I9 [μ Mo]/r: 0.000020 0.000020 (s) [μSD μRSD]/r: 0.000s 4.66%
    benchInitCoreExtension..................I9 [μ Mo]/r: 0.000149 0.000147 (s) [μSD μRSD]/r: 0.000s 2.14%

\PhpBench\Benchmarks\Macro\LogBench

    benchLog................................I9 [μ Mo]/r: 0.013 0.013 (s) [μSD μRSD]/r: 0.000s 1.95%

\PhpBench\Benchmarks\Macro\benchmarks\NothingBench

    benchNothing............................I0 [μ Mo]/r: 0.035 0.035 (μs) [μSD μRSD]/r: 0.000μs 0.00%

\PhpBench\Benchmarks\Macro\RunBench

    benchRun................................I9 [μ Mo]/r: 0.251 0.249 (s) [μSD μRSD]/r: 0.005s 2.11%
    benchRunAndReport.......................I9 [μ Mo]/r: 0.246 0.245 (s) [μSD μRSD]/r: 0.002s 0.64%

\PhpBench\Benchmarks\Macro\ReportBench

    benchAggregate..........................I9 [μ Mo]/r: 0.003 0.003 (s) [μSD μRSD]/r: 0.000s 1.46%
    benchDefault............................I9 [μ Mo]/r: 0.002 0.002 (s) [μSD μRSD]/r: 0.000s 8.01%
    benchEnv................................I9 [μ Mo]/r: 0.003 0.003 (s) [μSD μRSD]/r: 0.000s 1.53%

13 subjects, 151 iterations, 2,726 revs, 0 rejects, 0 failures, 0 warnings
(best [mean mode] worst) = 0.035 [32,387.692 32,234.895] 0.035 (μs)
⅀T: 5,182,030.367μs μSD/r 463.592μs μRSD/r: 2.798%
suite: 1343b190ebd290985ffe50a246c2af84e6a3359a, date: 2020-02-17, stime: 00:42:13
+-----------------+------------------------+---------------+------+-----+------------+-----------+-----------+-----------+-----------+-----------+--------+---------------+
| benchmark       | subject                | set           | revs | its | mem_peak   | best      | mean      | mode      | worst     | stdev     | rstdev | diff          |
+-----------------+------------------------+---------------+------+-----+------------+-----------+-----------+-----------+-----------+-----------+--------+---------------+
| HashingBench    | benchAlgos             | 0             | 1000 | 10  | 2,149,464b | 0.255μs   | 0.257μs   | 0.256μs   | 0.262μs   | 0.002μs   | 0.92%  | 7.35x         |
| HashingBench    | benchAlgos             | 1             | 1000 | 10  | 2,149,464b | 0.462μs   | 0.468μs   | 0.464μs   | 0.491μs   | 0.009μs   | 1.86%  | 13.37x        |
| KdeBench        | benchKde               | ten points    | 100  | 10  | 2,149,744b | 0.0267ms  | 0.0268ms  | 0.0268ms  | 0.0270ms  | 0.0001ms  | 0.45%  | 766.37x       |
| KdeBench        | benchKde               | twenty points | 100  | 10  | 2,149,744b | 0.0483ms  | 0.0494ms  | 0.0496ms  | 0.0501ms  | 0.0006ms  | 1.14%  | 1,412.31x     |
| KdeBench        | benchKde               | forty points  | 100  | 10  | 2,149,744b | 0.0858ms  | 0.0900ms  | 0.0877ms  | 0.1097ms  | 0.0067ms  | 7.47%  | 2,570.71x     |
| StatisticsBench | benchVariance          | 0             | 100  | 10  | 2,148,128b | 0.86μs    | 0.88μs    | 0.88μs    | 0.91μs    | 0.02μs    | 1.81%  | 25.20x        |
| StatisticsBench | benchStDev             | 0             | 100  | 10  | 2,148,128b | 0.92μs    | 0.98μs    | 0.95μs    | 1.22μs    | 0.08μs    | 8.61%  | 27.91x        |
| ContainerBench  | benchInitNoExtensions  | 0             | 10   | 10  | 2,147,768b | 0.000019s | 0.000020s | 0.000020s | 0.000023s | 0.000001s | 4.66%  | 581.14x       |
| ContainerBench  | benchInitCoreExtension | 0             | 10   | 10  | 2,330,128b | 0.000145s | 0.000149s | 0.000147s | 0.000157s | 0.000003s | 2.14%  | 4,245.14x     |
| LogBench        | benchLog               | 0             | 1    | 10  | 5,645,784b | 0.013s    | 0.013s    | 0.013s    | 0.014s    | 0.000s    | 1.95%  | 382,022.86x   |
| NothingBench    | benchNothing           | 0             | 200  | 1   | 2,147,736b | 0.035μs   | 0.035μs   | 0.035μs   | 0.035μs   | 0.000μs   | 0.00%  | 1.00x         |
| RunBench        | benchRun               | 0             | 1    | 10  | 5,515,792b | 0.246s    | 0.251s    | 0.249s    | 0.265s    | 0.005s    | 2.11%  | 7,174,488.57x |
| RunBench        | benchRunAndReport      | 0             | 1    | 10  | 5,941,168b | 0.243s    | 0.246s    | 0.245s    | 0.249s    | 0.002s    | 0.64%  | 7,022,771.43x |
| ReportBench     | benchAggregate         | 0             | 1    | 10  | 4,436,808b | 0.002s    | 0.003s    | 0.003s    | 0.003s    | 0.000s    | 1.46%  | 72,400.00x    |
| ReportBench     | benchDefault           | 0             | 1    | 10  | 4,424,992b | 0.002s    | 0.002s    | 0.002s    | 0.003s    | 0.000s    | 8.01%  | 71,171.43x    |
| ReportBench     | benchEnv               | 0             | 1    | 10  | 4,233,448b | 0.003s    | 0.003s    | 0.003s    | 0.003s    | 0.000s    | 1.53%  | 73,297.14x    |
+-----------------+------------------------+---------------+------+-----+------------+-----------+-----------+-----------+-----------+-----------+--------+---------------+
```
