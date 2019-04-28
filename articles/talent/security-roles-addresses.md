---
title: Güvenlik rolüne göre özel adreslere erişim
description: Bu konu, bir müşterinin özel adreslere erişemediği sorunun çözümünü açıklar.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f8aaa33e5fda404b48548f9a57977dd0ccd53dc1
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/19/2019
ms.locfileid: "859494"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="88359-103">Güvenlik rolüne göre özel adreslere erişim</span><span class="sxs-lookup"><span data-stu-id="88359-103">Access to private addresses by security role</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="88359-104">**Stok çıkışı**</span><span class="sxs-lookup"><span data-stu-id="88359-104">**Issue**</span></span>

<span data-ttu-id="88359-105">Bir müşteri, bir güvenlik rolünü çoğalttıktan sonra ve yeni rol ile oturum açtığında, müşteri özel olarak işaretlenmiş adresleri göremez.</span><span class="sxs-lookup"><span data-stu-id="88359-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="88359-106">**Çözünürlük**</span><span class="sxs-lookup"><span data-stu-id="88359-106">**Resolution**</span></span>

<span data-ttu-id="88359-107">Bu sorunu gidermek için müşterinin çoğaltılan güvenlik rolü için bu adımları izlemesi gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="88359-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="88359-108">**Kuruluş yönetimi \> Genel adres defteri \> Genel adres defteri parametreleri seçeneğine gidin.**</span><span class="sxs-lookup"><span data-stu-id="88359-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="88359-109">**Özel konum güvenliği** sekmesinde, yeni güvenlik rolünü **Kullanılabilir roller** listesinden **Seçilen roller** listesine taşıyın.</span><span class="sxs-lookup"><span data-stu-id="88359-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="88359-110">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="88359-110">Select **Save**.</span></span>

![Genel adres defteri parametreleri sayfası](media/GAD-parameters.png)
