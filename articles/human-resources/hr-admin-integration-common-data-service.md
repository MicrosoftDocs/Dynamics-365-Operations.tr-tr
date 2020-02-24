---
title: Common Data Service tümleştirmesini yapılandırma
description: Common Data Service ve bir Microsoft Dynamics 365 Human Resources kurulumu arasında tümleştirmeyi açabilir veya kapatabilirsiniz. Ayrıca, eşitleme ayrıntılarını görüntüleyebilir, izleme verilerini temizleyebilir ve iki ortam arasındaki veri sorunlarının giderilmesine yardımcı olarak bir varlığı yeniden eşitleyebilirsiniz.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 042daf3fdf7a906086af726472da050467d217e3
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010836"
---
# <a name="configure-common-data-service-integration"></a><span data-ttu-id="d1ae4-104">Common Data Service tümleştirmesini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="d1ae4-104">Configure Common Data Service integration</span></span>

<span data-ttu-id="d1ae4-105">Common Data Service ve bir Microsoft Dynamics 365 Human Resources kurulumu arasında tümleştirmeyi açabilir veya kapatabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-105">You can turn integration between Common Data Service and an instance of Microsoft Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="d1ae4-106">Ayrıca, eşitleme ayrıntılarını görüntüleyebilir, izleme verilerini temizleyebilir ve iki ortam arasındaki veri sorunlarının giderilmesine yardımcı olarak bir varlığı yeniden eşitleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-106">You can also view the synchronization details, clear tracking data, and resync an entity to help troubleshoot data issues between the two environments.</span></span>

<span data-ttu-id="d1ae4-107">Tümleştirmeyi kapattığınızda, kullanıcılar Human Resource veya Common Data Service'te değişiklikler yapabilir ancak bu değişiklikler iki ortam arasında eşitlenmez.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-107">When you turn off integration, users can make changes in Human Resources or Common Data Service, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="d1ae4-108">Varsayılan olarak, Human Resources ile Common Data Service arasındaki tümleştirme, ortamlardaki tanıtım verilerinin varlığına bağlı olarak açık veya kapalıdır:</span><span class="sxs-lookup"><span data-stu-id="d1ae4-108">By default, integration between Human Resources and Common Data Service is turned either off or on, depending on the presence of demo data in the environments:</span></span>

- <span data-ttu-id="d1ae4-109">Tanıtım verileri içermeyen yeni ortamlar için **Kapalı**</span><span class="sxs-lookup"><span data-stu-id="d1ae4-109">**Off** for new environments that don't include demo data</span></span>
- <span data-ttu-id="d1ae4-110">Tanıtım verileri içeren yeni ortamlar için **Açık**</span><span class="sxs-lookup"><span data-stu-id="d1ae4-110">**On** for new environments that include demo data</span></span>

<span data-ttu-id="d1ae4-111">Tanıtım verileri içeren yeni ortamlar, verileri alınca eşitlemeye başlayacaktır.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-111">New environments that include demo data will start to sync data when they are provisioned.</span></span>

<span data-ttu-id="d1ae4-112">Aşağıdaki durumlarda tümleştirmeyi kapatmak isteyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="d1ae4-112">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="d1ae4-113">Verileri, Veri Yönetimi Çerçevesi aracılığıyla dolduruyorsunuzdur ve doğru bir duruma getirmek için verileri birçok defa içe aktarmanız gerekiyordur.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-113">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="d1ae4-114">Human Resources veya Common Data Service'te verilerle ilgili sorunlar vardır.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-114">There are issues with data in either Human Resources or Common Data Service.</span></span> <span data-ttu-id="d1ae4-115">Tümleştirmeyi kapatırsanız, bir kaydı bir ortamda silip, diğerinde bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-115">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="d1ae4-116">Tümleştirmeyi yeniden açtığınız zaman, silme işlemi yapılmayan ortamdaki kayıt, silindiği ortama yeniden eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-116">When you turn integration back on, the record in the environment where it wasn't deleted will be synced back to the environment where it was deleted.</span></span> <span data-ttu-id="d1ae4-117">**Common Data Service tümleştirmesi - kaçırılan istek eşitleme** toplu işinin bir sonraki çalıştırılışında eşitleme başlar.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-117">Synchronization begins the next time the **Common Data Service integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="d1ae4-118">Veri tümleştirmeyi kapattığınızda, her iki ortamda aynı kaydı düzenlemediğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-118">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="d1ae4-119">Tümleştirmeyi yeniden açtığınızda, son düzenlediğiniz kayıt eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-119">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="d1ae4-120">Bu nedenle, her iki ortamda da kayıtta aynı değişiklikleri yapmadıysanız, veri kaybı oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-120">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-common-data-service-integration-page"></a><span data-ttu-id="d1ae4-121">Common Data Service tümleştirme sayfasına erişim</span><span class="sxs-lookup"><span data-stu-id="d1ae4-121">Access the Common Data Service integration page</span></span>

