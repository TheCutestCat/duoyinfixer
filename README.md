# Duoyinfixer 使用说明
在中文配音中，因为多音字有多种发音，而导致器很容易出错，对应的发音不是我们所希望的。
使用Duoyinfixer将所有的多音字文本转化为 单音字文本，从而避免配音中上述的多音字错误问题

## 安装
请使用以下命令安装 duoyinfixer：
```bash
pip install duoyinfixer==0.1
```

## 使用方法
在您的 Python 代码中，您可以通过以下方式导入并使用 duoyinfixer：
```python
from duoyinfixer import fixer
result = fixer('今天上山去砍柴，感觉很高兴')
print(result) # 今天丄山去砍柴，感爵很高莕

result= fixer('我好想睡一觉，然后出去玩！')
print(result) # 我郝想睡一酵，然后出去玩！
```

## 方法说明
该工具的工作流程如下：
1. 检查输入文本中是否存在多音字。
2. 使用 `pypinyin` 库获取多音字在当前语境下的拼音。
3. 找到并替换为对应的单音字。


## 参考仓库
[pypinyin](https://github.com/mozillazg/python-pinyin)
[chinese-dictionary](https://github.com/mapull/chinese-dictionary)