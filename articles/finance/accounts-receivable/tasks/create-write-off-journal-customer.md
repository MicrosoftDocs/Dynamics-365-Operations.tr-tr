---
title: Müşteri için silme günlüğü oluşturma
description: Bu görev kılavuzunda, silme işlemleri parametrelerinin ve ardından silme hareketlerinin Tahsilatlar sayfasından, Açık müşteri faturaları sayfasından ve Müşteri sayfasından nasıl ayarlanacağını göreceksiniz.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2422f0a9d168daa76d105099c8b7455c97f92125
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188844"
---
# <a name="create-a-write-off-journal-for-a-customer"></a><span data-ttu-id="29141-103">Müşteri için silme günlüğü oluşturma</span><span class="sxs-lookup"><span data-stu-id="29141-103">Create a write-off journal for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="29141-104">Bu görev kılavuzunda, silme işlemleri parametrelerinin ve ardından silme hareketlerinin Tahsilatlar sayfasından, Açık müşteri faturaları sayfasından ve Müşteri sayfasından nasıl ayarlanacağını göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="29141-104">This task guide will show you how to set up the parameters for write-offs and then write off transactions from the Collections page, the Open customer invoices page, and the Customer page.</span></span> <span data-ttu-id="29141-105">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="29141-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-the-write-off-parameters"></a><span data-ttu-id="29141-106">Silme parametrelerini ayarlayın</span><span class="sxs-lookup"><span data-stu-id="29141-106">Set up the write off parameters</span></span>
1. <span data-ttu-id="29141-107">**Gezinti bölmesi > Modüller > Alacak ve tahsilatlar > Kurulum > Alacak hesapları parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="29141-107">Go to **Navigation pane > Modules > Credit and collections > Setup > Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="29141-108">**Tahsilatlar**  sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="29141-108">Click the **Collections** tab.</span></span>
3. <span data-ttu-id="29141-109">**Silme bölümünü** genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="29141-109">Expand or collapse the **Write-off** section.</span></span>
    - <span data-ttu-id="29141-110">**Silme günlüğü**, oluşturduğunuz silme hareketlerini tutan yevmiye defteridir.</span><span class="sxs-lookup"><span data-stu-id="29141-110">The **Write-off journal** is the general journal that will hold the write-off transactions that you create.</span></span>  
    - <span data-ttu-id="29141-111">Her silme işlemine bir neden kodu ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="29141-111">You can attach a reason code to every write-off.</span></span> <span data-ttu-id="29141-112">Bu varsayılan değeri silme işlemi sırasında geçersiz kılabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="29141-112">You can override this default at the time of the write-off.</span></span>  
    - <span data-ttu-id="29141-113">Silme işleminde satış vergisini orijinal hareketten ayırmak isterseniz **Satış vergisini ayır**'ı Evet yapın.</span><span class="sxs-lookup"><span data-stu-id="29141-113">Set the **Separate sales tax** to Yes if you want to separate the sales tax from the original transaction in the write-off.</span></span>  
4. <span data-ttu-id="29141-114">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="29141-114">Close the page.</span></span>
5. <span data-ttu-id="29141-115">**Alacak ve tahsilatlar > Kurulum > Müşteri deftere nakil profilleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="29141-115">Go to **Credit and collections > Setup > Customer posting profiles**.</span></span> <span data-ttu-id="29141-116">Silme hesabı gider hesabı olarak veya yevmiye defterinde rezerv düzeltme olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="29141-116">The write-off account will be used as the expense account or reserve adjustment in the general journal.</span></span>
6. <span data-ttu-id="29141-117">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="29141-117">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a><span data-ttu-id="29141-118">Bir müşteri bakiyesini yaşlandırılmış bakiyeler sayfasında silin</span><span class="sxs-lookup"><span data-stu-id="29141-118">Write off a customer balance from the aged balances page</span></span>
1. <span data-ttu-id="29141-119">**Alacak ve tahsilatlar > Tahsilatlar > Yaşlandırılmış bakiyeler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="29141-119">Go to **Credit and collections > Collections > Aged balances**.</span></span>
2. <span data-ttu-id="29141-120">Silme işlemi yapmak istediğiniz müşterinin satırını işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="29141-120">Mark the row for the customer that you want to write off.</span></span> <span data-ttu-id="29141-121">Örneğin, Birch şirketinin bulunduğu satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="29141-121">For example, mark the line with Birch Company on it.</span></span>
3. <span data-ttu-id="29141-122">**Eylem Bölmesinde**, **Tahsil et** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="29141-122">On the **Action Pane**, click **Collect**.</span></span>
4. <span data-ttu-id="29141-123">**Sil**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="29141-123">Click **Write off**.</span></span>
5. <span data-ttu-id="29141-124">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="29141-124">Click **OK**.</span></span>
6. <span data-ttu-id="29141-125">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="29141-125">Close the page.</span></span>
7. <span data-ttu-id="29141-126">**Gezinti bölmesi > Modüller > Genel muhasebe > Günlük girişleri > Genel günlükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="29141-126">Go to **Navigation pane > Modules > General ledger > Journal entries > General journals**.</span></span>
8. <span data-ttu-id="29141-127">Silme işleminizi içeren günlüğün günlük toplu iş numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="29141-127">Select the journal batch number for the journal that contains your write-off.</span></span> <span data-ttu-id="29141-128">Müşteri bakiyesini ters kaydetmek için bir satır oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="29141-128">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="29141-129">Silme işlemini silme hesabına nakletmek için bir veya birden fazla satır oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="29141-129">One or more lines are created to post the write-off to the write-off account.</span></span>  
9. <span data-ttu-id="29141-130">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="29141-130">Close the page.</span></span>
10. <span data-ttu-id="29141-131">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="29141-131">Close the page.</span></span>

