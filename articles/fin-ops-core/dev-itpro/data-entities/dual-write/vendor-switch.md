---
title: Satıcı tasarımları arasında geçiş yapma
description: Bu konu Finance and Operations uygulamaları ile Common Data Service arasında satıcı verisi tümleştirmesi arasında geçiş yapmayı açıklar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 587a9b98f28b11e303aff4b59e9726f220d956eb
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2020
ms.locfileid: "3020053"
---
# <a name="switch-between-vendor-designs"></a>Satıcı tasarımları arasında geçiş yapma

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

## <a name="vendor-data-flow"></a>Satıcı veri akışı 

Satıcı yönetimi için diğer Dynamics 365 uygulamalarını kullanmak ve satıcı bilgilerini müşterilerden ayırmak istiyorsanız bu temel satıcı tasarımını kullanın.  

![Temel satıcı akışı](media/dual-write-vendor-data-flow.png)
 
Satıcı yönetimi için diğer Dynamics 365 uygulamalarını kullanmak ve satıcı bilgilerini depolamak için **Hesap** varlığını kullanmaya devam etmek istiyorsanız bu genişletilmiş satıcı tasarımını kullanın. Bu tasarımda, satıcı beklemede durumu ve satıcı profili gibi genişletilmiş satıcı bilgileri Common Data Service'te **satıcılar** varlığında depolanır. 

![Genişletilmiş satıcı akışı](media/dual-write-vendor-detail.jpg)
 
Genişletilmiş satıcı tasarımını kullanmak için aşağıdaki adımları izleyin: 
 
1. **SupplyChainCommon** çözüm paketi, aşağıdaki görüntüde gösterilen iş akışı işlem şablonlarını içerir.
    > [!div class="mx-imgBorder"]
    > ![İş akışı işlem şablonları](media/dual-write-switch-3.png)
2. İş akışı işlem şablonlarını kullanarak yeni iş akışı işlemleri oluşturma: 
    1. **Hesap Varlığında Satıcılar Oluşturma** iş akışı işlemi şablonunu kullanarak **Satıcı** varlığı için yeni bir iş akışı işlemi oluşturun ve **Tamam**'a tıklayın. Bu iş akışı **Hesap** varlığı için satıcı oluşturma senaryosunu işler.
        > [!div class="mx-imgBorder"]
        > ![Hesap Varlığında Satıcılar oluşturma](media/dual-write-switch-4.png)
    2. **Hesaplar Varlığını Güncelleştirme** iş akışı işlemi şablonunu kullanarak **Satıcı** varlığı için yeni bir iş akışı işlemi oluşturun ve **Tamam**'a tıklayın. Bu iş akışı **Hesap** varlığı için satıcı güncelleştirme senaryosunu işler. 
        > [!div class="mx-imgBorder"]
        > ![Hesaplar Varlığını Güncelleştirme](media/dual-write-switch-5.png)
    3. **Hesaplar** varlığında oluşturulan şablonlardan yeni iş akışı işlemleri oluşturun. 
        > [!div class="mx-imgBorder"]
        > ![Satıcılar varlığında satıcılar oluşturma](media/dual-write-switch-6.png)
        > [!div class="mx-imgBorder"]
        > ![Satıcı varlığını güncelleştirme](media/dual-write-switch-7.png)
    4. İş akışlarını gereksinimlerinize göre gerçek zamanlı veya arka plan iş akışları olarak yapılandırabilirsiniz. 
        > [!div class="mx-imgBorder"]
        > ![Arka plan iş akışına dönüştürme](media/dual-write-switch-8.png)
    5. Satıcı bilgilerini depolamak için **Hesap** varlığını kullanmaya başlamak için **Hesap** ve **Satıcı** varlıklarında oluşturduğunuz iş akışlarını etkinleştirin. 
 
