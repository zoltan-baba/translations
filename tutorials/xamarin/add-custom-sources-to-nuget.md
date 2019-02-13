---
title: 独自の NuGet ソースの追加
redirect_from:
  - "/xamarin/add-custom-sources-to-nuget/"
  - "/xamarin/add-custom-sources-to-nuget"
menu:
  xamarin:
    weight: 3
---

アプリケーション内に NuGet によるサードパーティーパッケージを利用したい場合は,
それらのソースを自身の NuGet のソースに加える必要があります。

やることは単純で, あなたのワークフローに`Script`ステップを新たに追加し, 以下の内容の bash script を記述するだけです！

```
#!/bin/bash
set -ex

nuget sources add -Name NAME_FOR_SOURCE -Source SOURCE_URL
```

!!! 注意
`NAME_FOR_SOURCE`と`SOURCE_URL`のパラメーターを更新することと
`NuGet Restore Step`の前に`Script`ステップを追加することを忘れないでください。

### 認証情報が必要な NuGet ソースの場合

もしあなたの NuGet ソースに認証情報が必要な場合, 以下のように`Script`を変更してください。

```
#!/bin/bash
set -ex

nuget sources add -Name NAME_FOR_SOURCE -Source SOURCE_URL -UserName NUGET_USERNAME -Password NUGET_PASSWORD
```
