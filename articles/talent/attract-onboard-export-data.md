---
title: Attract ve Onboard üzerinden veri dışarı aktarmak
description: Dynamics 365 Talent üzerinden veri dışarı aktarmak - Attract ve Onboard.
author: andreabichsel
manager: AnnBe
ms.date: 01/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: eb97a16c15476c2f34ec581a32a677fa6fee8739
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462773"
---
# <a name="export-data-from-attract-and-onboard"></a><span data-ttu-id="fa817-103">Attract ve Onboard üzerinden veri dışarı aktarmak</span><span class="sxs-lookup"><span data-stu-id="fa817-103">Export data from Attract and Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fa817-104">[Dynamics 365 Talent: Attract ve Dynamics 365 Talent: Onboard Uygulamaları devre dışı kalıyor](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps), 1 Şubat 2022 tarihinde Dynamics 365 Talent: Attract ve Dynamics 365 Talent: Onboard ürünlerini devre dışı bırakıyoruz.</span><span class="sxs-lookup"><span data-stu-id="fa817-104">As announced in [Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps), we're retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard on February 1, 2022.</span></span> <span data-ttu-id="fa817-105">Başka bir ürüne geçişinize yardımcı olmak için, her iki uygulama da veri dışa aktarma becerisi sağlar.</span><span class="sxs-lookup"><span data-stu-id="fa817-105">To help with your migration to another product, both apps now provide data export capabilities.</span></span>

## <a name="export-data-from-attract"></a><span data-ttu-id="fa817-106">Verileri Attract üzerinden dışa aktar</span><span class="sxs-lookup"><span data-stu-id="fa817-106">Export data from Attract</span></span>

<span data-ttu-id="fa817-107">Verilerinizi, ortamınıza erişimi sınırlamadan verebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fa817-107">You can export your data without restricting access to your environment.</span></span> <span data-ttu-id="fa817-108">Bunu test amacıyla veya veri yapımızı anlamak için yapmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fa817-108">You might want to do this for testing purposes or to understand our data structure.</span></span> <span data-ttu-id="fa817-109">Taşımaya hazır olduğunuzda, bu yordamdan sonraki yönergeleri kullanarak atmaya çalışma ortamınıza erişimi kısıtlayın.</span><span class="sxs-lookup"><span data-stu-id="fa817-109">When you're ready to migrate, restrict access to your Attract environment using the instructions after this procedure.</span></span> <span data-ttu-id="fa817-110">Verilerinizi yeniden dışa aktardığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="fa817-110">Be sure to export your data again.</span></span> 

1. <span data-ttu-id="fa817-111">[https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport) gidin.</span><span class="sxs-lookup"><span data-stu-id="fa817-111">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="fa817-112">**Veri dışa aktarma** altında, **Veri dışa aktarma talebi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="fa817-112">Under **Data export**, select **Request a data export**.</span></span>

   ![[<span data-ttu-id="fa817-113">Attract üzerinden bir veri dışa aktarma talep edin</span><span class="sxs-lookup"><span data-stu-id="fa817-113">Request a data export from Attract</span></span>](./media/attract-onboard-export-data-attract-request.png)](./media/attract-onboard-export-data-attract-request.png)

3. <span data-ttu-id="fa817-114">**İsteğiniz işleniyor** mesaj kutusu görüntülendiğinde, **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="fa817-114">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="fa817-115">Veri dışa aktarma 20 dakika kadar sürebilir, dışa aktarmanızın ebatlarına bağlı olarak.</span><span class="sxs-lookup"><span data-stu-id="fa817-115">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="fa817-116">Dışa aktarma işlemi tamamlandığında, yanındaki **İndir** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="fa817-116">When your export completes, select the **Download** button next to it.</span></span> 

   >[!NOTE]
   ><span data-ttu-id="fa817-117">Tüm veri dışa aktarma işlemleri yedi gün süreyle kullanılabilir, bu noktada **İndir** bağlantısı geçerliliğini yitirir.</span><span class="sxs-lookup"><span data-stu-id="fa817-117">All data exports are available for seven days, at which point the **Download** link expires.</span></span></br>
   
<span data-ttu-id="fa817-118">Karşıdan yükleme, aşağıdaki klasörler de dahil olmak üzere, Attract verinizi içeren bir .zip dosyası içerir:</span><span class="sxs-lookup"><span data-stu-id="fa817-118">The download contains a .zip file with your Attract data, including the following folders:</span></span>

