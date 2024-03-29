---
title: Veri tümleştirme projesi oluşturma
description: Bu makalede, veri tümleştirme projesinin nasıl oluşturulacağı açıklanmaktadır.
author: ShivamPandey-msft
ms.date: 05/06/2022
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
ms.openlocfilehash: 4ff4f88c6c5d55d853aebd7d437bfb107292fb2f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876254"
---
# <a name="create-a-data-integration-project"></a>Veri tümleştirme projesi oluşturma

[!include [banner](../includes/banner.md)]

Bu makalede, veri tümleştirme projesinin nasıl oluşturulacağı açıklanmaktadır.

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

    1. Yeni oluşturduğunuz bağlantı kümesini kullanarak aşağıdaki her bir şablon için tek bir veri tümleştirme projesi oluşturun:

        - Müşteri ödeme içgörüleri sonucu (CDS-Fin and Ops 10.0.17+)
        - Nakit akışı zaman serisi sonuçları (CDS-Fin and Ops)
        - Bütçe zaman serisi sonuçları (CDS-Fin and Ops)

      > [!NOTE]
      > Her şablon için birden çok veri tümleştirme projesi oluşturmak, güncelleştirmeleri engelleyen hatalara neden olabilir.

    2. Her proje için uygun zamanlamayı ayarlayın.

> [!NOTE]
> Dataverse'te gerekli varlıkları göremiyorsanız **Alacak ve tahsilatlar** > **Kurulum** > **Finance Insights** > **Finance Insights parametreleri** bölümüne gidin, **Müşteri ödeme tahminleri** özelliğini etkinleştirin ve **Tahmin modeli oluştur**'u seçin. Yapay zeka modelinin dağıtımı tamamlandığında tümleştirmeyi oluşturmak için gerekli Dataverse varlıkları dağıtılır.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
