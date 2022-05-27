# SEO优化

## 结果统计对比
工具: `SEMRUSH` (付费)

- 优化前: ![Before](./before.PNG)
- 优化后: ![After](./after.PNG)
- 竞争对手(mouser): ![After](./mouser.PNG)

**总体提升了14%，超出竞争对手26%。**仍然遗留了些许问题，由于项目在重构，后续优化将在重构后的站点上进行。

[google search seo doc](https://developers.google.com/search/docs/basics/get-started)

## seo优化历程

### 语义化标签
- `<title>`: 网页主题
- `<header>`: 页眉
- `<footer>`: 页尾
- `<nav>`: 导航
- `<aside>`: 侧边栏
- `<main>`: 网页主体
- `<article>`: 定义外部的内容，其中的内容独立于文档的其余部分
- `<section>`: 定义文档中的区。
- `<hn>`: 标题
- `<ul>`: 无序列表
- `<ol>`: 有序列表
- `<strong>`: 强调文本，粗体
- `<small>`: 呈现小号字体效果，输入免责声明、注解、署名、版权。
- `<em>`: 强调文本，斜体
- `<mark>`: 黄色文本，一般用于关键词搜索后标记搜索内容。

需要注意的是：
- 不要因为`strong em`等标签的样式去使用，`html`应关注内容和语义，样式交给`css`
- `<hn>`中`<h1>`的权重最高，但是一个页面尽可能只出现一次，放置网页中最重要的信息，滥用会降低搜索引擎中的权重比例。
- `<h2> ~ <h6>`虽然可以多次使用，但是需要安排好结构，例如：`<h3>`应该是`<h2>`的子标题，不能反过来。

### 站点地图 `sitemap.xml`
在搜索引擎上传，以便允许其抓取`Sitemap`提供的所有网址，并了解使用相关元数据的网址。使用`Sitemap`协议并不能保证网页会包含在搜索引擎中，但可向网络抓取工具提供一些提示以便它们更有效地抓取网站。示例：
``` html
<?xml version="1.0" encoding="UTF-8"?>
<urlset
  xmlns="http://www.sitemaps.org/schemas/sitemap/0.9"
  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://www.sitemaps.org/schemas/sitemap/0.9
        http://www.sitemaps.org/schemas/sitemap/0.9/sitemap.xsd">
  <url>
    <loc>https://www.lcsc.com/</loc>
    <lastmod>2022-03-21T03:32:32+00:00</lastmod>
    <priority>1.00</priority>
  </url>
</urlset>
```

### 字体加载`font-display`

`css`中使用`font-display: swap;`，字体文件未加载前显示系统字体，加载完后切换为web字体。

### 网页`TDK`
- title
- keyword
- description
**为了防止重复而降低评分，可以加料唯一值，例如商品编号**

### 结构化数据 
结构化数据是网页中一段固定格式的字符串，是个网页内容的元数据。搜索引擎通过结构化数据可以更好的理解页面内容，在搜索结果中，以富媒体方式展示搜索内容。
使用方式：
``` html
  <head>
    <title>Executive Anvil</title>
    <script type="application/ld+json">
    {
      "@context": "https://schema.org/",
      "@type": "Product",
      ...
    }
    </script>
  </head>
```
具体配置见文档 [google search seo doc](https://developers.google.com/search/docs/basics/get-started)

