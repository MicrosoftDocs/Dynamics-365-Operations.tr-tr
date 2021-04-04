---
title: Başlangıç kurulumu sırasında sorunları giderme
description: Bu konuda, çift yazma tümleştirmesinin ilk kurulumu sırasında oluşabilecek sorunları gidermenize yardımcı olabilecek bilgiler sağlanmaktadır.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f6ff9a304de8a94b86e6866d6d2cb65fbfdfb02f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561190"
---
# <a name="troubleshoot-issues-during-initial-setup"></a><span data-ttu-id="82d2d-103">Başlangıç kurulumu sırasında sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="82d2d-103">Troubleshoot issues during initial setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="82d2d-104">Bu konu, Finance and Operations uygulamaları ve Dataverse arasında çift yazma tümleştirme hakkında sorun giderme bilgileri sağlar.</span><span class="sxs-lookup"><span data-stu-id="82d2d-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="82d2d-105">Bu konu, çift-yazma tümleştirmesinin ilk kurulumu sırasında oluşabilecek sorunları gidermenize yardımcı olabilecek bilgileri sağlar.</span><span class="sxs-lookup"><span data-stu-id="82d2d-105">Specifically, it provides information that can help you fix issues that might occur during the initial setup of dual-write integration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="82d2d-106">Bu konu adresiyle ilgili bazı sorunların sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="82d2d-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="82d2d-107">Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="82d2d-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a><span data-ttu-id="82d2d-108">Bir Finance and Operations uygulamayı Dataverse'e bağlayamazsınız</span><span class="sxs-lookup"><span data-stu-id="82d2d-108">You can't link a Finance and Operations app to Dataverse</span></span>

<span data-ttu-id="82d2d-109">**Çift yazmayı ayarlamak için gereken rol:** Finance and Operations uygulamalarında ve Dataverse'ta sistem yöneticisi.</span><span class="sxs-lookup"><span data-stu-id="82d2d-109">**Required role to set up dual-write:** System administrator in Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="82d2d-110">**Dataverse'e bağlantı kur** sayfa üzerindeki hatalar genellikle tamamlanmamış kurulum veya izin sorunlarından kaynaklanır.</span><span class="sxs-lookup"><span data-stu-id="82d2d-110">Errors on the **Setup link to Dataverse** page are usually caused by incomplete setup or permissions issues.</span></span> <span data-ttu-id="82d2d-111">Aşağıdaki çizimde gösterildiği gibi, tüm sistem durumu denetiminin **Dataverse'e bağlantı kur** sayfası üzerinden geçerken emin olun.</span><span class="sxs-lookup"><span data-stu-id="82d2d-111">Make sure that the whole health check passes on the **Setup link to Dataverse** page, as shown in the following illustration.</span></span> <span data-ttu-id="82d2d-112">Tüm sistem durumu denetimi başarılı olmadıkça çift-yazma bağlantısı yapamazsınız.</span><span class="sxs-lookup"><span data-stu-id="82d2d-112">You can't link dual-write unless the whole health check passes.</span></span>

![Başarılı sistem durumu denetimi](media/health_check.png)

<span data-ttu-id="82d2d-114">Finance and Operations Ve Dataverse ortamları bağlamak için Azure AD kiracı yöneticisi kimlik bilgileriniz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="82d2d-114">You must have Azure AD tenant admin credentials to link the Finance and Operations and Dataverse environments.</span></span> <span data-ttu-id="82d2d-115">Ortamları bağladıktan sonra, kullanıcılar kendi hesap kimlik bilgilerini kullanarak oturum açabilir ve mevcut bir tablo eşlemesini güncelleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="82d2d-115">After you link the environments, users can sign in by using their account credentials and update an existing table map.</span></span>

## <a name="error-when-you-open-the-link-to-dataverse-page"></a><span data-ttu-id="82d2d-116">Dataverse sayfa bağlantısını açtığınızda hata oluştu</span><span class="sxs-lookup"><span data-stu-id="82d2d-116">Error when you open the Link to Dataverse page</span></span>

