---
title: ER yapılandırmalarının güncellenmiş sürümlerini içeri aktarma
description: Bu makalede, Yapılandırma hizmeti Genel deposundan Elektronik raporlama (ER) yapılandırmalarının güncel sürümlerinin nasıl içe aktarılacağı açıklanmaktadır.
author: kfend
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
ms.openlocfilehash: 0eef9c9a112fd58a43f6c3a85163ccf44bea3d61
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292661"
---
# <a name="import-updated-versions-of-er-configurations"></a>ER konfigürasyonlarının güncelleştirilmiş sürümlerini içe aktar

[!include [banner](../includes/banner.md)]

Elektronik raporlama (ER) [depoları](general-electronic-reporting.md#Repository), [ER konfigürasyonları](general-electronic-reporting.md#Configuration) paylaşmak için kullanılır. Farklı depolardaki ER yapılandırmalarını Microsoft Dynamics 365 Finance örneğiniz için [içeri aktarabilirsiniz](download-electronic-reporting-configuration-lcs.md). ER yapılandırmalarını içe aktardığınızda, [yapılandırma sağlayıcıları](general-electronic-reporting.md#Provider) paylaşılabilecek şekilde yeni sürüm depoları yayımlayabilir.

Bu makalede, Yapılandırma hizmeti Genel deposundan ER yapılandırmalarının güncel sürümlerinin nasıl içe aktarılacağı açıklanmaktadır. Daha fazla bilgi için bkz. [Microsoft Dynamics 365 Finance - Regulatory Services, Yapılandırma hizmeti](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).

## <a name="review-the-available-updated-versions"></a>Kullanılabilir güncelleştirilmiş sürümleri gözden geçirin

1. Aşağıdaki rollerden birini kullanarak Finance'de oturum açın:

    - Elektronik raporlama geliştirici
    - Elektronik raporlama işlev danışmanı
    - Sistem yöneticisi

2. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
3. **Yerelleştirme yapılandırmaları** sayfasında **İlgili bağlantılar** bölümünde **Yapılandırma sürümleri güncellemelerini içe aktarma** kutucuğunu seçin.

    ![Yerelleştirme yapılandırmaları sayfası.](./media/er-download-updated-versions-global-repo1.png)

4. **Elektronik raporlama konfigürasyonları sürümleri güncelleştirmelerini içe aktar** iletişim kutusunda, **çalıştırma modu** alanında **yalnızca kullanılabilir güncelleştirmeleri göster**'i seçin. Daha sonra **Tamam**'ı seçin. 

    ![Çalışma modu alanı yalnızca kullanılabilir güncelleştirmeleri gösterecek şekilde ayarlandı.](./media/er-download-updated-versions-global-repo2.png)

5. Aldığınız iletileri gözden geçirin. Bu iletiler, geçerli Finance örneğindeki ER konfigürasyonlarla ilgili aşağıdaki bilgileri ve bunların genel havuz içeriğiyle nasıl karşılaştırılacağını sağlar:

    - ER konfigürasyonların toplam sayısı
    - Genel havuzda bulunmayan yapılandırmalar
    - Geçerli finans örneğinde en son sürümün zaten kullanılabildiği yapılandırmalar (Bu konfigürasyonların tam listesini görüntülemek Için **Mesaj ayrıntıları** bağlantısını seçin.)

        !["Aşağıdaki yapılandırmaların en son sürümleri zaten alındı" ileti ve ileti ayrıntıları](./media/er-download-updated-versions-global-repo3.png)

    - Genel depoda kullanılabilir ve geçerli Finans örneğine en son sürümün zaten kullanılabildiği yapılandırmalar (Bu konfigürasyonların tam listesini görüntülemek Için **Mesaj ayrıntıları** bağlantısını seçin.)

        !["Kullanılabilir güncelleştirmeler" iletisi ve ileti ayrıntıları](./media/er-download-updated-versions-global-repo4.png)

## <a name="import-available-updated-versions"></a>Kullanılabilir güncelleştirilmiş sürümleri içe aktarın

1. Aşağıdaki rollerden birini kullanarak Finance'de oturum açın:

    - Elektronik raporlama geliştirici
    - Elektronik raporlama işlev danışmanı
    - Sistem yöneticisi

2. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
3. **Yerelleştirme yapılandırmaları** sayfasında **İlgili bağlantılar** bölümünde **Yapılandırma sürümleri güncellemelerini içe aktarma** kutucuğunu seçin.
4. **Elektronik raporlama konfigürasyonları sürümleri güncelleştirmelerini içe aktar** iletişim kutusunda, **çalıştırma modu** alanında, Global depodan geçerli finans örneğine ER konfigürasyonların en son sürümlerini içe aktarmak için, **en son güncelleştirmeleri içe aktar**'ı seçin.
5. İçe aktarma için bir toplu iş planlamak üzere, **Arka planda çalıştır** hızlı sekmesinde, **Toplu işleme** seçeneğini **Evet** olarak ayarlayın. İçe aktarmayı belirli aralıklarla tekrarlamak istiyorsanız, gerekli yinelemeyi konfigüre edin.

    ![En son güncelleştirmeleri Içe aktarmak için çalışma modu alanı ayarla.](./media/er-download-updated-versions-global-repo5.png)

6. **Tamam**'ı seçin.
7. Hangi konfigürasyon sürümlerinin içe aktarıldığını öğrenmek için aşağıdaki adımlardan birini izleyin:

    - Toplu işi kullanmak yerine, içe aktarmayı etkileşimli olarak çalıştırırsanız, aldığınız iletileri gözden geçirin.

        ![Etkileşimli içe aktarma çalıştırması sırasında alınan iletiler.](./media/er-download-updated-versions-global-repo6.png)

    - İçe aktarmayı toplu iş modunda çalıştırırsanız, şu adımları izleyin:

        1. **Ortak** \> **Sorgular** \> **Toplu işler** \> **Toplu işlerim**'e gidin.
        2. **Elektronik raporlama konfigürasyonları güncelleştirmeleri güncelleştirmelerini içe aktar** işini bulun ve seçin ve sonra eylem bölmesinde, **toplu iş** sekmesinde, iş geçmişini görüntülemek için **toplu iş geçmişi**'ni seçin.
        3. **Toplu iş geçmişi** sayfasında, **Günlük**'ü seçin. Sonra, aldığınız iletide, iş günlüğünü görüntülemek için **Mesaj ayrıntıları** bağlantısını seçin.

        ![İş günlükleri.](./media/er-download-updated-versions-global-repo7.png)

> [!IMPORTANT]
> İçe aktarılan versiyonlar hemen kullanılabilir olacağından, ER konfigürasyonlarının güncelleştirilmiş sürümlerini doğrudan Global depodan üretim ortamına içe aktarmak için bir yinelenen toplu iş zamanlamanızı önermiyoruz. Bunun yerine, ER konfigürasyonlarının sürümlerini bir korumalı alan ortamına dağıtmak için bu yaklaşımı kullanın. Bunlar, daha sonra üretim ortamına dağıtılmadan önce korumalı alan ortamında değerlendirilebilirler.

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md)
- [Yapılandırma hizmeti genel deposundan ER yapılandırmalarını indir](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
