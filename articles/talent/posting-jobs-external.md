---
title: Attract'tan harici kariyer sitelerinde iş ilanları yayınlama
description: Bu kon, harici işe alma sitelerine Dynamics 365 for Talent - Attract kullanarak ilan vermeyi açıklar
author: pganapmsft
manager: AnnBe
ms.date: 03/20/2019
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
ms.openlocfilehash: eca599ad189edae29ef2de496196b08799a5e745
ms.sourcegitcommit: 1653d1e28d02f8a9a4bea8df562ac98d7a350ed1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/15/2019
ms.locfileid: "993680"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a><span data-ttu-id="ec2b5-103">Attract'tan harici kariyer sitelerinde iş ilanları yayınlama</span><span class="sxs-lookup"><span data-stu-id="ec2b5-103">Post jobs to external career sites from Attract</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec2b5-104">Açık pozisyonlarınızı olabildiğince fazla kalifiye adayın önüne sunmak istersiniz.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="ec2b5-105">Broadbean gibi işe alma siteleri bu hedefinizi gerçekleştirmeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="ec2b5-106">Microsoft Dynamics 365 Talent: Attract, şimdi Broadbean'e iş ilanları vermenize olanak sağlar ve Microsoft düzenli olarak bu alanda yeni olanaklar sağlar.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

## <a name="post-jobs-to-broadbean"></a><span data-ttu-id="ec2b5-107">Broadbean'e iş ilanları vermek</span><span class="sxs-lookup"><span data-stu-id="ec2b5-107">Post jobs to Broadbean</span></span>

<span data-ttu-id="ec2b5-108">Broadbean'e iş ilanları verebilmeden önce, Broadbean tümleştirmesini yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-108">Before you can post jobs to Broadbean, you must configure the Broadbean integration.</span></span>

