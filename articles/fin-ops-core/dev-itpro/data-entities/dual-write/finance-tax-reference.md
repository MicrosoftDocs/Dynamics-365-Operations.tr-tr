---
title: Finans ve vergi referans verilerine erişim
description: Bu konu, finans ve vergi referans verilerine erişim hakkında bilgi sağlar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
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
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: f2602902bfdc201a3dfcd233b802a479b2630005
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997206"
---
# <a name="access-to-finance-and-tax-reference-data"></a><span data-ttu-id="db9d6-103">Finans ve vergi referans verilerine erişim</span><span class="sxs-lookup"><span data-stu-id="db9d6-103">Access to finance and tax reference data</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="db9d6-104">Her işletme mali takvim yılı, işletmenin işlemlerini gerçekleştirdiği para birimi, işletmenin çalışması sırasında giren ve giden paranın bulunduğu hesaplar, vergi oranları ve havale gibi temel bir mali veri kümesiyle çalışır.</span><span class="sxs-lookup"><span data-stu-id="db9d6-104">Every business works with a basic set of financial data, such as the fiscal calendar year, the currency that business is transacted in, the accounts that the money to run the business comes in to or goes out of, tax rates, and remittance.</span></span> <span data-ttu-id="db9d6-105">Bu veriler Finance and Operations uygulamalarında bulunur.</span><span class="sxs-lookup"><span data-stu-id="db9d6-105">This data resides in Finance and Operations apps.</span></span> <span data-ttu-id="db9d6-106">Ancak, Microsoft Dynamics 365'deki model temelli uygulamaların finans ve vergi verileri için tek bir kaynağı olabilmesi için Common Data Service'a sunulur.</span><span class="sxs-lookup"><span data-stu-id="db9d6-106">However, it's exposed to Common Data Service so that model-driven apps in Microsoft Dynamics 365 can have a single source for finance and tax data.</span></span> <span data-ttu-id="db9d6-107">Böylece, veriler işletme ekosistemi içinde aynı şekilde yer alır.</span><span class="sxs-lookup"><span data-stu-id="db9d6-107">In this way, data is uniform across the business ecosystem.</span></span> 

<span data-ttu-id="db9d6-108">Finans ve vergi verileri aşağıdaki eşlemeler kullanılarak tümleştirilir:</span><span class="sxs-lookup"><span data-stu-id="db9d6-108">Finance and tax data is integrated by using the following mappings:</span></span>

+ [<span data-ttu-id="db9d6-109">Tümleşik genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="db9d6-109">Integrated ledger</span></span>](ledger-mapping.md)
+ [<span data-ttu-id="db9d6-110">Tümleşik vergi aslı</span><span class="sxs-lookup"><span data-stu-id="db9d6-110">Integrated tax master</span></span>](tax-mapping.md)
