---
title: Ambar uygulaması olayları
description: Bu makale, toplu işin bir parçası olarak ambar uygulaması olay iletilerini işlemek için kullanılan ambar uygulaması olayını işlemeyi açıklamaktadır.
author: perlynne
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2dc24fed1ec71432d9e2a3e1cb5b366267c2938b
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218757"
---
# <a name="warehouse-app-event-processing"></a>Ambar uygulaması olayı işleme

[!include [banner](../includes/banner.md)]

Supply Chain Management'ta çalışan toplu işler, sinyal verilen olaylara gerektiğinde tepki vermek üzere Ambar Yönetimi mobil uygulaması tarafından yayınlanan olayları işlemek için bir kuyruktaki verileri kullanabilir. Bu özellik, uygulamayı kullanan çalışanların yaptığı belirli eylem türlerine yanıt olarak kuyruğa ilgili olayları ekler. Örneğin, *Ambar uygulamasından transfer emirleri oluşturma ve işleme* özelliği kullanıldığında sistem **Ambar uygulaması olaylarını işle** toplu işini çalıştırırken transfer emri başlıkları ve satırları arkauçta oluşturulur ve güncelleştirilir.

## <a name="turn-the-process-warehouse-app-events-feature-on-or-off"></a>Ambar uygulaması olaylarını işle özelliğini açma veya kapatma

Supply Chain Management sürüm 10.0.25 itibariyle, bu özellik varsayılan olarak açıktır. Supply Chain Management sürüm 10.0.29 itibarıyla, bu özellik zorunludur. Bu nedenle, varsayılan olarak açıktır ve yeniden kapatılamaz. 10.0.29 sürümünden daha eski bir sürümü çalıştırıyorsanız, yöneticiler [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanında *Ambar uygulaması olaylarını işle* özelliğini aratarak bu işlevi açabilir veya kapatabilir.

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Ambar uygulaması olaylarını işlemek için bir toplu iş ayarlayın

### <a name="process-warehouse-app-events"></a>Ambar uygulaması olaylarını işle

Transfer emri oluşturma ve satır güncelleştirmeleri için ambar uygulaması olaylarını işlemek üzere bir planlı toplu iş ayarlayın.

1. **Ambar yönetimi \> Periyodik görevler \> Ambar uygulaması olaylarını işle**'ye gidin.
1. Ambar uygulaması olaylarını işle iletişim kutusu açılır. **Arka planda çalıştır** hızlı sekmesini genişletin ve **Toplu işleme** öğesini **Evet** olarak ayarlayın.
1. **Arka planda çalıştır** sekmesinde **Tekrar**'ı seçin.
1. **Yinelemeyi tanımlayın** iletişim kutusu açılır. İşletmeniz için gereken çalışma zamanlamasını ayarlayın.
1. **Ambar uygulaması olaylarını işle** iletişim kutusuna dönmek için **Tamam**'ı seçin.
1. Toplu işi toplu iş kuyruğuna eklemek için **Ambar uygulaması olaylarını işle** iletişim kutusunda **Tamam**'ı seçin.

## <a name="query-warehouse-app-events"></a>Ambar uygulaması olaylarını sorgulama

Ambar Yönetimi mobil uygulaması tarafından oluşturulan olay kuyruğunu ve olay iletilerini **Ambar yönetimi \> Sorgular ve raporlar \> Mobil cihaz günlükleri \> Ambar uygulaması olayları**'na giderek görüntüleyebilirsiniz.

## <a name="the-standard-event-queue-process"></a>Standart olay kuyruğu işlemi

Ambar uygulaması olayları kuyruğu genellikle aşağıdaki açıklanan akışla kullanılır:

1. Bir olay, bir olay iletisi ile kuyruğa eklenir. Yeni iletin başlangıçta **Beklemede** Olay durumuna sahiptir; bu, **Ambar uygulaması olaylarını işle** toplu işinin bu iletiyi çekmeyeceği ve işlemeyeceği anlamına gelir.
1. İleti durumu **Kuyruğa alındı** olarak güncelleştirildiğinde, **Ambar uygulaması olaylarını işle** toplu işi olayı alır ve işler.
1. Toplu iş istenen işlemin gerçekleştirilmiş olup olmamasına bağlı olarak, olay durumlarını **Tamamlandı** veya **Başarısız oldu** olarak güncelleştirir.
1. İlgili tüm olay iletileri **Tamamlandığına** olay kuyruktan silinir.

 Ayrıntılı bir örnek için bkz. [Ambar uygulamasından transfer emri oluşturma işlemi](create-transfer-order-from-warehouse-app.md).

## <a name="handle-event-errors"></a>Olay hatalarını işleme

Ambar olayı işlemenin bir parçası olarak, istenen ileti etkinliği işlemleri toplu işten alamayabilir. Bu durumda, olay iletisi **Başarısız oldu** şekilde değişecektir. Nedenini öğrnemke ve sorunları düzeltmek için gerekli adımları atmak için **Toplu iş günlüğü** bilgilerini kullanabilirsiniz.

Ayrıntılı bir örnek için bkz. [Ambar uygulamasından transfer emri oluşturma](create-transfer-order-from-warehouse-app.md).

Başarısız olan bir ambar uygulaması olay iletisini sıfırlamak için:

1. **Ambar yönetimi \> Sorgulamalar ve raporlar \> Mobil cihaz günlükleri \> Ambar uygulaması olayları**'na gidin.
1. **Ambar uygulaması olay iletileri** hızlı sekmesinde, **Olay durumu** sütununda **Başarısız oldu** olarak gösterilen ilgili olayı seçin.
1. **Ambar uygulaması olay iletileri** araç çubuğundan **Sıfırla** seçeneğini belirleyin.
1. İlgili tüm iletiler sıfırlanana kadar çalışmaya devam edin.

Ayrıca, **Ambar uygulaması olay iletileri** araç çubuğundaki **Sil** seçeneğini kullanarak **Başarısız oldu** olay iletisini kaldırabilirsiniz.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