> [!NOTE]
> - <span data-ttu-id="ec2b5-109">Harici sitelere iş ilanı verebilmek için [Kapsamlı işe alma eklentisine](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-109">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="ec2b5-110">Bu özellik şu anda önizlemededir.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-110">This feature is currently in preview.</span></span> <span data-ttu-id="ec2b5-111">Denemek isterseniz, [Attract yönetici ayarlarında açmanız gerekir](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="ec2b5-111">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

### <a name="configure-broadbean-integration"></a><span data-ttu-id="ec2b5-112">Broadbean tümleştirmesini yapılandırın</span><span class="sxs-lookup"><span data-stu-id="ec2b5-112">Configure Broadbean integration</span></span>

1. <span data-ttu-id="ec2b5-113">Attract'e bir yönetici olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-113">Sign in to Attract as an admin.</span></span>
2. <span data-ttu-id="ec2b5-114">**Ayarlar** düğmesini (çark simgesi) sayfanın sağ üst köşesinde seçin ve sonra **Yönetici merkezini** seçin.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-114">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>
3. <span data-ttu-id="ec2b5-115">**İş panosu ayarları** sekmesinde, **Broadbean tümleştirmesini etkinleştir** bölmesinde, tümleştirmeyi açın.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-115">On the **Job board settings** tab, in the **Enable Broadbean integration** section, turn on the integration.</span></span>
4. <span data-ttu-id="ec2b5-116">Broadbean ile iletişime geçin ve **Kullanıcı adı, İstemci Kimliği, Şifreleme Belirteci** içerisine bilgilerinizi girin.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-116">Contact Broadbean, and enter your information in **Username, Client ID, Encryption Token**.</span></span>

> [!WARNING]
> <span data-ttu-id="ec2b5-117">Broadbean kimlik bilgileriniz hassas ve gizlidir.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-117">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="ec2b5-118">Bu nedenle, bunları dikkatli bir biçimde depolayın ve paylaşın.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-118">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="ec2b5-119">Attract içinde Yönetici rolüne sahip herkes bu kimlik bilgilerini görebilir.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-119">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="ec2b5-120">Microsoft ve Attract, bu değerleri oluşturmak ve saklanmakta söz sahibi değildir.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-120">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="ec2b5-121">Attract için bunları güncel tutmak ve kimlik bilgileriniz içeren herhangi bir sorunu Broadbean ile işbirliği yaparak çözmek sizin sorumluluğunuzdur.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-121">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>

### <a name="post-a-job-to-broadbean"></a><span data-ttu-id="ec2b5-122">Broadbean'e bir iş ilanı vermek</span><span class="sxs-lookup"><span data-stu-id="ec2b5-122">Post a job to Broadbean</span></span>

<span data-ttu-id="ec2b5-123">Broadbean açıldıktan sonra, işe alımcılar ve yöneticiler buraya iş ilanı gönderebilirler.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-123">After Broadbean has been turned on, recruiters and admins can post a job to it.</span></span> <span data-ttu-id="ec2b5-124">İş için bir başvur URL'sine sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-124">You must have an apply URL for the job.</span></span>

1. <span data-ttu-id="ec2b5-125">Attract içinde, Broadbean'e nakletmek istediğiniz işi açın.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-125">In Attract, open the job that you want to post to Broadbean.</span></span>
2. <span data-ttu-id="ec2b5-126">**İlanlar** bölmesinde, Broadbean'e karşılık gelen **Şimdi İlan Ver** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-126">In the **Postings** section, select the **Post Now** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="ec2b5-127">Broadbean penceresindeki talimatları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-127">Follow the instructions in the Broadbean window.</span></span>

<span data-ttu-id="ec2b5-128">Attract aşağıdaki bilgileri Broadbean'e aktarır:</span><span class="sxs-lookup"><span data-stu-id="ec2b5-128">Attract passes the following information to Broadbean:</span></span>

- <span data-ttu-id="ec2b5-129">Talep Kodu</span><span class="sxs-lookup"><span data-stu-id="ec2b5-129">Request ID</span></span>
- <span data-ttu-id="ec2b5-130">İş unvanı</span><span class="sxs-lookup"><span data-stu-id="ec2b5-130">Job title</span></span>
- <span data-ttu-id="ec2b5-131">İş açıklaması</span><span class="sxs-lookup"><span data-stu-id="ec2b5-131">Job description</span></span>
- <span data-ttu-id="ec2b5-132">İş konumu</span><span class="sxs-lookup"><span data-stu-id="ec2b5-132">Job location</span></span>
- <span data-ttu-id="ec2b5-133">Başvur URL'si</span><span class="sxs-lookup"><span data-stu-id="ec2b5-133">Apply URL</span></span>
- <span data-ttu-id="ec2b5-134">İşe alan bilgileri</span><span class="sxs-lookup"><span data-stu-id="ec2b5-134">Recruiter information</span></span>

<span data-ttu-id="ec2b5-135">Broadbean ilan vermeyi başarıyla tamamladıktan sonra, Attract içindeki **İlanlar** bölümü, Broadbean durumunu **İlan verildi** olarak gösterir.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-135">After Broadbean successfully completes the posting, the **Postings** section of the job in Attract shows the Broadbean status as **Posted**.</span></span>

> [!NOTE]
> - <span data-ttu-id="ec2b5-136">Broadbean **Endüstri** alanına ihtiyaç duyar.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-136">Broadbean requires the **Industry** field.</span></span> <span data-ttu-id="ec2b5-137">Şu anda bu alan varsayılan olarak **BT** olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-137">Currently, this field is set to **IT** by default.</span></span> <span data-ttu-id="ec2b5-138">Ancak, Broadbean iş ilanı verme sayfasında değeri doğru endüstriye değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-138">However, you can change the value to the correct industry in the window for Broadbean job posting.</span></span>
> - <span data-ttu-id="ec2b5-139">Broadbean'in iş ilanınızı seçtiğiniz tüm ilan panolarına göndermesi biraz zaman alır.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-139">It takes some time for Broadbean to finish posting your job to all the job boards that you selected.</span></span> <span data-ttu-id="ec2b5-140">Bu nedenle, Attract iş için bir durum güncelleştirmesi sağlamasından önce kısa bir gecikme olabilir.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-140">Therefore, there might be a slight delay before Attract provides a status update for the job.</span></span>

### <a name="view-a-broadbean-job-posting"></a><span data-ttu-id="ec2b5-141">Bir Broadbean iş ilanına göz atın</span><span class="sxs-lookup"><span data-stu-id="ec2b5-141">View a Broadbean job posting</span></span>

<span data-ttu-id="ec2b5-142">Bir işi Broadbean'e aktardıktan sonra, Attract içinden görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-142">After you post a job to Broadbean, you can view it from Attract.</span></span>

1. <span data-ttu-id="ec2b5-143">Attract içinde, Broadbean'de görüntülemek istediğiniz işi açın.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-143">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="ec2b5-144">**İlanlar** bölümünde, Broadbeana'e karşılık gelen üç nokta düğmesini seçin (**...**) ve sonra **Görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-144">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>

<span data-ttu-id="ec2b5-145">Broadbean iş ilanı yeni pencerede görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-145">The Broadbean job posting appears in a new window.</span></span>

### <a name="update-a-broadbean-job-posting"></a><span data-ttu-id="ec2b5-146">Bir Broadbean iş ilanını güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="ec2b5-146">Update a Broadbean job posting</span></span>

<span data-ttu-id="ec2b5-147">Bir Broadbean işini iki şekilde güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-147">You can update a Broadbean job posting in two ways.</span></span>

1. <span data-ttu-id="ec2b5-148">Attract içinde, güncelleştirmek istediğiniz işi açın.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-148">In Attract, open the job that you want to update.</span></span>
2. <span data-ttu-id="ec2b5-149">**İlanlar** bölmesinde, Broadbean'e karşılık gelen **İlanı Güncelleştir** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-149">In the **Postings** section, select the **Update Post** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="ec2b5-150">Broadbean penceresinde ilanı düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-150">Edit the posting in the Broadbean window.</span></span>

<span data-ttu-id="ec2b5-151">veya</span><span class="sxs-lookup"><span data-stu-id="ec2b5-151">–or–</span></span>

1. <span data-ttu-id="ec2b5-152">Attract içinde, Broadbean'de görüntülemek istediğiniz işi açın.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-152">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="ec2b5-153">**İlanlar** bölümünde, Broadbeana'e karşılık gelen üç nokta düğmesini seçin (**...**) ve sonra **Görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-153">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>
3. <span data-ttu-id="ec2b5-154">Broadbean penceresinde, iş ayrıntılarını düzenleyin ve işi yeniden ilan edin.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-154">In the Broadbean window, edit the job details, and then repost the job.</span></span> <span data-ttu-id="ec2b5-155">Attract içindeki iş ayrıntıları değiştirilmez.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-155">The job details in Attract aren't changed.</span></span>

### <a name="remove-a-broadbean-job-posting"></a><span data-ttu-id="ec2b5-156">Bir Broadbean iş ilanını kaldırın</span><span class="sxs-lookup"><span data-stu-id="ec2b5-156">Remove a Broadbean job posting</span></span>

<span data-ttu-id="ec2b5-157">Bir iş ilanını Broadbean'den ihtiyaç duyduğunuzda kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-157">You can remove a job posting from Broadbean as you require.</span></span>

1. <span data-ttu-id="ec2b5-158">Attract içinde, kaldırmak istediğiniz işi açın.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-158">In Attract, open the job that you want to remove.</span></span>
2. <span data-ttu-id="ec2b5-159">**İlanlar** bölümünde, Broadbeana'e karşılık gelen üç nokta düğmesini seçin (**...**) ve sonra **İlanı Kaldır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-159">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **Remove Post**.</span></span>

<span data-ttu-id="ec2b5-160">Broadbean işi kaldırdıktan sonra, Attract içindeki Broadbean öğesi bir **Şimdi İlan Ver** düğmesine sahip olur.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-160">After Broadbean removes the job, the Broadbean item in Attract has a **Post Now** button.</span></span> <span data-ttu-id="ec2b5-161">Bu düğmenin varlığı, işin kaldırıldığını ve yeniden ilan verilebileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-161">The presence of this button indicates that the job has been removed and can be posted again.</span></span>

### <a name="troubleshoot-the-broadbean-integration"></a><span data-ttu-id="ec2b5-162">Broadbean tümleştirmesi ile ilgili sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="ec2b5-162">Troubleshoot the Broadbean integration</span></span>

<span data-ttu-id="ec2b5-163">Bir işi Broadbean'e ilan vermekte zorluk çekiyorsanız şu adımları deneyin.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-163">If you're having trouble posting a job to Broadbean, try these steps.</span></span>

1. <span data-ttu-id="ec2b5-164">Attract içine girmiş olduğunuz Broadbean kimlik bilgilerinin doğru ve geçerli olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-164">Verify that the Broadbean credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="ec2b5-165">Kimlik bilgileri geçerli ve doğruysa, [Broadbean destek](https://www.broadbean.com/resources/support/) ile iletişime geçin.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-165">If the credentials are valid and correct, contact [Broadbean support](https://www.broadbean.com/resources/support/).</span></span>
3. <span data-ttu-id="ec2b5-166">Sorun devam ederse, [Microsoft destek](./talent-support.md) ile iletişime geçin.</span><span class="sxs-lookup"><span data-stu-id="ec2b5-166">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>
