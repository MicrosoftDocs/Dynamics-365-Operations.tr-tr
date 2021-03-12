---
title: Taşımacılık yönetimi sair giderleri
description: Bu konuda, taşıma nedeniyle oluşan masrafların bir masraf koduyla nasıl ilişkilendirileceği açıklanmaktadır.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: cb503072fb76e04aa01ff2d231c756eeb244c65a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004714"
---
# <a name="transportation-management-miscellaneous-charges"></a><span data-ttu-id="5ff71-103">Taşımacılık yönetimi sair giderleri</span><span class="sxs-lookup"><span data-stu-id="5ff71-103">Transportation management miscellaneous charges</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5ff71-104">Tüm diğer sair giderlerde olduğu gibi, taşıma nedeniyle oluşan masraflar bir masraf koduyla ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="5ff71-104">As with all miscellaneous charges, transportation-generated charges must be associated with a charge code.</span></span> <span data-ttu-id="5ff71-105">Aksi takdirde, bunlar sair gider olarak siparişe geri eklenmez.</span><span class="sxs-lookup"><span data-stu-id="5ff71-105">Otherwise, they won't be added back to the order as a miscellaneous charge.</span></span> <span data-ttu-id="5ff71-106">**Masraf kodu**, ilgili olduğu sipariş ve sipariş satırıyla ilişkili olarak masrafın nasıl hesaba alınacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ff71-106">The **Charges code** determines how the charge is accounted for in relation to the order and order line where it is added.</span></span>

<span data-ttu-id="5ff71-107">Masraflara belirli bir **Masraf kodunun** ne zaman uygulanacağını belirleyen uygun ölçütleri tanımlamak için **Taşımacılık yönetimi > Kurulum > derecelendirme > sair giderler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="5ff71-107">Go to **Transportation management > Setup > Rating > Miscellaneous charges** to define the qualifying criteria that determine when a specific **Charges code** is applied to a charge.</span></span>

<span data-ttu-id="5ff71-108">**Sair gider türü**'nün *Hiçbiri* olarak ayarlandığı her ilgili **Masraflar modülü** ayarı (*Müşteri* ve *Satıcı*) için en az bir kurulumunuz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5ff71-108">You should have at least one setup for each relevant **Charges module** setting (*Customer* and *Vendor*) where the **Miscellaneous charge type** is set to *None*.</span></span> <span data-ttu-id="5ff71-109">Bu eksikse sair gider siparişe *eklenmez*.</span><span class="sxs-lookup"><span data-stu-id="5ff71-109">If this is missing, the miscellaneous charge will *not* be added to the order.</span></span>
