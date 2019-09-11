---
title: Sabit kıymeti bölme
description: Bu konu bir kıymet defteri yüzdesini yeni bir kıymet defterine bölmeyi açıklar.
author: saraschi2
manager: AnnBe
ms.date: 08/06/2019
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
ms.openlocfilehash: a4e001a6fdf390c6211ba85aa327b60dcdf16d9e
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867595"
---
# <a name="split-a-fixed-asset"></a>Sabit kıymeti bölme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu konu bir kıymet defteri yüzdesini yeni bir kıymet defterine bölmeyi açıklar. Kılavuzda Muhasebeci rolü ve USMF demo verileri kullanılmaktadır.


## <a name="create-a-new-fixed-asset"></a>Yeni bir sabit kıymet oluştur
1. Gezinti bölmesinde **Modüller > Sabit kıymetler > Sabit kıymetler > Sabit kıymetler günlüğü**'ne gidin.
2. **Yeni**'yi seçin.
3. **Sabit kıymet grubu** alanında bir değer girin veya seçin. Sabit kıymet numarasını, bölme işleminde daha sonra kullanmak üzere not alın.  
4. **Ad** alanına bir değer yazın.
5. Formu kapatın.

## <a name="split-a-fixed-asset"></a>Sabit kıymeti bölme
1. Listede, bölünecek sabit kıymetin bağlantısını seçin.
2. **Defterler**'i seçin. Yeni kıymete bölünecek defteri seçin.  
3. **İşlevler**'i seçin.
4. **Sabit kıymet böl**'ü seçin.
5. **Sabit kıymet** alanına bir değer girin veya seçin.
6. **Deftere** alanında, aramayı açmak için açılır menü düğmesini seçin.
7. **Hareket tarihi** alanına bir tarih girin.
8. **Yüzde** alanına bir sayı girin.
9. **Günlük adı** alanına bir değer girin veya seçin.
10. **Tamam**'ı seçin.

## <a name="post-the-journal-transaction"></a>Günlük hareketini deftere nakledin
1. Gezinti bölmesinde **Modüller > Sabit kıymetler > Günlük girişleri> Sabit kıymetler günlüğü**'ne gidin.
2. Listede, bölme işlemiyle oluşturulan günlüğü seçin.
3. **Satırlar**'ı seçin.

    - Oluşturulan günlük satırlarını doğrulayın.  
    - Değeri, bölünme işlemi sırasında belirtilen yüzde oranında azaltmak üzere, orijinal kıymet için bir Alım düzeltme hareketi oluşturulur.  
    - Yeni kıymet için aynı tutarda bir düzeltme hareketi oluşturulur.  

4. **Naklet**'i seçin.

