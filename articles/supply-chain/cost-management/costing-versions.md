---
title: Maliyetlendirme sürümlerine genel bakış
description: Bu makalede, maliyetlendirme sürümleri, bu sürümlerin nasıl sürdürüleceği ve bu sürümlere ekleyebileceğiniz veri türleri hakkında bilgiler verilmektedir. Maliyetlendirme versiyonunun birincil amacı madde, maliyet kategorileri için dolaylı maliyet hesaplama formülleri hakkındaki maliyet kayıtlarını içermektir.
author: AndersGirke
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: 54532
ms.assetid: cd239da5-f434-4d1b-8196-5414c888d76d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 287aabaa6a0b3de709dae8b16dbccc21dc349cf5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987641"
---
# <a name="costing-versions-overview"></a>Maliyetlendirme sürümlerine genel bakış

[!include [banner](../includes/banner.md)]

Bu makalede, maliyetlendirme sürümleri, bu sürümlerin nasıl sürdürüleceği ve bu sürümlere ekleyebileceğiniz veri türleri hakkında bilgiler verilmektedir. Maliyetlendirme versiyonunun birincil amacı madde, maliyet kategorileri için dolaylı maliyet hesaplama formülleri hakkındaki maliyet kayıtlarını içermektir.

Bir maliyetlendirme versiyonu, içerisinde bulunan verilere bağlı olarak bir veya daha fazla amaca hizmet edebilir. Maliyetlendirme versiyonunun birincil amacı madde, maliyet kategorileri için dolaylı maliyet hesaplama formülleri hakkındaki maliyet kayıtlarını içermektir. Maliyetlendirme versiyonu, maliyetlendirme versiyonuna atanan maliyetlendirme tipine dayanan bir standart maliyet kayıtları veya planlanan maliyet kayıtları kümesi içerebilir.

## <a name="costing-versions-for-standard-or-planned-costs"></a>Standart veya planlı maliyetler için maliyet sürümleri oluşturun.
### <a name="standard-costs"></a>Standart maliyetler

Maliyetlendirme versiyonu maddelere ilişkin olarak, maliyetlendirme versiyonunun maddeler ve üretim süreçleri hakkında bir standart maliyet kayıtları kümesi içerdiği standart bir maliyet stok modelini destekleyebilir. Üretim süreçleri hakkındaki veri maliyetleri, rota operasyonlarının maliyet kategorileri ile üretim genel giderlerinin hesaplanma formülleri cinsinden ifade edilebilir.

### <a name="planned-costs"></a>Planlanan maliyetler

Maliyetlendirme versiyonu, maddeler ve üretim süreçleri hakkında bir planlanan maliyet kayıtları kümesi içerebilir. Planlanan maliyetler içeren bir maliyetlendirme versiyonu genelde, satın alınan malzeme veya üretim süreçlerine yönelik yapılan maliyet değişikliklerinin üretilmiş maddelerin hesaplanan maliyetlerine olan etkisi için uygulanan benzetimler gibi maliyet hesaplama benzetimlerini desteklemek için kullanılır. Planlanan maliyetlerin madde maliyeti kayıtları, madde maliyetlerinin ilk değerlerini sağlayarak gerçek bir maliyet stok modelini desteklemekte de kullanılabilir. Bu değerler üretilen maddeler için planlanan maliyetlerinin hesaplanması içerir.

## <a name="entering-costs"></a>Maliyetleri girme
Bir maliyetlendirme versiyonundaki maliyet kayıtlarının verilerinin sürdürülmesi için, satınalınan maddeler ve tesisler arasında transfer edilen maddelerin maliyetleri girilir. Üreticiler için ek veri sürdürme, rota operasyonlarıyla ilişkili maliyet kategorilerinin girilmesi, üretim genel giderini yansıtan dolaylı maliyetler için hesaplama formüllerinin girilmesi ve üretilmiş maddelerin maliyetlerinin hesaplanmasını da içerir. 

