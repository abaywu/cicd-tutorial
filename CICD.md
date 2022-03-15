# CI/CD 介紹

## 問題思考

當我們在開發軟體應用程式的時候會不會有這樣的思考？

- 如何縮短系統軟體開發週期?
- 報bug並且修正能不能更有效率?
- 這跟DevOps有沒有關係？

## 什麼是CI/CD?

何謂 CI/CD? CI是 Continuous Integration，CD是 Continuous Deployment，也就是持續整合與持續部署。簡單來說，就是把一些日常的建置環境、測試、build，一直到部署都交給自動化的工具。

## DevOps

![DevOps](https://upload.wikimedia.org/wikipedia/commons/thumb/0/05/Devops-toolchain.svg/512px-Devops-toolchain.svg.png)

DevOps（Development和Operations的組合詞）是一種重視「軟體開發人員（Dev）」和「IT運維技術人員（Ops）」之間溝通合作的文化、運動或慣例。通過自動化「軟體交付」和「架構變更」的流程，來使得構建、測試、發布軟體能夠更加地快捷、頻繁和可靠。

## Git Flow

專案開發一切重程式碼的本版控制開始。所有的參與的開發人員，如果可以遵循同一個規則來管理程式碼，如此一來在CI/CD的流程上便可以輕易管理。

- Vincent Driessen 
- The development model
- The branching model
- The branching strategy and release management

GitFlow的示意圖：

![gitflow](https://nvie.com/img/git-model@2x.png)

### Branch的類別

- The main branches
	- Master
	- Develop
- Supporting branches
	- Hotfix
	- Release
	- Feature

### Main branches

Master branch

- production ready state

Develop branch

- the latest delivered
- integration branch
- automatic nightly builds

![main branches](https://nvie.com/img/main-branches@2x.png)

### Supporting branches

Hotfix branch

- Branch off from:
	- Master
- Merge back:
	- Develop and Master
- Naming convention:
	- hotfix-*
- a critical bug in a production version must be resolved immediately

![hotfix branche](https://nvie.com/img/hotfix-branches@2x.png)

Release branch

- Branch off from:
	- Develop
- Merge back:
	- Develop and Master
- Naming convention:
	- release-*
- minor bug fixes
- preparing meta-data for a release
- Non targeted futures must wait until after the release branch is branched off

Feature branch

- Branch off from:
	- Develop
- Merge back:
	- Develop
- Naming convention:
	- feature-*
- exist in developer repos only, not in origin

![feature branch](https://nvie.com/img/merge-without-ff@2x.png)