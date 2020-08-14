# Source Control and Triggers

## Overview

The first step in running a build in CI requires fetching the code, but before this happens systems need to be configured to as to when to clone the code. These are referred to as triggers and can happen a number of ways:

* Polling
* Scheduled / Cron
* On changes to the repository
* By external events: Webhooks, other CI systems
* Manually through the UI
* From a chat client ala _GitOpts_

Now the majority of systems support Git, or it’s predecessor SVN. But just triggering off of code changes does not provide CI without a report back to the system. The following table illustrates the systems and SCM products they integrate with.  
****

|  | **Git Repo** | **Github** | **GitLab** | **Bitbucket** | **Azure Repos** |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Jenkins** ℹ  | ✔ | ✔ | ✔ | ✔ | ✔ |
| **Github Actions** |  | ✔ |  |  |  |
| **Gitlab-CI** | ✔ | ✔ | ✔ | ✔ |  |
| **Azure Pipelines** |  | ✔ |  | ✔ | ✔ |
| **Travis-CI** |  | ✔ |  | ✔ |  |
| **Circle-CI** |  | ✔ |  | ✔ |  |

{% hint style="info" %}
**Jenkins:** With the exception of Git Repo, all platforms require plugins to be installed
{% endhint %}

