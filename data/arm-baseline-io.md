## 3. iostat 磁盘 I/O 摘要（按场景）

### 3.1 snapshot_creation

| Device | r/s max | w/s max | rkB/s max | wkB/s max | r_await max (ms) | r_await avg (ms) | w_await max (ms) | w_await avg (ms) | aqu-sz max | %util max |
|---|---|---|---|---|---|---|---|---|---|---|
| dm-0 | 2.56 | 9.00 | 40.61 | 206.52 | 0.09 | 0.02 | 0.08 | 0.02 | — | 0.12 |
| dm-2 | 31.08 | 262.00 | 349.86 | 2,336.96 | 0.11 | 0.03 | 0.83 | 0.22 | 0.05 | 0.42 |
| ublkb1 | 37.50 | — | 6,406.00 | — | 0.28 | 0.14 | — | 0.00 | 0.01 | 0.20 |
| ublkb2 | 216.50 | 15.00 | 7,403.00 | 60.00 | 0.03 | 0.01 | — | 0.00 | 0.01 | 1.00 |
| nvme0n1 | 25.68 | 38.50 | 392.83 | 2,552.93 | 0.43 | 0.11 | 16.85 | 4.24 | 0.51 | 0.22 |

### 3.2 snapshot_creation_1gdisk

| Device | r/s max | w/s max | rkB/s max | wkB/s max | r_await max (ms) | r_await avg (ms) | w_await max (ms) | w_await avg (ms) | aqu-sz max | %util max |
|---|---|---|---|---|---|---|---|---|---|---|
| dm-0 | 2.56 | 23.00 | 40.61 | 206.52 | 0.09 | 0.01 | 0.08 | 0.01 | — | 0.12 |
| dm-2 | 31.08 | 188.00 | 349.86 | 35,764.00 | 0.11 | 0.02 | 0.83 | 0.13 | 0.05 | 0.42 |
| ublkb1 | 40.00 | — | 6,422.00 | — | 0.21 | 0.04 | — | 0.00 | 0.01 | — |
| ublkb2 | 392.50 | 5,494.50 | 6,422.50 | 1,220,824.00 | 0.12 | 0.06 | 0.38 | 0.28 | 1.79 | 50.60 |
| nvme0n1 | 25.68 | 337.00 | 392.83 | 35,808.00 | 0.43 | 0.06 | 16.85 | 2.64 | 0.51 | 0.22 |

### 3.3 snapshot_creation_1gmem

| Device | r/s max | w/s max | rkB/s max | wkB/s max | r_await max (ms) | r_await avg (ms) | w_await max (ms) | w_await avg (ms) | aqu-sz max | %util max |
|---|---|---|---|---|---|---|---|---|---|---|
| dm-0 | 2.56 | 25.00 | 40.61 | 206.52 | 0.09 | 0.01 | 1.20 | 0.14 | 0.03 | 0.20 |
| dm-2 | 31.08 | 87.50 | 349.86 | 2,336.99 | 0.11 | 0.01 | 0.83 | 0.09 | 0.05 | 0.42 |
| ublkb1 | 39.50 | — | 6,422.00 | — | 0.24 | 0.03 | — | 0.00 | 0.01 | — |
| ublkb2 | 289.00 | 5.00 | 2,907.00 | 20.00 | 0.04 | 0.03 | 0.10 | 0.01 | 0.01 | 0.40 |
| nvme0n1 | 25.68 | 29.33 | 392.83 | 2,552.95 | 0.43 | 0.05 | 16.85 | 1.90 | 0.51 | 0.22 |

### 3.4 snapshot_resume

| Device | r/s max | w/s max | rkB/s max | wkB/s max | r_await max (ms) | r_await avg (ms) | w_await max (ms) | w_await avg (ms) | aqu-sz max | %util max |
|---|---|---|---|---|---|---|---|---|---|---|
| dm-0 | 2.56 | 34.50 | 40.61 | 206.51 | 0.09 | 0.02 | 0.08 | 0.02 | — | 0.12 |
| dm-2 | 31.08 | 94.00 | 349.85 | 2,336.96 | 0.11 | 0.02 | 0.83 | 0.17 | 0.05 | 0.42 |
| ublkb1 | 39.00 | — | 6,418.00 | — | 0.22 | 0.11 | — | 0.00 | 0.01 | 0.40 |
| ublkb2 | 36.50 | 2.50 | 1,229.50 | 10.00 | 0.03 | 0.01 | — | 0.00 | — | 0.40 |
| nvme0n1 | 25.68 | 42.00 | 392.82 | 2,552.92 | 0.43 | 0.09 | 16.85 | 3.43 | 0.51 | 0.22 |
| ublkb3 | 184.50 | — | 18,482.00 | — | 0.05 | 0.03 | — | 0.00 | 0.01 | 0.20 |

### 3.5 snapshot_resume_cold

