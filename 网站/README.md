# MINGYU ARCHIVE Community

可部署的金珉奎公开物料档案社区前端。当前内置 346 条历史索引作为迁移种子。

## 本地预览
不要直接双击 HTML（浏览器可能阻止 JSON fetch）。在目录运行 `python -m http.server 8000` 后访问 localhost:8000。

## 启用登录 / 评论 / 收藏数据库
1. 在 Supabase 新建项目。
2. SQL Editor 执行 `supabase/schema.sql`。
3. Table Editor → materials → Import CSV，导入 `supabase/materials_seed.csv`。
4. 在 `index.html` 底部填入项目 URL 与 anon key。anon key 是公开前端 key；不要放 service_role key。
5. 注册站长账号后，用 schema.sql 最后一行示例把自己的 role 改为 admin。

## 部署
整个目录可直接部署到 Vercel / Netlify / Cloudflare Pages。

## 权限
游客可读；登录用户可评论、收藏和投稿；moderator/admin 可维护物料；只有 admin 可删除正式物料。RLS 已写入 schema。

## 内容原则
优先官方原链接；失效链接保留状态；杂志和采访仅存索引、摘要和必要短摘录，不未经授权镜像完整版权内容。
