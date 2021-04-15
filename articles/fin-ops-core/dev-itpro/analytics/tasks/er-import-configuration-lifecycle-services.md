---
title: Lifecycle Services'tan bir yapılandırmayı içe aktarma
description: Bu konuda, Microsoft Dynamics Lifecycle Services (LCS) portalından Elektronik raporlama (ER) yapılandırmasının yeni sürümünün nasıl içeri aktarılacağı açıklanmaktadır.
author: NickSelin
ms.date: 09/14/2020
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
ms.openlocfilehash: 674d0dc02b4a53e455a15a06fdb7f24ca3036ba3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752376"
---
# <a name="import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="58683-103">Lifecycle Services'tan bir yapılandırmayı içe aktarma</span><span class="sxs-lookup"><span data-stu-id="58683-103">Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="58683-104">Aşağıdaki konuda, Sistem yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcının [Elektronik Raporlama (ER) yapılandırmasına](../general-electronic-reporting.md#Configuration) ait yeni bir sürümü Microsoft Dynamics Lifecycle Services (LCS)'de [proje düzeyi Varlık kitaplığı'ndan](../../lifecycle-services/asset-library.md) içe aktarması açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="58683-104">This topic explains how a user in the System administrator or Electronic reporting developer role can import a new version of an [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) from the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="58683-105">Bu örnekte bir ER yapılandırmasının istenilen sürümünü seçecek ve Litware, Inc. adlı örnek şirket için içe aktaracaksınız. Bu adımlar, ER yapılandırmaları şirketler arasında paylaşıldığından herhangi bir şirkette tamamlanabilir.</span><span class="sxs-lookup"><span data-stu-id="58683-105">In this example, you will select the desired version of the ER configuration and import it for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="58683-106">Bu adımları tamamlamak için, öncelikle [Bir yapılandırmayı Lifecycle Services'e içeri almak](er-upload-configuration-into-lifecycle-services.md) bölümündeki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="58683-106">To complete these steps, you must first complete the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="58683-107">LCS'ye erişim de gereklidir.</span><span class="sxs-lookup"><span data-stu-id="58683-107">Access to LCS is also required.</span></span>

1. <span data-ttu-id="58683-108">Aşağıdaki rollerden birini kullanarak uygulamada oturum açın:</span><span class="sxs-lookup"><span data-stu-id="58683-108">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="58683-109">Elektronik raporlama geliştirici</span><span class="sxs-lookup"><span data-stu-id="58683-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="58683-110">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="58683-110">System administrator</span></span>

