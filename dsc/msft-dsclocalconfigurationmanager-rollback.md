---
title: "MSFT_DSCLocalConfigurationManager クラスの RollBack メソッド"
ms.date: 2016-05-16
keywords: powershell,DSC
description: 
ms.topic: article
author: eslesar
manager: dongill
ms.prod: powershell
translationtype: Human Translation
ms.sourcegitcommit: c915ebd021ed20209bc491505d45cff2ac89f21d
ms.openlocfilehash: 771a9c7b50aba26f89dbf6b24eb3df67bafeac0a

---


# MSFT_DSCLocalConfigurationManager クラスの RollBack メソッド

構成を以前のバージョンにロールバックします。

構文
------

```mof
uint32 RollBack(
  [in] uint8 configurationNumber
);
```

パラメーター
----------

*configurationNumber* \[in\]  
要求された構成を指定します。 

## 戻り値
------------

成功した場合は 0 を返します。それ以外の場合はエラー コードを返します。

## コメント

これは静的メソッドです。

## 要件
------------
>**MOF:** DscCore.mof

>**名前空間**: Root\Microsoft\Windows\DesiredStateConfiguration


## 関連項目


[**MSFT_DSCLocalConfigurationManager**](msft-dsclocalconfigurationmanager.md)


 

 






<!--HONumber=Jun16_HO4-->


