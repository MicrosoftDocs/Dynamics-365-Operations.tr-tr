---
title: Dataverse tümleştirmesini yapılandırma
description: Microsoft Dataverse ve Dynamics 365 Human Resources arasındaki tümleştirmeyi açabilir veya kapatabilirsiniz. Ayrıca eşitleme ayrıntılarını görüntüleyebilir, izleme verilerini temizleyebilir ve iki ortam arasındaki veri sorunlarını gidermeye yardımcı olmak için bir tabloyu yeniden işleyebilirsiniz.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 721799c9a6fafe0a809f447189ce6814b30ca863
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052469"
---
# <a name="configure-dataverse-integration"></a><span data-ttu-id="1442c-104">Dataverse tümleştirmesini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="1442c-104">Configure Dataverse integration</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1442c-105">Microsoft Dataverse ve Dynamics 365 Human Resources arasındaki tümleştirmeyi açabilir veya kapatabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1442c-105">You can turn integration between Microsoft Dataverse and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="1442c-106">Eşitleme ayrıntılarını görüntüleyebilir, izleme verilerini temizleyebilir ve iki ortam arasındaki veri sorunlarını gidermeye yardımcı olmak için bir tabloyu yeniden işleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1442c-106">You can also view the synchronization details, clear tracking data, and resync a table to help troubleshoot data issues between the two environments.</span></span>

