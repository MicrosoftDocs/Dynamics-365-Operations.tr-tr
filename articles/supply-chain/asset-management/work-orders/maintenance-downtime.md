---
title: Bir iş emri için bakım kesinti süresi
description: Bu konuda bir iş emrinde seçilen kıymet üzerinde bakım kesinti süresi kayıtlarının nasıl oluşturulacağı açıklanır.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 09c20020e5e0b957785a88ad511cedfec50a5f29
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344628"
---
# <a name="maintenance-downtime-for-work-orders"></a>Bir iş emri için bakım kesinti süresi

[!include [banner](../../includes/banner.md)]


Bir iş emrinde seçilen kıymet üzerinde bakım kesinti süresi kayıtları oluşturabilirsiniz. Bu özellik, üretim alanındaki bir veya daha fazla makinede bakım kapalı kalma süresini kaydetmek istediğinizde yararlıdır. Önce, kullanmak istediğiniz bakım kesinti süresi nedeni kodlarını (örneğin, **Döküm** ve **Planlı durdurma**) oluşturursunuz. Bu adım, **Bakım kesinti süresi sebep kodları** sayfasında gerçekleştirilir. **Bakım kesinti süresi** sayfasında bakım kesinti süresi kayıtları oluşturabilir ve ilgili bakım kesinti süresi neden kodlarını ekleyebilirsiniz.

## <a name="create-maintenance-downtime-reason-codes"></a>Bakım kesinti süresi sebep kodları oluşturma

1. **Varlık yönetimi** > **Kurulum** > **İş emirleri** > **Bakım kesinti süresi neden kodları**'nı seçin.

2. **Yeni**'yi seçin.

3. **Bakım kesinti süresi neden kodu** alanına bakım kesinti süresi neden kodu için bir kod girin.

4. **Ad** alanına, bir ad girin.

5. Neden kodunun varlığın temel performans göstergeleri (KPI) hesaplamalarına dahil edilmesi gerekiyorsa, **KPI dahil et** onay kutusunu seçin. Genel olarak, planlanan üretim durakları beklenen performansı etkilemediği için KPI hesaplamalarına dahil edilmelidir.

6. **Kaydet**'i seçin.

Aşağıdaki şekilde bir **Bakım kesinti süresi neden kodları** sayfası örneği gösterilmektedir.

![Şekil 1.](media/15-work-orders.png)

Kullanmak istediğiniz bakım kesinti süresi nedeni kodlarını oluşturduktan sonra, iş emirleri ve varlıklar için bakım kesinti süresi kayıtları oluşturabilirsiniz.


## <a name="create-maintenance-downtime-registrations"></a>Bakım kesinti süresi kayıtları oluşturma

1. **Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ne tıklayın.

2. İş emrini seçin ve **İş emri** sekmesinde, **Varlık** grubunda **Bakım kesinti süresi** öğesini seçin.

3. **Yeni**'yi seçin.

4. **Başlangıç** ve **Bitiş** alanlarında bakım kesinti süresi kaydı için tarih ve saat aralığını tanımlayın.

>[!NOTE]
>**Giden** alanından çıktığınızda, saatlerin süresi otomatik olarak **Süre** alanına girilir.

5. **Bakım kesinti süresi neden kodu** alanında bir neden kodu seçin.

6. Daha fazla kayıt eklemek için 3 ile 5. adımlar arasındaki işlemleri tekrarlayın.

7. **Kaydet**'i seçin.

Aşağıdaki şekilde bir bakım kesinti süresi kaydı örneği gösterilmiştir.

![Şekil 2.](media/16-work-orders.png)

Bakım kapalı kalma süresini hesaplamak için kullanılan takvim, varlıklar ve parametreler kurulumunda yaptığınız seçime bağlıdır. **Tüm varlıklar** sayfasının **Sabit kıymetler** hızlı sekmesindeki **Kaynak** alanındaki bir varlıkta kaynak seçildiyse, ilişkili kaynak grubu için takvim kurulumu aşağıdaki şekildeki gibi gösterilir.

![Şekil 3.](media/17-work-orders.png)

Varlık üzerinde bir kaynak seçilmemişse, **Varlık yönetimi parametreleri** sayfasında seçilen standart takvim içinde kullanılır, aşağıdaki şekilde görüntülendiği gibi.

![Şekil 4.](media/18-work-orders.png)

**Varlık yönetimi** > **Sorgular** > **Bakım kesinti süresi**'ne tıklayarak tüm bakım kesinti süresi kayıtlarına genel bir bakışı görebilirsiniz.

>[!NOTE]
>**Varlık Yönetimi** modülü içinde kullanılan tüm takvimler, **Kuruluş yönetimi** > **Kurulum** > **Takvimler** > **Takvimler** içinde ayarlanır.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]