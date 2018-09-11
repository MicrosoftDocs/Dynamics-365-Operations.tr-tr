--- 
title: "Tek seferlik tedarikçi için satınalma siparişi oluşturma"
description: "Bu prosedür, size satınalma siparişinin tek seferlik bir tedarikçi için nasıl oluşturulacağını gösterir."
author: FrankDahl
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchCreateOrder
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 276a0031bb51e711b55c85c253164036a9d6c1f7
ms.contentlocale: tr-tr
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="c3def-103">Tek seferlik tedarikçi için satınalma siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="c3def-103">Create a purchase order for a one-time supplier</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c3def-104">Bu prosedür, size satınalma siparişinin tek seferlik bir tedarikçi için nasıl oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c3def-104">This procedure shows you how to create a purchase order for a one-time supplier.</span></span> <span data-ttu-id="c3def-105">Satıcı hesabını el ile oluşturmak yerine tedarikçi satınalma siparişi ile otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c3def-105">The supplier is created automatically with the purchase order, rather than having to create the vendor account manually.</span></span> <span data-ttu-id="c3def-106">Satınalma siparişleri genellikle bir satınalma temsilcisi tarafından oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c3def-106">Purchase orders are typically created by a purchasing agent.</span></span> <span data-ttu-id="c3def-107">Bu kılavuzda gösterilen örnek, demo veriler şirketi USMF'de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c3def-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="c3def-108">Tek seferlik satıcı hesabının Hesap borç parametreleri sayfasında ayarlanması bir önkoşuldur.</span><span class="sxs-lookup"><span data-stu-id="c3def-108">It is a prerequisite that a one-time vendor account has been set up in the Account payable parameters page.</span></span>


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="c3def-109">Tek seferlik tedarikçi için satınalma siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="c3def-109">Create a purchase order for a one-time supplier</span></span>
1. <span data-ttu-id="c3def-110">Tedarik ve kaynak atama > Sipariş emirleri > Tüm sipariş emirleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="c3def-110">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="c3def-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c3def-111">Click New.</span></span>
3. <span data-ttu-id="c3def-112">Tek seferlik tedarikçi alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c3def-112">Select Yes in the One-time supplier field.</span></span>
    * <span data-ttu-id="c3def-113">Bir satıcı hesabı otomatik olarak oluşturulur ve satınalma siparişine atanır.</span><span class="sxs-lookup"><span data-stu-id="c3def-113">A vendor account is automatically created and assigned to the purchase order.</span></span> <span data-ttu-id="c3def-114">Satıcı hesabı, Borç hesapları parametreleri sayfasındaki Genel sekmede belirtilen şablona göre oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c3def-114">The vendor account is created based on the template that is specified on the General tab in the Accounts payable parameters page.</span></span>  
4. <span data-ttu-id="c3def-115">Ad alanına tedarikçinin adını yazın.</span><span class="sxs-lookup"><span data-stu-id="c3def-115">In the Name field, type a name for the supplier.</span></span>
5. <span data-ttu-id="c3def-116">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c3def-116">Click OK.</span></span>
    * <span data-ttu-id="c3def-117">Satınalma siparişi şimdi tamamlanabilir ve başka bir sipariş gibi işlenebilir.</span><span class="sxs-lookup"><span data-stu-id="c3def-117">The purchase order can now be completed and processed like any other order.</span></span> <span data-ttu-id="c3def-118">Bunun yapılmasıyla ilgili özel karakterler bulunmamaktadır.</span><span class="sxs-lookup"><span data-stu-id="c3def-118">There are no special characteristics related to how this is done.</span></span> <span data-ttu-id="c3def-119">Fatura, hareket vade sonunu siparişle oluşturulmuş satıcı hesabı üzerinden dahil eder ve sonra ödeme işlenir.</span><span class="sxs-lookup"><span data-stu-id="c3def-119">The invoice will account a due transaction on the vendor account that was created with the order, and payment will then be processed.</span></span> <span data-ttu-id="c3def-120">Bu tamamlandığında, satıcı hesabı silinebilir.</span><span class="sxs-lookup"><span data-stu-id="c3def-120">When this is completed, the vendor account can be deleted.</span></span> <span data-ttu-id="c3def-121">Bu genellikle Borç hesapları departmanı tarafından yapılır.</span><span class="sxs-lookup"><span data-stu-id="c3def-121">This is typically done by the accounts payable department.</span></span>  


