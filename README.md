# Wi-Fi Avatar Lab

在浏览器中设计程序化 2D 头像、表情与动画，并导出图片或可复用组件。

[在线使用](https://wangyifang.com/web/wifi-avatar-lab/) · [上游项目](https://github.com/smontlouis/bible-strong-avatar-lab) · [English](./README.en.md)

## 功能

- 用几何参数与 SVG 创建多个头像
- 编辑脸部、眼睛、附加形状、颜色、透视与位置
- 保存表情并编排循环、转场、眨眼与微动
- 导出 React、JavaScript、SVG 与 PNG
- 用 JSON 导入或导出完整项目
- 支持英文、法文与简体中文界面

全部编辑在浏览器本地完成，数据保存在本地存储；清除网站数据前应先导出 JSON。

## 使用

需要 Node.js 22.12+ 与 pnpm 10.34.5：

```bash
corepack enable
pnpm install --frozen-lockfile
pnpm dev
```

生产构建与预览：

```bash
pnpm build
pnpm preview
```

完整检查：

```bash
pnpm check
```

不要直接编辑 `src/features/export/standaloneEngine.generated.ts`，应运行 `pnpm engine` 重新生成。

## 说明

本项目基于 Stéphane Montlouis-Calixte 的 [Bible Strong Avatar Lab](https://github.com/smontlouis/bible-strong-avatar-lab)，从上游提交 `1a341886dce6bc859e29d560123297aad7a125d0` 开始二次开发。当前修改包括 Wi-Fi 品牌、简体中文、站点元数据、分享图与独立源码入口；部分图标和示例角色仍来自上游。

重要修改应继续记录在 [NOTICE.md](./NOTICE.md)，不要把上游作者、素材或品牌表述为本项目原创或官方合作。

## 版权说明

项目代码依据 [GNU Affero General Public License v3.0 only](./LICENSE) 发布。上游版权归 Stéphane Montlouis-Calixte 及其贡献者所有；个人品牌和素材不在许可范围内。分发或通过网络提供修改版时，应保留上游署名和修改通知，并提供与运行版本对应的完整源码，详见 [许可范围](./LICENSE_SCOPE.md)。
