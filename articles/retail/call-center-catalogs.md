---
title: "Çağrı merkezi kataloglar"
description: "Bu makalede Microsoft Dynamics 365 for Retail'da kataloglar için çağrı merkezine özel işlevler açıklanır."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7be87496ceaea2d1d5f97a5cc17e50dcddbaf33d
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="call-center-catalogs"></a><span data-ttu-id="5275c-103">Çağrı merkezi katalogları</span><span class="sxs-lookup"><span data-stu-id="5275c-103">Call center catalogs</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="5275c-104">Bu makalede Microsoft Dynamics 365 for Retail'da kataloglar için çağrı merkezine özel işlevler açıklanır.</span><span class="sxs-lookup"><span data-stu-id="5275c-104">This article describes the call center–specific functionality for catalogs in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="5275c-105">Bir çağrı merkezinde ürün kataloglarını müşterilere sunmak istediğiniz ürünleri belirlemek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5275c-105">In a call center, you can use product catalogs to identify the products that you want to offer to customers.</span></span> <span data-ttu-id="5275c-106">Çağrı merkezleri genellikle basılı kataloglar kullanır.</span><span class="sxs-lookup"><span data-stu-id="5275c-106">Call centers typically use printed catalogs.</span></span> <span data-ttu-id="5275c-107">Basılı bir kataloğun tasarımı ve üretimi Dynamics 365 for Retail dışında yapılır.</span><span class="sxs-lookup"><span data-stu-id="5275c-107">The design and production of a printed catalog is handled outside Dynamics 365 for Retail.</span></span> <span data-ttu-id="5275c-108">Ancak, çevrimiçi perakende kataloglarını ayarlamak için kullandığınız aynı sayfaları kullanarak bir kataloğun dijital biçimini oluşturabilir ve saklayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5275c-108">However, you can create and store a digital form of a catalog by using the same pages that you use to set up online retail catalogs.</span></span> <span data-ttu-id="5275c-109">Bir katalog oluşturmak için önce ürün sınıflamalar ayarlayıp sınıflamaları bir çağrı merkezine atayın.</span><span class="sxs-lookup"><span data-stu-id="5275c-109">Before you can create a catalog, you must set up product assortments and assign the assortments to a call center.</span></span> <span data-ttu-id="5275c-110">Sonra ürün kataloğuna ürünleri bu sınıflamalardan seçerek ekleyin.</span><span class="sxs-lookup"><span data-stu-id="5275c-110">You then add products to the catalog by selecting products from these assortments.</span></span> <span data-ttu-id="5275c-111">Ürün kataloğuna eklendikten ve Katalog tamamlandıktan sonra verileri doğrulamak için katalogu doğrulamalısınız.</span><span class="sxs-lookup"><span data-stu-id="5275c-111">After products have been added to the catalog, and the catalog is complete, you must validate the catalog to verify the data.</span></span> <span data-ttu-id="5275c-112">Ardından kataloğu gözden geçirme ve onay için gönderin.</span><span class="sxs-lookup"><span data-stu-id="5275c-112">You must then submit the catalog for review and approval.</span></span> <span data-ttu-id="5275c-113">Katalog onaylandıktan sonra yayımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="5275c-113">After the catalog is approved, it can be published.</span></span> <span data-ttu-id="5275c-114">Bir çağrı merkezi katalogu oluşturulduğunda, katalog yayınlandığı zaman katalog verilerinin bir ekran görüntüsünü alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5275c-114">When a call center catalog is created, you can take a snapshot of the catalog data at the time that the catalog is published.</span></span> <span data-ttu-id="5275c-115">Bu anlık görüntü işlevselliği belirli bir sürüm için katalog daha sonra değiştirilmiş ve güncelleştirilmiş olsa bile kataloga erişmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="5275c-115">This snapshot functionality lets you access a particular version of the catalog even if the catalog is later changed and updated.</span></span> <span data-ttu-id="5275c-116">Çağrı merkezi kataloglarını aşağıdaki isteğe bağlı özellikleri içerecek şekilde de ayarlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="5275c-116">Call center catalogs can also be set up to include the following optional features:</span></span>

-   <span data-ttu-id="5275c-117">**Kaynak kodları** – Belirli katalog postalarına müşterinin tepkisini izlemek için kullanılan kaynak kodları.</span><span class="sxs-lookup"><span data-stu-id="5275c-117">**Source codes** – Source codes are used to track the customer response to specific catalog mailings.</span></span>
-   <span data-ttu-id="5275c-118">**Ücretsiz ürünler** – Ürünler bir müşterinin siparişine ek ücret olmaksızın dahil edilebilir.</span><span class="sxs-lookup"><span data-stu-id="5275c-118">**Free products** – Products can be included in a customer's order at no additional charge.</span></span> <span data-ttu-id="5275c-119">Siparişe kataloğun kaynak kodu girildiğinde, bu ürünler de otomatik olarak siparişe eklenir.</span><span class="sxs-lookup"><span data-stu-id="5275c-119">These products are automatically added to an order when the source code for the catalog is entered into the order.</span></span>
-   <span data-ttu-id="5275c-120">**Komut dosyaları** –Komut dosyaları satış siparişi oluşturulduğunda, çağrı merkezi çalışanının bir müşteriye okuyacağı metinlerdir.</span><span class="sxs-lookup"><span data-stu-id="5275c-120">**Scripts** – Scripts are texts that a call center worker reads to a customer when a sales order is being created.</span></span> <span data-ttu-id="5275c-121">Komut dosyaları tebrik veya satın alma önerileri içerebilir.</span><span class="sxs-lookup"><span data-stu-id="5275c-121">Scripts can include greetings or purchase suggestions.</span></span>
-   <span data-ttu-id="5275c-122">**Sayfa düzeni** – bir sayfa düzeni yazdırılan katalog ürünleri sayfa konumunda yakalar.</span><span class="sxs-lookup"><span data-stu-id="5275c-122">**Page layout** – A page layout captures the page position of products in the printed catalog.</span></span> <span data-ttu-id="5275c-123">Bu bilgiler katalog alan analiz raporu için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5275c-123">This information is used for the catalog area analysis report.</span></span>





