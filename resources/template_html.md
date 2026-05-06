# HTML 简历模板

> 使用此模板时，将下方提示词发送给 Claude，它会根据母版中的个人信息和项目经历填充内容。

---

## 提示词

请使用以下 HTML 模板和 CSS 样式，根据 `resume_base.md` 中的全量信息生成一份完整的中文简历：

- 保持 HTML 结构和 CSS 样式完全不变
- 将个人信息、教育经历、工作经历、竞赛经历、社会实践、自我评价各节内容替换为母版中的实际内容
- 保留 `photo.jpg` 占位符，用户自行替换照片
- 项目符号统一使用 ⚫ 圆点
- 所有日期格式统一为"YYYY年MM月 ~ YYYY年MM月"
- 确保打印样式（`@media print`）完整保留

---

## HTML 代码骨架

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>姓名 - 个人简历</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Microsoft YaHei', 'SimSun', sans-serif;
            background: #f5f5f5;
            color: #222;
            font-size: 13.5px;
            line-height: 1.7;
        }

        .page {
            max-width: 860px;
            margin: 36px auto;
            background: #fff;
            padding: 48px 56px;
            box-shadow: 0 2px 16px rgba(0,0,0,0.08);
        }

        /* ===== 头部 ===== */
        .header {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            margin-bottom: 28px;
        }

        .header-left {
            flex: 1;
        }

        .header-left h1 {
            font-size: 26px;
            font-weight: 700;
            letter-spacing: 4px;
            margin-bottom: 6px;
            color: #111;
        }

        .header-left .meta {
            font-size: 13px;
            color: #444;
            line-height: 2;
        }

        .header-left .meta span {
            margin-right: 6px;
        }

        .header-right {
            width: 90px;
            height: 110px;
            border: 1px solid #ddd;
            overflow: hidden;
            flex-shrink: 0;
            margin-left: 24px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: #f0f0f0;
            color: #aaa;
            font-size: 12px;
        }

        .header-right img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        /* ===== 分割线 & 板块标题 ===== */
        .section {
            margin-bottom: 22px;
        }

        .section-title {
            font-size: 14px;
            font-weight: 700;
            color: #111;
            border-bottom: 1.5px solid #111;
            padding-bottom: 4px;
            margin-bottom: 12px;
            letter-spacing: 1px;
        }

        /* ===== 条目头行 ===== */
        .entry-header {
            display: flex;
            justify-content: space-between;
            align-items: baseline;
            margin-bottom: 2px;
        }

        .entry-header .date {
            font-size: 13px;
            font-weight: 700;
            color: #222;
            white-space: nowrap;
        }

        .entry-header .org {
            font-size: 13px;
            font-weight: 700;
            color: #222;
            text-align: center;
            flex: 1;
        }

        .entry-header .role {
            font-size: 13px;
            font-weight: 700;
            color: #222;
            text-align: right;
            white-space: nowrap;
        }

        /* ===== 正文段落 ===== */
        .entry-body {
            font-size: 13px;
            color: #333;
            line-height: 1.8;
            margin-bottom: 10px;
        }

        .entry-body p {
            margin-bottom: 2px;
        }

        /* ===== 带点列表 ===== */
        .bullet-list {
            list-style: none;
            padding: 0;
            margin: 4px 0 10px 0;
        }

        .bullet-list li {
            display: flex;
            align-items: flex-start;
            gap: 6px;
            font-size: 13px;
            color: #333;
            line-height: 1.8;
            margin-bottom: 3px;
        }

        .bullet-list li::before {
            content: '\26AB';
            font-size: 7px;
            margin-top: 7px;
            flex-shrink: 0;
            color: #222;
        }

        .bullet-list li b {
            font-weight: 700;
            color: #111;
        }

        /* ===== 教育经历特有样式 ===== */
        .edu-detail {
            font-size: 13px;
            color: #333;
            line-height: 1.85;
        }

        .edu-detail b {
            font-weight: 700;
            color: #111;
        }

        /* ===== 自我评价 ===== */
        .summary {
            font-size: 13px;
            color: #333;
            line-height: 1.9;
        }

        /* ===== 打印 ===== */
        @media print {
            body { background: #fff; }
            .page {
                margin: 0;
                box-shadow: none;
                padding: 36px 48px;
            }
        }
    </style>
</head>
<body>
<div class="page">

    <!-- 头部 -->
    <div class="header">
        <div class="header-left">
            <h1>姓　名</h1>
            <div class="meta">
                <div>男 丨 2005-04 丨 湖北省-武汉市</div>
                <div>学历 丨 手机号 丨 邮箱</div>
            </div>
        </div>
        <div class="header-right">
            <!-- 替换 src 为实际照片路径 -->
            <img src="photo.jpg" alt="证件照" onerror="this.parentNode.innerHTML='照片'">
        </div>
    </div>

    <!-- 教育经历 -->
    <div class="section">
        <div class="section-title">教育经历</div>
        <!-- 从 resume_base.md 填充 -->
    </div>

    <!-- 工作经历 -->
    <div class="section">
        <div class="section-title">工作经历</div>
        <!-- 从 resume_base.md 填充 -->
    </div>

    <!-- 专业竞赛 -->
    <div class="section">
        <div class="section-title">专业竞赛</div>
        <!-- 从 resume_base.md 填充 -->
    </div>

    <!-- 社会实践 -->
    <div class="section">
        <div class="section-title">社会实践</div>
        <!-- 从 resume_base.md 填充 -->
    </div>

    <!-- 个人项目 -->
    <div class="section">
        <div class="section-title">个人项目</div>
        <!-- 从 resume_base.md 填充 -->
    </div>

    <!-- 自我评价 -->
    <div class="section">
        <div class="section-title">自我评价</div>
        <div class="summary">
            <!-- 从 self_profile.md 填充 -->
        </div>
    </div>

</div>
</body>
</html>
```

---

## 使用说明

1. 生成简历时，Claude 会读取 `resume_base.md` 和 `self_profile.md`，将实际内容填入上述 HTML 骨架
2. 保持 CSS 样式完全不变，只替换内容
3. 用户将照片命名为 `photo.jpg` 放在 HTML 同目录下即可
4. 浏览器打开 HTML → 打印 → 另存为 PDF，即可获得 PDF 版简历