## <a name="write-off-transactions-from-the-collections-form"></a><span data-ttu-id="29141-132">Hareketleri tahsilatlar formunda silin.</span><span class="sxs-lookup"><span data-stu-id="29141-132">Write off transactions from the collections form.</span></span>
1. <span data-ttu-id="29141-133">**Alacak ve tahsilatlar > Tahsilatlar > Yaşlandırılmış bakiyeler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="29141-133">Go to **Credit and collections > Collections > Aged balances**.</span></span>
2. <span data-ttu-id="29141-134">Silmek istediğiniz hareketlerin sahibi olan müşterinin adını seçin.</span><span class="sxs-lookup"><span data-stu-id="29141-134">Select the name of the customer that has the transactions that you want to write off.</span></span> <span data-ttu-id="29141-135">Örneğin Cave Wholesales (US-004) adını seçin.</span><span class="sxs-lookup"><span data-stu-id="29141-135">For example, select Cave Wholesales (US-004).</span></span>
3. <span data-ttu-id="29141-136">İlk hareketin satırını işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="29141-136">Mark the row for the first transaction.</span></span>
4. <span data-ttu-id="29141-137">İkinci hareketin satırını işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="29141-137">Mark the row for the second transaction.</span></span>
5. <span data-ttu-id="29141-138">**Sil**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="29141-138">Click **Write off**.</span></span>
6. <span data-ttu-id="29141-139">**Neden açıklaması** alanına "Ödenmeyen borçlar" yazın.</span><span class="sxs-lookup"><span data-stu-id="29141-139">In the **Reason comment** field, type 'Bad debts'.</span></span>
7. <span data-ttu-id="29141-140">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="29141-140">Click **OK**.</span></span>
8. <span data-ttu-id="29141-141">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="29141-141">Close the page.</span></span>
9. <span data-ttu-id="29141-142">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="29141-142">Close the page.</span></span>
10. <span data-ttu-id="29141-143">**Genel muhasebe > Günlük girişleri > Genel günlükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="29141-143">Go to **General ledger > Journal entries > General journals**.</span></span>
11. <span data-ttu-id="29141-144">Silme işleminizi içeren günlüğün günlük toplu iş numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="29141-144">Select the journal batch number for the journal that contains your write-off.</span></span> <span data-ttu-id="29141-145">Müşteri bakiyesini ters kaydetmek için bir satır oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="29141-145">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="29141-146">Silme işlemini silme hesabına nakletmek için bir veya birden fazla satır oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="29141-146">One or more lines are created to post the write-off to the write-off account.</span></span>  
12. <span data-ttu-id="29141-147">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="29141-147">Close the page.</span></span>
13. <span data-ttu-id="29141-148">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="29141-148">Close the page.</span></span>

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a><span data-ttu-id="29141-149">Bir faturayı Açık müşteri faturaları sayfasında silin</span><span class="sxs-lookup"><span data-stu-id="29141-149">Write off an invoice from the Open customers invoices page</span></span>
1. <span data-ttu-id="29141-150">**Gezinti bölmesi > Modüller > Alacak hesapları > Faturalar > Açık müşteri faturaları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="29141-150">Go to **Navigation pane > Modules > Accounts receivable > Invoices > Open customer invoices**.</span></span>
2. <span data-ttu-id="29141-151">Bir faturanın satırını işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="29141-151">Mark the line for an invoice.</span></span> <span data-ttu-id="29141-152">Örneğin, CIV-000667'ye ait satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="29141-152">For example, mark the line for CIV-000667.</span></span>
3. <span data-ttu-id="29141-153">**Eylem Bölmesinde** **Fatura** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="29141-153">On the **Action Pane**, click **Invoice**.</span></span>
4. <span data-ttu-id="29141-154">**Sil**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="29141-154">Click **Write off**.</span></span>
5. <span data-ttu-id="29141-155">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="29141-155">Click **OK**.</span></span>
6. <span data-ttu-id="29141-156">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="29141-156">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-customer-page"></a><span data-ttu-id="29141-157">Bir müşteri bakiyesini müşteri sayfasında silin</span><span class="sxs-lookup"><span data-stu-id="29141-157">Write off a customer balance from the customer page</span></span>
1. <span data-ttu-id="29141-158">**Alacak hesapları > Müşteriler > Tüm müşteriler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="29141-158">Go to **Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="29141-159">Bir müşteri hesabı seçin.</span><span class="sxs-lookup"><span data-stu-id="29141-159">Select a customer account.</span></span> <span data-ttu-id="29141-160">Örneğin, US-001 (Contoso Retail San Diego) değerini seçin.</span><span class="sxs-lookup"><span data-stu-id="29141-160">For example, select US-001 (Contoso Retail San Diego).</span></span>
3. <span data-ttu-id="29141-161">**Eylem Bölmesinde**, **Tahsil et** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="29141-161">On the **Action Pane**, click **Collect**.</span></span>
4. <span data-ttu-id="29141-162">**Sil**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="29141-162">Click **Write off**.</span></span>
5. <span data-ttu-id="29141-163">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="29141-163">Click **OK**.</span></span>
6. <span data-ttu-id="29141-164">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="29141-164">Close the page.</span></span>

