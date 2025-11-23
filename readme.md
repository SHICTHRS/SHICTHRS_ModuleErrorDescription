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

### SHICTHRSCSVLoader模块

| 错误代码 | 异常类 | 英文描述 | 中文描述 |
|---------|--------|---------|---------|
| 1017 | SHRCSVLoaderException | only .csv file is supported | 仅支持csv文件 |
| 1018 | SHRCSVLoaderException | unable to find csv file | 无法找到csv文件 |
| 1019 | SHRCSVLoaderException | unable to read csv file | 无法读取csv文件 |
| 1020 | SHRCSVLoaderException | data must be a dictionary | csv写入数据源必须为字典 |
| 1021 | SHRCSVLoaderException | only .csv file is supported | 仅支持csv文件 |
| 1022 | SHRCSVLoaderException | unable to write csv file | 在核心接口中发生错误 |
| 1023 | SHRCSVLoaderException | unable to write csv file | 在公共接口中发生错误 |
| 1024 | SHRCSVLoaderException | data must be a list | csv插入的表头必须为列表 |
| 1025 | SHRCSVLoaderException | only .csv file is supported | 仅支持csv文件 |
| 1026 | SHRCSVLoaderException | unable to insert csv file | 在核心接口中发生错误 |
| 1027 | SHRCSVLoaderException | unable to insert csv file | 在公共接口中发生错误 |

### SHICTHRSLogCore模块

| 错误代码 | 异常类 | 英文描述 | 中文描述 |
|---------|--------|---------|---------|
| 1028 | SHRLogCoreException | unable to init SHRLogCoreRecorder | 无法初始化日志记录器 |
| 1029 | SHRLogCoreException | unable to clean outdated logs | 无法清除过期日志 |
| 1030 | SHRLogCoreException | unable to read SHRLogCoreConfigSettings.ini | 无法正常加载logcore配置文件 |
| 1031 | SHRLogCoreException | unable to rebuild logcore config settings | 无法重载logcore配置文件 |
| 1032 | SHRLogCoreException | unable to output log to console | 无法向控制台输出日志 |
| 1033 | SHRLogCoreException | unable to record log | 无法记录日志 |
| 1034 | SHRLogCoreException | unable to update log config file | 无法更新logcore配置文件 |

### SHICTHRSMACE模块

| 错误代码 | 异常类 | 英文描述 | 中文描述 |
|---------|--------|---------|---------|
| 2000 | SHRMACEException | unable to get uuid | 系统uuid获取失败 |
| 2001 | SHRMACEException | unable to get WindowsProductID | windows产品序列号获取失败 |
| 2002 | SHRMACEException | unable to get CPU info | cpu信息获取失败 |
| 2003 | SHRMACEException | unable to get CPU id | cpu序列号获取失败 |
| 2004 | SHRMACEException | unable to get CPU vendor | cpu生产厂商获取失败 |
| 2005 | SHRMACEException | unable to get MotherBoard info | 主板信息获取失败 |
| 2006 | SHRMACEException | unable to get MotherBoard id | 主板序列号获取失败 |
| 2007 | SHRMACEException | unable to get GPU info | 显卡信息获取失败 |
| 2008 | SHRMACEException | unable to get GPU id | 显卡序列号获取失败 |
| 2009 | SHRMACEException | unable to get disk info | 硬盘信息获取失败 |
| 2009.0 | SHRMACEException | error occurred while getting disk info | 在读取硬盘信息时发生错误 |
| 2009.1 | SHRMACEException | error occurred while getting disk DISK_PARTITION info | 在读取硬盘分区信息时发生错误 |
| 2010 | SHRMACEException | unable to get disk id | 硬盘序列号获取失败 |
| 2011 | SHRMACEException | unable to get memory info | 内存信息获取失败 |

