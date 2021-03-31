---
title: Planlamayı En İyi Duruma Getirme ile otomatik kesinleştirme
description: Bu konuda, Planlamayı En İyi Duruma Getirme işlevi ile otomatik kesinleştirmenin nasıl kullanılacağı açıklanmaktadır.
author: ChristianRytt
manager: tfehr
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: 9106137fe6dd097beea9914cdde541e581946f46
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227810"
---
# <a name="autofirming-with-planning-optimization"></a>Planlamayı En İyi Duruma Getirme ile otomatik kesinleştirme

[!include [banner](../../includes/banner.md)]

Otomatik kesinleştirme, planlı siparişleri master planlama işleminin parçası olarak kesinleştirmenize (başka bir deyişle, serbest bırakmanıza) olanak tanır. Planlı siparişler kesinleştirildiğinde, gerçek satınalma siparişlerine, transfer emirlerine veya üretim emirlerine dönüştürülür. Planlamayı En İyi Duruma Getirme işlevi kullanıldığında sipariş tarihi kesinleştirme zaman dilimi içindeyse planlı siparişler, bir master planlama çalışması sırasında kesinleştirilir.

> [!NOTE]
> Planlanan bir satınalma siparişinin otomatik kesinleştirilmesi için bir maddenin bir satıcı ile ilişkilendirilmesi gerekir.

## <a name="turn-on-autofirming"></a>Otomatik kesinleştirmeyi açma

Otomatik kesinleştirmeyi açmak için aşağıdaki adımları izleyin.

1. **Özellik yönetimi** çalışma alanındaki **Yeni** sekmesinde listeden **Planlamayı En İyi Duruma Getirmek için otomatik kesinleştirme**'yi seçin. Özellik, **Yeni** sekmesinde görünmüyorsa **Etkileştirilmemiş** ve **Tümü** sekmelerine bakın.
1. **Şimdi etkinleştir**'i seçin. Alternatif olarak, **Planla**'yı seçin ve ardından özelliğin açılmasını istediğiniz zamanı seçin.

## <a name="set-up-the-firming-time-fence"></a>Kesinleştirme zaman dilimini ayarlayın.

Kesinleştirme zaman dilimi master planlama çalıştırma tarihinden ileriye doğru hesaplanır. Girdiğiniz gün sayısına göre tanımlanır. Kesinleştirme zaman dilimini aşağıdaki yollarla kontrol edebilirsiniz:

- Bir kapsam grubu için varsayılan kesinleştirme zaman dilimini tanımlamak üzere **Master planlama** \> **Ayar** \> **Karşılama** \> **Karşılama grupları**'na gidin ve bir karşılama grubu seçin. Ardından **Diğer** hızlı sekmesinde, **Otomatik kesinleştirme zaman dilimi (gün sayısı)** alanına gün sayısını girin.
- Belirli bir maddenin karşılama grubu için tanımlanan kesinleştirme zaman dilimini geçersiz kılmak için **Ürün bilgileri yönetimi** \> **Serbest bırakılan ürünler**'e gidin ve ardından Eylem Bölmesi'nden **Plan**'ı ve **Madde karşılama**'yı seçin. Ardından **Genel** sekmesinde, **Zaman dilimini geçersiz kıl**'ı seçin ve **Otomatik kesinleştirme zaman dilimi (gün)** alanına gün sayısını girin.
- Belirli bir master planın kapsam grubu ve madde kapsamı için tanımlanan kesinleştirme zaman dilimi üzerine yazmak için **Master planlama** \> **Ayar** \> **Master planlar**'a gidin ve bir Master plan seçin. Ardından **Gün cinsinden zaman dilimi** hızlı sekmesinde, **Kesinleştir** seçeneğini **Evet** olarak ayarlayın ve gün sayısını girin.

Planlama İyileştirmesi işlevini kullanan otomatik kesinleştirme özelliği bir master planlama çalışması için açılırsa otomatik kesinleştirme işlemi, otomatik kesinleştirme ayarına göre gerçekleştirilir. Otomatik kesinleştirme açılmazsa veya planlama **Net gereksinimler** sayfasından başlatılırsa otomatik kesinleştirme işlemi atlanır.

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a>Planlamayı En İyi Duruma Getirme işleviyle yerleşik Supply Chain Management planlama altyapısının karşılaştırılması

Planlamayı En İyi Duruma Getirme ve Microsoft Dynamics 365 Supply Chain Management'ta yerleşik olan planlama altyapısı işlevlerinin ikisi de planlı siparişleri kesinleştirmek için kullanılabilir. Ancak, bazı önemli farklar vardır. Örneğin, Planlamayı En İyi Duruma Getirme işlevi hangi planlı siparişlerin kesinleştirileceğini belirlemek için sipariş tarihini (başka bir deyişle, başlangıç tarihi) kullanırken yerleşik Supply Chain Management planlama altyapısı gereksinim tarihini (başka bir deyişle, bitiş tarihi) kullanır. Aşağıda, farkların bir özeti verilmiştir.

**Planlamayı En İyi Duruma Getirme**

- Otomatik kesinleştirme, sipariş tarihini (başlangıç tarihi) temel alır.
- Sipariş tarihi (başlangıç tarihi) kesinleştirmeyi tetiklediğinden sağlama süresini kesinleştirme zaman diliminin bir parçası olarak düşünmeniz gerekmez.
- Geçerli haftada başlaması gereken tüm siparişleri kesinleştirmek istiyorsanız kesinleştirme zaman dilimi bir hafta olmalıdır.

**Yerleşik Supply Chain Management planlama altyapısı**

- Otomatik kesinleştirme, gereksinim tarihini (bitiş tarihi) temel alır.
- Siparişlerin vade tarihinde kesinleştirilmesini garanti etmeye yardımcı olması için kesinleştirme zaman dilimi, sağlama süresinden daha uzun olmalıdır.
- Geçerli haftada başlaması gereken tüm siparişleri kesinleştirmek istiyorsanız kesinleştirme zaman dilimi, sağlama süresi artı bir hafta olmalıdır.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]