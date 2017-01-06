# Life Battery

> Android Final Project

## 进度

- 已完成：
  - logo设计
  - 配色选取
  - UI初步设计
  - 主页面
  - 数据库读写
  - [12.16已完成] 载入页面及动画制作
  - [12.17已完成] 注册与登入功能
  - [12.18已完成] 主页面中剩余周数的递减
  - [12.18已完成] 数据库表项设计调整
  - [12.18基本完成] PlansActivity添加表项中日期选择器与下拉框
  - [12.20已完成] 主页面点击生命电池查看无DDL的计划（静态）
  - [12.20已完成] PlanActivity Dialog 布局调整
  - [12.21已完成] AddActivity 布局调整
  - Widget设计与整合
  - Service对用户的后台提示功能实现
  - [12.28已完成] StatisticActivity中打卡功能制作
  - [12.28已完成] 主页面点击生命电池查看无DDL的计划与**数据库连接**
- 待完成：
  - [进行中] UI优化
  - [进行中] StoreActivity页面具体制作与设计（需要进行数据库操作）
  - 电池图标动态更新

## 总体介绍

Life Battery是一款帮助用户克服拖延症、更充实享受人生的App

隐喻：
人生短暂，如同一节一次性电池，耗尽的时间不能重来，
我们需要在有限的短暂几十年中尽可能活成自己想变成的模样。
主界面我们用一颗用了一部分的电池比喻用户人生中剩余的时间（按周计算）

我们将代办事件分为四类：
- 紧急且重要：
  - 通常为一些有DDL的任务，且迫在眼前，需要具备最高优先级
  - 我们在“规划”页面中按时间紧迫程度排序，放置此类任务，设置后App会周期性提醒用户
  - 同时，主页面中也会将最紧迫的事件列举出
- 紧急但不重要
  - 优先级仅次于第一类事件，但不同之处是对这些事件的超时有一定容忍度
  - 与上一类的区别是这类事件App不发出提醒，仅仅记录截止日期，避免平时干扰用户
- 重要但不紧急
  - 这些通常为一些人生中的“小目标”，不紧急、未计划、无DDL，但就是想要在未来去做，比如环球旅行
  - 我们在主页的生命电池下保存这些事件
  - 由于没有DDL，这类事件反倒是最容易被遗忘的，因此需要在重要时间节点，如节日、用户生日，对用户进行提醒
- 不重要且不紧急
  - 通常也就是一些平时零零散散的灵感或者想法
  - 同样在“仓库”页面中加以搜集

## 页面功能介绍

- 主页面：一颗电池，代表用户的人生剩余多少周的时间，点击弹出人生规划（即不设置DDL的事件）
- PlansActivity：“规划”页面，存放有DDL的事件
- StoreActivity：“仓库”页面
  - 存放一些电池，每颗电池代表该周需要做的事件，暂定共存放12颗（12周，近似三个月）
  - 每过去一周，该周电池变为空
  - 所有电池均变空后，页面刷新，获取新的一批电池（相当于从生命电池中重新取出）
- AddActivity：“添加”页面，用于添加新的事件
- StatisticActivity：“统计”页面，统计用户使用此App的情况，包括使用天数、完成任务数、超时任务数等等


