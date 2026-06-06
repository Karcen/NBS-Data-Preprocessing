# NBS Data Preprocessing

A Python toolkit for preprocessing data downloaded from the National Bureau of Statistics of China.

---

## 中文说明

### 项目简介

本项目提供一套完整的数据预处理流程，用于处理从**国家统计局 (National Bureau of Statistics, NBS)** 网站下载的数据，将其转换为适合面板数据分析的格式。

### 主要功能

1. **格式转换**: 将 `.xls` 文件批量转换为 `.xlsx` 格式
2. **数据合并**: 读取多个 `.xlsx` 文件，删除首行后合并到一个文件的不同工作表中
3. **面板数据转换**: 将宽格式数据转换为长格式面板数据

### 文件结构

| 文件 | 功能 |
|------|------|
| `Covert xls to xlsx.py` | 批量转换 `.xls` 到 `.xlsx` 格式 |
| `delete and combine.py` | 删除文件首行并合并到一个Excel文件 |
| `panel.py` | 将合并数据转换为长格式面板数据 |
| `Provin Name.txt` | 省份名称中英文对照表 |

### 使用方法

1. **准备数据**: 将从国家统计局下载的 `.xls` 文件放入指定文件夹
2. **格式转换**: 运行 `Covert xls to xlsx.py`，修改 `input_folder` 路径
3. **合并文件**: 运行 `delete and combine.py`，修改 `input_folder` 和 `output_file` 路径
4. **生成面板数据**: 运行 `panel.py`，修改 `file_path` 路径

### 依赖

- Python 3.x
- pandas
- openpyxl

### 省份名称映射

| 中文名称 | English Name |
|----------|--------------|
| 北京 | Beijing |
| 天津 | Tianjin |
| 河北 | Hebei |
| 山西 | Shanxi |
| 内蒙古 | Inner Mongolia |
| 辽宁 | Liaoning |
| 吉林 | Jilin |
| 黑龙江 | Heilongjiang |
| 上海 | Shanghai |
| 江苏 | Jiangsu |
| 浙江 | Zhejiang |
| 安徽 | Anhui |
| 福建 | Fujian |
| 江西 | Jiangxi |
| 山东 | Shandong |
| 河南 | Henan |
| 湖北 | Hubei |
| 湖南 | Hunan |
| 广东 | Guangdong |
| 广西 | Guangxi |
| 海南 | Hainan |
| 重庆 | Chongqing |
| 四川 | Sichuan |
| 贵州 | Guizhou |
| 云南 | Yunnan |
| 西藏 | Tibet |
| 陕西 | Shaanxi |
| 甘肃 | Gansu |
| 青海 | Qinghai |
| 宁夏 | Ningxia |
| 新疆 | Xinjiang |

---

## English Instructions

### Project Overview

This project provides a complete data preprocessing pipeline for handling data downloaded from the **National Bureau of Statistics (NBS)** of China, converting it into a format suitable for panel data analysis.

### Main Features

1. **Format Conversion**: Batch convert `.xls` files to `.xlsx` format
2. **Data Merging**: Read multiple `.xlsx` files, remove the first row, and merge into different sheets of one file
3. **Panel Data Transformation**: Convert wide-format data to long-format panel data

### File Structure

| File | Function |
|------|----------|
| `Covert xls to xlsx.py` | Batch convert `.xls` to `.xlsx` format |
| `delete and combine.py` | Remove first row and merge files into one Excel |
| `panel.py` | Transform merged data into long-format panel data |
| `Provin Name.txt` | Province name mapping table (Chinese-English) |

### Usage

1. **Prepare Data**: Place downloaded `.xls` files from NBS website into the specified folder
2. **Convert Format**: Run `Covert xls to xlsx.py`, update `input_folder` path
3. **Merge Files**: Run `delete and combine.py`, update `input_folder` and `output_file` paths
4. **Generate Panel Data**: Run `panel.py`, update `file_path`

### Dependencies

- Python 3.x
- pandas
- openpyxl

### Notes

- It is recommended to download data from the **Chinese version** of the NBS website for faster access.
- Province names in Chinese data can be replaced with English equivalents using the mapping table above.
