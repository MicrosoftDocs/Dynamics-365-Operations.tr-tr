---
title: İş bölme
description: Bu konu, iş bölme işlevi hakkında bilgi sağlar. Bu işlevsellik, büyük iş siparişlerini daha sonra birden çok ambar çalışanına atayabileceğiniz birkaç küçük iş siparişine bölmenize olanak tanır. Bu şekilde, aynı iş aynı anda birkaç ambar çalışanı tarafından çekilebilir.
author: mirzaab
manager: tfehr
ms.date: 10/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: WHSWorkTableListPage
ms.author: mirzaab
ms.search.validFrom: 2020-10-15
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 8a530f3887c3c66295177d480a8c486dd0984153
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965539"
---
# <a name="work-split"></a><span data-ttu-id="e2fac-105">İş bölme</span><span class="sxs-lookup"><span data-stu-id="e2fac-105">Work split</span></span>

<span data-ttu-id="e2fac-106">İş bölme işlevi, büyük iş kimliklerini (diğer bir şekilde, birkaç satırı olan iş emirleri) birden çok ambar çalışanına atayabileceğiniz birkaç küçük işe bölmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="e2fac-106">Work split functionality lets you split large work IDs (that is, work orders that have several lines) into several smaller work IDs that you can then assign to multiple warehouse workers.</span></span> <span data-ttu-id="e2fac-107">Bu şekilde, aynı iş oluşturma numarası aynı anda birkaç ambar çalışanı tarafından çekilebilir.</span><span class="sxs-lookup"><span data-stu-id="e2fac-107">In this way, the same work creation number can be picked simultaneously by several warehouse workers.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e2fac-108">Yalnızca *Açık* veya *Devam ediyor* durumundaki iş emirlerini bölebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e2fac-108">You can split only work orders that have a status of *Open* or *In-progress*.</span></span>

## <a name="turn-on-the-work-split-functionality"></a><span data-ttu-id="e2fac-109">İş bölme işlevini açma</span><span class="sxs-lookup"><span data-stu-id="e2fac-109">Turn on the work split functionality</span></span>

<span data-ttu-id="e2fac-110">İş bölme işlevini kullanamadan önce, özelliği ve sisteminizdeki ön koşul özelliğini açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e2fac-110">Before you can use the work split functionality, you must turn on the feature and its prerequisite feature in your system.</span></span> <span data-ttu-id="e2fac-111">Yöneticiler özelliklerin durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="e2fac-111">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on as required.</span></span>

<span data-ttu-id="e2fac-112">İlk olarak, zaten açık değilse, *Kuruluş genelinde iş engelleme* özelliğini açın.</span><span class="sxs-lookup"><span data-stu-id="e2fac-112">First, turn on the prerequisite *Organization-wide work blocking* feature if it isn't already turned on.</span></span> <span data-ttu-id="e2fac-113">**Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:</span><span class="sxs-lookup"><span data-stu-id="e2fac-113">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="e2fac-114">**Modül:** *Ambar yönetimi*</span><span class="sxs-lookup"><span data-stu-id="e2fac-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="e2fac-115">**Özellik adı:** *Kuruluş çapında işi engelleme*</span><span class="sxs-lookup"><span data-stu-id="e2fac-115">**Feature name:** *Organization-wide work blocking*</span></span>

> [!NOTE]
> <span data-ttu-id="e2fac-116">Bu özellik etkinleştirildiğinde, özellik tüm tüzel kişilerde etkinleştirildikten sonra otomatik olarak bir veri yükseltmesi uygulanır.</span><span class="sxs-lookup"><span data-stu-id="e2fac-116">When this feature is activated, a data upgrade is automatically applied after the feature is turned on across all legal entities.</span></span>

<span data-ttu-id="e2fac-117">Ardından, aşağıdaki şekilde listelenen *İş bölme* özelliğini açın:</span><span class="sxs-lookup"><span data-stu-id="e2fac-117">Next, turn on the *Work split* feature, which is listed in the following way:</span></span>

