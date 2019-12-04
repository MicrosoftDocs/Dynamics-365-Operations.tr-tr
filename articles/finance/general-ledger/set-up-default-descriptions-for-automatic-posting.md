---
title: Otomatik deftere nakil için varsayılan açıklamalar ayarlama
description: Bu konu, otomatik olarak genel muhasebeye nakledilen muhasebe girişlerini açıklamak için kullanılan varsayılan metnin nasıl ayarlanacağını açıklar. Serbest biçimli metni kullanarak veya sabit değişkenleri seçerek, varsayılan açıklama metnini ayarlayabilirsiniz.
author: aprilolson
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: eb89f50a3d227cad80226ce30f71c4f210129245
ms.sourcegitcommit: 0262a19e32b2c0c84c731d9f4fbe8ba91822afa3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/15/2019
ms.locfileid: "2622701"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a><span data-ttu-id="d375c-104">Otomatik deftere nakil için varsayılan açıklamalar ayarlama</span><span class="sxs-lookup"><span data-stu-id="d375c-104">Set up default descriptions for automatic posting</span></span>

<span data-ttu-id="d375c-105">Bu konu, otomatik olarak genel muhasebeye nakledilen muhasebe girişlerini açıklamak için kullanılan varsayılan metnin nasıl ayarlanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="d375c-105">This topic explains how to set up default text that is used to describe accounting entries that are posted automatically to the general ledger.</span></span> <span data-ttu-id="d375c-106">Serbest biçimli metni kullanarak veya sabit değişkenleri seçerek, varsayılan açıklama metnini ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d375c-106">You can set up default description text by using free-form text or by selecting fixed variables.</span></span>

> [!NOTE]
> <span data-ttu-id="d375c-107">Bazı ülke veya bölgelerdeki bazı hareket türleri için, Microsoft Dynamics AX veritabanındaki hareket türleriyle ilişkili olan alanlardaki metinleri de ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d375c-107">For some transaction types in some countries or regions, you can also include text from fields in the Microsoft Dynamics AX database that are related to those transaction types.</span></span> <span data-ttu-id="d375c-108">Hareket türlerinin ve ülkeler ile bölgelerin listesi için bu konunun ilerleyen kısımlarında bulunan [İsteğe bağlı: Varsayılan açıklamalara başka metin ekleme](#optional-add-other-text-to-default-descriptions) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="d375c-108">For a list of the transaction types, and the countries and regions, see the [Optional: Add other text to default descriptions](#optional-add-other-text-to-default-descriptions) section later in this topic.</span></span>

## <a name="set-up-default-descriptions"></a><span data-ttu-id="d375c-109">Varsayılan tanımlar oluşturma</span><span class="sxs-lookup"><span data-stu-id="d375c-109">Set up default descriptions</span></span>

