---
title: Bir iade emrinde bir değişiklik yapılandırma ve işleme
description: Bu konuda, Dynamics 365 Commerce için bir iadede bir değişikliğin nasıl yapılandırılacağı açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 11/12/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 60d58e4194481c875c5ff3f08fc3f8e12a87caa0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972764"
---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a><span data-ttu-id="de8c8-103">Bir iade emrinde bir değişiklik yapılandırma ve işleme</span><span class="sxs-lookup"><span data-stu-id="de8c8-103">Configure and process an exchange on a return order</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="de8c8-104">Dynamics 365 Commerce uygulamasının önceki sürümlerinde, müşteri siparişlerine göre iadeler Genel Merkez'deki iade emri belgesi kullanılarak işlenmiştir.</span><span class="sxs-lookup"><span data-stu-id="de8c8-104">In previous versions of Dynamics 365 Commerce, returns against customer orders were processed by using the return order document in Headquarters.</span></span> <span data-ttu-id="de8c8-105">Ancak iade emri belgesi yalnızca iade edilen ürünleri işlemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="de8c8-105">However, the return order document can be used to process only products that are being returned.</span></span> <span data-ttu-id="de8c8-106">İade edilen ürünler, iade emri satırlarında bir eksi miktarla belirtilir.</span><span class="sxs-lookup"><span data-stu-id="de8c8-106">The returned products are indicated by a negative quantity on the return order lines.</span></span> <span data-ttu-id="de8c8-107">Bunun aksine, satışlar ise artı bir miktarla gösterilir.</span><span class="sxs-lookup"><span data-stu-id="de8c8-107">By contrast, sales are indicated by a positive quantity.</span></span> <span data-ttu-id="de8c8-108">Ancak iade emri belgesi artı miktarları desteklemez.</span><span class="sxs-lookup"><span data-stu-id="de8c8-108">However, the return order document doesn't support positive quantities.</span></span> <span data-ttu-id="de8c8-109">Bu kısıtlama nedeniyle, uygulamanın önceki sürümleri ürün değişikliklerinin iade emri belgesi kullanılarak yapıldığı senaryoları desteklememiştir.</span><span class="sxs-lookup"><span data-stu-id="de8c8-109">Because of this limitation, previous versions of the app didn't support scenarios where product exchanges are done by using the return order document.</span></span>

<span data-ttu-id="de8c8-110">Ancak, değişikliklerin iade emirlerinde yapıldığı senaryoları desteklemek için işlevler eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="de8c8-110">However, functionality has been added to support scenarios where exchanges are done on return orders.</span></span> <span data-ttu-id="de8c8-111">Commerce artık bu tür hareketleri işlemek için iade emri belgesi yerine satış siparişi belgesini kullanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="de8c8-111">Commerce now uses the sales order document instead of the return order document to process these types of transactions.</span></span>

## <a name="configure-commerce-to-support-exchanges-on-return-orders"></a><span data-ttu-id="de8c8-112">Commerce uygulamasını iade emirlerinde değişiklikleri destekleyecek şekilde yapılandırma</span><span class="sxs-lookup"><span data-stu-id="de8c8-112">Configure Commerce to support exchanges on return orders</span></span>

<span data-ttu-id="de8c8-113">Sistemi, iade emirlerinde değişiklikleri destekleyecek şekilde yapılandırmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="de8c8-113">Follow these steps to configure the system to support exchanges on return orders.</span></span>

1. <span data-ttu-id="de8c8-114">**Retail ve Commerce \> Genel merkez ayarı \> Parametreler \> Commerce parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="de8c8-114">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="de8c8-115">**Müşteri siparişleri** hızlı sekmesinde, **İade emirlerine satış siparişleri olarak işlem yap** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="de8c8-115">On the **Customer orders** FastTab, set the **Process return orders as sales orders** option to **Yes**.</span></span>
2. <span data-ttu-id="de8c8-116">**Genel yapılandırma dağıtım planı** işini (**1110**) çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="de8c8-116">Run the **Global configuration distribution schedule** job (**1110**).</span></span>

## <a name="make-an-exchange"></a><span data-ttu-id="de8c8-117">Değişiklik yapma</span><span class="sxs-lookup"><span data-stu-id="de8c8-117">Make an exchange</span></span>

