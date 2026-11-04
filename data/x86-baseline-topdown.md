## 概览

| 指标 | snapshot_creation | snapshot_creation_1gdisk | snapshot_creation_1gmem | snapshot_resume | snapshot_resume_cold | concurrent_resume |
|---|---:|---:|---:|---:|---:|---:|
| Total_Cycles (LS_NOT_HALTED_CYC) | 1,048,918,262 | 1,033,941,232 | 1,037,413,349 | 1,035,315,884 | 1,032,371,941 | 1,051,575,620 |
| Total_Retired_Instructions | 1,958,663,616 | 1,959,600,651 | 1,960,971,135 | 1,959,717,107 | 1,956,821,809 | 1,961,127,923 |
| Total_Retired_Ops | 1,852,049,644 | 1,852,974,455 | 1,855,068,335 | 1,853,846,542 | 1,850,406,157 | 1,855,667,857 |
| Total_Dispatch_Slots (8*cyc) | 8,391,346,096 | 8,271,529,856 | 8,299,306,792 | 8,282,527,072 | 8,258,975,528 | 8,412,604,960 |
| IPC | 1.867 | 1.895 | 1.890 | 1.893 | 1.895 | 1.865 |

## Front-End Bound

| 指标 | snapshot_creation | snapshot_creation_1gdisk | snapshot_creation_1gmem | snapshot_resume | snapshot_resume_cold | concurrent_resume |
|---|---:|---:|---:|---:|---:|---:|
| **Front-End Bound** | 37.968% | 37.675% | 37.939% | 37.879% | 37.708% | 38.180% |
| Front-End Latency | 24.369% | 24.118% | 24.309% | 24.190% | 24.209% | 24.432% |
| ICache Miss | 124,733,680 | 126,385,643 | 123,476,128 | 127,310,114 | 123,863,889 | 126,080,098 |
| ITLB Miss (L1+L2) | 2,756,517 | 1,664,435 | 2,881,367 | 3,045,900 | 3,318,105 | 3,630,951 |
| Front-End Bandwidth | 13.600% | 13.557% | 13.631% | 13.689% | 13.499% | 13.748% |


## Bad Speculation

| 指标 | snapshot_creation | snapshot_creation_1gdisk | snapshot_creation_1gmem | snapshot_resume | snapshot_resume_cold | concurrent_resume |
|---|---:|---:|---:|---:|---:|---:|
| **Bad Speculation** | 5.731% | 5.503% | 5.426% | 5.638% | 5.510% | 5.640% |
| Branch Mispredicts | 5.424% | 5.205% | 5.141% | 5.337% | 5.220% | 5.349% |
| Indirect Branch Misp | 5.374% | 5.083% | 5.334% | 5.357% | 5.216% | 5.239% |
| Return Mispred | 0.632% | 0.742% | 0.630% | 0.708% | 0.697% | 0.738% |
| Machine Clears | 0.307% | 0.298% | 0.285% | 0.302% | 0.290% | 0.291% |


## Retiring

| 指标 | snapshot_creation | snapshot_creation_1gdisk | snapshot_creation_1gmem | snapshot_resume | snapshot_resume_cold | concurrent_resume |
|---|---:|---:|---:|---:|---:|---:|
| **Retiring** | 23.341% | 23.691% | 23.628% | 23.661% | 23.693% | 23.312% |

## Back-End Bound

| 指标 | snapshot_creation | snapshot_creation_1gdisk | snapshot_creation_1gmem | snapshot_resume | snapshot_resume_cold | concurrent_resume |
|---|---:|---:|---:|---:|---:|---:|
| **Back-End Bound** | 32.959% | 33.131% | 33.006% | 32.822% | 33.089% | 32.868% |
| **Core Bound** | 0.000% | 0.000% | 0.000% | 0.000% | 0.000% | 0.000% |
| Resource Bound | 15.571% | 14.393% | 14.575% | 15.082% | 15.041% | 15.304% |
| ROB RetQ Stall | 15,325,768 | 14,609,017 | 12,750,108 | 15,294,193 | 16,045,720 | 15,082,746 |
| IntReg Stall | 100,844,436 | 93,454,283 | 94,960,342 | 97,842,137 | 95,912,261 | 99,422,455 |
| LoadQ Stall | 7,964,603 | 8,003,887 | 7,885,055 | 6,817,085 | 7,478,296 | 7,866,805 |
| StoreQ Stall | 38,809,395 | 32,292,575 | 35,236,579 | 35,718,143 | 35,239,499 | 38,167,338 |
| Addl Resource Stalls | 386,604 | 458,535 | 370,519 | 478,518 | 600,909 | 396,915 |
| **Memory Bound** | 49.822% | 49.697% | 49.789% | 51.846% | 49.849% | 51.015% |
| L2 Bound (DC_Fill_L2) | 72.876% | 75.466% | 75.912% | 73.363% | 76.085% | 73.689% |
| L3 Bound (DC_Fill_CCX) | 18.851% | 18.659% | 17.679% | 18.063% | 18.860% | 18.401% |
| Near Cache | 1.105% | 0.767% | 1.573% | 1.380% | 1.231% | 1.527% |
| DRAM Near | 5.765% | 5.642% | 5.868% | 5.980% | 5.612% | 5.927% |
| Far Cache | 0.203% | 0.174% | 0.287% | 0.268% | 0.267% | 0.245% |
| DRAM Far | 0.807% | 0.841% | 0.886% | 0.853% | 0.888% | 0.884% |

## Miss Rate Summary

| 指标 | snapshot_creation | snapshot_creation_1gdisk | snapshot_creation_1gmem | snapshot_resume | snapshot_resume_cold | concurrent_resume |
|---|---:|---:|---:|---:|---:|---:|
| Branch Miss Rate | 1.505% | 1.516% | 1.469% | 1.534% | 1.542% | 1.601% |
| L1I Miss Rate | 15.162% | 15.488% | 15.351% | 15.497% | 15.096% | 15.229% |
| L1ITLB Miss Rate | 0.467% | 0.287% | 0.503% | 0.521% | 0.589% | 0.609% |
| L1DTLB Miss Rate | 0.868% | 0.880% | 0.843% | 0.866% | 0.849% | 0.881% |
| L2D Miss Rate | 38.346% | 39.621% | 38.238% | 40.547% | 37.946% | 38.447% |
| L3D Miss Rate | 47.330% | 45.032% | 47.502% | 49.166% | 52.694% | 46.883% |