1. <span data-ttu-id="d375c-110">**Kuruluş yönetimi** \> **Kurulum** \> **Varsayılan açıklamalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="d375c-110">Go to **Organization administration** \> **Setup** \> **Default descriptions**.</span></span>
2. <span data-ttu-id="d375c-111">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d375c-111">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="d375c-112">**Açıklama** alanında, varsayılan açıklama oluşturmak için hareket türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="d375c-112">In the **Description** field, select the type of transaction to create a default description for.</span></span>
4. <span data-ttu-id="d375c-113">**Dil** alanında, açıklamanın geçerli olduğu dili seçin.</span><span class="sxs-lookup"><span data-stu-id="d375c-113">In the **Language** field, select the language that the description applies to.</span></span>
5. <span data-ttu-id="d375c-114">**Metin** alanına bir varsayılan açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="d375c-114">In the **Text** field, enter the default description.</span></span> <span data-ttu-id="d375c-115">Alana metin yazabilir veya aşağıdaki serbest metin değişkenlerinden birini veya daha fazlasını kullanabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="d375c-115">You can type text in the field, or you can use one or more of the following free-text variables:</span></span>

    - <span data-ttu-id="d375c-116">**%1** – Hareket tarihi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d375c-116">**%1** – Add the transaction date.</span></span>
    - <span data-ttu-id="d375c-117">**%2** – Genel muhasebeye nakledilecek olan belge türüne karşılık gelen bir tanımlayıcı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d375c-117">**%2** – Add an identifier that corresponds to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="d375c-118">Örneğin, faturalarla ilişkili hareket türleri için **%2** değişkeni fatura numarasını ekler.</span><span class="sxs-lookup"><span data-stu-id="d375c-118">For example, for transaction types that are related to invoices, the **%2** variable adds the invoice number.</span></span>
    - <span data-ttu-id="d375c-119">**%3** – Genel muhasebeye nakledilecek olan belge türüyle ilgili bir tanımlayıcı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d375c-119">**%3** – Add an identifier that is related to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="d375c-120">Örneğin, faturalarla ilişkili hareket türleri için **%3** değişkeni müşteri hesabı numarasını ekler.</span><span class="sxs-lookup"><span data-stu-id="d375c-120">For example, for transaction types that are related to invoices, the **%3** variable adds the customer account number.</span></span>

## <a name="optional-add-other-text-to-default-descriptions"></a><span data-ttu-id="d375c-121">İsteğe bağlı: Varsayılan açıklamalara başka metin ekleme</span><span class="sxs-lookup"><span data-stu-id="d375c-121">Optional: Add other text to default descriptions</span></span>

<span data-ttu-id="d375c-122">Bazı ülke veya bölgelerdeki bazı hareket türleri için, varsayılan açıklamalara hareket türleriyle ilişkili olan verilerinizdeki alanlardan gelen metinleri de ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d375c-122">For some transaction types in some countries or regions, default descriptions can include text that comes from fields in your data that are related to those transaction types.</span></span> <span data-ttu-id="d375c-123">Aşağıdaki listelerde, bu seçeneğin kullanılabileceği hareket türleri ile ülkeler ve bölgeler gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="d375c-123">The following lists show the transaction types, and the countries and regions, that this option is available for.</span></span>

<span data-ttu-id="d375c-124">**Hareket tipleri**</span><span class="sxs-lookup"><span data-stu-id="d375c-124">**Transaction types**</span></span>

<span data-ttu-id="d375c-125">Aşağıdaki belge türleriyle ilişkili hareket türleriyle ilgili varsayılan açıklamalara başka metin ekleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="d375c-125">You can add other text to default descriptions for transaction types that are related to the following document types:</span></span>

- <span data-ttu-id="d375c-126">Müşteri faturaları</span><span class="sxs-lookup"><span data-stu-id="d375c-126">Customer invoices</span></span>
- <span data-ttu-id="d375c-127">Müşteri alacak dekontları</span><span class="sxs-lookup"><span data-stu-id="d375c-127">Customer credit notes</span></span>
- <span data-ttu-id="d375c-128">Müşteri nakit ödemeleri</span><span class="sxs-lookup"><span data-stu-id="d375c-128">Customer cash payments</span></span>
- <span data-ttu-id="d375c-129">Satıcı ödemeleri</span><span class="sxs-lookup"><span data-stu-id="d375c-129">Vendor payments</span></span>
- <span data-ttu-id="d375c-130">Satış siparişleri</span><span class="sxs-lookup"><span data-stu-id="d375c-130">Sales orders</span></span>
- <span data-ttu-id="d375c-131">Satınalma siparişleri</span><span class="sxs-lookup"><span data-stu-id="d375c-131">Purchase orders</span></span>
- <span data-ttu-id="d375c-132">Stok günlükleri</span><span class="sxs-lookup"><span data-stu-id="d375c-132">Inventory journals</span></span>
- <span data-ttu-id="d375c-133">Master planlama (MRP)</span><span class="sxs-lookup"><span data-stu-id="d375c-133">Master planning (MRP)</span></span>
- <span data-ttu-id="d375c-134">Sabit kıymetler</span><span class="sxs-lookup"><span data-stu-id="d375c-134">Fixed assets</span></span>

