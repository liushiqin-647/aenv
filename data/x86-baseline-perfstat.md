# perf_stat 指标汇总（x86 AMD Zen5）

> 采集工具：perf stat -e task-clock,instructions,cycles,context-switches,cpu-migrations,page-faults,minor-faults,major-faults
> CPU：AMD EPYC 9755 128-Core Processor
> Kernel：6.6.0-132.0.0.111.oe2403.x86_64
> 版本：dep_21-1.99.0（AgentENV v0.2.3, Rust 1.99.0）
> 数据来源：E:\results\perf_stat\<场景>\dep_21-1.99.0_20261104_*.txt

> **注**：x86 镜像解析（ImageResolver::resolve）网络等待 ~83s 膨胀了 time elapsed。
> 以下 4 项因分母含 time elapsed 而**不可用，已忽略**：
> ~~CPUs utilized~~、~~context-switches /sec~~、~~cpu-migrations /sec~~、~~time elapsed~~
> 其余 12 项为硬件/软件计数器原始值或基于 CPU 时间的派生值，不受影响。

| 指标 | snapshot_creation | snapshot_creation_1gdisk | snapshot_creation_1gmem | snapshot_resume | snapshot_resume_cold | concurrent_resume |
|------|:---:|:---:|:---:|:---:|:---:|:---:|
| **task-clock (msec)** | 2,015.04 | 6,135.69 | 6,398.04 | 1,066.58 | 946.89 | 11,096.55 |
| ~~CPUs utilized~~ | — | — | — | — | — | — |
| **instructions** | 4,671,645,176 | 25,347,207,943 | 19,365,503,679 | 5,519,500,108 | 4,404,663,456 | 38,548,517,976 |
| **insn per cycle (IPC)** | 1.13 | 1.44 | 1.20 | 1.55 | 1.43 | 0.94 |
| **cycles** | 4,149,985,914 | 17,644,679,992 | 16,172,284,574 | 3,553,949,005 | 3,081,752,405 | 40,935,919,372 |
| **GHz** | 2.060 | 2.876 | 2.528 | 3.332 | 3.255 | 3.689 |
| **context-switches** | 8,907 | 145,747 | 10,093 | 7,354 | 6,278 | 98,736 |
| ~~context-switches /sec~~ | — | — | — | — | — | — |
| **cpu-migrations** | 546 | 921 | 587 | 550 | 409 | 21,446 |
| ~~cpu-migrations /sec~~ | — | — | — | — | — | — |
| **page-faults** | 16,044 | 16,646 | 19,247 | 42,244 | 28,909 | 313,348 |
| **minor-faults** | 16,044 | 16,642 | 19,246 | 42,227 | 28,860 | 313,176 |
| **major-faults** | 0 | 0 | 0 | 15 | 47 | 75 |
| ~~time elapsed (sec)~~ | — | — | — | — | — | — |
| **user time (sec)** | 1.354 | 2.086 | 3.611 | 0.299 | 0.249 | 2.296 |
| **sys time (sec)** | 0.633 | 2.557 | 2.779 | 0.735 | 0.593 | 10.109 |

# 4 项忽略（time elapsed、CPUs utilized、context-switches /sec、cpu-migrations /sec）