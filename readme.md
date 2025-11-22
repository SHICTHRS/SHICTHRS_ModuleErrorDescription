# SHICTHRS Module Error Description

SHICTHRS模块错误代码与异常说明文档，为SHICTHRS系列项目提供统一的错误代码标准。

## 概述

本项目提供了SHICTHRS系列模块的错误代码定义和详细说明，帮助开发者和用户快速理解并处理各类异常情况。

## 模块错误代码

### SHICTHRSConfigLoader模块

| 错误代码 | 异常类 | 英文描述 | 中文描述 |
|---------|--------|---------|---------|
| 1000 | SHRConfigLoaderException | only .ini file is supported | 模块仅支持ini配置文件读取 |
| 1001 | SHRConfigLoaderException | unable to find config file | 找不到ini配置文件 |
| 1002 | SHRConfigLoaderException | unable to read config file | 无法读取配置文件 |
| 1003 | SHRConfigLoaderException | unable to write config file | 无法写入配置文件 |

### SHICTHRSJsonLoader模块

| 错误代码 | 异常类 | 英文描述 | 中文描述 |
|---------|--------|---------|---------|
| 1004 | SHRJsonLoaderException | only .json file is supported [read] | 读取模式下仅支持json文件 |
| 1005 | SHRJsonLoaderException | unable to find json file | 找不到json文件 |
| 1006 | SHRJsonLoaderException | unable to read json file | 无法读取json文件 |
| 1007 | SHRJsonLoaderException | only .json file is supported [write] | 写入模式下仅支持json文件 |
| 1008 | SHRJsonLoaderException | unable to write json file | 无法写入json文件 |
| 1009 | SHRJsonLoaderException | json file enkey not found | 找不到json文件加密密钥 |
| 1010 | SHRJsonLoaderException | invalid encrypted file | 不是一个加密文件 |
| 1011 | SHRJsonLoaderException | incorrect key provided | 错误的密钥 |
| 1012 | SHRJsonLoaderException | data integrity check failed | json文件数据完整性校验失败 |
| 1013 | SHRJsonLoaderException | unsupported encryption type | 不支持的加密类型 |
| 1014 | SHRJsonLoaderException | encryption type mismatch | 解密方法与文件加密类型不匹配 |
| 1015 | SHRJsonLoaderException | json_dict parameter must be a dictionary | 传入的json字典必须为字典 |
| 1016 | SHRJsonLoaderException | file integrity check failed | 文件完整性校验失败 |

## 错误代码命名规则

SHICTHRS项目错误代码遵循以下命名规则：

- **1000-1999**: 配置与文件加载相关错误
- **1000-1099**: SHICTHRSConfigLoader模块错误
- **1100-1199**: SHICTHRSJsonLoader模块错误

## 使用方法

```python
from SHICTHRSJsonLoader import SHRJsonLoaderException

try:
    # 您的代码
except SHRJsonLoaderException as e:
    error_code = e.error_code  # 获取错误代码
    print(f"错误代码: {error_code}")
    print(f"错误信息: {e.message}")
```

## 贡献

欢迎提交新的错误代码定义或修改建议。请确保：

1. 错误代码遵循现有编号规则
2. 提供清晰的英文和中文描述
3. 使用统一的格式提交Pull Request

## 许可证

本项目采用 SHICTHRS 标准许可证。

## 联系方式

如有疑问或建议，请联系SHICTHRS团队。

---

*最后更新: 2025年*