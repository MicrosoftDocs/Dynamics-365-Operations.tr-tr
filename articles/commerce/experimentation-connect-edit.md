---
title: Deneme bağlama ve varyasyonları düzenleme
description: Bu konuda, üçüncü taraf bir hizmetteki bir denemebib Dynamics 365 Commerce'a nasıl bağlanacağı ve denemeler için varyasyonların nasıl düzenleneceği açıklanmaktadır.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
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
ms.openlocfilehash: 030640ba8907ae52c198ac96ad2c243b533d8c53
ms.sourcegitcommit: 7592c2dec0428d56843ab395d2a52c89f77f99b5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096979"
---
# <a name="connect-an-experiment-and-edit-variations"></a>Deneme bağlama ve varyasyonları düzenleme

Bu konu, Commerce'taki denemenizi nasıl bağlayacağınızı ve varyasyonlarınızda varsayımınızla uygun olmaları için nasıl düzenleme yapacağınız açıklamaktadır. 

Aşağıdaki diyagramda, Dynamics 365 Commerce'taki bir e-Ticaret web sitesinde deneme ayarlama ve çalıştırmayla ilgili tüm adımlar gösterilmektedir. Ek adımlar ayrı konularda ele alınmıştır.

[ ![Deneme kullanıcı yolculuğu - Bağla ve Düzenle](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)

Üçüncü taraf bir hizmette [denemenizi ayarladıktan sonra](experimentation-setup.md), denemeyi Dynamics 365 Commerce'ta bağlayıp deneme varyasyonlarını düzenleyebilirsiniz.

## <a name="planning-considerations"></a>Planlama değerlendirmeleri

Denemenizi Commerce'ta bağlamadan önce Commerce'ın içeriğinizi yönetme biçimini etkileyen bazı kararlar almanız gerekir.

### <a name="determine-the-scope-of-your-experiment"></a>Denemenin kapsamını belirleyin
Bir denemeyi bağladığınızda, denemenizin kapsamını tanımlamanız istenir. Denemeler **kısmi** kapsam veya **tam** kapsam olarak tanımlanır.
- Sayfanın belirli bir bölümünde denemeler yapmak istiyorsanız **kısmi** seçeneğini belirleyin. Bu seçeneği seçerseniz, deneme içine hangi modüllerin dahil edileceğini tanımlamanız gerekir. Varsayılan sayfa veya parçanın, deneme ile ilgili olmayan kısımlarında yapılan değişiklikler otomatik olarak varyasyonlar arasında eşitlenir.
- Tüm sayfa veya parça üzerinde denemeler yapmak istiyorsanız, **tüm** seçeneğini belirleyin. Varsayılan sayfa veya parçanın ayrı kopyaları oluşturulur. Tüm düzenleme yüzeyinin değiştirilebilir olması nedeniyle, denemeye dahil edilecek modülleri seçmeniz gerekmez. Gerektiğinde modülleri ekleyebilir, silebilir veya yeniden sıralayabilirsiniz. Ancak, denemenin ilişkili olduğu varsayılan sayfa veya parça üzerinde herhangi bir değişiklik yapılırsa, bu değişikliklerin tüm varyasyonlarda el ile eşitlenmesi gerekir.

<!-- not to editors, we're adding an image here to illustrate the difference. it will help.) -->

> [!NOTE]
> Denemenizi düzen kullanan bir sayfayla ilişkilendirirseniz, yalnızca **tüm** deneme kapsamını tanımlayabilirsiniz.

### <a name="decide-if-you-want-to-schedule-when-your-experiment-is-published"></a>Denemenizin ne zaman yayımlanacağını planlamak isteyip istemediğinize karar verin
Denemenizin canlı sitenizde ne zaman yayımlanacağını planlamak istiyorsanız, deneme ile ilişkilendirmek istediğiniz içeriğin denemeyi bağlamadan *önce* bir yayımlama grubunda kullanılabilir olduğundan emin olun. 

Yayımlama grupları hakkında daha fazla bilgi için [Yayımlama gruplarıyla çalışma](publish-groups.md) konusuna bakın.


## <a name="connect-your-experiment"></a>Denemenizi bağlama
Denemenizi bağlamak için **Deneme bağlama** sihirbazını başlatın. Sihirbaz, denemenizi bağlamak için gerekli olan adımlarda size yol gösterecektir. Sihirbazı tamamladığınızda, denemeniz bağlanır ve varyasyonlar oluşturulup düzenlenmeye hazır hale gelir.

Commerce site oluşturucuda denemenizi bağlamaya başlamak için aşağıdaki adımları izleyin.

1. **Denemeyi bağlama** sihirbazını başlatmak için, sol gezinti bölmesinde **Denemeler** 'i seçin ve sonra **Bağlan** 'ı seçin. Alternatif olarak, sihirbaza bir sayfa veya parça düzenleyicisinden de erişebilirsiniz. Bunun için sihirbazı düzenleyin ve komut çubuğunda **Denemeyi bağla** 'yı seçin.

    > [!NOTE]
    > Bir sayfa, bir seferde yalnızca bir denemeye bağlanabilir. Bir sayfayı farklı bir denemeye bağlamak için, önce sayfanın bağlı olduğu denemeyi silin.

1. Denemenizi çalıştırmak istediğiniz sayfayı veya parçayı seçin.
1. Yukarıdaki [Denemenizin kapsamını belirleme](#determine-the-scope-of-your-experiment) bölümünde yaptığınız seçimi temel alarak deneme kapsamını **kısmi** veya **tüm** olarak ayarlayın.
    > [!NOTE]
    > Tam sayfa veya parça üzerinde denemeler yapmak istiyorsanız, **Sayfalar veya parçalar üzerinde deneme** özelliği bayrağının etkinleştirilmesi gerekir. Daha fazla bilgi için [Dynamics 365 Commerce'ta deneme](experimentation-overview.md) konusuna bakın.
    
1. Sihirbazın son adımında, **Varyasyonlar oluştur ve sihirbazdan çık** 'ı seçin. Denemeler için varyasyonlar oluşturulur. 

## <a name="edit-your-variations"></a>Varyasyonlarınızı düzenleme
Sihirbazdan çıktığınızda, varyasyonlar sizin için oluşturulur. 

Daha sonra, varyasyonları deneme varsayımında doğrulamanız gereken seçimleri yansıtacak şekilde düzenlersiniz. Yukarıdaki [Denemenizin kapsamını belirleme](#determine-the-scope-of-your-experiment) bölümünde denemeniz için seçtiğiniz kapsama karşılık gelen aşağıdaki yordamlardan birini seçin.

### <a name="edit-variations-for-experiments-with-partial-scope"></a>Kısmi kapsamlı denemeler için varyasyonları düzenleme
**Denemeyi bağla** sihirbazında denemenizin kapsamını **kısmi** olarak tanımladıysanızşu adımları izleyin.

1. Düzenleyici görünümünde, her varyasyonu özgün varsayıma göre düzenlemek için komut çubuğunun altındaki varyasyonlar açılan menüsünü kullanın. Varyasyonlardan birini değiştirilmemiş şekilde bırakarak bir denetim veya temel varyasyon da oluşturmak isteyebilirsiniz.
1. Denemede kullanılacak modülü seçin, üç noktayı (...) seçin ve sonra **Denemeye ekle** 'yi seçin.

### <a name="edit-variations-for-experiments-with-entire-scope"></a>Tam kapsamlı denemeler için varyasyonları düzenleme
Deneme kapsamını **Denemeyi bağla** sihirbazında **tam** olarak tanımladıysanız, düzenleyici görünümündeyken, özgün varsayımınıza göre her bir varyasyonu düzenlemek için, komut çubuğunun altındaki varyasyonlar açılan menüsünü kullanın. 

> [!NOTE]
> Her iki durumda da, varyasyonlardan birini değiştirilmemiş şekilde bırakarak bir denetim veya temel varyasyon da oluşturmak isteyebilirsiniz.

## <a name="previous-step"></a>Önceki adım
[Deneme ayarlama](experimentation-setup.md) 


## <a name="next-step"></a>Sonraki adım
[Deneme önizleme ve yayımlama](experimentation-preview-publish.md)
