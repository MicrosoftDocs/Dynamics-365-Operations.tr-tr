---
title: Güvenlik rolüne göre özel adreslere erişim
description: Bu konu, bir müşterinin özel adreslere erişemediği sorunun çözümünü açıklar.
author: andreabichsel
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8daee1b645836e96a4bf3057cb317d5409d4583a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803933"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="c704f-103">Güvenlik rolüne göre özel adreslere erişim</span><span class="sxs-lookup"><span data-stu-id="c704f-103">Access to private addresses by security role</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c704f-104">**Stok çıkışı**</span><span class="sxs-lookup"><span data-stu-id="c704f-104">**Issue**</span></span>

<span data-ttu-id="c704f-105">Bir müşteri, bir güvenlik rolünü çoğalttıktan sonra ve yeni rol ile oturum açtığında, müşteri özel olarak işaretlenmiş adresleri göremez.</span><span class="sxs-lookup"><span data-stu-id="c704f-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="c704f-106">**Çözünürlük**</span><span class="sxs-lookup"><span data-stu-id="c704f-106">**Resolution**</span></span>

<span data-ttu-id="c704f-107">Bu sorunu gidermek için müşterinin çoğaltılan güvenlik rolü için bu adımları izlemesi gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="c704f-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="c704f-108">**Kuruluş yönetimi \> Genel adres defteri \> Genel adres defteri parametreleri seçeneğine gidin.**</span><span class="sxs-lookup"><span data-stu-id="c704f-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="c704f-109">**Özel konum güvenliği** sekmesinde, yeni güvenlik rolünü **Kullanılabilir roller** listesinden **Seçilen roller** listesine taşıyın.</span><span class="sxs-lookup"><span data-stu-id="c704f-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="c704f-110">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c704f-110">Select **Save**.</span></span>

![Genel adres defteri parametreleri sayfası](media/GAD-parameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]