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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: f988732549ce82919f02c87b320623d8d4218735
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477912"
---
# <a name="create-a-default-customer"></a><span data-ttu-id="d5522-103">Varsayılan müşteri oluşturma</span><span class="sxs-lookup"><span data-stu-id="d5522-103">Create a default customer</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d5522-104">Bu konuda, Microsoft Dynamics 365 Commerce'te bir kanal oluşturulurken kullanılacak bir varsayılan müşterinin nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d5522-104">This topic describes how to create a default customer to use when creating a channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d5522-105">Bir kanal oluştururken varsayılan bir müşteri sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d5522-105">When creating a channel, you will need to provide a default customer.</span></span> <span data-ttu-id="d5522-106">Müşteri grubu ve müşteri adres defteri oluşturulduktan sonra, varsayılan bir müşteri kolayca oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="d5522-106">A default customer can easily be created after first creating the customer group and customer address book.</span></span>

## <a name="create-a-customer-group"></a><span data-ttu-id="d5522-107">Müşteri grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="d5522-107">Create a customer group</span></span>

<span data-ttu-id="d5522-108">Henüz müşteri grupları yoksa bir müşteri grubu oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d5522-108">If no customer groups exist yet, you can create one.</span></span> <span data-ttu-id="d5522-109">Bunlar, örneğin, toptan satış, perakende, Internet, Çalışanlar gibi farklı müşteri gruplarını temsil eden gruplar olabilir.</span><span class="sxs-lookup"><span data-stu-id="d5522-109">Examples may be groups to represent different customer groups, such as wholesale, retail, Internet, Employees, etc.</span></span>

<span data-ttu-id="d5522-110">Müşteri grubu oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="d5522-110">To create a customer group, follow these steps.</span></span>

1. <span data-ttu-id="d5522-111">Gezinti bölmesinde **Modüller \> Perakende ve ticaret \> Müşteriler \> Müşteri grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="d5522-111">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> Customer groups**.</span></span>
1. <span data-ttu-id="d5522-112">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d5522-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d5522-113">**Müşteri grubu** alanına bir müşteri grubu kodu girin.</span><span class="sxs-lookup"><span data-stu-id="d5522-113">In the **Customer group** box, enter a customer group ID.</span></span>
1. <span data-ttu-id="d5522-114">**Açıklama** kutusuna, uygun bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="d5522-114">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="d5522-115">**Ödeme koşulları** kutusuna, uygun bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d5522-115">In the **Terms of payment** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="d5522-116">**Fatura vade tarihi ile ödeme tarihi arasındaki süre** kutusuna, uygun değer girin.</span><span class="sxs-lookup"><span data-stu-id="d5522-116">In the **Time between invoice due date and payment date** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="d5522-117">**Varsayılan vergi grubu** kutusuna, varsa bir vergi grubu girin.</span><span class="sxs-lookup"><span data-stu-id="d5522-117">In the **Default tax group** box, enter a tax group if applicable.</span></span>
1. <span data-ttu-id="d5522-118">**Fiyatlara satış vergisi dahildir** onay kutusunu (uygunsa) işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="d5522-118">Select the **Prices include sales tax** check box if applicable.</span></span>
1. <span data-ttu-id="d5522-119">**Varsayılan silme nedeni** kutusuna, varsa uygun bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d5522-119">In the **Default write-off reason** box, enter an appropriate value, if applicable.</span></span>

<span data-ttu-id="d5522-120">Aşağıdaki resimde, yapılandırılmış birkaç müşteri grubu gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="d5522-120">The following image shows several configured customer groups.</span></span>

