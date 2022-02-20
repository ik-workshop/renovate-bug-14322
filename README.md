# Renovate Bug Fix

Labels not set when there is an empty label.

---

![](https://img.shields.io/github/commit-activity/m/ik-workshop/renovate-bug-14322)
![](https://img.shields.io/github/last-commit/ik-workshop/renovate-bug-14322)
[![](https://img.shields.io/github/license/ivankatliarchuk/.github)](https://github.com/ivankatliarchuk/.github/LICENCE)
[![](https://img.shields.io/github/languages/code-size/ik-workshop/renovate-bug-14322)](https://github.com/ik-workshop/renovate-bug-14322)
[![](https://img.shields.io/github/repo-size/ik-workshop/renovate-bug-14322)](https://github.com/ik-workshop/renovate-bug-14322)
![](https://img.shields.io/github/languages/top/ik-workshop/renovate-bug-14322?color=green&logo=markdown&logoColor=blue)

---

[![governance][governance-badge]][governance-action]
[![governance.link-checker][governance.link-checker.badge]][governance.link-checker.status]

---

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
## Contents

- [Example](#example)
  - [Example 2](#example-2)
- [How to run](#how-to-run)
- [Create](#create)
- [Resources](#resources)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

---

## Example

### Example 2

- [Renovate config](./config-ex2.js)

```js
    {
      "matchUpdateTypes": ["major", "minor", "patch", "pin", "digest"],
      "addLabels": [process.env.TEAM_LABEL]
    }
```

Error, when `process.env.TEAM_LABEL` not set, it can be optional, config shared accross teams

```
ERROR: Repository has unknown error (repository=ik-workshop/renovate-bug-14322)
       "err": {
         "message": "Cannot read property 'addLabels' of null",
         "stack": "TypeError: Cannot read property 'addLabels' of null\n    at getFilteredObject (/usr/src/app/node_modules/renovate/lib/util/template/index.ts:162:22)\n    at /usr/src/app/node_modules/renovate/lib/util/template/index.ts:165:9\n    at Array.map (<anonymous>)\n    at getFilteredObject (/usr/src/app/node_modules/renovate/lib/util/template/index.ts:164:26)\n    at Object.compile (/usr/src/app/node_modules/renovate/lib/util/template/index.ts:184:40)\n    at generateBranchName (/usr/src/app/node_modules/renovate/lib/workers/repository/updates/branch-name.ts:87:34)\n    at applyUpdateConfig (/usr/src/app/node_modules/renovate/lib/workers/repository/updates/flatten.ts:59:21)\n    at flattenUpdates (/usr/src/app/node_modules/renovate/lib/workers/repository/updates/flatten.ts:126:28)\n    at branchifyUpgrades (/usr/src/app/node_modules/renovate/lib/workers/repository/updates/branchify.ts:21:19)\n    at lookup (/usr/src/app/node_modules/renovate/lib/workers/repository/process/extract-update.ts:113:36)\n    at extractDependencies (/usr/src/app/node_modules/renovate/lib/workers/repository/process/index.ts:96:31)\n    at Object.renovateRepository (/usr/src/app/node_modules/renovate/lib/workers/repository/index.ts:42:52)\n    at Object.start (/usr/src/app/node_modules/renovate/lib/workers/global/index.ts:150:7)\n    at /usr/src/app/node_modules/renovate/lib/renovate.ts:16:22"
       }
```

## How to run

## Create

[**Create a repository using this template →**][template.generate]

## Resources

- [Issue](https://github.com/renovatebot/renovate/issues/14328)
- [Bug fix](https://github.com/renovatebot/renovate/pull/14322)

<!-- resources -->
[template.generate]: https://github.com/ik-workshop/renovate-bug-14322/generate
[code-style.badge]: https://img.shields.io/badge/code_style-prettier-ff69b4.svg?style=flat-square

[governance-badge]: https://github.com/ik-workshop/renovate-bug-14322/actions/workflows/governance.bot.yml/badge.svg
[governance-action]: https://github.com/ik-workshop/renovate-bug-14322/actions/workflows/governance.bot.yml

[governance.link-checker.badge]: https://github.com/ik-workshop/renovate-bug-14322/actions/workflows/governance.links-checker.yml/badge.svg
[governance.link-checker.status]: https://github.com/ik-workshop/renovate-bug-14322/actions/workflows/governance.links-checker.yml
