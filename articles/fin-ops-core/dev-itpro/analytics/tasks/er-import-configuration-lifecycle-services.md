---
title: Lifecycle Services'tan bir yapılandırmayı içe aktarma
description: Bu konuda, Microsoft Dynamics Lifecycle Services (LCS) portalından Elektronik raporlama (ER) yapılandırmasının yeni sürümünün nasıl içeri aktarılacağı açıklanmaktadır.
author: NickSelin
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b58ecb8a7d6f52631dbca7642a4acbcf6ff895a3
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270849"
---
# <a name="import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="b75d4-103">Lifecycle Services'tan bir yapılandırmayı içe aktarma</span><span class="sxs-lookup"><span data-stu-id="b75d4-103">Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b75d4-104">Aşağıdaki konuda, Sistem yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcının [Elektronik Raporlama (ER) yapılandırmasına](../general-electronic-reporting.md#Configuration) ait yeni bir sürümü Microsoft Dynamics Lifecycle Services (LCS)'de [proje düzeyi Varlık kitaplığı'ndan](../../lifecycle-services/asset-library.md) içe aktarması açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="b75d4-104">This topic explains how a user in the System administrator or Electronic reporting developer role can import a new version of an [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) from the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b75d4-105">LCS'nin, ER yapılandırmaları için saklama deposu olarak kullanılma özelliği [kullanım dışı bırakılıyor](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span><span class="sxs-lookup"><span data-stu-id="b75d4-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="b75d4-106">Daha fazla bilgi için bkz. [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) depolamasının kullanım dışı bırakılması](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span><span class="sxs-lookup"><span data-stu-id="b75d4-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

