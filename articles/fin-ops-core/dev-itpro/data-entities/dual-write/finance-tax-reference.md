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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 50f906d62ad6f1e0b79c9c1bb6fcd373ba350c98
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172610"
---
# <a name="access-to-finance-and-tax-reference-data"></a><span data-ttu-id="a5c87-103">Finans ve vergi referans verilerine erişim</span><span class="sxs-lookup"><span data-stu-id="a5c87-103">Access to finance and tax reference data</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="a5c87-104">Her işletme mali takvim yılı, işletmenin işlemlerini gerçekleştirdiği para birimi, işletmenin çalışması sırasında giren ve giden paranın bulunduğu hesaplar, vergi oranları ve havale gibi temel bir mali veri kümesiyle çalışır.</span><span class="sxs-lookup"><span data-stu-id="a5c87-104">Every business works with a basic set of financial data, such as the fiscal calendar year, the currency that business is transacted in, the accounts that the money to run the business comes in to or goes out of, tax rates, and remittance.</span></span> <span data-ttu-id="a5c87-105">Bu veriler Finance and Operations uygulamalarında bulunur.</span><span class="sxs-lookup"><span data-stu-id="a5c87-105">This data resides in Finance and Operations apps.</span></span> <span data-ttu-id="a5c87-106">Ancak, Microsoft Dynamics 365'deki model temelli uygulamaların finans ve vergi verileri için tek bir kaynağı olabilmesi için Common Data Service'a sunulur.</span><span class="sxs-lookup"><span data-stu-id="a5c87-106">However, it's exposed to Common Data Service so that model-driven apps in Microsoft Dynamics 365 can have a single source for finance and tax data.</span></span> <span data-ttu-id="a5c87-107">Böylece, veriler işletme ekosistemi içinde aynı şekilde yer alır.</span><span class="sxs-lookup"><span data-stu-id="a5c87-107">In this way, data is uniform across the business ecosystem.</span></span> 

<span data-ttu-id="a5c87-108">Finans ve vergi verileri aşağıdaki eşlemeler kullanılarak tümleştirilir:</span><span class="sxs-lookup"><span data-stu-id="a5c87-108">Finance and tax data is integrated by using the following mappings:</span></span>

+ [<span data-ttu-id="a5c87-109">Tümleşik genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="a5c87-109">Integrated ledger</span></span>](ledger-mapping.md)
+ [<span data-ttu-id="a5c87-110">Tümleşik vergi aslı</span><span class="sxs-lookup"><span data-stu-id="a5c87-110">Integrated tax master</span></span>](tax-mapping.md)