<span data-ttu-id="82d2d-117">**Sorunun düzeltilmesi için gerekli olan kimlik bilgileri:** Azure AD Kiracı Yönetimi</span><span class="sxs-lookup"><span data-stu-id="82d2d-117">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="82d2d-118">Finance and Operations uygulamasında **Dataverse'e bağlantı** açtığınızda aşağıdaki hata iletisini alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="82d2d-118">You might receive the following error message when you open the **Link to Dataverse** page in a Finance and Operations app:</span></span>

<span data-ttu-id="82d2d-119">*Yanıt durum kodu başarıyı göstermiyor: 404 (Bulunamadı)*</span><span class="sxs-lookup"><span data-stu-id="82d2d-119">*Response status code does not indicate success: 404 (Not Found).*</span></span>

<span data-ttu-id="82d2d-120">Bu hata, onay adımı tamamlanmamışsa oluşur.</span><span class="sxs-lookup"><span data-stu-id="82d2d-120">This error occurs when the consent step hasn't been completed.</span></span> <span data-ttu-id="82d2d-121">Onay adımının tamamlanıp tamamlanmadığını doğrulamak için Azure AD kiracı yöneticisi hesabını kullanarak portal.Azure.com oturum açın ve Azure AD **kurumsal uygulamalar** listesinde **33976c19-1db5-4c02-810e-c243db79efde** kimliğine sahip üçüncü taraf uygulamanın görünüp görünmeyeceğini görün.</span><span class="sxs-lookup"><span data-stu-id="82d2d-121">To validate whether the consent step has been completed, sign in to portal.Azure.com by using the Azure AD tenant admin account, and see whether the third-party app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** appears in the Azure AD **Enterprise applications** list.</span></span> <span data-ttu-id="82d2d-122">İçermiyorsa, uygulama onayı sağlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="82d2d-122">If it doesn't, you must provide app consent.</span></span>

<span data-ttu-id="82d2d-123">Uygulama onayı sağlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="82d2d-123">To provide app consent, follow these steps.</span></span>

1. <span data-ttu-id="82d2d-124">Yönetici kimlik bilgilerinizi kullanarak aşağıdaki URL 'YI açın.</span><span class="sxs-lookup"><span data-stu-id="82d2d-124">Open the following URL by using your admin credentials.</span></span> <span data-ttu-id="82d2d-125">Sizden izin vermeniz istenecektir.</span><span class="sxs-lookup"><span data-stu-id="82d2d-125">You should be prompted for consent.</span></span>

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. <span data-ttu-id="82d2d-126">Kiracınıza **33976c19-1db5-4c02-810e-c243db79efde** kimliği olan uygulamayı yükleme izniniz olduğunu belirtmek için **kabul et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="82d2d-126">Select **Accept** to indicate that you're giving your consent to install the app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** in your tenant.</span></span>

    > [!TIP]
    > <span data-ttu-id="82d2d-127">Bu uygulama Dataverse ve Finance and Operations uygulamalarını bağlamak için gerekli.</span><span class="sxs-lookup"><span data-stu-id="82d2d-127">This app is required to link Dataverse and Finance and Operations apps.</span></span> <span data-ttu-id="82d2d-128">Bu adımla ilgili sorununuz varsa, tarayıcınızı Google Chrome ya da Microsoft Edge'de gizli modunda açın.</span><span class="sxs-lookup"><span data-stu-id="82d2d-128">If you have trouble with this step, open your browser in incognito mode (in Google Chrome) or InPrivate mode (in Microsoft Edge).</span></span>

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a><span data-ttu-id="82d2d-129">Şirket verileri ve çift-yazılır takımların bağlantı sırasında doğru şekilde ayarlandığını doğrulayın</span><span class="sxs-lookup"><span data-stu-id="82d2d-129">Verify that company data and dual-write teams are set up correctly during linking</span></span>

