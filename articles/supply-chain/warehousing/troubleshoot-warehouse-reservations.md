---
title: Ambar yönetiminde rezervasyonlarla ilgili sorunları giderme
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta ambar rezervasyonları ile çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: d0d73396772ed9e8397797d6685fb550d911303b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828118"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a>Ambar yönetiminde rezervasyonlarla ilgili sorunları giderme

[!include [banner](../includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta ambar rezervasyonları ile çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.

Toplu iş ve seri numarası kayıtları ile ilgili konular için bkz. [Ambar toplu iş ve seri rezervasyon hiyerarşilerinde sorun giderme](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
