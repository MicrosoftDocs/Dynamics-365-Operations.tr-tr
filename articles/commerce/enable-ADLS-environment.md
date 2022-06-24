---
title: Dynamics 365 Commerce ortamında Azure Data Lake Storage'ı etkinleştirme
description: Bu makalede, bir Azure Data Lake Storage Gen2 çözümünün bir Dynamics 365 Commerce ortamının Varlık deposuna nasıl bağlanacağına ilişkin yönergeler sağlanmaktadır. Bu, ürün önerilerini etkinleştirmeden önce gerekli bir adımdır.
author: bebeale
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6e0c84dd6b173a111b70a8adb6036be946149f7c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885183"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a>Dynamics 365 Commerce ortamında Azure Data Lake Storage'ı etkinleştirme

[!include [banner](includes/banner.md)]

Bu makalede, bir Azure Data Lake Storage Gen2 çözümünün bir Dynamics 365 Commerce ortamının Varlık deposuna nasıl bağlanacağına ilişkin yönergeler sağlanmaktadır. Bu, ürün önerilerini etkinleştirmeden önce gerekli bir adımdır.

Dynamics 365 Commerce çözümünde önerileri, ürünleri ve hareketleri hesaplamak için gerekli veriler ortamın Varlık deposunda toplanır. Veri analizi, iş zekası ve kişiselleştirilmiş öneriler gibi bu verileri diğer Dynamics 365 hizmetlerinin erişimine açmak için ortamı müşteriye ait bir Azure Data Lake Storage Gen2 çözümüne bağlamak gerekir.

Yukarıdaki adımlar tamamlandıktan sonra, ortamın Varlık deposundaki tüm müşteri verileri otomatik olarak müşterinin Azure Data Lake Storage Gen 2 çözümüne yansıtılır. Öneriler özellikleri Commerce genel merkezinde Özellik yönetimi çalışma alanı aracılığıyla etkinleştirildiğinde, öneriler yığınına aynı Azure Data Lake Storage Gen2 çözümüne erişim izni sağlanır.

Tüm işlem boyunca müşterilerin verileri korunmaya devam eder ve denetimleri altında kalır.

## <a name="prerequisites"></a>Önkoşullar

Dynamics 365 Commerce ortamının Varlık deposu, bir Azure Data Lake Gen Storage Gen2 hesabına ve sağlayan hizmetlere bağlı olmalıdır.

Azure Data Lake Storage Gen2'nin nasıl ayarlanacağı hakkında daha fazla bilgi için bkz. [Azure Data Lake Storage Gen2 resmi belgeleri](https://azure.microsoft.com/pricing/details/storage/data-lake).
  
## <a name="configuration-steps"></a>Yapılandırma adımları

Bu bölüm, ürün önerileriyle ilgili bir ortamda Azure Data Lake Storage Gen2'yi etkinleştirmek için gerekli olan yapılandırma adımlarını kapsamaktadır.
Azure Data Lake Storage Gen2'yi etkinleştirmek için gereken adımlara ilişkin daha ayrıntılı bir genel bakış için bkz. [Varlık deposunu Data Lake olarak kullanılabilir yapma](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).

### <a name="enable-azure-data-lake-storage-in-the-environment"></a>Ortamda Azure Data Lake Storage etkinleştirme

1. Ortamın arka ofis portalında oturum açın.
1. **Sistem Parametreleri** ni arayın ve **Veri bağlantıları** sekmesine gidin. 
1. **Data Lake tümleştirmesi** ayarını **Evet** yapın.
1. Sonra aşağıdaki gerekli bilgileri girin:
    1. **Uygulama Kodu** // **Uygulama Parolası** // **DNS Adı** - Azure Data Lake Storage gizliliğinin saklandığı KeyVault bağlanmak için gereklidir.
    1. **Parola adı** - KeyVault'ta depolanan ve Azure Data Lake Storage ile kimlik doğrulamak için kullanılan parola adı.
1. Değişikliklerinizi sayfanın sol üst köşesinde kaydedin.

Aşağıdaki resimde örnek bir Azure Data Lake Storage yapılandırması gösterilmektedir.

![Azure Data Lake Storage yapılandırması örneği.](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a>Azure Data Lake Storage bağlantısını test etme

1. KeyVault'a bağlantıyı **Azure Key Vault'u test et** bağlantısını kullanarak test edin.
1. Azure Data Lake Storage'ye bağlantıyı **Azure Depolamayı test et** bağlantısını kullanarak test edin.

> [!NOTE]
> Yukarıdaki testlerden herhangi biri başarısız olursa yukarıda eklenen tüm KeyVault bilgilerinin doğru olduğunu onaylayın ve ardından yeniden deneyin.

Bağlantı testleri başarıyla sonuçlandıktan sonra Varlık deposu için otomatik yenilemeyi etkinleştirmeniz gerekir.

Varlık deposu için otomatik yenilemeyi etkinleştirmek üzere bu adımları izleyin.

1. **Varlık Deposu**'nu arayın.
1. Soldaki listede **RetailSales** girişine gidin ve **Düzenle**'yi seçin.
1. **Otomatik Yenileme Etkin** ayarının **Evet** yapıldığından emin olun, **Yenile**'yi ve ardından **Kaydet**'i seçin.

Aşağıdaki resimde, otomatik yenilemenin etkinleştirildiği bir Varlık deposu örneği gösterilmektedir.

![Otomatik yenileme özelliği etkin olan Varlık deposu örneği.](./media/exampleADLSConfig2.png)

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
