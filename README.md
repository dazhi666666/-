# 人名词云图
docx文档中的人名生成词云图
### Repository Name
**`NameCloud-Generator`**

---

### README 文档

# NameCloud-Generator

**NameCloud-Generator** 是一个基于 Python 的工具，用于从 Word 文档（`.docx`）中提取中文人名，并生成词云图。它可以帮助用户快速可视化文档中出现的人名频率，适用于文本分析、数据可视化等场景。

---

## 功能特性

- **人名提取**：从 `.docx` 文档中自动识别中文人名。
- **词云生成**：根据人名频率生成美观的词云图。
- **过滤功能**：支持自定义过滤词列表，屏蔽不需要的词汇。
- **简单易用**：只需提供文档路径，即可一键生成词云。
- **中文优化**：内置中文字体支持，完美显示中文词汇。

---

## 快速开始

### 环境要求

- Python 3.6 或更高版本
- 安装依赖库：
  ```bash
  pip install python-docx jieba wordcloud matplotlib
  ```

### 使用步骤

1. **准备文档**：
   - 将需要分析的 Word 文档放入项目目录，命名为 `input.docx`。
   - 或修改代码中的 `input_file` 参数为你的文档路径。

2. **运行脚本**：
   ```bash
   python NameCloud-Generator.py
   ```

3. **查看结果**：
   - 生成的词云图将保存为 `names_cloud.png`。
   - 图片会显示在屏幕上，并自动保存到项目目录。

---

## 配置文件说明

在脚本的 `CONFIG` 部分，可以自定义以下参数：

```python
CONFIG = {
    "input_file": "input.docx",       # 输入文档路径
    "output_image": "names_cloud.png",# 输出图片路径
    "blacklist": ["某人", "佚名"]       # 需要过滤的词汇
}
```

- **`input_file`**：指定输入的 `.docx` 文件路径。
- **`output_image`**：指定生成的词云图保存路径。
- **`blacklist`**：添加需要过滤的词汇列表。

---

## 示例

### 输入文档内容
```
张三和李四是项目组的核心成员。王五负责测试工作，临时工小明也参与了部分任务。
```

### 生成词云
![示例词云](names_cloud.png)

---

## 常见问题

### 1. 词云图无法显示中文
- 确保项目中包含 `simhei.ttf` 字体文件。
- 或修改代码中的 `font_path` 参数为系统中已安装的中文字体路径。

### 2. 文档处理速度慢
- 如果文档较大，可以尝试优化过滤规则，减少不必要的词汇处理。

### 3. 未检测到人名
- 检查文档中是否包含符合条件的中文人名。
- 尝试调整 `jieba` 分词器的过滤条件。

---

## 贡献与反馈

欢迎提交 Issue 或 Pull Request 改进本项目！  
如有问题或建议，请联系
---

