---
title: Deftere nakledilen kira hareketlerini ters kaydetme
description: Bu konu, deftere nakledilen bir kira hareketinin nasıl ters kaydedilebileceğini açıklamaktadır. Varlık Kiralama üzerinden oluşturulan tüm hareketler için ters kayıt oluşturulabilir.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3e4908ddab2650e5ff7e4a28bf916604d165d08c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969540"
---
# <a name="reverse-posted-lease-transactions"></a><span data-ttu-id="7a59e-104">Deftere nakledilen kira hareketlerini ters kaydetme</span><span class="sxs-lookup"><span data-stu-id="7a59e-104">Reverse posted lease transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a59e-105">Varlık Kiralama üzerinden oluşturulan tüm hareketler için ters kayıt oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="7a59e-105">Any transaction that is created through Asset leasing can be reversed.</span></span> <span data-ttu-id="7a59e-106">Varlık kiralama aracılığıyla tersine çevrilen hareketler kiralama verilerinizi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7a59e-106">Transactions that are reversed through Asset leasing update your lease data.</span></span> <span data-ttu-id="7a59e-107">Bu nedenle, kiralama yükümlülüğün ve kullanım hakkı (ROU) varlığının defter değerlerini de güncelleştirirler.</span><span class="sxs-lookup"><span data-stu-id="7a59e-107">Therefore, they also update the carrying values of the lease liability and right-of-use (ROU) asset.</span></span>

<span data-ttu-id="7a59e-108">Bir kiralamanın ters kaydedilen hareketini oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="7a59e-108">To create a reversing transaction for a lease, follow these steps.</span></span>

1. <span data-ttu-id="7a59e-109">**Varlık hareketleri** sayfası veya **Yükümlülük hareketleri** sayfasında hareketi seçin ve ardından **Ters hareket**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7a59e-109">On either the **Asset transactions** page or the **Liability transactions** page, select the transaction, and then select **Reverse transaction**.</span></span>
2. <span data-ttu-id="7a59e-110">Görüntülenen iletişim kutusunda, ters kaydedilen girişinin deftere nakledileceği tarihi düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7a59e-110">In the dialog box that appears, you can edit the date when the reversing entry will be posted.</span></span> <span data-ttu-id="7a59e-111">Varsayılan olarak, **Tarih** alanı seçtiğiniz hareketin hareket deftere nakil tarihine ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="7a59e-111">By default, the **Date** field is set to the transaction posting date of the transaction that you selected.</span></span> <span data-ttu-id="7a59e-112">Ters kaydedilen giriş, seçili hareketin asıl deftere nakil tarihinden daha önceki bir tarihle deftere nakledilemez.</span><span class="sxs-lookup"><span data-stu-id="7a59e-112">The reversing entry can't be posted earlier than the original posting date of the selected transaction.</span></span>
3. <span data-ttu-id="7a59e-113">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7a59e-113">Select **OK**.</span></span> <span data-ttu-id="7a59e-114">Seçtiğiniz girişi tersine çeviren bir günlük girişi deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="7a59e-114">A journal entry is posted that reverses the entry that you selected.</span></span> <span data-ttu-id="7a59e-115">Ters kayıt işlemi, **Varlık hareketleri** veya **Yükümlülük hareketleri** sayfasında gösterilir ve sayfada gösterilen geçerli bakiyenin net toplamı güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="7a59e-115">The reversal is shown on the **Asset transactions** or **Liability transactions** page, and the net total of the current balance that is shown on the page is updated.</span></span>

<span data-ttu-id="7a59e-116">**Ters kayıt izleme**'yi seçtiğinizde, hem orijinal hareketleri, hem de ters kayıt hareketlerini, *izleme numarası* olarak bilinen bağlı bir sayıyla birlikte gösteren bir iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="7a59e-116">When you select **Reverse tracing**, a dialog box appears that shows both the original transactions and the reversed transactions, together with a linked number that is known as a *trace number*.</span></span> <span data-ttu-id="7a59e-117">Ters kayıtların daha iyi anlaşılması ve görünürlüğün artması için kira planlarını kullanarak da ters kayıtları izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7a59e-117">To make the reversals easier to understand and to improve visibility, you can also track reversals by using the lease schedules.</span></span>

<span data-ttu-id="7a59e-118">**Planlama** sayfasındaki **En son günlük numarası** alanı hareketlerin günlük numaralarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7a59e-118">The **Latest journal number** field on the **Schedule** page shows the journal numbers of transactions.</span></span> <span data-ttu-id="7a59e-119">Bir hareket ters kaydedildiğinde, bu alan ters kaydedilen hareketin günlük numarasıyla güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="7a59e-119">When a transaction is reversed, this field is updated with the journal number of a reversing transaction.</span></span> <span data-ttu-id="7a59e-120">Ayrıca, hareketin ters kaydedildiğini gösteren **Ters kaydedildi** onay kutusu ile **Deftere nakledildi** alanı seçilidir.</span><span class="sxs-lookup"><span data-stu-id="7a59e-120">Additionally, the **Reversed** check box is selected to indicate that the transaction is reversed, and the **Posted** field is selected.</span></span>

