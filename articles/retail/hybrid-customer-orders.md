---
title: "Karma müşteri siparişleri"
description: "Bir karma müşteri siparişi, hem müşteri tarafından mağazadan alınabilecek ürünler içeren hem de daha sonra çekilecek veya sevk edilecek tek bir sipariştir."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: a00e69a589ffe744f88edb6a8b3709c4029fc1ec
ms.contentlocale: tr-tr
ms.lasthandoff: 01/04/2019

---

# <a name="hybrid-customer-orders"></a><span data-ttu-id="6fab8-103">Karma müşteri siparişleri</span><span class="sxs-lookup"><span data-stu-id="6fab8-103">Hybrid customer orders</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6fab8-104">Bir karma müşteri siparişi, hem müşteri tarafından mağazadan alınabilecek ürünler içeren hem de daha sonra çekilecek veya sevk edilecek tek bir sipariştir.</span><span class="sxs-lookup"><span data-stu-id="6fab8-104">A hybrid customer order is a single order, which contains products that can be carried out of the store by the customer, as well as products that will be picked up or shipped later.</span></span>

<span data-ttu-id="6fab8-105">Microsoft Dynamics 365 for Retail içerisinde, bir müşteri siparişi için tüm ürünleri yerine getirmeyi veya yalnızca seçilen ürünleri yerine getirmeyi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6fab8-105">In Microsoft Dynamics 365 for Retail, you can select either carry out all products or carry out selected products for a customer order.</span></span> <span data-ttu-id="6fab8-106">Yerine getirilmek üzere işaretlenmiş ürün satırları, sipariş oluşturulduktan sonra otomatik olarak faturalanır, sipariş oluşturulduktan sonra çekilecek bir sipariş için de aynı şey geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="6fab8-106">The product lines that are marked as carry out are automatically invoiced after the order is created, similarly this is the same for an order that is to be picked-up after the order is created.</span></span> <span data-ttu-id="6fab8-107">Karma siparişlerde kalan tutar, ürün çekme ve sevk satırlarındaki depozito yüzdesini, yürütülecek satırların toplam tutarına eklenerek belirlenir.</span><span class="sxs-lookup"><span data-stu-id="6fab8-107">The amount due on hybrid orders is determined by adding the deposit percentage on pick and ship product lines with the full amount of the carry out lines.</span></span> <span data-ttu-id="6fab8-108">Sistem, karma siparişler için müşteri sipariş modur ve nakit ve taşı modları arasında şöyle geçiş yapar:</span><span class="sxs-lookup"><span data-stu-id="6fab8-108">For hybrid orders, the system switches between customer order mode and cash and carry mode as follows:</span></span>

- <span data-ttu-id="6fab8-109">Sepetteki tüm ürünler **Teslim alınan taşıma** olarak ayarlanmışsa, sipariş Öde ve Al hareketi olarak ele alınır.</span><span class="sxs-lookup"><span data-stu-id="6fab8-109">If all products in the cart are set to **Carry out delivery**, the order will be handled as a Cash and Carry transaction.</span></span>
- <span data-ttu-id="6fab8-110">Sepetteki tüm veya bazı satırlar **Çekme** veya **sevk nakliyesi** olarak ayarlanmışsa, sipariş Müşteri sipariş hareketi olarak ele alınır.</span><span class="sxs-lookup"><span data-stu-id="6fab8-110">If any or all lines in the cart are set to either **Pick** or **ship delivery**, the order will be handled as a Customer order transaction.</span></span>

<span data-ttu-id="6fab8-111">Bir sepet satırı seçildiyse ve **Seçileni çek**, **Seçileni sevk et** veya **Seçileni al git** seçiliyse, sadece belirli sepet satırları bu teslim yöntemiyle ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="6fab8-111">If a cart line is selected and **Pick selected**, **Ship selected**, or **Carry out selected** is selected, only the specific cart line is set with that delivery method.</span></span> <span data-ttu-id="6fab8-112">Bu durumda, işlem akışı her zaman olduğu gibi devam eder.</span><span class="sxs-lookup"><span data-stu-id="6fab8-112">In that case, the downstream flow of the operation continues as usual.</span></span> <span data-ttu-id="6fab8-113">Ancak, **Seçileni çek**, **Seçileni sevk et** veya **Seçileni al git**, sepet satırı seçmeden seçildiyse, tüm sepet satırlarını listeleyen yeni bir sayfa açılır.</span><span class="sxs-lookup"><span data-stu-id="6fab8-113">However, if **Pick selected**, **Ship selected**, or **Carry out selected** is selected without a cart line being selected, a new page opens that lists all the cart lines.</span></span> <span data-ttu-id="6fab8-114">Bu ekranda, bir teslim yöntemi ayarlamak için birden fazla satırı aynı anda seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6fab8-114">On that screen, you can select multiple lines at once for setting the delivery method.</span></span> <span data-ttu-id="6fab8-115">Satırları seçmek için bu yöntemi kullandığınızda, satıra daha önce atanan tüm teslim yöntemleri geçersiz kılınır.</span><span class="sxs-lookup"><span data-stu-id="6fab8-115">When you use that method for selecting lines, any previous delivery method that has been assigned to the line will be overridden.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6fab8-116">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="6fab8-116">Additional resources</span></span>

[<span data-ttu-id="6fab8-117">Müşteri siparişlerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="6fab8-117">Customer orders overview</span></span>](customer-orders-overview.md)