Bir maliyetlendirme versiyonundaki madde maliyeti verileri, her madde için bir veya daha fazla kayıttan oluşur. Bir madde maliyeti kaydı ilk olarak girildiğinde **Bekleyen** durumundadır ve amaçlanan yürürlük tarihi vardır. Madde maliyeti kaydını etkinleştirdiğinizde, durumu **Etkin** olarak güncellenir ve yürürlük tarihini etkinleştirme tarihine güncelleştirilir. Farklı madde maliyet kayıtları, farklı tesisleri, yürürlük tarihlerini veya durumları yansıtabilir. Üretilmiş maddeler için maliyetleri gelecekteki bir tarih için hesaplarken, ürün reçetesi hesaplaması durumu, hesaplamaları **Bekleyen** veya **Etkin** olduğundan bağımsız olarak kullanır. Bir maddenin geçerli etkin maliyet kaydı, üretim emri maliyetlerini tahmin etmek ve stok hareketlerini bir standart maliyetlendirme stok modeli çerçevesinde değerlendirmek için kullanılır. Maliyet kategorileri ve dolaylı maliyet hesaplama formüllerinin sürdürülmesi madde maliyeti kayıtlarının sürdürülmesine benzer. 

Bir maliyetlendirme versiyonu için geçerli olan iki engelleme ilkesi, bekleyen maliyetlerin sürdürülebilirliğini ve bekleyen maliyetin etkinleştirilebilirliğini belirler. Engelleme ilkelerini, veri sürdürmeye izin vermek ve bir maliyetlendirme versiyonundaki maliyet kayıtları için veri sürdürmeyi engellemek için kullanın. 

Maliyetlendirme versiyonu, ürün reçetesi hesaplaması amaçlı olarak madde satış fiyatları veya satınalma fiyatları hakkındaki verileri içerebilir.

## <a name="item-sales-prices-for-bom-calculations"></a>Ürün reçetesi hesaplamaları için madde satış fiyatları
Satış fiyatları hakkındaki verileri dahil etmenin ana sebebi üretilen maddenin hesaplanan satış fiyatını korumak içindir. Daha sonra hesaplanan satış fiyatı bileşenlerin, üretim akışı operasyonlarının ve ek yükün maliyete ve satış fiyatına nasıl katkıda belirlemek için analiz edilebilir. 

Satış fiyatları hakkında veri dahil etmenin ikincil bir sebebi bileşen maddeleri için satış fiyatı kayıtlarını tanımlamaktır. Bu kayıtlar daha sonra üretilen maddelerin satış fiyatını hesaplamak için kullanılabilir. Önce bir ürün reçetesi hesaplama grubuna gömülü olan satış fiyatı modelini tanımlamak ve ürünleri satın almak için ürün reçetesi hesaplama grubu atayın. Ardından planlanan maliyetleri kullanan ürün reçetesi hesaplamaları gerçekleştirdiğinizde, ürün reçetesi hesaplama grubunun maliyet fiyatı modelini seçin. 

Aksi takdirde, maddeler için satış fiyatı kayıtları, el ile girilmiş de olsa hesaplanmış da olsa, referans bilgisi olarak kullanılırlar. Bir maddenin satış fiyatı kaydını etkinleştirilerek, maddenin temel satış fiyatını güncelleştirebilirsiniz. Ancak, temel satış fiyatı tesise özgü değildir ve el ile geçersiz kılınabilir. Maddenin temel satış fiyatı, satış siparişlerinde ve satış tekliflerinde varsayılan satış fiyatı olarak kullanılır.

## <a name="item-purchase-prices-for-bom-calculations"></a>Ürün reçetesi hesaplamaları için madde satınalma fiyatları
Satınalma fiyatı verilerinin bulunmasına olanak sağlamanın birincil amacı, bileşen maddeleri için, üretilen maddelerin maliyetlerini hesaplamak amacıyla daha sonra kullanılabilecek satınalma fiyatı kayıtları tanımlamaktır. Madde satınalma fiyatı kayıtlarının el ile girilmesi gerekir. 

Satınalma fiyat içeriğini etkinleştirmek için, öncelikle maddenin satınalma fiyatını için bir maliyet fiyatı modeli içeren bir ürün reçetesi hesaplama grubunu tanımlamalı ve ürün reçetesi hesaplama grubunu satın alınmış maddelere atayın. Sonra ürün reçetesi hesaplama grubu için bir maliyet fiyatı modeli kullanarak üretilen maddelerin satış fiyatlarını hesaplamak için planlanan maliyetleri ürün reçetesi hesaplamalarını kullanın. 

Maddeler için satınalma fiyatı kayıtları da başvuru bilgisi olarak kullanılır. Satınalma fiyatı kaydından bir öğenin durumunu **Bekleyen**'den **Etkin**'e değiştirerek, maddenin temel satınalma fiyatı güncelleştirebilirsiniz. Ancak, temel satınalma fiyatı tesise özgü değildir ve el ile geçersiz kılınabilir. Maddenin temel satınalma fiyatı satınalma siparişlerinde varsayılan satınalma fiyatı olarak kullanılır.



