---
title: 2. Configure Hugo
weight: 30
pre: ''
---

### Configure Hugo

- Hugo Template

  1. Download Theme : [Link](https://amazon.awsapps.com/workdocs/index.html#/document/4345081821f097c60a74d5c7f1f8529639b4d7fc84eb672f70bfeac6b8a36324)
  2. Uncompress to folder.

- Edit config.toml (edit ./hugobasedhol/config.toml)
  - baseURL : your own hands on lab name
  - title
  - description
  - author

```
# baseURL
baseURL = "/hugobasedhol/"
languageCode = "en-US"
defaultContentLanguage = "en"

# title
title = "Title"
theme = "hugo-theme-learn"
themesdir = "."
metaDataFormat = "yaml"
defaultContentLanguageInSubdir= true
ignoreFiles = []

# description, author
[params]
description = "Description"
author = "Author Name"
showVisitedLinks = true
disableBreadcrumb = false
disableNextPrev = false
themeVariant = "aws"

[outputs]
home = [ "HTML", "RSS", "JSON"]

[Languages.en]
title = ""
weight = 1
languageName = "English"

[[Languages.en.menu.shortcuts]]
name = "<i class='fas fa-fw fa-bullhorn'></i> Credits"
url = "/credits/"
weight = 30
```

- Edit ./hugobasedhol/layout/partials/logo.html
  - href : same with baseUrl
  - src : baseUrl/image/logo.png

```html
<a id="logo" href="/hugobasedhol/">
  <img src="/hugobasedhol/images/logo.png" height="70px" />
</a>
```

---

<p align="center">
© 2020 Amazon Web Services, Inc. All rights reserved.
</p>
```
