---
title: Deneme önizleme ve yayımlama
description: Bu konu, Dynamics 365 Commerce'tan denemeyi önizlemeyi ve yayımlamayı açıklamaktadır.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 91e2e4840a2d53f195d881279050b6415d48b070
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930309"
---
# <a name="preview-and-publish-an-experiment"></a>Deneme önizleme ve yayımlama

Bu konuda, [denemenizi bağlandıktan ve varyasyonlarınızı düzenledikten](experimentation-connect-edit.md) sonra denemenize Dynamics 365 Commerce'ta nasıl önizleme yapacağınız ve denemenizi nasıl yayımlayacağınız açıklanmaktadır. Aşağıdaki diyagramda, Dynamics 365 Commerce'taki bir e-Ticaret web sitesinde deneme ayarlama ve çalıştırmayla ilgili tüm adımlar gösterilmektedir. Ek adımlar ayrı konularda ele alınmıştır.

[ ![Deneme kullanıcı yolculuğu - Önizleme ve Yayımlama](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)

## <a name="preview-your-experiment-variations"></a>Deneme varyasyonlarınızı önizleme
Varyasyonlarınızın önizlemesini yapabilir ve istediğiniz gibi görününceye kadar bunları düzenlemeye devam edebilirsiniz.

1. Site oluşturucuda, önizlemek istediğiniz içeriği seçmek için komut çubuğunun altındaki varyasyonlar açılır menüsünü kullanın. 
1. Üst çubukta **Önizleme**'yi seçin. Yayımlandığında içeriğin nasıl görüneceğine ilişkin önizleme görüntülenir.
1. Farklı bir varyasyonun önizlemesini görmek için varyasyon açılır menüsünde bunu seçin ve tekrar **Önizleme**'yi seçin.

## <a name="publish-your-experiment"></a>Denemenizi yayımlama
Denemenizin ne zaman canlı olarak yayımlanacağını planlamak için yayımlama grubu kullanmıyorsanız ve hemen yayımlamak istiyorsanız, komut çubuğunda **Yayımla**'yı seçin. Denemeye ait tüm varyasyonlar yayımlanacaktır.
    
> [!IMPORTANT]
> Sayfada yayımdan kaldırılmış bir URL varsa, ilk olarak URL'yi yayımlamanız gerekir aksi durumda web sitesi kullanıcılarınıza gösterilmez. Ayrıntılar için bkz. [Sayfa kaydetme, önizleme ve yayımlama](save-preview-publish-page.md).
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a>Denemenizin ne zaman canlı yayımlanacağını planlamak için yayımlama grupları kullanma
Site oluşturucuda oluşturulan varyasyonlar, bir yayımlama grubu kullanılarak yayımlanmak üzere zamanlanabilir. Bir yayınlama grubu içinde, **Denemeler** sekmesine veya **Sayfalar** ya da **Parçalar** sekmesine giderek denemenize bir sayfa veya parça bağlayabilirsiniz. Daha fazla bilgi için, bkz. [Deneme bağlama ve varyasyonları düzenleme](experimentation-connect-edit.md) konusuna bakın. Yayımlama grupları hakkında daha fazla bilgi için bkz. [Yayımlama gruplarıyla çalışma](publish-groups.md).

Yayımlama gruplarını denemeler ile kullanırken, bilinmesi gereken bazı önemli noktalar vardır.
- Bir yayımlama grubuna, üzerinde çalışan deneme bulunan bir sayfa veya parça eklediğinizde, deneme yayınlama grubundaki sayfadan veya parçadan kaldırılır.
- Canlı sitedeki sayfalara bağlanan denemeler yayınlama grupları içindeki sayfalar tarafından kullanılamaz ve bunun tersi de geçerlidir. Benzer şekilde, canlı bir sitede üzerlerinde denemeler çalıştıran sayfalar, yayımlama gruplarındaki diğer denemelerde kullanılamaz ve tam tersi de geçerlidir.
- Bir yayımlama grubunu yayımladığınızda veya zamanladığınızda, yayınlama grubundaki tüm içerik yayımlama grubuyla ilişkilendirilmiş bir deneme olup olmadığına bakılmaksızın yayımlanır.
- Yayımlama grubu canlı bir siteye yayımlandıktan sonra devam ettiğinden, yayımlama grubundaki denemeler de devam eder. Bu nedenle, diğer denemeleri aynı sayfa veya parça ile ilişkilendiremezsiniz. Bu sınırlamayı önlemek için, kalıcı denemeler içeren tüm yayımlama gruplarını silin. Benzer şekilde, aynı zamanda bir yayımlama grubunda da bulunan canlı bir sitedeki denemeyi silmek isterseniz, denemeyi önce yaymnlama grubundan silin.

## <a name="previous-step"></a>Önceki adım
[Deneme bağlama ve düzenleme](experimentation-connect-edit.md)

## <a name="next-step"></a>Sonraki adım
[Deneme çalıştırma ve izleme](experimentation-run-monitor.md)
