---
title: Toplu iş oluşturma
description: Toplu iş, otomatik işlem için bir Uygulama Nesne Sunucusu (AOS) kurulumuna gönderilmiş görevlerin bir grubudur.
author: matapg007
ms.date: 11/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: matgupta
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
ms.openlocfilehash: 06fb9a18e70c316be97645ba76f9462cd3ccc729
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292465"
---
# <a name="create-a-batch-job"></a>Toplu iş oluşturma

[!include [banner](../../includes/banner.md)]

Toplu iş, otomatik işlem için bir Uygulama Nesne Sunucusu (AOS) kurulumuna gönderilmiş görevlerin bir grubudur. Toplu işler işi oluşturan kullanıcının güvenlik kimlik bilgilerini kullanarak çalışır. Toplu bir iş oluşturmak için aşağıdaki yordamı kullanın. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.


## <a name="create-the-batch-job"></a>Toplu işi oluşturun
1. **Gezinti bölmesi > Modüller > Sistem yönetimi > Sorgular > Toplu işler**'e gidin.
2. **Yeni**'yi seçin.
3. **İş açıklaması** alanına toplu iş için bir açıklama girin.
4. **Zamanlanan başlangıç tarihi/saati** alanına, toplu işlemin çalışacağı tarihi ve saati girin.
5. **Kaydet**'i seçin.

## <a name="create-a-recurrence"></a>Yineleme oluşturun
1. Eylem Bölmesi'nde **Toplu iş**'i seçin.
2. **Yineleme**'yi seçin. Bu seçenekleri bir aralık ve yineleme için model girmek için kullanın.  
3. **Tamam**'ı seçin.

## <a name="add-alerts"></a>Uyarılar ekleyin
1. Eylem Bölmesi'nde **Toplu iş**'i seçin.
2. **Uyarılar**'ı seçin. Toplu işlem bittiğinde, bir hata olduğunda veya iptal edildiğinde uyarı iletileri istiyorsanız belirtin. Ardından uyarıların açılır pencere iletileri olarak gösterilmesini istiyorsanız belirtin.   
3. **Tamam**'ı seçin.

## <a name="add-a-task-to-a-batch-job"></a>Toplu işe görev ekleme
1.  **Toplu işler** sayfasında, **Görevleri görüntüle**'yi seçin.
2.  Görev oluşturmak için **CTRL+N**'yi seçin.
3.  Toplu görevin bir açıklamasını girin.
4.  **Şirket hesapları** alanında, görevin çalışacağı şirket veri tabanını seçin.
5.  **Sınıf adı** alanında, görevin çalıştırmasını istediğiniz işlemi seçin. 
6.  Uygun şekilde, görev için bir toplu grup seçin.

    İstemci görevlerinin bir toplu iş grubuna atanması gerekir. Bunlar, otomatik olarak varsayılan toplu iş grubuna atanır (boş toplu iş grubu olarak da bilinir).

7.  Görevi kaydetmek için **CTRL+S**'yi seçin.
8.  Seçili görevi projedeki başka bir göreve bağımlı hale getirmek için, **Koşullar var** kılavuzunu seçin ve tanımlamak istediğiniz her koşul için aşağıdaki adımları izleyin:

    1. Koşul oluşturmak için **CTRL+N**'yi seçin.
    2. Üst görevin görev kodunu seçin.
    3. Bağımlı görevin çalışabilmesi için üst görevin ulaşması gereken durumu seçin.
    4. Koşulu kaydetmek için **CTRL+S**'yi seçin.

    Birden fazla koşul belirlerseniz ve bağımlı görevin çalışabilmesi için *tüm* koşulların sağlanması gerekiyorsa, **Tümü** koşul tipini seçin. Bağımlı görev, koşullardan *biri* sağlandıktan sonra çalışabilirse, **Biri** koşul tipini seçin.

9.  Görev başarısızlıklarının nasıl işleneceğini seçin. **Genel** sekmesinde belirli bir görevin başarısızlığını yok saymak üzere bu görev için **Görev hatalarını yok say** seçeneğini belirleyin. Bu seçenek seçilirse, görev başarısızlığı işin başarısız olmasına neden olmaz. Bir görevin başarısız olarak kabul edilmesi için kaç kez denenmesi gerektiğini belirtmek için **Maksimum yeniden denemeler** alanını da kullanabilirsiniz. En iyi yöntem olarak, **Maksimum yeniden deneme** alanını **5**'ten büyük bir değere ayarlamamanızı öneririz.

    Toplu iş denemeleri hakkında daha fazla bilgi için bkz. [Toplu iş yeniden denemelerini etkinleştirme](../retryable-batch.md).

## <a name="adjust-batch-job-status"></a>Toplu iş durumunu düzelt
1. **Sistem yönetimi > Sorgular > Toplu işler**'e gidin.
2. Uygun olan toplu işi seçin.
3. Eylem Bölmesi'nde **Toplu iş > İşlevler > Durumu değiştir**'i seçin.
4. Uygun olan durumu seçin:
    - **Stopaj**: Toplu işi **stopaj** olarak ayarlayın, böylece toplu iş planlayıcısından kesilir. *Durdur* ile eşdeğerdir.
    - **Bekliyor**: Toplu işi **bekliyor** olarak ayarlayın, böylece toplu iş planlayıcısı tarafından alınmayı bekler. *Git* ile eşdeğerdir.
5. **Tamam**'ı seçin.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
