<<<<<<< HEAD
[![Version](https://img.shields.io/github/package-json/v/dmego/home.github.io)](https://www.npmjs.com/package/dmego-home-page)
[![Website](https://img.shields.io/website-up-down-green-red/http/i.dmego.cn.svg)](http://i.dmego.cn/)
[![License](https://img.shields.io/github/license/dmego/home.github.io.svg)](/LICENSE)
[![Say Thanks](https://img.shields.io/badge/Say-Thanks!-1EAEDB.svg)](https://saythanks.io/to/dmego)

### 个人主页

>这是我的个人主页

>衍生自 [Vno](https://github.com/onevcat/vno-jekyll) Jekyll 主题

>页面部分加载效果借鉴于 [Mno](https://github.com/mcc108/mno) Ghost 主题

>借鉴了[北岛向南的小屋](https://javef.github.io/)的头像样式

### 效果图

>静态图

![主页JPG](https://unpkg.com/dmego-home-page@latest/assets/img/home.jpg)

>动态图

![主页GIF](https://unpkg.com/dmego-home-page@latest/assets/img/home.gif)

### 注

- 访问地址：[个人主页](http://i.dmego.cn/)
- 使用了 [一言](http://hitokoto.cn/) 的 API 服务
- ~~使用了 [Bing 壁纸 API](https://github.com/xCss/bing/) 服务~~
- ~~使用了 [Yahoo Query Language (YQL)](https://developer.yahoo.com/yql/) 来解决获取 Bing 壁纸跨域问题~~
- ~~原先 YQL 服务将被淘汰，现改用 [JsonBird](https://bird.ioliu.cn/)~~
- 使用 `GitHub Action` 来获取 Bing 壁纸，使用 `JSONP` 获取 Bing 壁纸 URL 文件

### GitHub Action 补充说明

- 利用 `Github Action` 提交代码需要一个 `GitHub API` 令牌, 可以在 [Create Tokens](https://github.com/settings/tokens) 这个地址，点击 `Generate new token` 按钮来创建
  - `Expiration` 过期时间设置为 `No expiration`
  - `Select scopes` 勾选 `repo`
  - 点击 `Generate Token` 生成
- 在仓库的 `Settings` ——>`Secrets` 功能栏中，点击 `New repository secrets` 按钮
  -  在 `Name` 框中填写 `GH_TOKEN`
  - 在 `Secrets` 栏中填写第一步生成的 `Token` 值
- 详细配置步骤图可以参考《[GitHub Action 配置详细步骤](./ActionNotes.md)》文档

### 更新记录
- 2022-06-10
  - 发布 NPM 包，使用 UNPKG 作为资源文件的 CDN 
- 2023-02-27
  - 添加《GitHub Action 配置详细步骤》文档
- 2023-04-12
  - 移除 Jquery 依赖，使用原生 JS
- 2023-08-28
  - 将壁纸地址换成 cn.bing.com

### Star History

[![Star History Chart](https://api.star-history.com/svg?repos=dmego/home.github.io&type=Date)](https://star-history.com/#dmego/home.github.io&Date)

=======
# Unlock Music 音乐解锁

[![Build Status](https://ci.unlock-music.dev/api/badges/um/web/status.svg)](https://ci.unlock-music.dev/um/web)

- 在浏览器中解锁加密的音乐文件。 Unlock encrypted music file in the browser.
- Unlock Music 项目是以学习和技术研究的初衷创建的，修改、再分发时请遵循[授权协议]。
- Unlock Music 的 CLI 版本可以在 [unlock-music/cli] 找到，大批量转换建议使用 CLI 版本。
- 我们新建了 Telegram 群组 [`@unlock_music_chat`] ，欢迎加入！
- CI 自动构建已经部署，可以在 [um-packages] 下载

> **WARNING**
> 在本站 fork 不会起到备份的作用，只会浪费服务器储存空间。如无必要请勿 fork 该仓库。

[授权协议]: https://git.unlock-music.dev/um/web/src/branch/master/LICENSE
[unlock-music/cli]: https://git.unlock-music.dev/um/cli
[`@unlock_music_chat`]: https://t.me/unlock_music_chat
[um-packages]: https://git.unlock-music.dev/um/-/packages/generic/web-build/

## 特性

### 支持的格式

- [x] QQ 音乐 (.qmc0/.qmc2/.qmc3/.qmcflac/.qmcogg/.tkm)
- [x] Moo 音乐格式 (.bkcmp3/.bkcflac/...)
- [x] QQ 音乐 Tm 格式 (.tm0/.tm2/.tm3/.tm6)
- [x] QQ 音乐新格式 (.mflac/.mgg/.mflac0/.mgg1/.mggl)
- [x] <ruby>QQ 音乐海外版<rt>JOOX Music</rt></ruby> (.ofl_en)
- [x] 网易云音乐格式 (.ncm)
- [x] 虾米音乐格式 (.xm)
- [x] 酷我音乐格式 (.kwm)
- [x] 酷狗音乐格式 (.kgm/.vpr)
- [x] Android 版喜马拉雅文件格式 (.x2m/.x3m)
- [x] 咪咕音乐格式 (.mg3d)

### 其他特性

- [x] 在浏览器中解锁
- [x] 拖放文件
- [x] 批量解锁
- [x] 渐进式 Web 应用 (PWA)
- [x] 多线程
- [x] 写入和编辑元信息与专辑封面

## 使用方法

### 使用预构建版本

- 从 [Release] 或 [CI 构建][um-packages] 下载预构建的版本
  - :warning: 本地使用请下载`legacy版本`（`modern版本`只能通过 **http(s)协议** 访问）
- 解压缩后即可部署或本地使用（**请勿直接运行源代码**）

[release]: https://git.unlock-music.dev/um/web/releases/latest

### 自行构建

- 环境要求
  - nodejs (v16.x)
  - npm

1. 获取项目源代码后安装相关依赖：

   ```sh
   npm install
   npm ci
   ```

2. 然后进行构建：

   ```sh
   npm run build
   ```

   - 构建后的产物可以在 `dist` 目录找到。
   - 如果是用于开发，可以执行 `npm run serve`。

3. 如需构建浏览器扩展，构建成功后还需要执行：

   ```sh
   npm run make-extension
   ```
>>>>>>> 24ae873 (update website)
