---
title: Lifecycle Services'dan çift yazma kurulumu
description: Bu konuda, Microsoft Dynamics Lifecycle Services (LCS) portalından nasıl çift yazma bağlantısı ayarlayacağınız açıklanmaktadır.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 6971c8e2d5fa03c2991b9a3054c638cff6322c8b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567732"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Lifecycle Services'dan çift yazma kurulumu

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu konu, yeni bir Finance and Operations ortamı ile yeni bir Dataverse ortamı arasında Microsoft Dynamics Lifecycle Services'tan (LCS) nasıl çift yazma bağlantısı kurulabileceğini açıklar.

## <a name="prerequisites"></a>Önkoşullar

Çift yazma bağlantısı kurmak için yönetici olmanız gerekir.

+ Kiracıya erişiminiz olmalıdır.
+ Hem Finance and Operations ortamları hem de Dataverse ortamlarında yönetici olmanız gerekir.

## <a name="set-up-a-dual-write-connection"></a>Çift yazma bağlantısı ayarlama

Çift yazma bağlantısı ayarlamak için aşağıdaki adımları izleyin.

1. LCS'de projenize gidin.
2. Yeni bir ortam dağıtmak için **Yapılandır**'ı seçin.
3. Sürümü seçin. 
4. Topolojiyi seçin. Kullanılabilir yalnızca bir topoloji varsa, otomatik olarak seçilir.
5. **Dağıtım ayarları** sihirbazında ilk adımları tamamlayın.
6. **Dataverse** sekmesinde, aşağıdaki adımlardan birini uygulayın:

    - Dataverse ortamı kiracınız için zaten sağlanmışsa, onu seçebilirsiniz.

        1. **Dataverse'ı yapılandır** seçeneğini **Evet** olarak ayarlayın.
        2. **Kullanılabilir ortamlar** sütununda, Finance and Operations verileriyle tümleştirilecek ortamı seçin. Liste, yönetici ayrıcalıklarına sahip olduğunuz tüm ortamları içerir.
        3. Hüküm ve koşulları kabul etmiş olduğunuzu belirtmek için **Kabul et** onay kutusunu seçin.

        ![Dataverse ortamı kiracınız için zaten sağlandığında Dataverse sekmesi](../dual-write/media/lcs_setup_1.png)

    - Kiracınızda Dataverse ortamı yoksa, yeni bir ortam sağlanacaktır.

        1. **Dataverse'ı yapılandır** seçeneğini **Evet** olarak ayarlayın.
        2. Dataverse ortamı için bir ad girin.
        3. Ortamın dağıtılacağı bölgeyi seçin.
        4. Ortam için varsayılan dili ve para birimini seçin.

            > [!NOTE]
            > Dil ve para birimini daha sonra değiştiremezsiniz.

        5. Hüküm ve koşulları kabul etmiş olduğunuzu belirtmek için **Kabul et** onay kutusunu seçin.

        ![Kiracınızda Dataverse ortamı olmadığında Dataverse sekmesi](../dual-write/media/lcs_setup_2.png)

7. **Dağıtım ayarları** sihirbazında kalan adımları tamamlayın.
8. Ortamın durumu **Dağıtıldı** olduktan sonra, ortam ayrıntıları sayfasını açın. **Power Platform Tümleştirmesi** bölümü, Finance and Operations ortamı adını ve bağlanan Dataverse ortamı adını gösterir.

    ![Power Platform Tümleştirmesi bölümü](../dual-write/media/lcs_setup_3.png)

9. Finance and Operations ortam yöneticisinin LCS'de oturum açması ve bağlantıyı tamamlamak için **Uygulamalar için CDS'ye Bağla**'yı seçmesi gerekir. Ortam ayrıntıları sayfası yöneticinin ilgili kişi bilgilerini gösterir.

    Bağlantı tamamlandıktan sonra, durum **Ortam bağlantısı başarıyla tamamlandı** olarak güncelleştirilir.

10. Finance and Operations ortamındaki **Veri tümleştirme** çalışma alanını açmak ve kullanılabilir şablonları kontrol etmek için **Uygulamalar için CDS'ye Bağla**'yı seçin.

    ![Power Platform Tümleştirmesi bölümündeki Uygulamalar için CDS'ye Bağla düğmesi](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> Ortamların bağlantısını LCS kullanarak kaldıramazsınız. Bir ortamın bağlantısını kaldırmak için Finance and Operations ortamdaki **Veri tümleştirme** çalışma alanını açın ve sonra **Bağlantıyı kaldır**'ı seçin.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]