---
title: Lifecycle Services'e bir yapılandırma yükleme
description: Aşağıdaki konuda, Sistem yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcının Elektronik Raporlama (ER) yapılandırması oluşturarak Microsoft Dynamics Lifecycle Services (LCS)'ye yükleyebilirsiniz.
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2ebafb52882fd33f4f0ef140c5d23d3288af97a2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684175"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="338c0-103">Lifecycle Services'e bir yapılandırma yükleme</span><span class="sxs-lookup"><span data-stu-id="338c0-103">Upload a configuration into Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="338c0-104">Aşağıdaki konuda, Sistem yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcının yeni bir [Elektronik Raporlama (ER) yapılandırması](../general-electronic-reporting.md#Configuration) oluşturarak Microsoft Dynamics Lifecycle Services (LCS)'de [proje düzeyi Varlık kitaplığı'na](../../lifecycle-services/asset-library.md) yüklemesi açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="338c0-104">This topic explains how a user in the System administrator or Electronic reporting developer role can create a new [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) and upload it into the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="338c0-105">Bu örnekte Litware, Inc. örnek şirketi için bir yapılandırma oluşturacak ve bunu LCS'ye yükleyeceksiniz. Bu adımlar, ER yapılandırmaları şirketler arasında paylaşımlı olduğundan herhangi bir şirkette tamamlanabilir.</span><span class="sxs-lookup"><span data-stu-id="338c0-105">In this example, you will create a configuration and upload it into LCS for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="338c0-106">Bu adımları tamamlamak için öncelikle [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](er-configuration-provider-mark-it-active-2016-11.md) adımlarını tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="338c0-106">To complete these steps, you must first complete the steps in [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="338c0-107">LCS'ye erişim de gereklidir.</span><span class="sxs-lookup"><span data-stu-id="338c0-107">Access to LCS is also required.</span></span>

1. <span data-ttu-id="338c0-108">Aşağıdaki rollerden birini kullanarak uygulamada oturum açın:</span><span class="sxs-lookup"><span data-stu-id="338c0-108">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="338c0-109">Elektronik raporlama geliştirici</span><span class="sxs-lookup"><span data-stu-id="338c0-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="338c0-110">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="338c0-110">System administrator</span></span>

