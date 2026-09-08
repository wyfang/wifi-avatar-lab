# Wi-Fi Avatar Lab

Design procedural 2D avatars, expressions, and animations in the browser, then export images or reusable components.

[Open app](https://wangyifang.com/web/wifi-avatar-lab/) · [Upstream project](https://github.com/smontlouis/bible-strong-avatar-lab) · [简体中文](./README.md)

## Features

- Create multiple avatars with geometric parameters and SVG.
- Edit faces, eyes, extra shapes, colors, perspective, and position.
- Save expressions and compose loops, transitions, blinks, and subtle movement.
- Export React, JavaScript, SVG, and PNG.
- Import and export complete projects as JSON.
- Use English, French, or Simplified Chinese interfaces.

Editing happens locally in the browser, with data kept in local storage. Export JSON before clearing the site's data.

## Usage

Requires Node.js 22.12+ and pnpm 10.34.5:

```bash
corepack enable
pnpm install --frozen-lockfile
pnpm dev
```

Build and preview:

```bash
pnpm build
pnpm preview
```

Run the full checks:

```bash
pnpm check
```

Regenerate `src/features/export/standaloneEngine.generated.ts` with `pnpm engine`; do not edit it directly.

## Notes

This project is derived from Stéphane Montlouis-Calixte's [Bible Strong Avatar Lab](https://github.com/smontlouis/bible-strong-avatar-lab), starting at upstream revision `1a341886dce6bc859e29d560123297aad7a125d0`. Modifications include Wi-Fi branding, Simplified Chinese, site metadata, a sharing image, and a standalone source entry point. Some icons and example characters still come from upstream.

Continue recording significant modifications in [NOTICE.md](./NOTICE.md). Do not describe upstream authorship, assets, or branding as original work by this project or as an official partnership.

## License

Project code is licensed under the [GNU Affero General Public License v3.0 only](./LICENSE). Upstream copyright belongs to Stéphane Montlouis-Calixte and contributors. Personal branding and assets are excluded. When distributing a modified version or making it available over a network, retain upstream attribution and modification notices and provide the complete corresponding source for the running version. See [license scope](./LICENSE_SCOPE.md).
