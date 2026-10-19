# 铝产业全产业链数据看板

单文件 HTML 看板，覆盖 L1 铝土矿 → L5 铝加工全产业链。

## 数据
- 铝产业链数据.xlsx (44 sheet) · 近 5 年 (2021-10 → 当前)
- 41 个有效 sheet，月度/日度/分省/进口/库存/成本利润等

## 功能
- **9 个 Tab**：概览 / L1-L8 产业链层级
- **44 张图表**：年度对比 + 同比叠加（左右双轴单图）、日度含 30 日 MA
- **2026 数据加粗红色高亮**，#N/A 自动忽略
- **投资决策面板**（顶部）：
  - ⚡ 电解铝策略：原料/成本/供给/需求/库存 5 步，权重按数据异常度动态调整
  - 🧪 氧化铝策略：原料/成本/供给/进出口 4 步
  - 策略观点由 bull/bear 评分自动生成
- **目录侧边栏**（左下 📑）：所有 Tab + 思维导图快速跳转
- **数据框架思维导图** (`../data-framework/思维导图.html`)：12 层 · 274 项 · 颜色标注 Excel 覆盖情况

## 本地运行
```bash
# 看板已嵌入 echarts + data.json，单文件可直接打开
# 但 file:// 协议下 fetch 思维导图会失败，建议用本仓库 server：
cd ..
node start-server.js
# 访问 http://localhost:8765/
```

## 文件结构
- `index.html` — 看板 (3.6 MB, 自包含)
- `../dashboard/` — 生成脚本 (extract_data.js, generate.js)
- `../data-framework/` — 思维导图 (md + html)
- `../start-server.js` — 本地服务器

## 部署
- GitHub Pages 源：`main` 分支根目录
- 访问：`https://Kerr-hrc.github.io/aluminum-dashboard/`
