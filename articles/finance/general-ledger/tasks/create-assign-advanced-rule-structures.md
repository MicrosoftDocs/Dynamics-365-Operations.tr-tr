---
title: Gelişmiş kural yapıları oluşturma ve atama
description: Bu konu, bir hesap yapısına gelişmiş bir kural yapısının nasıl oluşturulacağını ve atanacağını açıklar.
author: aprilolson
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b81e3cc169bf0164af0b9c4de4faeb936df6784
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837069"
---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="39a4a-103">Gelişmiş kural yapıları oluşturma ve atama</span><span class="sxs-lookup"><span data-stu-id="39a4a-103">Create and assign advanced rule structures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="39a4a-104">Bu konu, bir hesap yapısına gelişmiş bir kural yapısının nasıl oluşturulacağını ve atanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="39a4a-104">This topic explains how to create and assign an advanced rule structure to an account structure.</span></span> <span data-ttu-id="39a4a-105">Bu kılavuz, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="39a4a-105">This guide uses the USMF demo company.</span></span>

## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="39a4a-106">Gelişmiş kural yapısı oluştur</span><span class="sxs-lookup"><span data-stu-id="39a4a-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="39a4a-107">**Gezinti bölmesi > Modüller > Genel muhasebe > Hesap planı > Yapılar > Gelişmiş kural yapıları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="39a4a-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Advanced rule structures**.</span></span>
2. <span data-ttu-id="39a4a-108">Açılır iletişim kutusunu açmak için **Yeni** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="39a4a-108">Select **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="39a4a-109">**Gelişmiş kural yapısı** alanında, kural yapısını açıklayan için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="39a4a-109">In the **Advanced rule structure** field, type a name to describe the rule structure.</span></span>
4. <span data-ttu-id="39a4a-110">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="39a4a-110">Select **OK**.</span></span>
5. <span data-ttu-id="39a4a-111">**Segment ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="39a4a-111">Select **Add segment**.</span></span>
6. <span data-ttu-id="39a4a-112">Segmentler listesinde, bir mali boyut seçin.</span><span class="sxs-lookup"><span data-stu-id="39a4a-112">In the list of segments, select a financial dimension.</span></span> <span data-ttu-id="39a4a-113">Örneğin, **Mağaza**.</span><span class="sxs-lookup"><span data-stu-id="39a4a-113">For example, **Store**.</span></span>  
7. <span data-ttu-id="39a4a-114">**Segment ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="39a4a-114">Select **Add segment**.</span></span>
8. <span data-ttu-id="39a4a-115">**Etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="39a4a-115">Select **Activate**.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="39a4a-116">Gelişmiş bir kural yapısını bir hesap yapısına uygula</span><span class="sxs-lookup"><span data-stu-id="39a4a-116">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="39a4a-117">**Gezinti bölmesi > Modüller > Genel muhasebe > Hesap planı > Yapılar > Hesap yapılarını yapılandır**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="39a4a-117">Go to **navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="39a4a-118">Listede, gelişmiş kural uygulamak istediğiniz hesap yapısını bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="39a4a-118">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
3. <span data-ttu-id="39a4a-119">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="39a4a-119">Select **Edit**.</span></span> <span data-ttu-id="39a4a-120">**Gelişmiş kurallar**'ı da seçebilirsiniz, ardından hesap yapısını **Taslak modu**'na yerleştirmeniz istenir.</span><span class="sxs-lookup"><span data-stu-id="39a4a-120">You can also select **Advanced rules** and you will be prompted to put the account structure in **Draft mode**.</span></span>  
4. <span data-ttu-id="39a4a-121">**Gelişmiş kurallar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="39a4a-121">Select **Advanced rules**.</span></span>
5. <span data-ttu-id="39a4a-122">Açılır iletişim kutusunu açmak için **Yeni** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="39a4a-122">Select **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="39a4a-123">**Gelişmiş kural** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="39a4a-123">In the **Advanced rule** field, type a value.</span></span>
7. <span data-ttu-id="39a4a-124">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="39a4a-124">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="39a4a-125">**Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="39a4a-125">Select **Create**.</span></span>
9. <span data-ttu-id="39a4a-126">**Yeni ölçüt ekle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="39a4a-126">Select **Add new criteria**.</span></span>
10. <span data-ttu-id="39a4a-127">**Nereye** alanında, ana hesabı veya bir mali boyutu seçin.</span><span class="sxs-lookup"><span data-stu-id="39a4a-127">In the **Where** field, select main account or a financial dimension.</span></span>
11. <span data-ttu-id="39a4a-128">**İşleç** alanında, **arasında** ve **içerir** gibi bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="39a4a-128">In the **Operator** field, select an option, such as **is between** and **includes**.</span></span>
12. <span data-ttu-id="39a4a-129">**Değer** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="39a4a-129">In the **Value** field, type a value.</span></span>
13. <span data-ttu-id="39a4a-130">**Aracılığıyla** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="39a4a-130">In the **through** field, type a value.</span></span>
14. <span data-ttu-id="39a4a-131">Açılır iletişim kutusunu açmak için **Ekle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="39a4a-131">Select **Add** to open the drop dialog.</span></span>
15. <span data-ttu-id="39a4a-132">Listede, girdiğiniz ölçüt gerçekleştiğinde kullanmak istediğiniz gelişmiş kural yapısını bulun.</span><span class="sxs-lookup"><span data-stu-id="39a4a-132">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
16. <span data-ttu-id="39a4a-133">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="39a4a-133">Select **Add**.</span></span>
17. <span data-ttu-id="39a4a-134">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="39a4a-134">Close the page.</span></span>
18. <span data-ttu-id="39a4a-135">**Etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="39a4a-135">Select **Activate**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]