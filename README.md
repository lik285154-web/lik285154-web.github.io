# 李坤的个人网站

[访问网站](https://lik285154-web.github.io/)

个人介绍、AI 应用项目、辅修与能力认证、实习经历、精选荣誉与成长记录。网页适配电脑和手机，支持首页小程序扫码体验、AI 小精灵与篮球互动、滚动渐入、卡片光影、明暗主题、动效暂停及证书放大。

## 下载与继续维护

本仓库的 `website-source.zip` 是可恢复的完整网站源码，顶层目录为 `site/`。下载该文件并解压，安装 Node.js 24 LTS 后，在 `site` 中运行：

```bash
npm ci
npm run dev
```

- 自我介绍、经历、奖项和项目：`site/src/content/profile.json`
- 国家级重点卡：同一内容文件中的 `nationalHonorHighlights`，用 `awardIds` 引用现有奖项
- 辅修、HCIP 备考与英语能力：同一内容文件中的 `learning`
- 成长记录：`site/src/content/notes/`
- 公开图片和证书：`site/public/media/`
- 完整维护说明：`site/README.md`

## 更新在线网站

在本地 `site` 目录完成修改后运行：

```bash
npm run check
npm run build
npm run package:source
```

新的 `website-source.zip` 生成在 `site` 上一级。通过本仓库 **Add file → Upload files** 上传同名压缩包并提交，GitHub Actions 会自动解压、构建、检查并发布。进入 **Actions** 确认 build 和 deploy 均成功，再打开网站检查。日常更新不需要改工作流。

压缩包不含 `node_modules`、构建产物、本地测试截图、私人材料、原始简历、私密配置或密钥。源码和公开素材可以随文件夹迁移；本地安装依赖后即可继续。静态网站目前通过内容文件维护，没有网页管理后台。

## 内容说明

精选 16 项荣誉，包括中国国际大学生创新大赛省级金奖 1 项、银奖 2 项，以及国家级、省级一二等奖和贵客松最佳技术实现奖。灵岐智小程序关联早期“苗遗智卫”的 6 项竞赛荣誉。四个项目分别介绍问题、思路、流程、关键功能与实践收获；研究成果包含已发表论文，以及逐项列出的 1 项已登记、2 项申请受理软件著作权。

荣誉展示位于首页小程序体验区之后，创新大赛和挑战杯优先展示；机器人及人工智能大赛、RAICOM、计算机设计大赛分别使用国家级荣誉卡，支持打开对应获奖证书。

独立学习区域重点介绍人工智能华为创新实验班 AI 视觉识别辅修、华为 HCIP 高级工程师认证备考和 CET-6 通过。原创 AI 小精灵吉祥物结合篮球和 AI 的个人热爱，关于区域可查看本人照片。

## 发布结构

- `website-source.zip`：可编辑网站源码及公开素材。
- `.github/workflows/deploy-pages.yml`：从压缩包构建并仅发布 `site/dist`。
- GitHub Pages Source：GitHub Actions。

本仓库保存发布版本的历史提交；解压后的 `site/` 可进一步改为直接源码仓库，但需使用源码版工作流。
