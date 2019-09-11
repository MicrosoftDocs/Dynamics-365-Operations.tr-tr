---
title: Bakım kesinti süresi
description: Bu konuda Varlık Yönetimi'ndeki bakım kesinti süresini açıklar.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cc79dc1b5911679586fa560142ada5add1a881d2
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918256"
---
# <a name="maintenance-downtime"></a>Bakım kesinti süresi


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Bir iş emrinde seçilen kıymet üzerinde bakım kapalı kalma kayıtları oluşturabilirsiniz. Bu, üretim alanındaki bir veya daha fazla makinede bakım kapalı kalma süresini kaydetmek istediğinizde yararlıdır. Önce, kullanmak istediğiniz bakım kapalı kalma nedeni kodlarını (örneğin, döküm ve planlı durak) oluşturursunuz. Bu, **Bakım kesinti süresi sebep kodları** içinde gerçekleştirilir. Ardından **bakım kapalı kalma süresi** ve ilgili neden kodlarını ekleyebileceğiniz bakım süresi kaydı oluşturabilirsiniz.

## <a name="create-maintenance-downtime-reason-codes"></a>Bakım kesinti süresi sebep kodları oluşturma

1. **Varlık yönetimi** > **Kurulum** > **İş emirleri** > **Bakım kesinti süresi sebep kodları**'na tıklayın.

2. **Yeni**'ye tıklayın.

3. **Bakım kesinti nedeni kodu** alanına bir kimlik ekleyin.

4. **Ad** alanında sebep kodu için bir ad girin.

5. **KPI dahil et** onay kutusunu, sebep kodu varlık KPI hesaplamalarına dahil edilecekse seçin. Genel olarak, planlanan üretim durakları beklenen performansı etkilemediği için KPI hesaplamalarına dahil edilmelidir.

6. **Kaydet**'e tıklayın.

![Şekil 1](media/15-work-orders.png)


Kullanmak istediğiniz bakım kapalı kalma nedeni kodlarını oluşturduğunuzda, iş emirleri ve varlıklar için bakım kapalı kalma kayıtları oluşturabilirsiniz.


## <a name="create-maintenance-downtime-registrations"></a>Bakım kesinti süresi kayıtları oluşturma

1. **Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ne tıklayın.

2. İş emrini seçin ve **bakım kapalı kalma süresini** tıklatın.

3. **Yeni**'ye tıklayın.

4. **Başlangıç** ve **Bitiş** alanlarında bakım kesinti süresi için tarih ve saat aralığını girin.

5. **Giden** alanından çıktığınızda, saatlerin süresi otomatik olarak **Süre** alanına girilir.

6. **Bakım kesinti süresi sebep kodu** alanında bir sebep kodu girin.

7. Daha fazla kayıt eklemek istiyorsanız, 3-6 arasındaki adımları yineleyin.

8. **Kaydet**'e tıklayın.


![Şekil 2](media/16-work-orders.png)


Bakım kapalı kalma süresini hesaplamak için kullanılan takvim, kıymetler ve parametreler kurulumunda yaptığınız seçime bağlıdır. Kaynak **Tüm varlıklar** > **Sabit varlıklar** Hızlı sekmesi > **Kaynak** alanındaki bir varlıkta seçildiyse, ilişkili kaynak grubu için takvim kurulumu aşağıdaki şekildeki gibi gösterilir.

![Şekil 3](media/17-work-orders.png)


Varlık üzerinde bir kaynak seçilmemişse, **Varlık yönetimi parametreleri** içinde seçilen standart takvim içinde kullanılır, aşağıdaki şekilde görüntülendiği gibi.

![Şekil 4](media/18-work-orders.png)


**Kurumsal varlık yönetimi** > **Sorgular** > **Bakım kesinti süresi** üzerine tıklayarak tüm bakım kesinti süresi kayıtlarının bir genel bakışını görebilirsiniz.

>[!NOTE]
>**Varlık Yönetimi** modülü içinde kullanılan tüm takvimler, **Kuruluş yönetimi** > **Kurulum** > **Takvimler** > **Takvimler** içinde ayarlanır.

