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
ms.openlocfilehash: 1dd4dfc5b8ca7af66941d081b4c20be0f5d6001d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993412"
---
# <a name="create-a-default-customer"></a><span data-ttu-id="1d8de-103">Varsayılan müşteri oluşturma</span><span class="sxs-lookup"><span data-stu-id="1d8de-103">Create a default customer</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="1d8de-104">Bu konuda, Microsoft Dynamics 365 Commerce'te bir kanal oluşturulurken kullanılacak bir varsayılan müşterinin nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="1d8de-104">This topic describes how to create a default customer to use when creating a channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1d8de-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="1d8de-105">Overview</span></span>

<span data-ttu-id="1d8de-106">Bir kanal oluştururken varsayılan bir müşteri sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1d8de-106">When creating a channel, you will need to provide a default customer.</span></span> <span data-ttu-id="1d8de-107">Müşteri grubu ve müşteri adres defteri oluşturulduktan sonra, varsayılan bir müşteri kolayca oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="1d8de-107">A default customer can easily be created after first creating the customer group and customer address book.</span></span>

## <a name="create-a-customer-group"></a><span data-ttu-id="1d8de-108">Müşteri grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="1d8de-108">Create a customer group</span></span>

<span data-ttu-id="1d8de-109">Henüz müşteri grupları yoksa bir müşteri grubu oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d8de-109">If no customer groups exist yet, you can create one.</span></span> <span data-ttu-id="1d8de-110">Bunlar, örneğin, toptan satış, perakende, Internet, Çalışanlar gibi farklı müşteri gruplarını temsil eden gruplar olabilir.</span><span class="sxs-lookup"><span data-stu-id="1d8de-110">Examples may be groups to represent different customer groups, such as wholesale, retail, Internet, Employees, etc.</span></span>

<span data-ttu-id="1d8de-111">Müşteri grubu oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="1d8de-111">To create a customer group, follow these steps.</span></span>

1. <span data-ttu-id="1d8de-112">Gezinti bölmesinde **Modüller \> Perakende ve ticaret \> Müşteriler \> Müşteri grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="1d8de-112">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> Customer groups**.</span></span>
1. <span data-ttu-id="1d8de-113">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1d8de-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="1d8de-114">**Müşteri grubu** alanına bir müşteri grubu kodu girin.</span><span class="sxs-lookup"><span data-stu-id="1d8de-114">In the **Customer group** box, enter a customer group ID.</span></span>
1. <span data-ttu-id="1d8de-115">**Açıklama** kutusuna, uygun bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="1d8de-115">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="1d8de-116">**Ödeme koşulları** kutusuna, uygun bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="1d8de-116">In the **Terms of payment** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="1d8de-117">**Fatura vade tarihi ile ödeme tarihi arasındaki süre** kutusuna, uygun değer girin.</span><span class="sxs-lookup"><span data-stu-id="1d8de-117">In the **Time between invoice due date and payment date** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="1d8de-118">**Varsayılan vergi grubu** kutusuna, varsa bir vergi grubu girin.</span><span class="sxs-lookup"><span data-stu-id="1d8de-118">In the **Default tax group** box, enter a tax group if applicable.</span></span>
1. <span data-ttu-id="1d8de-119">**Fiyatlara satış vergisi dahildir** onay kutusunu (uygunsa) işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1d8de-119">Select the **Prices include sales tax** check box if applicable.</span></span>
1. <span data-ttu-id="1d8de-120">**Varsayılan silme nedeni** kutusuna, varsa uygun bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="1d8de-120">In the **Default write-off reason** box, enter an appropriate value, if applicable.</span></span>

<span data-ttu-id="1d8de-121">Aşağıdaki resimde, yapılandırılmış birkaç müşteri grubu gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="1d8de-121">The following image shows several configured customer groups.</span></span>

