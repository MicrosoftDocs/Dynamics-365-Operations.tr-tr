---
title: NF-e özel sertifika doğrulaması
description: Bu konu, NF-e özel sertifikasını etkinleştirme ve kullanma hakkında bilgi sağlar.
author: gionoder
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 3efa05f49748f6bbff680f322a77cec24da46c0c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240591"
---
# <a name="nf-e-custom-certificate-validation"></a><span data-ttu-id="2dfa9-103">NF-e özel sertifika doğrulaması</span><span class="sxs-lookup"><span data-stu-id="2dfa9-103">NF-e custom certificate validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2dfa9-104">NF-e özel sertifika doğrulama özelliğini etkinleştirdiğinizde, özel doğrulama Web hizmetleriyle bağlantı yapılmasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="2dfa9-104">When you turn the NF-e custom certificate verification feature, custom validation allows a connection with the web services.</span></span> <span data-ttu-id="2dfa9-105">Bu bağlantı, SEFAZ üzerinden NF-e aktarmak ve yetkilendirme almak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2dfa9-105">This connection is required to transmit NF-e and receive authorization from SEFAZ.</span></span>

<span data-ttu-id="2dfa9-106">Sertifika V5'deki **Sunucu kimlik doğrulama amacı** özelliği, Brezilya Kök Sertifika Yetkilisi tarafından verilir.</span><span class="sxs-lookup"><span data-stu-id="2dfa9-106">The **Server authentication purpose** property from the certificate V5 is issued by the Brazilian Root Certificate Authority.</span></span> <span data-ttu-id="2dfa9-107">Bu özellik varsayılan olarak kapalıdır ve el ile etkinleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="2dfa9-107">This property is turned off by default and must be manually enabled.</span></span> <span data-ttu-id="2dfa9-108">Bazı durumlarda, otomatik sertifika güncelleştirme bu özelliği artık etkin olmayacak şekilde değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="2dfa9-108">In some circumstances, the automatic certificate update can switch this property to no longer be enabled.</span></span> <span data-ttu-id="2dfa9-109">Bu durumda, TLS bağlantısı etkilenir ve artık güvenilir değildir.</span><span class="sxs-lookup"><span data-stu-id="2dfa9-109">If this happens, the TLS connection is affected and is no longer trusted.</span></span> <span data-ttu-id="2dfa9-110">Minas Gerais (MG) ve Paraná (PR) eyaletlerinin üretim ortamlarında NF-e verme yeteneği de etkilenebilir.</span><span class="sxs-lookup"><span data-stu-id="2dfa9-110">The ability to issue NF-e on production environments for states of Minas Gerais (MG) and Paraná (PR) states is also impacted.</span></span>

<span data-ttu-id="2dfa9-111">Bu güncelleştirme, sertifika doğrulaması için alternatif bir çözüme olanak tanır, başka bir deyişle, güvenli bir iletişim kurma olanağı vardır.</span><span class="sxs-lookup"><span data-stu-id="2dfa9-111">This update allows for an alternative solution for certificate validation, which means that it’s possible to establish a secure communication.</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]