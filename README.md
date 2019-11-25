# da-bbr
Delay-Aware BBR Congestion Control Algorithm

## Introduction

Delay-Aware BBR Congestion Control Algorithm (DA-BBR) is a implementation of *a*STEAM Project <https://asteam.korea.ac.kr>. 
Google proposed the Bottleneck Bandwidth and Round-trip time (BBR) congestion control algorithm to achieve high bandwidth and low latency for Internet traffic. BBR can reduce packet loss and minimize end-to-end packet delay, which has attracted the attention of many researchers. However, there is a serious fairness issue between TCP BBR flows with different RTTs. In this work, we propose a solution to mitigate the RTT fairness issue between BBR flows.

## Requirements and Dependencies

* Please access `include/net/inet_connection_socket.h` and set `ICSK_CA_PRIV_SIZE` to `256 * sizeof(u64)`.
* Above development was based on the Linux version of 4.14.64+.

## Instructions

* How to Run
  1. Just replace the existing `tcp_bbr.c` in `/usr/src/.../net/ipv4/`.
  2. `make && make install` for the directory.
  3. `reboot` the system.
  4. Change the default Congestion Algorithm to *bbr*

