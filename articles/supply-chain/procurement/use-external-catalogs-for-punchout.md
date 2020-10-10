---
title: PunchOut e-procurement için harici katalogları kullanma
description: Bu konu, istekler oluşturmak ve göndermek için harici katalogları nasıl kullanacağınızı açıklar.
author: mkirknel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: adeffa101aa5a17543ca531aacde2130a07086e9
ms.sourcegitcommit: b281ac04157f6ccbd159fc89f58910b430a3b6a9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/21/2020
ms.locfileid: "3826816"
---
# <a name="use-external-catalogs-for-punchout-e-procurement"></a><span data-ttu-id="1f735-103">PunchOut e-procurement için harici katalogları kullanma</span><span class="sxs-lookup"><span data-stu-id="1f735-103">Use external catalogs for PunchOut e-procurement</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1f735-104">PunchOut e-tedarik için harici katalogları kullanarak, satıcılarınızın ürünleriyle ilgili bilgileri kendi ana verileriniz içinde korumanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="1f735-104">By using external catalogs for PunchOut e-procurement, you don't have to maintain information about your vendors' products in your own master data.</span></span> <span data-ttu-id="1f735-105">Bunun yerine, satıcının web sitesindeki alışveriş sepeti doğru ürün bilgisine sahip istek satırlarına dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="1f735-105">Instead, the shopping cart on a vendor's website is converted to requisition lines that have the correct product information.</span></span> 

<span data-ttu-id="1f735-106">Satıcınızın ürünlerinin açıklamalarını ve fiyatlarını kendi ana ürün verilerinizde tutmaktan kaçınmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1f735-106">You should avoid maintaining the descriptions and prices of your vendors’ products in your own product master data.</span></span> <span data-ttu-id="1f735-107">Bunun yerine, PunchOut e-tedarik için harici katalogları kullanın.</span><span class="sxs-lookup"><span data-stu-id="1f735-107">Instead, use external catalogs for PunchOut e-procurement.</span></span> <span data-ttu-id="1f735-108">Ardından, çalışanlar taleplerini oluşturduğunda, satıcının harici katalog sitesine çıkış yapabilirler (diğer bir deyişle, sisteminizden ayrılıp satıcının sitesine giderler).</span><span class="sxs-lookup"><span data-stu-id="1f735-108">Then, when employees create requisitions, they can “punch out” to a vendor’s external catalog site (in other words, they leave your system and go to the vendor’s site).</span></span> <span data-ttu-id="1f735-109">Satıcının web sitesinde alışveriş sepetine eklenen ürünler daha sonra talep satırlarına dönüştürülebilir.</span><span class="sxs-lookup"><span data-stu-id="1f735-109">The products that are added to the shopping cart on the vendor’s website can then be converted to requisition lines.</span></span> <span data-ttu-id="1f735-110">Bu nedenle, doğru ürün bilgilerini alırsınız: ürün kimliği, adı, fiyat ve benzeri.</span><span class="sxs-lookup"><span data-stu-id="1f735-110">Therefore, you get the correct product information: product ID, name, price, and so on.</span></span>

<span data-ttu-id="1f735-111">Harici katalogları kullanmak için çalışanın **Satınalma taleplerim** sayfasında bir talep oluşturması gerekir.</span><span class="sxs-lookup"><span data-stu-id="1f735-111">To use external catalogs, an employee must create a requisition on the **My purchase requisitions** page.</span></span>

<span data-ttu-id="1f735-112">Talebi oluşturan çalışan talebin hazırlayıcısı olarak geçer.</span><span class="sxs-lookup"><span data-stu-id="1f735-112">The employee who creates a requisition is referred to as the preparer of the requisition.</span></span> <span data-ttu-id="1f735-113">Hazırlayan kişi olarak aşağıdaki görevleri tamamlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1f735-113">As a preparer, you can complete the following tasks.</span></span>

<span data-ttu-id="1f735-114">Belirli talep sahibi, satınalma tüzelkişiliği ve alıcı işlem birimi için kullanılabilir olan tüm harici katalogları içeren bir sayfayı açmak için **Harici kataloglar** satırı eylemini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1f735-114">Use the **External catalogs** line action to open a page that includes all external catalogs that are available for the specified requester, buying legal entity, and receiving operating unit.</span></span>

