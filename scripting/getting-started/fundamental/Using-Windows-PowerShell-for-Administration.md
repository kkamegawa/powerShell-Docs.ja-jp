---
title: "Windows PowerShell を管理に使用する"
ms.date: 2016-05-11
keywords: powershell,cmdlet
description: 
ms.topic: article
author: jpjofre
manager: dongill
ms.prod: powershell
ms.assetid: db6334ec-ace6-436d-ab88-77aefc817511
translationtype: Human Translation
ms.sourcegitcommit: 03ac4b90d299b316194f1fa932e7dbf62d4b1c8e
ms.openlocfilehash: f6d5477c32f8f254ab7280945847509588002e83

---

# Windows PowerShell を管理に使用する
Windows PowerShell の基本的目標は、より良く、より簡単なシステム管理を、対話式でもスクリプトでも提供することです。 この章では、Windows システムの管理に関する多くの問題への Windows PowerShell を使用した解決策を取り上げます。 Windows PowerShell ユーザー ガイドではスクリプトや関数について取り上げませんでしたが、後からスクリプトや関数で解決策を利用することができます。 問題の解決策の一部として、関数を含んだ例を示します。

解決策の説明全体を通し、特定のコマンドレット、一般的な Get\-WmiObject コマンドレット、さらには Windows および .NET Framework インフラストラクチャの一部である外部ツールを使用した解決策の組み合わせを使用します。 外部ツールの使用は、Windows PowerShell を長期的に使用するために意図されて設計されたものの一部です。\- システムが大きくなるにつれて、ユーザーは、使用できるツールセットでは必要なことすべてが行えない状況に絶えず直面することになります。 Windows PowerShell では、コマンドレットの実装だけに依存することを助長するのではなく、利用できるあらゆる代替シナリオの解決策を統合することをサポートしようとしています。




<!--HONumber=Jun16_HO4-->


