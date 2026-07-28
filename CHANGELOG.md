# theme-Xmao 更新日志

## 2.1.2

### 修复

- 修复首页“生活回想”图片浮层描述直接显示瞬间插件富文本标签的问题。
- 优化“生活回想”描述清理逻辑，先将富文本内容转换为纯文本，再压缩空白并截断展示，避免出现 `<p style="">` 等 HTML 片段。

### 验证

- 已通过 `node --check templates/assets/js/main.js`。

## 2.1.1

### 修复

- 修复启用 PJAX 与 Lenis 平滑滚动后，从其他页面返回首页时页面滚动边界未及时刷新，导致页脚下方出现大面积空白并可继续滚动的问题。
- 修复首页 Swiper、图片等异步内容加载后未同步刷新 Lenis 滚动高度的问题。
- 优化 PJAX 内容替换后的滚动复位流程，切页后会同步重置 Lenis 与浏览器原生滚动位置。
- 移除会误触发首页视觉样式变化的 `index-page` 强制注入逻辑，避免首页风向标、随想碎片等模块样式被错误改写。

### 验证

- 已通过 `node --check templates/assets/js/pjax.js`。
- 已通过 `node --check templates/assets/js/main.js`。
