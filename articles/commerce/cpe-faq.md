---
title: Dynamics 365 Commerce değerlendirme ortamıyla ilgili SSS
description: Bu konu, Microsoft Dynamics 365 Commerce değerlendirme ortamı istemcisi hakkında sık sorulan soruların yanıtlarını verilmektedir.
author: v-chgri
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e8a3e760353b351d42aff82c0d372d2aca350cd2
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343570"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a>Dynamics 365 Commerce değerlendirme ortamıyla ilgili SSS

[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce değerlendirme ortamı istemcisi hakkında sık sorulan soruların yanıtlarını verilmektedir.

## <a name="can-we-use-the-commerce-evaluation-environment-as-an-e-commerce-storefront-for-customers-that-currently-implement-retail"></a>Commerce değerlendirme ortamı, şu anda Retail uygulayan müşteriler için bir e-Ticaret mağazası olarak kullanabilir mi?

No Commerce değerlendirme ortamı yalnızca değerlendirme içindir. Perakende satış teknolojisini kullanan bir müşteri için ortam gerekiyorsa Microsoft 'a başvurun.

## <a name="can-the-commerce-evaluation-environment-be-used-to-provision-the-e-commerce-features-on-top-of-an-existing-applicationenvironment-that-implements-retail"></a>Commerce değerlendirme ortamı, Retail uygulayan mevcut bir uygulamanın/ortamın üstünde e-Ticaret özelliklerinin sağlanması için kullanılabilir mi?

Hayır (çoğunlukla). Commerce değerlendirme bileşenleri, yalnızca önkoşullar ve sağlama kılavuzunda belirtilen yapılandırmalarla eşleşen ortamlar için geçerlidir. Ek olarak, gerekli temel demo verileri 10.0.8 öncesindeki ilk sürümle dağıtılan ortamlarda kullanılamaz. 

## <a name="what-costs-are-involved-in-deploying-the-commerce-evaluation-environment-on-microsoft-azure-via-microsoft-dynamics-lifecycle-services-lcs"></a>Microsoft Dynamics Lifecycle Services (LCS) yoluyla Microsoft Azure üzerine Commerce değerlendirme ortamını dağıtmaya hangi maliyetler dahildir?

Geleneksel Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce genel merkezi demo ortamı (sanal makine \[VM\]) Azure aboneliğinizde barındırılacaktır. Bu maliyeti tahmin etmek için [Azure fiyatlandırma hesap makinesini](https://azure.microsoft.com/pricing/calculator/) kullanabilirsiniz.

Commerce Scale Unit, Commerce Site Oluşturucu ve e-Ticaret siteniz gibi diğer bileşenler, hizmet olarak yazılım olarak kullanılacak ve Microsoft tarafından barındırılacaktır.

## <a name="which-azure-geographies-are-currently-supported-for-the-commerce-evaluation-environment"></a>Şu anda Commerce değerlendirme ortamında hangi Azure coğrafyaları destekleniyor?

Commerce değerlendirme ortamı yalnızca Kuzey Amerika Coğrafyasında dağıtılabilir.

## <a name="is-there-a-downloadable-virtual-hard-disk-vhd-that-has-the-complete-onebox-virtual-machine-vm-option"></a>Tam OneBox sanal makinesi (VM) seçeneği olan bir indirilebilir sanal sabit disk (VHD) var mı?

Dynamics 365 Commerce ve Commerce Scale Unit tamamen hizmet olarak yazılımdır (SaaS) ve bulutta barındırılmalıdır.

## <a name="how-long-can-the-commerce-evaluation-environment-be-used"></a>Commerce değerlendirme ortamı ne kadar süreyle kullanılabilir?

Commerce değerlendirme ortamının Commerce Scale Unit, Commerce site oluşturucu ve e-Ticaret gibi SaaS bileşenlerinin sağlandığı tarihten itibaren 30 günlük zaman sınırı vardır.

## <a name="can-i-extend-the-time-limit-for-my-commerce-evaluation-environment"></a>Commerce değerlendirme ortamım için zaman sınırını genişletebilirim?

Zaman sınırı genişletme norm için bir istisnadır ve duruma göre değerlendirilir. Yardım için Microsoft iş ortağınıza başvurmanız gerekir.

## <a name="additional-resources"></a>Ek kaynaklar

[Dynamics 365 Commerce değerlendirme ortamına genel bakış](cpe-overview.md)

[Dynamics 365 Commerce değerlendirme ortamı sağlama](provisioning-guide.md)

[Dynamics 365 Commerce değerlendirme ortamı yapılandırma](cpe-post-provisioning.md)

[Dynamics 365 Commerce değerlendirme ortamında BOPIS yapılandırma](cpe-bopis.md)

[Dynamics 365 Commerce değerlendirme ortamı için isteğe bağlı özellikleri yapılandırma](cpe-optional-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
