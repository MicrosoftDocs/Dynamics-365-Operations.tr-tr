---
title: Varsayılan müşteri oluşturma
description: Bu konuda, Microsoft Dynamics 365 Commerce'te bir kanal oluşturulurken kullanılacak bir varsayılan müşterinin nasıl oluşturulacağı açıklanmaktadır.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ba1d10a897f349703737068d772423f7d0292944
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416340"
---
# <a name="create-a-default-customer"></a><span data-ttu-id="3a656-103">Varsayılan müşteri oluşturma</span><span class="sxs-lookup"><span data-stu-id="3a656-103">Create a default customer</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="3a656-104">Bu konuda, Microsoft Dynamics 365 Commerce'te bir kanal oluşturulurken kullanılacak bir varsayılan müşterinin nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="3a656-104">This topic describes how to create a default customer to use when creating a channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3a656-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="3a656-105">Overview</span></span>

<span data-ttu-id="3a656-106">Bir kanal oluştururken varsayılan bir müşteri sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3a656-106">When creating a channel, you will need to provide a default customer.</span></span> <span data-ttu-id="3a656-107">Müşteri grubu ve müşteri adres defteri oluşturulduktan sonra, varsayılan bir müşteri kolayca oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="3a656-107">A default customer can easily be created after first creating the customer group and customer address book.</span></span>

## <a name="create-a-customer-group"></a><span data-ttu-id="3a656-108">Müşteri grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="3a656-108">Create a customer group</span></span>

<span data-ttu-id="3a656-109">Henüz müşteri grupları yoksa bir müşteri grubu oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3a656-109">If no customer groups exist yet, you can create one.</span></span> <span data-ttu-id="3a656-110">Bunlar, örneğin, toptan satış, perakende, Internet, Çalışanlar gibi farklı müşteri gruplarını temsil eden gruplar olabilir.</span><span class="sxs-lookup"><span data-stu-id="3a656-110">Examples may be groups to represent different customer groups, such as wholesale, retail, Internet, Employees, etc.</span></span>

<span data-ttu-id="3a656-111">Müşteri grubu oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="3a656-111">To create a customer group, follow these steps.</span></span>

1. <span data-ttu-id="3a656-112">Gezinti bölmesinde **Modüller \> Perakende ve ticaret \> Müşteriler \> Müşteri grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="3a656-112">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> Customer groups**.</span></span>
1. <span data-ttu-id="3a656-113">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3a656-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="3a656-114">**Müşteri grubu** alanına bir müşteri grubu kodu girin.</span><span class="sxs-lookup"><span data-stu-id="3a656-114">In the **Customer group** box, enter a customer group ID.</span></span>
1. <span data-ttu-id="3a656-115">**Açıklama** kutusuna, uygun bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="3a656-115">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="3a656-116">**Ödeme koşulları** kutusuna, uygun bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="3a656-116">In the **Terms of payment** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="3a656-117">**Fatura vade tarihi ile ödeme tarihi arasındaki süre** kutusuna, uygun değer girin.</span><span class="sxs-lookup"><span data-stu-id="3a656-117">In the **Time between invoice due date and payment date** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="3a656-118">**Varsayılan vergi grubu** kutusuna, varsa bir vergi grubu girin.</span><span class="sxs-lookup"><span data-stu-id="3a656-118">In the **Default tax group** box, enter a tax group if applicable.</span></span>
1. <span data-ttu-id="3a656-119">**Fiyatlara satış vergisi dahildir** onay kutusunu (uygunsa) işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="3a656-119">Select the **Prices include sales tax** check box if applicable.</span></span>
1. <span data-ttu-id="3a656-120">**Varsayılan silme nedeni** kutusuna, varsa uygun bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="3a656-120">In the **Default write-off reason** box, enter an appropriate value, if applicable.</span></span>

<span data-ttu-id="3a656-121">Aşağıdaki resimde, yapılandırılmış birkaç müşteri grubu gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="3a656-121">The following image shows several configured customer groups.</span></span>

