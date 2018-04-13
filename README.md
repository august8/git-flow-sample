# git-flow-sample
git-flow のテスト

## Git-flowの導入
```bash
$ brew install git-flow
```

## 初期処理
```bash
$ git flow init
```

```shell-session
Which branch should be used for bringing forth production releases?
   - master
Branch name for production releases: [master]
Branch name for "next release" development: [develop]

How to name your supporting branch prefixes?
Feature branches? [feature/]
Release branches? [release/]
Hotfix branches? [hotfix/]
Support branches? [support/]
Version tag prefix? []

$ git branch
* develop
  master
```

## 機能作成のためのfeatureブランチの作成
```bash
$ git flow feature start top
```

```shell-session
Switched to a new branch 'feature/top'

Summary of actions:
- A new branch 'feature/top' was created, based on 'develop'
- You are now on branch 'feature/top'

Now, start committing on your feature. When done, use:

    git flow feature finish top
```
```bash
$ git branch
```
```shell-session
     develop
   * feature/top
     master
```

## ローカルに作成したfeatureブランチをリモートへpush
```bash
$ git flow feature publish top
```
```shell-screen
Total 0 (delta 0), reused 0 (delta 0)
To https://github.com/august8/git-flow-sample.git
 * [new branch]      feature/top -> feature/top
Already on 'feature/top'
Your branch is up to date with 'origin/feature/top'.

Summary of actions:
- A new remote branch 'feature/top' was created
- The local branch 'feature/top' was configured to track the remote branch
- You are now on branch 'feature/top'
```

## リモートから最新の状態をPull
```bash
$ git flow feature pull origin top
```
```shell-screen
Pulled origin's changes into feature/top.
```