<span data-ttu-id="1f735-115">İzinlere bağlı olarak talep sahibini, satınalma tüzel kişiliğini ve alıcı işlem birimini değiştirin.</span><span class="sxs-lookup"><span data-stu-id="1f735-115">Depending on your permissions, change the requester, buying legal entity, and receiving operating unit.</span></span> <span data-ttu-id="1f735-116">Bu değerlerdeki bir değişiklik bir talep sahibi için kullanılabilir olan harici kataloglar listesini değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="1f735-116">A change in those values might change the list of external catalogs that are available to a requester.</span></span> <span data-ttu-id="1f735-117">Kullanılabilir olan harici kataloglar, satınalma tüzel kişiliği veya alıcı işlem birimi için geçerli etkin satın alma ilkelerine bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="1f735-117">The external catalogs that are available depend on the current active purchasing policies for the buying legal entity or the receiving operating unit.</span></span> <span data-ttu-id="1f735-118">Bu ilkeler belirli tedarik kategorilerine erişime izin verebilir veya erişimi engelleyebilir.</span><span class="sxs-lookup"><span data-stu-id="1f735-118">These policies can allow or prevent access to specific procurement categories.</span></span> <span data-ttu-id="1f735-119">Bu nedenle, bu tedarik kategorileriyle eşlenen harici katalogların listesi etkilenebilir.</span><span class="sxs-lookup"><span data-stu-id="1f735-119">Therefore, the list of external catalogs that are mapped to these procurement categories can be affected.</span></span>

<span data-ttu-id="1f735-120">İlkelerle ilgili daha fazla bilgi için bkz. [Satınalma ilkelerine genel bakış](../procurement/purchase-policies.md).</span><span class="sxs-lookup"><span data-stu-id="1f735-120">For more information about policies, see [Purchasing policies overview](../procurement/purchase-policies.md).</span></span>

- <span data-ttu-id="1f735-121">Belirli tedarik kategorileri için harici katalogları bulmak üzere katalog arama alanına metin girin.</span><span class="sxs-lookup"><span data-stu-id="1f735-121">To find external catalogs for specific procurement categories, enter text in the catalog search field.</span></span>
- <span data-ttu-id="1f735-122">Satıcının web sitesindeki harici kataloğundan ürünler eklemek için harici kataloğu tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1f735-122">To add products from a vendor’s external catalog on the vendor’s website, click the external catalog.</span></span> <span data-ttu-id="1f735-123">Daha sonra ürünleri alışveriş sepetine ekleyin ve ödemeye geçin. Alışveriş sepeti satırları Microsoft Dynamics 365'e aktarılacaktır.</span><span class="sxs-lookup"><span data-stu-id="1f735-123">Then add products to the shopping cart, and check out. The shopping cart lines will be transferred to Microsoft Dynamics 365.</span></span>

<span data-ttu-id="1f735-124">Tedarik kategorileri için birden fazla seçenek varsa, talebe satırları eklemeden önce doğru tedarik kategorisini seçin.</span><span class="sxs-lookup"><span data-stu-id="1f735-124">If there are multiple options for procurement categories, select the correct procurement category before you add the lines to the requisition.</span></span>
<span data-ttu-id="1f735-125">Talebe satırlar eklendikten sonra harici katalogları kullanmadan daha fazla satır ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1f735-125">After lines have been added to a requisition, you can add more lines without using external catalogs.</span></span> <span data-ttu-id="1f735-126">Alternatif olarak, satır eklemek için harici katalogları kullanmaya devam edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1f735-126">Alternatively, you can continue to use external catalogs to add lines.</span></span>

<span data-ttu-id="1f735-127">Talep hazır olduğunda, onay için göndermek üzere **İş akışı** > **Gönder** eylemini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1f735-127">When the requisition is ready, use the **Workflow** > **Submit** action to submit it for approval.</span></span>

### <a name="additional-resources"></a><span data-ttu-id="1f735-128">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="1f735-128">Additional resources</span></span>

- [<span data-ttu-id="1f735-129">PunchOut e-procurement için harici katalog ayarlama</span><span class="sxs-lookup"><span data-stu-id="1f735-129">Set up an external catalog for PunchOut e-procurement</span></span>](set-up-external-catalog-for-punchout.md)
- [<span data-ttu-id="1f735-130">CXML geliştirmeleri satın alma</span><span class="sxs-lookup"><span data-stu-id="1f735-130">Purchasing cXML enhancements</span></span>](purchasing-cxml-enhancements.md)