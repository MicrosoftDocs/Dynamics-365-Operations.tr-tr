---
title: Ambar yönetiminde rezervasyonlarla ilgili sorunları giderme
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta ambar rezervasyonları ile çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a9a5d20732a802fc58c392853af8334bbc07de73
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248727"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a>Ambar yönetiminde rezervasyonlarla ilgili sorunları giderme

[!include [banner](../includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta ambar rezervasyonları ile çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a>Şu hata iletisini alıyorum: "Rezervasyonlara dayanan iş oluşturulduğu için rezervasyonlar silinemedi."

### <a name="issue-description"></a>Sorun açıklaması

Satır karşılığında açık iş bulunduğundan bir satış satırındaki stok ayırmayı geri alamazsınız.

### <a name="issue-resolution"></a>Sorunun çözümü

Maddeyi bir paketleme istasyonundan başka bir konuma (*Baydoor* gibi) getirmek için açık paketleme grubu işinin bulunup bulunmadığını araştırın. Stok ayırma işlemini fiziksel olarak neyin yaptığını belirlemek için **İş oluşturma geçmişi günlüğü** ve **İş ayrıntıları** sayfalarındaki kayıtları gözden geçirin ve daha sonra ayırmayı geri almak için işi tamamlayın veya silin.

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a>Şu hata iletisini alıyorum: "Stok miktarı %1, %2 maddesi için yetersiz stok hareketi nedeniyle güncelleştirilemedi..."

### <a name="issue-description"></a>Sorun açıklaması

Bu sorun, belirtilen boyutlara sahip yeterli stok hareketi bulunmadığından, sistem bir stok miktarını güncelleştiremediği takdirde oluşabilir. Tam hata iletisinin tüm metni şöyledir:

> %12 Lot Kimliği ve %11 başvuru kodu için boyutları Boyut=%3, Renk=%4, Ekler=%5, Tesis=%6, Ambar=%7, Konum=%8, Stok durumu=Mevcut, Plaka=%9, Parti numarası=%10 olan %2 maddesi için yeterli stok hareketi olmadığından %1 stok miktarı güncelleştirilemedi.

### <a name="issue-resolution"></a>Sorunun çözümü

Hiçbir stok hareketinin fiziksel olarak miktar ayırmadığından emin olun. Örneğin, bu hareketler açık kalite emirleri, stok bloke kayıtları veya çıkış emirleri olabilir.

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a>Şu hata iletisini alıyorum: "Fiziksel eldeki miktar... stokta yalnızca 0,00 mevcut olduğundan ayrılamaz."

### <a name="issue-description"></a>Sorun açıklaması

Bu sorun, belirtilen boyutlara sahip yeterli stok hareketi bulunmadığından, sistem bir stok miktarını güncelleştiremediği takdirde oluşabilir. Tam hata iletisinin tüm metni şöyledir:

> Fiziksel eldeki miktar Tesis=%1, Ambar=%2, Stok durumu = Mevcut, Parti numarası=%3, Sahip=%4: Stokta yalnızca 0,00 mevcut olduğundan %5 ayrılamaz.

### <a name="issue-resolution"></a>Sorunun çözümü

Bu sorun büyük olasılıkla açık olan bir iş nedeniyle oluşur. İşi tamamlayın ya da iş oluşturma işlemi olmadan alın. Hiçbir stok hareketinin fiziksel olarak miktar ayırmadığından emin olun. Örneğin, bu hareketler açık kalite emirleri, stok bloke kayıtları veya çıkış emirleri olabilir.

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a>Şu hata iletisini alıyorum: "Dalgaya atanması için yük satırlarının konum üzerindeki boyutları belirtmelidir. Bu boyutları atamak için yük satırını ayırın ve yeniden oluşturun."

### <a name="issue-description"></a>Sorun açıklaması

"Yukarıdaki parti" rezervasyon hiyerarşisine sahip bir madde kullandığınızda (**Konum** boyutunun *üzerine* yerleştirilen **Parti numarası** boyutu ile), Kısmi bir miktar için **Yük planlama çalışma ekranı** sayfasındaki **Ambara serbest bırak** komutu çalışmaz. Bu hata iletisini alırsınız ve kısmi miktar için hiçbir iş oluşturulmaz.

Ancak, "aşağıdaki parti" ayırma hiyerarşisine sahip bir madde kullandığınızda (**Konum** boyutunun *altına* yerleştirilen **Parti numarası** boyutu ile), kısmi bir miktar için **Yük planlama çalışma ekranı** sayfasından bir yükü ambara serbest bırakabilirsiniz.

### <a name="issue-resolution"></a>Sorunun çözümü

Bu davranış tasarımdan kaynaklanır. Ayırma hiyerarşisindeki **Konum** boyutunun üzerine bir boyut eklerseniz ambara serbest bırakma işlemi öncesinde belirtilmelidir. Microsoft bu sorunu değerlendirmiş ve yük planlama çalışma ekranından ambara serbest bırakma sırasında bir özellik kısıtlaması oluştuğunu tespit etmiştir. **Konum** üzerinde bir veya daha fazla boyut belirtilmemişse kısmi miktarlar serbest bırakılamaz.

Daha fazla bilgi için bkz. [Esnek ambar düzeyi boyut rezervasyonu ilkesi](flexible-warehouse-level-dimension-reservation.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]