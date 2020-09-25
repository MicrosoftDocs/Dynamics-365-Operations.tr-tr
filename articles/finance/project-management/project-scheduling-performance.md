---
title: Proje kaynak planlaması performansı
description: Bu konuda, çok sayıda proje için kaynak planlama performansının nasıl geliştirileceği ile ilgili bilgiler sağlanır.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 988fc83230f08a6534caa7c37784757d73c1cc12
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760689"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="af363-103">Proje kaynak planlaması performansı</span><span class="sxs-lookup"><span data-stu-id="af363-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="af363-104">Kaynak iş planlaması ile ilgili performans sorunları proje sayısı binlere ulaştığında oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="af363-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="af363-105">Kaynak planlama performansını artırmak için, kullanıcıların kaynak kullanılabilirlik formunu başlatmak için gerekli süreyi azaltmasına olanak tanıyan bir özellik sunulmuştur.</span><span class="sxs-lookup"><span data-stu-id="af363-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="af363-106">Bu işlem, kaynak kapasitesi toplaması eşitleme işlemini kaldırır ve kaynak aramasını hızlandırmak için **ResProjectResource** tablosunu kullanır.</span><span class="sxs-lookup"><span data-stu-id="af363-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="af363-107">**Resrollup** tablosunun artık kullanılmayacağını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="af363-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="af363-108">Kaynak kapasitesi toplaması eşitleme işleminde veya **ResProjectResource** tablosunda bir bağımlılık varsa, bu özelliği kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="af363-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="af363-109">Kaynak planlama performansı geliştirme özelliğini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="af363-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="af363-110">Kaynak planlama performansı geliştirmeyi etkinleştirmek için aşağıdaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="af363-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="af363-111">**Özellik yönetimi** > **Tüm** seçeneğine gidin ve özellik listesinde, **Proje kaynak planlaması performans geliştirmesi özelliğini etkinleştir** seçeneğini bulun.</span><span class="sxs-lookup"><span data-stu-id="af363-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="af363-112">**Şimdi etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="af363-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="af363-113">Eğer özelliği listede bulamazsanız, listeyi yenilemek için **Güncelleştirmeleri denetle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="af363-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="af363-114">Tarayıcınızı yenileyin ve **Proje yönetimi ve muhasebe** > **Dönemsel** > **Proje kaynakları** > **Tüm şirketler arasındaki kaynak takvimleri kapasitesini eşitle** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="af363-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="af363-115">Önceki verileri kaldırmak için, **Var olan kapasite kayıtlarını kaldır** öğesini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="af363-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="af363-116">Artımlı veri oluşturmak istiyorsanız, bunu **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="af363-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="af363-117">**Dönem kodu** alanında, verilerin oluşturulması gereken dönemi seçin.</span><span class="sxs-lookup"><span data-stu-id="af363-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="af363-118">Bir dönem kodu seçerseniz, bir başlangıç ve bitiş tarihinin tanımlanması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="af363-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="af363-119">**Dönem kodu** alanını boş bırakırsanız, veri oluşturmak için belirli başlangıç ve bitiş tarihlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="af363-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="af363-120">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="af363-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="af363-121">Bu işlem, genel verileri ortamınızdaki tüm şirketler arasında **ResCalendarCapacity** tablosuna dağıtır, bu nedenle toplu işin yalnızca bir yasal varlıkta çalıştırılması gereklidir.</span><span class="sxs-lookup"><span data-stu-id="af363-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="af363-122">Bu toplu işteki veriler, kaynak kapasitesini ilişkili takvimle hesaplamak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="af363-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="af363-123">**Proje yönetimi ve muhasebe** > **Dönemsel** > **Proje kaynakları** > **Proje kaynaklarını tüm şirketlerde doldur** öğesine gidin **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="af363-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="af363-124">Bu; **ResProjectResource**, **ResCalendarDateTimeRange** ve **ResEffectiveDateTimeRange** tablolarındaki genel veriler için veri yükseltme kodudur.</span><span class="sxs-lookup"><span data-stu-id="af363-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="af363-125">**PSAPRojSchedRole.RootActivity** alanı değerleri de güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="af363-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="af363-126">Bu çalıştırılmadıysa, kaynak planlama işlemlerini yürütmeye çalıştığınızda bir uyarı alırsınız.</span><span class="sxs-lookup"><span data-stu-id="af363-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="af363-127">Kaynak planlama performansı geliştirmeyi kapatma</span><span class="sxs-lookup"><span data-stu-id="af363-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="af363-128">**Özellik yönetimi** > **Tüm** seçeneğine gidin ve **Proje kaynak planlaması performans geliştirmesi özelliğini etkinleştir** seçeneğini bulun.</span><span class="sxs-lookup"><span data-stu-id="af363-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="af363-129">Özelliği seçin ve **Devre dışı bırak** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="af363-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="af363-130">Tarayıcınızı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="af363-130">Refresh your browser.</span></span>
4. <span data-ttu-id="af363-131">**Proje yönetimi ve muhasebe** > **Dönemsel** > **Kapasite eşitleme** > **Kaynakların kapasite toplamlarını eşitle** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="af363-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="af363-132">**Kapasite toplama eşitleme** sayfasında, önceki verileri kaldırmak için, **Var olan kapasite kayıtlarını kaldır** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="af363-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="af363-133">Artımlı veri oluşturmak istiyorsanız, bunu **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="af363-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="af363-134">**Dönem kodu** alanında, verilerin oluşturulması gereken dönemi seçin.</span><span class="sxs-lookup"><span data-stu-id="af363-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="af363-135">Bir dönem kodu seçerseniz, bir başlangıç ve bitiş tarihinin tanımlanması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="af363-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="af363-136">**Dönem kodu** alanını boş bırakırsanız, veri oluşturmak için belirli başlangıç ve bitiş tarihlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="af363-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="af363-137">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="af363-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="af363-138">Bu işlem, genel verileri ortamınızdaki tüm şirketler arasında **ResRollup** tablosuna dağıtır, bu nedenle toplu işin yalnızca bir yasal varlıkta çalıştırılması gereklidir.</span><span class="sxs-lookup"><span data-stu-id="af363-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="af363-139">Bu toplu iş, tüm **Kaynak kullanılabilirliği** görünümlerinde gereklidir.</span><span class="sxs-lookup"><span data-stu-id="af363-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="af363-140">Bu toplu iş çalıştırılmazsa, **ResRolluo** verileri yeniden oluşturulur ve bu işlem zaman alabilir.</span><span class="sxs-lookup"><span data-stu-id="af363-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>
