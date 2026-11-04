# perf_stat 指标汇总（ARM 鲲鹏）

> 采集工具：perf stat -e task-clock,instructions,cycles,context-switches,cpu-migrations,page-faults,minor-faults,major-faults
> 版本：dep_21-1.99.0（AgentENV v0.2.3, Rust 1.99.0）
> 架构：aarch64
> 数据来源：E:\arm-results\perf_stat\<场景>\dep_21-1.99.0_20261104_*.txt

| 指标 | snapshot_creation | snapshot_creation_1gdisk | snapshot_creation_1gmem | snapshot_resume | snapshot_resume_cold | concurrent_resume |
|------|:---:|:---:|:---:|:---:|:---:|:---:|
| **task-clock (msec)** | 2,738.48 | 12,452.86 | 11,186.85 | 1,426.16 | 1,434.14 | 19,928.52 |
| **CPUs utilized** | 0.371 | 0.997 | 0.696 | 0.160 | 0.184 | 0.844 |
| **instructions** | 6,095,990,610 | 29,700,478,481 | 29,543,537,681 | 4,639,266,773 | 4,682,155,613 | 39,804,956,823 |
| **insn per cycle (IPC)** | 1.25 | 1.22 | 1.73 | 1.55 | 1.53 | 1.06 |
| **cycles** | 4,865,343,285 | 24,370,770,366 | 17,115,762,329 | 3,001,767,603 | 3,056,988,325 | 37,525,848,315 |
| **GHz** | 1.777 | 1.957 | 1.530 | 2.105 | 2.132 | 1.883 |
| **context-switches** | 9,052 | 174,340 | 9,946 | 6,900 | 6,124 | 105,407 |
| **context-switches /sec** | 3,305 | 14,000 | 889 | 4,838 | 4,270 | 5,289 |
| **cpu-migrations** | 564 | 681 | 651 | 443 | 305 | 21,998 |
| **cpu-migrations /sec** | 205.953 | 54.686 | 58.193 | 310.624 | 212.671 | 1,104 |
| **page-faults** | 16,674 | 17,963 | 18,525 | 32,539 | 26,632 | 268,057 |
| **minor-faults** | 16,673 | 17,963 | 18,525 | 32,521 | 26,573 | 267,840 |
| **major-faults** | 1 | 0 | 0 | 11 | 53 | 104 |
| **time elapsed (sec)** | 7.382 | 12.494 | 16.081 | 8.905 | 7.787 | 23.620 |
| **user time (sec)** | 0.925 | 2.280 | 4.822 | 0.445 | 0.358 | 3.860 |
| **sys time (sec)** | 1.773 | 6.371 | 6.357 | 0.941 | 0.906 | 16.320 |

# 4 项忽略（time elapsed、CPUs utilized、context-switches /sec、cpu-migrations /sec）