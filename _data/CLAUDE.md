# _data/ — 站点数据文件

Jekyll 数据文件目录，所有 YAML 文件通过 `site.data.xxx` 在模板中访问。

## 文件说明

| 文件 | 用途 | 模板引用 |
|------|------|----------|
| `profile.yml` | 个人信息（姓名、简介、教育、经历、奖项、社交链接） | `site.data.profile` |
| `display.yml` | 首页板块显示开关（experience、news、publications、visitor_statistics） | `site.data.display.homepage` |
| `navigation.yml` | 导航栏页面配置 | `site.data.navigation` |
| `authors.yml` | 论文合作者姓名与链接 | `site.data.authors` |

## profile.yml 结构

```yaml
primary_name: "显示名"
secondary_name: "全名"
navbar_name: "导航栏名称"
positions:
  - name: "身份描述"
    logo: /assets/images/badges/xxx.svg
email: "邮箱"
cv_link: /assets/CV/cv.pdf
github: GitHub用户名
short_bio: "HTML格式简介"
portrait_url: /assets/images/photos/profile.jpg
portrait_caption: "头像下方文字"
education:
  - name: "学校名"
    logo: "logo路径"
    position: "专业 学位"
    date: "时间"
experience:
  - name: "项目名"
    logo: "logo路径"
    position: "角色描述"
    date: "时间"
awards:
  - name: "奖项名"
    date: "时间"
```

## 注意事项

- `education`、`experience` 的 `logo` 字段必须指向存在的图片，否则会显示空图
- `awards` 不支持 logo，只显示名称和日期
- `display.yml` 中 `show_visitor_statistics: false` 已关闭访客统计
