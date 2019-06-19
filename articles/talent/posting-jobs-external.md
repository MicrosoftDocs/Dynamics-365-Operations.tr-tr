---
title: Attract'tan harici kariyer sitelerinde iş ilanları yayınlama
description: Bu kon, harici işe alma sitelerine Dynamics 365 for Talent - Attract kullanarak ilan vermeyi açıklar
author: pganapmsft
manager: AnnBe
ms.date: 05/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-03-19
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 9c27d1810a89ed7d7a7745e41c5f118dbdfe5dda
ms.sourcegitcommit: cadce85ca3004d53caf6bc49147a524c1bfd421f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/16/2019
ms.locfileid: "1590494"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a><span data-ttu-id="3326a-103">Attract'tan harici kariyer sitelerinde iş ilanları yayınlama</span><span class="sxs-lookup"><span data-stu-id="3326a-103">Post jobs to external career sites from Attract</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3326a-104">Açık pozisyonlarınızı olabildiğince fazla kalifiye adayın önüne sunmak istersiniz.</span><span class="sxs-lookup"><span data-stu-id="3326a-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="3326a-105">Broadbean gibi işe alma siteleri bu hedefinizi gerçekleştirmeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="3326a-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="3326a-106">Microsoft Dynamics 365 Talent: Attract, şimdi Broadbean'e iş ilanları vermenize olanak sağlar ve Microsoft düzenli olarak bu alanda yeni olanaklar sağlar.</span><span class="sxs-lookup"><span data-stu-id="3326a-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

## <a name="post-jobs-to-broadbean"></a><span data-ttu-id="3326a-107">Broadbean'e iş ilanları vermek</span><span class="sxs-lookup"><span data-stu-id="3326a-107">Post jobs to Broadbean</span></span>

<span data-ttu-id="3326a-108">Broadbean'e iş ilanları verebilmeden önce, Broadbean tümleştirmesini yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3326a-108">Before you can post jobs to Broadbean, you must configure the Broadbean integration.</span></span>