1. <span data-ttu-id="d1ae4-122">Common Data Service ile tümleştirme için ayarları görüntülemek veya yapılandırmak istediğiniz Human Resources kurulumunda **Sistem yönetimi** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-122">In the Human Resources instance where you want to view or configure settings for the integration with Common Data Service, select the **System administration** tile.</span></span>

    <span data-ttu-id="d1ae4-123">[![Sistem yönetimi kutucuğu](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="d1ae4-123">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="d1ae4-124">**Bağlantılar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-124">Select the **Links** tab.</span></span>

    <span data-ttu-id="d1ae4-125">[![Bağlantılar sekmesi](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="d1ae4-125">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="d1ae4-126">**Tümleştirmeler** altında, **Common Data Service yapılandırması**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-126">Under **Integrations**, select **Common Data Service configuration**.</span></span>

    <span data-ttu-id="d1ae4-127">[![Common Data Service yapılandırması bağlantısı](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="d1ae4-127">[![Common Data Service configuration link](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a><span data-ttu-id="d1ae4-128">Human Resources ve Common Data Service arasında tümleştirmeyi açma veya kapatma</span><span class="sxs-lookup"><span data-stu-id="d1ae4-128">Turn data integration between Human Resources and Common Data Service on or off</span></span>

- <span data-ttu-id="d1ae4-129">Tümleştirmeyi açmak için, **Common Data Service'e tümleştirmeyi etkinleştir** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-129">To turn on integration, set the **Enable the integration to the Common Data Service** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d1ae4-130">Tümleştirmeyi açarsanız, **Common Data Service tümleştirmesi - kaçırılan istek eşitleme** toplu işinin bir sonraki çalıştırılışında veriler eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-130">When you turn on integration, data will be synced the next time that the **Common Data Service integration missed request sync** batch job runs.</span></span> <span data-ttu-id="d1ae4-131">Toplu iş tamamlandıktan sonra tüm veriler kullanılabilir hale gelecektir.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-131">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="d1ae4-132">Tümleştirmeyi kapatmak için, seçeneği **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-132">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="d1ae4-133">[![Common Data Service tümleştirmesini açma veya kapatma](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="d1ae4-133">[![Turning the Common Data Service integration on or off](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="d1ae4-134">Veri tümleştirme ayrıntılarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="d1ae4-134">View data integration details</span></span>

<span data-ttu-id="d1ae4-135">**Common Data Service tümleştirmesi** sayfasının **Yönetim** hızlı sekmesinde, kayıtların Human Resources ve Common Data Service arasında birbirlerine nasıl bağlandığını görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-135">On the **Administration** FastTab of the **Common Data Service integration** page, you can see how records are linked together between Human Resources and Common Data Service.</span></span>

- <span data-ttu-id="d1ae4-136">Bir varlığın kayıtlarını görüntülemek için, **CDS varlığının adı** alanında varlığı seçin.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-136">To view the records for an entity, select the entity in the **CDS entity name** field.</span></span> <span data-ttu-id="d1ae4-137">Kılavuz, seçilen varlıkla bağlantılı tüm kayıtları gösterir.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-137">The grid shows all the records that are linked to the selected entity.</span></span>

<span data-ttu-id="d1ae4-138">[![Bir varlığın kayıtlarını görüntüleme](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span><span class="sxs-lookup"><span data-stu-id="d1ae4-138">[![Viewing the records for an entity](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span></span>

> [!NOTE]
> <span data-ttu-id="d1ae4-139">Şu anda tüm Common Data Service varlıkları listede değildir.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-139">Not all Common Data Service entities are currently listed.</span></span> <span data-ttu-id="d1ae4-140">Yalnızca özel alanların kullanımını destekleyen varlıklar kılavuzda görünür.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-140">Only entities that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="d1ae4-141">Human Resources'ın devam eden sürümleriyle yeni varlıklar sunuluyor.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-141">New entities become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="d1ae4-142">Kılavuz aşağıdaki alanları içerir:</span><span class="sxs-lookup"><span data-stu-id="d1ae4-142">The grid includes the following fields:</span></span>

- <span data-ttu-id="d1ae4-143">**CDS varlığının adı** – Common Data Service'teki varlığın adı.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-143">**CDS entity name** – The name of the entity in Common Data Service.</span></span>
- <span data-ttu-id="d1ae4-144">**CD varlığı başvurusu** – Common Data Service'in bir kaydı belirlemek için kullandığı tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-144">**CDS entity reference** – The identifier that Common Data Service uses to identify a record.</span></span> <span data-ttu-id="d1ae4-145">Bu değer Human Resources'taki bir**Kayıt kodu** değerinin eşdeğeridir.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-145">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="d1ae4-146">Common Data Service varlığını Microsoft Excel'de açtığınız zaman tanımlayıcıyı bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-146">You can find the identifier when you open the Common Data Service entity in Microsoft Excel.</span></span>
- <span data-ttu-id="d1ae4-147">**Human Resources varlığının adı** – Verileri Common Data Service'e en son eşitlenen varlık.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-147">**Human Resources entity name** – The entity that last synced data to Common Data Service.</span></span> <span data-ttu-id="d1ae4-148">Varlık ya Common Data Service öneki veya başka bir önek taşımalıdır.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-148">The entity can have either the Common Data Service prefix or another prefix.</span></span>
- <span data-ttu-id="d1ae4-149">**Human Resources başvurusu** – Human Resources'taki kayıtla ilişkili **Kayıt kodu** değeri.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-149">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="d1ae4-150">**CDS'den silindi** – Kaydın Common Data Service'ten silinip silinmediğini gösteren bir değer.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-150">**Was deleted from CDS** – A value that indicates whether the record was deleted from Common Data Service.</span></span>

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a><span data-ttu-id="d1ae4-151">Human Resources'taki bir kaydın ilişkilendirmesini Common Data Service'tan kaldırma</span><span class="sxs-lookup"><span data-stu-id="d1ae4-151">Remove the association of a record in Human Resources from Common Data Service</span></span>

<span data-ttu-id="d1ae4-152">Human Resources ve Common Data Service arasındaki veri eşitleme sırasında sorunlarla karşılaşırsanız, izlemeyi temizleyerek ve izleme tablosunun yeniden eşitlenmesine izin vererek bu sorunları çözebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-152">If you experience issues during data synchronization between Human Resources and Common Data Service, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="d1ae4-153">İlişkilendirmeyi kaldırır ve Common Data Service'te bir kaydı değiştirir veya silerseniz, değişiklikler Human Resources'a eşitlenmez.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-153">If you remove the association, and then change or delete a record in Common Data Service, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="d1ae4-154">Human Resources'ta değişiklikler yaparsanız yeni bir izleme kaydı oluşturulur ve kayıt Common Data Service'te güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-154">If you make changes in Human Resources, a new tracking record is created, and the record is updated in Common Data Service.</span></span>

- <span data-ttu-id="d1ae4-155">Human Resources ve Common Data Service arasında bir kaydın ilişkilendirmesini kaldırmak için, **CDS varlığının adı** alanında varlığı ve ardından **İzleme bilgilerini temizle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-155">To remove the association of a record between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="d1ae4-156">[![İzleme bilgilerini temizleme](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="d1ae4-156">[![Clearing tracking information](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span></span>

<span data-ttu-id="d1ae4-157">İzlemeyi temizledikten sonra varlıkta bir tam eşitleme çalıştırmak için, sonraki yordama bakın.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-157">To run a full synchronization on the entity after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a><span data-ttu-id="d1ae4-158">Varlığı Human Resources ve Common Data Service arasında eşitleme</span><span class="sxs-lookup"><span data-stu-id="d1ae4-158">Sync an entity between Human Resources and Common Data Service</span></span>

<span data-ttu-id="d1ae4-159">Common Data Service'teki değişikliklerin Human Resources'ta görünmesi çok uzun sürüyorsa veya izlemeyi temizledikten sonra izleme tablosunu yenilemeniz gerekiyorsa bu yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-159">Use this procedure if changes from Common Data Service are taking too long to appear in Human Resources, or if you must refresh the tracking table after you clear the tracking.</span></span>

- <span data-ttu-id="d1ae4-160">Human Resources ve Common Data Service arasında bir varlık üzerinde tam eşitleme çalıştırmak için **CDS varlığının adı** alanında varlığı seçin ve **Şimdi eşitle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d1ae4-160">To run a full synchronization on an entity between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Sync now**.</span></span>

<span data-ttu-id="d1ae4-161">[![Tam eşitleme çalıştırma](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="d1ae4-161">[![Running a full synchronization](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span></span>


