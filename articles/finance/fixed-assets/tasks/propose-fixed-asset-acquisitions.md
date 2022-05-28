---
title: Sabit kıymet alımları teklif etme
description: Bu konu, Sabit kıymetler günlüğündeki alım teklifi kullanılarak bir sabit kıymetin nasıl alındığını açıklar.
author: moaamer
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd54642e5ec6c56fbc3a5ebb07fc8fdaf5545926
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725694"
---
# <a name="propose-fixed-asset-acquisitions"></a>Sabit kıymet alımları teklif etme

[!include [banner](../../includes/banner.md)]

Bu konu, Sabit kıymetler günlüğündeki alım teklifi kullanılarak bir sabit kıymetin nasıl alındığını açıklar. Muhasebeci rolünü ve USMF adlı tüzel kişilik için tanıtım verilerini kullanır. Sabit kıymeti sabit kıymet teklif günlüğü aracılığıyla almak için önce sabit kıymet kaydını oluşturmanız ve sonra kıymet defterinde edinme fiyatını tanımlamanız gerekir.

## <a name="create-an-asset-acquisition-proposal"></a>Kıymet alım teklifi oluşturma

Bir kıymet Alım teklifi oluşturmak için aşağıdaki adımları tamamlayın. 

1. Gezinti bölmesinde **Modüller > Sabit kıymetler > Günlük girişleri> Sabit kıymetler günlüğü**'ne gidin.
2. **Yeni**'yi seçin.
3. **Ad** alanına bir değer girin veya buradan bir değer seçin.
4. Eylem Bölmesinde, **Satırlar**'ı seçin.
5. **Teklifler**'i seçin.
6. **Alım teklifi**'ni seçin.
7. **Filtre**'yi seç. Önceki değerleri temizlemek için **Sıfırla**'yı seçin.
8. **Sabit varlık numarası** satırını seçin.
9. **Ölçütler** alanında bir değer girin veya seçin. Bu teklifle almak istediğiniz sabit kıymetler için kalan ölçütleri ayarlayın.  
10. Bölmeden çıkmak için, iki kere **Tamam**'ı seçin.
- İşlem satırlarının oluşturulduğunu doğrulayın.  
- Yalnızca, defterde alım tarihi ve alım fiyatı ayarlanmış olan sabit kıymetler alım teklifine dahil edilir.  
11. Bu sayfada **Defterler** sekmesini seçin.
12. **Naklet**'i seçin.

## <a name="include-default-financial-dimensions-in-an-acquisition-proposal"></a>Alım teklifine varsayılan mali boyutları dahil et

Alım işlemi, **Sabit kıymetler > Günlük girişleri > Sabit kıymet günlüğü**'ne giderek Excel eklentileri kullanılarak oluşturulabilir. Yeni bir günlük oluşturun ve sayfadaki **satırlar** bölümüne gidin ve Excel simgesini seçin ve sonra bir sabit kıymet günlük satırı seçin. Sistem, günlük satırlarını temsil eden bir Excel şablonu oluşturur ve açar. Şablona eklemekte olduğunuz günlük satırları için veri ekleyebilir ve sonra bu bilgileri sisteme geri yayımlayabilirsiniz. 

Seçili kıymet defteri ve Excel şablonunda girilen ilgili sabit kıymetler için varsayılan boyutlar ayarlanmışsa, günlük, Excel'den sisteme yayımlandığında varsayılan finansal boyutlar kıymet defteri ana verilerinden çağrılır. Sabit kıymet günlüğünü Excel eklentisinden yayımlarken, bir kıymet defterine mali boyutları otomatik olarak eklemek için varsayılan boyutlar önceden ayarlanmalıdır.  


[!INCLUDE [footer-include](../../../includes/footer-banner.md)]