## <a name="revoke-a-reversed-transaction"></a><span data-ttu-id="7a59e-121">Ters kaydedilen hareketi iptal etme</span><span class="sxs-lookup"><span data-stu-id="7a59e-121">Revoke a reversed transaction</span></span>

<span data-ttu-id="7a59e-122">Tersine kaydedilen hareketi iptal etmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="7a59e-122">To revoke a reversed transaction, follow these steps.</span></span>

1. <span data-ttu-id="7a59e-123">**Planlama** veya **Hareketler** sayfasında orijinal hareketi seçin.</span><span class="sxs-lookup"><span data-stu-id="7a59e-123">On either the **Schedule** page or the **Transactions** page, select the original transaction.</span></span>
2. <span data-ttu-id="7a59e-124">Şu adımlardan birini izleyin:</span><span class="sxs-lookup"><span data-stu-id="7a59e-124">Follow one of these steps:</span></span>

    - <span data-ttu-id="7a59e-125">Hareketi **Planlama** sayfasında seçtiyseniz [Toplu işte aylık günlük girişleri oluşturma](create-monthly-journals-batch.md) konusundaki günlük oluşturma adımlarını izleyin.</span><span class="sxs-lookup"><span data-stu-id="7a59e-125">If you selected the transaction on the **Schedule** page, follow the steps for creating a journal in [Create monthly journal entries in a batch](create-monthly-journals-batch.md).</span></span> <span data-ttu-id="7a59e-126">Günlüğü el ile deftere nakletmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="7a59e-126">You must manually post the journal.</span></span>
    - <span data-ttu-id="7a59e-127">Hareketi **Hareketler** sayfasında seçtiyseniz **Ters hareket**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7a59e-127">If you selected the transaction on the **Transactions** page, select **Reverse transaction**.</span></span> <span data-ttu-id="7a59e-128">Bu iptal işleminin daha önceki bir ters kayıt işleminin iptali olduğunu ve bu iptal işlemi için deftere nakil tarihini düzenleyebileceğinizi bildiren bir ileti alırsınız.</span><span class="sxs-lookup"><span data-stu-id="7a59e-128">You receive a message that states that this revocation is a revocation of an earlier reversal, and that you can edit the posting date for this revocation.</span></span> <span data-ttu-id="7a59e-129">Ancak, genel iş doğrulamaları **Tarih** alanına girilebilecek tarihleri etkiler.</span><span class="sxs-lookup"><span data-stu-id="7a59e-129">However, general business validations affect the dates that can be entered in the **Date** field.</span></span> 

3. <span data-ttu-id="7a59e-130">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7a59e-130">Select **OK**.</span></span> <span data-ttu-id="7a59e-131">Seçtiğiniz girişi tersine çeviren bir günlük girişi deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="7a59e-131">A journal entry is posted that reverses the entry that you selected.</span></span> <span data-ttu-id="7a59e-132">Ters kayıt **Hareketler** sayfasında gösterilir ve net toplam geçerli bakiyesi ilk ters kayıt işleminden önceki durumuna geri yüklenir.</span><span class="sxs-lookup"><span data-stu-id="7a59e-132">The reversal is shown on the **Transactions** page, and the net total current balance is restored to what it was before the first reversal.</span></span> <span data-ttu-id="7a59e-133">Böylece, ters kayıt işleminin bakiyelerdeki etkisi kaldırılmış olur.</span><span class="sxs-lookup"><span data-stu-id="7a59e-133">Therefore, the impact that the reversal had on the balances is negated.</span></span>

<span data-ttu-id="7a59e-134">**Ters kayıt izleme**'yi seçtiğinizde, hem orijinal hareketleri, hem de ters kayıt hareketlerini, bağlı izleme numarasıyla birlikte gösteren bir iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="7a59e-134">When you select **Reverse tracing**, a dialog box appears that shows both the original transactions and the reversed transactions, together with a linked trace number.</span></span>

<span data-ttu-id="7a59e-135">İlgili **Planlamalar** sayfasını kullanarak iptal işlemlerini de izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7a59e-135">You can also track revocations by using the appropriate **Schedules** page.</span></span> <span data-ttu-id="7a59e-136">**Ters kayıt** alanının işareti kaldırılmış, **Günlük deftere nakledildi** alanı seçilidir.</span><span class="sxs-lookup"><span data-stu-id="7a59e-136">The **Reverse** field is cleared, whereas the **Journal posted** field is selected.</span></span> <span data-ttu-id="7a59e-137">Ayrıca, **En son günlük numarası** alanı iptal hareketinin günlük numarasıyla güncelleştirilir ve **Günlük numarası** alanı ters kayıt günlük numarasıyla güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="7a59e-137">Additionally, the **Latest journal number** field is updated with the journal number of the revocation transaction, and the **Journal number** field is updated with the reversal journal number.</span></span>
