---
title: Şirketlerarası sipariş fiyatı farklılıklarını denetle
description: Bu konuda, şirketlerarası sipariş fiyatı uyuşmazlıkları açıklanmaktadır
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 3167077e653f2316f5ce54c2a07ef9c2978ecebb
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678332"
---
# <a name="check-intercompany-order-price-discrepancies"></a>Şirketlerarası sipariş fiyatı farklılıklarını denetle

[!include [banner](../../includes/banner.md)]

Şirketlerarası siparişlerde fiyat uyuşmazlıklarını kontrol etmek için bu yordamı kullanabilirsiniz.

1. **Tedarik ve kaynak atama \> Periyodik \> Temizle \> Şirketlerarası sipariş fiyatı farklılıklarını denetle**'ye gidin.
1. Gerekiyorsa bir toplu iş ayarlayın ve ardından şirketlerarası satış siparişleri ve satınalma siparişleri için fiyatları ve iskontoları denetlemek üzere **Tamam**'a tıklayın. Aksi takdirde, denetim gerçekleştirmeden sayfayı kapatmak için **İptal et**'i seçin.

    > [!TIP]
    > Fiyatlarla ilgili eşitleme sorunları veya sorunlar varsa bunlar, görüntülenecek bir bilgi iletisinde listelenir. Referans için bilgi iletisini yazdırabilirsiniz.

1. Bilgi iletisinde, geçerli tüzel kişilikteki siparişi açmak için ilgili satırı seçin. **Şirketlerarası**'nı seçip **Şirketlerarası satınalma siparişi** veya **Şirketlerarası satış siparişi** seçeneğini belirleyerek ilgili tüzel kişilikteki siparişi açın.

    > [!NOTE]
    > Şirketlerarası siparişe yönelik güncelleştirmeye izin vermek için:
    >
    > 1. **Alacak hesapları \> Müşteriler \> Tüm müşteriler**'e gidin.
    > 1. Eylem Bölmesi'nde, **Genel** sekmesini seçin ve ardından **Şirketlerarası** seçeneğini belirleyin.
    > 1. **Şirketlerarası** sayfasında, **Satınalma siparişi politikaları** veya **Satış siparişi politikaları**'nı seçin.
    > 1. İki alanda da **Fiyat düzenlemesine izin ver** ve **İskonto düzenlemesine izin ver**'i seçin.

1. Fiyatı tutmak istediğiniz ilgili şirketlerarası siparişi açın.
1. Her sipariş satırı için, satırın **Birim fiyat** alanını değiştirin ve ardından orijinal değerine geri değiştirin. Satır için **İskonto** alanını ileri geri değiştirin ve ilgili **Satınalmadaki masraflar** veya **Satış masrafları** alanlarını ileri geri değiştirin. Değerler ileri geri değiştirildiğinde fiyat, iskonto ve masrafların otomatik olarak hizalanacak şekilde bu şirketlerarası sipariş satırından başvurulan şirketlerarası sipariş satırına eşitlenmesi tetiklenir.

    > [!NOTE]
    > Bu eşitleme yalnızca şirketlerarası satış siparişi faturalanmamışsa geçerlidir. Şirketlerarası satış siparişinin faturası deftere nakledilmişse ve müşteri faturası günlüğü oluşturulmuşsa fiyat, iskonto ve masrafları şirketlerarası müşteri faturası günlüğündekilere eşit olarak ayarlayarak değişikliklerin doğrudan şirketlerarası satınalma sipariş satırlarında gerçekleştirilmesi gerekir. Yapılmamışsa sipariş toplamlarında uyumsuzluk olacağından şirketlerarası satınalma siparişi faturası deftere nakledilemez.

1. Tüm şirketlerarası satınalma ve satış siparişleri eşitlenene kadar yordamı tekrarlayın.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