| Device | r/s max | w/s max | rkB/s max | wkB/s max | r_await max (ms) | r_await avg (ms) | w_await max (ms) | w_await avg (ms) | aqu-sz max | %util max |
|---|---|---|---|---|---|---|---|---|---|---|
| dm-0 | 2.56 | 20.50 | 40.61 | 206.51 | 0.09 | 0.02 | 0.08 | 0.02 | — | 0.12 |
| dm-2 | 31.08 | 97.00 | 349.85 | 4,274.00 | 0.11 | 0.03 | 0.83 | 0.28 | 0.05 | 0.42 |
| ublkb1 | 39.50 | — | 6,418.00 | — | 0.22 | 0.11 | — | 0.00 | 0.01 | — |
| ublkb2 | 36.50 | 2.50 | 1,229.50 | 10.00 | 0.03 | 0.01 | — | 0.00 | — | — |
| nvme0n1 | 25.68 | 63.00 | 392.82 | 4,346.00 | 0.43 | 0.11 | 16.85 | 4.41 | 0.51 | 0.22 |
| ublkb3 | 976.00 | — | 236,788.00 | — | 0.59 | 0.45 | — | 0.00 | 0.57 | 6.20 |

### 3.6 concurrent_resume

| Device | r/s max | w/s max | rkB/s max | wkB/s max | r_await max (ms) | r_await avg (ms) | w_await max (ms) | w_await avg (ms) | aqu-sz max | %util max |
|---|---|---|---|---|---|---|---|---|---|---|
| ublkb1 | 39.50 | — | 6,422.00 | — | 0.23 | 0.03 | — | 0.00 | 0.01 | 0.40 |
| ublkb2 | 197.00 | 10.50 | 1,229.50 | 80.00 | 0.08 | 0.02 | 0.43 | 0.04 | 0.01 | 0.20 |
| ublkb3 | 172.00 | — | 16,926.00 | — | 0.08 | 0.01 | — | 0.00 | 0.01 | 0.40 |
| nvme0n1 | 25.68 | 38.50 | 392.82 | 2,552.89 | 0.43 | 0.03 | 16.85 | 1.37 | 0.51 | 0.22 |
| dm-0 | 2.56 | 72.00 | 40.61 | 352.00 | 0.09 | 0.01 | 0.08 | 0.01 | — | 0.20 |
| dm-2 | 31.08 | 105.50 | 349.85 | 2,336.94 | 0.11 | 0.01 | 0.83 | 0.06 | 0.05 | 0.42 |

---

## 4. sar -B 内存分页摘要

| Scenario | pgpgin/s max | pgpgin/s avg | pgpgout/s max | pgpgout/s avg | fault/s max | majflt/s max |
|---|---|---|---|---|---|---|
| snapshot_creation | 13,809.00 | 4,605.67 | 1,158.00 | 479.33 | 22,052.00 | 0.00 |
| snapshot_creation_1gdisk | 8,195.50 | 4,351.50 | 2,270,804.00 | 1,200,195.00 | 26,188.00 | 0.00 |
| snapshot_creation_1gmem | 7,787.50 | 2,744.12 | 390.00 | 285.75 | 19,781.50 | 0.00 |
| snapshot_resume | 26,133.50 | 7,089.88 | 660.00 | 328.00 | 19,429.00 | 154.00 |
| snapshot_resume_cold | 236,788.00 | 97,155.83 | 4,346.00 | 1,670.67 | 19,083.50 | 164.00 |
| concurrent_resume | 24,681.50 | 2,626.79 | 702.00 | 270.50 | 178,096.50 | 149.00 |

---

## 5. x86 vs ARM 交叉对比

### 5.1 延迟对比

| Scenario | x86 Mean (ms) | ARM Mean (ms) | x86/ARM | 胜方 | x86 CV | ARM CV |
|---|---|---|---|---|---|---|
| snapshot_creation | 11.33 | 18.49 | 0.61x | x86 | ~3.2% | ~1.1% |
| snapshot_creation_1gdisk | 12.43 | 19.83 | 0.63x | x86 | ~2.3% | ~1.8% |
| snapshot_creation_1gmem | 131.43 | 269.58 | 0.49x | x86 | ~0.6% | ~0.4% |
| snapshot_resume | 70.13 | 53.18 | 1.32x | ARM | ~33% | ~46% |
| snapshot_resume_cold | 83.94 | 66.50 | 1.26x | ARM | ~20% | ~30% |
| concurrent_resume | 48.33 | 93.67 | 0.52x | x86 | ~42% | ~38% |

### 5.2 Cache miss 率对比

