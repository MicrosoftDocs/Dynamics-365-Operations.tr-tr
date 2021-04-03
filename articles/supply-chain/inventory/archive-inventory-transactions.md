---
title: Stok hareketlerini arşivleme
description: Bu konuda, sistem performansını artırmaya yardımcı olmak için stok hareketi verilerinin nasıl arşivleneceği açıklanmaktadır.
author: sherry-zheng
manager: tfehr
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransArchiveProcessForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 3a0fa65eb728e4ce96bdfc3f7a0f04901551ccea
ms.sourcegitcommit: 70b1567d316f19c15a4b032b4897f15c8dcdca09
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/08/2021
ms.locfileid: "5556447"
---
# <a name="archive-inventory-transactions"></a><span data-ttu-id="0d087-103">Stok hareketlerini arşivleme</span><span class="sxs-lookup"><span data-stu-id="0d087-103">Archive inventory transactions</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="0d087-104">Zamanla, stok hareketleri tablosu (`InventTrans`) büyümeye ve daha fazla veritabanı alanı tüketmeye devam eder.</span><span class="sxs-lookup"><span data-stu-id="0d087-104">Over time, the inventory transactions table (`InventTrans`) will continue to grow and consume more database space.</span></span> <span data-ttu-id="0d087-105">Bu nedenle, tabloya göre yapılan sorgular zamanla yavaşlar.</span><span class="sxs-lookup"><span data-stu-id="0d087-105">Therefore, queries that are made against the table will gradually become slower.</span></span> <span data-ttu-id="0d087-106">Bu konuda, sistem performansını artırmaya yardımcı olmak için stok hareketleri hakkındaki verileri arşivlemek için *Stok hareketlerini arşivleme* özelliğini nasıl kullanabileceğiniz açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="0d087-106">This topic describes how you can use the *Inventory transactions archive* feature to archive data about inventory transactions to help improve system performance.</span></span>

> [!NOTE]
> <span data-ttu-id="0d087-107">Seçili kapalı genel muhasebe döneminde yalnızca mali olarak güncelleştirilmiş stok hareketleri arşivlenebilir.</span><span class="sxs-lookup"><span data-stu-id="0d087-107">Only financially updated inventory transactions can be archived in a selected closed ledger period.</span></span> <span data-ttu-id="0d087-108">Arşivlenebilmesi için mali olarak güncelleştirilmiş gidiş stok hareketlerinin *Satıldı* çıkış durumuna sahip olması ve geliş stok hareketlerinin giriş durumunun *Satın alındı* olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="0d087-108">To be archived, financially updated outbound inventory transactions must have an issue status of *Sold*, and inbound inventory transactions must have a receipt status of *Purchased*.</span></span>

<span data-ttu-id="0d087-109">Stok hareketlerini arşivlediğinizde, ilgili tüm hareketler `InventTransArchive` tablosuna taşınır.</span><span class="sxs-lookup"><span data-stu-id="0d087-109">When you archive inventory transactions, all related transactions are moved to the `InventTransArchive` table.</span></span> <span data-ttu-id="0d087-110">Stok çıkış hareketleri ve stok girişi hareketleri, madde kodu (`itemId`) ve stok boyutu kimliği (`inventDimId`) kombinasyonuna göre ayrı ayrı arşivlenir ve özetlenen çıkış ve özetlenen giriş hareketlerine yerleştirilir.</span><span class="sxs-lookup"><span data-stu-id="0d087-110">Inventory issue transactions and inventory receipt transactions are archived separately, based on the combination of the item ID (`itemId`) and inventory dimension ID (`inventDimId`), and they are put into the summarized issue and summarized receipt transactions.</span></span>

<span data-ttu-id="0d087-111">Bir `itemId` ve `inventDimId` kombinasyonu yalnızca bir giriş veya çıkış hareketi içeriyorsa hareket arşivlenmez.</span><span class="sxs-lookup"><span data-stu-id="0d087-111">If an `itemId` and `inventDimId` combination contains only one receipt or issue transaction, the transaction won't be archived.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="0d087-112">Sisteminizdeki özelliği etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="0d087-112">Turn on the feature in your system</span></span>

