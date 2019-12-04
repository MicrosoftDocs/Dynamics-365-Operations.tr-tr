---
title: Satıcı tasarımları arasında geçiş yapma
description: ''
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
ms.openlocfilehash: 4e97ff0b0e6195b5e3703e15a0bb0de7644ef8d1
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772376"
---
# <a name="switch-between-vendor-designs"></a>Satıcı tasarımları arasında geçiş yapma

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a>Satıcı veri akışı 

Satıcı yönetimi için diğer Dynamics 365 uygulamalarını kullanmak ve satıcı bilgilerini müşterilerden ayırmak istiyorsanız bu temel satıcı tasarımını kullanın.  

![Temel satıcı akışı](media/dual-write-switch-1.png)
 
Satıcı yönetimi için diğer Dynamics 365 uygulamalarını kullanmak ve satıcı bilgilerini depolamak için **Hesap** varlığını kullanmaya devam etmek istiyorsanız bu genişletilmiş satıcı tasarımını kullanın. Bu tasarımda, satıcı beklemede durumu ve satıcı profili gibi genişletilmiş satıcı bilgileri Common Data Service'te **satıcılar** varlığında depolanır. 

![Genişletilmiş satıcı akışı](media/dual-write-switch-2.png)
 
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
    5. Satıcı bilgilerini depolamak için Customer Engagement **Hesap** varlığını kullanmaya başlamak için **Hesap** ve **Satıcı** varlıklarında oluşturduğunuz iş akışlarını etkinleştirin. 
 
