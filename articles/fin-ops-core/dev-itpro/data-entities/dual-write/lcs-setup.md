---
title: Lifecycle Services'dan çift yazma kurulumu
description: Bu konuda, Microsoft Dynamics Lifecycle Services (LCS) portalından nasıl çift yazma bağlantısı ayarlayacağınız açıklanmaktadır.
author: laneswenka
ms.date: 08/03/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 825d6a4b3462077d0f4b3f4275792ea0fe5152df
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8063684"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Lifecycle Services'dan çift yazma kurulumu

[!include [banner](../../includes/banner.md)]



Bu konuda, Microsoft Dynamics Lifecycle Services (LCS) portalından nasıl çift yazma bağlantısı ayarlayacağınız açıklanmaktadır.

## <a name="prerequisites"></a>Önkoşullar

Power Platform tümleştirmeyi aşağıdaki konularda açıklandığı gibi tamamlamanız gerekir:

+ [Power Platform Tümleştirme - Ortam dağıtımı sırasında etkinleştir](../../power-platform/enable-power-platform-integration.md#enable-during-deploy)
+ [Power Platform tümleştirmesi - Ortam dağıtımı sonrasında etkinleştir](../../power-platform/enable-power-platform-integration.md#enable-after-deploy)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a>Yeni Dataverse ortamları için çift yazmayı ayarlama

LCS **Ortam Ayrıntıları** sayfasından çift yazma ayarlamak için şu adımları izleyin:

1. **Ortam Ayrıntıları** sayfasında **Power Platform Tümleştirme** bölümünü genişletin.

2. **Çift yazma uygulaması** düğmesini seçin.

    ![Power Platform tümleştirmesi.](media/powerplat_integration_step2.png)

3. Hüküm ve koşulları inceleyin ve ardından **Yapılandır**'ı seçin.

4. Devam etmek için **Tamam**'ı seçin.

5. Ortam ayrıntıları sayfasını düzenli aralıklarla yenileyerek ilerleme durumunu izleyebilirsiniz. Kurulum genellikle 30 dakika veya daha az sürer.  

6. Kurulum tamamlandığında, işlemin başarılı olup olmadığını veya bir hata olup olmadığını bildiren bir ileti bildirir. Kurulum başarısız olursa, ilgili bir hata iletisi görüntülenir. Sonraki adıma geçmeden önce hataları düzeltmeniz gerekir.

7. Geçerli ortamın veritabanları ile Dataverse arasında bağlantı oluşturmak için **Power Platform Ortama bağla**'yı seçin. Bu genellikle 5 dakikadan daha az sürer.

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Power Platform ortamı bağlantısı.":::

8. Bağlama tamamlandığında, bir köprü görüntülenir. Finans ve Operasyon ortamındaki çift yazma yönetim alanına giriş yapmak için bağlantıyı kullanın. Buradan varlık eşlemeleri ayarlayabilirsiniz.

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a>Mevcut Dataverse ortamı için çift yazmayı ayarlama

Varolan bir Dataverse ortam için çift yazma ayarlamak için bir Microsoft [destek bileti](../../lifecycle-services/lcs-support.md) oluşturmanız gerekir. Bilet şunları içermelidir:

+ Finans ve Operasyon ortamınızın kimliği.
+ Lifecycle Services'den ortam adınız.
+ Power Platform Yönetim Merkezi'ndeki Dataverse kuruluş kimliği veya Power Platform Ortam Kimliği. Biletinizde, kimliğin Power Platform tümleştirme için kullanılan örnek olmasını isteyin.

> [!NOTE]
> Ortamların bağlantısını LCS kullanarak kaldıramazsınız. Bir ortamın bağlantısını kaldırmak için Finans ve Operasyon ortamındaki **Veri tümleştirme** çalışma alanını açın ve sonra **Bağlantıyı kaldır**'ı seçin.

## <a name="linking-mismatch"></a>Bağlama uyuşmazlığı

Çift yazma ortamınız bir Dataverse kurulumuna bağlanırken LCS ortamınızın başka bir Dataverse kurulumuna bağlanması mümkündür. Bu bağlama uyuşmazlığı, beklenmeyen davranışa neden olabilir ve verilerin yanlış ortama gönderilmesiyle sonuçlanabilir. Çift yazma için kullanılacak önerilen ortam, Power Platform tümleştirmesinin parçası olarak oluşturulan ortamdır ve uzun vadeli olarak bu, ortamlar arasında bağlantı oluşturmanın tek yolu olacaktır.

Ortamınızda bağlama uyuşmazlığı varsa LCS'de ortam ayrıntıları sayfanızda "Microsoft, ortamınızın Çift yazma aracılığıyla Power Platform Tümleştirmesi'nde belirtilenden farklı bir hedefe bağlandığını algıladı; bu önerilen bir durum değildir" gibi bir uyarı görüntülenir:

:::image type="content" source="media/powerplat_integration_mismatchLink.png" alt-text="Power Platform tümleştirme bağlantısı eşleşmiyor.":::

Bu hatayla karşılaşırsanız gereksinimlerinize göre iki seçenek vardır:

+ LCS ortam ayrıntıları sayfanızda belirtildiği üzere [Çift yazma ortamlarının bağlantısını kaldırın ve yeniden bağlayın (Bağlantıyı sıfırlayın veya değiştirin)](relink-environments.md#scenario-reset-or-change-linking). Microsoft desteği olmadan çalıştırabileceğinizden bu ideal bir seçenektir.  
+ Bağlantınızı çift yazmada tutmak isterseniz önceki bölümde belgelendiği gibi mevcut Dataverse ortamınızı kullanmak için Power Platform tümleştirmesini değiştirmek üzere Microsoft Desteği'nden yardım isteyebilirsiniz.  

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
