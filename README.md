# 区块链性能测试工具

## 项目概述

本工具用于测试区块链网络的性能指标，包括共识时间、吞吐量和交易溯源查询时间。

## 功能特性

- 测试不同节点数量的平均共识时间
- 测试不同交易规模的吞吐量(TPS)
- 测试交易溯源查询时间
- 支持Ganache本地测试网络
- 自动检测网络连接和账户状态

## 安装步骤

1. 确保已安装Python 3.7+环境
2. 安装依赖包：

```bash
pip install web3


3. 启动Ganache本地测试网络

## 使用方法

```python
from blockchain_performance_test import BlockchainPerformanceTester

# 初始化测试器
tester = BlockchainPerformanceTester(node_count=8)

# 测试共识时间
print(f"平均共识时间: {tester.test_consensus_time():.2f} ms")

# 测试吞吐量
print(f"吞吐量: {tester.test_throughput(tx_count=1000):.2f} TPS")

# 测试交易溯源时间
print(f"交易查询时间: {tester.test_traceability(tx_count=1000):.2f} ms")
```

## 测试指标说明

1. **共识时间**：测量多个节点达成共识所需的平均时间
2. **吞吐量(TPS)**：系统每秒能够处理的交易数量
3. **交易溯源时间**：查询特定交易信息所需的时间

## 运行示例

```bash
python blockchain_performance_test.py
```

## 注意事项

- 确保Ganache运行在<http://127.0.0.1:7545>
- Ganache中至少需要2个账户
- 测试前确保网络连接正常