<span data-ttu-id="82d2d-130">Çift-yazmanın doğru çalışmasını sağlamak için, konfigürasyon sırasında seçtiğiniz şirketler Dataverse ortamda oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="82d2d-130">To ensure that dual-write works correctly, the companies that you select during configuration are created in the Dataverse environment.</span></span> <span data-ttu-id="82d2d-131">Varsayılan olarak, bu şirketler salt okunurdur **IsDualWriteEnable** özelliği **doğru** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="82d2d-131">By default, these companies are read-only, and the **IsDualWriteEnable** property is set to **True**.</span></span> <span data-ttu-id="82d2d-132">Ek olarak, varsayılan sorumlu departman sahibi ve ekibi oluşturulur ve şirket adını içerir.</span><span class="sxs-lookup"><span data-stu-id="82d2d-132">In addition, the default owning business unit owner and team are created and include the company name.</span></span> <span data-ttu-id="82d2d-133">Eşlemeleri etkinleştirmeden önce varsayılan takım sahibinin belirtildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="82d2d-133">Before you enable the maps, verify that the default team owner is specified.</span></span> <span data-ttu-id="82d2d-134">**Companies (CDM\_Company)** tablosunu bulmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="82d2d-134">To find the **Companies (CDM\_Company)** table, follow these steps.</span></span>

1. <span data-ttu-id="82d2d-135">Dynamics 365'deki model kullanımlı uygulamada, sağ üst köşedeki filtreyi seçin.</span><span class="sxs-lookup"><span data-stu-id="82d2d-135">In the model-driven app in Dynamics 365, select the filter in the upper-right corner.</span></span>
2. <span data-ttu-id="82d2d-136"> açılır listede, **Şirket**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="82d2d-136">In the drop-down list, select **Company**.</span></span>
3. <span data-ttu-id="82d2d-137">Sonuçları görmek için **Çalıştır** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="82d2d-137">Select **Run** to see the results.</span></span>
4. <span data-ttu-id="82d2d-138">Çift-yazmayı konfigüre ettiğinizde bağlanan şirketi seçin.</span><span class="sxs-lookup"><span data-stu-id="82d2d-138">Select the company that was linked when you configured dual-write.</span></span>
5. <span data-ttu-id="82d2d-139">**Varsayılan sahibi olan takım** sütununun bir değere sahip olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="82d2d-139">Verify that the **Default owning team** column has a value.</span></span> <span data-ttu-id="82d2d-140">Aşağıdaki çizimde, **Varsayılan sahibi olan takım** sütunu **USMF Çift Yazma** olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="82d2d-140">In the following illustration, the **Default owning team** column is set to **USMF Dual Write**.</span></span>

    ![Varsayılan sahip olan takım doğrulanıyor](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a><span data-ttu-id="82d2d-142">Çift-yazma için bağlanabilen yasal tablo veya şirket sayısı sınırını bulma</span><span class="sxs-lookup"><span data-stu-id="82d2d-142">Find the limit on the number of legal tables or companies that can be linked for dual-write</span></span>

<span data-ttu-id="82d2d-143">Haritaları etkinleştirmeyi denediğinizde aşağıdaki hata iletisini alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="82d2d-143">You might receive the following error message when you try to enable maps:</span></span>

<span data-ttu-id="82d2d-144">*İkili yazma hatası - Eklenti kaydı başarısız oldu: \[(Proje DWM için bölüm eşlemesi alınamıyor - 1ae35e60-4bc2-4905-88ea-69efd3b29260-.7f12cb89-1550-42e2-858e-4761fc1443ea. Hata, DWM için izin verilen maksimum bölüm sayısını aşıyor - 1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], bir veya daha fazla hata oluştu.*</span><span class="sxs-lookup"><span data-stu-id="82d2d-144">*Dual write failure - Plugin registration failed: \[(Unable to get partition map for project DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Error Exceeds the maximum partitions allowed for mapping DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], One or more errors occurred.*</span></span>

<span data-ttu-id="82d2d-145">Ortam bağlamayla ilgili geçerli sınır yaklaşık 40 yasal tablodur.</span><span class="sxs-lookup"><span data-stu-id="82d2d-145">The current limit when you link the environments is approximately 40 legal tables.</span></span> <span data-ttu-id="82d2d-146">Bu hata, eşlemeleri etkinleştirmeye çalışırsanız ve ortamlar arasında 40'tan fazla yasal tablo bağlanmışsa oluşur.</span><span class="sxs-lookup"><span data-stu-id="82d2d-146">This error occurs if you try to enable maps, and more than 40 legal tables are linked between the environments.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]