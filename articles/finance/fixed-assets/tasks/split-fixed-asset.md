---
title: Sabit kıymeti parçalara ayırın
description: Bu makale bir kıymet defteri yüzdesini yeni bir kıymet defterine bölmeyi açıklar.
author: moaamer
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d7fe30702717f960a42fb2a118e0d12587024f5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880802"
---
# <a name="split-a-fixed-asset"></a>Sabit kıymeti parçalara ayırın

[!include [banner](../../includes/banner.md)]

Bu makale bir kıymet defteri yüzdesini yeni bir kıymet defterine bölmeyi açıklar. 

## <a name="create-a-new-fixed-asset"></a>Yeni bir sabit kıymet oluştur

1. Gezinti bölmesinde **Modüller \> Sabit kıymetler \> Sabit kıymetler \> Sabit kıymetler**'e gidin.
2. **Yeni**'yi seçin.
3. **Sabit kıymet grubu** alanında bir değer girin veya seçin. Sabit kıymet numarasını, bölme işleminde daha sonra kullanmak üzere not alın.
4. **Ad** alanına bir değer girin.
5. Formu kapatın.

## <a name="split-a-fixed-asset"></a>Sabit kıymeti bölme

Tam amortismana tabi bir kıymet bölünmeden önce, kıymet defteri durumunun elle **Kapalı**'dan **Açık**'a değiştirilmesi gerekir. Bu adım gereklidir, çünkü kıymetle ilgili işlemleri deftere nakletmeniz gerekiyorsa (örneğin, elden çıkarma satışı için) Defter durumunun **Açık** olması gerekir. **Genel muhasebe parametreleri** sayfasının **Genel** sekmesinde **Tek bir fiş içinde birden fazla harekete izin ver** parametresini de açmanız gerekir. Varlık defter durumu değiştirildikten ve bir fiş içinde birden fazla harekete izin verildikten sonra varlığı bölmek için aşağıdaki adımları tamamlayın.

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

1. Gezinti bölmesinde **Modüller \> Sabit kıymetler \> Günlük girişleri \> Sabit kıymetler günlüğü**'ne gidin.
2. Listede, bölme işlemiyle oluşturulan günlüğü seçin.
3. **Satırlar**'ı seçin.

    - Oluşturulan günlük satırlarını doğrulayın.
    - Değeri, bölünme işlemi sırasında belirtilen yüzde oranında azaltmak üzere, orijinal kıymet için bir Alım düzeltme hareketi oluşturulur.
    - Yeni kıymet için aynı tutarda bir düzeltme hareketi oluşturulur.

4. **Naklet**'i seçin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
