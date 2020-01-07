---
title: 在 openSUSE 15 上安装 .NET Core - 包管理器 - .NET Core
description: 使用包管理器在 openSUSE 15 上安装 .NET Core SDK 和运行时。
author: thraka
ms.author: adegeo
ms.date: 12/04/2019
ms.openlocfilehash: 0ea232438aa4c61e2064d0323dc706dffac15039
ms.sourcegitcommit: a4f9b754059f0210e29ae0578363a27b9ba84b64
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2019
ms.locfileid: "74998935"
---
# <a name="opensuse-15-package-manager---install-net-core"></a><span data-ttu-id="daca9-103">openSUSE 15 包管理器 - 安装 .NET Core</span><span class="sxs-lookup"><span data-stu-id="daca9-103">openSUSE 15 Package Manager - Install .NET Core</span></span>

[!INCLUDE [package-manager-switcher](./includes/package-manager-switcher.md)]

<span data-ttu-id="daca9-104">本文介绍如何使用包管理器在 openSUSE 15 上安装 .NET Core。</span><span class="sxs-lookup"><span data-stu-id="daca9-104">This article describes how to use a package manager to install .NET Core on openSUSE 15.</span></span> <span data-ttu-id="daca9-105">如果要安装该运行时，建议安装 [ASP.NET Core 运行时](#install-the-aspnet-core-runtime)，因为它同时包括 .NET Core 和 ASP.NET Core 运行时。</span><span class="sxs-lookup"><span data-stu-id="daca9-105">If you're installing the runtime, we suggest you install the [ASP.NET Core runtime](#install-the-aspnet-core-runtime), as it includes both .NET Core and ASP.NET Core runtimes.</span></span>

## <a name="register-microsoft-key-and-feed"></a><span data-ttu-id="daca9-106">注册 Microsoft 密钥和源</span><span class="sxs-lookup"><span data-stu-id="daca9-106">Register Microsoft key and feed</span></span>

<span data-ttu-id="daca9-107">安装 .NET 之前，需要：</span><span class="sxs-lookup"><span data-stu-id="daca9-107">Before installing .NET, you'll need to:</span></span>

- <span data-ttu-id="daca9-108">注册 Microsoft 密钥</span><span class="sxs-lookup"><span data-stu-id="daca9-108">Register the Microsoft key</span></span>
- <span data-ttu-id="daca9-109">注册产品存储库</span><span class="sxs-lookup"><span data-stu-id="daca9-109">register the product repository</span></span>
- <span data-ttu-id="daca9-110">安装必需的依赖项</span><span class="sxs-lookup"><span data-stu-id="daca9-110">Install required dependencies</span></span>

<span data-ttu-id="daca9-111">每台计算机只需要执行一次此操作。</span><span class="sxs-lookup"><span data-stu-id="daca9-111">This only needs to be done once per machine.</span></span>

<span data-ttu-id="daca9-112">打开终端并运行以下命令。</span><span class="sxs-lookup"><span data-stu-id="daca9-112">Open a terminal and run the following commands.</span></span>

```bash
sudo zypper install libicu
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
wget -q https://packages.microsoft.com/config/opensuse/15/prod.repo
sudo mv prod.repo /etc/zypp/repos.d/microsoft-prod.repo
sudo chown root:root /etc/zypp/repos.d/microsoft-prod.repo
```

## <a name="install-the-net-core-sdk"></a><span data-ttu-id="daca9-113">安装 .NET Core SDK</span><span class="sxs-lookup"><span data-stu-id="daca9-113">Install the .NET Core SDK</span></span>

<span data-ttu-id="daca9-114">更新可供安装的产品，然后安装 .NET Core SDK。</span><span class="sxs-lookup"><span data-stu-id="daca9-114">Update the products available for installation, then install the .NET Core SDK.</span></span> <span data-ttu-id="daca9-115">在终端中，运行以下命令。</span><span class="sxs-lookup"><span data-stu-id="daca9-115">In your terminal, run the following command.</span></span>

```bash
sudo zypper install dotnet-sdk-3.1
```

## <a name="install-the-aspnet-core-runtime"></a><span data-ttu-id="daca9-116">安装 ASP.NET Core 运行时</span><span class="sxs-lookup"><span data-stu-id="daca9-116">Install the ASP.NET Core runtime</span></span>

<span data-ttu-id="daca9-117">更新可供安装的产品，然后安装 ASP.NET 运行时。</span><span class="sxs-lookup"><span data-stu-id="daca9-117">Update the products available for installation, then install the ASP.NET runtime.</span></span> <span data-ttu-id="daca9-118">在终端中，运行以下命令。</span><span class="sxs-lookup"><span data-stu-id="daca9-118">In your terminal, run the following command.</span></span>

```bash
sudo zypper install aspnetcore-runtime-3.1
```

## <a name="install-the-net-core-runtime"></a><span data-ttu-id="daca9-119">安装 .NET Core 运行时</span><span class="sxs-lookup"><span data-stu-id="daca9-119">Install the .NET Core runtime</span></span>

<span data-ttu-id="daca9-120">更新可供安装的产品，然后安装 .NET Core 运行时。</span><span class="sxs-lookup"><span data-stu-id="daca9-120">Update the products available for installation, then install the .NET Core runtime.</span></span> <span data-ttu-id="daca9-121">在终端中，运行以下命令。</span><span class="sxs-lookup"><span data-stu-id="daca9-121">In your terminal, run the following command.</span></span>

```bash
sudo zypper install dotnet-runtime-3.1
```

## <a name="how-to-install-other-versions"></a><span data-ttu-id="daca9-122">如何安装其他版本</span><span class="sxs-lookup"><span data-stu-id="daca9-122">How to install other versions</span></span>

[!INCLUDE [package-manager-switcher](./includes/package-manager-heading-hack-pkgname.md)]