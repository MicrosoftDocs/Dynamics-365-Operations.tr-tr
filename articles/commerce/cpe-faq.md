---
title: Ticaret önizleme ortamı SSS
description: Bu konu, Microsoft Dynamics 365 Commerce önizleme ortamı istemcisi hakkında sık sorulan soruların yanıtlarını verilmektedir.
author: v-chgri
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 53e593931850d6b8b22bb756d5828f742416aa4d
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906105"
---
# <a name="commerce-preview-environment-faq"></a>Ticaret önizleme ortamı SSS

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce önizleme ortamı istemcisi hakkında sık sorulan soruların yanıtlarını verilmektedir.

**Ticari önizleme ortamı için daveti başka bir kiracıya aktarabilir miyim?**

Evet. Davet aktarımları için, [Commerce Önizleme aktarım formunu](https://aka.ms/Dynamics365CommercePreviewTransferForm) kullanabilirsiniz.

**Davetiye aktarımının ne kadar sürer?**

Aktarım, yaklaşık üç-beş iş günü ortalamasını alır. Ancak, özel durumlar geçerli olabilir.

**Commerce önizleme ortamı Dynamics 365 Finance ile veya Dynamics 365 tedarik zinciri projeleriyle çalışıyor mu?**

Hayır. Commerce önizleme ortamı yalnızca Dynamics 365 Retail projelerle çalışır.

**Commerce önizleme ortamını, şu anda perakende satılan müşteriler için bir e-ticaret mağazası olarak kullanabilir mi?**

Hayır. Ticari önizleme ortamı yalnızca değerlendirme ortamıdır. Perakende satış teknolojisini kullanan bir müşteri için ortam gerekiyorsa Microsoft 'a başvurun.

**Perakende önizleme ortamı, perakendeciyi uygulayan varolan bir uygulamanın/ortamın en üstünde e-ticaret özelliklerinin sağlanması için kullanılabilir mi?**

Hayır. Ticari önizleme ortamı şu anda yalnızca 10.0.6 sürümünde tanıtım verileri bulunan perakende stok tutma birimi (SKU) projelerinde dağıtılan yeni ortamlarda kullanılabilir.

**Microsoft Dynamics Lifecycle Services (LCS) yoluyla Microsoft Azure üzerine Commerce önizleme ortamını dağıtmaya hangi maliyetler dahil edilecek?**

Perakende, aboneliğinizde bulunan tek bileşendir. Retail Cloud Scale Unit (Rcsu) ve e-ticaret gibi diğer bileşenler Microsoft abonelikleri içinde barınacaktır. Bu maliyeti tahmin etmek için [Azure fiyatlandırma hesap makinesini](https://azure.microsoft.com/pricing/calculator/) kullanabilirsiniz.

**Şu anda Commerce önizleme ortamında hangi Azure coğrafyaları destekleniyor?**

Commerce önizleme ortamı yalnızca Kuzey Amerika Coğrafyasında dağıtılabilir.

**Tam OneBox sanal makinesi (VM) seçeneği olan bir indirilebilir sanal sabit disk (VHD) var mı?**

Dynamics 365 Retail Cloud Scale Unit (RCSU) ve e-ticaret, tamamen hizmet olarak yazılımdır (SaaS) ve bulutta barındırılan bulut olmalıdır.

**Ticari önizleme ortamı ne kadar süreyle kullanılabilir?**

Commerce önizleme ortamının, e-ticaret sağlama tarihinden itibaren 30 günlük zaman sınırlaması vardır.

**Commerce önizleme ortamım için zaman sınırını genişletebilirim?**

Evet. [Commerce önizleme genişletme formunu](https://aka.ms/Dynamics365CommercePreviewExtensionForm) kullanarak destek ekibine başvurabilirsiniz.

**Bir Commerce önizleme ortamı için çoklu istekler yapabilir mi?**

Kabul edilen her istek için bir Commerce önizleme ortamının kotası veriyoruz. Birden fazla önizleme ortamına gereksinim duyarsanız, Microsoft'a başvurun. İletişim bilgileri için sonraki bölüme bakın.

## <a name="dynamics-365-commerce-preview-environment-contact-information"></a>Dynamics 365 Commerce önizleme ortamı iletişim bilgileri

Commerce önizleme ortamıyla ilgili sorularınız veya istekleriniz varsa, Microsoft'a başvurmak için yardım almak üzere [Microsoft Dynamics 365 Commerce Önizleme Yammer grubunu](https://aka.ms/Dynamics365CommercePreviewYammer) ziyaret edin.

Yammer Gruba erişmeye çalıştığınızda sorunlarla karşılaşırsanız, Microsoft'a e-posta ile başvurabilirsiniz:  <Dynamics365Commerce@microsoft.com>. Bu e-posta adresi etkin şekilde izlenmiyor. Bu nedenle, yanıtta bir gecikme olmasını bekler.

## <a name="additional-resources"></a>Ek kaynaklar

[Ticaret önizleme ortamına genel bakış](cpe-overview.md)

[Ticaret önizleme ortamı sağlama](provisioning-guide.md)

[Ticaret önizleme ortamı yapılandırma](cpe-post-provisioning.md)

[Bir Commerce Preview ortamı için isteğe bağlı özellikleri konfigüre edin](cpe-optional-features.md)
