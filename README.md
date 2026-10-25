# Code Review Demo

一个用于测试 Pull Request 代码审查的小型 Python 仓库。

`main` 分支实现简单的库存预留与结算，包含边界条件测试。
`bug/exact-stock-check` 分支只改动一个比较运算符，产生可复现的逻辑回归：
当订单数量**刚好等于**库存时，结算错误地拒绝订单。

```powershell
python -m unittest discover -s tests -v
```

审查这个 PR 时应根据分支差异和 `minishop/inventory.py`、
`tests/test_checkout.py` 的上下文定位问题，而不是孤立评价变更行。
仓库仅包含演示代码，不包含真实用户数据或密钥。
