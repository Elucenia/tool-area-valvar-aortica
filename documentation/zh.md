<!-- ELUCENIA technical documentation · area-valvar-aortica · zh · no clinical/professional/rights approval -->

# 主动脉瓣面积（连续性方程）

[条件、来源与许可](https://elucenia.org/zh/tools/area-valvar-aortica)

## 使用方法

在门户中使用工具，或通过本地 HTTP 服务器打开 index.html。选择语言，填写各字段，然后计算。

## 输入与单位

### 左心室流出道直径

`dvsve`

cm · 范围: 1.2–3.5

### 左心室流出道 VTI

`vtivsve`

cm · 范围: 5–50

### 主动脉瓣 VTI

`vtiao`

cm · 范围: 10–250

### 主动脉峰值流速（可选）

`vmax`

m/s · 选填 · 范围: 0.5–8

### 体表面积（可选）

`sc`

m² · 选填 · 范围: 0.8–3

## 方法版本

EACVI/ASE 2017：VTI连续性方程；DVI；简化伯努利4 v²

## 已记录的公式

左室流出道面积 = π × (直径 ÷ 2)²

主动脉瓣面积 = 左室流出道面积 × 左室流出道VTI ÷ 主动脉VTI

无量纲指数（DVI） = 左室流出道VTI ÷ 主动脉VTI

峰值压差（简化伯努利方程） = 4 × V²

## 限制与适用人群

EACVI/ASE 2017建议对主动脉瓣狭窄进行综合评估：应同时考虑压差、血流、射血分数以及心室流出道评估质量。低流量或低压差情况需要文档规定的专项评估。单独计算出的数值不能再现完整评估流程。

## 参考文献

- [Baumgartner H et al. Recommendations on the echocardiographic assessment of aortic valve stenosis (EACVI/ASE). J Am Soc Echocardiogr, 2017.](https://doi.org/10.1016/j.echo.2017.02.009)

- [Otto CM et al. 2020 ACC/AHA Guideline for the Management of Patients With Valvular Heart Disease. Circulation, 2021.](https://doi.org/10.1161/CIR.0000000000000923)

## 复现技术测试

在此仓库的根目录中运行 node test.cjs，以重复已记录的合成案例。原始输入、预期结果和容差保持不变。技术测试不构成临床验证。

```sh
node test.cjs
```

tool.json 包含来源、版本和审查范围。examples.json 保留合成输入与预期结果；results.json 记录实际得到的结果。

[记录与参考文献](../tool.json) · [JavaScript代码](../calculator.js) · [参考案例](../examples.json) · [results.json](../results.json)

## 审查与使用条件

尚未开展独立临床审查。

此界面为自主编写的翻译，并非官方或认证版本。尚未完成独立临床审查、专业语言审查或工具权利授权。

公式或分类结果。解释、处理及适用性须结合专业评估和所选来源。

## 许可与署名

Apache-2.0 仅适用于 ELUCENIA 代码。工具、出版物、翻译和数据的权利仍归各自权利人所有。请保留 LICENSE 和 NOTICE。

ELUCENIA · Felipe Guedes · Copyright © 2026

## 已记录的结果

以下信息保留该方法对合成示例的输出，不构成独立的临床验证。

### 1

按面积判定为重度主动脉瓣狭窄

| 结果详情 | |
| --- | --- |
| 左室流出道面积 | 3.14 cm² |
| 无量纲指数（DVI） | 0.25 |
| 最大压差梯度（4V²） | 64 mmHg |


### 2

按面积分级为中度主动脉瓣狭窄

| 结果详情 | |
| --- | --- |
| 左室流出道面积 | 3.80 cm² |
| 无量纲指数（DVI） | 0.37 |

