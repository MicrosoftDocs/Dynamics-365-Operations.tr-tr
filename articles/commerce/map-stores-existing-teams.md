---
title: Microsoft Teams'de önceden var olan ekipler varsa mağazaları ve ekipleri eşleme
description: Bu makale, kuruluşunuz Commerce tümleştirmesinden önce Microsoft Teams'de oluşturulan ekiplere sahipse Dynamics 365 Commerce Headquarters'da mağazaların ve ilgili ekiplerin nasıl eşlendiğini açıklar.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 67a1a79dd74d411aa7e21000c8baaa8a069cede7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279132"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a>Microsoft Teams'de önceden var olan ekipler varsa mağazaları ve ekipleri eşleme

[!include [banner](includes/banner.md)]

Bu makale, kuruluşunuz Commerce tümleştirmesinden önce Microsoft Teams'de oluşturulan ekiplere sahipse Dynamics 365 Commerce Headquarters'da mağazaların ve ilgili ekiplerin nasıl eşlendiğini açıklar.

Kuruluşunuz Dynamics 365 Commerce ve Microsoft Teams'i tümleştirmeden önce mağazalarınızın bir kısmı veya tümü için oluşturulmuş ekiplere sahip olabilir. Bu durumda, Commerce POS ve Microsoft Teams arasında görev eşitlemesi oluşturmak için mağazaların ve ilgili ekibin Commerce Headquarters'da eşlemesini sağlamanız gerekir.

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a>Commerce Headquarters'da mağazaları ve ilgili ekipleri eşleme 

Commerce Headquarters'da mağazaları ve ilgili ekipleri eşlemek için aşağıdaki adımları uygulayın.

1. **Sistem Yönetimi \> Çalışma alanı \> Veri yönetimi** seçeneğine gidin.
1. **Dışa Aktar**'ı seçin. 
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Grup adı** altında "Teams eşlemesini dışa aktarma"'yı girin.
1. **Seçili varlıklar** hızlı sekmesinde **Varlık ekle**'yi seçin. **Varlık Ekle** iletişim kutusu görünür.  
1. **Varlık adı** açılan listesinde, **kaynak ve ekip arasında Teams eşlemesi**'ni seçin.
1. **Hedef veri biçimi** açılan listesinde **CSV**'yi seçin.
1. **Ekle**'yi ve ardından **Kapat**'ı seçin.
1. Eylem bölmesinin sol üstünde, **Şimdi dışa aktar**'ı seçin.
1. **Varlık işleme durumu** altında, **dosyayı indir**'i seçin.
1. Dışa aktarılan CSV dosyasında, **SOURCETYPE**, **SourceId** ve **TEAMID** değerlerini aşağıdaki gibi girin:
    - **SOURCETYPE** için "RetailStore" girin. 
    - **SOURCEID** olarak, mağaza numarasını girin (örneğin, San Francisco mağazası için "000135"). Mağaza numaralarını **Retail ve Commerce \> kanallar \> Mağazalar**'da bulabilirsiniz.
    - **TEAMID** için, Microsoft Teams'den ilgili ekip kodunu (örneğin, "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c") girin. Ekip kodu bilgilerini [admin.teams.microsoft.com](https://admin.teams.microsoft.com) adresinden bulabilirsiniz.
1. CSV dosyasını yerel makinenize kaydedin.
1. **Sistem Yönetimi \> Çalışma alanı \> Veri yönetimi** seçeneğine gidin ve **İçe Aktar**'ı seçin.
1. **Seçili varlıklar** hızlı sekmesinde **Dosya ekle**'yi seçin. **Dosya Ekle** iletişim kutusu görünür.
1. **Varlık adı** açılan listesinde, **kaynak ve ekip arasında Teams eşlemesi**'ni seçin.
1. **Kaynak veri biçimi** açılan listesinde **CSV**'yi seçin.
1. **Yükle ve Ekle**'yi seçin, daha önce kaydetmiş olduğunuz CSV dosyasını seçin ve **aç**'ı seçin.
1. **Dosya Ekle** iletişim kutusunda **Kapat**'ı seçin.
1. Eylem Bölmesinde, **Kaydet**'i ve sonra **İçe Aktar**'ı seçin.

Aşağıdaki örnek görüntü, Commerce'te **varlık ekle** öğeleri ve dışa aktarılan CSV dosyası üstbilgilerinin vurgulandığı **Ekip eşlemesini dışa aktar** grubunu gösterir.

![Commerce'te varlık ekle öğeleri ve dışa aktarılan CSV dosyası üst bilgilerinin vurgulandığı takımlar eşlemesi grubunu dışa aktarma.](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> Önceki adımları tamamladıktan sonra, görev yönetimini eşlemek için [Microsoft Teams ve POS arasında görev eşleme](synchronize-tasks-teams-pos.md) adımlarını izleyin. 

## <a name="additional-resources"></a>Ek kaynaklar

[Dynamics 365 Commerce ve Microsoft Teams tümleştirmesine genel bakış](commerce-teams-integration.md)

[Dynamics 365 Commerce ve Microsoft Teams tümleştirmesini etkinleştirme](enable-teams-integration.md)

[Dynamics 365 Commerce'ten Microsoft Teams sağlama](provision-teams-from-commerce.md)

[Microsoft Teams ve Dynamics 365 Commerce POS arasında görev yönetimini eşitleme](synchronize-tasks-teams-pos.md)

[Microsoft Teams'de kullanıcı rollerini yönetme](manage-user-roles-teams.md)

[Dynamics 365 Commerce ve Microsoft Teams tümleştirmesi SSS](teams-integration-faq.md)