2. <span data-ttu-id="58683-111">**Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="58683-111">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="58683-112">**Yapılandırmalar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="58683-112">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="58683-113">Geçerli Dynamics 365 Finance kullanıcısının, ER konfigürasyonlarını içe aktarmak için [erişmek](../../lifecycle-services/asset-library.md#asset-library-support) istediği Varlık kitaplığı'nı içeren LCS projesine üye olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="58683-113">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the Asset library that the user wants to [access](../../lifecycle-services/asset-library.md#asset-library-support) to import ER configurations.</span></span>
>
> <span data-ttu-id="58683-114">Bir LCS projesine Finance içinde kullanılan etki alanından farklı bir etki alanını temsil eden bir ER havuzundan erişemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="58683-114">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="58683-115">Denediğinizde, boş bir LCS proje listesi görüntülenir ve bu yapılandırmaları LCS'de proje düzeyi Varlık kitaplığı'ndan içe aktarmanız mümkün olmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="58683-115">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="58683-116">ER yapılandırmalarını içe aktarmak için kullanılan bir ER havuzundan proje düzeyi Varlık kitaplıkları'na erişmek için, geçerli Finance örneğinin sağlandığı kiracıya (etki alanı) ait bir kullanıcının kimlik bilgilerini kullanarak Finance uygulamasında oturum açın.</span><span class="sxs-lookup"><span data-stu-id="58683-116">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a><span data-ttu-id="58683-117">Veri modeli yapılandırmasının paylaşılan bir sürümünü silme</span><span class="sxs-lookup"><span data-stu-id="58683-117">Delete a shared version of a data model configuration</span></span>

1. <span data-ttu-id="58683-118">**Yapılandırmalar** sayfasında, yapılandırmalar ağacında, **Örnek model yapılandırması** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="58683-118">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="58683-119">Örnek veri modeli yapılandırmasının ilk sürümünü oluşturdunuz ve [Bir yapılandırmayı Lifecycle Services'e yüklemek](er-upload-configuration-into-lifecycle-services.md) yordamındaki adımlar tamamlandığında yayımladınız.</span><span class="sxs-lookup"><span data-stu-id="58683-119">You created the first version of a sample data model configuration and published it to LCS when you completed the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="58683-120">Bu yordamda, ER yapılandırmasının bu sürümünü sileceksiniz.</span><span class="sxs-lookup"><span data-stu-id="58683-120">In this procedure, you will delete that version of the ER configuration.</span></span> <span data-ttu-id="58683-121">Bu konuda daha sonra LCS'den bu sürümü içe aktaracaksınız.</span><span class="sxs-lookup"><span data-stu-id="58683-121">You will then import that version from LCS later in this topic.</span></span>

2. <span data-ttu-id="58683-122">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="58683-122">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="58683-123">BU örnek için yapılandırmanın **Paylaşılan** durumda olan sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="58683-123">For this example, select the version of the configuration that has a status of **Shared**.</span></span> <span data-ttu-id="58683-124">Bu durum, yapılandırmanın LCS için yayımlandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="58683-124">This status indicates that the configuration has been published to LCS.</span></span>

3. <span data-ttu-id="58683-125">**Durumu değiştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="58683-125">Select **Change status**.</span></span>
4. <span data-ttu-id="58683-126">**Durdur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="58683-126">Select **Discontinue**.</span></span>

    <span data-ttu-id="58683-127">Seçili sürümün durumunu **Paylaşılan**'dan **Durduruldu** olarak değiştirerek, silinebilir duruma getirin.</span><span class="sxs-lookup"><span data-stu-id="58683-127">By changing the status of the selected version from **Shared** to **Discontinued**, you make the version available for deletion.</span></span>

5. <span data-ttu-id="58683-128">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="58683-128">Select **OK**.</span></span>
6. <span data-ttu-id="58683-129">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="58683-129">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="58683-130">Bu örnek için yapılandırmanın **Durduruldu** durumda olan sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="58683-130">For this example, select the version of the configuration that has a status of **Discontinued**.</span></span>

7. <span data-ttu-id="58683-131">**Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="58683-131">Select **Delete**.</span></span>
8. <span data-ttu-id="58683-132">**Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="58683-132">Select **Yes**.</span></span>

    <span data-ttu-id="58683-133">Yalnızca seçili veri modeli yapılandırması için taslak sürümü 2'nin artık kullanılabilir olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="58683-133">Notice that the only draft version 2 of the selected data model configuration is now available.</span></span>

9. <span data-ttu-id="58683-134">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="58683-134">Close the page.</span></span>

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a><span data-ttu-id="58683-135">Veri modeli yapılandırmasının paylaşılan bir sürümünü LCS'den içeri alma</span><span class="sxs-lookup"><span data-stu-id="58683-135">Import a shared version of a data model configuration from LCS</span></span>

1. <span data-ttu-id="58683-136">**Organizasyon yönetimi \> Çalışma alanları \> Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="58683-136">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="58683-137">**Yapılandırma sağlayıcıları** bölümünde, **Liteware, Inc.** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="58683-137">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="58683-138">**Liteware, Inc.** kutucuğunda, **Depolar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58683-138">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="58683-139">Artık Litware, Inc. yapılandırma sağlayıcısı için depoların listesini açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58683-139">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="58683-140">**Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="58683-140">Select **Open**.</span></span>

    <span data-ttu-id="58683-141">Bu örnekte, **LCS** deposunu seçin ve açın.</span><span class="sxs-lookup"><span data-stu-id="58683-141">For this example, select the **LCS** repository, and open it.</span></span> <span data-ttu-id="58683-142">LCS projesine ve seçili ER deposu tarafından erişilen Varlık kitaplığı'na [erişiminizin](#accessconditions) olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="58683-142">You must have [access](#accessconditions) to the LCS project and to the Asset library that is accessed by the selected ER repository.</span></span>

5. <span data-ttu-id="58683-143">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="58683-143">In the list, mark the selected row.</span></span>

    <span data-ttu-id="58683-144">Bu örnek için sürüm listesinden **Örnek model yapılandırması**'nın ilk sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="58683-144">For this example, select the first version of **Sample model configuration** in the version list.</span></span>

6. <span data-ttu-id="58683-145">**İçe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="58683-145">Select **Import**.</span></span>
7. <span data-ttu-id="58683-146">Seçili sürümün LCS'den içe aktarıldığını onaylamak için **Evet** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="58683-146">Select **Yes** to confirm the import of the selected version from LCS.</span></span>

    <span data-ttu-id="58683-147">Bilgi iletisi, seçili sürümün başarıyla içe aktarıldığını onaylar.</span><span class="sxs-lookup"><span data-stu-id="58683-147">An informational message confirms that the selected version was successfully imported.</span></span>

8. <span data-ttu-id="58683-148">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="58683-148">Close the page.</span></span>
9. <span data-ttu-id="58683-149">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="58683-149">Close the page.</span></span>
10. <span data-ttu-id="58683-150">**Yapılandırmalar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="58683-150">Select **Configurations**.</span></span>
11. <span data-ttu-id="58683-151">Ağaçtan **Örnek model yapılandırması** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="58683-151">In the tree, select **Sample model configuration**.</span></span>
12. <span data-ttu-id="58683-152">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="58683-152">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="58683-153">BU örnek için yapılandırmanın **Paylaşılan** durumda olan sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="58683-153">For this example, select the version of the configuration that has a status of **Shared**.</span></span>

    <span data-ttu-id="58683-154">Yalnızca seçili veri modeli yapılandırması için paylaşılan sürümü 1'in de artık kullanılabilir olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="58683-154">Notice that shared version 1 of the selected data model configuration is also available now.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]