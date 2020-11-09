---
title: Müşteri bağlılık programı kartları ve ödül puanları
description: Bu konu, müşteri bağlılık programı kartları ve Finance and Operations uygulamaları ile Common Data Service arasındaki ödül puanlarıyla ilgili verilerin tümleştirilmesini açıklar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 24ce08bb6cba9c74075151bafe0b07509fbdf73d
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "3998026"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="323ba-103">Müşteri bağlılık programı kartları ve ödül puanları</span><span class="sxs-lookup"><span data-stu-id="323ba-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="323ba-104">İşletmeler, müşteri alışverişi ve harcama alışkanlıkları temel alınarak müşterileri sınıflandırmakta ve karmaşık servisler sağlıyor.</span><span class="sxs-lookup"><span data-stu-id="323ba-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="323ba-105">Microsoft Dynamics 365 uygulama paketinde, Dynamics 365 Commerce müşteri bağlılık programı kartlarını, ödüllendirmeyi, bağlılık programı tabanlı fiyatlandırmayı ve ödül tabanlı alışveriş deneyimlerini kolaylaştırmak ve işlemek için gerekli altyapıyı ve işlevleri vardır.</span><span class="sxs-lookup"><span data-stu-id="323ba-105">In the Microsoft Dynamics 365 suite of applications, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="323ba-106">Commerce'teki müşteri bağlılık programı kartları ve ödül puanları Common Data Service'e eşitlendiğinde Dynamics 365'teki modele dayalı uygulamalar bu verileri kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="323ba-106">When data about customer loyalty cards and reward points in Commerce is synced to Common Data service, model-driven apps in Dynamics 365 can use that data.</span></span> <span data-ttu-id="323ba-107">Örneğin, Dynamics 365 Customer Service kullanıcıları, verileri yardım masasıyla aynı Gelişmiş hizmetleri sağlamak için kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="323ba-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="323ba-108">Şablonlar</span><span class="sxs-lookup"><span data-stu-id="323ba-108">Templates</span></span>

| <span data-ttu-id="323ba-109">Finance and Operations uygulamaları</span><span class="sxs-lookup"><span data-stu-id="323ba-109">Finance and Operations apps</span></span> | <span data-ttu-id="323ba-110">Dynamics 365'teki model yönetimli uygulamalar</span><span class="sxs-lookup"><span data-stu-id="323ba-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="323ba-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="323ba-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="323ba-112">Bağlılık programı kartı</span><span class="sxs-lookup"><span data-stu-id="323ba-112">Loyalty card</span></span>                | <span data-ttu-id="323ba-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="323ba-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="323ba-114">Bu şablon müşteri bağlılık programı kartılarıyla ilgili bilgileri eşitler.</span><span class="sxs-lookup"><span data-stu-id="323ba-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="323ba-115">Bağlılık programı ödül puanları</span><span class="sxs-lookup"><span data-stu-id="323ba-115">Loyalty reward points</span></span>       | <span data-ttu-id="323ba-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="323ba-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="323ba-117">Bu şablon müşteri ödül puanlarıyla ilgili bilgileri eşitler.</span><span class="sxs-lookup"><span data-stu-id="323ba-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
