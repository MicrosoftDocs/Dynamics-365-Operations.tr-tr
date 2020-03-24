---
title: Müşteri kredi yönetimi
description: Müşteri kredi yönetimi, oluşturduğunuz kredi kurallarına göre kredi limitlerini yönetmenizi ve deftere nakil işlemi aracılığıyla satış siparişlerinin akışını denetlemenizi sağlar.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1e7d3325587d7cfc876e8f8c7b9207d44046ccd4
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124289"
---
# <a name="customer-credit-management-overview"></a><span data-ttu-id="a5ece-103">Müşteri kredi yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="a5ece-103">Customer credit management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a5ece-104">Müşteri kredi yönetimi, oluşturduğunuz kredi kurallarına göre kredi limitlerini yönetmenizi ve deftere nakil işlemi aracılığıyla satış siparişlerinin akışını denetlemenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="a5ece-104">Customer credit management allows you to manage credit limits and control the flow of sales orders through the posting process based on credit rules that you create.</span></span> 

<span data-ttu-id="a5ece-105">Kredi yönetimini kullanma işlemi aşağıdaki adımlardan bazılarını veya tümünü içerebilir:</span><span class="sxs-lookup"><span data-stu-id="a5ece-105">The process for using credit management can include some or all of the following steps:</span></span>
- <span data-ttu-id="a5ece-106">Müşterileri kredi tutarları hakkında ek bilgiler sağlamayan kredi öznitelikleriyle güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="a5ece-106">Update customers with credit attributes that provide additional information about their credit worthiness</span></span> 
- <span data-ttu-id="a5ece-107">Kredi limiti ayarlamalarını kullanarak müşteriler için kredi limitleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="a5ece-107">Create credit limits for customers using credit limit adjustments</span></span>
- <span data-ttu-id="a5ece-108">İş gereksinimlerine göre kredi limitini geçici olarak artırmak veya azaltmak istediğinizde Kredi limiti ayarlamalarını kullanarak müşteriler için geçici kredi limitleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="a5ece-108">Create temporary credit limits for customers using credit limit adjustments when you want to increase or decrease their credit limit temporarily based on business needs</span></span>
- <span data-ttu-id="a5ece-109">Kredi limitini etkileyebilen bilgiler (sigorta ve garantiler hakkındaki bilgiler vb.) ekleme</span><span class="sxs-lookup"><span data-stu-id="a5ece-109">Add additional information that can affect the credit limit such as insurance and guarantees</span></span>
- <span data-ttu-id="a5ece-110">Müşterileri tek bir kredi limitini paylaşabilecekleri şekilde birbirine bağlayan müşteri kredi grupları oluşturma</span><span class="sxs-lookup"><span data-stu-id="a5ece-110">Create customer credit groups that link customers together so they can share a single credit limit</span></span>
- <span data-ttu-id="a5ece-111">Müşterilere risk puanları atama ve daha sonra kredi limiti ayarlamalarıyla bu müşteriler için otomatik olarak kredi limitleri oluşturmada bu puanları kullanma</span><span class="sxs-lookup"><span data-stu-id="a5ece-111">Assign risk scores to customers and then use those scores to automatically generate credit limits for customers using credit limit adjustments</span></span>
- <span data-ttu-id="a5ece-112">Risk, ödeme koşulları, kredi limitleri, vadesi geçmiş tutarlar ve kullanılmış kredi limiti yüzdesi gibi faktörlere bağlı olarak bir veya daha fazla deftere nakil işlemi sırasında siparişi beklemeye alacak durdurma kuralları oluşturma</span><span class="sxs-lookup"><span data-stu-id="a5ece-112">Create blocking rules that will place an order on hold during one or more posting processes based on factors such as risk, payment terms, credit limits, overdue amounts, and percentage of credit limit used</span></span>
- <span data-ttu-id="a5ece-113">Beklemedeki satış siparişlerinin listesini yönetin, bekletme nedenlerini inceleme ve sorunları çözme</span><span class="sxs-lookup"><span data-stu-id="a5ece-113">Manage a list of sales orders that are on hold, review the reasons for the hold, and mitigate the issues</span></span>
- <span data-ttu-id="a5ece-114">Satış siparişlerini deftere nakil işlemi üzerinden devam edecek şekilde serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="a5ece-114">Release sales orders and allow it to continue through the posting process</span></span>
- <span data-ttu-id="a5ece-115">Kredi limiti değişikliklerinin ve satış siparişi serbest bırakma işlemlerinin onayını yönetmek için bir iş akışı ayarlama</span><span class="sxs-lookup"><span data-stu-id="a5ece-115">Set up workflow to manage the approval of credit limit changes and sales order releases</span></span>


<a name="additional-resources"></a><span data-ttu-id="a5ece-116">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="a5ece-116">Additional resources</span></span>
--------
[<span data-ttu-id="a5ece-117">Müşteri kredi yönetimi parametreleri kurulumu</span><span class="sxs-lookup"><span data-stu-id="a5ece-117">Customer credit management parameters setup</span></span>](./cm-credit-mgmt-setup.md)

[<span data-ttu-id="a5ece-118">Müşteri kredi yönetimi kurulum bilgileri</span><span class="sxs-lookup"><span data-stu-id="a5ece-118">Customer credit management setup information</span></span>](./cm-setup-information.md)

[<span data-ttu-id="a5ece-119">Müşteri için alacak yönetimi bilgileri ekleme</span><span class="sxs-lookup"><span data-stu-id="a5ece-119">Add credit management information for a customer</span></span>](./cm-add-credit-mgmt-information-customer.md)

[<span data-ttu-id="a5ece-120">Müşteri alacak grupları</span><span class="sxs-lookup"><span data-stu-id="a5ece-120">Customer credit groups</span></span>](./cm-customer-credit-groups.md)

[<span data-ttu-id="a5ece-121">Müşteri kredi limiti ayarlamaları</span><span class="sxs-lookup"><span data-stu-id="a5ece-121">Customer credit limit adjustments</span></span>](./cm-credit-limit-adjustments.md)

[<span data-ttu-id="a5ece-122">Satış siparişleri için askıda krediler</span><span class="sxs-lookup"><span data-stu-id="a5ece-122">Credit holds for sales orders</span></span>](./cm-sales-order-credit-holds.md)

[<span data-ttu-id="a5ece-123">Müşteri kredi yönetimi periyodik görevleri</span><span class="sxs-lookup"><span data-stu-id="a5ece-123">Customer credit management periodic tasks</span></span>](./cm-periodic-tasks.md)