![Müşteri grupları](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a><span data-ttu-id="3a656-123">Müşteri adres defteri oluşturma</span><span class="sxs-lookup"><span data-stu-id="3a656-123">Create a customer address book</span></span>

<span data-ttu-id="3a656-124">Müşterinin bir adres defteriyle ilişkilendirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="3a656-124">A customer needs to be associated with an address book.</span></span> <span data-ttu-id="3a656-125">Henüz oluşturulmadıysa, bir tane oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3a656-125">If one has not yet been created, then you will need to create one.</span></span>

<span data-ttu-id="3a656-126">Bir müşteri adres defteri oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="3a656-126">To create a customer address book, follow these steps.</span></span>

1. <span data-ttu-id="3a656-127">Gezinti bölmesinde **Modüller \> Perakende ve ticaret \> Kanal kurulumu \> Adres Defterleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="3a656-127">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Address Books**.</span></span>
1. <span data-ttu-id="3a656-128">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3a656-128">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="3a656-129">**Ad** kutusuna bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="3a656-129">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="3a656-130">**Açıklama** kutusuna bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="3a656-130">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="3a656-131">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3a656-131">On the action pane, select **Save**.</span></span>

<span data-ttu-id="3a656-132">Aşağıdaki resimde örnek bir adres defteri gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="3a656-132">The following image shows an example address book.</span></span>

![Adres defteri](media/address-book.png)

## <a name="create-a-default-customer"></a><span data-ttu-id="3a656-134">Varsayılan müşteri oluşturma</span><span class="sxs-lookup"><span data-stu-id="3a656-134">Create a default customer</span></span>

<span data-ttu-id="3a656-135">Bir varsayılan müşteri oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="3a656-135">To create a default customer, follow these steps.</span></span>

1. <span data-ttu-id="3a656-136">Gezinti bölmesinde **Modüller \> Perakende ve ticaret \> Müşteriler \> Tüm müşteriler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="3a656-136">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="3a656-137">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3a656-137">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="3a656-138">**Tür** açılır listesinde "Kişi"yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3a656-138">In the **Type** drop-down list, select "Person".</span></span>
1. <span data-ttu-id="3a656-139">**Müşteri hesabı** açılır listesinde bir hesap numarası seçin veya girin (örneğin "100001").</span><span class="sxs-lookup"><span data-stu-id="3a656-139">In the **Customer account** drop-down list, select or enter an account number (for example, "100001").</span></span>
1. <span data-ttu-id="3a656-140">**Ad** açılır listesinde, bir ad seçin veya girin (örneğin "Varsayılan").</span><span class="sxs-lookup"><span data-stu-id="3a656-140">In the **First name** drop-down list, select or enter a name (for example, "Default").</span></span>
1. <span data-ttu-id="3a656-141">**İkinci ad** açılır listesinde, bir ad seçin veya girin (örneğin "Perakende").</span><span class="sxs-lookup"><span data-stu-id="3a656-141">In the **Middle name** drop-down list, select or enter a name (for example, "Retail").</span></span>
1. <span data-ttu-id="3a656-142">**Soyadı** açılır listesinde, bir ad seçin veya girin (örneğin "Müşteri").</span><span class="sxs-lookup"><span data-stu-id="3a656-142">In the **Last name** drop-down list, select or enter a name (for example, "Customer").</span></span>
1. <span data-ttu-id="3a656-143">**Para birimi** açılır listesinde, bir para birimi seçin veya girin (örneğin "USD").</span><span class="sxs-lookup"><span data-stu-id="3a656-143">In the **Currency** drop-down list, select or enter a currency (for example, "USD").</span></span>
1. <span data-ttu-id="3a656-144">**Para birimi** açılır listesinde, önceden oluşturulan müşteri grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="3a656-144">In the **Currency** drop-down list, select the customer group created previously.</span></span>
1. <span data-ttu-id="3a656-145">**Adres defterleri** açılır listesinde, varolan bir müşteri adres defterini seçin.</span><span class="sxs-lookup"><span data-stu-id="3a656-145">In the **Address books**  drop-down list, select an existing customer address book.</span></span>
1. <span data-ttu-id="3a656-146">Kaydetmek ve yeni müşterinin müşteri ayrıntıları ekranına dönmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3a656-146">Select **Save** to save and return to customer details screen for the new customer.</span></span>

> [!NOTE]
> <span data-ttu-id="3a656-147">Varsayılan müşteri için bir adres eklemek gerekmez.</span><span class="sxs-lookup"><span data-stu-id="3a656-147">It is not necessary to add an address for a default customer.</span></span>

<span data-ttu-id="3a656-148">Aşağıdaki resimde bir müşteri oluşturma örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="3a656-148">The following image shows an example of customer creation.</span></span>

![Varsayılan müşteri oluşturma](media/default-customer-creation.png)

<span data-ttu-id="3a656-150">Aşağıdaki resimde, bir varsayılan müşteri yapılandırması gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="3a656-150">The following image shows a default customer configuration.</span></span>

![Örnek müşteri yapılandırması](media/default-customer-configuration1.png)

<span data-ttu-id="3a656-152">Müşteri ayrıntıları ekranındaki varsayılan değerlerin çoğu kalabilir ancak iki değer değiştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="3a656-152">Most of the default values on the customer detials screen can remain, but two values should be changed.</span></span>

1. <span data-ttu-id="3a656-153">Müşteri ayrıntıları ekranında **Satış siparişi varsayılanları**'nı genişletin.</span><span class="sxs-lookup"><span data-stu-id="3a656-153">On the customer details screen, expand **Sales order defaults**.</span></span>
1. <span data-ttu-id="3a656-154">**Site** açılır listesinde, önceden yapılandırılmış bir siteyi seçin veya girin.</span><span class="sxs-lookup"><span data-stu-id="3a656-154">In the **Site** drop-down list, select or enter a pre-configured site.</span></span>
1. <span data-ttu-id="3a656-155">**Ambar** açılır listesinde, önceden yapılandırılmış bir ambarı seçin veya girin.</span><span class="sxs-lookup"><span data-stu-id="3a656-155">In the **Warehouse** drop-down list, and select or enter a pre-configured warehouse.</span></span>

<span data-ttu-id="3a656-156">Aşağıdaki resimde bir müşteri yapılandırma örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="3a656-156">The following image shows an example customer configuration.</span></span>

![Örnek müşteri yapılandırması](media/default-customer-configuration2.png)

## <a name="additional-resources"></a><span data-ttu-id="3a656-158">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="3a656-158">Additional resources</span></span>

[<span data-ttu-id="3a656-159">Kanallara genel bakış</span><span class="sxs-lookup"><span data-stu-id="3a656-159">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="3a656-160">Kanal kurulum önkoşulları</span><span class="sxs-lookup"><span data-stu-id="3a656-160">Channel setup prerequisites</span></span>](channels-prerequisites.md)
