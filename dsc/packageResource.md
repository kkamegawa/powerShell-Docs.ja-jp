---
title: "DSC Package リソース"
ms.date: 2016-05-16
keywords: powershell,DSC
description: 
ms.topic: article
author: eslesar
manager: dongill
ms.prod: powershell
translationtype: Human Translation
ms.sourcegitcommit: 6477ae8575c83fc24150f9502515ff5b82bc8198
ms.openlocfilehash: bcaf82cbafe67cc309765e16b3c9cd6eff0a982a

---

# DSC Package リソース

> 適用先: Windows PowerShell 4.0、Windows PowerShell 5.0

Windows PowerShell Desired State Configuration (DSC) の **Package** リソースは、Windows インストーラーや setup.exe パッケージなど、ターゲット ノードでパッケージをインストールまたはアンインストールするメカニズムを備えています。

## 構文

```
Package [string] #ResourceName
{
    Name = [string]
    Path = [string]
    ProductId = [string]
    [ Arguments = [string] ]
    [ Credential = [PSCredential] ]
    [ Ensure = [string] { Absent | Present }  ]
    [ LogPath = [string] ]
    [ DependsOn = [string[]] ]
    [ ReturnCode = [UInt32[]] ]
}
```

## プロパティ
|  プロパティ  |  説明   | 
|---|---| 
| 名前| 特定の状態を保証するパッケージの名前を示します。| 
| パス| パッケージが存在するパスを示します。| 
| ProductId| パッケージを一意に識別する製品 ID を示します。| 
| 引数| 指定されたとおりにパッケージに渡される引数の文字列を一覧表示します。| 
| Credential| リモート ソースのパッケージへのアクセスを提供します。 このプロパティは、パッケージのインストールには使用されません。 パッケージは常に、ローカル システムにインストールされます。| 
| Ensure| パッケージがインストールされるかどうかを示します。 このプロパティを "Absent" に設定すると、パッケージはインストールされません (またはパッケージがインストールされている場合はアンインストールされます)。 パッケージがインストールされるようにするには、"Present" に設定します (既定値)。| 
| LogPath| プロバイダーがパッケージをインストールまたはアンインストールするためのログ ファイルを保存する場所の完全パスを示します。| 
| DependsOn | このリソースを構成する前に、他のリソースの構成を実行する必要があることを示します。 たとえば、最初に実行するリソース構成スクリプト ブロックの ID が **ResourceName** で、そのタイプが **ResourceType** である場合、このプロパティを使用する構文は DependsOn = "[ResourceType]ResourceName" になります。| 
| ReturnCode| 想定されるリターン コードを示します。 実際のリターン コードがここで指定される想定される値と一致しない場合、構成はエラーを返します。| 

## 例

この例では、指定されたパスに配置され、指定された製品 ID が割り当てられている .msi インストーラーを実行します。

```powershell
Package PackageExample
{
    Ensure = "Present"  # You can also set Ensure to "Absent"
    Path  = "$Env:SystemDrive\TestFolder\TestProject.msi"
    Name = "TestPackage"
    ProductId = "ACDDCDAF-80C6-41E6-A1B9-8ABD8A05027E"
} 
```




<!--HONumber=Jun16_HO4-->


