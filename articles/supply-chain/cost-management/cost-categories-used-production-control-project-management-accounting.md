---
title: Üretim kontrolde ve Proje yönetimi muhasebesinde kullanılan maliyet kategorileri
description: Bazı üretim iş türleri, proje süresi tahminlerine ve raporlamaya uygulanabilir. Bu makalede, bu tip üretim işi için üretim ve proje amaçlı olarak tanımlamanız gereken maliyet kategorileri hakkında bilgiler sağlanmıştır.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjCategory
audience: Application User
ms.reviewer: kamaybac
ms.custom: 78253
ms.assetid: cfdd58a0-8afa-4a6f-a208-a76e2c162429
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bffb56fa195c040520ad35bbadaa90816f14dc2a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839475"
---
# <a name="cost-categories-used-in-production-control-and-project-management-accounting"></a><span data-ttu-id="662c2-104">Üretim kontrolde ve Proje yönetimi muhasebesinde kullanılan maliyet kategorileri</span><span class="sxs-lookup"><span data-stu-id="662c2-104">Cost categories used in Production control and Project management accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="662c2-105">Bazı üretim iş türleri, proje süresi tahminlerine ve raporlamaya uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="662c2-105">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="662c2-106">Bu makalede, bu tip üretim işi için üretim ve proje amaçlı olarak tanımlamanız gereken maliyet kategorileri hakkında bilgiler sağlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="662c2-106">This article provides information about the cost categories that you must define for these types of production work for production and project purposes.</span></span>

<span data-ttu-id="662c2-107">Bazı üretim iş türleri, proje süresi tahminlerine ve raporlamaya uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="662c2-107">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="662c2-108">Bu durumda, üretim ve proje amaçları için bir maliyet kategorisi gereklidir.</span><span class="sxs-lookup"><span data-stu-id="662c2-108">In this case, a cost category is required for production and project purposes.</span></span> <span data-ttu-id="662c2-109">Bir maliyet kategorisi üretim ve projelerde kullanılacaksa, projeyle ilgili ek bilgilerin tanımlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="662c2-109">When a cost category is used in production and projects, additional project-related information must be defined.</span></span> <span data-ttu-id="662c2-110">Örneğin, projelerle ilişkilendirilmiş olan saatlik maliyetler üretimle ilişkilendirilmiş olan saatlik maliyetlerden farklıdır.</span><span class="sxs-lookup"><span data-stu-id="662c2-110">For example, the hourly costs that are associated with projects can differ from the hourly costs that are associated with production.</span></span> <span data-ttu-id="662c2-111">**Maliyet kategorileri** sayfasını kullanarak Üretim kontrol ve Proje yönetim muhasebesinde kullanılan bir maliyet kategorisi tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="662c2-111">You can use the **Cost categories** page to define a cost category that is used in Production control and Project management accounting.</span></span> 

<span data-ttu-id="662c2-112">**Not:** Maliyet muhasebesinde bir **Proje kategorileri** sayfası vardır ama bu sayfanın bu konuda açıklanan işlevle ilişkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="662c2-112">**Note:** Cost accounting has a **Project categories** page, but this page has no relationship to the functionality that is described in this topic.</span></span> <span data-ttu-id="662c2-113">Projelerde bir maliyet kategorisi kullandığınızda **Maliyet kategorileri** sayfasında proje ile ilgili ek bilgiler gösteren ek sekmeler olur.</span><span class="sxs-lookup"><span data-stu-id="662c2-113">When you use a cost category in projects, the **Cost categories** page has additional tabs that show additional project-related information.</span></span> <span data-ttu-id="662c2-114">Bu bilgiler, maliyet kategorisine atanmış kategori grubu, bir satır özelliğini ve genel muhasebe hesaplarını içerir.</span><span class="sxs-lookup"><span data-stu-id="662c2-114">This information includes the category group, a line property, and ledger accounts that are assigned to the cost category.</span></span>

-   <span data-ttu-id="662c2-115">Maliyet kategorisi, hareket tipi olarak **Saat**'i destekleyen bir kategori grubuna atanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="662c2-115">The cost category must be assigned to a category group that supports a transaction type of **Hours**.</span></span>
-   <span data-ttu-id="662c2-116">Satır özelliği, raporlanan sürenin bir proje için nasıl masraflandırılabileceği hakkında varsayılan bilgileri belirtir.</span><span class="sxs-lookup"><span data-stu-id="662c2-116">The line property indicates default information about how reported time can be charged to a project.</span></span>
-   <span data-ttu-id="662c2-117">Genellikle, maliyetler ve satışlarla ilişkili genel muhasebe hesapları maliyet kategorisine atanmış kategori grubu için tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="662c2-117">Typically, the ledger accounts that are related to costs and sales are defined for the category group that is assigned to the cost category.</span></span> <span data-ttu-id="662c2-118">Ancak, belirli bir maliyet kategorisi için spesifik hesaplar tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="662c2-118">However, specific accounts can be defined for an individual cost category.</span></span>

<span data-ttu-id="662c2-119">**Maliyet kategorileri** sayfasındaki ek düğmeler, seçili bir maliyet kategorisi hakkında projeyle ilgili bilgilere erişim sağlar.</span><span class="sxs-lookup"><span data-stu-id="662c2-119">Additional buttons on the **Cost categories** page let you access project-related information about a selected cost category.</span></span> <span data-ttu-id="662c2-120">Örneğin, proje ile ilgili hareketleri görüntüleyebilir, çalışanları veya projeleri tanımlayabilir, saatlik maliyet ve satış fiyatlarını tanımlayabilir ve raporlarını görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="662c2-120">For example, you can view project-related transactions, define employees or projects, define hourly costs and sales prices, and view reports.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]