| <span data-ttu-id="fa817-119">Klasör adı</span><span class="sxs-lookup"><span data-stu-id="fa817-119">Folder name</span></span> | <span data-ttu-id="fa817-120">Tanım</span><span class="sxs-lookup"><span data-stu-id="fa817-120">Description</span></span> |
| --- | --- |
| <span data-ttu-id="fa817-121">Yönetici ayarları</span><span class="sxs-lookup"><span data-stu-id="fa817-121">Admin settings</span></span> | <span data-ttu-id="fa817-122">Attract yönetim merkezi yapılandırmaları.</span><span class="sxs-lookup"><span data-stu-id="fa817-122">Attract admin center configurations.</span></span> |
| <span data-ttu-id="fa817-123">Adaylar</span><span class="sxs-lookup"><span data-stu-id="fa817-123">Candidates</span></span> | <span data-ttu-id="fa817-124">İşlere veya yetenek havuzlarına eklenen tüm adaylar.</span><span class="sxs-lookup"><span data-stu-id="fa817-124">All candidates that were added to jobs or talent pools.</span></span> |
| <span data-ttu-id="fa817-125">E-posta şablonları</span><span class="sxs-lookup"><span data-stu-id="fa817-125">Email templates</span></span> | <span data-ttu-id="fa817-126">Ortam için yapılandırılan tüm e-posta şablonları.</span><span class="sxs-lookup"><span data-stu-id="fa817-126">All email templates that were configured for the environment.</span></span> |
| <span data-ttu-id="fa817-127">İş teklifi paketi şablonları</span><span class="sxs-lookup"><span data-stu-id="fa817-127">Job offer package templates</span></span> | <span data-ttu-id="fa817-128">Tüm iş, oluşturulan paket şablonları ve bunların ilişkili yapılandırmalarını sunar.</span><span class="sxs-lookup"><span data-stu-id="fa817-128">All job offer package templates that were created, plus their associated configurations.</span></span> |
| <span data-ttu-id="fa817-129">İş teklifi kural kümeleri</span><span class="sxs-lookup"><span data-stu-id="fa817-129">Job offer rule sets</span></span> |  <span data-ttu-id="fa817-130">Tüm kural, teklif yönetimi için karşıya yüklenen dosyaları ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fa817-130">All rule set files that were uploaded for offer management.</span></span> |
| <span data-ttu-id="fa817-131">İş teklifi şablonları</span><span class="sxs-lookup"><span data-stu-id="fa817-131">Job offer templates</span></span> | <span data-ttu-id="fa817-132">Tüm iş, ortam için oluşturulmuş belge şablonlarını sunar.</span><span class="sxs-lookup"><span data-stu-id="fa817-132">All job offer document templates created for the environment.</span></span> |
| <span data-ttu-id="fa817-133">Açık pozisyonlar</span><span class="sxs-lookup"><span data-stu-id="fa817-133">Job openings</span></span> | <span data-ttu-id="fa817-134">Oluşturulan işler.</span><span class="sxs-lookup"><span data-stu-id="fa817-134">All created jobs.</span></span> <span data-ttu-id="fa817-135">Silinen işler aktarılmaz.</span><span class="sxs-lookup"><span data-stu-id="fa817-135">Deleted jobs aren't exported.</span></span> <span data-ttu-id="fa817-136">Alt klasörler, aday uygulama ekleri için alt klasörlerle, uygun durumlarda paketleri sunan aday uygulamaları içerir.</span><span class="sxs-lookup"><span data-stu-id="fa817-136">The sub-folders contain candidate applications, with sub-folders for candidate application attachments and offer packages, where applicable.</span></span> |
| <span data-ttu-id="fa817-137">Açık pozisyon şablonları</span><span class="sxs-lookup"><span data-stu-id="fa817-137">Job opening templates</span></span> | <span data-ttu-id="fa817-138">Ortamda yapılandırılan İş işlemi şablonları.</span><span class="sxs-lookup"><span data-stu-id="fa817-138">Job process templates that were configured in the environment.</span></span> |
| <span data-ttu-id="fa817-139">Yetenek havuzları</span><span class="sxs-lookup"><span data-stu-id="fa817-139">Talent pools</span></span> | <span data-ttu-id="fa817-140">Tüm oluşturulan havuzlar, katılımcı listeleri ve yetenek havuzları için aday listeleri.</span><span class="sxs-lookup"><span data-stu-id="fa817-140">All created talent pools, their contributors lists, and the candidates lists for the talent pools.</span></span> |
| <span data-ttu-id="fa817-141">Çalışanlar</span><span class="sxs-lookup"><span data-stu-id="fa817-141">Workers</span></span> | <span data-ttu-id="fa817-142">Ortamda bulunan tüm çalışanların ve bunların rollerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="fa817-142">List of all the workers who are present in the environment, plus their roles.</span></span> |
| <span data-ttu-id="fa817-143">(kök klasör)</span><span class="sxs-lookup"><span data-stu-id="fa817-143">(root folder)</span></span> | <span data-ttu-id="fa817-144">Veri yapısı alanlarını açıklayan bir JSON şema dosyası.</span><span class="sxs-lookup"><span data-stu-id="fa817-144">A JSON schema file that describes the data structure fields.</span></span> |

