---
title: "Mali raporlama veri reyonunu sıfırlama"
description: "Bu konuda Mali raporlama veri reyonunun nasıl sıfırlanacağı açıklanmaktadır."
author: aolson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 5b956dcc5a4a93033396ae0ffcf8b7aeba2cf3f2
ms.openlocfilehash: a07e8b5bae2c4f71e9212cd2f8080d2481769818
ms.contentlocale: tr-tr
ms.lasthandoff: 12/14/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a><span data-ttu-id="68527-103">Mali raporlama veri reyonunu sıfırlama</span><span class="sxs-lookup"><span data-stu-id="68527-103">Reset the Financial reporting data mart</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="68527-104">Bu konu Mali raporlama veri reyonunun aşağıdaki sürümler için nasıl sıfırlanacağını açıklar:</span><span class="sxs-lookup"><span data-stu-id="68527-104">This topic explains how to reset the Financial reporting data mart for the following versions:</span></span>

- <span data-ttu-id="68527-105">Microsoft Dynamics 365 for Finance and Operations Mali raporlama sürüm 7.2.6.0 veya üstü</span><span class="sxs-lookup"><span data-stu-id="68527-105">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>
- <span data-ttu-id="68527-106">Microsoft Dynamics 365 for Finance and Operations Mali raporlama sürüm 7.0.10000.4 veya üstü</span><span class="sxs-lookup"><span data-stu-id="68527-106">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>
- <span data-ttu-id="68527-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (şirket içi)</span><span class="sxs-lookup"><span data-stu-id="68527-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises)</span></span>

<span data-ttu-id="68527-108">Finance and Operations Mali raporlama sürüm 7.2.6.0'ı edinmek için <https://fix.lcs.dynamics.com/Issue/Resolved?kb=4052514>adresinden KB 4052514'ü indirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="68527-108">To get Finance and Operations Financial reporting release 7.2.6.0, you can download KB 4052514 from <https://fix.lcs.dynamics.com/Issue/Resolved?kb=4052514>.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a><span data-ttu-id="68527-109">Finance and Operations Mali raporlama sürüm 7.2.6.0 ve üstü için Mali raporlama veri reyonunu sıfırlama</span><span class="sxs-lookup"><span data-stu-id="68527-109">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a><span data-ttu-id="68527-110">Mali raporlama veri reyonunu Rapor tasarımcısından sıfırlama</span><span class="sxs-lookup"><span data-stu-id="68527-110">Reset the Financial reporting data mart from Report designer</span></span>

> [!NOTE]
> <span data-ttu-id="68527-111">Bu işlemdeki adımlar, Finance and Operations Mali raporlama sürüm 7.2.6.0 ve üstü için desteklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="68527-111">The steps in this process are supported for Finance and Operations Financial reporting release 7.2.6.0 and later.</span></span> <span data-ttu-id="68527-112">Önceki bir sürüme sahipseniz, Yardım için Destek ekibine başvurun.</span><span class="sxs-lookup"><span data-stu-id="68527-112">If you have an earlier release, contact the Support team for assistance.</span></span>

<span data-ttu-id="68527-113">Belirli senaryolarda, Mali raporlama için veri reyonunu sıfırlamanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="68527-113">In specific scenarios, you might have to reset the data mart for Financial reporting.</span></span> <span data-ttu-id="68527-114">Rapor Tasarımcısı istemcisinde bu görevi gerçekleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="68527-114">You can complete this task in the Report designer client.</span></span> <span data-ttu-id="68527-115">Veri merkezini sıfırlamanızı gerektirebilecek bazı senaryolar aşağıda verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="68527-115">Here are some scenarios where you might have to reset the data mart:</span></span>

- <span data-ttu-id="68527-116">Finance and Operations veri tabanı geri yüklendir, ancak veri reyonu veri tabanı geri yüklenmedi.</span><span class="sxs-lookup"><span data-stu-id="68527-116">The Finance and Operations database was restored, but the data mart database wasn't restored.</span></span>
- <span data-ttu-id="68527-117">Bir dönem için yanlış veriler görüyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="68527-117">You see incorrect data for a period.</span></span>
- <span data-ttu-id="68527-118">Destek, sorun giderme işleminin bir adımı olarak veri reyonunu sıfırlamanızı söylüyor.</span><span class="sxs-lookup"><span data-stu-id="68527-118">Support instructs you to reset the data mart as part of a troubleshooting step.</span></span>

