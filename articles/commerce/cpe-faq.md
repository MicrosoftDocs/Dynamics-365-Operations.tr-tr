---
title: Dynamics 365 Commerce değerlendirme ortamıyla ilgili SSS
description: Bu konu, Microsoft Dynamics 365 Commerce değerlendirme ortamı istemcisi hakkında sık sorulan soruların yanıtlarını verilmektedir.
author: v-chgri
manager: annbe
ms.date: 07/16/2020
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
ms.openlocfilehash: 637714e28b9f8f4aa66e251e709d8f78bff2739d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416324"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a>Dynamics 365 Commerce değerlendirme ortamıyla ilgili SSS

[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce değerlendirme ortamı istemcisi hakkında sık sorulan soruların yanıtlarını verilmektedir.

**Commerce değerlendirme ortamı, şu anda Retail uygulayan müşteriler için bir e-Ticaret mağazası olarak kullanabilir mi?**

No Commerce değerlendirme ortamı yalnızca değerlendirme içindir. Perakende satış teknolojisini kullanan bir müşteri için ortam gerekiyorsa Microsoft 'a başvurun.

**Commerce değerlendirme ortamı, Retail uygulayan mevcut bir uygulamanın/ortamın üstünde e-Ticaret özelliklerinin sağlanması için kullanılabilir mi?**

Hayır (çoğunlukla). Commerce değerlendirme bileşenleri, yalnızca önkoşullar ve sağlama kılavuzunda belirtilen yapılandırmalarla eşleşen ortamlar için geçerlidir. Ek olarak, gerekli temel demo verileri 10.0.8 öncesindeki ilk sürümle dağıtılan ortamlarda kullanılamaz. 

**Microsoft Dynamics Lifecycle Services (LCS) yoluyla Microsoft Azure üzerine Commerce değerlendirme ortamını dağıtmaya hangi maliyetler dahil edilecek?**

Geleneksel Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce genel merkezi demo ortamı (sanal makine \[VM\]) Azure aboneliğinizde barındırılacaktır. Bu maliyeti tahmin etmek için [Azure fiyatlandırma hesap makinesini](https://azure.microsoft.com/pricing/calculator/) kullanabilirsiniz.

Commerce Scale Unit, Commerce Site Oluşturucu ve e-Ticaret siteniz gibi diğer bileşenler, hizmet olarak yazılım olarak kullanılacak ve Microsoft tarafından barındırılacaktır.

**Şu anda Commerce değerlendirme ortamında hangi Azure coğrafyaları destekleniyor?**

Commerce değerlendirme ortamı yalnızca Kuzey Amerika Coğrafyasında dağıtılabilir.

**Tam OneBox sanal makinesi (VM) seçeneği olan bir indirilebilir sanal sabit disk (VHD) var mı?**

Dynamics 365 Commerce ve Commerce Scale Unit tamamen hizmet olarak yazılımdır (SaaS) ve bulutta barındırılmalıdır.

**Commerce değerlendirme ortamı ne kadar süreyle kullanılabilir?**

Commerce değerlendirme ortamının Commerce Scale Unit, Commerce site oluşturucu ve e-Ticaret gibi SaaS bileşenlerinin sağlandığı tarihten itibaren 30 günlük zaman sınırı vardır.

**Commerce değerlendirme ortamım için zaman sınırını genişletebilirim?**

Zaman sınırı genişletme norm için bir istisnadır ve duruma göre değerlendirilir. Yardım için Microsoft iş ortağınıza başvurmanız gerekir.

## <a name="additional-resources"></a>Ek kaynaklar

[Dynamics 365 Commerce değerlendirme ortamına genel bakış](cpe-overview.md)

[Dynamics 365 Commerce değerlendirme ortamı sağlama](provisioning-guide.md)

[Dynamics 365 Commerce değerlendirme ortamı yapılandırma](cpe-post-provisioning.md)

[Dynamics 365 Commerce değerlendirme ortamında BOPIS yapılandırma](cpe-bopis.md)

[Dynamics 365 Commerce değerlendirme ortamı için isteğe bağlı özellikleri yapılandırma](cpe-optional-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]