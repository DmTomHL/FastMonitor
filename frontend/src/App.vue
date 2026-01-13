<template>
  <div id="app" class="app-container">
    <router-view />
  </div>
</template>

<script setup lang="ts">
</script>

<style lang="scss">
:root {
  /* 品牌色 - 沉稳、权威的深蓝 */
  --brand-primary: #0056b3;
  --brand-hover: #004494;

  /* 布局背景 */
  --bg-body: #f0f2f5;
  --bg-card: #ffffff;
  --bg-header: #001529;
  --bg-table-head: #fafafa;

  /* 文字颜色 */
  --text-main: #333333;
  --text-sub: #666666;
  --text-placeholder: #bfbfbf;
  --text-disabled: #999999;

  /* 边框与分割线 */
  --border-base: #d9d9d9;
  --border-light: #f0f0f0;

  /* 语义状态色 */
  --state-error-bg: #fff1f0;
  --state-error-border: #ffccc7;
  --state-error-text: #cf1322;
  --state-warn-bg: #fffbe6;
  --state-warn-border: #ffe58f;
  --state-warn-text: #d48806;
  --state-success-bg: #f6ffed;
  --state-success-border: #b7eb8f;
  --state-success-text: #389e0d;
  --state-info-bg: #e6f7ff;
  --state-info-border: #91d5ff;
  --state-info-text: #096dd9;

  /* Element Plus overrides */
  --el-color-primary: var(--brand-primary);
  --el-color-primary-light-3: #2f74c9;
  --el-color-primary-light-5: #5b96dc;
  --el-color-primary-light-7: #8bb7ed;
  --el-color-primary-light-8: #b9d6f7;
  --el-color-primary-light-9: #e6f1ff;
  --el-color-primary-dark-2: var(--brand-hover);

  --el-border-radius-base: 2px;
  --el-border-radius-small: 2px;
  --el-border-radius-round: 2px;

  --el-text-color-primary: var(--text-main);
  --el-text-color-regular: var(--text-main);
  --el-text-color-secondary: var(--text-sub);
  --el-text-color-placeholder: var(--text-placeholder);
  --el-text-color-disabled: var(--text-disabled);

  --el-border-color: var(--border-base);
  --el-border-color-light: var(--border-light);
  --el-border-color-lighter: var(--border-light);

  --el-bg-color: var(--bg-card);
  --el-bg-color-page: var(--bg-body);
  --el-bg-color-overlay: var(--bg-card);
  --el-fill-color-blank: var(--bg-card);
  --el-fill-color: #f5f7fa;
  --el-fill-color-light: #f2f4f7;
  --el-fill-color-lighter: #f7f9fc;
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html, body {
  height: 100%;
  overflow: hidden;
  font-family: "PingFang SC", "Microsoft YaHei", "Helvetica Neue", Arial, sans-serif;
  font-size: 14px;
  background: var(--bg-body);
  color: var(--text-main);
}

.app-container {
  width: 100%;
  height: 100vh;
  background: var(--bg-body);
  color: var(--text-main);
}

/* 表格 */
.el-table {
  border: 1px solid var(--border-base);
  border-radius: 2px;
}

.el-table th.el-table__cell {
  background: var(--bg-table-head);
  color: var(--text-sub);
  font-weight: 500;
}

.el-table td.el-table__cell {
  padding: 12px 16px;
  color: var(--text-main);
}

.el-table__body tr:hover > td.el-table__cell {
  background: var(--bg-table-head);
}

/* 表单与按钮 */
.el-input__wrapper,
.el-select .el-input__wrapper,
.el-textarea__inner {
  border-radius: 2px;
  min-height: 32px;
}

.el-input__wrapper.is-focus,
.el-select .el-input__wrapper.is-focus {
  box-shadow: 0 0 0 2px rgba(0, 86, 179, 0.2);
  border-color: var(--brand-primary);
}

.el-button {
  border-radius: 2px;
  min-height: 32px;
}

.el-button--primary {
  background: var(--brand-primary);
  border-color: var(--brand-primary);
}

.el-button--primary:hover {
  background: var(--brand-hover);
  border-color: var(--brand-hover);
}

/* 状态标签 */
.el-tag {
  border-radius: 2px;
  border-width: 1px;
}

.el-tag--success {
  background: var(--state-success-bg);
  border-color: var(--state-success-border);
  color: var(--state-success-text);
}

.el-tag--warning {
  background: var(--state-warn-bg);
  border-color: var(--state-warn-border);
  color: var(--state-warn-text);
}

.el-tag--danger {
  background: var(--state-error-bg);
  border-color: var(--state-error-border);
  color: var(--state-error-text);
}

.el-tag--info {
  background: var(--state-info-bg);
  border-color: var(--state-info-border);
  color: var(--state-info-text);
}

.el-tag__close {
  color: inherit;
}

/* 面板卡片 */
.el-card,
.el-tabs--border-card {
  border-radius: 2px;
  border-color: var(--border-base);
  box-shadow: none;
}

/* 统一滚动条 */
::-webkit-scrollbar {
  width: 8px;
  height: 8px;
}

::-webkit-scrollbar-track {
  background: var(--border-light);
}

::-webkit-scrollbar-thumb {
  background: var(--border-base);
  border-radius: 2px;
}
</style>
