---
title: Global Stok Muhasebesi için Power BI'yı etkinleştirme
description: Bu konuda, Global Stok Muhasebesi için Microsoft Power BI'yı nasıl etkinleştirebileceğiniz açıklanmaktadır.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8be486409d60cc4927599816e30e1e4ab21a312a
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669796"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a>Global Stok Muhasebesi için Power BI'yı etkinleştirme

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 4/30/2022 -->

[PowerBI.com](https://powerbi.com/) hesabınızdaki kutucukları, panoları ve raporları Microsoft Dynamics 365 uygulaması çalışma alanınıza sabitleyebilirsiniz.

## <a name="prerequisites"></a>Önkoşullar

Power BI raporlamasını etkinleştirmeden önce aşağıdaki önkoşulların karşılanması gerekir:

- Dynamics 365 uygulamasında sistem yöneticisi olmanız gerekir.
- [PowerBI.com](https://powerbi.com/) hesabınız olması gerekir.
- Power BI hesabınızda en az bir pano ve bir rapor olmalıdır.
- Azure Active Directory (Azure AD) hesabınız için yönetici olmanız gerekir.
- Azure AD etki alanının, [PowerBI.com](https://powerbi.com/) hesabınız için kullandığınız etki alanıyla aynı olması gerekir.

## <a name="setup"></a>Ayar

Power BI tümleştirmesini ayarlamak için aşağıdaki adımları izleyin.

1. [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index)'de oturum açın.
1. **Paylaşılan varlık kitaplığı**'na gidin, varlık türü olarak **Power BI rapor modeli**'ni seçin ve **Global Stok Muhasebesi** paketini indirin. 
1. [PowerBI.com](https://app.powerbi.com/)'a giriş yapın ve aşağıdaki adımları izleyerek **Global Stok Muhasebesi** Power BI rapor dosyasını yükleyin:

    1. **Yeni**'yi seçin.
    1. **Dosya yükle**'yi seçin.
    1. **Global Stok Muhasebesi** Power BI raporu dosyasını seçin.

1. Aşağıdaki adımları izleyerek **Global Stok Muhasebesi** Power BI raporunu yapılandırın:

    1. **Çalışma alanım**'a gidin, Global Stok Muhasebesi veri kümesini bulun ve **Seçenekler** menüsünde **Ayarlar**'ı seçin.
    1. **Global stok muhasebesi ayarları**'nda **Parametreler**'i genişletin ve tüm parametreleri gerektiği gibi güncelleştirin. Özellikle, aşağıdaki ayarları kontrol edin:
        1. LCS içindeki **Power platform ortam bilgileri** sayfasında bulunan değerleri kullanarak varsayılan **Dataverse URL'nin** ve ortam kimliği değerlerinin üzerine yazın (**Power platform tümleştirme** bölümünde).
        1. LCS içindeki **Ortam ayrıntıları** sayfasında bulunan değerleri kullanarak varsayılan **Ortam Kimliğinin** ve ortam kimliği değerlerinin üzerine yazın (**Ortamı yönet** bölümünde).
        1. **Veri kaynağı kimlik bilgileri** bölümündeki **CDS** etiketinin yanında **Kimlik bilgilerini düzenle** bağlantısını seçin. Daha sonra **OAuth2** kimlik doğrulama yöntemini kullanarak Dataverse hesabınızda oturum açın.
    1. **Çalışma alanım \> Raporlar \> Global Stok Muhasebesi**'ndeki Power BI raporlarının şimdi düzgün çalışıyor olduğunu doğrulayın ve içeriği sisteminizden görüntüleyin.

1. Uygulamayı, [PowerBI.com tümleştirmesini yapılandırma](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process) bölümünde açıklandığı gibi kaydedin.
1. Aşağıdaki adımları izleyerek **Global Stok Muhasebesi** Power BI raporu dosyasını Dynamics 365 Supply Chain Management ile tümleştirin:

    1. **Sistem yönetimi \> Kurulum \> PowerBI.com yapılandırması** seçeneğine gidin.
    1. **Düzenle** öğesini seçin.
    1. **PowerBI.Com tümleştirmesini etkinleştir**'i seçin.
    1. **Uygulama kodu** alanına uygulama kodunu girin.
    1. **Uygulama anahtarı** alanına uygulama anahtarını girin.
    1. **Kaydet**'i seçin.

1. Power BI oturum açma iletişim kutusunun görünmesi için sayfayı yenileyin.
1. **Seçenekler** sekmesinde **Rapor kataloğunu aç**'ı seçin ve ardından daha önce yüklediğiniz **Global Stok Muhasebesi** Power BI rapor dosyasını seçin.
1. Sayfayı yenileyin. Raporunuzun eklendiğini görmeniz gerekir.
1. **Power BI raporları** altında **Global Stok Muhasebesi** bağlantısını seçin.

Daha fazla bilgi için bkz. [PowerBI.com tümleştirmesini yapılandırma](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).
