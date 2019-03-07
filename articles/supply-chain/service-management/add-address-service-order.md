---
title: Servis siparişine adres ekleme
description: Bu konu bir servis siparişine nasıl müşteri adresi ekleneceğini açıklar.
author: ShylaThompson
manager: AnnBe
ms.date: 05/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 58188be6f82b6587011188379e5370b81f8fd114
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "311922"
---
# <a name="add-an-address-to-a-service-order"></a><span data-ttu-id="d3472-103">Servis siparişine adres ekleme</span><span class="sxs-lookup"><span data-stu-id="d3472-103">Add an address to a service order</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d3472-104">Bu konu bir servis siparişine nasıl müşteri adresi ekleneceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="d3472-104">This topic describes how to add a customer address to a service order.</span></span> <span data-ttu-id="d3472-105">Bir servis siparişi oluşturduğunuzda, adres bilgileri servis siparişinin iliştirildiği projeden transfer edilir.</span><span class="sxs-lookup"><span data-stu-id="d3472-105">When you create a service order, the address information is transferred from the project that the service order is attached to.</span></span> <span data-ttu-id="d3472-106">Ancak müşteriler, satıcılar, tesisler, ambarlar, servis siparişleri ve projeler için Microsoft Dynamics AX'e önceden girilmiş adreslerden alternatif bir konum seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d3472-106">However, you can select an alternative location from addresses that are already entered in Microsoft Dynamics AX for customers, vendors, sites, warehouses, service orders, and projects.</span></span>

<span data-ttu-id="d3472-107">Yeni bir adres de oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d3472-107">You can also create a new address.</span></span> <span data-ttu-id="d3472-108">Varsayılan olarak, yeni adres projeye transfer edilir.</span><span class="sxs-lookup"><span data-stu-id="d3472-108">By default, the new address is transferred to the project.</span></span> <span data-ttu-id="d3472-109">Ancak, yeni adresin yalnızca hizmetin bu örneği için geçerli olduğunu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d3472-109">However, you can specify that the new address is only relevant for this instance of the service.</span></span> <span data-ttu-id="d3472-110">Bunu yaparsanız, yeni adres projeye transfer edilmez.</span><span class="sxs-lookup"><span data-stu-id="d3472-110">If you do, the new address is not transferred to the project.</span></span>

## <a name="create-a-customer-address-for-a-service-order"></a><span data-ttu-id="d3472-111">Servis siparişi için bir müşteri adresi oluşturma</span><span class="sxs-lookup"><span data-stu-id="d3472-111">Create a customer address for a service order</span></span>

<span data-ttu-id="d3472-112">Servis siparişine bir adres eklemek için bu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="d3472-112">To add an address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="d3472-113">**Servis yönetimi** \> **Ortak** \> **Servis siparişleri** \> **Servis siparişleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d3472-113">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="d3472-114">Bir adres oluşturmak istediğiniz servis siparişini açın.</span><span class="sxs-lookup"><span data-stu-id="d3472-114">Open the service order that you want to create an address for.</span></span>

3.  <span data-ttu-id="d3472-115">**Eylem Bölmesinde** **Düzenle**'ye ve ardından **Başlık görünümü**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d3472-115">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="d3472-116">**Adres** hızlı sekmesinde **Adres ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d3472-116">On the **Address** FastTab, click **Add address**.</span></span>

5.  <span data-ttu-id="d3472-117">**Yeni adres** formuna, adres için benzersiz bir ad girin ve kalan alanları doldurun.</span><span class="sxs-lookup"><span data-stu-id="d3472-117">In the **New address** form, enter a unique name for the address and complete the remaining fields.</span></span> 
    

    > [!WARNING]
    > <P><span data-ttu-id="d3472-118">Varolan bir adresle aynı adı girerseniz, kalan alanlara girdiğiniz bilgiler varolan adres bilgilerini geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="d3472-118">If you enter the same name as an existing address, the information that you enter in the remaining fields will overwrite information for the existing address.</span></span></P>


6.  <span data-ttu-id="d3472-119">Yeni adresi servis siparişine kopyalamak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d3472-119">Click **OK** to copy the new address to your service order.</span></span>

## <a name="specify-an-alternative-address-on-a-service-order"></a><span data-ttu-id="d3472-120">Bir servis sipariş siparişinde alternatif bir adres belirtme</span><span class="sxs-lookup"><span data-stu-id="d3472-120">Specify an alternative address on a service order</span></span>

<span data-ttu-id="d3472-121">Servis siparişine alternatif bir adres eklemek için bu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="d3472-121">To add an alternative address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="d3472-122">**Servis yönetimi** \> **Ortak** \> **Servis siparişleri** \> **Servis siparişleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d3472-122">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="d3472-123">Alternatif adres girmek istediğiniz servis siparişini açın.</span><span class="sxs-lookup"><span data-stu-id="d3472-123">Open the service order that you want to enter an alternative address for.</span></span>

3.  <span data-ttu-id="d3472-124">**Eylem Bölmesinde** **Düzenle**'ye ve ardından **Başlık görünümü**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d3472-124">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="d3472-125">**Adres** hızlı sekmesinde **Diğer adresler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d3472-125">On the **Address** FastTab, click **Other address**.</span></span>

5.  <span data-ttu-id="d3472-126">**Adres seçimi** formunda**Kayıt türü** alanında **Servis siparişleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="d3472-126">In the **Address selection** form, in the **Record type** field, select **Service orders**.</span></span>

6.  <span data-ttu-id="d3472-127">Bir adres seçin ve servis siparişine kopyalamak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d3472-127">Select an address, and then click **OK** to copy it to your service order.</span></span>


  


