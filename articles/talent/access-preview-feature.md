---
title: Özellikleri yönetme
description: Bu konu Microsoft Dynamics 365 Talent içindeki önizleme özelliklerini bir yöneticinin nasıl etkinleştirebileceğini tanımlar ve önizleme için etkin olan özellikleri listeler.
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
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.1.0, Talent
ms.openlocfilehash: d818e9e04ce88e5ab285ef8176334809447fb477
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124808"
---
# <a name="manage-features"></a><span data-ttu-id="b3269-103">Özellikleri yönetme</span><span class="sxs-lookup"><span data-stu-id="b3269-103">Manage features</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b3269-104">Microsoft Dynamics 365 Human Resources için sürekli olarak kullanıma sunduğumuz insan sermayesi yönetim döngüsü (HCM) özelliklerinin bir parçası olarak, müşterilerimizin yeni özellikleri mümkün olan en kısa sürede deneyimlemesini istiyoruz.</span><span class="sxs-lookup"><span data-stu-id="b3269-104">As part of our continuous rollout of human capital management (HCM) capabilities for Microsoft Dynamics 365 Human Resources, we want to let customers experience new features as soon as possible.</span></span> <span data-ttu-id="b3269-105">Yöneticiler önizleme özelliklerini kendi ortamlarında görebilir ve kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="b3269-105">Administrators can see and use preview features in their environments.</span></span> <span data-ttu-id="b3269-106">Bu özellikler neredeyse genel kullanıma sunulmak üzere hazır durumdadır ve kapsamlı bir sınamadan geçirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="b3269-106">These features are almost ready for general availability and have gone through extensive testing.</span></span> <span data-ttu-id="b3269-107">Bu özellikleri genel kullanım için yayımlamadan önce müşterilerimizden son kez geribildirim almak istiyoruz.</span><span class="sxs-lookup"><span data-stu-id="b3269-107">We're just looking for a final round of customer feedback and validation before we release them for general availability.</span></span>

