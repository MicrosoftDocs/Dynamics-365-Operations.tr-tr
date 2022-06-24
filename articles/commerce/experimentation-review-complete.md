---
title: Varyasyon yükseltme ve deneme tamamlama
description: Bu makale, Dynamics 365 Commerce'ta başarılı bir varyasyonun nasıl yükseltileceğini ve denemenin nasıl tamamlanacağını açıklar.
author: sushma-rao
ms.date: 06/07/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 3e9a978551622bbb14d9213f607d9dfabe42672a
ms.sourcegitcommit: ddcb62bb5fbf26a1178c2bb1aec45a3d2362339e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/07/2022
ms.locfileid: "8942755"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a>Varyasyon yükseltme ve deneme tamamlama

Bu makale, denemede en iyi sonuçları üreten değişimin nasıl yükseltileceğini ve denemenin nasıl tamamlanacağını açıklamaktadır. Aşağıdaki diyagramda, Dynamics 365 Commerce'taki bir e-Ticaret web sitesinde deneme ayarlama ve çalıştırmayla ilgili tüm adımlar gösterilmektedir. Ek adımlar ayrı makalelerde ele alınmıştır.

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

Commerce site oluşturucuda tamamlanan bir denemeyi silmek için aşağıdaki adımları izleyin.

1. Sol gezinti bölmesinde **Denemeler**'i seçin ve ardından denemeyi seçin. 
    > [!NOTE]
    > Deneme hala etkinse, devam etmeden önce üçüncü taraf hizmetinde denemeyi durdurun.
1. Varyasyon içeriğini canlı siteden kaldırmak için komut çubuğunda **Yayımdan Kaldır**'ı seçin.
1. Denemeyi silmek için **Sil**'i seçin.

## <a name="previous-step"></a>Önceki adım
[Deneme çalıştırma ve izleme](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
