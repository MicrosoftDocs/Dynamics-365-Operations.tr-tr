---
title: Master planlama sorunlarını giderme
description: Bu konu, master planlama üzerinde çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklamaktadır.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 8e78634c0efb1c401297559ce40b2ca30519f3bf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809482"
---
# <a name="troubleshoot-master-planning"></a>Master planlama sorunlarını giderme

Bu konu, master planlama üzerinde çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklamaktadır.

## <a name="bill-of-materials-explosion-behaves-differently-for-firmed-production-orders-and-for-estimated-production-orders-for-manually-created-work"></a>Ürün reçetesi açılımı, kesinleştirilen üretim emirleri için ve el ile oluşturulmuş iş için tahmini üretim emirlerinde farklı şekilde davranır.

### <a name="issue-description"></a>Sorun açıklaması

Bir üretim emri kesinleştirildiğinde, ürün reçetesini açtığınızda maddeler açılmaz. Ancak, bir iş emrini el ile oluşturduğunuzda ve üretim emrini tahmin ettiğinizde, maddeler açılır.

### <a name="issue-resolution"></a>Sorunun çözümü

Sistem beklendiği gibi çalışmaktadır. Üretim emri kesinleştirildiğinde gerçekleşen açılım, planlı siparişi işaret eder ancak bu durumda planlı sipariş kesinleştirilmiş olduğu görünmüyor. Ancak üretim emri tahmin edildiyse açılım, planlanmış sipariş bulunmayan serbest bırakılmış üretim emrinden tetiklenir.

## <a name="the-delay-value-isnt-updated-when-i-reschedule-a-planned-order"></a>Planlanan bir siparişi yeniden zamanladıktan sonra, Gecikme değeri güncelleştirilmez.

Planlı sipariş gecikmesini güncelleştirmek için planlı sipariş için **Yeniden Programlama** iletişim kutusunu açın. **Açılım** hızlı sekmesinde, **Yeniden programlamadan sonra açılım gerçekleştir** seçeneğinin *Evet* olarak ayarlandığından emin olun.

## <a name="production-scheduling-doesnt-consider-the-safety-margins-that-are-set-on-the-item-coverage-for-pegged-supply"></a>Üretim programlaması, ilişkilendirilmiş arz için madde karşılamasının ayarlandığı emniyet marjlarını dikkate almaz.

### <a name="issue-description"></a>Sorun açıklaması

Master planlama emniyet marjlarını dikkate alır. Ancak planlanan üretim emirleri planlandığında emniyet marjları yoksayılır.

### <a name="issue-resolution"></a>Sorunun çözümü

Marjlar yalnızca master planlama sırasında değerlendirilir, el ile zamanlama sırasında değil. Marjlar planlama aşamasında, gerçek işleme "marj" vermek için bir tampon olarak çalışacak şekilde tasarlanmıştır.

İstenen sonuca ulaşmak için marjı kaldırabilirsiniz. Rotanın istenen saati (örneğin, kuyruk süresi olarak) içermesi için güncelleştirilmesi gerekir. Hem master planlama hem de el ile programlamanın aynı sonucu üretmesi gerekir.

## <a name="planned-orders-are-generated-even-though-we-have-items-in-stock-and-production-orders-already-exist-for-them"></a>Stokta maddeler ve maddeler için üretim emirleri olsa bile planlı siparişler oluşturulur.

**Kapsam grubu** sayfasında, ilgili grupların **Pozitif günler** değerlerini artırarak bu sorunu giderebilirsiniz. Bu değişiklik, sistemin talep için eldeki stoğun kullanılabileceği konusunda karar vermesine neden olur. Daha sonra, stokta bulunan maddeler için yeni bir planlı sipariş oluşturulmaz.

## <a name="master-planning-doesnt-seem-to-respect-capacity-limitations-and-is-scheduling-more-than-the-available-capacity"></a>Master planlama, kapasite sınırlamalarını dikkate almıyor ve kullanılabilir kapasitenin fazlasını planlıyor.

### <a name="issue-description"></a>Sorun açıklaması

Sınırlı kapasite bulunan ve rotanın hem bir kaynak grubu hem de bağımsız kaynaklar için çeşitli gereksinimler belirttiği durumlarda işlem programlamayı kullandığınızda, algoritmanın kapasite çakışmalarını doğrulama biçimi nedeniyle küçük bir aşırı planlama olasılığı vardır. Bu fazla planlama, master planlamayı çalıştırmak için yardımcıları kullandığınızda ortaya çıkabilir. Görece daha kısa bir çalışma zamanı olan birçok iş olduğunda ortaya çıkması olasıdır.

### <a name="issue-resolution"></a>Sorunun çözümü

İşlem programlama için hiçbir fazla planlama oluşmuyorsa **Master planlama parametreleri** sayfasında **İşlem Programlaması için Sınırlı Doğru Kapasite**'yi açarak master planlamanın programlama bölümünü tekli iş parçacıklı hale getirebilirsiniz. Bu seçenek varsayılan olarak kullanılamaz. Kişiselleştirme özelliklerini kullanarak bunu sayfaya el ile eklemeniz gerekir. Bu seçeneği kullandığınızda, paralel işlem olmaması nedeniyle planlama daha yavaş çalışır.

## <a name="planned-orders-take-a-long-time-to-update"></a>Planlı siparişlerin güncelleştirilmesi uzun zaman alabilir.

### <a name="issue-description"></a>Sorun açıklaması

Planlı bir siparişte gereksinim miktarı ve/veya teslimat tarihi güncelleştirilirken, güncelleştirmeyi kaydetmek için genellikle sipariş başına en az 30 saniye süre gerekir.

### <a name="issue-resolution"></a>Sorunun çözümü

Bu, yerleşik master planlama altyapısında oluşan bilinen bir sorundur. Düzenleme sırasında, ürün reçetesi yapısı üzerinden, temel alınan otomatik açılımdan kaynaklanır. Bu sorun, Planlama İyileştirmesi'nde giderilmiştir ve burada bir planlayıcı ilgili siparişleri güncelleştirebilir ve onaylayabilir ve istendiğinde, temel alınan ürün reçetesi yapısı için planlı siparişleri güncelleştirmek amacıyla bir planlama çalıştırmasını tetikleyebilir.

Yerleşik master planlama altyapısıyla performansı artırmanın bir yolu aşağıdakileri yapmaktır:

1. **Master planlama \> Kurulum \> Planlar \> Master planlar** bölümüne gidin.
1. Plan seçin.
1. **Gün cinsinden zaman dilimi** hızlı sekmesini genişletin.
1. **Açılım**'ı *Evet* olarak ayarlayın ve bu ayarın altındaki alanı 0 (sıfır) olarak ayarlayın.

> [!NOTE]
> Bu, bu master plan için gerçekleştirilen açılımları tek bir güne sınırlandırır.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]