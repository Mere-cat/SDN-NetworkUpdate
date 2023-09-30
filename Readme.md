# Readme

SDN 最佳化更新路徑演算法

## Problem Description

在原本的網路圖中，路徑的權重變更。因此設計一演算法，讓更新這個網路圖的成本是最小的。

* **Goal:** minimize the new path cost + node cost (total cost)

* **Input:**

  * Numbers of node (i.e., switches)
  * Links with new weights (between switches)
  * An source-destination pair with an old path and forward start time
  * 1st and 2nd time for old and new rules, respectively
  * Simulation duration

* **Procedure:**

  * Send packets to install old rules at 1st time for installation
  * Upload link costs to the controller from nodes at 2nd time
  * Compute the new path for the SD pair with a small total cost
  * Update new rules after the controller receives the link costs
  * Forward the packet for the SD pair at the forward start time

* **Output:**

  * a new routing path

* **Result:** All packets transmitted in the network 
  
  

## Solution

我在這裡使用 **Shortest Path Tree** 演算法，雖然不是班上「最佳的」解法，但成果已是相當不錯（班級前 20%）
