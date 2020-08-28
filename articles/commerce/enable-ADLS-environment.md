---
title: Dynamics 365 Commerce ortamında Azure Data Lake Storage'yi etkinleştirme
description: Bu konu, ürün önerilerinin etkinleştirilmesinin bir önkoşulu olan, Dynamics 365 Commerce ortamı için Azure Data Lake Storage'ın nasıl etkinleştirileceğini ve test edileceğini açıklamaktadır.
author: bebeale
manager: AnnBe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 27e4f1c751ee865b0df536f3c1912cb1d8946032
ms.sourcegitcommit: 8905d7a7a010e451c5435086480f66650ec54926
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2020
ms.locfileid: "3665014"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a>Dynamics 365 Commerce ortamında Azure Data Lake Storage'yi etkinleştirme

[!include [banner](includes/banner.md)]

Bu konu, ürün önerilerinin etkinleştirilmesinin bir önkoşulu olan, Dynamics 365 Commerce ortamı için Azure Data Lake Storage'ın nasıl etkinleştirileceğini ve test edileceğini açıklamaktadır.

## <a name="overview"></a>Genel Bakış

Dynamics 365 Commerce çözümünde, tüm ürün ve hareket bilgileri ortamın Varlık deposunda izlenir. Bu verileri (veri analizi, iş zekası ve kişiselleştirilmiş öneriler gibi) diğer Dynamics 365 hizmetlerinin erişimine açmak için, ortamı, müşteriye ait bir Azure Data Lake Storage Gen 2 çözümüne bağlamak gerekir.

Azure Data Lake Storage bir ortamda yapılandırılırken, gerekli tüm veriler korunmaya devam eden ve müşterinin denetiminde bulunan Varlık deposundan yansıtılır.

Ürün önerileri veya kişiselleştirilmiş öneriler de ortamda etkinleştirildiyse, müşteri verilerini almak ve bu verileri temel alan önerileri hesaplamak için, ürün önerileri yığınına Azure Data Lake Storage içindeki özel klasöre erişim hakkı verilir.

## <a name="prerequisites"></a>Önkoşullar

Müşterilerin, sahip oldukları bir Azure aboneliğinde Azure Data Lake Storage yapılandırmaları gerekir. Bu konu bir Azure aboneliği satın almayı veya Azure Data Lake Storage özelliği etkinleştirilmiş bir depolama hesabı kurulumunu kapsamaz.

Azure Data Lake Storage hakkında daha fazla bilgi için bkz. [Azure Data Lake Storage Gen2 resmi belgeler](https://azure.microsoft.com/pricing/details/storage/data-lake).
  
## <a name="configuration-steps"></a>Yapılandırma adımları

Bu bölüm, ürün önerileriyle ilgili bir ortamda Azure Data Lake Storage öğesini etkinleştirmek için gerekli olan yapılandırma adımlarını kapsamaktadır.
Azure Data Lake Storage'yi etkinleştirmek için gereken adımlara daha ayrıntılı bir genel bakış için bkz. [Veri deposununu Data Lake olarak kullanılabilir hale getirme](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).

### <a name="enable-azure-data-lake-storage-in-the-environment"></a>Ortamda Azure Data Lake Storage etkinleştirme

1. Ortamın arka ofis portalında oturum açın.
1. **Sistem Parametreleri**ni arayın ve **Veri bağlantıları** sekmesine gidin. 
1. **Data Lake tümleştirmesi** ayarını **Evet** yapın.
1. **Data Lake'i yavaş yavaş güncelleştir** ayarını **Evet** yapın.
1. Sonra aşağıdaki gerekli bilgileri girin:
    1. **Uygulama Kodu** // **Uygulama Parolası** // **DNS Adı** - Azure Data Lake Storage gizliliğinin saklandığı KeyVault bağlanmak için gereklidir.
    1. **Parola adı** - KeyVault'ta depolanan ve Azure Data Lake Storage ile kimlik doğrulamak için kullanılan parola adı.
1. Değişikliklerinizi sayfanın sol üst köşesinde kaydedin.

Aşağıdaki resimde örnek bir Azure Data Lake Storage yapılandırması gösterilmektedir.

![Azure Data Lake Storage yapılandırması örneği](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a>Azure Data Lake Storage bağlantısını test etme

1. KeyVault'a bağlantıyı **Azure Key Vault'u test et** bağlantısını kullanarak test edin.
1. Azure Data Lake Storage'ye bağlantıyı **Azure Depolamayı test et** bağlantısını kullanarak test edin.

> [!NOTE]
> Testler başarısız olursa, yukarıda eklenen tüm KeyVault bilgilerinin doğruluğunu iki kez kontrol edin ve sonra yeniden deneyin.

Bağlantı testleri başarıyla sonuçlandıktan sonra Varlık deposu için otomatik yenilemeyi etkinleştirmeniz gerekir.

Varlık deposu için otomatik yenilemeyi etkinleştirmek üzere bu adımları izleyin.

1. **Varlık Deposu**'nu arayın.
1. Soldaki listede **RetailSales** girişine gidin ve **Düzenle**'yi seçin.
1. **Otomatik Yenileme Etkin** ayarının **Evet** yapıldığından emin olun, **Yenile**'yi ve ardından **Kaydet**'i seçin.

Aşağıdaki resimde, otomatik yenilemenin etkinleştirildiği bir Varlık deposu örneği gösterilmektedir.

![Otomatik yenileme özelliği etkin olan Varlık deposu örneği](./media/exampleADLSConfig2.png)

Artık Azure Data Lake Storage ortam için yapılandırılmış durumdadır. 

Henüz tamamlanmadıysa, ortam için [ürün önerilerini ve kişiselleştirmeyi etkinleştirme](enable-product-recommendations.md) adımlarını izleyin.

## <a name="additional-resources"></a>Ek kaynaklar

[Varlık deposunu Data Lake olarak kullanılabilir hale getirme](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[Ürün önerilerine genel bakış](product-recommendations.md)

[Ürün önerilerini etkinleştir](enable-product-recommendations.md)

[Kişiselleştirilmiş önerileri etkinleştirme](personalized-recommendations.md)

[Kişiselleştirilmiş önerilerden vazgeçme](personalization-gdpr.md)

["Benzer görünümleri araştır" önerilerini etkinleştirme](shop-similar-looks.md)

[POS'ta ürün önerileri ekleme](product.md)

[Hareket ekranına öneriler ekleme](add-recommendations-control-pos-screen.md)

[AI-ML öneri sonuçlarını ayarlama](modify-product-recommendation-results.md)

[Seçkin önerileri el ile oluşturma](create-editorial-recommendation-lists.md)

[Demo verileriyle öneriler oluşturma](product-recommendations-demo-data.md)

[Ürün önerileri SSS](faq-recommendations.md)
