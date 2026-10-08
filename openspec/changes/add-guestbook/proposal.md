## Why

访客需要独立的站点交流入口，作者需要在内容公开前审核，避免未经审核的留言展示。

## What Changes

- 在全站导航“关于”后加入“留言”，指向独立 `/guestbook/` 页面。
- 访客免登录提交昵称和纯文本，所有新留言默认待审核。
- 后台增加留言列表、通过、拒绝和隐藏操作；只有通过审核的留言公开展示。
- 留言使用独立持久化存储，提交和审核不触发静态站点发布。

## Capabilities

### New Capabilities
- `guestbook`: 独立留言页面、公开提交读取、作者审核及访问控制。

### Modified Capabilities
无。

## Impact

涉及 Astro 导航和新增页面、Express API、后台界面与测试。使用 Node 内置 SQLite，数据存放在 ADMIN_DATA_DIR 中，不改变文章内容或发布模型。
