---
title: Deneme önizleme ve yayımlama
description: Bu makale, Dynamics 365 Commerce'tan denemeyi önizlemeyi ve yayımlamayı açıklamaktadır.
author: sushma-rao
ms.date: 06/08/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 5da7a4e3c17057278d02ebd45702d1de404f0dc6
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946154"
---
# <a name="preview-and-publish-an-experiment"></a>Deneme önizleme ve yayımlama

Bu makalede, [denemenizi bağlandıktan ve varyasyonlarınızı düzenledikten](experimentation-connect-edit.md) sonra denemenize Dynamics 365 Commerce'ta nasıl önizleme yapacağınız ve denemenizi nasıl yayımlayacağınız açıklanmaktadır. Aşağıdaki diyagramda, Dynamics 365 Commerce'taki bir e-Ticaret web sitesinde deneme ayarlama ve çalıştırmayla ilgili tüm adımlar gösterilmektedir. Ek adımlar ayrı makalelerde ele alınmıştır.

[ ![Deneme kullanıcı yolculuğu - Önizleme ve Yayımlama.](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)

## <a name="preview-your-experiment-variations"></a>Deneme varyasyonlarınızı önizleme
Varyasyonlarınızın önizlemesini yapabilir ve istediğiniz gibi görününceye kadar bunları düzenlemeye devam edebilirsiniz.

Commerce site oluşturucuda deneme varyasyonlarınızı önizlemek için aşağıdaki adımları izleyin.

1. Önizlemek istediğiniz içeriği seçmek için komut çubuğunun altındaki varyasyonlar açılır menüsünü kullanın. 
1. Komut çubuğunda, **Önizleme** öğesini seçin. Yayımlandığında içeriğin nasıl görüneceğine ilişkin önizleme görüntülenir.
1. Farklı bir varyasyonun önizlemesini görmek için varyasyon açılır menüsünde bunu seçin ve tekrar **Önizleme**'yi seçin.

## <a name="publish-your-experiment"></a>Denemenizi yayımlama
Denemenizin ne zaman canlı olarak yayımlanacağını planlamak için yayımlama grubu kullanmıyorsanız ve hemen yayımlamak istiyorsanız, komut çubuğunda **Yayımla**'yı seçin. Denemeye ait tüm varyasyonlar yayımlanacaktır.
    
> [!IMPORTANT]
> Sayfada yayımdan kaldırılmış bir URL varsa, ilk olarak URL'yi yayımlamanız gerekir aksi durumda web sitesi kullanıcılarınıza gösterilmez. Ayrıntılar için bkz. [Sayfa kaydetme, önizleme ve yayımlama](save-preview-publish-page.md).
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a>Denemenizin ne zaman canlı yayımlanacağını planlamak için yayımlama grupları kullanma
Site oluşturucuda oluşturulan varyasyonlar, bir yayımlama grubu kullanılarak yayımlanmak üzere zamanlanabilir. Bir yayınlama grubunda, soldaki gezinti bölmesinde **Denemeler**'i seçerek bir sayfa veya parçayı denemenize bağlayabilirsiniz. Bunu, **sayfalar** veya **parçaları** seçerek ve [bir denemeyi bağlama ve varyasyonları düzenleme](experimentation-connect-edit.md) bölümündeki yönergeleri izleyerek de yapabilirsiniz. Yayımlama grupları hakkında daha fazla bilgi için bkz. [Yayımlama gruplarıyla çalışma](publish-groups.md).

Yayımlama gruplarını denemeler ile kullanırken, bilinmesi gereken bazı önemli noktalar vardır.
- Bir yayımlama grubuna, üzerinde çalışan deneme bulunan bir sayfa veya parça eklediğinizde, deneme yayınlama grubundaki sayfadan veya parçadan kaldırılır.
- Canlı sitedeki sayfalara bağlanan denemeler yayınlama grupları içindeki sayfalar tarafından kullanılamaz ve bunun tersi de geçerlidir. Benzer şekilde, canlı bir sitede üzerlerinde denemeler çalıştıran sayfalar, yayımlama gruplarındaki diğer denemelerde kullanılamaz ve tam tersi de geçerlidir.
- Bir yayımlama grubunu yayımladığınızda veya zamanladığınızda, yayınlama grubundaki tüm içerik yayımlama grubuyla ilişkilendirilmiş bir deneme olup olmadığına bakılmaksızın yayımlanır.
- Yayımlama grubu canlı bir siteye yayımlandıktan sonra devam ettiğinden, yayımlama grubundaki denemeler de devam eder. Bu nedenle, diğer denemeleri aynı sayfa veya parça ile ilişkilendiremezsiniz. Bu sınırlamayı önlemek için, kalıcı denemeler içeren tüm yayımlama gruplarını silin. Benzer şekilde, aynı zamanda bir yayımlama grubunda da bulunan canlı bir sitedeki denemeyi silmek isterseniz, denemeyi önce yaymnlama grubundan silin.

### <a name="force-variations-for-testing"></a>Test için varyasyonları zorlama

Deneme kullanıma alındığında, test veya otomasyon amaçlarıyla varyasyonu zorlamak için deneme kimliğini ve varyasyon kimliğini varsayılan sayfa URL'sine ekleyebilirsiniz. Örneğin, varsayılan sayfa URL'si `https://fabrikam.com/modern/homepage` ise `https://fabrikam.com/modern/homepage?exp=18012910471|18024360464` gibi bir URL ile varyasyonu zorlayabilirsiniz. Deneme varyasyonunuz için yukarıda açıklanan **Önizleme** deneyimindeki önizleme URL'sinden deneme kimliği ve varyasyon kimliğini edinebilirsiniz.

## <a name="previous-step"></a>Önceki adım
[Deneme bağlama ve düzenleme](experimentation-connect-edit.md)

## <a name="next-step"></a>Sonraki adım
[Deneme çalıştırma ve izleme](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