2. <span data-ttu-id="338c0-111">**Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="338c0-111">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="338c0-112">**Litware, Inc.** öğesini seçin ve **Etkin** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="338c0-112">Select **Litware, Inc.**, and mark it as **Active**.</span></span>
4. <span data-ttu-id="338c0-113">**Yapılandırmalar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="338c0-113">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="338c0-114">Geçerli Dynamics 365 Finance kullanıcısının, ER konfigürasyonlarını içe aktarmak için kullanılacak [Varlık kitaplığı'nı](../../lifecycle-services/asset-library.md#asset-library-support) içeren LCS projesine üye olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="338c0-114">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the [Asset library](../../lifecycle-services/asset-library.md#asset-library-support) that is used to import ER configurations.</span></span>
>
> <span data-ttu-id="338c0-115">Bir LCS projesine Finance içinde kullanılan etki alanından farklı bir etki alanını temsil eden bir ER havuzundan erişemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="338c0-115">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="338c0-116">Denediğinizde, boş bir LCS proje listesi görüntülenir ve bu yapılandırmaları LCS'de proje düzeyi Varlık kitaplığı'ndan içe aktarmanız mümkün olmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="338c0-116">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="338c0-117">ER yapılandırmalarını içe aktarmak için kullanılan bir ER havuzundan proje düzeyi Varlık kitaplıkları'na erişmek için, geçerli Finance örneğinin sağlandığı kiracıya (etki alanı) ait bir kullanıcının kimlik bilgilerini kullanarak Finance uygulamasında oturum açın.</span><span class="sxs-lookup"><span data-stu-id="338c0-117">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="338c0-118">Yeni bir veri modeli yapılandırması oluşturun</span><span class="sxs-lookup"><span data-stu-id="338c0-118">Create a new data model configuration</span></span>

1. <span data-ttu-id="338c0-119">**Kuruluş yönetimi \> Elektronik raporlama \> Yapılandırmalar** seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="338c0-119">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="338c0-120">Açılır iletişim kutusunu açmak için **Yapılandırmalar** sayfasında **Yapılandırma oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="338c0-120">On the **Configurations** page, select **Create configuration** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="338c0-121">Bu örnekte elektronik belgeler için örnek bir veri modeli içeren bir yapılandırma oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="338c0-121">In this example, you will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="338c0-122">Bu veri modeli yapılandırması daha sonra LCS'ye yüklenecektir.</span><span class="sxs-lookup"><span data-stu-id="338c0-122">This data model configuration will be uploaded into LCS later.</span></span>

3. <span data-ttu-id="338c0-123">**Ad** alanına **Örnek model yapılandırması** değerini girin.</span><span class="sxs-lookup"><span data-stu-id="338c0-123">In the **Name** field, enter **Sample model configuration**.</span></span>
4. <span data-ttu-id="338c0-124">**Açıklama** alanına **Örnek model yapılandırması** değerini girin.</span><span class="sxs-lookup"><span data-stu-id="338c0-124">In the **Description** field, enter **Sample model configuration**.</span></span>
5. <span data-ttu-id="338c0-125">**Yapılandırma oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="338c0-125">Select **Create configuration**.</span></span>
6. <span data-ttu-id="338c0-126">**Model Tasarımcısı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="338c0-126">Select **Model designer**.</span></span>
7. <span data-ttu-id="338c0-127">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="338c0-127">Select **New**.</span></span>
8. <span data-ttu-id="338c0-128">**Ad** alanına **Giriş noktası** değerini girin.</span><span class="sxs-lookup"><span data-stu-id="338c0-128">In the **Name** field, enter **Entry point**.</span></span>
9. <span data-ttu-id="338c0-129">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="338c0-129">Select **Add**.</span></span>
10. <span data-ttu-id="338c0-130">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="338c0-130">Select **Save**.</span></span>
11. <span data-ttu-id="338c0-131">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="338c0-131">Close the page.</span></span>
12. <span data-ttu-id="338c0-132">**Durumu değiştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="338c0-132">Select **Change status**.</span></span>
13. <span data-ttu-id="338c0-133">**Tamamlandı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="338c0-133">Select **Complete**.</span></span>
14. <span data-ttu-id="338c0-134">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="338c0-134">Select **OK**.</span></span>
15. <span data-ttu-id="338c0-135">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="338c0-135">Close the page.</span></span>

## <a name="register-a-new-repository"></a><span data-ttu-id="338c0-136">Yeni bir depo kaydetme</span><span class="sxs-lookup"><span data-stu-id="338c0-136">Register a new repository</span></span>

1. <span data-ttu-id="338c0-137">**Organizasyon yönetimi \> Çalışma alanları \> Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="338c0-137">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="338c0-138">**Yapılandırma sağlayıcıları** bölümünde, **Liteware, Inc.** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="338c0-138">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="338c0-139">**Liteware, Inc.** kutucuğunda, **Depolar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="338c0-139">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="338c0-140">Artık Litware, Inc. yapılandırma sağlayıcısı için depoların listesini açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="338c0-140">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="338c0-141">Açılır iletişim kutusunu açmak için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="338c0-141">Select **Add** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="338c0-142">Şimdi yeni bir depo ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="338c0-142">You can now add a new repository.</span></span>

5. <span data-ttu-id="338c0-143">**Yapılandırma deposu giriş** alanında **LCS**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="338c0-143">In the **Configuration repository enter** field, select **LCS**.</span></span>
6. <span data-ttu-id="338c0-144">**Depo oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="338c0-144">Select **Create repository**.</span></span>
7. <span data-ttu-id="338c0-145">**Proje** alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="338c0-145">In the **Project** field, enter or select a value.</span></span>

    <span data-ttu-id="338c0-146">Bu örnekte, istenilen LCS projesini seçin.</span><span class="sxs-lookup"><span data-stu-id="338c0-146">For this example, select the desired LCS project.</span></span> <span data-ttu-id="338c0-147">Projeye [erişiminiz](#accessconditions) olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="338c0-147">You must have [access](#accessconditions) to the project.</span></span>

8. <span data-ttu-id="338c0-148">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="338c0-148">Select **OK**.</span></span>

    <span data-ttu-id="338c0-149">Yeni bir havuz girişini tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="338c0-149">Complete a new repository entry.</span></span>

9. <span data-ttu-id="338c0-150">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="338c0-150">In the list, mark the selected row.</span></span>

    <span data-ttu-id="338c0-151">Bu örnekte, **LCS** depo kaydını seçin.</span><span class="sxs-lookup"><span data-stu-id="338c0-151">For this example, select the **LCS** repository record.</span></span>

    <span data-ttu-id="338c0-152">Kayıtlı bir deponun geçerli sağlayıcı tarafından işaretlendiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="338c0-152">Note that a registered repository is marked by the current provider.</span></span> <span data-ttu-id="338c0-153">Başka bir deyişle, yalnızca bu sağlayıcıya ait olan yapılandırmalar bu depoda yer alabilir ve bu nedenle seçili LCS projesine yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="338c0-153">In other words, only configurations that are owned by that provider can be put in this repository and therefore uploaded into the selected LCS project.</span></span>

10. <span data-ttu-id="338c0-154">**Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="338c0-154">Select **Open**.</span></span>

    <span data-ttu-id="338c0-155">ER yapılandırmalarının listesini görüntülemek için havuzu açarsınız.</span><span class="sxs-lookup"><span data-stu-id="338c0-155">You open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="338c0-156">Seçili proje ER yapılandırmaları paylaşımı için henüz kullanılmamışsa, liste boş olur.</span><span class="sxs-lookup"><span data-stu-id="338c0-156">If the selected project hasn't yet been used for ER configurations sharing, the list will be empty.</span></span>

11. <span data-ttu-id="338c0-157">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="338c0-157">Close the page.</span></span>
12. <span data-ttu-id="338c0-158">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="338c0-158">Close the page.</span></span>

## <a name="upload-a-configuration-into-lcs"></a><span data-ttu-id="338c0-159">Bir yapılandırmayı LCS'ye yükleme</span><span class="sxs-lookup"><span data-stu-id="338c0-159">Upload a configuration into LCS</span></span>

1. <span data-ttu-id="338c0-160">**Kuruluş yönetimi \> Elektronik raporlama \> Yapılandırmalar** seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="338c0-160">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="338c0-161">**Yapılandırmalar** sayfasında, yapılandırmalar ağacında, **Örnek model yapılandırması** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="338c0-161">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="338c0-162">Tamamlanmış olan oluşturulmuş bir yapılandırmayı seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="338c0-162">You must select a created configuration that has been already completed.</span></span>

3. <span data-ttu-id="338c0-163">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="338c0-163">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="338c0-164">Bu örnek için seçili yapılandırmanın **Tamamlandı** durumda olan sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="338c0-164">For this example, select the version of the selected configuration that has a status of **Completed**.</span></span>

4. <span data-ttu-id="338c0-165">**Durumu değiştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="338c0-165">Select **Change status**.</span></span>
5. <span data-ttu-id="338c0-166">**Paylaş**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="338c0-166">Select **Share**.</span></span>

    <span data-ttu-id="338c0-167">Yapılandırma LCS 'de yayımlandığında yapılandırmanın durumu, **Tamamlandı**'dan **Paylaşıldı**'ya geçer.</span><span class="sxs-lookup"><span data-stu-id="338c0-167">The status of the configuration is changed from **Completed** to **Shared** when the configuration is published in LCS.</span></span>

6. <span data-ttu-id="338c0-168">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="338c0-168">Select **OK**.</span></span>
7. <span data-ttu-id="338c0-169">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="338c0-169">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="338c0-170">Bu örnek için yapılandırmanın **Paylaşıldı** durumda olan sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="338c0-170">For this example, select the configuration version that has a status of **Shared**.</span></span>

    <span data-ttu-id="338c0-171">Seçili sürümün durumunun **Tamamlandı**'dan **Paylaşıldı**'ya geçtiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="338c0-171">Note that the status of the selected version was changed from **Completed** to **Shared**.</span></span>

8. <span data-ttu-id="338c0-172">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="338c0-172">Close the page.</span></span>
9. <span data-ttu-id="338c0-173">**Depolar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="338c0-173">Select **Repositories**.</span></span>

    <span data-ttu-id="338c0-174">Artık Litware, Inc. yapılandırma sağlayıcısı için depoların listesini açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="338c0-174">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

10. <span data-ttu-id="338c0-175">**Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="338c0-175">Select **Open**.</span></span>

    <span data-ttu-id="338c0-176">Bu örnekte, **LCS** deposunu seçin ve açın.</span><span class="sxs-lookup"><span data-stu-id="338c0-176">For this example, select the **LCS** repository, and open it.</span></span>

    <span data-ttu-id="338c0-177">Seçili yapılandırmanın seçili LCS projesinin bir varlığı olarak gösterildiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="338c0-177">Notice that the selected configuration is shown as an asset of the selected LCS project.</span></span>

11. <span data-ttu-id="338c0-178"><https://lcs.dynamics.com> adresine giderek LCS'yi açın.</span><span class="sxs-lookup"><span data-stu-id="338c0-178">Open LCS by going to <https://lcs.dynamics.com>.</span></span>
12. <span data-ttu-id="338c0-179">Depo kaydı için daha önce kullanılan bir projeyi açın.</span><span class="sxs-lookup"><span data-stu-id="338c0-179">Open a project that was used earlier for repository registration.</span></span>
13. <span data-ttu-id="338c0-180">Projenin Varlık kitaplığı'nı açın.</span><span class="sxs-lookup"><span data-stu-id="338c0-180">Open the Asset library of the project.</span></span>
14. <span data-ttu-id="338c0-181">**GER yapılandırması** varlık türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="338c0-181">Select the **GER configuration** asset type.</span></span>

    <span data-ttu-id="338c0-182">Karşıya yüklediğiniz ER yapılandırması listelenmelidir.</span><span class="sxs-lookup"><span data-stu-id="338c0-182">The ER configuration that you uploaded should be listed.</span></span>

    <span data-ttu-id="338c0-183">Bu LCS projesine sağlayıcıların erişimi varsa, karşıya yüklenen LCS yapılandırmasının başka bir örneğe aktarılabildiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="338c0-183">Note that the uploaded LCS configuration can be imported into another instance if providers have access to this LCS project.</span></span>
