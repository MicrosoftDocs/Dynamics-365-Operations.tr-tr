---
title: Tek seferlik tedarikçi için satınalma siparişi oluşturma
description: Bu prosedür, size satınalma siparişinin tek seferlik bir tedarikçi için nasıl oluşturulacağını gösterir.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 76915772809d736cac9e8a9439d9e693a4490eec
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204919"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="a0c3c-103">Tek seferlik tedarikçi için satınalma siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="a0c3c-103">Create a purchase order for a one-time supplier</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a0c3c-104">Bu prosedür, size satınalma siparişinin tek seferlik bir tedarikçi için nasıl oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a0c3c-104">This procedure shows you how to create a purchase order for a one-time supplier.</span></span> <span data-ttu-id="a0c3c-105">Satıcı hesabını el ile oluşturmak yerine tedarikçi satınalma siparişi ile otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a0c3c-105">The supplier is created automatically with the purchase order, rather than having to create the vendor account manually.</span></span> <span data-ttu-id="a0c3c-106">Satınalma siparişleri genellikle bir satınalma temsilcisi tarafından oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a0c3c-106">Purchase orders are typically created by a purchasing agent.</span></span> <span data-ttu-id="a0c3c-107">Bu kılavuzda gösterilen örnek, demo veriler şirketi USMF'de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a0c3c-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="a0c3c-108">Tek seferlik satıcı hesabının Hesap borç parametreleri sayfasında ayarlanması bir önkoşuldur.</span><span class="sxs-lookup"><span data-stu-id="a0c3c-108">It is a prerequisite that a one-time vendor account has been set up in the Account payable parameters page.</span></span>


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="a0c3c-109">Tek seferlik tedarikçi için satınalma siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="a0c3c-109">Create a purchase order for a one-time supplier</span></span>
1. <span data-ttu-id="a0c3c-110">Tedarik ve kaynak atama > Sipariş emirleri > Tüm sipariş emirleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="a0c3c-110">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="a0c3c-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a0c3c-111">Click New.</span></span>
3. <span data-ttu-id="a0c3c-112">Tek seferlik tedarikçi alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a0c3c-112">Select Yes in the One-time supplier field.</span></span>
    * <span data-ttu-id="a0c3c-113">Bir satıcı hesabı otomatik olarak oluşturulur ve satınalma siparişine atanır.</span><span class="sxs-lookup"><span data-stu-id="a0c3c-113">A vendor account is automatically created and assigned to the purchase order.</span></span> <span data-ttu-id="a0c3c-114">Satıcı hesabı, Borç hesapları parametreleri sayfasındaki Genel sekmede belirtilen şablona göre oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a0c3c-114">The vendor account is created based on the template that is specified on the General tab in the Accounts payable parameters page.</span></span>  
4. <span data-ttu-id="a0c3c-115">Ad alanına tedarikçinin adını yazın.</span><span class="sxs-lookup"><span data-stu-id="a0c3c-115">In the Name field, type a name for the supplier.</span></span>
5. <span data-ttu-id="a0c3c-116">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a0c3c-116">Click OK.</span></span>
    * <span data-ttu-id="a0c3c-117">Satınalma siparişi şimdi tamamlanabilir ve başka bir sipariş gibi işlenebilir.</span><span class="sxs-lookup"><span data-stu-id="a0c3c-117">The purchase order can now be completed and processed like any other order.</span></span> <span data-ttu-id="a0c3c-118">Bunun yapılmasıyla ilgili özel karakterler bulunmamaktadır.</span><span class="sxs-lookup"><span data-stu-id="a0c3c-118">There are no special characteristics related to how this is done.</span></span> <span data-ttu-id="a0c3c-119">Fatura, hareket vade sonunu siparişle oluşturulmuş satıcı hesabı üzerinden dahil eder ve sonra ödeme işlenir.</span><span class="sxs-lookup"><span data-stu-id="a0c3c-119">The invoice will account a due transaction on the vendor account that was created with the order, and payment will then be processed.</span></span>