- <span data-ttu-id="e2fac-118">**Modül:** *Ambar yönetimi*</span><span class="sxs-lookup"><span data-stu-id="e2fac-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="e2fac-119">**Özellik adı:** *İş bölme*</span><span class="sxs-lookup"><span data-stu-id="e2fac-119">**Feature name:** *Work split*</span></span>

## <a name="enhancements-to-the-work-details-and-all-work-pages"></a><span data-ttu-id="e2fac-120">İş ayrıntıları ve Tüm iş sayfalarındaki geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="e2fac-120">Enhancements to the Work details and All work pages</span></span>

<span data-ttu-id="e2fac-121">*İş bölme* özelliği, **İş ayrıntılar** ve **Tüm işler** sayfalarının Eylem Bölmesi'ndeki **İş** sekmesine aşağıdaki iki düğmeyi ekler:</span><span class="sxs-lookup"><span data-stu-id="e2fac-121">The *Work split* feature adds the following two buttons to the **Work** tab on the Action Pane of the **Work details** and **All work** pages:</span></span>

- <span data-ttu-id="e2fac-122">**İşi böl**: Geçerli iş kimliğini ayrı çalışanlar tarafından işlenebilen birden çok küçük iş kimliğine böler.</span><span class="sxs-lookup"><span data-stu-id="e2fac-122">**Split work** – Split the current work ID into multiple smaller work IDs that can be processed by separate workers.</span></span>
- <span data-ttu-id="e2fac-123">**İş bölme oturumunu iptal et**: İş bölme oturumunu iptal eder ve işi işlemeye hazır hale getirir.</span><span class="sxs-lookup"><span data-stu-id="e2fac-123">**Cancel work split session** – Cancel the work split session, and make the work available for processing.</span></span>