> [!NOTE]
> <span data-ttu-id="1442c-107">Dataverse (önceden Common Data Service) ve terminoloji güncelleştirmeleri hakkında daha fazla bilgi için bkz. [Microsoft Dataverse nedir?](/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="1442c-107">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="1442c-108">Tümleştirmeyi kapattığınızda, kullanıcılar Human Resource veya Dataverse'te değişiklikler yapabilir ancak bu değişiklikler iki ortam arasında eşitlenmez.</span><span class="sxs-lookup"><span data-stu-id="1442c-108">When you turn off integration, users can make changes in Human Resources or Dataverse, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="1442c-109">Varsayılan olarak, Human Resources ve Dataverse arasındaki tümleştirme kapalıdır.</span><span class="sxs-lookup"><span data-stu-id="1442c-109">By default, integration between Human Resources and Dataverse is turned off.</span></span>

<span data-ttu-id="1442c-110">Aşağıdaki durumlarda tümleştirmeyi kapatmak isteyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="1442c-110">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="1442c-111">Verileri, Veri Yönetimi Çerçevesi aracılığıyla dolduruyorsunuzdur ve doğru bir duruma getirmek için verileri birçok defa içe aktarmanız gerekiyordur.</span><span class="sxs-lookup"><span data-stu-id="1442c-111">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="1442c-112">Human Resources veya Dataverse'te verilerle ilgili sorunlar vardır.</span><span class="sxs-lookup"><span data-stu-id="1442c-112">There are issues with data in either Human Resources or Dataverse.</span></span> <span data-ttu-id="1442c-113">Tümleştirmeyi kapatırsanız, bir kaydı bir ortamda silip, diğerinde bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1442c-113">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="1442c-114">Tümleştirmeyi yeniden açtığınız zaman, silme işlemi yapılmayan ortamdaki kayıt, silindiği ortama yeniden eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="1442c-114">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="1442c-115">**Dataverse tümleştirmesi - kaçırılan istek eşitleme** toplu işinin bir sonraki çalıştırılışında eşitleme başlar.</span><span class="sxs-lookup"><span data-stu-id="1442c-115">Synchronization begins the next time the **Dataverse integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="1442c-116">Veri tümleştirmeyi kapattığınızda, her iki ortamda aynı kaydı düzenlemediğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="1442c-116">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="1442c-117">Tümleştirmeyi yeniden açtığınızda, son düzenlediğiniz kayıt eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="1442c-117">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="1442c-118">Bu nedenle, her iki ortamda da kayıtta aynı değişiklikleri yapmadıysanız, veri kaybı oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="1442c-118">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-dataverse-integration-page"></a><span data-ttu-id="1442c-119">Dataverse tümleştirme sayfasına erişim</span><span class="sxs-lookup"><span data-stu-id="1442c-119">Access the Dataverse integration page</span></span>

1. <span data-ttu-id="1442c-120">Dataverse ile tümleştirme için ayarları görüntülemek veya yapılandırmak istediğiniz Human Resources kurulumunda **Sistem yönetimi** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="1442c-120">In the Human Resources instance where you want to view or configure settings for the integration with Dataverse, select the **System administration** tile.</span></span>

    <span data-ttu-id="1442c-121">[![Sistem yönetimi kutucuğu](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="1442c-121">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="1442c-122">**Bağlantılar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1442c-122">Select the **Links** tab.</span></span>

    <span data-ttu-id="1442c-123">[![Bağlantılar sekmesi](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="1442c-123">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="1442c-124">**Tümleştirmeler** altında, **Dataverse yapılandırması**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="1442c-124">Under **Integrations**, select **Dataverse configuration**.</span></span>

    <span data-ttu-id="1442c-125">[![Dataverse yapılandırması bağlantısı](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span><span class="sxs-lookup"><span data-stu-id="1442c-125">[![Dataverse configuration link](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a><span data-ttu-id="1442c-126">Human Resources ve Dataverse arasında tümleştirmeyi açma veya kapatma</span><span class="sxs-lookup"><span data-stu-id="1442c-126">Turn data integration between Human Resources and Dataverse on or off</span></span>

- <span data-ttu-id="1442c-127">Tümleştirmeyi etkinleştirmek için **Microsoft Dataverse tümleştirme** sayfasında **Dataverse tümleştirmesini etkinleştir** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1442c-127">To turn on integration, set the **Enable Dataverse integration** option to **Yes** on the **Microsoft Dataverse integration** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1442c-128">Tümleştirmeyi açarsanız, **Dataverse tümleştirmesi - kaçırılan istek eşitleme** toplu işinin bir sonraki çalıştırılışında veriler eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="1442c-128">When you turn on integration, data will be synced the next time that the **Dataverse integration missed request sync** batch job runs.</span></span> <span data-ttu-id="1442c-129">Toplu iş tamamlandıktan sonra tüm veriler kullanılabilir hale gelecektir.</span><span class="sxs-lookup"><span data-stu-id="1442c-129">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="1442c-130">Tümleştirmeyi kapatmak için, seçeneği **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1442c-130">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="1442c-131">[![Dataverse tümleştirmesini açma veya kapatma](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span><span class="sxs-lookup"><span data-stu-id="1442c-131">[![Turning the Dataverse integration on or off](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span></span>

> [!WARNING]
> <span data-ttu-id="1442c-132">Veri taşıma görevleri gerçekleştirirken Dataverse tümleştirmesini kapatmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="1442c-132">We strongly recommend turning off Dataverse integration while performing data migration tasks.</span></span> <span data-ttu-id="1442c-133">Büyük veri yüklemeleri, performansı önemli ölçüde etkileyebilir.</span><span class="sxs-lookup"><span data-stu-id="1442c-133">Large data uploads can significantly impact performance.</span></span> <span data-ttu-id="1442c-134">Örneğin, 2000 çalışan karşıya yüklemek, tümleştirme etkinleştirildiğinde birkaç saat sürebilir ve devre dışı bırakıldığında bir saatten az olabilir.</span><span class="sxs-lookup"><span data-stu-id="1442c-134">For example, uploading 2000 workers can take several hours when integration is enabled, and less than one hour when it's disabled.</span></span> <span data-ttu-id="1442c-135">Bu örnekte verilen sayılar yalnızca gösterim amaçlıdır.</span><span class="sxs-lookup"><span data-stu-id="1442c-135">The numbers provided in this example are for demonstration purposes only.</span></span> <span data-ttu-id="1442c-136">Kayıtları içe aktarmak için gereken tam süre birçok etkene göre büyük ölçüde değişebilir.</span><span class="sxs-lookup"><span data-stu-id="1442c-136">The exact amount of time it takes to import records can vary greatly based on many factors.</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="1442c-137">Veri tümleştirme ayrıntılarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="1442c-137">View data integration details</span></span>

<span data-ttu-id="1442c-138">**Microsoft Dataverse tümleştirmesi** sayfasının **Yönetim** hızlı sekmesinde, satırların Human Resources ile Dataverse arasında nasıl bağlandığını görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1442c-138">On the **Administration** FastTab of the **Microsoft Dataverse integration** page, you can see how rows are linked together between Human Resources and Dataverse.</span></span>

- <span data-ttu-id="1442c-139">Tablonun satırlarını görüntülemek için **Dataverse tablosu** alanında tabloyu seçin.</span><span class="sxs-lookup"><span data-stu-id="1442c-139">To view the rows for a table, select the table in the **Dataverse table** field.</span></span> <span data-ttu-id="1442c-140">Kılavuz, seçilen tablo ile bağlı tüm satırları gösterir.</span><span class="sxs-lookup"><span data-stu-id="1442c-140">The grid shows all the rows that are linked to the selected table.</span></span>

> [!NOTE]
> <span data-ttu-id="1442c-141">Tüm Dataverse tabloları şu anda listelenmiyor.</span><span class="sxs-lookup"><span data-stu-id="1442c-141">Not all Dataverse tables are currently listed.</span></span> <span data-ttu-id="1442c-142">Kılavuzda yalnızca özel alanların kullanımını destekleyen tablolar görünür.</span><span class="sxs-lookup"><span data-stu-id="1442c-142">Only tables that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="1442c-143">Human Resources'nın sürekli sürümleri aracılığıyla yeni tablolar kullanılabilir hale gelir.</span><span class="sxs-lookup"><span data-stu-id="1442c-143">New tables become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="1442c-144">Kılavuz aşağıdaki alanları içerir:</span><span class="sxs-lookup"><span data-stu-id="1442c-144">The grid includes the following fields:</span></span>

- <span data-ttu-id="1442c-145">**Dataverse tablo** – Dataverse'teki tablonun adı.</span><span class="sxs-lookup"><span data-stu-id="1442c-145">**Dataverse table** – The name of the table in Dataverse.</span></span>
- <span data-ttu-id="1442c-146">**Dataverse tablo başvurusu** – Bir kaydı tanımlamak için Dataverse kullanan tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="1442c-146">**Dataverse table reference** – The identifier that Dataverse uses to identify a record.</span></span> <span data-ttu-id="1442c-147">Bu değer Human Resources'taki bir **Kayıt kodu** değerinin eşdeğeridir.</span><span class="sxs-lookup"><span data-stu-id="1442c-147">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="1442c-148">Dataverse tablosunu Microsoft Excel'de açtığınızda tanımlayıcıyı bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1442c-148">You can find the identifier when you open the Dataverse table in Microsoft Excel.</span></span>
- <span data-ttu-id="1442c-149">**Human Resources varlık adı** – Verileri Dataverse'e en son eşitleyen Human Resources varlığı.</span><span class="sxs-lookup"><span data-stu-id="1442c-149">**Human Resources entity name** – The Human Resources entity that last synced data to Dataverse.</span></span> <span data-ttu-id="1442c-150">Varlık ya Dataverse öneki veya başka bir önek taşımalıdır.</span><span class="sxs-lookup"><span data-stu-id="1442c-150">The entity can have either the Dataverse prefix or another prefix.</span></span>
- <span data-ttu-id="1442c-151">**Human Resources başvurusu** – Human Resources'taki kayıtla ilişkili **Kayıt kodu** değeri.</span><span class="sxs-lookup"><span data-stu-id="1442c-151">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="1442c-152">**Dataverse'ten silindi** – Satırın Dataverse'ten silinip silinmediğini gösteren değer.</span><span class="sxs-lookup"><span data-stu-id="1442c-152">**Deleted from Dataverse** – A value that indicates whether the row was deleted from Dataverse.</span></span>

> [!NOTE]
> <span data-ttu-id="1442c-153">Human Resources'daki kayıtlar, Dataverse'teki satırlara karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="1442c-153">Records in Human Resources correspond to rows in Dataverse.</span></span>

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a><span data-ttu-id="1442c-154">Human Resources kaydının ilişkisini Dataverse satırından kaldırma</span><span class="sxs-lookup"><span data-stu-id="1442c-154">Remove the association of a Human Resources record from a Dataverse row</span></span>

<span data-ttu-id="1442c-155">Human Resources ve Dataverse arasındaki veri eşitleme sırasında sorunlarla karşılaşırsanız, izlemeyi temizleyerek ve izleme tablosunun yeniden eşitlenmesine izin vererek bu sorunları çözebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1442c-155">If you experience issues during data synchronization between Human Resources and Dataverse, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="1442c-156">İlişkilendirmeyi kaldırır ve sonra satırı Dataverse'te değiştirir veya silerseniz, değişiklikler Human Resources ile eşitlenmez.</span><span class="sxs-lookup"><span data-stu-id="1442c-156">If you remove the association, and then change or delete a row in Dataverse, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="1442c-157">Human Resources'da değişiklik yaparsanız, yeni bir izleme kaydı oluşturulur ve satır Dataverse'te güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="1442c-157">If you make changes in Human Resources, a new tracking record is created, and the row is updated in Dataverse.</span></span>

- <span data-ttu-id="1442c-158">Human Resources kaydının ve Dataverse satırının ilişkisini kaldırmak için **Dataverse tablosu** alanında tabloyu seçin ve ardından **İzleme bilgilerini temizle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1442c-158">To remove the association of a Human Resources record and a Dataverse row, select the table in the **Dataverse table** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="1442c-159">[![İzleme bilgilerini temizleme](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="1442c-159">[![Clearing tracking information](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span></span>

<span data-ttu-id="1442c-160">İzlemeyi temizledikten sonra tabloda tam eşitleme çalıştırmak için sonraki yordama bakın.</span><span class="sxs-lookup"><span data-stu-id="1442c-160">To run a full synchronization on the table after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-a-table-between-human-resources-and-dataverse"></a><span data-ttu-id="1442c-161">Human Resources ile Dataverse arasında tablo eşitleme</span><span class="sxs-lookup"><span data-stu-id="1442c-161">Sync a table between Human Resources and Dataverse</span></span>

<span data-ttu-id="1442c-162">Bu yordamı şu durumlarda kullanın:</span><span class="sxs-lookup"><span data-stu-id="1442c-162">Use this procedure when:</span></span>

- <span data-ttu-id="1442c-163">Dataverse'taki değişikliklerin Human Resources'ta görünmesi çok uzun zaman aldığında.</span><span class="sxs-lookup"><span data-stu-id="1442c-163">Changes from Dataverse take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="1442c-164">İzlemeyi temizledikten sonra izleme tablosunu yenilemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1442c-164">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="1442c-165">Human Resources ile Dataverse arasında bir tablonun tam eşitlemesini çalıştırmak için:</span><span class="sxs-lookup"><span data-stu-id="1442c-165">To run a full synchronization on a table between Human Resources and Dataverse:</span></span>

1. <span data-ttu-id="1442c-166">**Dataverse tablosu** alanında tabloyu seçin.</span><span class="sxs-lookup"><span data-stu-id="1442c-166">Select the table in the **Dataverse table** field.</span></span>

2. <span data-ttu-id="1442c-167">**Şimdi eşitle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1442c-167">Select **Sync now**.</span></span>

<span data-ttu-id="1442c-168">[![Tam eşitleme çalıştırma](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="1442c-168">[![Running a full synchronization](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="1442c-169">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="1442c-169">See also</span></span>

[<span data-ttu-id="1442c-170">Dataverse tabloları</span><span class="sxs-lookup"><span data-stu-id="1442c-170">Dataverse tables</span></span>](hr-developer-entities.md)<br>
[<span data-ttu-id="1442c-171">Dataverse sanal tablolarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="1442c-171">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="1442c-172">Human Resources sanal tablolarıyla ilgili SSS</span><span class="sxs-lookup"><span data-stu-id="1442c-172">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="1442c-173">Microsoft Dataverse nedir?</span><span class="sxs-lookup"><span data-stu-id="1442c-173">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="1442c-174">Terminoloji güncelleştirmeleri</span><span class="sxs-lookup"><span data-stu-id="1442c-174">Terminology updates</span></span>](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]