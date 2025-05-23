# 智能行车路线规划系统

作者 CSDN：mp9只想干开发   https://blog.csdn.net/2301_78947898?spm=1011.2266.3001.5343
     WeChat: mp9
## 项目简介

基于A*算法的智能行车路线规划系统，提供直观的图形界面和交互式操作体验。系统能够在地图上规划最优路径，支持障碍物避让和实时路径显示。
![img.png](img.png)

### 主要特点

- 交互式地图界面
- 智能路径规划
- 实时路径显示
- 动态障碍物避让
- 路径统计信息
- 现代化界面设计

## 系统要求

- Python 3.9+
- 操作系统：Windows/macOS/Linux
- 显示器分辨率：1024x768+

## 安装说明

1. 克隆项目到本地：
```bash
git clone [项目地址]
cd luxianguihua
```

2. 创建并激活虚拟环境（推荐）：
```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

3. 安装依赖包：
```bash
pip install -r requirements.txt
```

## 启动说明

1. 确保已激活虚拟环境（如果使用）

2. 运行主程序：
```bash
python -m route_planner.main
```

## 使用指南

### 基本操作

1. 选择起点和终点
   - 左键点击地图上的节点选择起点
   - 再次左键点击其他节点选择终点
   - 系统会自动计算并显示最优路径

2. 重置路径
   - 按R键重置当前路径
   - 可以重新选择起点和终点

3. 显示控制
   - 按H键显示/隐藏信息面板
   - 按ESC键退出程序

### 界面说明

1. 地图区域
   - 蓝色线条：可通行的道路
   - 红色线条：障碍物
   - 绿色节点：起点
   - 红色节点：终点
   - 黄色动画：当前路径

2. 信息面板
   - 系统标题
   - 操作说明
   - 路径统计信息（计算用时、路径长度、起终点信息）

## 项目结构

```
luxianguihua/
├── README.md
├── requirements.txt
└── route_planner/
    ├── __init__.py
    ├── main.py          # 主程序入口
    ├── graph.py         # 图数据结构
    ├── astar.py         # A*算法实现
    └── visualization.py # 可视化模块
```

### 核心模块说明

1. graph.py
   - 实现图数据结构
   - 管理节点和边的连接
   - 支持网格图的创建

2. astar.py
   - 实现A*路径规划算法
   - 使用欧几里得距离作为启发函数
   - 支持带权重的路径规划

3. visualization.py
   - 实现图形界面
   - 处理用户交互
   - 管理动画效果

4. main.py
   - 程序入口
   - 集成各个模块
   - 管理程序流程

## 技术特点

1. A*算法优化
   - 使用优先队列优化搜索效率
   - 支持动态障碍物避让
   - 保证找到最优路径

2. 交互设计
   - 实时路径显示
   - 动画效果反馈
   - 直观的操作方式

3. 可视化效果
   - 现代化界面设计
   - 清晰的路径显示
   - 动态的动画效果

## 常见问题

1. 中文显示问题
   - 系统会自动尝试加载系统中可用的中文字体
   - 如果出现乱码，请确保系统安装了中文字体

2. 性能问题
   - 路径计算时间与地图大小相关
   - 建议使用分辨率1024x768或更高

3. 操作响应
   - 点击有0.3秒的冷却时间
   - 防止重复触发和误操作

## 开发说明

### 依赖包版本

```
numpy==1.24.3
pygame==2.5.0
```

### 扩展建议

1. 功能扩展
   - 添加多种路径规划算法
   - 支持自定义地图导入
   - 增加路径导出功能

2. 界面优化
   - 添加缩放功能
   - 支持自定义主题
   - 增加更多交互方式

3. 性能优化
   - 优化大规模地图的显示
   - 改进路径计算效率
   - 添加多线程支持

## 贡献指南

欢迎提交Issue和Pull Request来帮助改进项目。在提交代码前，请确保：

1. 代码符合项目的编码规范
2. 添加了必要的注释和文档
3. 通过了基本的测试

## 许可证

本项目采用MIT许可证。详见LICENSE文件。

## 联系方式

如有问题或建议，请通过以下方式联系：

- 提交Issue
- 发送邮件至：1353632408@qq.com

## 致谢

感谢所有为项目做出贡献的开发者。 