<span data-ttu-id="b75d4-107">Bu örnekte bir ER yapılandırmasının istenilen sürümünü seçecek ve Litware, Inc. adlı örnek şirket için içe aktaracaksınız. Bu adımlar, ER yapılandırmaları şirketler arasında paylaşıldığından herhangi bir şirkette tamamlanabilir.</span><span class="sxs-lookup"><span data-stu-id="b75d4-107">In this example, you will select the desired version of the ER configuration and import it for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="b75d4-108">Bu adımları tamamlamak için, öncelikle [Bir yapılandırmayı Lifecycle Services'e içeri almak](er-upload-configuration-into-lifecycle-services.md) bölümündeki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b75d4-108">To complete these steps, you must first complete the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="b75d4-109">LCS'ye erişim de gereklidir.</span><span class="sxs-lookup"><span data-stu-id="b75d4-109">Access to LCS is also required.</span></span>

1. <span data-ttu-id="b75d4-110">Aşağıdaki rollerden birini kullanarak uygulamada oturum açın:</span><span class="sxs-lookup"><span data-stu-id="b75d4-110">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="b75d4-111">Elektronik raporlama geliştirici</span><span class="sxs-lookup"><span data-stu-id="b75d4-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="b75d4-112">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="b75d4-112">System administrator</span></span>

2. <span data-ttu-id="b75d4-113">**Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="b75d4-113">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="b75d4-114">**Yapılandırmalar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b75d4-114">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="b75d4-115">Geçerli Dynamics 365 Finance kullanıcısının, ER konfigürasyonlarını içe aktarmak için [erişmek](../../lifecycle-services/asset-library.md#asset-library-support) istediği Varlık kitaplığı'nı içeren LCS projesine üye olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="b75d4-115">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the Asset library that the user wants to [access](../../lifecycle-services/asset-library.md#asset-library-support) to import ER configurations.</span></span>
>
> <span data-ttu-id="b75d4-116">Bir LCS projesine Finance içinde kullanılan etki alanından farklı bir etki alanını temsil eden bir ER havuzundan erişemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="b75d4-116">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="b75d4-117">Denediğinizde, boş bir LCS proje listesi görüntülenir ve bu yapılandırmaları LCS'de proje düzeyi Varlık kitaplığı'ndan içe aktarmanız mümkün olmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="b75d4-117">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="b75d4-118">ER yapılandırmalarını içe aktarmak için kullanılan bir ER havuzundan proje düzeyi Varlık kitaplıkları'na erişmek için, geçerli Finance örneğinin sağlandığı kiracıya (etki alanı) ait bir kullanıcının kimlik bilgilerini kullanarak Finance uygulamasında oturum açın.</span><span class="sxs-lookup"><span data-stu-id="b75d4-118">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a><span data-ttu-id="b75d4-119">Veri modeli yapılandırmasının paylaşılan bir sürümünü silme</span><span class="sxs-lookup"><span data-stu-id="b75d4-119">Delete a shared version of a data model configuration</span></span>

1. <span data-ttu-id="b75d4-120">**Yapılandırmalar** sayfasında, yapılandırmalar ağacında, **Örnek model yapılandırması** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="b75d4-120">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="b75d4-121">Örnek veri modeli yapılandırmasının ilk sürümünü oluşturdunuz ve [Bir yapılandırmayı Lifecycle Services'e yüklemek](er-upload-configuration-into-lifecycle-services.md) yordamındaki adımlar tamamlandığında yayımladınız.</span><span class="sxs-lookup"><span data-stu-id="b75d4-121">You created the first version of a sample data model configuration and published it to LCS when you completed the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="b75d4-122">Bu yordamda, ER yapılandırmasının bu sürümünü sileceksiniz.</span><span class="sxs-lookup"><span data-stu-id="b75d4-122">In this procedure, you will delete that version of the ER configuration.</span></span> <span data-ttu-id="b75d4-123">Bu konuda daha sonra LCS'den bu sürümü içe aktaracaksınız.</span><span class="sxs-lookup"><span data-stu-id="b75d4-123">You will then import that version from LCS later in this topic.</span></span>

2. <span data-ttu-id="b75d4-124">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="b75d4-124">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="b75d4-125">BU örnek için yapılandırmanın **Paylaşılan** durumda olan sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="b75d4-125">For this example, select the version of the configuration that has a status of **Shared**.</span></span> <span data-ttu-id="b75d4-126">Bu durum, yapılandırmanın LCS için yayımlandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b75d4-126">This status indicates that the configuration has been published to LCS.</span></span>

3. <span data-ttu-id="b75d4-127">**Durumu değiştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b75d4-127">Select **Change status**.</span></span>
4. <span data-ttu-id="b75d4-128">**Durdur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="b75d4-128">Select **Discontinue**.</span></span>

    <span data-ttu-id="b75d4-129">Seçili sürümün durumunu **Paylaşılan**'dan **Durduruldu** olarak değiştirerek, silinebilir duruma getirin.</span><span class="sxs-lookup"><span data-stu-id="b75d4-129">By changing the status of the selected version from **Shared** to **Discontinued**, you make the version available for deletion.</span></span>

5. <span data-ttu-id="b75d4-130">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b75d4-130">Select **OK**.</span></span>
6. <span data-ttu-id="b75d4-131">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="b75d4-131">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="b75d4-132">Bu örnek için yapılandırmanın **Durduruldu** durumda olan sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="b75d4-132">For this example, select the version of the configuration that has a status of **Discontinued**.</span></span>

7. <span data-ttu-id="b75d4-133">**Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b75d4-133">Select **Delete**.</span></span>
8. <span data-ttu-id="b75d4-134">**Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b75d4-134">Select **Yes**.</span></span>

    <span data-ttu-id="b75d4-135">Yalnızca seçili veri modeli yapılandırması için taslak sürümü 2'nin artık kullanılabilir olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="b75d4-135">Notice that the only draft version 2 of the selected data model configuration is now available.</span></span>

9. <span data-ttu-id="b75d4-136">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="b75d4-136">Close the page.</span></span>

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a><span data-ttu-id="b75d4-137">Veri modeli yapılandırmasının paylaşılan bir sürümünü LCS'den içeri alma</span><span class="sxs-lookup"><span data-stu-id="b75d4-137">Import a shared version of a data model configuration from LCS</span></span>

1. <span data-ttu-id="b75d4-138">**Organizasyon yönetimi \> Çalışma alanları \> Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="b75d4-138">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="b75d4-139">**Yapılandırma sağlayıcıları** bölümünde, **Liteware, Inc.** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="b75d4-139">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="b75d4-140">**Liteware, Inc.** kutucuğunda, **Depolar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b75d4-140">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="b75d4-141">Artık Litware, Inc. yapılandırma sağlayıcısı için depoların listesini açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b75d4-141">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="b75d4-142">**Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b75d4-142">Select **Open**.</span></span>

    <span data-ttu-id="b75d4-143">Bu örnekte, **LCS** deposunu seçin ve açın.</span><span class="sxs-lookup"><span data-stu-id="b75d4-143">For this example, select the **LCS** repository, and open it.</span></span> <span data-ttu-id="b75d4-144">LCS projesine ve seçili ER deposu tarafından erişilen Varlık kitaplığı'na [erişiminizin](#accessconditions) olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="b75d4-144">You must have [access](#accessconditions) to the LCS project and to the Asset library that is accessed by the selected ER repository.</span></span>

5. <span data-ttu-id="b75d4-145">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="b75d4-145">In the list, mark the selected row.</span></span>

    <span data-ttu-id="b75d4-146">Bu örnek için sürüm listesinden **Örnek model yapılandırması**'nın ilk sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="b75d4-146">For this example, select the first version of **Sample model configuration** in the version list.</span></span>

6. <span data-ttu-id="b75d4-147">**İçe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b75d4-147">Select **Import**.</span></span>
7. <span data-ttu-id="b75d4-148">Seçili sürümün LCS'den içe aktarıldığını onaylamak için **Evet** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="b75d4-148">Select **Yes** to confirm the import of the selected version from LCS.</span></span>

    <span data-ttu-id="b75d4-149">Bilgi iletisi, seçili sürümün başarıyla içe aktarıldığını onaylar.</span><span class="sxs-lookup"><span data-stu-id="b75d4-149">An informational message confirms that the selected version was successfully imported.</span></span>

8. <span data-ttu-id="b75d4-150">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="b75d4-150">Close the page.</span></span>
9. <span data-ttu-id="b75d4-151">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="b75d4-151">Close the page.</span></span>
10. <span data-ttu-id="b75d4-152">**Yapılandırmalar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b75d4-152">Select **Configurations**.</span></span>
11. <span data-ttu-id="b75d4-153">Ağaçtan **Örnek model yapılandırması** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="b75d4-153">In the tree, select **Sample model configuration**.</span></span>
12. <span data-ttu-id="b75d4-154">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="b75d4-154">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="b75d4-155">BU örnek için yapılandırmanın **Paylaşılan** durumda olan sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="b75d4-155">For this example, select the version of the configuration that has a status of **Shared**.</span></span>

    <span data-ttu-id="b75d4-156">Yalnızca seçili veri modeli yapılandırması için paylaşılan sürümü 1'in de artık kullanılabilir olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="b75d4-156">Notice that shared version 1 of the selected data model configuration is also available now.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
