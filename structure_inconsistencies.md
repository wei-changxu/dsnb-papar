# `main.tex` 内容不协调记录

本笔记只记录论文现有内容之间的不一致、疑问和待确认事项，不对正文作出裁决或修改。位置名称采用重组后的章节标题。

## 章节结构

- 原稿在事件重建之后出现了一个没有正文的 `Sensitivity study`，在判选章节之后又出现了同名且包含公式、图片和结论的章节。重组后删除空标题，只保留后者。

## 拟合优度定义与实现

- `Event Selection / Fitting goodness` 的早期描述称：只有 `n_i \neq 0` 时才累计自由度和 `\chi_P^2`。
- 同一小节后续引用 Cowan，并指出 `n_i=0` 时仍应计算 `\nu_i-n_i`，同时把“不计入零 bin”的方法明确标为错误算法。
- 同一部分比较了 `80\times68`、`200\times6444` 以及直接使用负对数似然等多种定义。正文保留这些不同版本，尚需作者确认最终采用的定义。

## 拟合优度判选边界

- `Event Selection / selection efficiency` 的效率表使用 `\chi_P^2 < 311 E_{prompt}/MeV+1212`。
- `Selection Results and Residual Backgrounds / Event classification and selection metrics` 的判选条件表使用 `\chi_{fit}^2 < 331 E_{prompt}+1212`。
- `Event Selection / 判选条件重复问题` 将指标写为 `I_{\chi_P^2}=-\chi_P^2+310 E_{prompt}/\mathrm{MeV}+1412>0`。
- 三处斜率或截距不一致；另有附录建议把指标进一步收紧到 `I_{\chi_P^2}>200`。

## CPE/SPE 重建的先验概率

- `Simulation and Event Reconstruction / CPE and SPE reconstruction` 先按电子模型预测的 `n_c,n_s` 构造 `P_c=n_cf_c/(n_cf_c+n_sf_s)`。
- 随后正文指出未知粒子种类时并不存在该电子模型先验，并提出改用 `P_c=f_c/(f_c+f_s)`。两种定义在文中同时保留，尚未说明后续图表具体采用哪一种。

## 慢信号能量条件

- `Event Selection / Coincidence` 中原有判选概览只列出 `E_{delayed}`，没有给出完整范围。
- 同一小节后续按不同核素的俘获能量及 `3\sigma` 分辨率定义 `E_{cap}-3\sigma_{cap}\le E_{delayed}\le E_{cap}+3\sigma_{cap}`。
- 需要确认判选是按核素分别使用能窗，还是存在一个统一的慢信号能窗。

## 本底率与曝光量

- `Event Selection / selection efficiency` 给出的最终大气中微子率为 `0.0212 (20 kt year)^{-1}`。
- `Selection Results and Residual Backgrounds / Residual-background investigation` 给出的结果为在 `22.5 kt year` 下剩余 `5\times10^{-3}`。
- 两组数值使用不同曝光量，且即使换算后也不直接一致；可能对应不同判选版本或样本，需要确认。
- 原稿的多个表和正文交替使用 `20 kt year` 与 `22.5 kt year`，目前未统一归一化基准。

## 大气中微子末态分类术语

- `Atmospheric-neutrino Background / Final-state classification` 在介绍完 NC 分类后写有“对于 NC 末态，我们也进行同样的分类”，但紧接着讨论带电轻子以及不同中微子/反中微子下缺失的核子种类；结合上下文，该处疑似本应指 CC 末态。

## 判选条件相关性

- `Event Selection / 判选条件重复问题` 指出，拟合优度和 Cherenkov/Scintillation 比例都依赖电子模型，并展示两指标明显相关。
- 原稿同时保留了二者作为独立 cut，也展示了收紧拟合优度后重新计算的效率和相关系数；尚未决定是否合并、删除或重新优化其中一个判选。

## Cherenkov-ring 判选的状态

- 判选边界 `\chi_{\mathrm{chev}}^2<-0.025 E_{prompt}/\mathrm{MeV}+1.25` 被说明为根据分布目测选定，尚未通过参数扫描优化。
- 当前使用固定正电子模板，正文同时指出尚未考虑模板对能量和顶点位置的依赖。

## 尚未完成的内容

- 大气中微子末态分类选择效率处仍保留“待整理”。
- 多维选择效率图后仍保留“NC 末态和 CC 末态可以分在两个图里”的待完善说明。
- 文末待做清单要求补充信号特征与分类动机、搬入全部味道的 NC/CC 表格，以及放大或重做图片。这些均未在本次纯结构整理中执行。
