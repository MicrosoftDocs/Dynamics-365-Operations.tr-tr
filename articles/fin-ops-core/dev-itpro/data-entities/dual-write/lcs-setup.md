---
title: Lifecycle Services'tan çift yazma kurulumu
description: Bu konu, yeni bir Finance and Operations ortamı ile yeni bir Common Data Service ortamı arasında Microsoft Dynamics Lifecycle Services'tan (LCS) nasıl çift yazma bağlantısı kurulabileceğini açıklar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
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
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 75765c0cc03c64030fac6bc656f57a143828b85b
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112536"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Lifecycle Services'tan çift yazma kurulumu

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Bu konu, yeni bir Finance and Operations ortamı ile yeni bir Common Data Service ortamı arasında Microsoft Dynamics Lifecycle Services'tan (LCS) nasıl çift yazma bağlantısı kurulabileceğini açıklar.

## <a name="prerequisites"></a>Önkoşullar

Çift yazma bağlantısı kurmak için yönetici olmanız gerekir.

+ Kiracıya erişiminiz olmalıdır.
+ Hem Finance and Operations ortamları hem de Common Data Service ortamlarında yönetici olmanız gerekir.

## <a name="set-up-a-dual-write-connection"></a>Çift yazma bağlantısı ayarlama

Çift yazma bağlantısı ayarlamak için aşağıdaki adımları izleyin.

1. LCS'de projenize gidin.
2. Yeni bir ortam dağıtmak için **Yapılandır**'ı seçin.
3. Sürümü seçin. 
4. Topolojiyi seçin. Kullanılabilir yalnızca bir topoloji varsa, otomatik olarak seçilir.
5. **Dağıtım ayarları** sihirbazında ilk adımları tamamlayın.
6. **Common Data Service** sekmesinde, aşağıdaki adımlardan birini uygulayın:

    - Common Data Service ortamı kiracınız için zaten sağlanmışsa, onu seçebilirsiniz.

        1. **Common Data Service'ı yapılandır** seçeneğini **Evet** olarak ayarlayın.
        2. **Kullanılabilir ortamlar** alanında, Finance and Operations verileriyle tümleştirilecek ortamı seçin. Liste, yönetici ayrıcalıklarına sahip olduğunuz tüm ortamları içerir.
        3. Hüküm ve koşulları kabul etmiş olduğunuzu belirtmek için **Kabul et** onay kutusunu seçin.

        ![Common Data Service ortamı kiracınız için zaten sağlandığında Common Data Service sekmesi](../dual-write/media/lcs_setup_1.png)

    - Kiracınızda Common Data Service ortamı yoksa, yeni bir ortam sağlanacaktır.

        1. **Common Data Service'ı yapılandır** seçeneğini **Evet** olarak ayarlayın.
        2. Common Data Service ortamı için bir ad girin.
        3. Ortamın dağıtılacağı bölgeyi seçin.
        4. Ortam için varsayılan dili ve para birimini seçin.

            > [!NOTE]
            > Dil ve para birimini daha sonra değiştiremezsiniz.

        5. Hüküm ve koşulları kabul etmiş olduğunuzu belirtmek için **Kabul et** onay kutusunu seçin.

        ![Kiracınızda Common Data Service ortamı olmadığında Common Data Service sekmesi](../dual-write/media/lcs_setup_2.png)

7. **Dağıtım ayarları** sihirbazında kalan adımları tamamlayın.
8. Ortamın durumu **Dağıtıldı** olduktan sonra, ortam ayrıntıları sayfasını açın. **Common Data Service ortam bilgileri** bölümü, Finance and Operations ortamı adını ve bağlanan Common Data Service ortamı adını gösterir.

    ![Common Data Service ortam bilgileri bölümü](../dual-write/media/lcs_setup_3.png)

9. Finance and Operations ortam yöneticisinin LCS'de oturum açması ve bağlantıyı tamamlamak için **Uygulamalar için CDS'ye Bağla**'yı seçmesi gerekir. Ortam ayrıntıları sayfası yöneticinin ilgili kişi bilgilerini gösterir.

    Bağlantı tamamlandıktan sonra, durum **Ortam bağlantısı başarıyla tamamlandı** olarak güncelleştirilir.

10. Finance and Operations ortamındaki **Veri tümleştirme** çalışma alanını açmak ve kullanılabilir şablonları kontrol etmek için **Uygulamalar için CDS'ye Bağla**'yı seçin.

    ![Common Data Service ortam bilgileri bölümündeki Uygulamalar için CDS'ye Bağla düğmesi](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> Ortamların bağlantısını LCS kullanarak kaldıramazsınız. Bir ortamın bağlantısını kaldırmak için Finance and Operations ortamdaki **Veri tümleştirme** çalışma alanını açın ve sonra **Bağlantıyı kaldır**'ı seçin.