<span data-ttu-id="d375c-135">**Ülkeler ve bölgeler**</span><span class="sxs-lookup"><span data-stu-id="d375c-135">**Countries and regions**</span></span>

<span data-ttu-id="d375c-136">Bu seçenek aşağıdaki ülkeler ve bölgeler için kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="d375c-136">This option is available for the following countries and regions:</span></span>

- <span data-ttu-id="d375c-137">Brezilya</span><span class="sxs-lookup"><span data-stu-id="d375c-137">Brazil</span></span>
- <span data-ttu-id="d375c-138">Çin</span><span class="sxs-lookup"><span data-stu-id="d375c-138">China</span></span>
- <span data-ttu-id="d375c-139">Çek Cumhuriyeti</span><span class="sxs-lookup"><span data-stu-id="d375c-139">Czech Republic</span></span>
- <span data-ttu-id="d375c-140">Doğu Avrupa</span><span class="sxs-lookup"><span data-stu-id="d375c-140">Eastern Europe</span></span>
- <span data-ttu-id="d375c-141">Macaristan</span><span class="sxs-lookup"><span data-stu-id="d375c-141">Hungary</span></span>
- <span data-ttu-id="d375c-142">Hindistan</span><span class="sxs-lookup"><span data-stu-id="d375c-142">India</span></span>
- <span data-ttu-id="d375c-143">Japonya</span><span class="sxs-lookup"><span data-stu-id="d375c-143">Japan</span></span>
- <span data-ttu-id="d375c-144">Litvanya</span><span class="sxs-lookup"><span data-stu-id="d375c-144">Lithuania</span></span>
- <span data-ttu-id="d375c-145">Letonya</span><span class="sxs-lookup"><span data-stu-id="d375c-145">Latvia</span></span>
- <span data-ttu-id="d375c-146">Polonya</span><span class="sxs-lookup"><span data-stu-id="d375c-146">Poland</span></span>
- <span data-ttu-id="d375c-147">Rusya</span><span class="sxs-lookup"><span data-stu-id="d375c-147">Russia</span></span>

### <a name="add-text-to-default-descriptions"></a><span data-ttu-id="d375c-148">Varsayılan açıklamalara metin ekleme</span><span class="sxs-lookup"><span data-stu-id="d375c-148">Add text to default descriptions</span></span>

<span data-ttu-id="d375c-149">Bu konunun önceki kısımlarındaki [Varsayılan açıklamalar ayarlama](#set-up-default-descriptions) bölümünde bulunan adımları tamamladıktan sonra, başka metni varsayılan açıklamalara eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="d375c-149">After you complete the steps in the [Set up default descriptions](#set-up-default-descriptions) section earlier in this topic, follow these steps to add other text to the default descriptions.</span></span>

1. <span data-ttu-id="d375c-150">**Parametreler** hızlı sekmesinde, **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d375c-150">On the **Parameters** FastTab, select **Add**.</span></span>
2. <span data-ttu-id="d375c-151">**Referans tablosu** alanında, açıklamaya parametre verilerinin ekleneceği veritabanı tablosunu seçin.</span><span class="sxs-lookup"><span data-stu-id="d375c-151">In the **Reference table** field, select the database table from which to add parameter data to the description.</span></span>
3. <span data-ttu-id="d375c-152">**Referans alanı** alanında, açıklamaya parametre verilerinin ekleneceği alanı seçin.</span><span class="sxs-lookup"><span data-stu-id="d375c-152">In the **Reference field** field, select the field from which to add parameter data to the description.</span></span>
4. <span data-ttu-id="d375c-153">Daha fazla parametre eklemek için 1 ile 3. adımlar arasındaki işlemleri tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="d375c-153">Repeat steps 1 through 3 to add more parameters.</span></span>