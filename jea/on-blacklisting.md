---
description: 
manager: dongill
ms.topic: article
author: jpjofre
ms.prod: powershell
keywords: powershell,cmdlet,jea
ms.date: 2016-06-22
title: "ブラックリストへの登録"
ms.technology: powershell
translationtype: Human Translation
ms.sourcegitcommit: 7504fe496a8913718847e45115d126caf4049bef
ms.openlocfilehash: 8892e5e08a763fbc66d782bbc9252d1f3a7dcfcf

---

### ブラックリストへの登録
JEA を一通り試したら、コマンドをブラックリストに登録できるか気になるかもしれません。
これはもっともな要求ですが、現時点では次の理由で JEA ではその予定はありません。

1.  JEA では、オペレーターの操作を、オペレーターが必要なアクションにのみ制限しています。
ブラックリストは、その対極に位置します。

2.  PowerShell コマンドの設計者は、その設計時に JEA を念頭に置いていませんでした。
Windows Server 2016 の初期インストール時には、1520 個のコマンドを直ちに使用できるようになります。
これらのコマンドの脅威モデルには、ユーザーがより特権の高いアカウントとしてコマンドを実行するようになるという可能性は含まれていませんでした。
たとえば、特定のコマンドでは、設計上のコード インジェクションが許可されます (コア PowerShell モジュールの Add-Type や Invoke-Command など)。
マイクロソフトは、認識しているコマンドが公開されると JEA により警告を表示できますが、新しい脅威モデルに基づいて Windows の他のすべてのコマンドを再評価することはしていません。
JEA を通じて公開するコマンドの機能はご自身で把握している必要があります。  

3.  また、JEA がコード インジェクションの脆弱性によりすべてのコマンドをブロックしていても、悪意のあるユーザーがブラックリストに掲載された操作を他の関連するコマンドで実行できなくなるという保証はありません。
特定の操作を確実に実行されないようにするには、公開するすべてのコマンドを理解しておくことが不可欠です。
ホワイトリストまたはブラックリストの使用の有無にかかわらず、ご自身の判断のもと、公開するコマンドを選択してください。
ブラックリストで公開されるコマンドは管理することが困難なため、JEA は代わりにホワイトリストを使って実装されます。




<!--HONumber=Jul16_HO1-->


