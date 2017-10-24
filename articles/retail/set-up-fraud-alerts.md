---
title: "Sahtekarlık uyarıları ayarla"
description: "Bu konu, siparişler işlendiğinde, müşteri hizmetleri temsilcilerini sahte olması olası bilgilere karşı uyarmak için kuralların nasıl ayarlanacağını açıklar. Siparişleri otomatik olarak veya el ile beklemeye almak için kullanılacak belirli kodlar tanımlayabilirsiniz."
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
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 09d80015298c3d0219b6ffb290dc456990536a62
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-fraud-alerts"></a><span data-ttu-id="53272-104">Sahtekarlık uyarıları ayarla</span><span class="sxs-lookup"><span data-stu-id="53272-104">Set up fraud alerts</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="53272-105">Bu konu, siparişler işlendiğinde, müşteri hizmetleri temsilcilerini sahte olması olası bilgilere karşı uyarmak için kuralların nasıl ayarlanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="53272-105">This topic explains how to set up rules to alert customer service representatives of potentially fraudulent information when orders are processed.</span></span> <span data-ttu-id="53272-106">Siparişleri otomatik olarak veya el ile beklemeye almak için kullanılacak belirli kodlar tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="53272-106">You can define specific codes to use to automatically or manually put suspicious orders on hold.</span></span> 

<span data-ttu-id="53272-107">Dolandırıcılık denetimi kurallarını ayarlamadan ve kullanmadan önce sahtekarlık denetimini etkinleştirmeniz ve çağrı merkezi parametrelerinde temel dolandırıcılık değerlerini tanımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="53272-107">Before you set up and use fraud checking rules, you must enable fraud checking and define the basic fraud checking values in the call center parameters.</span></span> <span data-ttu-id="53272-108">İki tip sahtekarlık kuralı vardır:</span><span class="sxs-lookup"><span data-stu-id="53272-108">There are two types of fraud rules:</span></span>

-   <span data-ttu-id="53272-109">**Statik kuralları** kara listede bir telefon numarası gibi belirli bir değer kullanır.</span><span class="sxs-lookup"><span data-stu-id="53272-109">**Static rules** use a specific value, such as a phone number that has been blacklisted.</span></span>
-   <span data-ttu-id="53272-110">**Dinamik kuralları** değişkenler ve koşullardan oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="53272-110">**Dynamic rules** can be composed from variables and conditions.</span></span>

<span data-ttu-id="53272-111">Dinamik kuralı oluşturmadan önce kuralın kime uygulanacağını ve kuralın ne zaman uygulanacağını tanımlayan değişkenleri ve koşulları oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="53272-111">Before you create a dynamic rule, you must create the variables and conditions that define who the rule applies to and when the rule should be applied.</span></span> <span data-ttu-id="53272-112">Örneğin, müşteri 1202'in 1.000,00 veya üzerinde değerinde koyduğu her satış siparişinin müşteri ödemesi doğrulanıncaya kadar beklemeye konmasını gerektiren bir kural oluşturmak istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="53272-112">For example, you want to create a rule to require that any sales order that customer 1202 places that is worth 1,000.00 or more be put on hold until the customer payment can be verified.</span></span> <span data-ttu-id="53272-113">Bu durumda, müşteri 1202 ve sipariş toplamı 1.000,00 değişkenlerdir.</span><span class="sxs-lookup"><span data-stu-id="53272-113">In this case, the variables are customer 1202 and an order total of 1,000.00.</span></span> <span data-ttu-id="53272-114">Koşul, müşteri 1202 bir sipariş yaparsa ve toplam sipariş miktarı 1,000.00'e eşittir veya fazlaysa satış siparişi müşteri ödemesi doğrulanıncaya kadar beklemeye alınmalıdır.</span><span class="sxs-lookup"><span data-stu-id="53272-114">The condition specifies that if customer 1202 places an order, and the total amount of the order is equal to or more than 1,000.00, the sales order must be put on hold until the customer payment can be verified.</span></span>