<span data-ttu-id="0d087-113">Sisteminiz bu konuda açıklanan özellikleri zaten içermiyorsa [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ne gidin ve *Stok hareketlerini arşivleme* özelliğini açın.</span><span class="sxs-lookup"><span data-stu-id="0d087-113">If your system doesn't already include the features that is described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Inventory transactions archive* feature.</span></span>

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a><span data-ttu-id="0d087-114">Stok hareketlerini arşivlemeden önce dikkat edilmesi gerekenler</span><span class="sxs-lookup"><span data-stu-id="0d087-114">Things to consider before you archive inventory transactions</span></span>

<span data-ttu-id="0d087-115">Stok hareketlerini arşivlemeden önce, işlemden etkilenecekleri için aşağıdaki iş senaryolarını göz önünde bulundurmalısınız:</span><span class="sxs-lookup"><span data-stu-id="0d087-115">Before you archive inventory transactions, you should consider the following business scenarios, because they will be affected by the operation:</span></span>

- <span data-ttu-id="0d087-116">Satın alma siparişi satırları gibi ilgili belgelerden stok hareketlerini denetlediğinizde, bunlar arşivlenmiş olarak gösterilir.</span><span class="sxs-lookup"><span data-stu-id="0d087-116">When you audit inventory transactions from related documents, such as purchase order lines, they will be shown as archived.</span></span> <span data-ttu-id="0d087-117">Arşivlenen hareketleri gözden geçirmek için **Stok yönetimi \> Periyodik görevler \> Temizleme \> Stok hareketlerini arşivleme**'ye gitmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="0d087-117">To review the archived transactions, you must go to **Inventory management \> Periodic tasks \> Clean up \> Inventory transactions archive**.</span></span>
- <span data-ttu-id="0d087-118">Arşivlenen dönemler için stok kapanışı iptal edilemez.</span><span class="sxs-lookup"><span data-stu-id="0d087-118">Inventory closing can't be canceled for archived periods.</span></span> <span data-ttu-id="0d087-119">Stok kapanışını iptal etmek için önce ilgili döneme ait stok hareketi arşivini tersine çevirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="0d087-119">Before you can cancel an inventory closing, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="0d087-120">Arşivlenen dönemler için standart maliyet dönüştürme işlemi yapılamaz.</span><span class="sxs-lookup"><span data-stu-id="0d087-120">Standard cost conversion can't be done for archived periods.</span></span> <span data-ttu-id="0d087-121">Standart maliyet dönüştürmeyi yapmadan önce, ilgili dönem için stok hareketi arşivini tersine çevirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="0d087-121">Before you can do standard cost conversion, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="0d087-122">Stok hareketlerini arşivlediğinizde, stok hareketlerinden elde edilen stok raporları etkilenir.</span><span class="sxs-lookup"><span data-stu-id="0d087-122">Inventory reports that are sourced from inventory transactions will be affected when you archive inventory transactions.</span></span> <span data-ttu-id="0d087-123">Bu raporlar stok yaşlandırma raporunu ve stok değer raporlarını içerir.</span><span class="sxs-lookup"><span data-stu-id="0d087-123">These reports include the inventory aging report and inventory value reports.</span></span>
- <span data-ttu-id="0d087-124">Stok tahminleri, arşivlenen dönemlerin öngörülen süreleri sırasında çalıştırılırsa etkilenebilir.</span><span class="sxs-lookup"><span data-stu-id="0d087-124">Inventory forecasts might be affected if they are run during the time horizon of archived periods.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0d087-125">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="0d087-125">Prerequisites</span></span>

<span data-ttu-id="0d087-126">Stok hareketleri yalnızca aşağıdaki koşulların karşılandığı dönemlerde arşivlenebilir:</span><span class="sxs-lookup"><span data-stu-id="0d087-126">Inventory transactions can be archived only during periods where the following conditions are met:</span></span>

- <span data-ttu-id="0d087-127">Genel muhasebe dönemi kapatılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0d087-127">The ledger period must be closed.</span></span>
- <span data-ttu-id="0d087-128">Stok kapanışı, arşivin dönem bitiş tarihinde veya sonrasında çalıştırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0d087-128">Inventory closing must be run on or after the to-period date of the archive.</span></span>
- <span data-ttu-id="0d087-129">Dönem, arşivin dönem tarihinden en az bir yıl önce olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0d087-129">The period must be at least one year before the from-period date of the archive.</span></span>
- <span data-ttu-id="0d087-130">Mevcut stok yeniden hesaplamaları bulunmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="0d087-130">There must not be any existing inventory recalculations.</span></span>

## <a name="archive-inventory-transactions"></a><span data-ttu-id="0d087-131">Stok hareketlerini arşivleme</span><span class="sxs-lookup"><span data-stu-id="0d087-131">Archive inventory transactions</span></span>

<span data-ttu-id="0d087-132">Stok hareketlerini arşivlemek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="0d087-132">To archive inventory transactions, follow these steps.</span></span>

1. <span data-ttu-id="0d087-133">**Stok yönetimi** \> **Periyodik görevler** \> **Temizleme** \> **Stok hareketlerini arşivleme**’ye gidin.</span><span class="sxs-lookup"><span data-stu-id="0d087-133">Go to **Inventory management** \> **Periodic tasks** \> **Clean up** \> **Inventory transaction archive**.</span></span>

    <span data-ttu-id="0d087-134">**Stok hareketlerini arşivleme** sayfası görüntülenir ve arşivlenen işlem kayıtlarının listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0d087-134">The **Inventory transactions archive** page appears and shows a list of archived process records.</span></span>

    <span data-ttu-id="0d087-135">![Stok hareketlerini arşivleme sayfası](media/archive-inventory-empty.png "Stok hareketlerini arşivleme sayfası")</span><span class="sxs-lookup"><span data-stu-id="0d087-135">![Inventory transactions archive page](media/archive-inventory-empty.png "Inventory transactions archive page")</span></span>

1. <span data-ttu-id="0d087-136">Stok hareketi arşivi oluşturmak için Eylem Bölmesinde **Stok hareketlerini arşivleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0d087-136">On the Action Pane, select **Inventory transactions archive** to create an inventory transaction archive.</span></span>
1. <span data-ttu-id="0d087-137">**Stok hareketlerini arşivleme** iletişim kutusunda, **Parametreler** hızlı sekmesinde aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="0d087-137">In the **Inventory transactions archive** dialog box, on the **Parameters** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="0d087-138">**Kapalı genel muhasebe dönemindeki başlangıç tarihi**: Arşive dahil edilecek en erken hareket tarihini seçin.</span><span class="sxs-lookup"><span data-stu-id="0d087-138">**From date in closed ledger period** – Select the earliest transaction date to include in the archive.</span></span>
    - <span data-ttu-id="0d087-139">**Kapalı genel muhasebe dönemindeki bitiş tarihi**: Arşive dahil etmek için en son hareket tarihini seçin.</span><span class="sxs-lookup"><span data-stu-id="0d087-139">**To date in closed ledger period** – Select the latest transaction date to include in the archive.</span></span>

    <span data-ttu-id="0d087-140">![Stok hareketlerini arşivleme iletişim kutusu](media/archive-inventory-dates.png "Stok hareketlerini arşivleme iletişim kutusu")</span><span class="sxs-lookup"><span data-stu-id="0d087-140">![Inventory transactions archive dialog box](media/archive-inventory-dates.png "Inventory transactions archive dialog box")</span></span>

    > [!NOTE]
    > <span data-ttu-id="0d087-141">Yalnızca [ön koşulları](#prerequisites) karşılayan dönemler seçim için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0d087-141">Only periods that meet the [prerequisites](#prerequisites) will be available for selection.</span></span>

1. <span data-ttu-id="0d087-142">**Arka planda çalıştır** hızlı sekmesinde, toplu işleme ayrıntılarını gerektiği gibi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0d087-142">On the **Run in the background** FastTab, set up batch processing details as you require.</span></span> <span data-ttu-id="0d087-143">Microsoft Dynamics 365 Supply Chain Management'taki toplu işler için tipik adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="0d087-143">Follow the usual steps for batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="0d087-144">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0d087-144">Select **OK**.</span></span>
1. <span data-ttu-id="0d087-145">Devam etmek istediğinizi onaylamanızı isteyen bir ileti alırsınız.</span><span class="sxs-lookup"><span data-stu-id="0d087-145">You receive a message that prompts you to confirm that you want to continue.</span></span> <span data-ttu-id="0d087-146">İletiyi dikkatlice okuyun ve devam etmek istiyorsanız **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0d087-146">Read the message carefully, and then select **Yes** if you want to continue.</span></span>

    <span data-ttu-id="0d087-147">Stok hareketlerini arşivleme işinizin toplu iş kuyruğuna eklendiğini bildiren bir ileti alırsınız.</span><span class="sxs-lookup"><span data-stu-id="0d087-147">You receive a message that states that your inventory transactions archive job has been added to the batch queue.</span></span> <span data-ttu-id="0d087-148">İş artık seçili dönemdeki stok hareketlerini arşivlemeye başlayacaktır.</span><span class="sxs-lookup"><span data-stu-id="0d087-148">The job will now start to archive inventory transactions from the selected period.</span></span>

## <a name="view-archived-inventory-transactions"></a><span data-ttu-id="0d087-149">Arşivlenmiş stok hareketlerini görüntüle</span><span class="sxs-lookup"><span data-stu-id="0d087-149">View archived inventory transactions</span></span>

<span data-ttu-id="0d087-150">**Stok hareketlerini arşivleme** sayfası arşivleme geçmişinizin tamamını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0d087-150">The **Inventory transactions archive** page shows your full archiving history.</span></span> <span data-ttu-id="0d087-151">Kılavuzdaki her satır, arşivin oluşturulduğu tarih, oluşturan kullanıcı ve durumu gibi bilgileri gösterir.</span><span class="sxs-lookup"><span data-stu-id="0d087-151">Each row in the grid shows information such as the date when the archive was created, the user who created it, and its status.</span></span>

<span data-ttu-id="0d087-152">![Stok hareketlerini arşivleme sayfasındaki arşivleme geçmişi](media/archive-inventory-full.png "Stok hareketlerini arşivleme sayfasındaki arşivleme geçmişi")</span><span class="sxs-lookup"><span data-stu-id="0d087-152">![Archiving history on the Inventory transactions archive page](media/archive-inventory-full.png "Archiving history on the Inventory transactions archive page")</span></span>

<span data-ttu-id="0d087-153">Sayfanın üst kısmında açılan listede, kılavuzda gösterilen arşivlere filtre uygulamak için aşağıdaki değerlerden birini seçin:</span><span class="sxs-lookup"><span data-stu-id="0d087-153">In the drop-down list at the top of the page select one of the following values to filter the archives that are shown in the grid:</span></span>

- <span data-ttu-id="0d087-154">**Etkin**: Ters çevrilen arşivleri değil, yalnızca etkin arşivleri göster.</span><span class="sxs-lookup"><span data-stu-id="0d087-154">**Active** – Show only active archives, not reversed archives.</span></span>
- <span data-ttu-id="0d087-155">**Tümü**: Hem etkin hem de ters çevrilen tüm arşivleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="0d087-155">**All** – Show all archives, both active and reversed.</span></span>

<span data-ttu-id="0d087-156">Kılavuzdaki her arşiv için aşağıdaki bilgiler sağlanır:</span><span class="sxs-lookup"><span data-stu-id="0d087-156">For each archive in the grid, the following information is provided:</span></span>

- <span data-ttu-id="0d087-157">**Etkin**: Onay işareti arşivin etkin olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="0d087-157">**Active** – A check mark indicates that the archive is active.</span></span>
- <span data-ttu-id="0d087-158">**Başlangıç tarihi**: Arşive dahil edilebilen en eski hareketin tarihi.</span><span class="sxs-lookup"><span data-stu-id="0d087-158">**From date** – The date of the oldest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="0d087-159">**Son tarih**: Arşive dahil edilebilen en son hareketin tarihi.</span><span class="sxs-lookup"><span data-stu-id="0d087-159">**To date** – The date of the latest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="0d087-160">**Zamanlayan**: Arşivi oluşturan kullanıcı hesabı.</span><span class="sxs-lookup"><span data-stu-id="0d087-160">**Scheduled by** – The user account that created the archive.</span></span>
- <span data-ttu-id="0d087-161">**Yürütülme tarihi**: Arşivin oluşturulduğu tarih.</span><span class="sxs-lookup"><span data-stu-id="0d087-161">**Executed** – The date when the archive was created.</span></span>
- <span data-ttu-id="0d087-162">**Ters**: Onay işareti arşivin tersine çevrildiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0d087-162">**Reverse** – A check mark indicates that the archive has been reversed.</span></span>
- <span data-ttu-id="0d087-163">**Geçerli güncelleştirmeyi durdur**: Onay işareti arşivin devam ettiğini ancak duraklatıldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0d087-163">**Stop current update** – A check mark indicates that the archive is in progress, but it has been paused.</span></span>
- <span data-ttu-id="0d087-164">**Durum**: Arşivin işleme durumu.</span><span class="sxs-lookup"><span data-stu-id="0d087-164">**State** – The processing status of the archive.</span></span> <span data-ttu-id="0d087-165">Olası değerler *Beklemede*, *Devam Ediyor* ve *Tamamlandı*'dır.</span><span class="sxs-lookup"><span data-stu-id="0d087-165">The possible values are *Waiting*, *In progress*, and *Finished*.</span></span>

<span data-ttu-id="0d087-166">Kılavuzun üstündeki araç çubuğu, seçili bir arşivle çalışmak için kullanabileceğiniz aşağıdaki düğmeleri sağlar:</span><span class="sxs-lookup"><span data-stu-id="0d087-166">The toolbar above the grid provides the following buttons that you can use to work with a selected archive:</span></span>

- <span data-ttu-id="0d087-167">**Arşivlenen hareketler**: Seçili arşivin tüm ayrıntılarını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="0d087-167">**Archived transactions** – View the full details of the selected archive.</span></span> <span data-ttu-id="0d087-168">Görüntülenen **Arşivlenen hareketler** sayfası arşivdeki tüm hareketleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="0d087-168">The **Archived transactions** page that appears shows all the transactions in the archive.</span></span>

    <span data-ttu-id="0d087-169">![Arşivlenen hareketler sayfası](media/archive-inventory-transactions.png "Arşivlenen hareketler sayfası")</span><span class="sxs-lookup"><span data-stu-id="0d087-169">![Archived transactions page](media/archive-inventory-transactions.png "Archived transactions page")</span></span>

    <span data-ttu-id="0d087-170">**Arşivlenen hareketler** sayfasında belirli bir hareket hakkında daha fazla bilgi görüntülemek için kılavuzda hareketi seçin ve sonra eylem bölmesinde **Arşivlenen işlem ayrıntıları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="0d087-170">To view more information about a specific transaction on the **Archived transactions** page, select it in the grid, and then, on the Action Pane, select **Archived transaction details**.</span></span> <span data-ttu-id="0d087-171">Görüntülenen **Arşivlenen hareket ayrıntıları** sayfası, genel muhasebe deftere nakli, ilgili alt genel muhasebe referansları ve mali boyutlar gibi bilgileri gösterir.</span><span class="sxs-lookup"><span data-stu-id="0d087-171">The **Archived transaction details** page that appears shows information such as the ledger posting, related subledger references, and financial dimensions.</span></span>

- <span data-ttu-id="0d087-172">**Arşivlemeyi duraklat**: İşlenmekte olan seçili arşivi duraklatın.</span><span class="sxs-lookup"><span data-stu-id="0d087-172">**Pause archiving** – Pause a selected archive that is currently being processed.</span></span> <span data-ttu-id="0d087-173">Duraklatma yalnızca arşivleme görevi oluşturulduktan sonra etkinleşir.</span><span class="sxs-lookup"><span data-stu-id="0d087-173">The pause takes effect only after the archiving task has been generated.</span></span> <span data-ttu-id="0d087-174">Bu nedenle, duraklatma etkili olmadan önce kısa bir gecikme olabilir.</span><span class="sxs-lookup"><span data-stu-id="0d087-174">Therefore, there might be a short delay before the pause takes effect.</span></span> <span data-ttu-id="0d087-175">Bir arşiv duraklatılmışsa **Geçerli güncelleştirmeyi durdur** alanında bir onay işareti görünür.</span><span class="sxs-lookup"><span data-stu-id="0d087-175">If an archive has been paused, a check mark appears in its **Stop current update** field.</span></span>
- <span data-ttu-id="0d087-176">**Arşivlemeye devam et**: Şu anda duraklatılmış olan seçili bir arşiv için işlemeyi devam ettirir.</span><span class="sxs-lookup"><span data-stu-id="0d087-176">**Resume archiving** – Resume processing for a selected archive that is currently paused.</span></span>
- <span data-ttu-id="0d087-177">**Ters Çevir**: Seçili arşivi ters çevirin.</span><span class="sxs-lookup"><span data-stu-id="0d087-177">**Reverse** – Reverse the selected archive.</span></span> <span data-ttu-id="0d087-178">Arşivi yalnızca **Durum** alanı *Tamamlandı* olarak ayarlanmışsa tersine çevirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0d087-178">You can reverse an archive only if its **State** field is set to *Finished*.</span></span> <span data-ttu-id="0d087-179">Arşiv tersine çevrilmişse **Ters** alanında bir onay işareti görünür.</span><span class="sxs-lookup"><span data-stu-id="0d087-179">If an archive has been reversed, a check mark appears in its **Reverse** field.</span></span>
