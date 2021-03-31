---
title: Servis siparişine adres ekleme
description: Bu konu bir servis siparişine nasıl müşteri adresi ekleneceğini açıklar.
author: ShylaThompson
manager: tfehr
ms.date: 05/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7b9c6a410acbfebb3a83e753c422dd87dbf52566
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205869"
---
# <a name="add-an-address-to-a-service-order"></a><span data-ttu-id="19ee9-103">Servis siparişine adres ekleme</span><span class="sxs-lookup"><span data-stu-id="19ee9-103">Add an address to a service order</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="19ee9-104">Bu konu bir servis siparişine nasıl müşteri adresi ekleneceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="19ee9-104">This topic describes how to add a customer address to a service order.</span></span> <span data-ttu-id="19ee9-105">Bir servis siparişi oluşturduğunuzda, adres bilgileri servis siparişinin iliştirildiği projeden transfer edilir.</span><span class="sxs-lookup"><span data-stu-id="19ee9-105">When you create a service order, the address information is transferred from the project that the service order is attached to.</span></span> <span data-ttu-id="19ee9-106">Ancak müşteriler, satıcılar, tesisler, ambarlar, servis siparişleri ve projeler için Microsoft Dynamics AX'e önceden girilmiş adreslerden alternatif bir konum seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="19ee9-106">However, you can select an alternative location from addresses that are already entered in Microsoft Dynamics AX for customers, vendors, sites, warehouses, service orders, and projects.</span></span>

<span data-ttu-id="19ee9-107">Yeni bir adres de oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="19ee9-107">You can also create a new address.</span></span> <span data-ttu-id="19ee9-108">Varsayılan olarak, yeni adres projeye transfer edilir.</span><span class="sxs-lookup"><span data-stu-id="19ee9-108">By default, the new address is transferred to the project.</span></span> <span data-ttu-id="19ee9-109">Ancak, yeni adresin yalnızca hizmetin bu örneği için geçerli olduğunu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="19ee9-109">However, you can specify that the new address is only relevant for this instance of the service.</span></span> <span data-ttu-id="19ee9-110">Bunu yaparsanız, yeni adres projeye transfer edilmez.</span><span class="sxs-lookup"><span data-stu-id="19ee9-110">If you do, the new address is not transferred to the project.</span></span>

## <a name="create-a-customer-address-for-a-service-order"></a><span data-ttu-id="19ee9-111">Servis siparişi için bir müşteri adresi oluşturma</span><span class="sxs-lookup"><span data-stu-id="19ee9-111">Create a customer address for a service order</span></span>

<span data-ttu-id="19ee9-112">Servis siparişine bir adres eklemek için bu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="19ee9-112">To add an address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="19ee9-113">**Servis yönetimi** \> **Ortak** \> **Servis siparişleri** \> **Servis siparişleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="19ee9-113">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="19ee9-114">Bir adres oluşturmak istediğiniz servis siparişini açın.</span><span class="sxs-lookup"><span data-stu-id="19ee9-114">Open the service order that you want to create an address for.</span></span>

3.  <span data-ttu-id="19ee9-115">**Eylem Bölmesinde** **Düzenle**'ye ve ardından **Başlık görünümü**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="19ee9-115">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="19ee9-116">**Adres** hızlı sekmesinde **Adres ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="19ee9-116">On the **Address** FastTab, click **Add address**.</span></span>

5.  <span data-ttu-id="19ee9-117">**Yeni adres** formuna, adres için benzersiz bir ad girin ve kalan alanları doldurun.</span><span class="sxs-lookup"><span data-stu-id="19ee9-117">In the **New address** form, enter a unique name for the address and complete the remaining fields.</span></span> 
    

    > [!WARNING]
    > <P><span data-ttu-id="19ee9-118">Varolan bir adresle aynı adı girerseniz, kalan alanlara girdiğiniz bilgiler varolan adres bilgilerini geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="19ee9-118">If you enter the same name as an existing address, the information that you enter in the remaining fields will overwrite information for the existing address.</span></span></P>


6.  <span data-ttu-id="19ee9-119">Yeni adresi servis siparişine kopyalamak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="19ee9-119">Click **OK** to copy the new address to your service order.</span></span>

## <a name="specify-an-alternative-address-on-a-service-order"></a><span data-ttu-id="19ee9-120">Bir servis sipariş siparişinde alternatif bir adres belirtme</span><span class="sxs-lookup"><span data-stu-id="19ee9-120">Specify an alternative address on a service order</span></span>

<span data-ttu-id="19ee9-121">Servis siparişine alternatif bir adres eklemek için bu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="19ee9-121">To add an alternative address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="19ee9-122">**Servis yönetimi** \> **Ortak** \> **Servis siparişleri** \> **Servis siparişleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="19ee9-122">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="19ee9-123">Alternatif adres girmek istediğiniz servis siparişini açın.</span><span class="sxs-lookup"><span data-stu-id="19ee9-123">Open the service order that you want to enter an alternative address for.</span></span>

3.  <span data-ttu-id="19ee9-124">**Eylem Bölmesinde** **Düzenle**'ye ve ardından **Başlık görünümü**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="19ee9-124">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="19ee9-125">**Adres** hızlı sekmesinde **Diğer adresler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="19ee9-125">On the **Address** FastTab, click **Other address**.</span></span>

5.  <span data-ttu-id="19ee9-126">**Adres seçimi** formunda **Kayıt türü** alanında **Servis siparişleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="19ee9-126">In the **Address selection** form, in the **Record type** field, select **Service orders**.</span></span>

6.  <span data-ttu-id="19ee9-127">Bir adres seçin ve servis siparişine kopyalamak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="19ee9-127">Select an address, and then click **OK** to copy it to your service order.</span></span>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]