![Müşteri grupları](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a><span data-ttu-id="1d8de-123">Müşteri adres defteri oluşturma</span><span class="sxs-lookup"><span data-stu-id="1d8de-123">Create a customer address book</span></span>

<span data-ttu-id="1d8de-124">Müşterinin bir adres defteriyle ilişkilendirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="1d8de-124">A customer needs to be associated with an address book.</span></span> <span data-ttu-id="1d8de-125">Henüz oluşturulmadıysa, bir tane oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1d8de-125">If one has not yet been created, then you will need to create one.</span></span>

<span data-ttu-id="1d8de-126">Bir müşteri adres defteri oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="1d8de-126">To create a customer address book, follow these steps.</span></span>

1. <span data-ttu-id="1d8de-127">Gezinti bölmesinde **Modüller \> Perakende ve ticaret \> Kanal kurulumu \> Adres Defterleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="1d8de-127">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Address Books**.</span></span>
1. <span data-ttu-id="1d8de-128">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1d8de-128">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="1d8de-129">**Ad** kutusuna bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="1d8de-129">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="1d8de-130">**Açıklama** kutusuna bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="1d8de-130">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="1d8de-131">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1d8de-131">On the action pane, select **Save**.</span></span>

<span data-ttu-id="1d8de-132">Aşağıdaki resimde örnek bir adres defteri gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="1d8de-132">The following image shows an example address book.</span></span>

![Adres defteri](media/address-book.png)

## <a name="create-a-default-customer"></a><span data-ttu-id="1d8de-134">Varsayılan müşteri oluşturma</span><span class="sxs-lookup"><span data-stu-id="1d8de-134">Create a default customer</span></span>

<span data-ttu-id="1d8de-135">Bir varsayılan müşteri oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="1d8de-135">To create a default customer, follow these steps.</span></span>

1. <span data-ttu-id="1d8de-136">Gezinti bölmesinde **Modüller \> Perakende ve ticaret \> Müşteriler \> Tüm müşteriler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="1d8de-136">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="1d8de-137">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1d8de-137">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="1d8de-138">**Tür** açılır listesinde "Kişi"yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1d8de-138">In the **Type** drop-down list, select "Person".</span></span>
1. <span data-ttu-id="1d8de-139">**Müşteri hesabı** açılır listesinde bir hesap numarası seçin veya girin (örneğin "100001").</span><span class="sxs-lookup"><span data-stu-id="1d8de-139">In the **Customer account** drop-down list, select or enter an account number (for example, "100001").</span></span>
1. <span data-ttu-id="1d8de-140">**Ad** açılır listesinde, bir ad seçin veya girin (örneğin "Varsayılan").</span><span class="sxs-lookup"><span data-stu-id="1d8de-140">In the **First name** drop-down list, select or enter a name (for example, "Default").</span></span>
1. <span data-ttu-id="1d8de-141">**İkinci ad** açılır listesinde, bir ad seçin veya girin (örneğin "Perakende").</span><span class="sxs-lookup"><span data-stu-id="1d8de-141">In the **Middle name** drop-down list, select or enter a name (for example, "Retail").</span></span>
1. <span data-ttu-id="1d8de-142">**Soyadı** açılır listesinde, bir ad seçin veya girin (örneğin "Müşteri").</span><span class="sxs-lookup"><span data-stu-id="1d8de-142">In the **Last name** drop-down list, select or enter a name (for example, "Customer").</span></span>
1. <span data-ttu-id="1d8de-143">**Para birimi** açılır listesinde, bir para birimi seçin veya girin (örneğin "USD").</span><span class="sxs-lookup"><span data-stu-id="1d8de-143">In the **Currency** drop-down list, select or enter a currency (for example, "USD").</span></span>
1. <span data-ttu-id="1d8de-144">**Para birimi** açılır listesinde, önceden oluşturulan müşteri grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="1d8de-144">In the **Currency** drop-down list, select the customer group created previously.</span></span>
1. <span data-ttu-id="1d8de-145">**Adres defterleri** açılır listesinde, varolan bir müşteri adres defterini seçin.</span><span class="sxs-lookup"><span data-stu-id="1d8de-145">In the **Address books**  drop-down list, select an existing customer address book.</span></span>
1. <span data-ttu-id="1d8de-146">Kaydetmek ve yeni müşterinin müşteri ayrıntıları ekranına dönmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1d8de-146">Select **Save** to save and return to customer details screen for the new customer.</span></span>

> [!NOTE]
> <span data-ttu-id="1d8de-147">Varsayılan müşteri için bir adres eklemek gerekmez.</span><span class="sxs-lookup"><span data-stu-id="1d8de-147">It is not necessary to add an address for a default customer.</span></span>

<span data-ttu-id="1d8de-148">Aşağıdaki resimde bir müşteri oluşturma örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="1d8de-148">The following image shows an example of customer creation.</span></span>

![Varsayılan müşteri oluşturma](media/default-customer-creation.png)

<span data-ttu-id="1d8de-150">Aşağıdaki resimde, bir varsayılan müşteri yapılandırması gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="1d8de-150">The following image shows a default customer configuration.</span></span>

![Örnek müşteri yapılandırması](media/default-customer-configuration1.png)

<span data-ttu-id="1d8de-152">Müşteri ayrıntıları ekranındaki varsayılan değerlerin çoğu kalabilir ancak iki değer değiştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="1d8de-152">Most of the default values on the customer detials screen can remain, but two values should be changed.</span></span>

1. <span data-ttu-id="1d8de-153">Müşteri ayrıntıları ekranında **Satış siparişi varsayılanları**'nı genişletin.</span><span class="sxs-lookup"><span data-stu-id="1d8de-153">On the customer details screen, expand **Sales order defaults**.</span></span>
1. <span data-ttu-id="1d8de-154">**Site** açılır listesinde, önceden yapılandırılmış bir siteyi seçin veya girin.</span><span class="sxs-lookup"><span data-stu-id="1d8de-154">In the **Site** drop-down list, select or enter a pre-configured site.</span></span>
1. <span data-ttu-id="1d8de-155">**Ambar** açılır listesinde, önceden yapılandırılmış bir ambarı seçin veya girin.</span><span class="sxs-lookup"><span data-stu-id="1d8de-155">In the **Warehouse** drop-down list, and select or enter a pre-configured warehouse.</span></span>

<span data-ttu-id="1d8de-156">Aşağıdaki resimde bir müşteri yapılandırma örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="1d8de-156">The following image shows an example customer configuration.</span></span>

![Örnek müşteri yapılandırması](media/default-customer-configuration2.png)

## <a name="additional-resources"></a><span data-ttu-id="1d8de-158">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="1d8de-158">Additional resources</span></span>

[<span data-ttu-id="1d8de-159">Kanallara genel bakış</span><span class="sxs-lookup"><span data-stu-id="1d8de-159">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="1d8de-160">Kanal kurulum önkoşulları</span><span class="sxs-lookup"><span data-stu-id="1d8de-160">Channel setup prerequisites</span></span>](channels-prerequisites.md)