<span data-ttu-id="de8c8-118">Sistem önceki bölümde açıklandığı gibi yapılandırıldıktan sonra, satış noktası (POS) kullanıcısının uygulamanın önceki sürümlerinde olduğu gibi bir iadeye işlem yapmak için yine bir satış siparişi veya satış faturası seçmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="de8c8-118">After the system is configured as described in the previous section, the point of sale (POS) user will still select a sales order or sales invoice to process a return, as in previous versions of the app.</span></span> <span data-ttu-id="de8c8-119">Ancak iade maddeler sepete eklendikten sonra, kullanıcı yeni satış satırlarını sepete ekleyebilir.</span><span class="sxs-lookup"><span data-stu-id="de8c8-119">However, after the return items are added to the cart, the user will be able to add new sales lines to the cart.</span></span>

<span data-ttu-id="de8c8-120">Kullanıcı, bu yeni satış satırları için bir müşteri sipariş satırını işlemek amacıyla gerekli olan tüm öznitelikleri tanımlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="de8c8-120">For these new sales lines, the user must define all the attributes that are required in order to process a customer order line.</span></span> <span data-ttu-id="de8c8-121">Bu öznitelikler, teslimat yöntemini ve karşılama konumunu içerir.</span><span class="sxs-lookup"><span data-stu-id="de8c8-121">These attributes include the delivery method and fulfillment location.</span></span> <span data-ttu-id="de8c8-122">Hareket için yapılması gereken ödeme iade emri satırları ile satış siparişi satırlarının net değeri olacaktır.</span><span class="sxs-lookup"><span data-stu-id="de8c8-122">The payment that is due for the transaction will be a net of the return order lines and sales order lines.</span></span> <span data-ttu-id="de8c8-123">Hareketin ödemesi yapıldıktan sonra, iade emri Genel Merkez'de satış siparişi belgesi olarak deftere nakledilir ve sistem, iade satırlarını derhal faturalandırır.</span><span class="sxs-lookup"><span data-stu-id="de8c8-123">When payment is tendered for the transaction, the return order will be posted as a sales order document in Headquarters, and the system will immediately invoice the return lines.</span></span>

<span data-ttu-id="de8c8-124">Sepet için çeşitli tutarlara yönelik daha iyi bir görüş sağlamak üzere, sepete üç yeni tutar alanı eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="de8c8-124">To provide better visibility into the various amounts for the cart, three new amount fields have been added to the cart.</span></span> <span data-ttu-id="de8c8-125">Bu yeni alanların POS kullanıcı arabiriminde kullanılabilmesini sağlamak için ekran tasarımcısını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="de8c8-125">You can use the screen designer to make these new fields available in the POS user interface (UI).</span></span>

- <span data-ttu-id="de8c8-126">**Uygulanan havale**: Kullanıcı bir müşteri siparişi teslim alma hareketi gerçekleştirdiğinde bir işlemde uygulanan havale tutarı.</span><span class="sxs-lookup"><span data-stu-id="de8c8-126">**Deposit applied** – The deposit amount that is applied on a transaction when the user does a customer order pickup.</span></span> <span data-ttu-id="de8c8-127">Havale geçersiz kılma işlemi yoksa ve yüzde 10 havale yapılandırıldıysa bu alandaki tutar müşteri siparişinin toplam tutarının yüzde 90'ıdır.</span><span class="sxs-lookup"><span data-stu-id="de8c8-127">If there is no deposit override, and a 10-percent deposit is configured, the amount in this field is 90 percent of the total amount of the customer order.</span></span>
- <span data-ttu-id="de8c8-128">**Gerçekleşen tutar**: Müşteri siparişi oluşturulduğunda veya düzenlendiğinde ya da bir müşteri siparişi değişikliği sırasında teslimat şeklinin **Gerçekleştirme** olarak ayarlandığı satırların toplam tutarı.</span><span class="sxs-lookup"><span data-stu-id="de8c8-128">**Carry out amount** – The total amount for lines where the delivery mode was set to **Carry out** when the customer order was created or edited, or during a customer order exchange.</span></span> <span data-ttu-id="de8c8-129">Bu alandaki tutar, vergileri ve masrafları içerir.</span><span class="sxs-lookup"><span data-stu-id="de8c8-129">The amount in this field includes taxes and charges.</span></span>
- <span data-ttu-id="de8c8-130">**İade tutarı**: Müşteri siparişi değişikliği sırasında eksi miktarlar içeren satırların toplam tutarı.</span><span class="sxs-lookup"><span data-stu-id="de8c8-130">**Return amount** – The total amount for lines that have negative quantities during the customer order exchange.</span></span> <span data-ttu-id="de8c8-131">Bu alandaki tutar, vergileri ve masrafları içerir.</span><span class="sxs-lookup"><span data-stu-id="de8c8-131">The amount in this field includes taxes and charges.</span></span>
