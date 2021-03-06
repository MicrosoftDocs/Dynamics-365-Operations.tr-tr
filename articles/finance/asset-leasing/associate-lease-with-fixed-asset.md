---
title: Kiralamaları sabit varlıklarla ilişkilendirme
description: Bu konuda, mevcut bir sabit varlığın yeni bir kiralamayla nasıl ilişkilendirileceği açıklanır.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseDetail
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 02a17b8c995e8aa97384d8b855afb688324017d6
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881360"
---
# <a name="associate-fixed-assets-with-leases"></a>Kiralamaları sabit varlıklarla ilişkilendirme

[!include [banner](../includes/banner.md)]

Bu konuda, mevcut bir sabit varlığın yeni bir kiralamayla nasıl ilişkilendirileceği açıklanır. Bir sabit varlığı kiralamayla ilişkilendirdiğinizde, ilk kabuldeki kullanım hakkı (ROU) varlığı sabit varlığın alım maliyeti olur.

Sabit bir varlığı kiralamayla ilişkilendirmeden önce Sabit varlıklarda sabit varlık için bir kayıt oluşturmanız gerekir. Ardından, **Kiralama özeti** sayfasında kiralama oluşturmanız ve varlığı bu kiralamaya bağlamanız gerekir.

1. [Kiralama ekleme veya kopyalama](add-lease.md) konu başlığındaki adımları izleyerek kiralama ekleyin. **Kiralama ekle** sayfasındaki **Sabit varlık numarası** alanında henüz alınmamış olan varlığı seçin.
2. **Defterler**'i seçin ve ödeme planını onaylayın.
3. **İlk kabul**'ü seçin.
4. **Varlık kiralama günlüğü**'nü seçin.

    Kiralama için ilk kabul günlüğü girişi, genellikle ROU varlığı hesabına borçlandırılan tutar için sabit varlığı borçlandırır.

    Sabit varlıkla ilgili hareket türü ve defteri artık görüntüleyebilirsiniz.

5. **Günlük ayrıntılar**'ı seçin.
6. Günlük girişiyle ilgili ayrı satırları görüntülemek için **Satırlar**'ı seçin.
7. Varlığı içeren günlük girişini seçin ve ardından **Sabit Varlıklar** sekmesini seçin.

    **Sabit varlıklar** sekmesi hareket türünü ve defteri gösterir. Varsayılan olarak, **Hareket türü** alanı **Alım** olarak ayarlanır, **Defter** alanı sabit varlık için geçerli defter olarak ayarlanır.

İlk kabul günlüğü girişi deftere nakledildikten sonra, hareket sabit varlık için alım hareketi olarak görünür. Hareket tablosunu görüntülemek için **Sabit varlıklar \> Sabit varlıklar \> Sabit varlıklar** bölümüne gidin, uygun varlığı seçin ve **Değerlemeler**'i seçin. İlk kabul günlüğü girişinde belirtilen sabit varlık için bir alım hareketi oluşturulduğu görebilirsiniz.

Artık Sabit varlıklardaki standart amortisman işlevi kullanılarak sabit varlığa amortisman uygulanabilir. Amortisman hakkında daha fazla bilgi için bkz. [Amortisman yöntemleri ve kuralları](../fixed-assets/depreciation-methods-conventions.md).

> [!NOTE]
> Sabit varlığı bir kiralamayla ilişkilendirirseniz Varlık kiralamada **Varlık amortismanı** ve **Kira değer düşüşü** düğmeleri devre dışı bırakılır. Sabit varlıklardaki varlık amortismanı ve kira değer düşüşü hareketlerini görüntüleyebilirsiniz. Bir sorgu formu açan **Varlık hareketleri** düğmesi de devre dışı bırakılır. **Varlık hareketleri** sorgu formunu Sabit varlıklarda da açabilirsiniz.  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
