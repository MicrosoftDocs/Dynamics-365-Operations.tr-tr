---
title: Müşteri bağlılık programı kartları ve ödül puanları
description: Bu konuda, müşteri bağlılık programı kartları ve çift yazmadaki ödül puanlarıyla ilgili verilerin tümleştirilmesi açıklanmaktadır.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: d2c3845c1a7371d9e992495246e8dd0eb8631020
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747999"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="05043-103">Müşteri bağlılık programı kartları ve ödül puanları</span><span class="sxs-lookup"><span data-stu-id="05043-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="05043-104">İşletmeler, müşteri alışverişi ve harcama alışkanlıkları temel alınarak müşterileri sınıflandırmakta ve karmaşık servisler sağlıyor.</span><span class="sxs-lookup"><span data-stu-id="05043-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="05043-105">Örneğin Dynamics 365 Commerce, müşteri bağlılık programı kartlarını, ödüllendirme puanlarını, bağlılık programı tabanlı fiyatlandırmayı ve ödül tabanlı alışveriş deneyimlerini kolaylaştırmak ve işlemek için gerekli altyapıya ve işlevlere sahiptir.</span><span class="sxs-lookup"><span data-stu-id="05043-105">For example, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="05043-106">Commerce'teki müşteri bağlılık programı kartları ve ödül puanları Dataverse'e eşitlendiğinde, müşteri etkileşimi uygulamaları bu verileri kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="05043-106">When data about customer loyalty cards and reward points in Commerce is synced to Dataverse, customer engagement apps can use that data.</span></span> <span data-ttu-id="05043-107">Örneğin, Dynamics 365 Customer Service kullanıcıları, verileri yardım masasıyla aynı Gelişmiş hizmetleri sağlamak için kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="05043-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="05043-108">Şablonlar</span><span class="sxs-lookup"><span data-stu-id="05043-108">Templates</span></span>

| <span data-ttu-id="05043-109">Finance and Operations uygulamaları</span><span class="sxs-lookup"><span data-stu-id="05043-109">Finance and Operations apps</span></span> | <span data-ttu-id="05043-110">Dynamics 365'teki model yönetimli uygulamalar</span><span class="sxs-lookup"><span data-stu-id="05043-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="05043-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="05043-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="05043-112">Bağlılık programı kartı</span><span class="sxs-lookup"><span data-stu-id="05043-112">Loyalty card</span></span>                | <span data-ttu-id="05043-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="05043-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="05043-114">Bu şablon müşteri bağlılık programı kartılarıyla ilgili bilgileri eşitler.</span><span class="sxs-lookup"><span data-stu-id="05043-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="05043-115">Bağlılık programı ödül puanları</span><span class="sxs-lookup"><span data-stu-id="05043-115">Loyalty reward points</span></span>       | <span data-ttu-id="05043-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="05043-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="05043-117">Bu şablon müşteri ödül puanlarıyla ilgili bilgileri eşitler.</span><span class="sxs-lookup"><span data-stu-id="05043-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]