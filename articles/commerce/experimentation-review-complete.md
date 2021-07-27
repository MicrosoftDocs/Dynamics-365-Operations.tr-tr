---
title: Varyasyon yükseltme ve deneme tamamlama
description: Bu konu, Dynamics 365 Commerce'ta başarılı bir varyasyonun nasıl yükseltileceğini ve denemenin nasıl tamamlanacağını açıklar.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 2d098f323d58bf3233a83655b213afe131ae3f36
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349292"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a>Varyasyon yükseltme ve deneme tamamlama

Bu konu, denemede en iyi sonuçları üreten değişimin nasıl yükseltileceğini ve denemenin nasıl tamamlanacağını açıklamaktadır. Aşağıdaki diyagramda, Dynamics 365 Commerce'taki bir e-Ticaret web sitesinde deneme ayarlama ve çalıştırmayla ilgili tüm adımlar gösterilmektedir. Ek adımlar ayrı konularda ele alınmıştır.

[ ![Deneme kullanıcı yolculuğu - İnceleme ve Tamamlama.](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)

[Denemenizi çalıştırdıktan](experimentation-run-monitor.md) ve canlı sitenizde hangi varyasyonu kullanmak istediğinizi belirlemek için yeterli veri topladıktan sonra varyasyonu yükseltip denemeyi sonlandırırsınız.

## <a name="promote-a-variation"></a>Varyasyon yükseltme
Hangi varyasyonun en iyi sonuçları ürettiğine karar vermek için, üçüncü taraf hizmetteki denemeyle ilgili verileri ve analizleri kullanın. Ardından web sitenizin tüm kullanıcıları tarafından kullanılabilmesi için canlı sitedeki geçerli içeriği, kazanan varyasyonla değiştirerek yükseltebilirsiniz.

Kazanan varyasyonu yükseltmek için, aşağıdaki adımları izleyin. 

1. Commerce site oluşturucuda, sol gezinti bölmesinde **Denemeler**'i seçin ve ardından denemeyi seçin.
1. Komut çubuğunda **Denemeyi tamamla**'yı seçin.
1. **Denemeyi tamamla** iletişim kutusunda **Deneme verilerini gözden geçir**'i seçin. Ölçümleri doğrulayabileceğiniz ve hangi varyasyonun en iyi performansı gösterdiğini belirleyebileceğiniz üçüncü taraf hizmeti açılır.
1. **Denemeyi tamamla** iletişim kutusunda kazanan varyasyonu ve ardından **İleri**'yi seçin.
1. Üçüncü taraf hizmetini açın ve denemeyi durdurun.
1. Site oluşturucuda, orijinal canlı sayfanın üzerine yazmak ve web sitenizin tüm kullanıcılarına sunulması için kazanan varyasyonu yayımlamak üzere **Tamamla**'yı seçin. 

> [!NOTE]
> Geçerli canlı sayfayı saklamayı ve bir varyasyon yayımlamamayı tercih ederseniz, **Özgün sayfayı yeniden yayımla**'yı seçin.

## <a name="delete-your-experiment"></a>Denemenizi silme
Commerce'ta tamamlanmış bir denemeyi silmeniz gerekli olmasa da alan kazanmak veya çalışma alanınızı temizlemek için denemeyi silmeyi tercih edebilirsiniz. 

Commerce site oluşturucuda deneme silmek için aşağıdaki adımları izleyin.

1. Sol gezinti bölmesinde **Denemeler**'i seçin ve ardından denemeyi seçin. 
    > [!NOTE]
    > Deneme hala etkinse, devam etmeden önce üçüncü taraf hizmetinde denemeyi durdurun.
1. Varyasyon içeriğini canlı siteden kaldırmak için komut çubuğunda **Yayımdan Kaldır**'ı seçin.
1. Denemeyi silmek için **Sil**'i seçin.

## <a name="previous-step"></a>Önceki adım
[Deneme çalıştırma ve izleme](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]