| Scenario | x86 miss% | ARM miss% | x86 cache-refs | ARM cache-refs | ARM/x86 cache-refs |
|---|---|---|---|---|---|
| snapshot_creation | 7.32% | 2.61% | 262.9M | 1,863.3M | 7.09x |
| snapshot_creation_1gdisk | 14.77% | 5.16% | 1,925.4M | 10,776.4M | 5.60x |
| snapshot_creation_1gmem | 4.00% | 4.12% | 1,403.0M | 10,350.3M | 7.37x |
| snapshot_resume | 17.17% | 2.85% | 214.7M | 1,458.6M | 6.79x |
| snapshot_resume_cold | 17.73% | 3.62% | 214.3M | 1,507.1M | 7.03x |
| concurrent_resume | 17.40% | 4.68% | 2,109.5M | 11,841.5M | 5.61x |

### 5.3 I/O 峰值吞吐对比

| Scenario | x86 峰值设备 | x86 峰值 (MB/s) | ARM 峰值设备 | ARM 峰值 (MB/s) | 模式 |
|---|---|---|---|---|---|
| snapshot_creation | nvme2n1/dm-6 | 34 写 | ublkb2 | 7.4 读 | x86 写密集, ARM 读为主 |
| snapshot_creation_1gdisk | ublkb3 | 1,573 写 | ublkb2 | 1,221 写 | 均大顺序写, x86 略高 |
| snapshot_creation_1gmem | dm-0/nvme2n1 | 50 写 | ublkb2 | 2.9 读 | x86 写, ARM 读 |
| snapshot_resume | dm-6/nvme2n1 | 95 写 | ublkb3 | 18.5 读 | x86 写为主, ARM 读为主 |
| snapshot_resume_cold | ublkb4 | 273 读 | ublkb3 | 237 读 | 均大量读, x86 略高 |
| concurrent_resume | ublkb4 | 27 读 | ublkb3 | 16.9 读 | 均读, x86 略高 |

### 5.4 sar 分页峰值对比

| Scenario | x86 pgpgin/s max | ARM pgpgin/s max | x86 pgpgout/s max | ARM pgpgout/s max | x86 majflt/s max | ARM majflt/s max |
|---|---|---|---|---|---|---|
| snapshot_creation | 16,911 | 13,809 | 34,236 | 1,158 | 0 | 0 |
| snapshot_creation_1gdisk | 14,389 | 8,196 | 3,149,204 | 2,270,804 | 0 | 0 |
| snapshot_creation_1gmem | 10,444 | 7,788 | 50,392 | 390 | 0.5 | 0 |
| snapshot_resume | 20,510 | 26,134 | 94,370 | 660 | 163.5 | 154.0 |
| snapshot_resume_cold | 272,732 | 236,788 | 6,428 | 4,346 | 220.0 | 164.0 |
| concurrent_resume | 38,234 | 24,682 | 2,778 | 702 | 179.5 | 149.0 |

---

## 6. 关键观察

### 6.1 延迟特征

- **creation 系列 x86 全面领先**：snapshot_creation 快 1.63x，1gdisk 快 1.60x，1gmem 快 2.05x。x86 Zen5 单核性能优势在写元数据/内存转储路径上充分发挥
- **resume 系列 ARM 领先**：snapshot_resume 快 1.32x，resume_cold 快 1.26x。ARM 鲲鹏在恢复读路径上更优，可能与 page cache 预读效率有关
- **concurrent_resume x86 大幅领先**：快 1.94x，但两者 CV 都很高（38-42%），并发竞争激烈导致波动大

### 6.2 Cache 效率

- **ARM cache-refs 总量是 x86 的 5.6-7.4 倍**，但 miss 率更低（2.6-5.2% vs x86 4-17.7%）
- ARM 鲲鹏 L1/L2 cache 更大但访问次数更多，整体 cache 效率更好
- x86 resume 系列 miss 率 17-18% 是瓶颈信号——恢复路径访存模式不规则，x86 cache 层次对此更敏感

### 6.3 I/O 模式差异

- **x86 偏写密集**：creation 和 resume 路径以写 I/O 为主（dm-6/nvme2n1 写吞吐高），符合"创建=写"语义
- **ARM 偏读密集**：同样场景 ARM 以读 I/O 为主（ublkb2/ublkb3 读吞吐高），可能与 ARM 的 page cache 策略或 ublk 设备映射差异有关
- **1gdisk 是 I/O 最重场景**：x86 ublkb3 峰值 1,573 MB/s 写，ARM ublkb2 峰值 1,221 MB/s 写，两者 %util 都最高（x86 35.6%, ARM 50.6%）

### 6.4 分页特征

- **1gdisk**: x86 pgpgout/s 峰值 3.15M > ARM 2.27M，但 ARM avg 1.20M > x86 200K——ARM 持续换出更均匀
- **resume_cold**: x86 pgpgin/s 峰值 273K > ARM 237K，ARM avg 97K >> x86 6.6K——ARM 冷恢复换入更持续
- **majflt**: resume 系列两者都有 majflt（x86 163-220, ARM 149-164），说明冷恢复路径确实触发主缺页中断；creation 系列均无 majflt
- **concurrent_resume**: x86 fault/s 峰值 326K >> ARM 178K，并发场景 x86 缺页中断压力更大
