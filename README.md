# Hi, I am 沈炜丹 👋

岭南师范学院 · 计算机科学与技术 · 2027 届本科在读
求职方向：**嵌入式软件 / 测试开发 / IoT 物联网开发**（深圳 · 可连续实习 6 个月以上）

> 我的主线是「**设备侧开发 + 质量保障**」：既能写 STM32 / ESP32 的驱动与 FreeRTOS 任务，也能给它们搭自动化测试框架。会写 pytest 的人很多，既懂设备又会写测试框架的人不多——我把力气花在这个交叉点上。

## 📊 先看这四个（带量化结果，固定种子可复现）

| 项目 | 做了什么 | 结果 |
| --- | --- | --- |
| [device-test-harness](https://github.com/swdscsc/device-test-harness) | 设备侧自动化回归框架：pytest + 串口 AT 协议，三层分离（协议 / 设备 / 客户端），后端可插拔——模拟器零硬件可跑，改一个环境变量切真板子 | **55 条用例全通过**，**协议分支覆盖 15/15**，521 条命令、时延 P50 4.47ms |
| [test-framework](https://github.com/swdscsc/test-framework) | pytest 分层自动化框架：API 客户端封装 → 数据驱动（parametrize + JSON 场景矩阵）→ 页面级冒烟；自研 HTML 报告插件，导出 JUnit XML 接 CI | **26 条用例 100% 通过**，覆盖 400 / 401 / 404 错误分支 |
| [defect-detection](https://github.com/swdscsc/defect-detection) | 无需训练的经典 CV 流水线：中值差分 → 形态学 → 轮廓分析，按旋转包围盒判别划痕 / 污点 / 崩角 | **整体 F1 = 0.970**（P=1.0 / R=0.942），正常样本零误报 |
| [net-sentinel](https://github.com/swdscsc/net-sentinel) | 纯 Python 可解释规则引擎：端口扫描 / SYN 洪水 / 暴力破解 / 数据外泄四类检测 + SVG 告警报告 | 四类攻击 **P / R / F1 均 100%** |

四个项目都满足：`python xxx.py` 一条命令出报告、README 写清设计取舍（为什么不用 Canny、为什么 SYN 洪水要按「目标+端口」聚合、为什么设备测试必须做故障注入）、评测结果可复现。

> `device-test-harness` 是我认为最能说明「设备侧 + 质量保障」这个交叉点的项目：接口测试碰不到丢包、串包、半截帧、设备忙，而这些恰恰是固件联调里最常见的问题。它用一个可注入故障的模拟固件把这些场景全部变成可回归的用例。

## 🔧 技术栈

- **语言**：C / Python / Java / SQL / Shell
- **嵌入式**：ESP32-S3、STM32、FreeRTOS、I2C / SPI / UART / ADC / PWM、LVGL、MQTT、OpenHarmony 设备开发
- **物联网云平台**：华为云 IoT（设备接入 / 物模型 / 属性上报 / 命令下发）、微信小程序联动
- **测试与质量**：pytest 分层框架、数据驱动、接口测试、可视化报告、JUnit XML / CI
- **系统与运维**：Linux（Ubuntu）、Shell 脚本
- **数据库**：MySQL（JDBC）、SQLite、Oracle PL/SQL（课程学习）
- **数据与可视化**：pandas、NumPy、OpenCV

> 说明：以上均为课程 / 项目中有真实实践的内容。Docker、Prometheus 等仅作了解，未系统学习，不列入技术栈。

## 📦 全部项目

### 嵌入式 / 物联网
| 项目 | 说明 |
| --- | --- |
| [stm32-esp8266-huaweicloud-iot](https://github.com/swdscsc/stm32-esp8266-huaweicloud-iot) | STM32 + ESP8266 AT 指令接入华为云 IoT：MQTT 属性上报 + 小程序订阅 Topic 下发控制，端-云-端四层链路联调 |
| [esp32-esp-idf-training](https://github.com/swdscsc/esp32-esp-idf-training) | ESP-IDF 实训进阶工程集：8 个由浅入深、均可独立编译运行的工程（hello-world → LED/按键 → FreeRTOS → LVGL → QMI8658 姿态 → WiFi 联网） |
| [esp32-attitude-iot-dashboard](https://github.com/swdscsc/esp32-attitude-iot-dashboard) | ESP32-S3 姿态数据 MQTT(QoS1) 上云 + 云端命令控制 LED 双向通信 + pandas 采集分析 |
| [esp32-qmi8658-attitude-monitor](https://github.com/swdscsc/esp32-qmi8658-attitude-monitor) | ESP32-S3 + QMI8658 六轴姿态监测：I2C 驱动、姿态解算、LVGL 显示 |
| [esp32-freertos-task-queue](https://github.com/swdscsc/esp32-freertos-task-queue) | 姿态监测的多任务改造：采集 / 解算 / UI 三任务 + 双队列 |
| [esp32-freertos-peripheral-basics](https://github.com/swdscsc/esp32-freertos-peripheral-basics) | GPIO、按键中断、多任务创建与事件组同步基础实验 |
| [esp32-wifi-station](https://github.com/swdscsc/esp32-wifi-station) | WiFi STA / AP 双模式：事件组同步、断线重连、敏感信息脱敏管理 |
| [stm32-charging-monitor](https://github.com/swdscsc/stm32-charging-monitor) | 毕业设计（在研开源）：STM32 智能充电监控，ADC 采样 + 充电状态机 + 显示告警 |
| [openharmony-env-setup-guide](https://github.com/swdscsc/openharmony-env-setup-guide) | OpenHarmony 设备开发环境搭建实录：Ubuntu + Docker 编译 → mkimage.stm32 → 烧录排错 |

### 测试 / 安全 / 数据
| 项目 | 说明 |
| --- | --- |
| [device-test-harness](https://github.com/swdscsc/device-test-harness) | 设备侧自动化回归测试框架（55 用例 / 分支覆盖 15/15，故障注入 + 时延统计） |
| [test-framework](https://github.com/swdscsc/test-framework) | pytest 分层自动化测试框架（26 用例 100% 通过，JUnit XML 接 CI） |
| [net-sentinel](https://github.com/swdscsc/net-sentinel) | 网络入侵检测与可视化（四类攻击 P/R/F1 均 100%） |
| [defect-detection](https://github.com/swdscsc/defect-detection) | 工业表面缺陷视觉检测（F1 = 0.970） |
| [log-analysis-toolkit](https://github.com/swdscsc/log-analysis-toolkit) | 零依赖 Python 日志分析：错误率 / UV / TOP IP / 慢请求 / **故障接口定位**，输出 CSV + 自绘 HTML 报表 |
| [credit-card-fraud-detection](https://github.com/swdscsc/credit-card-fraud-detection) | 特征工程 + 不平衡采样 + Stacking 集成 + SHAP 可解释性 |

### 机器人
| 项目 | 说明 |
| --- | --- |
| [guidebot](https://github.com/swdscsc/guidebot) | 行人引导机器人：感知—规划—控制—触觉反馈闭环，Simulink / Stateflow + ANSI C 代码生成 |

### Java / 工具实践
| 项目 | 说明 |
| --- | --- |
| [JavaClassScoreSystem](https://github.com/swdscsc/JavaClassScoreSystem) | JavaFX + SQLite 班级成绩管理：文件解析、班级统计、数据库持久化、图形界面 |
| [JavaClassScoreSystem-v2](https://github.com/swdscsc/JavaClassScoreSystem-v2) | v2 重构：Java Swing + JDBC + MySQL |
| [linux-server-health-check](https://github.com/swdscsc/linux-server-health-check) | Shell 服务器健康巡检：CPU / 内存 / 磁盘 / inode / 负载 / 进程 + 阈值告警 + JSON 快照 |
| [mysql-backup-automation](https://github.com/swdscsc/mysql-backup-automation) | MySQL 备份恢复自动化：自动备份 + 6 项完整性校验 + 三重防护恢复流程 |
| [docker-monitoring-stack](https://github.com/swdscsc/docker-monitoring-stack) | docker compose 一键部署 Prometheus + Grafana + Node Exporter + Alertmanager（学习用） |

### 个人主页
| 项目 | 说明 |
| --- | --- |
| [swdscsc.github.io](https://swdscsc.github.io) | 个人作品集网站 |

## 📮 联系

- 邮箱：3103141093@qq.com
- 作品集：https://swdscsc.github.io
