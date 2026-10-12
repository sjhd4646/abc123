# Week 05 — Pendulum Simulation Workspace

> **无菌工作区就绪状态 (Sterile Workspace Ready)**
> 状态：✅ 已初始化 / 🧪 待实验注入
> 锁定基线提交：`feat(week05): init pendulum experiment workspace`

---

## 1. 目录说明

本目录为第 5 周单摆仿真实验的**专属子模块**，
与课程主仓库的其他周次目录保持物理与逻辑上的隔离。
目录在创建后仅包含本实验所需文件，不携带任何外部依赖、构建产物或历史污染。

## 2. 无菌准则 (Sterility Rules)

为保证实验环境纯净，本目录遵循以下约束：

| 类别 | 允许 | 禁止 |
| --- | --- | --- |
| 源码 | 实验脚本、配置、文档 | 其它周次代码、复制粘贴的杂项 |
| 数据 | 实验输入参数 | 上一周遗留的输出、缓存 |
| 构建 | 明确的依赖清单 (`requirements.txt`) | 隐式全局环境依赖 |
| 元数据 | `.gitkeep`、`.gitignore` | IDE 个人配置、临时日志 |

## 3. 目录结构

```
week05_pendulum_sim/
├── README.md            # 本文件
├── .gitkeep             # 占位文件，确保空目录被 Git 跟踪
└── .gitignore           # 屏蔽 IDE/系统临时产物
```

后续实验文件将按以下约定填充：

```
pendulum.py             # 主仿真脚本
requirements.txt        # 依赖清单
data/                   # 实验输入数据
results/                # 实验输出（被 .gitignore 忽略）
```

## 4. 与主仓库的关系

* 子模块根路径：`week05_pendulum_sim/`
* 命名空间：完全独立，不与其它周次交叉引用
* 版本控制基线：已通过 `git commit` 在主仓库中锁定
* 后续每次实验进展将以独立 commit 追加，commit message 须以 `feat(week05):` 前缀开头

## 5. 复现步骤

```bash
# 1. 切换到课程主仓库根目录
cd <course-repo-root>

# 2. 进入本周子模块
cd week05_pendulum_sim

# 3. 拉取基线（如在另一台机器）
git pull
```

---

**请在注入实验代码前确认以上无菌状态；任何污染须立即通过 `git reset` 回退至本基线。**
