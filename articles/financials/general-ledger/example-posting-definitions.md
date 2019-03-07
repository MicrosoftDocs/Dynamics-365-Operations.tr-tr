---
title: Deftere nakil tanımları
description: Bu makale, deftere nakil tanımlarının satınalma siparişleri yükümlülükleri ve bütçe tahsis etme için nasıl kullanılacağına dair örnekler sağlar.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f5fb08a86639e9a9a79dca5fc1200e73e5870432
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "310266"
---
# <a name="posting-definition-examples"></a><span data-ttu-id="6e2b5-103">Deftere nakil tanım örnekleri</span><span class="sxs-lookup"><span data-stu-id="6e2b5-103">Posting definition examples</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e2b5-104">Bu makale, deftere nakil tanımlarının satınalma siparişleri yükümlülükleri ve bütçe tahsis etme için nasıl kullanılacağına dair örnekler sağlar.</span><span class="sxs-lookup"><span data-stu-id="6e2b5-104">This article provides examples that show how posting definitions are used for purchase order encumbrances and budget appropriations.</span></span>

<span data-ttu-id="6e2b5-105">Bu konuyu okumadan önce, nakil tanımlarını ve hareket nakil tanımlarını biliyor olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="6e2b5-105">Before you read this topic, you should be familiar with posting definitions and transaction posting definitions.</span></span> <span data-ttu-id="6e2b5-106">Daha fazla bilgi için, bkz. [Nakil tanımları](posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="6e2b5-106">For information, see [Posting definitions](posting-definitions.md).</span></span> <span data-ttu-id="6e2b5-107">**Nakil tanımları** sayfasında aşağıdaki örnekler ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="6e2b5-107">The following examples can be set up on the **Posting definitions** page.</span></span> <span data-ttu-id="6e2b5-108">Her bir örnek, şu bölümleri içerir:</span><span class="sxs-lookup"><span data-stu-id="6e2b5-108">Each example contains these sections:</span></span>

-   <span data-ttu-id="6e2b5-109">Nakil tanımı – Eşleşme ölçütleri</span><span class="sxs-lookup"><span data-stu-id="6e2b5-109">Posting definition – Match criteria</span></span>
-   <span data-ttu-id="6e2b5-110">Nakil tanımı – Üretilen girişler</span><span class="sxs-lookup"><span data-stu-id="6e2b5-110">Posting definition – Generated entries</span></span>
-   <span data-ttu-id="6e2b5-111">Hesaplar, boyut değerleri ve tutarlar ile birlikte hareketler</span><span class="sxs-lookup"><span data-stu-id="6e2b5-111">Transactions with the accounts, dimension values, and amounts</span></span>
-   <span data-ttu-id="6e2b5-112">Nakil tanımından üretilen genel muhasebe girişleri</span><span class="sxs-lookup"><span data-stu-id="6e2b5-112">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="6e2b5-113">Hareketteki nakil tanımı ve hesaplar ile boyut değerleri için **Eşleşme ölçütleri** bölmesinde hesaplar ile boyut değerleri arasında bir eşleşme ortaya çıktığında, genel muhasebe girişleri nakil tanımına yönelik **Üretilen girişler** bölmesi temel alınarak üretilir.</span><span class="sxs-lookup"><span data-stu-id="6e2b5-113">When a match occurs between the accounts and dimension values in the **Match criteria** pane for the posting definition and the accounts and dimension values on the transaction, ledger entries are generated based on the **Generated entries** pane for the posting definition.</span></span> 
> [!NOTE]
> <span data-ttu-id="6e2b5-114">Bir deftere nakil tanımını belirli bir hareket türü ile ilişkilendirmek için **İşlem deftere nakil tanımları** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="6e2b5-114">To associate a posting definition with a specific transaction type, use the **Transaction posting definitions** page.</span></span> <span data-ttu-id="6e2b5-115">Bir deftere nakil tanımını bir hareket türü ile ilişkilendirdikten sonra, **Deftere nakil tanımları kullan** seçeneğini, **Genel muhasebe parametreleri** sayfasında seçin, seçilen hareket türünün tüm hareketleri, deftere nakil tanımlarını kullanmak zorundadır.</span><span class="sxs-lookup"><span data-stu-id="6e2b5-115">After you associate a posting definition with a transaction type and select **Use posting definitions** on the **General ledger parameters** page, all transactions of the selected transaction type must use posting definitions.</span></span>

## <a name="example-purchase-order-encumbrances"></a><span data-ttu-id="6e2b5-116">Örnek: Satınalma emri yükümlülükleri</span><span class="sxs-lookup"><span data-stu-id="6e2b5-116">Example: Purchase order encumbrances</span></span>
<span data-ttu-id="6e2b5-117">**Genel muhasebe parametreleri** sayfasında **Yükümlülük işlemini etkinleştir** seçeneğini belirleyerek yükümlülük işlemesini etkinleştirdiğinizde, yükümlülükleri genel muhasebeye kaydetmek için rezerve edilmesi gereken tüm hesaplara yönelik nakil tanımlarının kullanılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="6e2b5-117">When you enable encumbrance processing by selecting **Enable encumbrance process** on the **General ledger parameters** page, posting definitions must be used to record encumbrances to the general ledger for any accounts that should be reserved.</span></span> <span data-ttu-id="6e2b5-118">Çoğu durumda, tüm gider hesapları bilançoda rezerve edilir.</span><span class="sxs-lookup"><span data-stu-id="6e2b5-118">In most cases, all expense accounts are reserved on the balance sheet.</span></span> 

<span data-ttu-id="6e2b5-119">Yükümlülüklere yönelik nakil tanımları, **Nakil tanımları** sayfasındaki, **Satınalma** modülünde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="6e2b5-119">Posting definitions for encumbrances are set up for the **Purchasing** module on the **Posting definitions** page.</span></span> <span data-ttu-id="6e2b5-120">Ardından, **Hareket nakil tanımları** sayfasının **Satınalma** alanında **Satınalma emri** hareket türünü seçerek nakil tanımını satınalma emirleri ile ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6e2b5-120">Then, in the **Purchasing** area of the **Transaction posting definitions** page, you can select the **Purchase order** transaction type to associate the posting definition with purchase orders.</span></span> 

<span data-ttu-id="6e2b5-121">Satınalma emri yükümlülüğüne yönelik tüm fiş hareketleri, bir fiş üzerindeki her bir benzersiz boyutu dengelemelidir (yani borçlar kredilere eşit olmalıdır).</span><span class="sxs-lookup"><span data-stu-id="6e2b5-121">All voucher transactions for purchase order encumbrances must balance (that is, debits must equal credits) in each unique dimension on a voucher.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="6e2b5-122">Nakil tanımı – Eşleşme ölçütleri</span><span class="sxs-lookup"><span data-stu-id="6e2b5-122">Posting definition – Match criteria</span></span>

| <span data-ttu-id="6e2b5-123">Hesap yapısı</span><span class="sxs-lookup"><span data-stu-id="6e2b5-123">Account structure</span></span>       | <span data-ttu-id="6e2b5-124">Hesap numarasını eşleştir</span><span class="sxs-lookup"><span data-stu-id="6e2b5-124">Match account number</span></span> | <span data-ttu-id="6e2b5-125">Öncelik </span><span class="sxs-lookup"><span data-stu-id="6e2b5-125">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="6e2b5-126">Hesap Yapısı - Kar ve Zarar</span><span class="sxs-lookup"><span data-stu-id="6e2b5-126">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="6e2b5-127">1</span><span class="sxs-lookup"><span data-stu-id="6e2b5-127">1</span></span>        |

<span data-ttu-id="6e2b5-128"><em>\**Hesap numarasını</em>* eşleştir alanında boş bir değer olması, tanımlı hesap yapısındaki tüm eşleşen hesapların eşleştirme kuralının parçası olduğu anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="6e2b5-128"><em>A blank value in the \**Match account number</em>* field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="6e2b5-129">Nakil tanımı – Üretilen girişler</span><span class="sxs-lookup"><span data-stu-id="6e2b5-129">Posting definition – Generated entries</span></span>

| <span data-ttu-id="6e2b5-130">Hesap yapısı</span><span class="sxs-lookup"><span data-stu-id="6e2b5-130">Account structure</span></span> | <span data-ttu-id="6e2b5-131">Oluşturulan hesap numarası</span><span class="sxs-lookup"><span data-stu-id="6e2b5-131">Generated account number</span></span>                    | <span data-ttu-id="6e2b5-132">Oluşturulan borç/alacak</span><span class="sxs-lookup"><span data-stu-id="6e2b5-132">Generated debit/credit</span></span> |
|-------------------|---------------------------------------------|------------------------|
| <span data-ttu-id="6e2b5-133">Kalan</span><span class="sxs-lookup"><span data-stu-id="6e2b5-133">Balance</span></span>           | <span data-ttu-id="6e2b5-134">300143 - -(Yükümlülük hesabı)</span><span class="sxs-lookup"><span data-stu-id="6e2b5-134">300143 - -(Encumbrance account)</span></span>             | <span data-ttu-id="6e2b5-135">Aynısı</span><span class="sxs-lookup"><span data-stu-id="6e2b5-135">Same</span></span>                   |
| <span data-ttu-id="6e2b5-136">Kalan</span><span class="sxs-lookup"><span data-stu-id="6e2b5-136">Balance</span></span>           | <span data-ttu-id="6e2b5-137">300144 - -(Yükümlülük hesabına rezerve et)</span><span class="sxs-lookup"><span data-stu-id="6e2b5-137">300144 - -(Reserve for encumbrance account)</span></span> | <span data-ttu-id="6e2b5-138">Dengeleme</span><span class="sxs-lookup"><span data-stu-id="6e2b5-138">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="6e2b5-139">Hesaplar, boyut değerleri ve tutarlar ile birlikte hareketler</span><span class="sxs-lookup"><span data-stu-id="6e2b5-139">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="6e2b5-140">Hesaplar ve boyut değerleri ya bir satınalma emri satırı için girdiğiniz muhasebe dağılımlarından ya da satıcılar, maddeler, kategoriler ve boyut şablonları için varsayılan ayarlar temel alınarak otomatik olarak üretilen hesaplar ve boyutlardan gelir.</span><span class="sxs-lookup"><span data-stu-id="6e2b5-140">The accounts and dimension values come either from the accounting distributions that you enter for a purchase order line, or from the accounts and dimensions that are automatically generated based on the default settings for vendors, items, categories, and dimension templates.</span></span>

| <span data-ttu-id="6e2b5-141">Hesap + boyutlar</span><span class="sxs-lookup"><span data-stu-id="6e2b5-141">Account + dimensions</span></span>           | <span data-ttu-id="6e2b5-142">Borç</span><span class="sxs-lookup"><span data-stu-id="6e2b5-142">Debit</span></span>  | <span data-ttu-id="6e2b5-143">Alacak</span><span class="sxs-lookup"><span data-stu-id="6e2b5-143">Credit</span></span> | <span data-ttu-id="6e2b5-144">Açıklama</span><span class="sxs-lookup"><span data-stu-id="6e2b5-144">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="6e2b5-145">606400-OU\_1-OU\_3566-Eğitimi</span><span class="sxs-lookup"><span data-stu-id="6e2b5-145">606400-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="6e2b5-146">250.00</span><span class="sxs-lookup"><span data-stu-id="6e2b5-146">250.00</span></span> |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="6e2b5-147">Nakil tanımından üretilen genel muhasebe girişleri</span><span class="sxs-lookup"><span data-stu-id="6e2b5-147">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="6e2b5-148">Yükümlülükleri kaydetmek için genel muhasebe girişleri üretilir.</span><span class="sxs-lookup"><span data-stu-id="6e2b5-148">Generated ledger entries are created to record the encumbrances.</span></span>

| <span data-ttu-id="6e2b5-149">Hesap + boyutlar</span><span class="sxs-lookup"><span data-stu-id="6e2b5-149">Account + dimensions</span></span>           | <span data-ttu-id="6e2b5-150">Borç</span><span class="sxs-lookup"><span data-stu-id="6e2b5-150">Debit</span></span>  | <span data-ttu-id="6e2b5-151">Alacak</span><span class="sxs-lookup"><span data-stu-id="6e2b5-151">Credit</span></span> | <span data-ttu-id="6e2b5-152">Açıklama</span><span class="sxs-lookup"><span data-stu-id="6e2b5-152">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="6e2b5-153">300143-OU\_1-OU\_3566-Eğitimi</span><span class="sxs-lookup"><span data-stu-id="6e2b5-153">300143-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="6e2b5-154">250.00</span><span class="sxs-lookup"><span data-stu-id="6e2b5-154">250.00</span></span> |        |         |
| <span data-ttu-id="6e2b5-155">300144-OU\_1-OU\_3566-Eğitimi</span><span class="sxs-lookup"><span data-stu-id="6e2b5-155">300144-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="6e2b5-156">250.00</span><span class="sxs-lookup"><span data-stu-id="6e2b5-156">250.00</span></span> |         |

<span data-ttu-id="6e2b5-157">Bu örnekte, Hesap Yapısı - Kar ve Zarar'ın parçası olan tüm hesaplar nakil tanımı kriterlerini karşılar.</span><span class="sxs-lookup"><span data-stu-id="6e2b5-157">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="6e2b5-158">Dolayısıyla, 606500-OU\_1-OU\_3566-Eğitim değerlendirildiğinde, üretilen girişler, nakil tanımı için **Genel girişler** bölmesinde tanımlanan hesaplara yönelik oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6e2b5-158">Therefore, when 606500-OU\_1-OU\_3566-Training is evaluated, generated entries are created for the accounts that are defined in the **Generated entries** pane for the posting definition.</span></span>

## <a name="example-budget-appropriations"></a><span data-ttu-id="6e2b5-159">Örnek: Bütçe tahsisatları</span><span class="sxs-lookup"><span data-stu-id="6e2b5-159">Example: Budget appropriations</span></span>
<span data-ttu-id="6e2b5-160">**Genel muhasebe parametreleri** sayfasındaki **Bütçe tahsisatını etkinleştir**'i seçerek bütçe tahsisatını etkinleştirdiğinizde, bütçe kayıt girişlerini genel muhasebeye kaydetmek için nakil tanımlarının kullanılması gereklidir.</span><span class="sxs-lookup"><span data-stu-id="6e2b5-160">When you enable budget appropriation by selecting **Enable budget appropriation** on the **General ledger parameters** page, posting definitions must be used to record budget register entries to the general ledger.</span></span> <span data-ttu-id="6e2b5-161">Bir bütçe kontrol yapılandırması aktif ve açık durumda iken, tahsisatlar, revizyonlar, transferler, projeler, sabit kıymetler ve genel muhasebeye tedarik ve talep tahminlerine yönelik girişlerin kaydını desteklemek için nakil tanımları ve hareket nakil tanımları kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6e2b5-161">When a budget control configuration is active and is turned on, posting definitions and transaction posting definitions can be used to support the recording of entries for appropriations, revisions, transfers, projects, fixed assets, and supply and demand forecasts to the general ledger.</span></span> 

<span data-ttu-id="6e2b5-162">**Orijinal bütçe** bütçe türüne sahip ve tahsisatları etkinleştirilmiş bütçe kaydı girişlerine yönelik bir nakil tanımı ayarlamak için, **Nakil tanımları** sayfasındaki **Bütçe** modülünü seçin.</span><span class="sxs-lookup"><span data-stu-id="6e2b5-162">To set up a posting definition for budget register entries that has a budget type of **Original budget**, and that has appropriations enabled, select the **Budget** module on the **Posting definitions** page.</span></span> <span data-ttu-id="6e2b5-163">Ardından, **Hareket nakil tanımları** sayfasının **Bütçe** alanında, nakil tanımını bütçe türü **Orijinal bütçe** olan bütçe kaydı girişleri ile ilişkilendirmek için bütçe kodları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6e2b5-163">Then, in the **Budget** area of the **Transaction posting definitions** page, you can use budget codes to associate the posting definition with budget register entries that have a budget type of **Original budget**.</span></span> 

<span data-ttu-id="6e2b5-164">Bütçe tahsisatları ve nakil tanımları etkinleştirildiğinde, bütçe kaydı girişleri bütçe kontrolü için ve genel muhasebede kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="6e2b5-164">When budget appropriations and posting definitions are enabled, the budget register entries are recorded for budget control and in the general ledger.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="6e2b5-165">Nakil tanımı – Eşleşme ölçütleri</span><span class="sxs-lookup"><span data-stu-id="6e2b5-165">Posting definition – Match criteria</span></span>

| <span data-ttu-id="6e2b5-166">Hesap yapısı</span><span class="sxs-lookup"><span data-stu-id="6e2b5-166">Account structure</span></span>       | <span data-ttu-id="6e2b5-167">Hesap numarasını eşleştir</span><span class="sxs-lookup"><span data-stu-id="6e2b5-167">Match account number</span></span> | <span data-ttu-id="6e2b5-168">Öncelik </span><span class="sxs-lookup"><span data-stu-id="6e2b5-168">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="6e2b5-169">Hesap Yapısı - Kar ve Zarar</span><span class="sxs-lookup"><span data-stu-id="6e2b5-169">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="6e2b5-170">1</span><span class="sxs-lookup"><span data-stu-id="6e2b5-170">1</span></span>        |

<span data-ttu-id="6e2b5-171"><em>\**Hesap numarasını</em>* eşleştir alanında boş bir değer olması, tanımlı hesap yapısındaki tüm eşleşen hesapların eşleştirme kuralının parçası olduğu anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="6e2b5-171"><em>A blank value in the \**Match account number</em>* field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="6e2b5-172">Nakil tanımı – Üretilen girişler</span><span class="sxs-lookup"><span data-stu-id="6e2b5-172">Posting definition – Generated entries</span></span>

| <span data-ttu-id="6e2b5-173">Hesap yapısı</span><span class="sxs-lookup"><span data-stu-id="6e2b5-173">Account structure</span></span> | <span data-ttu-id="6e2b5-174">Oluşturulan hesap numarası</span><span class="sxs-lookup"><span data-stu-id="6e2b5-174">Generated account number</span></span>              | <span data-ttu-id="6e2b5-175">Oluşturulan borç/alacak</span><span class="sxs-lookup"><span data-stu-id="6e2b5-175">Generated debit/credit</span></span> |
|-------------------|---------------------------------------|------------------------|
| <span data-ttu-id="6e2b5-176">Hesap yapısı</span><span class="sxs-lookup"><span data-stu-id="6e2b5-176">Account structure</span></span> | <span data-ttu-id="6e2b5-177">300145 - -(Tahmini gelir hesabı)</span><span class="sxs-lookup"><span data-stu-id="6e2b5-177">300145 - -(Estimated revenue account)</span></span> | <span data-ttu-id="6e2b5-178">Aynısı</span><span class="sxs-lookup"><span data-stu-id="6e2b5-178">Same</span></span>                   |
| <span data-ttu-id="6e2b5-179">Hesap yapısı</span><span class="sxs-lookup"><span data-stu-id="6e2b5-179">Account structure</span></span> | <span data-ttu-id="6e2b5-180">300146 - -(Tahsisat hesabı)</span><span class="sxs-lookup"><span data-stu-id="6e2b5-180">300146 - -(Appropriation account)</span></span>     | <span data-ttu-id="6e2b5-181">Dengeleme</span><span class="sxs-lookup"><span data-stu-id="6e2b5-181">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="6e2b5-182">Hesaplar, boyut değerleri ve tutarlar ile birlikte hareketler</span><span class="sxs-lookup"><span data-stu-id="6e2b5-182">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="6e2b5-183">Bütçe hesabı girişine yönelik hesapları, boyut değerlerini ve tutarları **Bütçe kaydı girişi** sayfasına girersiniz.</span><span class="sxs-lookup"><span data-stu-id="6e2b5-183">You enter the accounts, dimension values, and amounts for the budget account entry on the **Budget register entry** page.</span></span>

| <span data-ttu-id="6e2b5-184">Hesap + boyutlar</span><span class="sxs-lookup"><span data-stu-id="6e2b5-184">Account + dimensions</span></span>           | <span data-ttu-id="6e2b5-185">Borç</span><span class="sxs-lookup"><span data-stu-id="6e2b5-185">Debit</span></span> | <span data-ttu-id="6e2b5-186">Alacak</span><span class="sxs-lookup"><span data-stu-id="6e2b5-186">Credit</span></span> | <span data-ttu-id="6e2b5-187">Açıklama</span><span class="sxs-lookup"><span data-stu-id="6e2b5-187">Comment</span></span> |
|--------------------------------|-------|--------|---------|
| <span data-ttu-id="6e2b5-188">606400-OU\_1-OU\_3566-Eğitimi</span><span class="sxs-lookup"><span data-stu-id="6e2b5-188">606400-OU\_1-OU\_3566-Training</span></span> |       | <span data-ttu-id="6e2b5-189">250.00</span><span class="sxs-lookup"><span data-stu-id="6e2b5-189">250.00</span></span> |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="6e2b5-190">Nakil tanımından üretilen genel muhasebe girişleri</span><span class="sxs-lookup"><span data-stu-id="6e2b5-190">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="6e2b5-191">Üretilen genel muhasebe girişleri, her bir boyutta orijinal bütçeyi kaydetmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6e2b5-191">Generated ledger entries are created to record the original budget in each dimension.</span></span>

| <span data-ttu-id="6e2b5-192">Hesap + boyutlar</span><span class="sxs-lookup"><span data-stu-id="6e2b5-192">Account + dimensions</span></span>           | <span data-ttu-id="6e2b5-193">Borç</span><span class="sxs-lookup"><span data-stu-id="6e2b5-193">Debit</span></span>  | <span data-ttu-id="6e2b5-194">Alacak</span><span class="sxs-lookup"><span data-stu-id="6e2b5-194">Credit</span></span> | <span data-ttu-id="6e2b5-195">Açıklama</span><span class="sxs-lookup"><span data-stu-id="6e2b5-195">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="6e2b5-196">300145-OU\_1-OU\_3566-Eğitimi</span><span class="sxs-lookup"><span data-stu-id="6e2b5-196">300145-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="6e2b5-197">250.00</span><span class="sxs-lookup"><span data-stu-id="6e2b5-197">250.00</span></span> |         |
| <span data-ttu-id="6e2b5-198">300146-OU\_1-OU\_3566-Eğitimi</span><span class="sxs-lookup"><span data-stu-id="6e2b5-198">300146-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="6e2b5-199">250.00</span><span class="sxs-lookup"><span data-stu-id="6e2b5-199">250.00</span></span> |        |         |

<span data-ttu-id="6e2b5-200">Bu örnekte, Hesap Yapısı - Kar ve Zarar'ın parçası olan tüm hesaplar nakil tanımı kriterlerini karşılar.</span><span class="sxs-lookup"><span data-stu-id="6e2b5-200">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="6e2b5-201">Dolayısıyla 606400-OU\_1-OU\_3566-Eğitim değerlendirildiğinde, üretilen genel muhasebe girişleri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6e2b5-201">Therefore, when 606400-OU\_1-OU\_3566-Training is evaluated, the generated ledger entries are created.</span></span>





