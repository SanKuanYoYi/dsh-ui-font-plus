# Changelog

## 0.9.7

Fork of [dsh-ui-font](https://github.com/warmwine/dsh-ui-font) 0.9.6 by warmwine.

### Fixed

- **代码字号轴**：全局字号滑杆现在同时驱动代码块、行内代码与工具输出（`--dsh-code-font-size`）。上游只重写 `var(--dsh-code-font-size, 11px)` 的兜底值，而该变量由 DSH 以行内样式写在 `body` 上，兜底值永远不生效，所以上游滑杆对代码族无效。本版额外发一条 `--dsh-code-font-size: Npx !important`，`--dsh-code-font-delta` 随之重算，字号与行高一起走。
- 新增 `perToken["markdown-code-block"]` 微调通道，与正文轴的 `perToken["markdown-base"]` 对称。

### Changed

- 包名 / 插件 id 改为 `dsh-ui-font-plus` / `ui-font-plus`，避免与上游 `dsh-ui-font` 同时安装时冲突。设置键（`ui-font`）与 API 路径（`/api/dsh-ui-font/*`）保持兼容，可直接沿用旧设置。

## 0.9.6 及更早

见上游 [CHANGELOG](https://github.com/warmwine/dsh-ui-font)。
