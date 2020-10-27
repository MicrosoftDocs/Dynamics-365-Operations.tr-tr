---
title: Varyasyon yükseltme ve deneme tamamlama
description: Bu konu, Dynamics 365 Commerce'ta başarılı bir varyasyonun nasıl yükseltileceğini ve denemenin nasıl tamamlanacağını açıklar.
author: sushma-rao
manager: AnnBe
ms.date: 09/15/2020
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
ms.openlocfilehash: 2e011f10e908d6a2efe2e928fc5e0abc7659cb8b
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930304"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a>Varyasyon yükseltme ve deneme tamamlama

Bu konu, denemede en iyi sonuçları üreten değişimin nasıl yükseltileceğini ve denemenin nasıl tamamlanacağını açıklamaktadır. Aşağıdaki diyagramda, Dynamics 365 Commerce'taki bir e-Ticaret web sitesinde deneme ayarlama ve çalıştırmayla ilgili tüm adımlar gösterilmektedir. Ek adımlar ayrı konularda ele alınmıştır.

[ ![Deneme kullanıcı yolculuğu - İnceleme ve Tamamlama](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)

[Denemenizi çalıştırdıktan](experimentation-run-monitor.md) ve canlı sitenizde hangi varyasyonu kullanmak istediğinizi belirlemek için yeterli veri topladıktan sonra varyasyonu yükseltip denemeyi sonlandırırsınız.

## <a name="promote-a-variation"></a>Varyasyon yükseltme
Hangi varyasyonun en iyi sonuçları ürettiğine karar vermek için, üçüncü taraf hizmetteki denemeyle ilgili verileri ve analizleri kullanın. Web sitenizin tüm kullanıcıları tarafından kullanılabilmesi için canlı sitedeki geçerli içeriği kazanan varyasyonla değiştirmek için aşağıdakileri yapın. 

1. Site oluşturucuda **Denemeler** sekmesine gidin ve denemeyi seçin.
1. Üst çubukta **Denemeyi tamamla**'yı seçin.
1. **Denemeyi tamamla** iletişim kutusu menüsünde, **Deneme verilerini gözden geçir**'i seçin. Ölçümleri doğrulayabileceğiniz ve hangi varyasyonun en iyi performansı gösterdiğini belirleyebileceğiniz üçüncü taraf hizmeti açılır.
1. Site oluşturucudaki **Denemeyi tamamla** iletişim kutusu menüsünde kazanan varyasyonu ve ardından **İleri**'yi seçin.
1. Üçüncü taraf hizmetini açın ve denemeyi durdurun.
1. Site oluşturucuda, orijinal canlı sayfanın üzerine yazmak ve web sitenizin tüm kullanıcılarına sunulması için kazanan varyasyonu yayımlamak üzere **Tamamla**'yı seçin. 

> [!NOTE]
> Geçerli canlı sayfayı saklamayı ve bir varyasyon yayımlamamayı tercih ederseniz, **Özgün sayfayı yeniden yayımla**'yı seçin.

## <a name="delete-your-experiment"></a>Denemenizi silme
Commerce'ta tamamlanmış bir denemeyi silmeniz gerekli olmasa da alan kazanmak veya çalışma alanınızı temizlemek için denemeyi silmeyi tercih edebilirsiniz. Bir denemeyi silmek için aşağıdakileri yapın.

1. Site oluşturucuda **Denemeler** sekmesine gidin ve denemeyi seçin. 
    > [!NOTE]
    > Deneme hala etkinse, devam etmeden önce üçüncü taraf hizmetinde denemeyi durdurun.
1. Varyasyon içeriğini canlı siteden kaldırmak için komut çubuğunda **Yayımdan Kaldır**'ı seçin.
1. Denemeyi silmek için komut çubuğunda **Sil**'i seçin.

## <a name="previous-step"></a>Önceki adım
[Deneme çalıştırma ve izleme](experimentation-run-monitor.md)
