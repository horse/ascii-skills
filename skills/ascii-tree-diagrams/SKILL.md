---
name: ascii-tree-diagrams
description: |
  ASCII 树形图技巧：层级结构、缩进、连接线。使用此技能绘制目录树、继承关系、
  组织结构等层级分明的信息。
triggers:
- /ascii-tree-diagrams
- 树形图
- tree
- 层级
- 目录
- 组织结构
---

# ASCII 树形图技巧

## 核心理念

树形图展示**层级关系**，让树状结构一目了然。

## 1. 基本结构

### 经典树形

```
根节点
├── 分支1
│   ├── 叶子1.1
│   └── 叶子1.2
├── 分支2
│   ├── 叶子2.1
│   └── 叶子2.2
└── 分支3
    └── 叶子3.1
```

### 符号说明

```
├──  → 带有同级兄弟的节点
└──  → 最后/唯一子节点
│    → 垂直连接线
    → 缩进（2 或 4 空格）
```

## 2. 连接线变体

### 方案一：经典风格

```
root
├── child1
│   └── grandchild1
├── child2
└── child3
```

### 方案二：紧凑风格

```
root
├─ child1
│  └─ grandchild1
├─ child2
└─ child3
```

### 方案三：双线风格

```
╔══════╗
║ root ║
╠══════╣
║ ├─ child1 ║
║ │  └─ gc1 ║
║ ├─ child2 ║
║ └─ child3 ║
╚════════╝
```

### 方案四：带方框

```
┌─────┐
│ root│
└──┬──┘
   │
   ├─► child1
   ├─► child2
   └─► child3
```

## 3. 实际应用示例

### 目录结构

```
project/
├── src/
│   ├── components/
│   │   ├── Button.tsx
│   │   ├── Input.tsx
│   │   └── Modal.tsx
│   ├── hooks/
│   │   ├── useAuth.ts
│   │   └── useTheme.ts
│   └── utils/
│       ├── format.ts
│       └── validate.ts
├── tests/
│   ├── unit/
│   └── e2e/
├── package.json
└── README.md
```

### 类继承关系

```
Animal (基类)
├── Mammal
│   ├── Dog
│   │   └── Poodle
│   ├── Cat
│   └── Whale
├── Bird
│   ├── Eagle
│   └── Penguin
└── Fish
    ├── Salmon
    └── Shark
```

### 组织结构

```
CEO
├── CTO
│   ├── 前端团队
│   │   ├── Web 组
│   │   └── Mobile 组
│   └── 后端团队
│       ├── API 组
│       └── 基础设施组
├── CFO
│   ├── 财务部
│   └── 审计部
└── COO
    ├── 运营部
    └── 客服部
```

## 4. 垂直树形

### 向下生长

```
        根
        │
    ┌───┴───┐
    │       │
   子1     子2
    │       │
  ┌─┴─┐   ┌─┴─┐
  │   │   │   │
 叶1 叶2  叶3 叶4
```

### 缩进风格

```
根
│
└── 子1
    │
    └── 孙1
        │
        └── 曾孙
```

### 紧凑版本

```
根
├─子1
│ ├─孙1
│ └─孙2
├─子2
└─子3
```

## 5. 多根树（森林）

```
森林:
┌─────┐     ┌─────┐
│ 树1 │     │ 树2 │
└──┬──┘     └──┬──┘
   │          │
   ├─叶子     ├─叶子
   └─叶子     └─叶子
```

## 6. 带编号的树

### 方案一：完全编号

```
1. 根
   1.1. 分支1
        1.1.1. 叶子1
        1.1.2. 叶子2
   1.2. 分支2
        1.2.1. 叶子3
```

### 方案二：路径编号

```
root (1)
├── child1 (1.1)
│   └── leaf1 (1.1.1)
└── child2 (1.2)
    └── leaf2 (1.2.1)
```

### 方案三：级别编号

```
Level 0: 根
  Level 1: 分支1
    Level 2: 叶子1
    Level 2: 叶子2
  Level 1: 分支2
    Level 2: 叶子3
```

## 7. 复杂示例

### 文件系统树（详细）

```
/
├── bin/                  # 可执行文件
│   ├── bash
│   ├── ls -> /coreutils/ls
│   └── sh -> /bash/sh
├── etc/                  # 配置文件
│   ├── passwd
│   ├── shadow
│   └── nginx/
│       ├── nginx.conf
│       └── sites-enabled/
│           └── default
├── home/                 # 用户目录
│   ├── user1/
│   │   ├── Documents/
│   │   ├── Downloads/
│   │   └── .config/
│   └── user2/
├── var/                  # 可变数据
│   ├── log/
│   │   ├── syslog
│   │   └── nginx/
│   │       └── access.log
│   └── cache/
└── tmp/                  # 临时文件
```

### API 端点树

```
API v1
├── /users
│   ├── GET    (列表)
│   ├── POST   (创建)
│   └── /{id}
│       ├── GET    (详情)
│       ├── PUT    (更新)
│       └── DELETE (删除)
├── /posts
│   ├── GET
│   ├── POST
│   └── /{id}
│       ├── GET
│       ├── PUT
│       ├── DELETE
│       └── /comments
│           ├── GET
│           └── POST
└── /auth
    ├── /login
    ├── /logout
    └── /refresh
```

### 决策树

```
问题: 需要服务器?
│
├─ 是
│   └─ 需要数据库?
│       ├─ 是
│       │   └─ 推荐: 云服务器 + RDS
│       └─ 否
│           └─ 推荐: 云服务器 + Redis
└─ 否
    └─ 需要数据库?
        ├─ 是
        │   └─ 推荐: 容器 + 云数据库
        └─ 否
            └─ 推荐: 静态托管 + CDN
```

## 8. 快速参考

```
基础:
├── 节点     (非最后)
└─ 节点     (最后)

连接:
│    竖线
├    T 形
└    L 形

缩进:
  2 空格（紧凑）
  4 空格（清晰）

常用树:
目录树   → 经典风格
继承树   → 紧凑风格
决策树   → 编号风格
```

## 下一步

- 基础：[ascii-foundations](ascii-foundations)
- 表格：[ascii-tables](ascii-tables)
- 流程：[ascii-flowcharts](ascii-flowcharts)
- 布局：[ascii-box-layouts](ascii-box-layouts)