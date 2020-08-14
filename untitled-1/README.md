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

## **Jenkins**

Triggers:

* Polling
* Github PR
* Gitlab MR
* Bitbucket PR
* Azure Repo MR
* API Trigger
* Other jobs

 ****[**https://www.jenkins.io/doc/pipeline/steps/workflow-scm-step/**](https://www.jenkins.io/doc/pipeline/steps/workflow-scm-step/)

## Github Actions

## GitLab-CI

Triggers:

* API
* Branches
* Chat
* External
* Github PRs
* Gitlab MRs
* Pipelines
* Pushes
* Schedules
* Tags
* Triggers
* Web
* GitLab Web IDE
* [Manual](https://docs.gitlab.com/ee/ci/yaml/README.html#whenmanual)

[https://docs.gitlab.com/ee/ci/yaml/README.html\#onlyexcept-basic](https://docs.gitlab.com/ee/ci/yaml/README.html#onlyexcept-basic)  
[https://docs.gitlab.com/ee/ci/yaml/README.html\#common-if-clauses-for-rules](https://docs.gitlab.com/ee/ci/yaml/README.html#common-if-clauses-for-rules)

## Azure Pipelines

[https://docs.microsoft.com/en-us/azure/devops/pipelines/repos/?view=azure-devops](https://docs.microsoft.com/en-us/azure/devops/pipelines/repos/?view=azure-devops)

## Travis-CI

[https://docs.travis-ci.com/user/tutorial/\#prerequisites](https://docs.travis-ci.com/user/tutorial/#prerequisites)

## Circle-CI

[https://circleci.com/docs/2.0/triggers/](https://circleci.com/docs/2.0/triggers/)  
[https://circleci.com/docs/2.0/getting-started/\#prerequisites-for-running-your-first-build](https://circleci.com/docs/2.0/getting-started/#prerequisites-for-running-your-first-build)  




  


