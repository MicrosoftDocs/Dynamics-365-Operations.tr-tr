---
title: "Sipariş tutmaları"
description: "Bu konu Dynamics 365 for Retail kullanarak siparişlerdeki tutmaları açıklar."
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
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8b4c8ecbef1dc667d3b60411a53f0c63686529c2
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="order-holds"></a><span data-ttu-id="7bb74-103">Sipariş tutmaları</span><span class="sxs-lookup"><span data-stu-id="7bb74-103">Order holds</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="7bb74-104">Bu konu Dynamics 365 for Retail kullanarak siparişlerdeki tutmaları açıklar.</span><span class="sxs-lookup"><span data-stu-id="7bb74-104">This topic describes holds on orders using Dynamics 365 for Retail.</span></span>

<span data-ttu-id="7bb74-105">Sipariş çeşitli nedenlerle bekletmeye alınabilir.</span><span class="sxs-lookup"><span data-stu-id="7bb74-105">An order can be put on hold for various reasons.</span></span> <span data-ttu-id="7bb74-106">Örneğin, müşteri adresi veya ödeme yöntemi doğrulanıncaya kadar veya bir yönetici müşterinin kredi limiti gözden geçirene kadar siparişi beklemeye alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7bb74-106">For example, you might put an order on hold until the customer address or payment method can be verified, or until a manager can review the customer’s credit limit.</span></span> <span data-ttu-id="7bb74-107">Satış işlemi sırasında satış siparişlerinin beklenmeye alınması gereken zamanlar vardı.</span><span class="sxs-lookup"><span data-stu-id="7bb74-107">During the sales process, there are times when sales orders must be put on hold.</span></span> <span data-ttu-id="7bb74-108">Örneğin, bir satış siparişi, Müşteri ödeme ile ilgili sorunlar nedeniyle şüpheli dolandırıcılık nedeniyle veya bir yöneticinin sipariş incelemesi gerektiğinde beklemeye alınabilir.</span><span class="sxs-lookup"><span data-stu-id="7bb74-108">For example, a sales order might be put on hold because of issues with a customer payment, because of suspected fraud, or because a manager must review the order.</span></span> <span data-ttu-id="7bb74-109">Bir satış siparişi beklemeye alındığında, bir sipariş tutma kodu satış siparişine tutma nedenini belirtmek için atanır.</span><span class="sxs-lookup"><span data-stu-id="7bb74-109">When a sales order is put on hold, an order hold code is assigned to the sales order to indicate the reason for the hold.</span></span> <span data-ttu-id="7bb74-110">Satış siparişi tutma kodları **Satış ve pazarlama** &gt; **Kurulum** &gt; **Satış siparişleri** &gt; **Sipariş tutma kodları**'nda yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="7bb74-110">Sales order hold codes are configured at **Sales and marketing** &gt; **Setup** &gt; **Sales orders** &gt; **Order holds codes**.</span></span> <span data-ttu-id="7bb74-111">Bir satış siparişi oluşturma zamanında veya sonra el ile beklemeye alınabilir.</span><span class="sxs-lookup"><span data-stu-id="7bb74-111">A sales order can be put on hold manually at the time of order creation or later.</span></span> <span data-ttu-id="7bb74-112">Ayrıca, sipariş otomatik olarak, dolandırıcılık kurallarına göre beklemeye alınabilir.</span><span class="sxs-lookup"><span data-stu-id="7bb74-112">Additionally, an order can be put on hold automatically, based on fraud rules.</span></span> <span data-ttu-id="7bb74-113">Bir satış siparişi beklemedeyken bilgilerle güncelleştirmeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="7bb74-113">While a sales order is on hold, you might have to update it with more information.</span></span> <span data-ttu-id="7bb74-114">Alternatif olarak, üzerinde çalışmaya devam ederken satış siparişini denetlemek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7bb74-114">Alternatively, you might want to check out the sales order as you continue to work on it.</span></span> <span data-ttu-id="7bb74-115">Bir satış siparişi denetleyebilirsiniz, yeniden kaydedebilirsiniz ve hatta sipariş bekletme çalışma ekranını kullanarak başka bir kullanıcının denetlemesini geçersiz kılabilirsiniz (**Perakende** &gt; **Müşteriler** &gt; **Sipariş tutmaları**).</span><span class="sxs-lookup"><span data-stu-id="7bb74-115">You can check out a sales order, check it back in, and even override the checkout of another user by using the order hold workbench (**Retail** &gt; **Customers** &gt; **Order holds**).</span></span> <span data-ttu-id="7bb74-116">Siparişin tamamlanması hazır olduğunda, sipariş işlemini tamamlamadan önce tutma kaldırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7bb74-116">When an order is ready to be completed, you must remove the hold before you can complete the order process.</span></span>




