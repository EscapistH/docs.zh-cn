---
title: dotnet remove reference 命令
description: dotnet remove reference 命令可便于删除项目间引用。
ms.date: 02/14/2020
ms.openlocfilehash: 92d36bbbde64d806abc8f223c5f08e3f3d79ce9d
ms.sourcegitcommit: 927b7ea6b2ea5a440c8f23e3e66503152eb85591
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/16/2020
ms.locfileid: "81463447"
---
# <a name="dotnet-remove-reference"></a>dotnet remove reference

**本文适用于：** ✔️ .NET Core 2.x SDK 及更高版本

## <a name="name"></a>名称

`dotnet remove reference` - 删除“项目到项目”引用。

## <a name="synopsis"></a>摘要

```dotnetcli
dotnet remove [<PROJECT>] reference [-f|--framework <FRAMEWORK>] <PROJECT_REFERENCES>

dotnet remove reference -h|--help
```

## <a name="description"></a>说明

使用 `dotnet remove reference` 命令可方便地从项目删除项目引用。

## <a name="arguments"></a>参数

`PROJECT`

目标项目文件。 如果未指定，此命令会搜索当前目录来获取一个项目文件。

`PROJECT_REFERENCES`

要删除的项目到项目 (P2P) 引用。 可指定一个或多个项目。 基于 Unix/Linux 的终端支持 [Glob 模式](https://en.wikipedia.org/wiki/Glob_(programming))。

## <a name="options"></a>选项

- **`-h|--help`**

  打印出有关命令的简短帮助。

- **`-f|--framework <FRAMEWORK>`**

  仅在以特定[框架](../../standard/frameworks.md)为目标时删除引用。

## <a name="examples"></a>示例

- 从指定项目删除项目引用：

  ```dotnetcli
  dotnet remove app/app.csproj reference lib/lib.csproj
  ```

- 从当前目录中的项目删除多个项目引用：

  ```dotnetcli
  dotnet remove reference lib1/lib1.csproj lib2/lib2.csproj
  ```

- 使用 Unix/Linux 的 glob 模式删除多个项目引用：

  ```dotnetcli
  dotnet remove app/app.csproj reference **/*.csproj`
  ```
