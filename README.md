# Wi-Fi Avatar Lab

> Wi-Fi 头像实验室：在浏览器中设计会表达、会动的程序化 2D 头像。

Wi-Fi Avatar Lab 是一个面向二次创作的头像设计工作室。它使用带有 3D 空间感的几何参数与 SVG 渲染，让你能够创建头像、定义中性外观和表情、编排可复用动画，并导出 React、JavaScript、SVG 或 PNG 资源。

本项目基于 [Bible Strong Avatar Lab](https://github.com/smontlouis/bible-strong-avatar-lab) 修改。应用名称、站点元数据和源码入口已更换为 Wi-Fi Avatar Lab；现有图标和示例角色仍沿用上游内容，后续会逐步替换为 Wi-Fi 品牌设计。原项目作者、来源和许可证信息见 [版权与来源](#版权与来源) 与 [NOTICE.md](./NOTICE.md)。

## 主要功能

- 创建、复制、排序和管理多个程序化头像。
- 调整脸部与附加几何体的尺寸、圆角、位置、旋转、透视和颜色。
- 分别或联动编辑双眼，并直接在画布上移动、旋转头像。
- 保存表情，设置临时颜色覆盖和自然的身体、眼部微动。
- 用表情序列制作动画，配置停留时间、转场、循环和眨眼。
- 导出可复用的 React 或原生 JavaScript 组件包。
- 导出透明或自定义背景的 SVG、PNG 图片。
- 用 JSON 导入、导出完整工作室项目。
- 使用英文、法文或简体中文界面。

所有编辑均在浏览器本地完成；项目数据保存在浏览器本地存储中，不需要账号或后端服务。清除网站数据前，请先导出 JSON 备份。

## 本地运行

### 环境要求

- Node.js 22.12 或更高版本
- pnpm 10.34.5（版本记录在 `package.json` 中）

### 安装与启动

```bash
pnpm install
pnpm dev
```

浏览器打开 [http://localhost:5173](http://localhost:5173)。

线上版本：[https://wangyifang.com/web/](https://wangyifang.com/web/)

### 常用命令

| 命令             | 用途                                     |
| ---------------- | ---------------------------------------- |
| `pnpm dev`       | 生成独立运行引擎并启动开发服务器         |
| `pnpm typecheck` | 执行 TypeScript 严格类型检查             |
| `pnpm test`      | 运行 Vitest 测试                         |
| `pnpm build`     | 构建生产版本到 `dist/`                   |
| `pnpm preview`   | 本地预览生产版本                         |
| `pnpm check`     | 完整执行生成检查、格式、类型、测试和构建 |

提交代码前建议运行：

```bash
pnpm check
```

## 技术组成

- React 19 + TypeScript
- Vite 8
- SVG 程序化渲染
- Motion 动画与高频渲染状态
- Tailwind CSS 4
- Vitest

主要目录：

| 路径                      | 内容                         |
| ------------------------- | ---------------------------- |
| `src/app/`                | 应用外壳、公共控件和全局样式 |
| `src/components/ui/`      | 可复用 UI 基础组件           |
| `src/features/avatar/`    | 头像、几何、表情和交互逻辑   |
| `src/features/animation/` | 动画序列与播放逻辑           |
| `src/features/rendering/` | SVG 场景和画布预览           |
| `src/features/export/`    | 图片、项目包和独立运行时导出 |
| `src/features/studio/`    | 工作室界面、状态与本地持久化 |
| `src/i18n/`               | 英文、法文和简体中文文案     |
| `docs/adr/`               | 架构决策记录                 |

更改项目文档格式或持久化逻辑前，请先阅读 [CONTEXT.md](./CONTEXT.md)。不要直接编辑 `src/features/export/standaloneEngine.generated.ts`，应运行 `pnpm engine` 重新生成。

## 二次开发状态

2026-08-14 建立 Wi-Fi Avatar Lab：

- 从上游 `main` 分支的提交 `1a341886dce6bc859e29d560123297aad7a125d0` 开始二次开发；
- 将新项目命名为 **Wi-Fi Avatar Lab（Wi-Fi 头像实验室）**；
- 建立本 README 与独立的来源、修改记录；
- 将应用品牌、网页元数据、PWA 信息和源码入口更新为 Wi-Fi Avatar Lab；
- 配置生产地址 `https://wangyifang.com/web/`，移除仅适用于 Vercel 的统计组件；
- 保留上游作者署名，暂未更改头像编辑功能、图标和示例角色素材。

今后的重要修改应继续在本节或 [NOTICE.md](./NOTICE.md) 中注明内容与日期，以满足 AGPL 对修改版本的通知要求。

## 同步上游

本项目自己的仓库配置为 `origin`，原作者仓库配置为 `upstream`：

```bash
git push -u origin main
```

需要获取上游更新时：

```bash
git fetch upstream
git merge upstream/main
```

## 版权与来源

- 上游项目：**Bible Strong Avatar Lab**
- 原作者：**Stéphane Montlouis-Calixte**
- 上游源码：[smontlouis/bible-strong-avatar-lab](https://github.com/smontlouis/bible-strong-avatar-lab)
- 上游网站：[avatars.bible-strong.app](https://avatars.bible-strong.app)

Wi-Fi Avatar Lab 是上游项目的修改版本，不代表原作者或与原作者存在官方合作关系。原项目及本修改版本均依据 [GNU Affero General Public License v3.0 only](./LICENSE) 发布。

### 上传 GitHub 与部署时必须遵守

- 保留完整的 `LICENSE`、原作者署名、版权和许可证通知。
- 明确说明项目已经修改，并记录重要修改内容和日期。
- 整个衍生项目继续采用 `AGPL-3.0-only`，不能改成闭源许可证或仅使用更宽松许可证。
- 分发构建产物时，同时以机器可读形式提供生成、安装、运行和修改所需的对应源码。
- 如果把修改版本部署为网站，必须在界面中给所有网络用户提供醒目的免费源码入口，并确保链接指向与线上版本一致的源码。
- 不要把上游作者的名称、网站、图标或示例素材表述成自己的原创或官方背书；替换素材时，只使用自己拥有权利或许可证兼容的内容。
- 保留第三方依赖的许可证与必要通知；新增字体、图片、音频和代码前先确认授权。
- 软件按“原样”提供，不附带任何明示或默示担保。

应用内的 “Source” 链接已指向本项目的[公开源码仓库](https://github.com/wyfang/wifi-avatar-lab)。React/JavaScript 导出包中包含程序衍生代码时，也应按 AGPL 要求提供源码。单纯使用工具创作的输出是否受 AGPL 约束，取决于输出本身是否包含受保护的程序代码或素材。

以上是根据仓库当前许可证整理的合规提示，不构成法律意见；完整且具有约束力的条款以 [LICENSE](./LICENSE) 为准。
