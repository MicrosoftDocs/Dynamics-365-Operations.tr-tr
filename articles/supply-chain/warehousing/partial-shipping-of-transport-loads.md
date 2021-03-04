---
title: Taşıma yükü kısmi sevkiyatı
description: Bu konu yükü nasıl kısmen sevk edebileceğinizi ve yük için kapasite planlamasını nasıl erteleyebileceğinizi açıklar.
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTransportLoad
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: e92a15cf4e2694eba1804184a02a7fd13159799e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439180"
---
# <a name="partial-shipment-of-a-transport-load"></a>Taşıma yükü kısmi sevkiyatı

[!include[banner](../includes/banner.md)]

Yüklerin kısmi sevkiyatını ayarlayarak bir yüke tüm satış satırları eklenene kadar kapasitenin belirlenemediği yükleri işleyebilirsiniz. İşlem kesin palet sayısı bilindiğinde sonlandırılabilir. Bu nedenle, bir taşıma fiziksel olarak hazırlanmış stoktan yüklendiği zamana kadar hangi paletlerin hangi taşımaya atanacağına karar vermeniz gerekmez.

Bu özellik, malzeme çekme veya yükleme işi oluşturulmadan önce hangi paletlerin hangi taşımaya atanacağını belirlemenizi gerektiren daha katı yapı bir yapının oluşturduğu zorlamaya bir alternatif sunar. Bunun yerine, kullanıcılar kısmı bir sevkiyat onayı için tek tek yükleri yapılandırabilir. Bu yükler için taşıma yüklemesi işlemleri daha sonra gerçekleşir. Bu nedenle, taşıma planlama departmanı yükleri tek tek taşıyıcıların kapasitesini dikkate almak zorunda kalmadan planlayabilir.

Yükleme zamanında, çalışanlar paletin yüklenebileceği yeni bir taşıma yükü tanımlayabilir. Alternatif olarak, varolan bir taşıma yükü tanımlayabilirler. Bu veriler bir mobil cihazla kaydedilebilir. Bu nedenle, birden fazla ambar çalışanı yanı kamyona aynı yüklerden veya farklı yüklerden stok yükleyebilir. Yükler daha sonra tamamen veya kısmen sevk edilebilir.

> [!NOTE] 
> Stoğu bir yükten belirli bir taşıma yüküne yüklemek ve yükü kısmen sevk etmek için işin iş şablonunda yükleme sınıfı kullanılarak oluşturulması gerekir. **Malzeme çekme** türündeki normal malzeme çekme işi kamyon gibi bir taşıma yüküne yüklenemez.

## <a name="set-up-transport-loads-for-partial-shipment"></a>Kısmi sevkiyat için taşıma yüklerini ayarlama

Yüklerin kısmı sevkiyatının kurulumu aşağıdaki iki yordamdan oluşur.

### <a name="set-the-loading-strategy"></a>Yükleme stratejisini ayarlama

Yükleme stratejisini ayarlayarak kısmi yüklemeyi etkinleştirmeniz gerekir. Bir yük oluşturduktan sonra yükleme stratejisini ayarlayabilirsiniz.

1. **Ambar yönetimi** \> **Yükler** \> **Tüm yükler**'i seçin.
2. Bir yük seçin, sonra **Başlık** öğesini tıklatın.
3. **Yükleme stratejisi** alanında **Kısmi yük sevkiyatına izin verildi**'yi seçin.

### <a name="create-a-menu-item-for-loading-of-transport-loads"></a>Taşıma yüklerinin yüklenmesi için bir menü öğesi oluşturma

Yüklenecek taşıma yüklerini etkinleştiren yeni bir menü öğesi oluşturmanız gerekir. Bir taşıma yükü iş satırlarını bir yükten veya birden fazla yükten gruplandırmanıza olanak tanır. Taşıma yüküne eklenen her şey bir mobil tarayıcı kullanılarak sevk edilebilir.

1. **Ambar yönetimi** \> **Kurulum** \> **Mobil cihaz** \> **Mobil cihaz menüsü öğeleri**'ni seçin.
2. **Yeni**'yi seçin ve sonra **Mod** alanında, **İş**'i seçin.
3. **Mevcut işi kullan** seçeneğinde **Evet**'i işaretleyin.
4. **Genel** sekmesinde, **Yöneten** alanında **Taşıma yüklemesi**'ni seçin.
5. Bir mobil tarayıcıdan sevkiyat onayını etkinleştirmek için **İzin verilen sevk onay türü** alanında **Taşıma yükü**'nü seçin.

## <a name="confirm-shipment-of-a-transport-load-from-the-client"></a>Bir taşıma yükünün sevkiyatını istemciden onaylama

Bu ayar sevk edilecek bir tam yük veya kısmen yüklenmiş yük içeren bir taşıma yükünü onaylamanıza olanak tanır.

1. **Ambar yönetimi** \> **Yükler** \> **Taşıma yükleri**'ni seçin.
2. Eylem Bölmesinde **Sevk ve teslim alma** sekmesindeki **Onayla** grubunda **Taşıma**'yı seçin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]