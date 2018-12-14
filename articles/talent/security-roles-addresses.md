---
title: "Güvenlik rolüne göre özel adreslere erişim"
description: "Bu konu, bir müşterinin özel adreslere erişemediği sorunun çözümünü açıklar."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: c1c1c3ce1233408e73d177f9e04f1137f3171a49
ms.contentlocale: tr-tr
ms.lasthandoff: 12/04/2018

---

# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="274f0-103">Güvenlik rolüne göre özel adreslere erişim</span><span class="sxs-lookup"><span data-stu-id="274f0-103">Access to private addresses by security role</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="274f0-104">**Stok çıkışı**</span><span class="sxs-lookup"><span data-stu-id="274f0-104">**Issue**</span></span>

<span data-ttu-id="274f0-105">Bir müşteri, bir güvenlik rolünü çoğalttıktan sonra ve yeni rol ile oturum açtığında, müşteri özel olarak işaretlenmiş adresleri göremez.</span><span class="sxs-lookup"><span data-stu-id="274f0-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="274f0-106">**Çözünürlük**</span><span class="sxs-lookup"><span data-stu-id="274f0-106">**Resolution**</span></span>

<span data-ttu-id="274f0-107">Bu sorunu gidermek için müşterinin çoğaltılan güvenlik rolü için bu adımları izlemesi gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="274f0-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="274f0-108">**Kuruluş yönetimi \> Genel adres defteri \> Genel adres defteri parametreleri seçeneğine gidin.**</span><span class="sxs-lookup"><span data-stu-id="274f0-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="274f0-109">**Özel konum güvenliği** sekmesinde, yeni güvenlik rolünü **Kullanılabilir roller** listesinden **Seçilen roller** listesine taşıyın.</span><span class="sxs-lookup"><span data-stu-id="274f0-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="274f0-110">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="274f0-110">Select **Save**.</span></span>

![Genel adres defteri parametreleri sayfası](media/GAD-parameters.png)

