---
title: Üretim kurulumu gereksinimleri
description: Bu makalede, Üretim denetimiyle çalışabilmenize ilişkin kurulum gereksinimleri hakkında bilgi verilmektedir.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdParameters, RouteOpr, RouteOprTable, WorkCalendarTable, WorkTimeTable, WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 55561
ms.assetid: 1953059f-478d-4706-b461-25b89ace5fc3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 05a4c97697f13a41b65fba0df8c76bf884fc51a9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209384"
---
# <a name="production-setup-requirements"></a>Üretim kurulumu gereksinimleri

[!include [banner](../includes/banner.md)]

Bu makalede, Üretim denetimiyle çalışabilmenize ilişkin kurulum gereksinimleri hakkında bilgi verilmektedir. 

Üretim denetimi, diğer modüllerin özellikler ile tümleşiktir. Bu birbiriyle bağlantılı olma durumu, üretim emirlerini değiştirmenize ve bunların sistemdeki diğer tüm ilişkili işlemlerde ve hesaplamalarda otomatik olarak güncelleştirildiğinden emin olmanıza olanak tanır. Aşağıdaki kurulum yordamları, tamamlanmaları gereken sırada listelenmişlerdir.

## <a name="required-baseline-setup-in-other-modules"></a>Diğer modüllerdeki gerekli temel kurulum
Üretim kontrol ile çalışabilmeniz için diğer modüllerdeki bilgilerin ayarlanmış olması gerekir. Bu kurulum aşağıdaki görevleri içerir:

-   Genel şirket bilgilerini ayarlama.
-   Genel muhasebeyi ayarlama.
-   Madde grupları tanımlama..
-   Madde grupları için genel muhasebe hesapları ayarlama.
-   Stok yönetimindeki stok tablosunu ayarlama.
-   Stok Yönetimi'nde ürün reçeteleri (BOM) ve ürün reçetesi versiyonları oluşturun.

## <a name="required-calendar-and-resource-setup"></a>Gereken takvim ve kaynak kurulumu
Üretim Denetimi'ni kullanmadan önce Kuruluş Yönetimi'ni açın ve aşağıdaki sırayla takvim ve işlem kaynaklarını oluşturun ve tanımlayın:

1.  **Çalışma zamanı şablonları** – üretim planlaması için kullanılabilir zamanları tanımlamak için çalışma zamanı şablonları ayarlayın.
2.  **Takvimler** - Üretim çizelgeleme için yılın hangi günlerinin mevcut olduğunu tanımlamak üzere çalışma zamanı takvimleri ayarlayın.
3.  **Kaynak grupları** – planlamayı çalıştırdığınızda mevcut boş kapasite hakkında genel bir bakış elde edebilmek için işlem kaynaklarını gruplayacak kaynak gruplarını ayarlamak. İşlem kaynaklarını ayarlamadan önce kaynak gruplarını ayarlamak zorunda değilsiniz. Ancak, Üretim kontrolü ayarladığınızda, kaynakları nasıl gruplayacağınızı öğrenmenizi tavsiye ederiz..
4.  **Kaynaklar** – Kapasite planlamak ve üretim sürecini tamamlamak için kullanılacak kaynakları tanımlamak için işlem kaynaklarını ayarlayın.

## <a name="required-production-parameters-setup"></a>Gerekli üretim parametreleri kurulumu
**Üretim denetleme parametreleri** – Sistemin üretim emirlerini nasıl işleyeceğini ve ele alacağını tanımlamak için temel üretim parametrelerini ayarlayın. Üretim emirlerinin nasıl oluşturulduğunu, tahmin edildiğini, zamanlandığını ve tüketildiğini tanımlayın. Ne tür bir geri bildirim istediğinizi ve maliyet muhasebesinin nasıl yapılacağını da seçebilirsiniz.

## <a name="required-journal-name-identification"></a>Gerekli günlük adı tanımlaması
**Üretim günlüğü adları** – hareketleri deftere nakletmek ve kaydetmek için kullanılan üretim günlük adlarını belirtin.

## <a name="setup-if-you-use-operations"></a>Operasyonları kullanmanız durumunda geçerli kurulum
Operasyonlar tamamlanmış ürünü imal etmek üzere gerçekleştirilen belirli faaliyetleri göstermektedir. **Not:** Maddeyi üretmek için gerekli eylemlerin türlerini ve bu eylemlerin sıralamasını ve önceliklerini biliyor olmanız gereklidir Ayrıca hangi kaynakların, ne miktarda gerekli olduğunu bilmeniz gerekir.

1.  **Operasyonlar** – Tamamlanan maddeyi üretmek için tamamlanması gereken görevleri temsil eden operasyonları ayarlayın.
2.  **İlişkiler** – ayrıntılı özellikler oluşturmak için operasyon ilişkileri ayarlayın. Operasyon ilişkilerini tanımlamak için **İlişkiler** üzerinde **İşlemler** sayfasını tıklayın.

## <a name="setup-if-you-use-routes"></a>Rotaları kullanmanız durumunda geçerli kurulum
Rotalarla çalışıyorsanız, ayarladığınız tüm üretim rotaları için operasyonların ayarlanması gerekir. Rota, üretim sürecinin başlangıcından sonuna kadar maddenin operasyondan operasyona aldığı yolu gösterir.

1.  **Maliyet kategorileri** - belirtilen süreçlerin ve kurulum sürelerinin saat başına maliyetlerini tanımlamak üzere maliyet kategorileri ayarlayın.
2.  **Maliyet grupları** – farklı türde maliyetlendirmeleri oluşturmak ve sürdürmek için maliyet grupları ayarlayın.
3.  **Rota grupları** – rota gruplarıyla ilişkili parametreleri tanımlamak için rota grupları ayarlayın. Üretim rotaları oluşturabilmek için önce rota gruplarını ayarlamanız gerekmektedir.
4.  **Rotalar** - Üretim rotaları ayarlayın ve rota operasyonlarının planlamasını, maliyetlendirmesini, fiyatlandırmasını ve ilerleme raporlamasını kontrol etmek üzere varsayılan ayarlar tanımlayın.
5.  **Rota sürümü** - Üretimdeki madde varyasyonlarına olanak vermek üzere rota versiyonları ayarlayın.

## <a name="optional-advanced-settings"></a>İsteğe bağlı, gelişmiş ayarlar
1.  **Üretim grupları** – üretim emri ve genel muhasebe hesapları arasında ilişki kurmak için üretim grupları ayarlayın. Genel muhasebe hesapları, siparişleri raporlama için gruplandırmak veya nakletmek için kullanılır.
2.  **Üretim havuzları** – acil üretim emirlerini işlemek veya sipariş gruplarını silmek ve deftere nakletmek için üretim havuzları oluşturun.
3.  **Özellikler** – üretimlerin sırasını denetlemek için kaynaklarınıza atadığınız özel öznitelikleri oluşturmak için özellikleri tanımlayın. Bu öznitelikler çalışma süresi şablonuna bağlıdır.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]