> [!NOTE]
> - <span data-ttu-id="3326a-109">Harici sitelere iş ilanı verebilmek için [Kapsamlı işe alma eklentisine](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3326a-109">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="3326a-110">Attract üzerinden Broadbean'a iş göndermek için bir Broadbean aboneliğine sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3326a-110">To post jobs to Broadbean through Attract, you must have a Broadbean subscription.</span></span>
> - <span data-ttu-id="3326a-111">Bu özellik şu anda önizlemededir.</span><span class="sxs-lookup"><span data-stu-id="3326a-111">This feature is currently in preview.</span></span> <span data-ttu-id="3326a-112">Denemek isterseniz, [Attract yönetici ayarlarında açmanız gerekir](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="3326a-112">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

### <a name="configure-broadbean-integration"></a><span data-ttu-id="3326a-113">Broadbean tümleştirmesini yapılandırın</span><span class="sxs-lookup"><span data-stu-id="3326a-113">Configure Broadbean integration</span></span>

1. <span data-ttu-id="3326a-114">Attract'e bir yönetici olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="3326a-114">Sign in to Attract as an admin.</span></span>
2. <span data-ttu-id="3326a-115">**Ayarlar** düğmesini (çark simgesi) sayfanın sağ üst köşesinde seçin ve sonra **Yönetici merkezini** seçin.</span><span class="sxs-lookup"><span data-stu-id="3326a-115">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>
3. <span data-ttu-id="3326a-116">**İş panosu ayarları** sekmesinde, **Broadbean tümleştirmesini etkinleştir** bölmesinde, tümleştirmeyi açın.</span><span class="sxs-lookup"><span data-stu-id="3326a-116">On the **Job board settings** tab, in the **Enable Broadbean integration** section, turn on the integration.</span></span>
4. <span data-ttu-id="3326a-117">Broadbean ile iletişime geçin ve **Kullanıcı adı, İstemci Kimliği, Şifreleme Belirteci** içerisine bilgilerinizi girin.</span><span class="sxs-lookup"><span data-stu-id="3326a-117">Contact Broadbean, and enter your information in **Username, Client ID, Encryption Token**.</span></span>

> [!WARNING]
> <span data-ttu-id="3326a-118">Broadbean kimlik bilgileriniz hassas ve gizlidir.</span><span class="sxs-lookup"><span data-stu-id="3326a-118">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="3326a-119">Bu nedenle, bunları dikkatli bir biçimde depolayın ve paylaşın.</span><span class="sxs-lookup"><span data-stu-id="3326a-119">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="3326a-120">Attract içinde Yönetici rolüne sahip herkes bu kimlik bilgilerini görebilir.</span><span class="sxs-lookup"><span data-stu-id="3326a-120">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="3326a-121">Microsoft ve Attract, bu değerleri oluşturmak ve saklanmakta söz sahibi değildir.</span><span class="sxs-lookup"><span data-stu-id="3326a-121">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="3326a-122">Attract için bunları güncel tutmak ve kimlik bilgileriniz içeren herhangi bir sorunu Broadbean ile işbirliği yaparak çözmek sizin sorumluluğunuzdur.</span><span class="sxs-lookup"><span data-stu-id="3326a-122">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>

### <a name="post-a-job-to-broadbean"></a><span data-ttu-id="3326a-123">Broadbean'e bir iş ilanı vermek</span><span class="sxs-lookup"><span data-stu-id="3326a-123">Post a job to Broadbean</span></span>

<span data-ttu-id="3326a-124">Broadbean açıldıktan sonra, işe alımcılar ve yöneticiler buraya iş ilanı gönderebilirler.</span><span class="sxs-lookup"><span data-stu-id="3326a-124">After Broadbean has been turned on, recruiters and admins can post a job to it.</span></span> <span data-ttu-id="3326a-125">İş için bir başvur URL'sine sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3326a-125">You must have an apply URL for the job.</span></span>

1. <span data-ttu-id="3326a-126">Attract içinde, Broadbean'e nakletmek istediğiniz işi açın.</span><span class="sxs-lookup"><span data-stu-id="3326a-126">In Attract, open the job that you want to post to Broadbean.</span></span>
2. <span data-ttu-id="3326a-127">**İlanlar** bölmesinde, Broadbean'e karşılık gelen **Şimdi İlan Ver** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="3326a-127">In the **Postings** section, select the **Post Now** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="3326a-128">Broadbean penceresindeki talimatları izleyin.</span><span class="sxs-lookup"><span data-stu-id="3326a-128">Follow the instructions in the Broadbean window.</span></span>

<span data-ttu-id="3326a-129">Attract aşağıdaki bilgileri Broadbean'e aktarır:</span><span class="sxs-lookup"><span data-stu-id="3326a-129">Attract passes the following information to Broadbean:</span></span>

- <span data-ttu-id="3326a-130">Talep Kodu</span><span class="sxs-lookup"><span data-stu-id="3326a-130">Request ID</span></span>
- <span data-ttu-id="3326a-131">İş unvanı</span><span class="sxs-lookup"><span data-stu-id="3326a-131">Job title</span></span>
- <span data-ttu-id="3326a-132">İş açıklaması</span><span class="sxs-lookup"><span data-stu-id="3326a-132">Job description</span></span>
- <span data-ttu-id="3326a-133">İş konumu</span><span class="sxs-lookup"><span data-stu-id="3326a-133">Job location</span></span>
- <span data-ttu-id="3326a-134">Başvur URL'si</span><span class="sxs-lookup"><span data-stu-id="3326a-134">Apply URL</span></span>
- <span data-ttu-id="3326a-135">İşe alan bilgileri</span><span class="sxs-lookup"><span data-stu-id="3326a-135">Recruiter information</span></span>

<span data-ttu-id="3326a-136">Broadbean ilan vermeyi başarıyla tamamladıktan sonra, Attract içindeki **İlanlar** bölümü, Broadbean durumunu **İlan verildi** olarak gösterir.</span><span class="sxs-lookup"><span data-stu-id="3326a-136">After Broadbean successfully completes the posting, the **Postings** section of the job in Attract shows the Broadbean status as **Posted**.</span></span>

> [!NOTE]
> - <span data-ttu-id="3326a-137">Broadbean **Endüstri** alanına ihtiyaç duyar.</span><span class="sxs-lookup"><span data-stu-id="3326a-137">Broadbean requires the **Industry** field.</span></span> <span data-ttu-id="3326a-138">Şu anda bu alan varsayılan olarak **BT** olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="3326a-138">Currently, this field is set to **IT** by default.</span></span> <span data-ttu-id="3326a-139">Ancak, Broadbean iş ilanı verme sayfasında değeri doğru endüstriye değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3326a-139">However, you can change the value to the correct industry in the window for Broadbean job posting.</span></span>
> - <span data-ttu-id="3326a-140">Broadbean'in iş ilanınızı seçtiğiniz tüm ilan panolarına göndermesi biraz zaman alır.</span><span class="sxs-lookup"><span data-stu-id="3326a-140">It takes some time for Broadbean to finish posting your job to all the job boards that you selected.</span></span> <span data-ttu-id="3326a-141">Bu nedenle, Attract iş için bir durum güncelleştirmesi sağlamasından önce kısa bir gecikme olabilir.</span><span class="sxs-lookup"><span data-stu-id="3326a-141">Therefore, there might be a slight delay before Attract provides a status update for the job.</span></span>

### <a name="view-a-broadbean-job-posting"></a><span data-ttu-id="3326a-142">Bir Broadbean iş ilanına göz atın</span><span class="sxs-lookup"><span data-stu-id="3326a-142">View a Broadbean job posting</span></span>

<span data-ttu-id="3326a-143">Bir işi Broadbean'e aktardıktan sonra, Attract içinden görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3326a-143">After you post a job to Broadbean, you can view it from Attract.</span></span>

1. <span data-ttu-id="3326a-144">Attract içinde, Broadbean'de görüntülemek istediğiniz işi açın.</span><span class="sxs-lookup"><span data-stu-id="3326a-144">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="3326a-145">**İlanlar** bölümünde, Broadbeana'e karşılık gelen üç nokta düğmesini seçin (**...**) ve sonra **Görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3326a-145">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>

<span data-ttu-id="3326a-146">Broadbean iş ilanı yeni pencerede görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="3326a-146">The Broadbean job posting appears in a new window.</span></span>

### <a name="update-a-broadbean-job-posting"></a><span data-ttu-id="3326a-147">Bir Broadbean iş ilanını güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="3326a-147">Update a Broadbean job posting</span></span>

<span data-ttu-id="3326a-148">Bir Broadbean işini iki şekilde güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3326a-148">You can update a Broadbean job posting in two ways.</span></span>

1. <span data-ttu-id="3326a-149">Attract içinde, güncelleştirmek istediğiniz işi açın.</span><span class="sxs-lookup"><span data-stu-id="3326a-149">In Attract, open the job that you want to update.</span></span>
2. <span data-ttu-id="3326a-150">**İlanlar** bölmesinde, Broadbean'e karşılık gelen **İlanı Güncelleştir** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="3326a-150">In the **Postings** section, select the **Update Post** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="3326a-151">Broadbean penceresinde ilanı düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="3326a-151">Edit the posting in the Broadbean window.</span></span>

<span data-ttu-id="3326a-152">veya</span><span class="sxs-lookup"><span data-stu-id="3326a-152">–or–</span></span>

1. <span data-ttu-id="3326a-153">Attract içinde, Broadbean'de görüntülemek istediğiniz işi açın.</span><span class="sxs-lookup"><span data-stu-id="3326a-153">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="3326a-154">**İlanlar** bölümünde, Broadbeana'e karşılık gelen üç nokta düğmesini seçin (**...**) ve sonra **Görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3326a-154">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>
3. <span data-ttu-id="3326a-155">Broadbean penceresinde, iş ayrıntılarını düzenleyin ve işi yeniden ilan edin.</span><span class="sxs-lookup"><span data-stu-id="3326a-155">In the Broadbean window, edit the job details, and then repost the job.</span></span> <span data-ttu-id="3326a-156">Attract içindeki iş ayrıntıları değiştirilmez.</span><span class="sxs-lookup"><span data-stu-id="3326a-156">The job details in Attract aren't changed.</span></span>

### <a name="remove-a-broadbean-job-posting"></a><span data-ttu-id="3326a-157">Bir Broadbean iş ilanını kaldırın</span><span class="sxs-lookup"><span data-stu-id="3326a-157">Remove a Broadbean job posting</span></span>

<span data-ttu-id="3326a-158">Bir iş ilanını Broadbean'den ihtiyaç duyduğunuzda kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3326a-158">You can remove a job posting from Broadbean as you require.</span></span>

1. <span data-ttu-id="3326a-159">Attract içinde, kaldırmak istediğiniz işi açın.</span><span class="sxs-lookup"><span data-stu-id="3326a-159">In Attract, open the job that you want to remove.</span></span>
2. <span data-ttu-id="3326a-160">**İlanlar** bölümünde, Broadbeana'e karşılık gelen üç nokta düğmesini seçin (**...**) ve sonra **İlanı Kaldır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="3326a-160">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **Remove Post**.</span></span>

<span data-ttu-id="3326a-161">Broadbean işi kaldırdıktan sonra, Attract içindeki Broadbean öğesi bir **Şimdi İlan Ver** düğmesine sahip olur.</span><span class="sxs-lookup"><span data-stu-id="3326a-161">After Broadbean removes the job, the Broadbean item in Attract has a **Post Now** button.</span></span> <span data-ttu-id="3326a-162">Bu düğmenin varlığı, işin kaldırıldığını ve yeniden ilan verilebileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3326a-162">The presence of this button indicates that the job has been removed and can be posted again.</span></span>

### <a name="troubleshoot-the-broadbean-integration"></a><span data-ttu-id="3326a-163">Broadbean tümleştirmesi ile ilgili sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="3326a-163">Troubleshoot the Broadbean integration</span></span>

<span data-ttu-id="3326a-164">Bir işi Broadbean'e ilan vermekte zorluk çekiyorsanız şu adımları deneyin.</span><span class="sxs-lookup"><span data-stu-id="3326a-164">If you're having trouble posting a job to Broadbean, try these steps.</span></span>

1. <span data-ttu-id="3326a-165">Attract içine girmiş olduğunuz Broadbean kimlik bilgilerinin doğru ve geçerli olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="3326a-165">Verify that the Broadbean credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="3326a-166">Kimlik bilgileri geçerli ve doğruysa, [Broadbean destek](https://www.broadbean.com/resources/support/) ile iletişime geçin.</span><span class="sxs-lookup"><span data-stu-id="3326a-166">If the credentials are valid and correct, contact [Broadbean support](https://www.broadbean.com/resources/support/).</span></span>
3. <span data-ttu-id="3326a-167">Sorun devam ederse, [Microsoft destek](./talent-support.md) ile iletişime geçin.</span><span class="sxs-lookup"><span data-stu-id="3326a-167">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>
