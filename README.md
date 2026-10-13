# Hi, I am 沈炜丹 👋

岭南师范学院 · 计算机科学与技术 · 2027 届本科在读
求职方向：**嵌入式软件开发 / IoT 物联网开发 / 软件测试**（可提前到岗实习）

## 🔧 技术栈

- **语言**：C / Python / Java / SQL / Shell
- **嵌入式**：ESP32-S3、STM32、FreeRTOS、I2C / SPI / UART、LVGL、MQTT、OpenHarmony 设备开发
- **物联网云平台**：华为云 IoT（设备接入 / 属性上报 / 命令下发）、微信小程序联动
- **测试**：pytest 自动化测试框架、串口日志交叉验证
- **系统与运维**：Linux（Ubuntu）、Shell 脚本
- **数据库**：MySQL（JDBC）、SQLite、Oracle PL/SQL（课程学习）
- **数据与可视化**：pandas

> 说明：以上均为课程 / 项目中有真实实践的内容。Docker、Prometheus 等仅作了解，未系统学习，不列入技术栈。

## 📦 项目

### 嵌入式 / 物联网方向
| 项目 | 说明 |
| --- | --- |
| [stm32-esp8266-huaweicloud-iot](https://github.com/swdscsc/stm32-esp8266-huaweicloud-iot) | STM32+ESP8266 AT 指令接入华为云 IoT：MQTT 属性上报 + 小程序订阅 Topic 下发控制，端-云-端四层链路联调（含可运行的 MQTT 接入演示与原理讲解） |
| [esp32-esp-idf-training](https://github.com/swdscsc/esp32-esp-idf-training) | ESP32 (esp-idf) 实训进阶工程集：8 个由浅入深、均可独立编译运行的工程（hello-world→LED/按键/FreeRTOS/LVGL/QMI8658 姿态/WiFi 联网），体现完整嵌入式学习曲线 |
| [esp32-attitude-iot-dashboard](https://github.com/swdscsc/esp32-attitude-iot-dashboard) | ESP32-S3 姿态数据 MQTT(QoS1) 上云 + 云端命令控制 LED 双向通信 + Python(pandas) 采集分析 |
| [esp32-qmi8658-attitude-monitor](https://github.com/swdscsc/esp32-qmi8658-attitude-monitor) | ESP32-S3 + QMI8658 六轴姿态监测：I2C 驱动、姿态解算、LVGL 显示 |
| [esp32-freertos-task-queue](https://github.com/swdscsc/esp32-freertos-task-queue) | 上述项目的多任务改造：采集/解算/UI 三任务 + 双队列（FreeRTOS） |
| [esp32-wifi-station](https://github.com/swdscsc/esp32-wifi-station) | ESP32 WiFi STA/AP 双模式：事件组同步、断线重连、敏感信息脱敏 |
| [stm32-charging-monitor](https://github.com/swdscsc/stm32-charging-monitor) | 毕业设计（在研开源）：STM32 智能充电监控显示系统，ADC 采样 + 充电状态机 + 显示告警 |
| [openharmony-env-setup-guide](https://github.com/swdscsc/openharmony-env-setup-guide) | OpenHarmony 设备开发环境搭建实录：Ubuntu + Docker 编译 → mkimage.stm32 → 烧录排错 |

### 机器人方向
| 项目 | 说明 |
| --- | --- |
| [guidebot](https://github.com/swdscsc/guidebot) | 行人引导机器人：感知—规划—控制—触觉反馈闭环，含 Python / 仿真联调与跨平台验证 |

### Java / 数据处理方向
| 项目 | 说明 |
| --- | --- |
| [JavaClassScoreSystem](https://github.com/swdscsc/JavaClassScoreSystem) | JavaFX + SQLite 班级成绩管理：成绩文件解析、班级统计、数据库持久化、图形界面 |
| [log-analysis-toolkit](https://github.com/swdscsc/log-analysis-toolkit) | 零依赖 Python 日志分析：错误率/UV/TOP IP/慢请求/**故障接口定位**，输出 CSV + 自绘 HTML 报表 |

### 工具 / 实践
| 项目 | 说明 |
| --- | --- |
| [linux-server-health-check](https://github.com/swdscsc/linux-server-health-check) | Shell 服务器健康巡检：CPU/内存/磁盘/inode/负载/进程监控 + 阈值告警 + JSON 快照 |
| [mysql-backup-automation](https://github.com/swdscsc/mysql-backup-automation) | MySQL 备份恢复自动化：自动备份 + 6 项完整性校验 + 三重防护恢复流程 |
| [docker-monitoring-stack](https://github.com/swdscsc/docker-monitoring-stack) | docker compose 一键部署 Prometheus + Grafana + Node Exporter + Alertmanager（学习用） |

## 📮 联系

- 邮箱：3103141093@qq.com
- GitHub：github.com/swdscsc
