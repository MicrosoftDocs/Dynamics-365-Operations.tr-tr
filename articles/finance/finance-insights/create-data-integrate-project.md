---
title: Veri tümleştirici projesi oluşturma (önizleme)
description: Bu konuda, veri tümleştirici projesinin nasıl oluşturulacağı açıklanmaktadır.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: a32ad6eb1b1874a9f9ec452def3c213cd160c5faa2aec02b655a86e160e2b509
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768999"
---
# <a name="create-a-data-integrator-project-preview"></a>Veri tümleştirici projesi oluşturma (önizleme)

[!include [banner](../includes/banner.md)]

Bu konuda, veri tümleştirici projesinin nasıl oluşturulacağı açıklanmaktadır.

1. Microsoft Dynamics 365 Finance'te oturum açın.
2. **Çalışma alanları \> Veri yönetimi** bölümüne gidin ve **Veri varlıkları**'nı seçin. Bir sonraki adıma geçmeden önce tüm veri varlıkları yenilenene kadar bekleyin.
3. [Power Apps portalını](https://make.powerapps.com/) açıp şu adımları izleyin:

    1. Uygun ortamı seçin.
    2. Sol gezinti bölmesinde **Veri \> Bağlantılar** öğesini seçin.
    3. Aşağıdaki öğelerin uygun kurulumlarına bağlanın:

        - Dynamics 365
        - Fin & Ops için Dynamics 365

4. [Power Apps ortamlarını](https://admin.powerapps.com/environments) açıp şu adımları izleyin:

    1. **Veri tümleştiricisi**'ni seçin.
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

        - Müşteri ödeme içgörüleri sonuçları (CDS-Fin and Ops)
            - Sürüm 10.0.17 veya üstünü kullanıyorsanız, Müşteri ödeme içgörüleri sonucu (CD-Fin and Ops 10.0.17 +) adlı şablonu kullanmanız gerekir.
        - Nakit akışı zaman serisi sonuçları (CDS-Fin and Ops)
        - Bütçe zaman serisi sonuçları (CDS-Fin and Ops)

    2. Her proje için uygun zamanlamayı ayarlayın.

> [!NOTE]
> CDS'te gerekli varlıkları göremiyorsanız **Alacak ve tahsilatlar > Kurulum > Mali İçgörüler > Mali içgörü parametreleri** bölümüne gidin, Müşteri ödeme tahminleri özelliğini etkinleştirin ve **Tahmin modeli oluştur** düğmesine tıklayın. Yapay zeka modelinin dağıtımı tamamlandığında (başarılı veya başarısız), tümleştirmeyi oluşturmak için gerekli CDS varlıkları CDS'ye dağıtılır.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