<span data-ttu-id="68527-119">Veri reyonu sıfırlama yalnızca veritabanındaki işlem gerçekleştirme miktarı küçük olduğunda yapılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="68527-119">The data mart reset should be done only during times when the amount of processing on the database is small.</span></span> <span data-ttu-id="68527-120">Mali raporlama sıfırlama işlemi sırasında kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="68527-120">Financial reporting will be unavailable during the reset process.</span></span>

#### <a name="reset-the-data-mart"></a><span data-ttu-id="68527-121">Veri reyonunu sıfırlama</span><span class="sxs-lookup"><span data-stu-id="68527-121">Reset the data mart</span></span>

<span data-ttu-id="68527-122">Veri reyonunu sıfırlamak için Rapor tasarımcısında, **Araçlar** menüsünden **Veri Reyonunu Sıfırla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="68527-122">To reset the data mart, in Report designer, on the **Tools** menu, select **Reset Data Mart**.</span></span> <span data-ttu-id="68527-123">Görüntülenen iletişim kutusunda iki bölüm vardır: **İstatistikler** ve **Sıfırla**.</span><span class="sxs-lookup"><span data-stu-id="68527-123">The dialog box that appears has two sections: **Statistics** and **Reset**.</span></span>

<span data-ttu-id="68527-124">[![Veri Reyonunu Sıfırla iletişim kutusu](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span><span class="sxs-lookup"><span data-stu-id="68527-124">[![Reset Data Mart dialog box](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span></span>

##### <a name="integration-attempts"></a><span data-ttu-id="68527-125">Tümleştirme denemeleri</span><span class="sxs-lookup"><span data-stu-id="68527-125">Integration attempts</span></span>

<span data-ttu-id="68527-126">**Tümleştirme denemeleri** kılavuzu sistemin hareketleri tümleştirmek için kaç kez girişimde bulunduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="68527-126">The **Integration attempts** grid shows how many times the system has tried to integrate transactions.</span></span> <span data-ttu-id="68527-127">Sistem ilk birkaç deneme başarılı olmazsa verileri birkaç günlük bir dönem içinde tümleştirmeyi denemeye devam eder.</span><span class="sxs-lookup"><span data-stu-id="68527-127">The system continues to try to integrate data over a period of days if the first few attempts aren't successful.</span></span> <span data-ttu-id="68527-128">Deneme sayısının 8 veya üzerinde olması ve biçok Boyut kombinasyonu veya Hareket kaydı bulunması durumunda veri reyonunun sıfırlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="68527-128">You will know that the data mart must be reset is if the number of attempts is 8 or more, and if there are many Dimension combination or Transaction records.</span></span> <span data-ttu-id="68527-129">Bu durumda, veriler rapor edilmeyecektir.</span><span class="sxs-lookup"><span data-stu-id="68527-129">In this situation, the data won't be reported on.</span></span>

##### <a name="data-status"></a><span data-ttu-id="68527-130">Veri durumu</span><span class="sxs-lookup"><span data-stu-id="68527-130">Data status</span></span>

<span data-ttu-id="68527-131">**Veri durumu** kılavuzu, veri reyonundaki hareketlerin, döviz kurlarının ve boyut değerlerinin anlık görüntüsünü sağlar.</span><span class="sxs-lookup"><span data-stu-id="68527-131">The **Data status** grid provides a snapshot of the transactions, exchange rates, and dimension values in the data mart.</span></span> <span data-ttu-id="68527-132">Çok sayıda eski kayıt kayıtlara çok sayıda güncelleştirme yapıldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="68527-132">A large number of stale records indicates that numerous updates to the records have occurred.</span></span> <span data-ttu-id="68527-133">Bu durum daha yavaş rapor oluşturma sürelerine neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="68527-133">This situation might cause slower report generation times.</span></span>

##### <a name="misaligned-main-account-categories"></a><span data-ttu-id="68527-134">Yanlış düzenlenmiş ana hesap kategorileri</span><span class="sxs-lookup"><span data-stu-id="68527-134">Misaligned main account categories</span></span>

<span data-ttu-id="68527-135">Microsoft Dynamics 365 for Finance and Operations Mali raporlama sürümü 7.2.1'den daha eski bir sürüm kullanıyorsanız, hesapları yeniden adlandırmanız ve hesapları hesap kategorileri arasında taşımanız durumunda veri reyonunu sıfırlamanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="68527-135">If you're using a release that is earlier than Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.1, you might have to reset the data mart if you rename accounts and move accounts between account categories.</span></span> <span data-ttu-id="68527-136">Bu eylemler ana hesap kategorilerinin hatalı düzenlenmiş duruma gelmesine neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="68527-136">These actions can cause main account categories to become misaligned.</span></span> <span data-ttu-id="68527-137">**Yanlış düzenlenmiş ana hesap kategorileri** alanı, bu sorunla karşı karşıya olup olmadığınızı gösterir.</span><span class="sxs-lookup"><span data-stu-id="68527-137">The **Misaligned main account categories** field shows whether you're experiencing that issue.</span></span>

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a><span data-ttu-id="68527-138">Finance and Operations Mali raporlama sürümü 7.2.6.0'da veri reyonunu sıfırlama</span><span class="sxs-lookup"><span data-stu-id="68527-138">Reset the data mart in Finance and Operations Financial reporting release 7.2.6.0</span></span>

<span data-ttu-id="68527-139">Finance and Operations Mali raporlama sürümü 7.2.6.0'da veya öncesinde veri reyonunu sıfırlamak için **Veri Reyonunu Sıfırla** iletişim kutusunda, **Veri reyonunu sıfırla** onay kutusunu ve ardından **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="68527-139">To reset the data mart in Finance and Operations Financial reporting release 7.2.6.0 and earlier, in the **Reset Data Mart** dialog box, select the **Reset data mart** check box, and then select **OK**.</span></span> <span data-ttu-id="68527-140">Veri reyonunu yalnızca planlanmış bir kesinti sırasında sıfırlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="68527-140">You should reset the data mart only during scheduled downtime.</span></span>

<span data-ttu-id="68527-141">[![Veri reyonunu sıfırla onay kutusu](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span><span class="sxs-lookup"><span data-stu-id="68527-141">[![Reset data mart check box](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span></span>

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a><span data-ttu-id="68527-142">Microsoft Dynamics 365 for Finance and Operations Mali raporlama sürümü 7.3.0'da veri reyonunu sıfırlama ve bir neden seçme</span><span class="sxs-lookup"><span data-stu-id="68527-142">Reset the data mart and select a reason in Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.3.0</span></span>

<span data-ttu-id="68527-143">Veri reyonunun sıfırlanmasının gerekli olduğunu belirlerseniz, **Veri reyonunu sıfırla** onay kutusunu işaretleyin ve sonra **Neden** alanından bir neden seçin.</span><span class="sxs-lookup"><span data-stu-id="68527-143">If you determine that a data mart reset is required, select the **Reset data mart** check box, and then select a reason in the **Reason** field.</span></span> <span data-ttu-id="68527-144">Aşağıdaki seçenekler kullanılabilir durumdadır:</span><span class="sxs-lookup"><span data-stu-id="68527-144">The following options are available:</span></span>

- <span data-ttu-id="68527-145">**Eksik veya yanlış veri** – İstatistiklere bağlı olarak, verilerin eksik olabileceğini saptadınız.</span><span class="sxs-lookup"><span data-stu-id="68527-145">**Missing or incorrect data** – Based on the statistics, you've determined that data might be missing.</span></span> <span data-ttu-id="68527-146">Devam etmeden önce, temel nedeni belirlemek için Destek birimi ile birlikte çalışmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="68527-146">Before you continue, we recommend that you work with Support to determine the root cause.</span></span>
- <span data-ttu-id="68527-147">**Veritabanını sıfırlama**  – Finance and Operations veri tabanı geri yüklendi ancak Mali raporlama veri reyonu için veritabanı geri yüklenmedi.</span><span class="sxs-lookup"><span data-stu-id="68527-147">**Restore database** – The Finance and Operations database was restored, but the database for the Financial reporting data mart wasn't restored.</span></span>
- <span data-ttu-id="68527-148">**Diğer** – Veri reyonunu başka bir nedenle sıfırlıyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="68527-148">**Other** – You're resetting the data mart for another reason.</span></span> <span data-ttu-id="68527-149">Bir sorun olduğundan endişe duyuyorsanız, sorunu belirlemek için Desteğe başvurun.</span><span class="sxs-lookup"><span data-stu-id="68527-149">If you're concerned that there is an issue, contact Support to identify it.</span></span>

<span data-ttu-id="68527-150">[![Veri reyonunu sıfırla](./media/Integration.png)](./media/Integration.png)</span><span class="sxs-lookup"><span data-stu-id="68527-150">[![Reset data mart](./media/Integration.png)](./media/Integration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="68527-151">Tüm veri reyonu sıfırlama görevlerinin siz bir sıfırlama başlatmadan önce başlangıç yüklemesini tamamladığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="68527-151">Verify that all data mart reset tasks have completed an initial load before you begin a reset.</span></span> <span data-ttu-id="68527-152">Bunu, **Araçlar** &gt; **Tümleştirme durumu**'nu seçerek Son Çalıştırma Zamanı sütunundaki değere bakarak onaylayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="68527-152">You can confirm this by looking for a value in the Last Runtime column by selecting **Tools** &gt; **Integration status**.</span></span>

#### <a name="clear-users-and-companies"></a><span data-ttu-id="68527-153">Kullanıcıları ve şirketleri temizle</span><span class="sxs-lookup"><span data-stu-id="68527-153">Clear users and companies</span></span>

<span data-ttu-id="68527-154">Veritabanınızı geri yüklediyseniz ancak daha sonra kullanıcılar veya şirketlerde değişiklik yaptıysanız **Kullanıcıları ve şirketleri temizle** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="68527-154">Select the **Clear users and companies** check box if you restored your database, but you then made changes to users or companies.</span></span> <span data-ttu-id="68527-155">Bu onay kutusunu çok nadir olarak işaretlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="68527-155">You should rarely have to select this check box.</span></span>

<span data-ttu-id="68527-156">Sıfırlama işlemini başlatmaya hazır olduğunuzda, **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="68527-156">When you're ready to start the reset process, select **OK**.</span></span> <span data-ttu-id="68527-157">İşlemi başlatmak için hazır olduğunuzu onaylamanız istenir.</span><span class="sxs-lookup"><span data-stu-id="68527-157">You're prompted to confirm that you're ready to start the process.</span></span> <span data-ttu-id="68527-158">Mali raporlamanın sıfırlama ve daha sonra oluşan ilk veri tümleştirme sırasında kullanılamayacağını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="68527-158">Note that Financial reporting won't be available during the reset and the initial data integration that occurs afterward.</span></span>

<span data-ttu-id="68527-159">Tümleştirme durumunu gözden geçirmek isterseniz, tümleştirmenin en son çalıştırıldığı zamanı ve durumu görüntülemek için **Araçlar** &gt; **Tümleştirme durumu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="68527-159">If you want to review the status of the integration, select **Tools** &gt; **Integration status** to see the last time that the integration was run and the status.</span></span>

<span data-ttu-id="68527-160">[![Tümleştirmenin durumunu görüntüleme](./media/New-integration.PNG)](./media/New-integration.PNG)</span><span class="sxs-lookup"><span data-stu-id="68527-160">[![View the status of the integration](./media/New-integration.PNG)](./media/New-integration.PNG)</span></span>

> [!NOTE]
> <span data-ttu-id="68527-161">Sıfırlama işlemi tüm eşlemelerin durumu RanToCompletion olarak göründüğünde ve Tümleştirme Durumu penceresinin sol alt köşesinde "Tümleştirme tamamlandı" ifadesi olduğunda tamamlanır.</span><span class="sxs-lookup"><span data-stu-id="68527-161">The reset is finished when all mappings show the status of RanToCompletion and the Integration Status window says “Integration complete” in the bottom-left corner.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a><span data-ttu-id="68527-162">Finance and Operations Mali raporlama sürüm 7.0.10000.4 ve üstü için Mali raporlama veri reyonunu sıfırlama</span><span class="sxs-lookup"><span data-stu-id="68527-162">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>

<span data-ttu-id="68527-163">Finance and Operations veritabanınızı bir yedekten kurtarırsanız veya veritabanını bir ortamdan diğerine kopyalarsanız, Mali raporlama veri reyonunun Finance and Operations veritabanını doğru kullandığından emin olmak için bu bölümdeki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="68527-163">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this section to help guarantee that the Financial reporting data mart correctly uses the restored Finance and Operations database.</span></span>

> [!NOTE]
> <span data-ttu-id="68527-164">Bu işlemdeki adımların Microsoft Dynamics AX uygulaması 7.0.1 (Mayıs 2016) sürümü (uygulama derlemesi 7.0.1265.23014 ve Mali raporlama derlemesi 7.0.10000.4) ve daha yeni sürümler için desteklendiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="68527-164">The steps in this process are supported for Microsoft Dynamics AX application version 7.0.1 (May 2016) (application build 7.0.1265.23014 and Financial reporting build 7.0.10000.4) and later.</span></span> <span data-ttu-id="68527-165">Finance and Operations'ın önceki bir sürümüne sahipseniz, yardım için Destek ekibine başvurun.</span><span class="sxs-lookup"><span data-stu-id="68527-165">If you have an earlier version of Finance and Operations, contact Support for assistance.</span></span>

### <a name="export-report-definitions"></a><span data-ttu-id="68527-166">Rapor tanımlarını dışa aktarma</span><span class="sxs-lookup"><span data-stu-id="68527-166">Export report definitions</span></span>

<span data-ttu-id="68527-167">İlk olarak, rapor tasarımlarını Rapor tasarımcısından aktarmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="68527-167">First, follow these steps to export the report designs from Report designer.</span></span>

1. <span data-ttu-id="68527-168">Rapor tasarımcısında, **Şirket** &gt; **Yapı Taşı Grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="68527-168">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="68527-169">Dışa aktarılacak yapı taşı grubunu seçin ve **Dışa Aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="68527-169">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="68527-170">Finance and Operations için yalnızca bir yapı taşı grubu desteklenir, **Varsayılan**.</span><span class="sxs-lookup"><span data-stu-id="68527-170">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="68527-171">Dışa aktarılacak rapor tanımlarını seçin:</span><span class="sxs-lookup"><span data-stu-id="68527-171">Select the report definitions to export:</span></span>

    - <span data-ttu-id="68527-172">Tüm rapor tanımlarınızı ve ilişkili yapı taşlarını dışa aktarmak için **Tümünü Seç**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="68527-172">To export all your report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="68527-173">Belirli raporları, satırları, sütunları, ağaçları veya boyut kümelerini dışa aktarmak için, ilgili sekmeyi ve ardından dışa aktarılacak maddeleri seçin.</span><span class="sxs-lookup"><span data-stu-id="68527-173">To export specific reports, rows, columns, trees, or dimension sets, select the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="68527-174">Bir sekmede birden fazla öğeyi seçmek için Ctrl tuşunu basılı tutun. Dışa aktarılacak raporları seçtiğinizde ilişkili satırlar, sütunlar, ağaçlar ve boyut kümeleri seçilir.</span><span class="sxs-lookup"><span data-stu-id="68527-174">Press and hold the Ctrl key to select multiple items on a tab. When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4. <span data-ttu-id="68527-175">**Dışa Aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="68527-175">Select **Export**.</span></span>
5. <span data-ttu-id="68527-176">Bir dosya adı girin ve dışarı aktarılan rapor tanımlarını kaydetmek için istediğiniz güvenli bir konumu seçin.</span><span class="sxs-lookup"><span data-stu-id="68527-176">Enter a file name, and select a secure location where you want to save the exported report definitions.</span></span>
6. <span data-ttu-id="68527-177">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="68527-177">Select **Save**.</span></span>

<span data-ttu-id="68527-178">Dosyayı güvenli bir konuma kopyalayabilir veya yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="68527-178">You can copy or upload the file to a secure location.</span></span> <span data-ttu-id="68527-179">Bu şekilde, dosya daha sonra farklı bir ortama alınabilir.</span><span class="sxs-lookup"><span data-stu-id="68527-179">In this way, the file can be imported into a different environment later.</span></span> <span data-ttu-id="68527-180">Microsoft Azure depolama hesabını kullanma hakkındaki daha fazla bilgi için bkz. [AzCopy Komut Satırı Yardımcı Programı ile veri transferi](/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="68527-180">For information about how to use a Microsoft Azure storage account, see [Transfer data with the AzCopy Command-Line Utility](/azure/storage/storage-use-azcopy).</span></span>

> [!NOTE]
> <span data-ttu-id="68527-181">Microsoft, Finance and Operations sözleşmenizin bir parçası olarak bir depolama hesabı sağlamaz.</span><span class="sxs-lookup"><span data-stu-id="68527-181">Microsoft doesn't provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="68527-182">Bir depolama hesabı satın almanız veya ayrı bir Azure aboneliğine ait bir depolama hesabını kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="68527-182">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span>

> [!WARNING]
> <span data-ttu-id="68527-183">Azure Sanal Makineler'de (VM) D sürücüsünün davranışını dikkate alın.</span><span class="sxs-lookup"><span data-stu-id="68527-183">Be aware of the behavior of drive D on Azure virtual machines (VMs).</span></span> <span data-ttu-id="68527-184">Dışa aktarılan yapı taşı gruplarınızı kalıcı olarak D sürücüsünde depolamayın. Geçici sürücüler hakkında daha fazla bilgi için bkz. [Windows Azure Sanal Makinelerdeki geçici sürücüleri anlama](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="68527-184">Don't permanently store your exported building block groups on drive D. For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

### <a name="stop-services"></a><span data-ttu-id="68527-185">Hizmetleri durdurma</span><span class="sxs-lookup"><span data-stu-id="68527-185">Stop services</span></span>

<span data-ttu-id="68527-186">Aşağıdaki Microsoft Windows hizmetlerinin Finance and Operations veritabanına açık bağlantıları olacaktır.</span><span class="sxs-lookup"><span data-stu-id="68527-186">The following Microsoft Windows services will have open connections to the Finance and Operations database.</span></span> <span data-ttu-id="68527-187">Bu nedenle, ortamdaki tüm bilgisayarlara bağlanmak ve services.msc'yi kullanarak bu hizmetleri durdurmak için Microsoft Uzak Masaüstü'nü kullanmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="68527-187">Therefore, you must use Microsoft Remote Desktop to connect to all the computers in the environment and then use services.msc to stop these services.</span></span>

- <span data-ttu-id="68527-188">World wide web publishing service (tüm Uygulama Nesnesi Sunucuları [AOS] bilgisayarlarda)</span><span class="sxs-lookup"><span data-stu-id="68527-188">World wide web publishing service (on all Application Object Servers [AOS] computers)</span></span>
- <span data-ttu-id="68527-189">Microsoft Dynamics 365 for Finance and Operations Toplu İŞ Yönetimi Hizmeti (yalnızca özel olmayan AOS bilgisayarlarda)</span><span class="sxs-lookup"><span data-stu-id="68527-189">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="68527-190">Management Reporter 2012 İşlem Hizmeti (yalnızca İş zekası [BI] bilgisayarlarınızda)</span><span class="sxs-lookup"><span data-stu-id="68527-190">Management Reporter 2012 Process Service (on Business intelligence [BI] computers only)</span></span>

### <a name="reset"></a><span data-ttu-id="68527-191">Sıfırla</span><span class="sxs-lookup"><span data-stu-id="68527-191">Reset</span></span>

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="68527-192">En güncel MinorVersionDataUpgrade.zip paketini indirin.</span><span class="sxs-lookup"><span data-stu-id="68527-192">Download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="68527-193">En güncel MinorVersionDataUpgrade.zip paketini indirin.</span><span class="sxs-lookup"><span data-stu-id="68527-193">Download the latest MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="68527-194">Veri yükseltme paketinin doğru sürümünü bulma ve indirme ile ilgili yönergeler için bkz. [En son veri yükseltme dağıtılabilir paketini indirme](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span><span class="sxs-lookup"><span data-stu-id="68527-194">For instructions about how to find and download the correct version of the data upgrade package, see the[Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span></span> 

<span data-ttu-id="68527-195">MinorVersionDataUpgrade.zip paketini indirmek için bir yükseltme gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="68527-195">An upgrade isn't required in order to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="68527-196">Bu nedenle, bu konudaki "En son veri yükseltme dağıtılabilir paketini indirme" bölümündeki adımları izlemeniz yeterlidir.</span><span class="sxs-lookup"><span data-stu-id="68527-196">Therefore, you just have follow the steps in the "Download the latest data upgrade deployable package" section of that topic.</span></span> <span data-ttu-id="68527-197">Konu içindeki tüm diğer adımları atlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="68527-197">You can skip all the other steps in the topic.</span></span>

#### <a name="run-scripts-against-the-finance-and-operations-database"></a><span data-ttu-id="68527-198">Finance and Operations veritabanı için komut dosyalarını çalıştırma</span><span class="sxs-lookup"><span data-stu-id="68527-198">Run scripts against the Finance and Operations database</span></span>

<span data-ttu-id="68527-199">Aşağıdaki komut dosyalarını Finance and Operations veritabanı için çalıştırın (Mali raporlama veritabanı için değil):</span><span class="sxs-lookup"><span data-stu-id="68527-199">Run the following scripts against the Finance and Operations database (not against the Financial reporting database):</span></span>

- <span data-ttu-id="68527-200">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="68527-200">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
- <span data-ttu-id="68527-201">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="68527-201">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="68527-202">Bu komut dosyaları kullanıcıların, rollerin ve değişiklik izleme ayarlarının doğru olmasını sağlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="68527-202">These scripts help guarantee that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a><span data-ttu-id="68527-203">Veritabanı sıfırlamak için bir Windows PowerShell komutu çalıştırma</span><span class="sxs-lookup"><span data-stu-id="68527-203">Run a Windows PowerShell command to reset the database</span></span>

<span data-ttu-id="68527-204">AOS bilgisayarda Microsoft Windows PowerShell'i yönetici olarak başlatın ve Finance and Operations ve Mali raporlama tümleştirmesini sıfırlamak için aşağıdaki komutları çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="68527-204">On the AOS computer, start Microsoft Windows PowerShell as an administrator, and run the following commands to reset the integration between Finance and Operations and Financial reporting.</span></span>

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

<span data-ttu-id="68527-205">**Reset-DatamartIntegration** komutundaki parametrelerin açıklamasını aşağıda bulabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="68527-205">Here is an explanation of the parameters in the **Reset-DatamartIntegration** command:</span></span>

- <span data-ttu-id="68527-206">**-Reason** için geçerli değeler şunlardır: **SERVICING**, **BADDATA** ve **OTHER**.</span><span class="sxs-lookup"><span data-stu-id="68527-206">The valid values for **-Reason** are **SERVICING**, **BADDATA**, and **OTHER**.</span></span>
- <span data-ttu-id="68527-207">**-ReasonDetail** parametresi serbest metindir.</span><span class="sxs-lookup"><span data-stu-id="68527-207">The **-ReasonDetail** parameter is free text.</span></span>
- <span data-ttu-id="68527-208">Neden ve neden ayrıntısı telemetri/ortam izlemede kaydedilecektir.</span><span class="sxs-lookup"><span data-stu-id="68527-208">The reason and reason detail will be recorded in telemetry/environment monitoring.</span></span>

> [!NOTE]
> <span data-ttu-id="68527-209">Komutları çalıştırıldıktan sonra **Y** girerek veritabanını sıfırlamak istediğinizi onaylamanız istenir.</span><span class="sxs-lookup"><span data-stu-id="68527-209">After you run the commands, you will be asked to enter **Y** to confirm that you want to reset the database.</span></span>

#### <a name="restart-services"></a><span data-ttu-id="68527-210">Hizmetleri yeniden başlatma</span><span class="sxs-lookup"><span data-stu-id="68527-210">Restart services</span></span>

<span data-ttu-id="68527-211">Daha önce durdurduğunuz hizmetleri yeniden başlatmak için services.msc'yi kullanın:</span><span class="sxs-lookup"><span data-stu-id="68527-211">Use services.msc to restart the services that you stopped earlier:</span></span>

- <span data-ttu-id="68527-212">World wide web publishing service (tüm AOS bilgisayarlarda)</span><span class="sxs-lookup"><span data-stu-id="68527-212">World wide web publishing service (on all AOS computers)</span></span>
- <span data-ttu-id="68527-213">Microsoft Dynamics 365 for Finance and Operations Toplu İŞ Yönetimi Hizmeti (yalnızca özel olmayan AOS bilgisayarlarda)</span><span class="sxs-lookup"><span data-stu-id="68527-213">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="68527-214">Management Reporter 2012 İşlem Hizmeti (yalnızca BI bilgisayarlarda)</span><span class="sxs-lookup"><span data-stu-id="68527-214">Management Reporter 2012 Process Service (on BI computers only)</span></span>

#### <a name="import-report-definitions"></a><span data-ttu-id="68527-215">Rapor tanımlarını içe aktarma</span><span class="sxs-lookup"><span data-stu-id="68527-215">Import report definitions</span></span>

<span data-ttu-id="68527-216">Rapor tasarımcısındaki rapor tasarımlarınızı dışa aktarma sırasında oluşturulan dosyayı kullanarak içe aktarın.</span><span class="sxs-lookup"><span data-stu-id="68527-216">Import your report designs from Report designer by using the file that was created during the export.</span></span>

1. <span data-ttu-id="68527-217">Rapor tasarımcısında, **Şirket** &gt; **Yapı Taşı Grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="68527-217">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="68527-218">Dışa aktarılacak yapı taşı grubunu seçin ve **Dışa Aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="68527-218">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="68527-219">Finance and Operations için yalnızca bir yapı taşı grubu desteklenir, **Varsayılan**.</span><span class="sxs-lookup"><span data-stu-id="68527-219">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="68527-220">**Varsayılan** yapı bloğunu seçin ve **İçe Aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="68527-220">Select the **Default** building block, and then select **Import**.</span></span>
4. <span data-ttu-id="68527-221">Dışa aktarılan rapor tanımlarını içeren dosyayı ve ardından **Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="68527-221">Select the file that contains the exported report definitions, and then select **Open**.</span></span>
5. <span data-ttu-id="68527-222">**İçe Aktar** iletişim kutusunda, içe aktarılacak rapor tanımlarını seçin:</span><span class="sxs-lookup"><span data-stu-id="68527-222">In the **Import** dialog box, select the report definitions to import:</span></span>

    - <span data-ttu-id="68527-223">Tüm rapor tanımlarını ve ilişkili yapı taşlarını içe aktarmak için **Tümünü Seç**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="68527-223">To import all the report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="68527-224">Belirli raporları, satırları, sütunları, ağaçları veya boyut kümelerini içe aktarmak için, içe aktarılacak raporları, satırları, sütunları, ağaçları veya boyut kümelerini seçin.</span><span class="sxs-lookup"><span data-stu-id="68527-224">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6. <span data-ttu-id="68527-225">**İçe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="68527-225">Select **Import**.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a><span data-ttu-id="68527-226">Finance and Operations (şirket içi) için Mali raporlama veri reyonunu sıfırlama</span><span class="sxs-lookup"><span data-stu-id="68527-226">Reset the Financial reporting data mart for Finance and Operations (on-premises)</span></span>

1. <span data-ttu-id="68527-227">Tüm kullanıcılardan Rapor Tasarımcısı'ndan ve Finance and Operations'ın Mali raporlama alanından çıkmalarını isteyin.</span><span class="sxs-lookup"><span data-stu-id="68527-227">Instruct all users to exit Report designer and the Financial reporting area of Finance and Operations.</span></span>
2. <span data-ttu-id="68527-228">Mali raporlama veritabanında (MRDB) aşağıdaki komut dosyasını çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="68527-228">Run the following script against the Financial reporting database (MRDB).</span></span>

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ```

3. <span data-ttu-id="68527-229">Finance and Operations veritabanındaki (AXDB) FINANCIALREPORTS tablosundan tüm kayıtları kesin veya silin.</span><span class="sxs-lookup"><span data-stu-id="68527-229">Truncate or delete all records from the FINANCIALREPORTS table in the Finance and Operations database (AXDB).</span></span>
4. <span data-ttu-id="68527-230">Tablo Finance and Operations veritabanında varsa, FINANCIALREPORTVERSION tablosundan tüm kayıtları kesin veya silin.</span><span class="sxs-lookup"><span data-stu-id="68527-230">Truncate or delete all records from the FINANCIALREPORTVERSION table, if this table exists in the Finance and Operations database.</span></span> <span data-ttu-id="68527-231">Tablo Finance and Operations veritabanında yoksa bu adımı atlayın.</span><span class="sxs-lookup"><span data-stu-id="68527-231">If the table doesn't exist in the Finance and Operations database, skip this step.</span></span>
5. <span data-ttu-id="68527-232">Mali raporlama veritabanı için **ResetDatamart.sql** komut dosyasını çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="68527-232">Run the **ResetDatamart.sql** script against the Financial reporting database.</span></span> <span data-ttu-id="68527-233">Bu komut dosyası veri merkezi tümleştirmesini devre dışı bırakır, tüm veri merkezi verilerini siler ve veri reyonu tümleştirmesini yeniden etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="68527-233">This script disables the data mart integration, deletes all the data mart data, and then reenables the data mart integration.</span></span>

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
        FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
            EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
            INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
            WHERE o.[type] = 'V' 
            AND referenced_schema_name = @schemaname
            AND referenced_entity_name = @tablename))
            BEGIN
            PRINT 'deleting from ' + @tablename
            EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
            PRINT 'truncating from ' + @tablename
            EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    ------------------------------------------
    ------------------------------------------
    PRINT 'Reset the map tokens'
    UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Reset the tasks'
    UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
    PRINT 'Enable integration tasks, RunImmediately'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
    WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Enable the Maintenance Task'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
    (SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
    ------------------------------------------
    ------------------------------------------
    ```

6. <span data-ttu-id="68527-234">Sıfırlamadan sonra, Finansal raporlama veritabanı için aşağıdaki sorguyu çalıştırarak verileri yeniden yüklemeyi el ile doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="68527-234">After the reset, you can manually verify the data reload by running the following query against the Financial reporting database.</span></span>

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    <span data-ttu-id="68527-235">Tüm satırların **LastRunTime** değerine sahip olduğunu ve **StateType** değerinin **5** olarak ayarlandığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="68527-235">Confirm that all rows have a **LastRunTime** value, and that **StateType** is set to **5**.</span></span> <span data-ttu-id="68527-236">**5** olarak ayarlanan **StateType** değeri verilerin başarılı şekilde yüklendiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="68527-236">A **StateType** value of **5** indicates that the data was successfully reloaded.</span></span> <span data-ttu-id="68527-237"> **7** değeri hatalı bir durumu gösterir.</span><span class="sxs-lookup"><span data-stu-id="68527-237">A value of **7** indicates a faulted state.</span></span> <span data-ttu-id="68527-238">Bazı durumlarda, Kuruluş Hiyerarşisi eşlemesi ilk kez çalıştığında bu duruma sahip olur.</span><span class="sxs-lookup"><span data-stu-id="68527-238">Sometimes, the Organization Hierarchy map has this state the first time that it runs.</span></span> <span data-ttu-id="68527-239">Bununla birlikte, hatalı durum otomatik olarak giderilmelidir.</span><span class="sxs-lookup"><span data-stu-id="68527-239">However, the faulted state but should be automatically resolved.</span></span>

