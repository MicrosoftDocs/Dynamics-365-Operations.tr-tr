---
title: NF-e özel sertifika doğrulaması
description: Bu konu, NF-e özel sertifikasını etkinleştirme ve kullanma hakkında bilgi sağlar.
author: gionoder
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 895513f51798a797ebf59f8a5be4f5cde006726d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813980"
---
# <a name="nf-e-custom-certificate-validation"></a><span data-ttu-id="b2a8d-103">NF-e özel sertifika doğrulaması</span><span class="sxs-lookup"><span data-stu-id="b2a8d-103">NF-e custom certificate validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2a8d-104">NF-e özel sertifika doğrulama özelliğini etkinleştirdiğinizde, özel doğrulama Web hizmetleriyle bağlantı yapılmasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="b2a8d-104">When you turn the NF-e custom certificate verification feature, custom validation allows a connection with the web services.</span></span> <span data-ttu-id="b2a8d-105">Bu bağlantı, SEFAZ üzerinden NF-e aktarmak ve yetkilendirme almak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="b2a8d-105">This connection is required to transmit NF-e and receive authorization from SEFAZ.</span></span>

<span data-ttu-id="b2a8d-106">Sertifika V5'deki **Sunucu kimlik doğrulama amacı** özelliği, Brezilya Kök Sertifika Yetkilisi tarafından verilir.</span><span class="sxs-lookup"><span data-stu-id="b2a8d-106">The **Server authentication purpose** property from the certificate V5 is issued by the Brazilian Root Certificate Authority.</span></span> <span data-ttu-id="b2a8d-107">Bu özellik varsayılan olarak kapalıdır ve el ile etkinleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="b2a8d-107">This property is turned off by default and must be manually enabled.</span></span> <span data-ttu-id="b2a8d-108">Bazı durumlarda, otomatik sertifika güncelleştirme bu özelliği artık etkin olmayacak şekilde değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="b2a8d-108">In some circumstances, the automatic certificate update can switch this property to no longer be enabled.</span></span> <span data-ttu-id="b2a8d-109">Bu durumda, TLS bağlantısı etkilenir ve artık güvenilir değildir.</span><span class="sxs-lookup"><span data-stu-id="b2a8d-109">If this happens, the TLS connection is affected and is no longer trusted.</span></span> <span data-ttu-id="b2a8d-110">Minas Gerais (MG) ve Paraná (PR) eyaletlerinin üretim ortamlarında NF-e verme yeteneği de etkilenebilir.</span><span class="sxs-lookup"><span data-stu-id="b2a8d-110">The ability to issue NF-e on production environments for states of Minas Gerais (MG) and Paraná (PR) states is also impacted.</span></span>

<span data-ttu-id="b2a8d-111">Bu güncelleştirme, sertifika doğrulaması için alternatif bir çözüme olanak tanır, başka bir deyişle, güvenli bir iletişim kurma olanağı vardır.</span><span class="sxs-lookup"><span data-stu-id="b2a8d-111">This update allows for an alternative solution for certificate validation, which means that it’s possible to establish a secure communication.</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]