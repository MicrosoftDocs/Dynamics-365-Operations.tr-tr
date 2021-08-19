---
title: Üretim emirlerini serbest bırakma
description: Serbest bırakılmış bir üretim emri, üretim için yetkilendirilmiş bir emirdir. Serbest bırakılmış terimi, üretim emri yaşam döngüsünde, üretim emrinin üretim atölye katında uygulamaya geçirilmeye ve ambar işlemlerine hazır olduğu bir durumu ifade eder.
author: johanhoffmann
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 740ac516ffa01d8930aedabb9873834b07b7debf700dc61b14d93ac8d6dcd086
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718882"
---
# <a name="release-production-orders"></a>Üretim emirlerini serbest bırakma

[!include [banner](../includes/banner.md)]

Serbest bırakılmış bir üretim emri, üretim için yetkilendirilmiş bir emirdir. Serbest bırakılmış terimi, üretim emri yaşam döngüsünde, üretim emrinin üretim atölye katında uygulamaya geçirilmeye ve ambar işlemlerine hazır olduğu bir durumu ifade eder.

## <a name="characteristics-of-the-released-state"></a>Serbest durumu özellikleri

**Serbest** durumu, üretim emri yaşam döngüsündeki bir durumdur. **Serbest** durumundaki üretim siparişleri, üretim atölyesinde işleme konma ve ambar işlemleri için kullanılabilir. **Serbest** durumu aşağıdaki özelliklere sahiptir:

- Bir üretim emrinin durumu üretim emrinden veya bir toplu iş işlemi kullanılarak **Serbest** olarak değiştirilebilir. Üretim emri, **Master plan** sayfasındaki **Kesinleştirme zaman dilimi** alanı kullanılarak kesinleştirilmiş planlı üretim emirlerinden otomatik olarak güncellenebilir.
- **Serbest** durumu, atölye operatörleri (operatörler) için üretim işlerinin atölyede işleme konması için bir sinyaldir.
- Rota kartları, rota işleri ve iş kartları gibi üretim evrakı, üretim işleri hakkında bilgi sağlar ve yayınlanabilir.
- Fiziksel olarak rezerve edilmiş malzemelerde, üretim emri için malzeme çekmek üzere ambar çalışması üretilir.

## <a name="releasing-jobs-to-the-shop-floor"></a>İşleri atölyeye serbest bırakma

Bir üretim emri serbest bırakıldıktan sonra, siparişle ilgili üretim işleri görünür ve kayda hazır durumdadır. İşleçler **İş kartı terminali** veya **İş kartı cihazı** sayfasında Başlatma, Durdurma ve Tamamlama gibi iş kayıtları yapabilirler. Kaydedilen süre ve miktar, harcanan süre ve miktarın izlenmesi için otomatik olarak kayıt sayfalarından üretim günlüklerine transfer edilir.

## <a name="route-cards"></a>Rota kartları

Rota kartı, rota ve operasyon ayarları ve operasyon ve iş çizelgeleme yöntemlerinden gelen bilgiler için bir genel bakış sağlar.

## <a name="route-jobs"></a>Rotadaki işler

Bir rota işi, bir operasyonun her işini ayrıntılı olarak listeler ve kurulum, işlem, kuyruk ve taşıma sürelerini içerir. Örneğin, boyama gibi bir operasyon kurulum, çalışma süresi (boyama işlemi için) ve kuyruk süresi (kurutma için) gerektirebilir.

## <a name="job-cards"></a>İş kartları

Bir iş kartı, belirli bir operasyonun tek tek iş numaralarını listeler. Her sayfada bir iş görünür. Bir iş kartına dahil olan işler ve tahmini süreleri rotadan ve operasyon kurulum bilgilerinden gelir. Bir iş kartından, **Üretim günlüğü satırları**, **iş kartı** sayfasını açabilirsiniz. Operasyon kaynaklarını çalıştıran kişiler üretim sürecinde geri bildirim sağlayabilir. Bunlar, tüketim istatistikleri ve hata miktarı gibi bilgileri girebileceğiniz alanlardır.

## <a name="warehouse-work-for-raw-material-picking"></a>Hammadde çekmek için ambar çalışması

Hammadde çekme işi, serbest bırakma sırasında üretilir. İş yalnızca sipariş serbest bırakılmadan önce üretim emri için fiziksel olarak rezerve edilmiş olan miktarda malzeme için üretilir. Aşağıdaki kurulum hammadde çekme için ambar oluşturma işi için gereklidir:

- Hammadde çekmeye yönelik ve malzemelerin çekileceği ambar konumunu belirleyen bir konum yönergesi
- Hammaddeler için, ambar çalışmasının yürütülmesine yönelik politikaların yapılandırıldığı bir dalga şablonu
- Malzemelerin koyulacağı yeri belirleyen bir üretim girdisi konumu

Plaka kontrollü konumları kullanırken, ham madde malzeme çekme işini işlerken sipariş edilen miktarın mı yoksa madde için kullanılabilir tam miktarın mı seçileceğini belirleyebilirsiniz. Bu seçeneği ayarlamak için:

1. **Ürün bilgileri yönetimi \> Ürünler \> Serbest bırakılan ürünler**'e gidin ve ilgili maddeyi açın.
1. **Ambar** hızlı sekmesini genişletin.
1. **Plaka konumlarında malzeme çekme** alanı için aşağıdaki seçeneklerden birini belirleyin:
    - *Sipariş çekme*: Yalnızca sipariş edilen miktar seçilmelidir.
    - *Hazırlama*: Mümkün olduğunda, plakada bulunan tam miktar seçilmelidir. Bir çalışanın tam plaka miktarını seçebilmesi için plakanın karışık maddeler içermemesi ve karışık boyutlara sahip olmaması gerekir. Plaka karışık boyutlar veya maddeler içeriyorsa çekme işlemi *Sipariş çekme* olarak ayarlanmış gibi devam eder.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]