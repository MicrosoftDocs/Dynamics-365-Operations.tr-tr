---
title: Satış siparişi için aynı toplu işi rezerve etme
description: Bu makalede, bir ürünün, tek bir stok toplu işine karşılık stok rezervasyonuna izin verecek şekilde nasıl ayarlandığı açıklanmaktadır.
author: omulvad
manager: AnnBe
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d90105b4713041b0c1efdc8a2e0cdf50e7dedc7
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154632"
---
# <a name="reserve-the-same-batch-for-a-sales-order"></a>Satış siparişi için aynı toplu işi rezerve etme

[!include [banner](../includes/banner.md)]

Bu makalede, bir ürünün, tek bir stok toplu işine karşılık stok rezervasyonuna izin verecek şekilde nasıl ayarlandığı açıklanmaktadır.

Aynı toplu iş rezervasyonu, tek bir stok toplu işine karşılık bir satış siparişi satırı için stok rezerve etmenizi sağlar. Örneğin, duvar kağıdı sipariş eden bir müşteri, kağıt ruloları arasında tutarsızlıklar olmaması için tüm siparişin aynı toplu iş veya lottan karşılanmasını talep edebilir. Bir ürünü aynı toplu rezervasyonu kullanacak şekilde ayarlamak için, ürüne atadığınız madde model grubunda, etkin izleme boyut grubunda ve depolama boyut grubunda aşağıdaki ayarların etkin olması gerekir:

- **Madde model grupları** – Madde model grubu için, stok ilkelerine ilişkin **Rezervasyon** alan grubunda **Aynı toplu iş seçimi** ve **Gereksinimi konsolide et** alanları seçilmelidir.
- **İzleme boyutu grupları** – İzleme boyutu grubu için, toplu iş numarasına ilişkin **Boyuta göre tedarik planı** alanı seçilmelidir.
- **Depolama boyutu grupları** – Depolama boyutu grubu için, **Tesis** ve **Ambar** için **Boyuta göre tedarik planı** alanı seçilmelidir.

Aynı toplu iş seçimi için bir satış siparişi satırında bir ürüne ilişkin stok rezerve ettiğiniz zaman, sistem, sipariş edilen miktarı tek bir stok toplu işinden rezerve etmeyi dener. Tüm özel toplu iş özniteliği gereksinimleri de dikkate alınır. Miktar tek bir toplu işleminden doldurulamıyorsa, **Aynı toplu iş rezervasyon çakışması** sayfası görünür. Bu sayfada sorunlar ve rezervasyon işlemine devam etmek için alabileceğiniz önlemler açıklanır. Aşağıdaki koşullar, toplu işin rezerve edilmesini engelleyebilir:

- Toplu iş değerlendirme kodunda, satış için **Engellendi** olarak işaretlenmiş **Rezervasyonu engelle** uyarısı vardır.
- Bitiş tarihine ve varsa müşterinin ilgili satış yapılabilir gün sayısına göre, toplu işin tarihi geçmiştir. Madde için madde model grubu FEFO (İlk Sona Eren İlk Çıkar) tarih denetimliyse ve malzeme çekme ölçütü olarak bitiş tarihi seçilmişse madde yine rezervasyon için değerlendirilebilir.
- Bitiş tarihi/son kullanma tarihi ve varsa müşterinin satış yapılabilir gün sayısına göre toplu işin raf ömrü kalan gün sayısı yeterli değildir.

**Etkin ambar yönetimi işlemleri** kullanan bir depolama boyutu grubuyla ilişkilendirilmiş maddeler için, yerleşim boyutunun üstünde tanımlanan toplu iş numarası stok boyutuna sahip bir rezervasyon hiyerarşisi kullanarak belirli toplu iş numaralarını rezerve edebilirsiniz. Satış ve transfer emri satırları için **toplu rezervasyon** sayfası, kullanılabilir toplu iş numaralarına dayalı olarak çoklu satırları seçmenizi ve rezerve etmenize olanak tanır. Yerin altında toplu iş numarası boyutu olan bir rezervasyon hiyerarşisi kullanıyorsanız ne yapmanız gerektiğini öğrenmek için [esnek Ambar düzeyi boyut rezervasyon ilkesi](../warehousing/flexible-warehouse-level-dimension-reservation.md) 'ne bakın.