### <a name="restrict-access-to-attract"></a><span data-ttu-id="fa817-145">Attract'e erişimi kısıtla</span><span class="sxs-lookup"><span data-stu-id="fa817-145">Restrict access to Attract</span></span>

<span data-ttu-id="fa817-146">Geçirmeye hazır olduğunuzda, yönetici olmayanların Attract ortamınıza erişmesini ve verilerinizi dışa aktarmayı kısıtlayın.</span><span class="sxs-lookup"><span data-stu-id="fa817-146">When you're ready to migrate, restrict non-admins from accessing your Attract environment and export your data.</span></span>

>[!IMPORTANT]
><span data-ttu-id="fa817-147">Attract ortamınıza erişimi kısıtlamak kalıcıdır ve geri alınamaz.</span><span class="sxs-lookup"><span data-stu-id="fa817-147">Restricting access to your Attract environment is permanent and can't be undone.</span></span> <span data-ttu-id="fa817-148">Yönetici olmayan kullanıcıların ortamınıza erişmeye devam etmesini istiyorsanız, bu adımı atlayın.</span><span class="sxs-lookup"><span data-stu-id="fa817-148">If you want non-admin users to continue accessing your environment, skip this step.</span></span>

1. <span data-ttu-id="fa817-149">[https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport) gidin.</span><span class="sxs-lookup"><span data-stu-id="fa817-149">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="fa817-150">Yönetici olmayanların Attract erişim ortamınıza erişimini kısıtlamak için **Bu uygulama yerleşimi kısıtla** altında, **şimdi erişimi kısıtla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="fa817-150">To restrict non-admins from accessing your Attract environment, under **Restrict access to this app**, select **Restrict access now**.</span></span> <span data-ttu-id="fa817-151">Erişimin sınırlandırılması, ayrıca deftere nakledilen etkin işlerin deftere nakledilmesini geri alınmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="fa817-151">Restricting access also unposts any active jobs that have been posted.</span></span>

   ![[<span data-ttu-id="fa817-152">Attract'e yönetici olmayanların erişimini kısıtla</span><span class="sxs-lookup"><span data-stu-id="fa817-152">Restrict non-admin access to Attract</span></span>](./media/attract-onboard-export-data-attract-restrict-access.png)](./media/attract-onboard-export-data-attract-restrict-access.png)

3. <span data-ttu-id="fa817-153">**Bu kalıcı bir değişikliktir** uyarısını görürseniz, bu ortamdan yönetici olmayanların erişimini kalıcı olarak kısıtlamak için **Erişimi kısıtla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="fa817-153">When you see the warning **This is a permanent change**, select **Restrict access** to permanently restrict non-admin users from this environment.</span></span> <span data-ttu-id="fa817-154">Bu adımı tamamlamaya hazırsanız **İptal et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="fa817-154">If you're not ready to complete this step, select **Cancel**.</span></span>

   ![[<span data-ttu-id="fa817-155">Erişimi kısıtlamanın kalıcı bir değişiklik olduğu uyarısı</span><span class="sxs-lookup"><span data-stu-id="fa817-155">Warning that restricting access is a permanent change</span></span>](./media/attract-onboard-export-data-attract-warning.png)](./media/attract-onboard-export-data-attract-warning.png)

   >[!NOTE]
   ><span data-ttu-id="fa817-156">Attract ortamına erişimi kısıtladıktan sonra, Yöneticiler veri dışa aktarma ve kişi rapor sayfalarına erişmeye devam edebilir.</span><span class="sxs-lookup"><span data-stu-id="fa817-156">Admins can continue to access the data export and person report pages after you restrict access to the Attract environment.</span></span>

## <a name="export-data-from-onboard"></a><span data-ttu-id="fa817-157">Verileri Onboard'tan dışa aktar</span><span class="sxs-lookup"><span data-stu-id="fa817-157">Export data from Onboard</span></span>

<span data-ttu-id="fa817-158">Hazır olduğunuzda, şablonları, kılavuzları ve aday verilerini Onboard'tan karşıdan yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fa817-158">When you're ready, you can download templates, guides, and candidate data from Onboard.</span></span>

1. <span data-ttu-id="fa817-159">[https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport) gidin.</span><span class="sxs-lookup"><span data-stu-id="fa817-159">Go to [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).</span></span>

2. <span data-ttu-id="fa817-160">**Veri dışa aktarma** altında, **Veri dışa aktarma talebi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="fa817-160">Under **Data export**, select **Request a data export**.</span></span> 

   ![[<span data-ttu-id="fa817-161">Onboard üzerinden bir veri dışa aktarma talep edin</span><span class="sxs-lookup"><span data-stu-id="fa817-161">Request a data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-request.png)](./media/attract-onboard-export-data-onboard-request.png)

3. <span data-ttu-id="fa817-162">**İsteğiniz işleniyor** mesaj kutusu görüntülendiğinde, **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="fa817-162">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="fa817-163">Veri dışa aktarma 20 dakika kadar sürebilir, dışa aktarmanızın ebatlarına bağlı olarak.</span><span class="sxs-lookup"><span data-stu-id="fa817-163">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="fa817-164">Dışa aktarma işlemi tamamlandığında, yanındaki **İndir** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="fa817-164">When your export completes, select the **Download** button next to it.</span></span> 

   ![[<span data-ttu-id="fa817-165">Onboard'tan dışa aktarma verisini indirmek</span><span class="sxs-lookup"><span data-stu-id="fa817-165">Download data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-download.png)](./media/attract-onboard-export-data-onboard-download.png)

   >[!NOTE]
   ><span data-ttu-id="fa817-166">Veri dışa aktarma isteğiniz yedi gün süreyle kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="fa817-166">Your data export is available for seven days.</span></span> <span data-ttu-id="fa817-167">Yedi gün sonra, **karşıdan yükleme** bağlantısının süresi dolar ve verilerinizi tekrar yüklemeniz gerekiyorsa, yeni bir dışa aktarma istemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="fa817-167">After seven days, the **Download** link expires, and you must request a new export if you need to download your data again.</span></span> <span data-ttu-id="fa817-168">Yeni dışa veri aktarma işlemi başlattığınızda, yeni verme işlemi başarılı olduktan sonra varolan tüm karşıdan yükleme işlemleri sona erer.</span><span class="sxs-lookup"><span data-stu-id="fa817-168">When you start a new data export, any existing downloads will expire after the new export succeeds.</span></span>

<span data-ttu-id="fa817-169">Bu yükleme, aşağıdakileri içeren bir .zip dosyasıdır:</span><span class="sxs-lookup"><span data-stu-id="fa817-169">The download is a .zip file that contains:</span></span>

- <span data-ttu-id="fa817-170">Onboard şablonlarınızı bir Word belgesi biçiminde içeren bir **Şablonlar** klasörü.</span><span class="sxs-lookup"><span data-stu-id="fa817-170">A **Templates** folder that contains your Onboard templates in Word document format.</span></span>

- <span data-ttu-id="fa817-171">Onboard kılavuzlarınızı bir Word belgesi biçiminde içeren bir **Guides** klasörü.</span><span class="sxs-lookup"><span data-stu-id="fa817-171">A **Guides** folder that contains your Onboard guides in Word document format.</span></span>

## <a name="see-also"></a><span data-ttu-id="fa817-172">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="fa817-172">See also</span></span>

[<span data-ttu-id="fa817-173">Dynamics 365 Talent: Attract ve Dynamics 365 Talent: Onboard Uygulamalarının devre dışı bırakılması</span><span class="sxs-lookup"><span data-stu-id="fa817-173">Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)