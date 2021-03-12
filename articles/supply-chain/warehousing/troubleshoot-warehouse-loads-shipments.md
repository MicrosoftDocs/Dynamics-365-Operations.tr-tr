---
title: Yük oluşturma ve sevkiyatlar ile ilgili sorunları giderme
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta yük oluşturma ve sevkiyatlarla çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.
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
ms.openlocfilehash: f49a91afe9281f912d6d3579ac8e52cb1d8e5b5d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994066"
---
# <a name="troubleshoot-load-building-and-shipments"></a>Yük oluşturma ve sevkiyatlar ile ilgili sorunları giderme

[!include [banner](../includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta yük oluşturma ve sevkiyatlarla çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.

## <a name="i-receive-the-following-error-message-you-cant-create-a-load-line-for-this-order-line-because-it-contains-inventory-dimensions-that-are-invalid"></a>Şu hata iletisini alıyorum: "Sipariş satırı, geçersiz stok boyutları içerdiğinden bu sipariş için yükleme satırı oluşturamazsınız..."

### <a name="issue-description"></a>Sorun açıklaması

Ambara bir iade satış siparişini serbest bırakmaya çalıştığınızda aşağıdaki hata iletisini alırsınız:

> Sipariş satırı, geçersiz stok boyutları içerdiğinden bu sipariş için yükleme satırı oluşturamazsınız. Rezervasyon hiyerarşisinde konum boyutunun altında bulunan stok boyutlarına referans veremezsiniz. Sipariş satırından geçersiz boyutları kaldırın.

### <a name="issue-resolution"></a>Sorunun çözümü

Ne yazık ki, ürün bir satış iade işlemi için yük işlemeyi desteklemiyor. Bu nedenle, iade satış siparişini ambara serbest bırakamazsınız.

Satış siparişi hareketlerinde, rezervasyon hiyerarşisinde **Konum** boyutunun altında bulunan stok boyutlarına referans veremezsiniz. Çözüm, sipariş satırından geçersiz boyutları kaldırmaktadır.

## <a name="i-receive-the-following-error-message-one-of-the-lines-is-already-on-a-load-unable-to-release-to-warehouse"></a>Şu hata iletisini alıyorum: "Satırlardan biri zaten bir yükte yer alıyor. Ambara serbest bırakılamıyor."

### <a name="issue-description"></a>Sorun açıklaması

Yükleri el ile oluşturursanız veya süreci satış siparişi satırı girişi gerçekleşmeden önce yükler oluşturulacak şekilde ayarlarsanız sonraki serbest bırakmanın el ile yapılacağı ve yükün rotası ve değerlendirmesinin kullanılacağı varsayılır.

Başka bir olası senaryoda, ambara otomatik olarak serbest bırakma işlemi yapmaya çalışırsınız ancak dalga süreci işi oluşturamaz. Bu nedenle, açık bir sevkiyat veya yük yine de oluşturulur. Bu açık sevkiyat veya yük, açık sevkiyatı ya da yükü silinceye veya dalgayı el ile yeniden işleyinceye kadar, siparişin otomatik olarak serbest bırakılmasını deneyen sonraki girişimleri engeller.

### <a name="issue-resolution"></a>Sorunun çözümü

Yalnızca ambara serbest bırakmadan önce yük yoksa, satış siparişi sayfasından serbest bırakabilirsiniz veya otomatik serbest bırakma oluşturulabilir. Dalga işlendikten sonra yük otomatik olarak oluşturulacaktır.

## <a name="i-receive-the-following-error-message-the-delivery-note-correction-cant-be-processed-the-delivery-note-only-contains-items-that-are-subject-to-warehouse-management-processes-as-these-are-not-supported-by-delivery-note-correction"></a>Şu hata iletisini alıyorum: "Teslim notu düzeltmesi işlenemiyor. Teslimat notu yalnızca Teslimat Notu Düzeltmesi tarafından desteklenmeyen, ambar yönetim süreçlerine tabi olan maddeleri içerir."

### <a name="issue-description"></a>Sorun açıklaması

Teslim notunu deftere naklettikten sonra iptal edemiyorsunuz çünkü **İptal** düğmesi kullanılamıyor. Teslim notunu da düzeltemiyorsunuz. Denerseniz bu hata iletisini alıyorsunuz.

### <a name="issue-resolution"></a>Sorunun çözümü

Gelişmiş ambar yönetimi (WMS) için etkinleştirilen maddelere ait deftere nakledilen sevk irsaliyelerini düzeltmek için deftere nakletme işlemini doğrudan siparişten değil, yükten yapmanız gerekir.

## <a name="how-can-i-create-work-from-outbound-loads-instead-of-waves"></a>Dalgalar yerine giden yüklerden nasıl iş oluşturabilirim?

### <a name="issue-description"></a>Sorun açıklaması

Bu sorunu yeniden oluşturmanın bir yolu aşağıda verilmiştir.

1. Satış siparişi veya transfer emri kullanarak bir giden yük oluşturun.
2. Yükü ambara serbest bırakın.
3. Henüz malzeme çekme işi oluşturulmadığına dikkat edin.

### <a name="issue-resolution"></a>Sorunun çözümü

İşin yük serbest bırakıldığında hemen oluşturulması gerekiyorsa dalga şablonunu buna göre yapılandırmalısınız. Dalga şablonunda, aşağıdaki seçenekleri *Evet* olarak ayarlayın:

- Dalga oluşturmayı otomatik hale getir
- Dalgayı ambara serbest bırakma sırasında işle
- Dalga serbest bırakma işlemini otomatikleştir

## <a name="i-cant-re-release-a-partially-shipped-load"></a>Kısmen sevk edilen bir yükü yeniden serbest bırakamıyorum.

### <a name="issue-description"></a>Sorun açıklaması

Kısmen sevk edilen bir yükü ambara serbest bırakamazsınız. Ambarın serbest bırakılması işlemini gerçekleştirdiğinizde, bir "İşlem tamamlandı" iletisi görüntülenir, ancak hiçbir şey olmaz ve kalan miktar için hiçbir iş oluşturulmaz. Bu sorun, taşıma yükü işlevini kullandığınızda ve eksik bir ayırma varsa oluşur.

### <a name="issue-resolution"></a>Sorunun çözümü

[KB sorunu 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Kısmen sevk edilen yükler yeniden dalgaya eklenebilir ve yeniden işlenebilir"), [sürüm 10.0.15](../get-started/whats-new-scm-10-0-15.md)'te düzeltilmiştir.
