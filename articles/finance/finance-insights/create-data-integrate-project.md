---
title: Veri tümleştirme projesi oluşturma
description: Bu konuda, veri tümleştirme projesinin nasıl oluşturulacağı açıklanmaktadır.
author: ShivamPandey-msft
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 50f435f9d461667a1908baa529d73766085c183a
ms.sourcegitcommit: 6526acd0300d9c5800d3d7675d54e23090d031df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/10/2022
ms.locfileid: "8107299"
---
# <a name="create-a-data-integration-project"></a>Veri tümleştirme projesi oluşturma

[!include [banner](../includes/banner.md)]

Bu konuda, veri tümleştirme projesinin nasıl oluşturulacağı açıklanmaktadır.

1. Microsoft Dynamics 365 Finance'te oturum açın.
2. **Çalışma alanları \> Veri yönetimi** bölümüne gidin ve **Veri varlıkları**'nı seçin. Bir sonraki adıma geçmeden önce tüm veri varlıkları yenilenene kadar bekleyin.
3. [Power Apps portalını](https://make.powerapps.com/) açıp şu adımları izleyin:

    1. Uygun ortamı seçin.
    2. Sol gezinti bölmesinde **Dataverse \> Bağlantılar** öğesini seçin.
    3. Aşağıdaki öğelerin uygun kurulumlarına bağlanın:

        - Dynamics 365
        - Fin & Ops için Dynamics 365

4. [Power Apps ortamlarını](https://admin.powerapps.com/environments) açıp şu adımları izleyin:

    1. **Veri tümleştirme**'yi seçin.
    2. **Bağlantı kümeleri**'ni seçin.
    3. **Yeni bağlantı kümesi**'ni seçin.
    4. Bağlantı için bir ad girin.
    5. Aşağıdaki öğeler için uygun bağlantıları seçin:

        - Dynamics 365
        - Fin & Ops için Dynamics 365

    6. Uygun kuruluş eşlemesini seçin.
    7. **Oluştur**'u seçin.

5. [Power Apps ortamlarını](https://admin.powerapps.com/environments) açıp şu adımları izleyin:  

    1. Yeni oluşturduğunuz bağlantı kümesini kullanarak aşağıdaki şablonlar için veri tümleştirme projeleri oluşturun:

        - Müşteri ödeme içgörüleri sonucu (CDS-Fin and Ops 10.0.17+)
        - Nakit akışı zaman serisi sonuçları (CDS-Fin and Ops)
        - Bütçe zaman serisi sonuçları (CDS-Fin and Ops)

    2. Her proje için uygun zamanlamayı ayarlayın.

> [!NOTE]
> Dataverse'te gerekli varlıkları göremiyorsanız **Alacak ve tahsilatlar** > **Kurulum** > **Finance Insights** > **Finance Insights parametreleri** bölümüne gidin, **Müşteri ödeme tahminleri** özelliğini etkinleştirin ve **Tahmin modeli oluştur**'u seçin. Yapay zeka modelinin dağıtımı tamamlandığında tümleştirmeyi oluşturmak için gerekli Dataverse varlıkları dağıtılır.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
