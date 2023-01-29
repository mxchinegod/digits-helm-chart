# digits-helm-chart
Kubernetes Helm Chart for the Digits app.

## 🚀 Usage

Edit your values.yaml to include the necessary configuration.

    helm install digits .

## 📝 Modify

    helm upgrade digits

## 🗑️ Uninstall

    helm uninstall digits

## 🚧 Dev
---
### 💻 Apple Silicon

Using Docker Desktop, you will want to pull any images which throw:

`🚨 ERROR: no matching manifest for linux/arm64/v8 in the manifest list entries`

using the following command yourself (i.e. do not let kubernetes try to pull the image for the first time):

    docker pull --platform linux/x86_64 dylanalloy/digits-api-main:latest

as an example. The `--platform` argument is key here until I can create ARM images with Github Actions.


# 🙋 Contribution 

##### Proper commit message format is required for automated changelog generation. Examples:

    [<emoji>] [revert: ?]<type>[(scope)?]: <message>

    💥 feat(compiler): add 'comments' option
    🐛 fix(compiler): fix some bug
    📝 docs(compiler): add some docs
    🌷 UI(compiler): better styles
    🏰 chore(compiler): Made some changes to the scaffolding
    🌐 locale(compiler): Made a small contribution to internationalization

    Other commit types: refactor, perf, workflow, build, CI, typos, tests, types, wip, release, dep