<span data-ttu-id="e2fac-124">![İşi böl ve İş bölme oturumunu iptal et düğmeleri](media/Work_split_buttons.png "İşi böl ve İş bölme oturumunu iptal et düğmeleri")</span><span class="sxs-lookup"><span data-stu-id="e2fac-124">![Split work and Cancel work split session buttons](media/Work_split_buttons.png "Split work and Cancel work split session buttons")</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e2fac-125">Aşağıdaki koşullardan herhangi biri karşılanırsa **İşi böl** düğmesi kullanılamaz:</span><span class="sxs-lookup"><span data-stu-id="e2fac-125">The **Split work** button won't be available if any of the following conditions are met:</span></span>
>
> - <span data-ttu-id="e2fac-126">İş durumu, *Açık* veya *Devam ediyor*'dan farklıysa.</span><span class="sxs-lookup"><span data-stu-id="e2fac-126">The work status is something other than *Open* or *In progress*.</span></span>
> - <span data-ttu-id="e2fac-127">Kapsayıcı kimliği, iş kimliğiyle ilişkiliyse.</span><span class="sxs-lookup"><span data-stu-id="e2fac-127">A container ID is associated with the work ID.</span></span> <span data-ttu-id="e2fac-128">(Fiziksel eylemler gerektirdiğinden, bir kapsayıcı sistematik olarak bölünemez.)</span><span class="sxs-lookup"><span data-stu-id="e2fac-128">(A container can't be systematically split, because it requires physical actions.)</span></span>
> - <span data-ttu-id="e2fac-129">İş bir küme ile ilişkiliyse.</span><span class="sxs-lookup"><span data-stu-id="e2fac-129">The work is associated with a cluster.</span></span>
> - <span data-ttu-id="e2fac-130">İş emri türü aşağıdaki türlerden farklıysa:</span><span class="sxs-lookup"><span data-stu-id="e2fac-130">The work order type is something other than one of the following types:</span></span>
>
>    - <span data-ttu-id="e2fac-131">Satış siparişleri</span><span class="sxs-lookup"><span data-stu-id="e2fac-131">Sales orders</span></span>
>    - <span data-ttu-id="e2fac-132">Hammadde çekme</span><span class="sxs-lookup"><span data-stu-id="e2fac-132">Raw material picking</span></span>
>    - <span data-ttu-id="e2fac-133">Transfer sorunu</span><span class="sxs-lookup"><span data-stu-id="e2fac-133">Transfer issue</span></span>
>
> - <span data-ttu-id="e2fac-134">İş şu anda başka bir kullanıcı tarafından bölünmektedir.</span><span class="sxs-lookup"><span data-stu-id="e2fac-134">The work is currently being split by another user.</span></span> <span data-ttu-id="e2fac-135">Zaten başka bir kullanıcı tarafından bölünmekte olan iş için bölme sayfasını açmaya çalışırsanız aşağıdaki hata iletisini alırsınız: "\#\#\#\# kimliğine sahip iş şu anda bölünmektedir.</span><span class="sxs-lookup"><span data-stu-id="e2fac-135">If you try to open the splitting page for work that is already being split by another user, you receive the following error message: "The work with ID \#\#\#\# is currently being split.</span></span> <span data-ttu-id="e2fac-136">Birkaç dakika içinde tekrar deneyin.</span><span class="sxs-lookup"><span data-stu-id="e2fac-136">Retry in a few minutes.</span></span> <span data-ttu-id="e2fac-137">Bu iletiyi almaya devam ederseniz bir denetçiye başvurun."</span><span class="sxs-lookup"><span data-stu-id="e2fac-137">If you continue to receive this message, contact a supervisor."</span></span>

<span data-ttu-id="e2fac-138">Yeni bir iş engelleme nedeni, *İşi böl*, iş kimliği bölme işleminin devam etmekte olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="e2fac-138">A new work blocking reason, *Split work*, indicates when the work ID is in the process of being split.</span></span> <span data-ttu-id="e2fac-139">Bir kullanıcı işi çalıştırmaya çalışırsa hem **İşi böl** sayfasında hem de ambar uygulamasında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="e2fac-139">It's shown both on the **Split work** page and in the warehouse app if a user tries to run the work.</span></span> <span data-ttu-id="e2fac-140">Engelleme nedenleri kullanıldığında, iş kimliğindeki **Engellenen dalga** alanının adı **Engellendi** olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="e2fac-140">When blocking reasons are used, the name of the **Blocked wave** field from the work ID is changed to **Blocked**.</span></span>

## <a name="initiate-a-work-split"></a><span data-ttu-id="e2fac-141">İş bölme işlemi başlatma</span><span class="sxs-lookup"><span data-stu-id="e2fac-141">Initiate a work split</span></span>

<span data-ttu-id="e2fac-142">Özellik, kullanıcıların iş satırlarını iş kimliğinden ayırmasına olanak tanıyan yeni bir **İşi böl** sayfası ekler.</span><span class="sxs-lookup"><span data-stu-id="e2fac-142">The feature adds a new **Split work** page that lets users split work lines from the work ID.</span></span> <span data-ttu-id="e2fac-143">Sayfa ilk açıldığında, *Açık* iş durumu olan ve bölünebilecek satırlar gösterilir.</span><span class="sxs-lookup"><span data-stu-id="e2fac-143">When the page is first opened, it shows lines that have a work status of *Open* and that are available to be split.</span></span> <span data-ttu-id="e2fac-144">Eylem Bölmesi'nde, seçili işi işlemek için **İşi böl**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="e2fac-144">On the Action Pane, select **Split work** to process the selected work.</span></span>

<span data-ttu-id="e2fac-145">İşi bölmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e2fac-145">To split work, follow these steps.</span></span>

1. <span data-ttu-id="e2fac-146">Aşağıdaki iş sayfalarından birini açın:</span><span class="sxs-lookup"><span data-stu-id="e2fac-146">Open one of the following work pages:</span></span>

    - <span data-ttu-id="e2fac-147">**İş Ayrıntıları** (**Ambar yönetimi \> İş \> İş ayrıntıları**)</span><span class="sxs-lookup"><span data-stu-id="e2fac-147">**Work details** (**Warehouse management \> Work \> Work details**)</span></span>
    - <span data-ttu-id="e2fac-148">**Tüm iş** (**Ambar yönetimi \> İş \> Tüm iş**)</span><span class="sxs-lookup"><span data-stu-id="e2fac-148">**All work** (**Warehouse management \> Work \> All work**)</span></span>

1. <span data-ttu-id="e2fac-149">Kılavuzda, bölünecek bir iş kimliği seçin.</span><span class="sxs-lookup"><span data-stu-id="e2fac-149">In the grid, select a work ID to split.</span></span> <span data-ttu-id="e2fac-150">**İş emri türü** alanı, aşağıdaki değerlerden birine ayarlanmalıdır:</span><span class="sxs-lookup"><span data-stu-id="e2fac-150">The **Work order type** field must be set to one of the following values:</span></span>

    - <span data-ttu-id="e2fac-151">Satış siparişleri</span><span class="sxs-lookup"><span data-stu-id="e2fac-151">Sales orders</span></span>
    - <span data-ttu-id="e2fac-152">Hammadde çekme</span><span class="sxs-lookup"><span data-stu-id="e2fac-152">Raw material picking</span></span>
    - <span data-ttu-id="e2fac-153">Transfer sorunu</span><span class="sxs-lookup"><span data-stu-id="e2fac-153">Transfer issue</span></span>

1. <span data-ttu-id="e2fac-154">Eylem Bölmesinde **İş** sekmesindeki **İş** grubunda **İşi böl**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="e2fac-154">On the Action Pane, on the **Work** tab, in the **Work** group, select **Split work**.</span></span>

    <span data-ttu-id="e2fac-155">**İşi böl** sayfası görüntülenir ve açık ve bölünebilecek iş satırlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e2fac-155">The **Split work** page appears and shows the work lines that are open and available to be split.</span></span> <span data-ttu-id="e2fac-156">Varsayılan olarak, yalnızca kullanılabilir iş satırları gösterilir.</span><span class="sxs-lookup"><span data-stu-id="e2fac-156">By default, only available work lines are shown.</span></span> <span data-ttu-id="e2fac-157">İş kimliği için tüm satırları görüntülemek için (örneğin, *Yerine koyma* iş türüne sahip satırlar), kılavuzun üzerindeki **Tüm satırları göster** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="e2fac-157">To view all lines for the work ID (for example, lines that have a work type of *Put*), select the **Show all lines** check box above the grid.</span></span>

    <span data-ttu-id="e2fac-158">Aşağıdaki ileti gösterilir: "Kullanıcılar, siz bölmeyi bitirip bu sayfayı kapatana kadar işin satırlarını işleyemez."</span><span class="sxs-lookup"><span data-stu-id="e2fac-158">The following message is shown: "Users can't process lines of the work until you finish splitting and close this page."</span></span>

    <span data-ttu-id="e2fac-159">Geçerli işin **İş engelleme nedeni** alanı *İşi böl* olarak ayarlanır ve iş engellenir.</span><span class="sxs-lookup"><span data-stu-id="e2fac-159">The **Work blocking reason** field for the current work will be set to *Split work*, and the work will be blocked.</span></span>

    <span data-ttu-id="e2fac-160">![Engelleme nedeni](media/Blocking_reason.png "Engelleme nedeni")</span><span class="sxs-lookup"><span data-stu-id="e2fac-160">![Blocking reason](media/Blocking_reason.png "Blocking reason")</span></span>

1. <span data-ttu-id="e2fac-161">Geçerli iş kimliğinden kaldırılacak satırları seçin ve yeni bir iş kimliği ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e2fac-161">Select the lines to remove from the current work ID and add to a new work ID.</span></span> <span data-ttu-id="e2fac-162">Aşağıdaki olaylar gerçekleşir:</span><span class="sxs-lookup"><span data-stu-id="e2fac-162">The following events occur:</span></span>

    - <span data-ttu-id="e2fac-163">İşi böldüğünüzde, seçili satır veya özgün iş kimliğindeki satırlar iptal edilir ve ardından yeni bir iş kimliğine kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="e2fac-163">When you split the work, the selected line or lines from the original work ID are canceled and then copied to a new work ID.</span></span>
    - <span data-ttu-id="e2fac-164">Var olan iş şablonu yapısı ve yerine koyma konumu (ve ayrıca gelecekteki malzeme çekme/yerine koyma çiftleri) korunur.</span><span class="sxs-lookup"><span data-stu-id="e2fac-164">The existing work template structure and the location of the put (and also future pick/put pairs) are preserved.</span></span> <span data-ttu-id="e2fac-165">Aşağıdaki iş kimliği alanlarının değerleri özgün işten yeni işe kopyalanır:</span><span class="sxs-lookup"><span data-stu-id="e2fac-165">Values for the following work ID fields are copied from the original work to the new work:</span></span>

        - <span data-ttu-id="e2fac-166">Yük kodu</span><span class="sxs-lookup"><span data-stu-id="e2fac-166">Load ID</span></span>
        - <span data-ttu-id="e2fac-167">Sevkiyat Kodu</span><span class="sxs-lookup"><span data-stu-id="e2fac-167">Shipment ID</span></span>
        - <span data-ttu-id="e2fac-168">İş siparişi türü</span><span class="sxs-lookup"><span data-stu-id="e2fac-168">Work order type</span></span>
        - <span data-ttu-id="e2fac-169">Sipariş numarası</span><span class="sxs-lookup"><span data-stu-id="e2fac-169">Order number</span></span>
        - <span data-ttu-id="e2fac-170">Tesis</span><span class="sxs-lookup"><span data-stu-id="e2fac-170">Site</span></span>
        - <span data-ttu-id="e2fac-171">Ambar</span><span class="sxs-lookup"><span data-stu-id="e2fac-171">Warehouse</span></span>
        - <span data-ttu-id="e2fac-172">İş önceliği</span><span class="sxs-lookup"><span data-stu-id="e2fac-172">Work priority</span></span>
        - <span data-ttu-id="e2fac-173">İş havuzu kodu</span><span class="sxs-lookup"><span data-stu-id="e2fac-173">Work pool ID</span></span>
        - <span data-ttu-id="e2fac-174">Dalga kodu</span><span class="sxs-lookup"><span data-stu-id="e2fac-174">Wave ID</span></span>
        - <span data-ttu-id="e2fac-175">İş oluşturma numarası</span><span class="sxs-lookup"><span data-stu-id="e2fac-175">Work creation number</span></span>

    - <span data-ttu-id="e2fac-176">Aşağıdaki alanlar yeni iş kimliğine kopyalanır:</span><span class="sxs-lookup"><span data-stu-id="e2fac-176">The following fields aren't copied to the new work ID:</span></span>

        - <span data-ttu-id="e2fac-177">**İş Kimliği**: Uygun numara dizisinden yeni bir iş kimliği oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e2fac-177">**Work ID** – A new work ID is generated from the appropriate number sequence.</span></span>
        - <span data-ttu-id="e2fac-178">**İş durumu**: Bu alanı *Açık* konumuna ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e2fac-178">**Work status** – This field is set to *Open*.</span></span>
        - <span data-ttu-id="e2fac-179">**Kilitleyen**: Bu alan başlangıçta boş olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="e2fac-179">**Locked by** – This field is initially set to blank.</span></span>
        - <span data-ttu-id="e2fac-180">**Hedef plaka kimliği**: Bu alan boş bırakılır.</span><span class="sxs-lookup"><span data-stu-id="e2fac-180">**Target license plate ID** – This field is left blank.</span></span>
        - <span data-ttu-id="e2fac-181">**Oluşturulma tarihi ve saati**: Bu alan mevcut tarih ve saate ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="e2fac-181">**Created date and time** – This field is set to the current date and time.</span></span>
        - <span data-ttu-id="e2fac-182">**Engellenen dalga/dondurulmuş**: Bu alan, özgün iş kimliği ve yeni iş kimliği için yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="e2fac-182">**Blocked wave/frozen** – This field is recomputed for the original work ID and the new work ID.</span></span>

1. <span data-ttu-id="e2fac-183">Eylem bölmesinde **İşi böl**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="e2fac-183">On the Action Pane, select **Split work**.</span></span>

<span data-ttu-id="e2fac-184">İş bölünürken, aşağıdaki ileti gösterilir: "İşlem işleniyor - İşi böl".</span><span class="sxs-lookup"><span data-stu-id="e2fac-184">While the work is being split, the following message is shown: "Processing operation - Split work".</span></span> <span data-ttu-id="e2fac-185">Bu ileti görünürken, ileti kutusunda **İptal**'i seçerek işlemi iptal edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e2fac-185">While this message is visible, you can cancel the operation by selecting **Cancel** in the message box.</span></span>

<span data-ttu-id="e2fac-186">**Tüm satırları göster** onay kutusu temizlenirse bölünen ve iptal edilen satır artık kılavuzda görünmez.</span><span class="sxs-lookup"><span data-stu-id="e2fac-186">If the **Show all lines** check box is cleared, the line that was split off and canceled will no longer appear in the grid.</span></span> <span data-ttu-id="e2fac-187">Onay kutusu seçilirse, bu satırın **İş durumu** alanının değerinin *İptal* olarak değiştirildiğini görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="e2fac-187">If the check box is selected, you should see that the value of the **Work status** field for that line has changed to *Canceled*.</span></span>

<span data-ttu-id="e2fac-188">Yeni iş kimliğinin oluşturulduğunu belirtmek için aşağıdaki bildirim gösterilir: "\#\#\#\# işi, özgün \#\#\#\# işinden bölünerek oluşturuldu."</span><span class="sxs-lookup"><span data-stu-id="e2fac-188">The following notification is shown to indicate that the new work ID has been created: "Work \#\#\#\# has been created by splitting off from original work \#\#\#\#."</span></span>

<span data-ttu-id="e2fac-189">Özgün iş kimliğindeki diğer iş satırları (*Yerine koyma* satırları gibi) iptal edilen iş satırlarını yansıtacak şekilde gerektiği gibi ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="e2fac-189">Other work lines from the original work ID (such as *Put* lines) will be adjusted as required to reflect the lines of work that have been canceled.</span></span> <span data-ttu-id="e2fac-190">Örneğin, özgün iş kimliğinde 15'lik bir miktar için *Yerine Koyma* satırı varsa ve toplam miktarı 10 olan *Malzeme Çekme* satırları iptal edildiyse, özgün iş kimliğindeki yeni *Yerine Koyma* miktarı artık 5 olur.</span><span class="sxs-lookup"><span data-stu-id="e2fac-190">For example, if the original work ID had a *Put* line for a quantity of 15, and *Pick* lines that have a total quantity of 10 were canceled, the new *Put* quantity on the original work ID will now be 5.</span></span>

<span data-ttu-id="e2fac-191">Yeni iş hemen bir kullanıcıya atanmaz.</span><span class="sxs-lookup"><span data-stu-id="e2fac-191">The new work won't immediately be assigned to any user.</span></span> <span data-ttu-id="e2fac-192">Ancak **İş ayrıntıları** sayfasının standart işlevselliğini kullanarak gerektiğinde kullanıcıya atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e2fac-192">However, you can assign it to a user now, as required, by using the standard functionality of the **Work details** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e2fac-193">Yalnızca iki veya daha fazla kullanılabilir iş satırı içeren iş kimliklerini bölebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e2fac-193">You can split only work IDs that contain two or more available work lines.</span></span> <span data-ttu-id="e2fac-194">Yalnızca bir iş satırı olduğunda **İşi böl**'ü seçerseniz aşağıdaki hata iletisini alırsınız: "En az bir iş satırı ilk işte kalmalıdır."</span><span class="sxs-lookup"><span data-stu-id="e2fac-194">If you select **Split work** when there is only one work line, you will receive the following error message: "At least one work line must remain on initial work."</span></span> <span data-ttu-id="e2fac-195">Bu durumda, hiçbir bölme işlemi gerçekleşmez.</span><span class="sxs-lookup"><span data-stu-id="e2fac-195">In this case, no splitting will occur.</span></span>

## <a name="finish-a-work-split"></a><span data-ttu-id="e2fac-196">İş bölmeyi bitirme</span><span class="sxs-lookup"><span data-stu-id="e2fac-196">Finish a work split</span></span>

<span data-ttu-id="e2fac-197">İşi bölmeyi sonlandırmak için *İşi böl* engelleme nedeninin kaldırılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="e2fac-197">To finish splitting work, the *Split work* blocking reason must be removed.</span></span> <span data-ttu-id="e2fac-198">Bu adımı tamamlamanın iki yolu vardır:</span><span class="sxs-lookup"><span data-stu-id="e2fac-198">There are two ways to complete this step:</span></span>

- <span data-ttu-id="e2fac-199">İşi bölen kullanıcı, sağ üst köşedeki **Kapat** düğmesini **(X)** seçerek **İşi böl** sayfasını kapatır.</span><span class="sxs-lookup"><span data-stu-id="e2fac-199">The user who is splitting the work closes the **Split work** page by selecting the **Close** button (**X**) in the upper-right corner.</span></span> <span data-ttu-id="e2fac-200">Sayfa kapatıldığında, *İşi Böl* engelleme nedeni kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="e2fac-200">When the page is closed, the *Split Work* blocking reason will be removed.</span></span> <span data-ttu-id="e2fac-201">Bu işin *Engellendi* durumu yeniden hesaplanacaktır ve bu işin kalan engelleme nedeni yoksa, işin engeli kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="e2fac-201">The *Blocked* state of this work will be recomputed and, if there are no remaining blocking reasons for this work, the work will be unblocked.</span></span>
- <span data-ttu-id="e2fac-202">Herhangi bir kullanıcı iş kimliğini açar ve Eylem Bölmesi'ndeki **İş bölme oturumunu iptal et** düğmesini seçer.</span><span class="sxs-lookup"><span data-stu-id="e2fac-202">Any user opens the work ID and selects the **Cancel work split session** button on the Action Pane.</span></span> <span data-ttu-id="e2fac-203">*İşi böl* engelleme nedeni kaldırılır ve bu işin *Engellendi* durumu, **İşi böl** sayfası kapatıldığında yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="e2fac-203">The *Split work* blocking reason will be removed, and the *Blocked* state of this work will be recomputed, just as when the **Split work** page is closed.</span></span>

<span data-ttu-id="e2fac-204">*İşi böl* engelleme nedeni kaldırıldıktan sonra, **Engelledi** durumunun iş kimliğinde *Hayır* olarak ayarlanmış olması koşuluyla, iş mobil cihazda çalıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="e2fac-204">After the *Split work* blocking reason is removed, the work can be run on the mobile device, provided that the **Blocked** state is set to *No* on the work ID.</span></span>

## <a name="user-blocking-on-the-warehouse-app"></a><span data-ttu-id="e2fac-205">Ambar uygulamasında kullanıcı engelleme</span><span class="sxs-lookup"><span data-stu-id="e2fac-205">User blocking on the warehouse app</span></span>

<span data-ttu-id="e2fac-206">Ambar uygulamasını, bölünmekte olan bir iş kimliğine karşı malzeme çekme işini çalıştırmak için kullanmaya çalışırsanız aşağıdaki hata iletisini alırsınız: "\#\#\#\# kimlikli iş şu anda bölünmektedir."</span><span class="sxs-lookup"><span data-stu-id="e2fac-206">If you try to use the warehouse app to run picking work against a work ID that is being split, you will receive the following error message: "The work with ID \#\#\#\# is currently being split."</span></span> <span data-ttu-id="e2fac-207">Bu iletiyi alırsanız **İptal et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e2fac-207">If you receive this message, select **Cancel**.</span></span> <span data-ttu-id="e2fac-208">Daha sonra diğer işleri işlemeye devam edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e2fac-208">You can then continue to process other work.</span></span>

## <a name="other-blocked-operations"></a><span data-ttu-id="e2fac-209">Engellenen diğer işlemler</span><span class="sxs-lookup"><span data-stu-id="e2fac-209">Other blocked operations</span></span>

<span data-ttu-id="e2fac-210">İş satırlarını, iş stok hareketlerini veya bölünen işle ilgili stok yenileme bağlantılarını değiştiren işlemler başarısız olur ve aşağıdaki hata iletisi gösterilir: "\#\#\#\# kimlikli iş şu anda bölünmektedir."</span><span class="sxs-lookup"><span data-stu-id="e2fac-210">Any operations that modify work lines, work inventory transactions, or replenishment links that are related to work that is being split will fail, and the following error message will be shown: "The work with ID \#\#\#\# is currently being split."</span></span>
