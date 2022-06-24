---
title: Bir deneme için varsayım tanımlama ve ölçümleri belirleme
description: Bu makalede, Dynamics 365 Commerce uygulamasında bir e-ticaret web sitesinde çalıştıracağınız denemeler için varsayım ve başarı ölçümlerinin nasıl belirleneceği açıklanır.
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
ms.openlocfilehash: 0b6bdf160522fc93e841ec2f8a4542ff80d8f67f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852798"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a>Varsayım tanımlama ve deneme için başarı ölçümleri belirleme
Deneme yaşam döngüsünün ilk aşaması, deneme için varsayım tanımlamayı ve başarıyı değerlendirmek için izlenecek ölçümleri belirlemeyi içerir. Aşağıdaki diyagramda, Dynamics 365 Commerce'taki bir e-Ticaret web sitesinde [deneme ayarlama ve çalıştırmayla](experimentation-overview.md) ilgili tüm adımlar gösterilmektedir. Ek adımlar ayrı makalelerde ele alınmıştır. 

[ ![Deneme kullanıcı yolculuğu - Tanımlama.](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)

Varsayım, denemin sonucunu tahmin ettiğiniz bir ifadedir. Varsayım tanımlaya rol alan birçok etken vardır: örneğin kullanıcı davranışı araştırması ve topladığınız web sitesi verileri. Varsayımla, deneminiz ile doğrulamak istediğiniz varsayımı veya teoriyi tanımlarsınız. Denemeniz için bir varsayım örneği şu olabilir: "*giriş sayfamdaki beyaz bir tişört resmi, yaz aylarında lacivert bir kazaktan daha yüksek tıklama oranı oluşturur çünkü insanlar yazın hafif ve açık renkli kıyafetler giymek ister*" Bu durumda, beyaz tişört ve lacivert kazak içeren varyasyonlar oluşturur ve her ikisini aynı anda yayımlarsınız.

Bir varsayımını doğrulamak için, denemenin başarısı veya başarısızlığı doğrudan kullanıcı eylemlerine bağlı olmalıdır; örneğin, web sitesi kullanıcısının bir bağlantıya veya düğmeye tıklaması gibi. Bu eylemlerin, denemeyi izleyen üçüncü taraf hizmetine bildirilecek olaylara karşılık gelmesi gerekir. Zaman içinde, eylem gerçekleştiren kullanıcıların yüzdesi raporlar oluşturmak ve çözümlemeler yapmak için kullanabileceğiniz bir ölçüm olarak hesaplanacaktır. Kullanılabilir tüm olayları ve öznitelikleri incelemek için [Tanılama ve sorun giderme için Commerce bileşeni olayları](dev-itpro/retail-component-events-diagnostics-troubleshooting.md) konusuna bakın.

## <a name="previous-step"></a>Önceki adım
[Dynamics 365 Commerce'ta deneme](experimentation-overview.md)


## <a name="next-step"></a>Sonraki adım
[Deneme ayarlama](experimentation-setup.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]