<span data-ttu-id="b3269-108">Bu konu önizleme özelliklerini nasıl etkinleştirebileceğinizi tanımlar ve önizleme için kullanılabilir olan özellikleri listeler.</span><span class="sxs-lookup"><span data-stu-id="b3269-108">This topic describes how you can enable preview features, and it lists the features that are currently available for preview.</span></span> <span data-ttu-id="b3269-109">Bu liste özellikler genel kullanım için yayımladıkça ve yeni özellikler önizleme için yayımlandıkça güncelleştirilecektir.</span><span class="sxs-lookup"><span data-stu-id="b3269-109">This list will be updated as features are released to general availability and as new features are released to preview.</span></span> <span data-ttu-id="b3269-110">Yeni özellikler önizleme için yayımlandığında bildirim gönderilmeyecektir.</span><span class="sxs-lookup"><span data-stu-id="b3269-110">No notification is given when new features are released to preview.</span></span> <span data-ttu-id="b3269-111">Kullanıcılar özellikleri görmeye başlayacaktır.</span><span class="sxs-lookup"><span data-stu-id="b3269-111">Users will just start to see the features.</span></span> <span data-ttu-id="b3269-112">Talent içindeki yeni özellikler hakkında daha fazla bilgi için bkz. [Dynamics 365 Talent içinde neler yeni veya değişti](./whats-new.md) ve [Dynamics 365 ve Power Platform Sürüm Notları](https://docs.microsoft.com/business-applications-release-notes).</span><span class="sxs-lookup"><span data-stu-id="b3269-112">For more information about new features in Talent, see [What's new or changed in Dynamics 365 Talent](./whats-new.md) and [Dynamics 365 and Power Platform Release Notes](https://docs.microsoft.com/business-applications-release-notes).</span></span>

## <a name="enable-or-disable-preview-features"></a><span data-ttu-id="b3269-113">Önizleme özelliklerini etkinleştirme veya devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="b3269-113">Enable or disable preview features</span></span>

<span data-ttu-id="b3269-114">Önizleme özelliklerine erişmek için, önce ortamınızda etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b3269-114">To access preview features, you must first enable them in your environment.</span></span> <span data-ttu-id="b3269-115">Önizleme özelliklerini devre dışı bırakma veya etkinleştirme ortama özgüdür.</span><span class="sxs-lookup"><span data-stu-id="b3269-115">Enabling or disabling preview features is environment-specific.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b3269-116">**Önizleme özellikleri** ayarını açtığınızda, kuruluşunuzda bulunan bu ortamdaki tüm kullanıcılar için önizleme özelliklerini etkinleştirirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b3269-116">When you turn on the **Preview Features** setting, you enable preview features for all users in your organization who are in that environment.</span></span> <span data-ttu-id="b3269-117">Ayarı kapattığınızda, önizleme özelliklerini devre dışı bırakırsınız ve kullanıcılarınız bu özelliklere erişemez.</span><span class="sxs-lookup"><span data-stu-id="b3269-117">When you turn off the setting, you disable preview features and make them inaccessible to your users.</span></span> <span data-ttu-id="b3269-118">Önizleme özellikleri Talent'ta sınırlı şekilde desteklenir.</span><span class="sxs-lookup"><span data-stu-id="b3269-118">Preview features have limited support in Talent.</span></span> <span data-ttu-id="b3269-119">Daha az gizlilik ve güvenlik önemi kullanabilirler ve Talent hizmet düzeyi sözleşmene (SLA) dahil değildirler.</span><span class="sxs-lookup"><span data-stu-id="b3269-119">They might use fewer privacy and security measures, and they aren't included in the Talent service level agreement (SLA).</span></span> <span data-ttu-id="b3269-120">Kişisel verileri (diğer bir deyişle, sizi tanımlamaya yardımcı olabilecek tüm bilgileri) işlemek ya da yasa veya düzenlemelerle uyumluluk gereksinimlerine tabi olan diğer verileri işlemek için önizleme özelliklerini kullanmamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b3269-120">You should not use preview features to process personal data (that is, any information that could identify you), or to process other data that is subject to legal or regulatory compliance requirements.</span></span>

### <a name="attract"></a><span data-ttu-id="b3269-121">Attract</span><span class="sxs-lookup"><span data-stu-id="b3269-121">Attract</span></span>

1. <span data-ttu-id="b3269-122">Microsoft Dynamics 365 Talent: Attract'te oturum açın.</span><span class="sxs-lookup"><span data-stu-id="b3269-122">Sign in to Microsoft Dynamics 365 Talent: Attract.</span></span>
2. <span data-ttu-id="b3269-123">Sağ üst köşedeki **Kurulum** menüsünden (çark simgesi) **Yönetici merkezi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="b3269-123">On the **Setup** menu (the gear symbol) in the upper-right corner, select **Admin center**.</span></span>
3. <span data-ttu-id="b3269-124">**Özellik yönetimi** sekmesinde **Önizleme özellikleri** yanındaki seçeneği seçin. Seçildiğinde mavi renge dönecektir ve **Açık** ibaresini görüntüleyecektir.</span><span class="sxs-lookup"><span data-stu-id="b3269-124">On the **Feature management** tab, select the option next to **Preview features** so that it turns blue and says **On**.</span></span>

    ![Attract içinde önizleme özelliklerini etkinleştirme](./media/attract-enable-preview-features.png)

4. <span data-ttu-id="b3269-126">Bireysel önizleme özellikleri seçimini seçin veya iptal edin.</span><span class="sxs-lookup"><span data-stu-id="b3269-126">Select or cancel the selection of individual preview features.</span></span> <span data-ttu-id="b3269-127">Hiçbir şey yapmazsanız, var olan tüm önizleme özellikleri etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="b3269-127">If you do nothing, all available preview features are enabled.</span></span>
5. <span data-ttu-id="b3269-128">Yeni özellikleri görmek için tarayıcınızı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="b3269-128">Refresh your browser to start to see the new features.</span></span> <span data-ttu-id="b3269-129">Zaten oturum açmış kullanıcılar özellikleri daha sonra yeniden oturum açtıklarında görürler veya özellikleri hemen görmek için tarayıcıyı yenileyebilirler.</span><span class="sxs-lookup"><span data-stu-id="b3269-129">Any users who are already signed in will see the features the next time they sign in, or they can refresh their browser to see the features immediately.</span></span>

> [!NOTE]
> <span data-ttu-id="b3269-130">Bazı önizleme özellikleri için ek konfigürasyon gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="b3269-130">Some preview features might require additional configuration.</span></span> <span data-ttu-id="b3269-131">Kurulum işleminin tamamlanması için önizleme özelliğinin yanındaki bağlantıları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b3269-131">Follow the links next to the preview feature to complete the setup for it.</span></span>

## <a name="feedback"></a><span data-ttu-id="b3269-132">Bildirim</span><span class="sxs-lookup"><span data-stu-id="b3269-132">Feedback</span></span>

<span data-ttu-id="b3269-133">Bu önizleme özelliklerinden herhangi biriyle ilgili deneyiminizden haberdar olmak istiyoruz.</span><span class="sxs-lookup"><span data-stu-id="b3269-133">We want to hear from you about your experience with any of these preview features.</span></span> <span data-ttu-id="b3269-134">Bu özellikleri veya diğer yeni özellikleri kullandıkça aşağıdaki sitelerden bize düzenli olarak geribildirim göndermenizi rica ediyoruz:</span><span class="sxs-lookup"><span data-stu-id="b3269-134">We encourage you to regularly post your feedback on the following sites as you use these or any other features:</span></span>

- <span data-ttu-id="b3269-135">[Topluluk](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – Bu, kullanıcıların olayları tartışabileceği, sorular sorabileceği ve topluluktan yardım alabileceği yararlı bir kaynaktır.</span><span class="sxs-lookup"><span data-stu-id="b3269-135">[Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – This site is a great resource where users can discuss use cases, ask questions, and get community help.</span></span>
- <span data-ttu-id="b3269-136">Üründe görmek istediğiniz özellikleri ve mevcut özellikler için yapmamız gerektiğini düşündüğünüz herhangi bir değişikliği bize bildirin.</span><span class="sxs-lookup"><span data-stu-id="b3269-136">Let us know about features that you want to see in the product, or let us know about any changes you think we should make to existing features.</span></span> <span data-ttu-id="b3269-137">Aşağıdaki sitelerde ürün fikirleri önerin:</span><span class="sxs-lookup"><span data-stu-id="b3269-137">Suggest product ideas on the following sites:</span></span>

    - [<span data-ttu-id="b3269-138">Attract fikirleri</span><span class="sxs-lookup"><span data-stu-id="b3269-138">Attract ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [<span data-ttu-id="b3269-139">Onboard fikirleri</span><span class="sxs-lookup"><span data-stu-id="b3269-139">Onboard ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Onboard/idb-p/Onboard)

<span data-ttu-id="b3269-140">Kişisel verilerinizi (sizi tanımlamaya yardımcı olabilecek bilgiler) geribildiriminize veya ürün incelemesi gönderimlerinize eklemediğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="b3269-140">Make sure that you don't include personal data (any information that could identify you) in your feedback or product review submissions.</span></span> <span data-ttu-id="b3269-141">Toplanan bilgiler daha ayrıntılı incelenebilir ve yürürlükteki gizlilik yasaları kapsamında talepleri yanıtlamak için kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="b3269-141">Collected information might be analyzed further and isn't used to answer requests under applicable privacy laws.</span></span> <span data-ttu-id="b3269-142">Bu programlar altında ayrı olarak toplanan kişisel veriler [Microsoft Gizlilik Bildirimi](https://privacy.microsoft.com/privacystatement)'ne tabidir.</span><span class="sxs-lookup"><span data-stu-id="b3269-142">Personal data that is collected separately under these programs is subject to the [Microsoft Privacy Statement](https://privacy.microsoft.com/privacystatement).</span></span>

> [!TIP]
> <span data-ttu-id="b3269-143">Bu konuyu işaretleyin ve yayımladığımızda yeni önizleme özelliklerinden haberdar olmak için sık sık kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="b3269-143">Bookmark this topic, and check back often to stay up to date about new preview features as we release them.</span></span>

## <a name="see-also"></a><span data-ttu-id="b3269-144">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="b3269-144">See also</span></span>

- [<span data-ttu-id="b3269-145">Talent uygulamaları deneyin vey asatın alın</span><span class="sxs-lookup"><span data-stu-id="b3269-145">Try or buy Talent apps</span></span>](https://dynamics.microsoft.com/talent/overview/)
- [<span data-ttu-id="b3269-146">Dynamics 365 Talent'teki yenilikler veya değişiklikler</span><span class="sxs-lookup"><span data-stu-id="b3269-146">What's new or changed in Dynamics 365 Talent</span></span>](./whats-new.md)
- [<span data-ttu-id="b3269-147">Sürüm planları</span><span class="sxs-lookup"><span data-stu-id="b3269-147">Release plans</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="b3269-148">Microsoft Dynamics 365 Talent için destek alma</span><span class="sxs-lookup"><span data-stu-id="b3269-148">Get support for Microsoft Dynamics 365 Talent</span></span>](./talent-support.md)
