---
title: Lifecycle Services'dan çift yazma kurulumu
description: Bu konuda, Microsoft Dynamics Lifecycle Services (LCS) portalından nasıl çift yazma bağlantısı ayarlayacağınız açıklanmaktadır.
author: RamaKrishnamoorthy
ms.date: 05/11/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: eb4170ef6cb09c862f6a4163670c519d5d8077fb
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103581"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Lifecycle Services'dan çift yazma kurulumu

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu konuda, Microsoft Dynamics Lifecycle Services (LCS) portalından nasıl çift yazma bağlantısı ayarlayacağınız açıklanmaktadır.

## <a name="prerequisites"></a>Önkoşullar

Power Platform tümleştirmeyi aşağıdaki konularda açıklandığı gibi tamamlamanız gerekir:

+ [Power Platform Tümleştirme - Ortam dağıtımı sırasında etkinleştir](../../power-platform/overview.md#enable-during-environment-deployment)
+ [Power Platform Tümleştirme - Ortam dağıtımı sonrasında ayarlama](../../power-platform/overview.md#set-up-after-environment-deployment)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a>Yeni Dataverse ortamları için çift yazmayı ayarlama

LCS **Ortam Ayrıntıları** sayfasından çift yazma ayarlamak için şu adımları izleyin:

1. **Ortam Ayrıntıları** sayfasında **Power Platform Tümleştirme** bölümünü genişletin.

2. **Çift yazma uygulaması** düğmesini seçin.

    ![Power Platform Tümleştirmesi](media/powerplat_integration_step2.png)

3. Hüküm ve koşulları inceleyin ve ardından **Yapılandır**'ı seçin.

4. Devam etmek için **Tamam**'ı seçin.

5. Ortam ayrıntıları sayfasını düzenli aralıklarla yenileyerek ilerleme durumunu izleyebilirsiniz. Kurulum genellikle 30 dakika veya daha az sürer.  

6. Kurulum tamamlandığında, işlemin başarılı olup olmadığını veya bir hata olup olmadığını bildiren bir ileti bildirir. Kurulum başarısız olursa, ilgili bir hata iletisi görüntülenir. Sonraki adıma geçmeden önce hataları düzeltmeniz gerekir.

7. Geçerli ortamın veritabanları ile Dataverse arasında bağlantı oluşturmak için **Power Platform Ortama bağla**'yı seçin. Bu genellikle 5 dakikadan daha az sürer.

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Power Platform ortamı bağlantısı":::

8. Bağlama tamamlandığında, bir köprü görüntülenir. Finance and Operations ortamdaki çift yazma yönetim alanına giriş yapmak için bağlantıyı kullanın. Buradan varlık eşlemeleri ayarlayabilirsiniz.

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a>Mevcut Dataverse ortamı için çift yazmayı ayarlama

Varolan bir Dataverse ortam için çift yazma ayarlamak için bir Microsoft [destek bileti](../../lifecycle-services/lcs-support.md) oluşturmanız gerekir. Bilet şunları içermelidir:

+ Finance and Operations ortam kimliğiniz.
+ Lifecycle Services'den ortam adınız.
+ Power Platform Yönetim Merkezi'ndeki Dataverse kuruluş kimliği veya Power Platform Ortam Kimliği. Biletinizde, kimliğin Power Platform tümleştirme için kullanılan örnek olmasını isteyin.

> [!NOTE]
> Ortamların bağlantısını LCS kullanarak kaldıramazsınız. Bir ortamın bağlantısını kaldırmak için Finance and Operations ortamdaki **Veri tümleştirme** çalışma alanını açın ve sonra **Bağlantıyı kaldır**'ı seçin.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
