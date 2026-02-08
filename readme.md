<div align="center">

# SHICTHRS Module Error Description

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/)
[![Build Status](https://img.shields.io/badge/build-passing-brightgreen.svg)]()
[![Coverage](https://img.shields.io/badge/coverage-85%25-green.svg)]()

**SHICTHRS模块错误代码与异常说明文档，为SHICTHRS系列项目提供统一的错误代码标准**

[模块状态](#现有模块状态) • [错误代码](#模块错误代码)

</div>

---

## 概述

本项目提供了SHICTHRS系列模块的错误代码定义和详细说明，帮助开发者和用户快速理解并处理各类异常情况。通过统一的错误代码体系，提升项目的可维护性和用户体验。

---

## 现有模块状态

### 模块概览

| 模块名称 | 最新版本 | 更新时间 | 维护状态 | 项目地址 |
|---------|--------|---------|---------|---------|
| **SHICTHRSECThread** | `1.0.0` | 20260114 | ✅ | [SHICTHRS_ECThread](https://github.com/SHICTHRS/SHICTHRS_ECThread) |
| **SHICTHRSTimer** | `1.2.0` | 20260110 | ✅ | [SHICTHRS_Timer](https://github.com/SHICTHRS/SHICTHRS_Timer) |
| **SHICTHRSWMICManager** | `1.3.0` | 20251206 | ✅ | [SHICTHRS_WMICManager](https://github.com/SHICTHRS/SHICTHRS_WMICManager) |
| **SHICTHRSBrowserReader** | `1.3.0` | 20251129 | ✅ | [SHICTHRS_BrowserReader](https://github.com/SHICTHRS/SHICTHRS_BrowserReader) |
| **SHICTHRSVTChecker** | `1.2.0` | 20251129 | ✅ | [SHICTHRS_VTChecker](https://github.com/SHICTHRS/SHICTHRS_VTChecker) |
| **SHICTHRSWindowsDefenderManager** | `1.1.0` | 20251129 | ✅ | [SHICTHRS_WindowsDefenderManager](https://github.com/SHICTHRS/SHICTHRS_WindowsDefenderManager) |
| **SHICTHRSENCR** | `1.3.0` | 20251129 | ✅ | [SHICTHRS_ENCR](https://github.com/SHICTHRS/SHICTHRS_ENCR) |
| **SHICTHRSMACE** | `1.7.0` | 20260125 | ✅ | [SHICTHRS_MACE](https://github.com/SHICTHRS/SHICTHRS_MACE) |
| **SHICTHRSLogCore** | `1.12.0` | 20251214 | ✅ | [SHICTHRS_LogCore](https://github.com/SHICTHRS/SHICTHRS_LogCore) |
| **SHICTHRSCSVLoader** | `1.6.0` | 20260122 | ✅ | [SHICTHRS_CSVLoader](https://github.com/SHICTHRS/SHICTHRS_CSVLoader) |
| **SHICTHRSJsonLoader** | `1.5.0` | 20251129 | ✅ | [SHICTHRS_JsonLoader](https://github.com/SHICTHRS/SHICTHRS_JsonLoader) |
| **SHICTHRSConfigLoader** | `1.5.0` | 20251214 | ✅ | [SHICTHRS_ConfigLoader](https://github.com/SHICTHRS/SHICTHRS_ConfigLoader) |

---

## 模块错误代码

### SHICTHRSConfigLoader 模块

> 配置文件加载器模块，负责处理INI格式配置文件的读写操作

| 错误代码 | 异常类 | 英文描述 | 中文描述 |
|---------|--------|---------|---------|
| `1000` | `SHRConfigLoaderException` | only .ini file is supported | 模块仅支持ini配置文件读取 |
| `1001` | `SHRConfigLoaderException` | unable to find config file | 找不到ini配置文件 |
| `1002` | `SHRConfigLoaderException` | unable to read config file | 无法读取配置文件 |
| `1003` | `SHRConfigLoaderException` | unable to write config file | 无法写入配置文件 |

### SHICTHRSJsonLoader 模块

> JSON文件加载器模块，支持JSON文件的读写操作和加密功能

| 错误代码 | 异常类 | 英文描述 | 中文描述 |
|---------|--------|---------|---------|
| `1004` | `SHRJsonLoaderException` | only .json file is supported [read] | 读取模式下仅支持json文件 |
| `1005` | `SHRJsonLoaderException` | unable to find json file | 找不到json文件 |
| `1006` | `SHRJsonLoaderException` | unable to read json file | 无法读取json文件 |
| `1007` | `SHRJsonLoaderException` | only .json file is supported [write] | 写入模式下仅支持json文件 |
| `1008` | `SHRJsonLoaderException` | unable to write json file | 无法写入json文件 |
| `1009` | `SHRJsonLoaderException` | json file enkey not found | 找不到json文件加密密钥 |
| `1010` | `SHRJsonLoaderException` | invalid encrypted file | 不是一个加密文件 |
| `1011` | `SHRJsonLoaderException` | incorrect key provided | 错误的密钥 |
| `1012` | `SHRJsonLoaderException` | data integrity check failed | json文件数据完整性校验失败 |
| `1013` | `SHRJsonLoaderException` | unsupported encryption type | 不支持的加密类型 |
| `1014` | `SHRJsonLoaderException` | encryption type mismatch | 解密方法与文件加密类型不匹配 |
| `1015` | `SHRJsonLoaderException` | json_dict parameter must be a dictionary | 传入的json字典必须为字典 |
| `1016` | `SHRJsonLoaderException` | file integrity check failed | 文件完整性校验失败 |

### SHICTHRSCSVLoader 模块

> CSV文件加载器模块，提供CSV文件的读取、写入和插入功能

| 错误代码 | 异常类 | 英文描述 | 中文描述 |
|---------|--------|---------|---------|
| `1017` | `SHRCSVLoaderException` | only .csv file is supported | 仅支持csv文件 |
| `1018` | `SHRCSVLoaderException` | unable to find csv file | 无法找到csv文件 |
| `1019` | `SHRCSVLoaderException` | unable to read csv file | 无法读取csv文件 |
| `1020` | `SHRCSVLoaderException` | data must be a dictionary | csv写入数据源必须为字典 |
| `1021` | `SHRCSVLoaderException` | only .csv file is supported | 仅支持csv文件 |
| `1022` | `SHRCSVLoaderException` | unable to write csv file | 在核心接口中发生错误 |
| `1023` | `SHRCSVLoaderException` | unable to write csv file | 在公共接口中发生错误 |
| `1024` | `SHRCSVLoaderException` | data must be a list | csv插入的表头必须为列表 |
| `1025` | `SHRCSVLoaderException` | only .csv file is supported | 仅支持csv文件 |
| `1026` | `SHRCSVLoaderException` | unable to insert csv file | 在核心接口中发生错误 |
| `1027` | `SHRCSVLoaderException` | unable to insert csv file | 在公共接口中发生错误 |

### SHICTHRSLogCore 模块

> 日志核心模块，提供统一的日志记录和管理功能

| 错误代码 | 异常类 | 英文描述 | 中文描述 |
|---------|--------|---------|---------|
| `1028` | `SHRLogCoreException` | unable to init SHRLogCoreRecorder | 无法初始化日志记录器 |
| `1029` | `SHRLogCoreException` | unable to clean outdated logs | 无法清除过期日志 |
| `1030` | `SHRLogCoreException` | unable to read SHRLogCoreConfigSettings.ini | 无法正常加载logcore配置文件 |
| `1031` | `SHRLogCoreException` | unable to rebuild logcore config settings | 无法重载logcore配置文件 |
| `1032` | `SHRLogCoreException` | unable to output log to console | 无法向控制台输出日志 |
| `1033` | `SHRLogCoreException` | unable to record log | 无法记录日志 |
| `1034` | `SHRLogCoreException` | unable to update log config file | 无法更新logcore配置文件 |

### SHICTHRSMACE 模块

> 机器硬件信息收集模块，获取系统硬件和软件信息

| 错误代码 | 异常类 | 英文描述 | 中文描述 |
|---------|--------|---------|---------|
| `2000` | `SHRMACEException` | unable to get uuid | 系统uuid获取失败 |
| `2001` | `SHRMACEException` | unable to get WindowsProductID | windows产品序列号获取失败 |
| `2002` | `SHRMACEException` | unable to get CPU info | cpu信息获取失败 |
| `2003` | `SHRMACEException` | unable to get CPU id | cpu序列号获取失败 |
| `2004` | `SHRMACEException` | unable to get CPU vendor | cpu生产厂商获取失败 |
| `2005` | `SHRMACEException` | unable to get MotherBoard info | 主板信息获取失败 |
| `2006` | `SHRMACEException` | unable to get MotherBoard id | 主板序列号获取失败 |
| `2007` | `SHRMACEException` | unable to get GPU info | 显卡信息获取失败 |
| `2008` | `SHRMACEException` | unable to get GPU id | 显卡序列号获取失败 |
| `2009` | `SHRMACEException` | unable to get disk info | 硬盘信息获取失败 |
| `2009.0` | `SHRMACEException` | error occurred while getting disk info | 在读取硬盘信息时发生错误 |
| `2009.1` | `SHRMACEException` | error occurred while getting disk DISK_PARTITION info | 在读取硬盘分区信息时发生错误 |
| `2010` | `SHRMACEException` | unable to get disk id | 硬盘序列号获取失败 |
| `2011` | `SHRMACEException` | unable to get memory info | 内存信息获取失败 |
| `2012` | `SHRMACEException` | unable to get MAC info | 网卡物理描述地址获取失败 |
| `2013` | `SHRMACEException` | error occurred while getting creating threads pool | 创建异步线程池时发生错误 |
| `2014` | `SHRMACEException` | error occurred while getting mace info | 获取MACE信息时发生错误 |
| `2015` | `SHRMACEException` | unable to system info | 无法获取windows系统信息 |
| `2015.0` | `SHRMACEException` | windows version is not supported | 不支持的windows系统版本 |
| `2015.1` | `SHRMACEException` | windows version only support 10.0.22000 and above | 仅支持build 22000以上的windows版本 |

### SHICTHRSENCR 模块

> 加密模块，提供哈希计算、Base64编码解码和数据验证功能

| 错误代码 | 异常类 | 英文描述 | 中文描述 |
|---------|--------|---------|---------|
| `3000` | `SHRENCRException` | unable to get hash code | 无法获取字符串哈希值 |
| `3000.1.0` | `SHRENCRException` | only support file | 传入的路径必须指向文件 |
| `3000.1.1` | `SHRENCRException` | file not found | 找不到路径指向的文件 |
| `3000.1.2` | `SHRENCRException` | unable to get file hash code | 无法获取文件哈希值 |
| `3000.2` | `SHRENCRException` | unable to get hash code mask | 无法获取哈希值遮罩 |
| `3001` | `SHRENCRException` | unable to encrypt base64 code | 无法将字符串加密为base64字符 |
| `3002` | `SHRENCRException` | unable to decrypt base64 code | 无法将base64字符串解密为一般字符串 |
| `3003` | `SHRENCRException` | unable to check identity number | 校验身份证号时发生错误 |
| `3004` | `SHRENCRException` | unable to check chinese text | 正则表达式检查中文字符时发生错误 |
| `3005` | `SHRENCRException` | unable to check chinese phone number | 检查中国区手机号码时发生错误 |

### SHICTHRSWindowsDefenderManager 模块

> Windows Defender管理模块，提供系统安全软件的状态检查和控制功能

| 错误代码 | 异常类 | 英文描述 | 中文描述 |
|---------|--------|---------|---------|
| `4000` | `SHRWindowsDefenderManagerException` | unable to check Windows Defender status | 无法获取 Windows Defender 状态 |
| `4001.0` | `SHRWindowsDefenderManagerException` | unable to enable Windows Defender due to PermissionError | 因为注册表权限不足无法启用 Windows Defender |
| `4001.1` | `SHRWindowsDefenderManagerException` | failed to enable Windows Defender | 无法通过修改注册表方式启用 Windows Defender |
| `4001.2` | `SHRWindowsDefenderManagerException` | unable to enable Windows Defender | 无法启用 Windows Defender |
| `4002.0` | `SHRWindowsDefenderManagerException` | unable to disable Windows Defender due to PermissionError | 因为注册表权限不足无法禁用 Windows Defender |
| `4002.1` | `SHRWindowsDefenderManagerException` | failed to disable Windows Defender | 无法通过修改注册表方式禁用 Windows Defender |
| `4002.2` | `SHRWindowsDefenderManagerException` | unable to disable Windows Defender | 无法禁用 Windows Defender |

### SHICTHRSVTChecker 模块

> 虚拟化技术检查模块，检测系统虚拟化相关功能的状态

| 错误代码 | 异常类 | 英文描述 | 中文描述 |
|---------|--------|---------|---------|
| `5000` | `SHRVTCheckerException` | no result output | powershell 无输出 |
| `5000.1` | `SHRVTCheckerException` | an invalid parameter was output | powershell 输出了一个无效的参数 |
| `5001` | `SHRVTCheckerException` | unable to get virtualization firmware status | 无法获取 virtualization firmware 状态 |
| `5001.0` | `SHRVTCheckerException` | an invalid parameter was output | VirtualizationFirmware powershell 输出了一个无效的参数 |
| `5002` | `SHRVTCheckerException` | unable to get data execution prevention status | 无法获取 data execution prevention 状态 |
| `5002.0` | `SHRVTCheckerException` | an invalid parameter was output | DEP powershell 输出了一个无效的参数 |
| `5002.1` | `SHRVTCheckerException` | unable to get nx_supported status | 无法通过 WindowsApi 获取NX服务状态 |
| `5002.2` | `SHRVTCheckerException` | unable to get DEP_Strategy/DEP_Policy_Flag/DEP_Permanent_Setting status | 无法通过 WindowsApi 获取DEP相关服务状态 |
| `5003` | `SHRVTCheckerException` | unable to get second level address translation extensions status | 无法获取 SLAT 二级地址转换 状态 |
| `5003.0` | `SHRVTCheckerException` | an invalid parameter was output | SLAT powershell 输出了一个无效的参数 |
| `5004` | `SHRVTCheckerException` | unable to get VT info | 无法获取VT有关信息 |

### SHICTHRSBrowserReader 模块

> 浏览器数据读取模块，获取和分析浏览器历史记录信息

| 错误代码 | 异常类 | 英文描述 | 中文描述 |
|---------|--------|---------|---------|
| `6000` | `SHRBrowserReaderException` | unable to get browser history | 无法获取浏览器历史记录 |
| `6001` | `SHRBrowserReaderException` | unable to fetch browser history | 无法拉取浏览器历史记录 |
| `6002` <sup>⚠️ 弃用</sup> | `SHRBrowserReaderException` | unable to process browser history | 无法处理浏览器历史记录 |
| `6003` <sup>⚠️ 弃用</sup> | `SHRBrowserReaderException` | unable to extract keyword from browser history | 无法导出浏览器历史记录关键字 |
| `6004` | `SHRBrowserReaderException` | get empty browser history | 导出了空的浏览器历史记录 |

### SHICTHRWMICManager 模块

> WMI命令管理模块，处理Windows Management Instrumentation相关操作

| 错误代码 | 异常类 | 英文描述 | 中文描述 |
|---------|--------|---------|---------|
| `7000` | `SHRWMICManagerException` | unable to check wmic | 无法检查wmic状态 |
| `7001` | `SHRWMICManagerException` | unable to install wmic in Windows10 | 无法在win10环境下安装wmic |
| `7002` | `SHRWMICManagerException` | error occurred while installing wmic | 在win10环境下安装wmic时发生错误 |
| `7003` | `SHRWMICManagerException` | unable to install wmic in Windows11 | 无法在win11环境下安装wmic |
| `7004` | `SHRWMICManagerException` | error occurred while installing wmic | 在win11环境下安装wmic时发生错误 |
| `7005` | `SHRWMICManagerException` | unable to uninstall wmic in Windows11 | 无法在win11环境下卸载wmic |
| `7006` | `SHRWMICManagerException` | error occurred while uninstalling wmic | 在win11环境下卸载wmic时发生错误 |

### SHICTHRSTimer 模块

> 时间处理模块，提供时间格式化、时区转换和时间计算功能

| 错误代码 | 异常类 | 英文描述 | 中文描述 |
|---------|--------|---------|---------|
| `8000` | `SHRTimerException` | format type is not supported | 时间输出格式不被支持 |
| `8001` | `SHRTimerException` | unable to get system time | 无法获取系统时间 |
| `8002` | `SHRTimerException` | unable to get system time stamp | 无法获取系统时间戳 |
| `8003` | `SHRTimerException` | time zone is not supported | 输入的时区不被支持 |
| `8004` | `SHRTimerException` | unable to get pytz time | 无法获取时区时间 |
| `8005` | `SHRTimerException` | unable to determine whether the two times fall within the time period | 无法判断两个时间是否在时间段内 |

### SHICTHRSECThread 模块

> 线程管理模块，处理多线程执行和并发控制

| 错误代码 | 异常类 | 英文描述 | 中文描述 |
|---------|--------|---------|---------|
| `9000` | `SHRECThreadException` | error occurred while thread running | 线程运行时发生错误 |

---