![Müşteri grupları](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a><span data-ttu-id="d5522-122">Müşteri adres defteri oluşturma</span><span class="sxs-lookup"><span data-stu-id="d5522-122">Create a customer address book</span></span>

<span data-ttu-id="d5522-123">Müşterinin bir adres defteriyle ilişkilendirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="d5522-123">A customer needs to be associated with an address book.</span></span> <span data-ttu-id="d5522-124">Henüz oluşturulmadıysa, bir tane oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d5522-124">If one has not yet been created, then you will need to create one.</span></span>

<span data-ttu-id="d5522-125">Bir müşteri adres defteri oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="d5522-125">To create a customer address book, follow these steps.</span></span>

1. <span data-ttu-id="d5522-126">Gezinti bölmesinde **Modüller \> Perakende ve ticaret \> Kanal kurulumu \> Adres Defterleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="d5522-126">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Address Books**.</span></span>
1. <span data-ttu-id="d5522-127">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d5522-127">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d5522-128">**Ad** kutusuna bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="d5522-128">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="d5522-129">**Açıklama** kutusuna bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="d5522-129">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="d5522-130">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d5522-130">On the action pane, select **Save**.</span></span>

<span data-ttu-id="d5522-131">Aşağıdaki resimde örnek bir adres defteri gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="d5522-131">The following image shows an example address book.</span></span>

![Adres defteri](media/address-book.png)

## <a name="create-a-default-customer"></a><span data-ttu-id="d5522-133">Varsayılan müşteri oluşturma</span><span class="sxs-lookup"><span data-stu-id="d5522-133">Create a default customer</span></span>

<span data-ttu-id="d5522-134">Bir varsayılan müşteri oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="d5522-134">To create a default customer, follow these steps.</span></span>

1. <span data-ttu-id="d5522-135">Gezinti bölmesinde **Modüller \> Perakende ve ticaret \> Müşteriler \> Tüm müşteriler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="d5522-135">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="d5522-136">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d5522-136">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d5522-137">**Tür** açılır listesinde "Kişi"yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d5522-137">In the **Type** drop-down list, select "Person".</span></span>
1. <span data-ttu-id="d5522-138">**Müşteri hesabı** açılır listesinde bir hesap numarası seçin veya girin (örneğin "100001").</span><span class="sxs-lookup"><span data-stu-id="d5522-138">In the **Customer account** drop-down list, select or enter an account number (for example, "100001").</span></span>
1. <span data-ttu-id="d5522-139">**Ad** açılır listesinde, bir ad seçin veya girin (örneğin "Varsayılan").</span><span class="sxs-lookup"><span data-stu-id="d5522-139">In the **First name** drop-down list, select or enter a name (for example, "Default").</span></span>
1. <span data-ttu-id="d5522-140">**İkinci ad** açılır listesinde, bir ad seçin veya girin (örneğin "Perakende").</span><span class="sxs-lookup"><span data-stu-id="d5522-140">In the **Middle name** drop-down list, select or enter a name (for example, "Retail").</span></span>
1. <span data-ttu-id="d5522-141">**Soyadı** açılır listesinde, bir ad seçin veya girin (örneğin "Müşteri").</span><span class="sxs-lookup"><span data-stu-id="d5522-141">In the **Last name** drop-down list, select or enter a name (for example, "Customer").</span></span>
1. <span data-ttu-id="d5522-142">**Para birimi** açılır listesinde, bir para birimi seçin veya girin (örneğin "USD").</span><span class="sxs-lookup"><span data-stu-id="d5522-142">In the **Currency** drop-down list, select or enter a currency (for example, "USD").</span></span>
1. <span data-ttu-id="d5522-143">**Para birimi** açılır listesinde, önceden oluşturulan müşteri grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="d5522-143">In the **Currency** drop-down list, select the customer group created previously.</span></span>
1. <span data-ttu-id="d5522-144">**Adres defterleri** açılır listesinde, varolan bir müşteri adres defterini seçin.</span><span class="sxs-lookup"><span data-stu-id="d5522-144">In the **Address books**  drop-down list, select an existing customer address book.</span></span>
1. <span data-ttu-id="d5522-145">Kaydetmek ve yeni müşterinin müşteri ayrıntıları ekranına dönmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d5522-145">Select **Save** to save and return to customer details screen for the new customer.</span></span>

> [!NOTE]
> <span data-ttu-id="d5522-146">Varsayılan müşteri için bir adres eklemek gerekmez.</span><span class="sxs-lookup"><span data-stu-id="d5522-146">It is not necessary to add an address for a default customer.</span></span>

<span data-ttu-id="d5522-147">Aşağıdaki resimde bir müşteri oluşturma örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="d5522-147">The following image shows an example of customer creation.</span></span>

![Varsayılan müşteri oluşturma](media/default-customer-creation.png)

<span data-ttu-id="d5522-149">Aşağıdaki resimde, bir varsayılan müşteri yapılandırması gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="d5522-149">The following image shows a default customer configuration.</span></span>

![Örnek müşteri yapılandırması](media/default-customer-configuration1.png)

<span data-ttu-id="d5522-151">Müşteri ayrıntıları ekranındaki varsayılan değerlerin çoğu kalabilir ancak iki değer değiştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="d5522-151">Most of the default values on the customer detials screen can remain, but two values should be changed.</span></span>

1. <span data-ttu-id="d5522-152">Müşteri ayrıntıları ekranında **Satış siparişi varsayılanları**'nı genişletin.</span><span class="sxs-lookup"><span data-stu-id="d5522-152">On the customer details screen, expand **Sales order defaults**.</span></span>
1. <span data-ttu-id="d5522-153">**Site** açılır listesinde, önceden yapılandırılmış bir siteyi seçin veya girin.</span><span class="sxs-lookup"><span data-stu-id="d5522-153">In the **Site** drop-down list, select or enter a pre-configured site.</span></span>
1. <span data-ttu-id="d5522-154">**Ambar** açılır listesinde, önceden yapılandırılmış bir ambarı seçin veya girin.</span><span class="sxs-lookup"><span data-stu-id="d5522-154">In the **Warehouse** drop-down list, and select or enter a pre-configured warehouse.</span></span>

<span data-ttu-id="d5522-155">Aşağıdaki resimde bir müşteri yapılandırma örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="d5522-155">The following image shows an example customer configuration.</span></span>

![Örnek müşteri yapılandırması](media/default-customer-configuration2.png)

## <a name="additional-resources"></a><span data-ttu-id="d5522-157">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="d5522-157">Additional resources</span></span>

[<span data-ttu-id="d5522-158">Kanallara genel bakış</span><span class="sxs-lookup"><span data-stu-id="d5522-158">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="d5522-159">Kanal kurulum önkoşulları</span><span class="sxs-lookup"><span data-stu-id="d5522-159">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
