---
title: Deneme bağlama ve varyasyonları düzenleme
description: Bu makalede, üçüncü taraf bir hizmetteki bir denemebib Dynamics 365 Commerce'a nasıl bağlanacağı ve denemeler için varyasyonların nasıl düzenleneceği açıklanmaktadır.
author: sushma-rao
ms.date: 06/07/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: dcdbd61976402ddd719ece184a86692fbc7c628d
ms.sourcegitcommit: ddcb62bb5fbf26a1178c2bb1aec45a3d2362339e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/07/2022
ms.locfileid: "8942834"
---
# <a name="connect-an-experiment-and-edit-variations"></a>Deneme bağlama ve varyasyonları düzenleme

Bu makale, Commerce'taki denemenizi nasıl bağlayacağınızı ve varyasyonlarınızda varsayımınızla uygun olmaları için nasıl düzenleme yapacağınız açıklamaktadır. 

Aşağıdaki diyagramda, Dynamics 365 Commerce'taki bir e-Ticaret web sitesinde deneme ayarlama ve çalıştırmayla ilgili tüm adımlar gösterilmektedir. Ek adımlar ayrı makalelerde ele alınmıştır.

[ ![Deneme kullanıcı yolculuğu - Bağla ve Düzenle.](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)

Üçüncü taraf bir hizmette [denemenizi ayarladıktan sonra](experimentation-setup.md), denemeyi Dynamics 365 Commerce'ta bağlayıp deneme varyasyonlarını düzenleyebilirsiniz.

## <a name="connect-your-experiment"></a>Denemenizi bağlama
Denemenizi bağlamak için **Deneme bağlama** sihirbazını başlatın. Sihirbaz, denemenizi bağlamak için gerekli olan adımlarda size yol gösterecektir. Sihirbazı tamamladığınızda, denemeniz bağlanır ve varyasyonlar oluşturulup düzenlenmeye hazır hale gelir.

Commerce site oluşturucuda denemenizi bağlamaya başlamak için aşağıdaki adımları izleyin.

1. **Denemeyi bağlama** sihirbazını başlatmak için, sol gezinti bölmesinde **Denemeler**'i seçin ve sonra **Bağlan**'ı seçin. Alternatif olarak, sihirbaza bir sayfa veya parça düzenleyicisinden de erişebilirsiniz. Bunun için sihirbazı düzenleyin ve komut çubuğunda **Denemeyi bağla**'yı seçin.

    > [!NOTE]
    > - Bir sayfa, bir seferde yalnızca bir denemeye bağlanabilir. Bir sayfayı farklı bir denemeye bağlamak için, önce sayfanın bağlı olduğu denemeyi silin.
    > - Yalnızca özel bir düzen kullanılan sayfalarda deneme yapabilirsiniz. Sayfanızda önceden ayarlanmış bir düzen varsa önce bunu özel düzene dönüştürün. Bu işlemi sayfaya gidip komut çubuğundan **Özel düzene dönüştür**'ü seçerek yapabilirsiniz. Düzenler hakkında daha fazla bilgi için bkz. [Önceden ayaralanmış ve özel düzenler](templates-layouts-overview.md#preset-and-custom-layouts). 

1. Bir denemeye sol gezinti bölmesindeki **Denemeler** sekmesinden bağlanıyorsanız açılan listeden deneme adını seçin.
1. Denemenizi çalıştırmak istediğiniz sayfayı veya parçayı seçin.
1. Sihirbazın son adımında, **Varyasyonlar oluştur ve sihirbazdan çık**'ı seçin. Denemeler için varyasyonlar oluşturulur. 

> [!NOTE]
> Denemenizin canlı sitenizde ne zaman yayımlanacağını planlamak istiyorsanız, deneme ile ilişkilendirmek istediğiniz içeriğin denemeyi bağlamadan *önce* bir yayımlama grubunda kullanılabilir olduğundan emin olun. Yayımlama grupları hakkında daha fazla bilgi için [Yayımlama gruplarıyla çalışma](publish-groups.md) konusuna bakın.

## <a name="edit-your-variations"></a>Varyasyonlarınızı düzenleme

**Denemeye bağlanın** sihirbazından çıktığınızda , sizin için varyasyonlar oluşturulur. Varyasyonları deneme varsayımında doğrulamanız gereken seçimleri yansıtacak şekilde düzenlemek için aşağıdaki adımları izleyin.

1. Düzenleyici görünümünde, her varyasyonu özgün varsayıma göre düzenlemek için komut çubuğunun altındaki varyasyonlar açılan menüsünü kullanın. Varyasyonlardan birini değiştirilmemiş şekilde bırakarak bir denetim veya temel varyasyon da oluşturmak isteyebilirsiniz.
1. Denemede kullanılacak modülü seçin, üç noktayı (...) seçin ve sonra **Denemeye ekle**'yi seçin.

> [!NOTE]
> Varyasyonlardan birini değiştirilmemiş şekilde bırakarak bir denetim veya temel varyasyon da oluşturabilirsiniz.

## <a name="previous-step"></a>Önceki adım
[Deneme ayarlama](experimentation-setup.md) 


## <a name="next-step"></a>Sonraki adım
[Deneme önizleme ve yayımlama](experimentation-preview-publish.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
