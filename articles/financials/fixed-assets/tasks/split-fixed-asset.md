---
title: Sabit kıymeti bölme
description: Bu görev kılavuzu bir kıymet defteri yüzdesini yeni bir kıymet defterine böler.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8e5fdc8a7b326daca1fc0f0962c69bb8fb1ff64
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839725"
---
# <a name="split-a-fixed-asset"></a>Sabit kıymeti bölme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu görev kılavuzu bir kıymet defteri yüzdesini yeni bir kıymet defterine böler.  Kılavuzda Muhasebeci rolü ve USMF demo verileri kullanılmaktadır.


## <a name="create-a-new-fixed-asset"></a>Yeni bir sabit kıymet oluştur
1. Sabit kıymetler > Sabit kıymetler > Sabit kıymetler menüsüne gidin.
2. Yeni'ye tıklayın.
3. Sabit kıymet grubu alanında bir değer girin veya seçin.
4. Sabit kıymet numarasını, bölme işleminde daha sonra kullanmak üzere not alın.
5. İsim alanına bir değer yazın.
6. Formu kapatın.

## <a name="split-a-fixed-asset"></a>Sabit kıymeti bölme
1. Listede, bölünecek sabit kıymeti seçin.
2. Listede, seçili satırdaki bağlantıya tıklayın.
3. Defterler'e tıklayın.
    * Yeni kıymete bölünecek defteri seçin.  
4. İşlevler'i tıklatın.
5. Sabit kıymet parçala'ya tıklayın.
6. Sabit kıymet alanına bir değer girin veya seçin.
7. Deftere alanında, aramayı açmak için açılır menü düğmesine tıklayın.
8. Hareket tarihi alanına bir tarih girin.
9. Yüzde alanına bir sayı girin.
10. Günlük adı alanına bir değer girin veya seçin.
11. Tamam'a tıklayın.

## <a name="post-the-journal-transaction"></a>Günlük hareketini deftere nakledin
1. Sabit kıymetler > Günlük girişler > Sabit kıymetler günlüğü'ne gidin.
2. Listede, bölme işlemiyle oluşturulan günlüğü seçin.
3. Satırlar seçeneğine tıklayın.
    * Oluşturulan günlük satırlarını doğrulayın.  Değeri, bölünme işlemi sırasında belirtilen yüzde oranında azaltmak üzere, orijinal kıymet için bir Alım düzeltme hareketi oluşturulur.  Yeni kıymet için aynı tutarda bir düzeltme hareketi oluşturulur.  
4. Deftere Naklet öğesine tıklayın.

