---
title: 关于 GitHub Dependabot 版本更新
intro: '您可以使用 {{ site.data.variables.product.prodname_dependabot }} 来确保您使用的包更新到最新版本。'
redirect_from:
  - /github/administering-a-repository/about-github-dependabot
versions:
  free-pro-team: '*'
---

{{ site.data.reusables.dependabot.beta-note }}

### 关于 {{ site.data.variables.product.prodname_dependabot_version_updates }}

{{ site.data.variables.product.prodname_dependabot }} 负责维护您的依赖项。 您可以使用它来确保仓库自动跟上它所依赖的包和应用程序的最新版本。

通过将配置文件检入仓库，可启用 {{ site.data.variables.product.prodname_dependabot_version_updates }}。 配置文件指定存储在仓库中的清单或其他包定义文件的位置。 {{ site.data.variables.product.prodname_dependabot_short }} 使用此信息来检查过时的软件包和应用程序。 {{ site.data.variables.product.prodname_dependabot_short }} 确定依赖项是否有新版本，它通过查看依赖的语义版本 ([semver](https://semver.org/)) 来决定是否应更新该版本。 当 {{ site.data.variables.product.prodname_dependabot_short }} 发现过时的依赖项时，它会发起拉取请求以将清单更新到依赖项的最新版本。 检查测试是否通过，查看拉取请求摘要中包含的更改日志和发行说明，然后合并它。 更多信息请参阅“[启用和禁用版本更新](/github/administering-a-repository/enabling-and-disabling-version-updates)”。

如果启用安全更新，{{ site.data.variables.product.prodname_dependabot }} 还会发起拉取请求以更新易受攻击依赖项。 更多信息请参阅“[配置 {{ site.data.variables.product.prodname_dependabot_security_updates }}](/github/managing-security-vulnerabilities/configuring-github-dependabot-security-updates)”。

{{ site.data.reusables.dependabot.dependabot-tos }}

### {{ site.data.variables.product.prodname_dependabot }} 拉取请求的频率

在配置文件中指定检查每个生态系统的新版本的频率：每日、每周或每月。

{{ site.data.reusables.dependabot.initial-updates }}

如果您启用了安全更新，有时会看到额外的安全更新拉取请求。 这些由默认分支上依赖项的 {{ site.data.variables.product.prodname_dependabot_short }} 警报所触发。 {{ site.data.variables.product.prodname_dependabot }} 自动提出拉取请求以更新有漏洞的依赖项。

### 支持的仓库和生态系统

{% note %}

{{ site.data.reusables.dependabot.private-dependencies }}

{% endnote %}

您可以为包含其中一个受支持包管理器的依赖项清单或锁定文件的仓库配置版本更新。

{{ site.data.reusables.dependabot.supported-package-managers }}

如果您的仓库已使用集成进行依赖项管理，则在启用 {{ site.data.variables.product.prodname_dependabot }} 前需要禁用此集成。 更多信息请参阅“[关于集成](/github/customizing-your-github-workflow/about-integrations)”。