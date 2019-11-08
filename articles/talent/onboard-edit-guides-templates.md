---
title: Dynamics 365 Talent - Onboard'da işe alım ve alıştırma kılavuz ve şablonlarını düzenleme
description: Bu konuda Microsoft Dynamics 365 Talent - Onboard'da işe alım ve alıştırma kılavuz ve şablonuna etkinliklerin ve diğer bilgilerin nasıl ekleneceği açıklanmaktadır.
author: andreabichsel
manager: ''
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0f4c68acfe021e736c259e91a40ce7d43d401246
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/03/2019
ms.locfileid: "2552014"
---
# <a name="edit-onboarding-guides-and-templates-in-dynamics-365-talent---onboard"></a><span data-ttu-id="cec07-103">Dynamics 365 Talent - Onboard'da işe alım ve alıştırma kılavuz ve şablonlarını düzenleme</span><span class="sxs-lookup"><span data-stu-id="cec07-103">Edit onboarding guides and templates in Dynamics 365 Talent - Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cec07-104">Microsoft Dynamics 365 Talent: Onboard'da işe alım ve alıştırma kılavuzu veya şablonu oluşturduktan sonra giriş, etkinlik, ilgili kişi ve kaynak eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="cec07-104">After you create an onboarding guide or template in Microsoft Dynamics 365 Talent: Onboard, you must add an introduction, activities, contacts, and resources.</span></span> <span data-ttu-id="cec07-105">Onboard, işe alım kılavuzlarınıza aşağıdakiler dahil olmak üzere zengin içerik eklemenizi sağlar:</span><span class="sxs-lookup"><span data-stu-id="cec07-105">Onboard lets you include rich content in your onboarding guides, including:</span></span>

- <span data-ttu-id="cec07-106">YouTube videoları</span><span class="sxs-lookup"><span data-stu-id="cec07-106">YouTube videos</span></span>
- <span data-ttu-id="cec07-107">Microsoft Sway sunuları</span><span class="sxs-lookup"><span data-stu-id="cec07-107">Microsoft Sway presentations</span></span>
- <span data-ttu-id="cec07-108">Microsoft PowerApps uygulamaları</span><span class="sxs-lookup"><span data-stu-id="cec07-108">Microsoft PowerApps apps</span></span>
- <span data-ttu-id="cec07-109">Microsoft Stream videoları</span><span class="sxs-lookup"><span data-stu-id="cec07-109">Microsoft Stream videos</span></span>
- <span data-ttu-id="cec07-110">Microsoft Forms formları</span><span class="sxs-lookup"><span data-stu-id="cec07-110">Microsoft Forms forms</span></span>
- <span data-ttu-id="cec07-111">Web içeriği içeren iframe'ler</span><span class="sxs-lookup"><span data-stu-id="cec07-111">Iframes that contains web content</span></span>

## <a name="edit-introductions-or-activities-imported-from-a-template"></a><span data-ttu-id="cec07-112">Bir şablondan içe aktarılan tanıtımları veya faaliyetleri düzenle</span><span class="sxs-lookup"><span data-stu-id="cec07-112">Edit introductions or activities imported from a template</span></span>

<span data-ttu-id="cec07-113">Bir şablondan işe alım kılavuzu oluşturursanız veya bir şablondaki faaliyetleri bir başkasına içe aktardığınızda, içe aktarılan faaliyetlerde bir **Kilit** düğmesi görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="cec07-113">If you create an onboarding guide from a template, or if you import activities from one template into another, you'll notice a **Lock** button on the imported activities.</span></span> <span data-ttu-id="cec07-114">Bunlara *yönetilen faaliyetler* denir.</span><span class="sxs-lookup"><span data-stu-id="cec07-114">These are called *managed activities*.</span></span>

<span data-ttu-id="cec07-115">[![Yönetilen faaliyetler](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span><span class="sxs-lookup"><span data-stu-id="cec07-115">[![Managed activities](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span></span>

<span data-ttu-id="cec07-116">Yönetilen bir aktiviteyi seçtiğinizde, faaliyetin en üstünde kaynak şablonu görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cec07-116">When you select a managed activity, you can see the source template at the top of the activity.</span></span>

<span data-ttu-id="cec07-117">[![Yönetilen etkinlik kaynağı](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span><span class="sxs-lookup"><span data-stu-id="cec07-117">[![Managed activity source](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span></span>

<span data-ttu-id="cec07-118">Bir şablonda aktivite düzenlerseniz, Onboard, tüm şablonlara ve bu şablonu temel alan gönderilmemiş kılavuzlara değişiklikleri sağlar.</span><span class="sxs-lookup"><span data-stu-id="cec07-118">If you edit an activity in a template, Onboard will push the changes to all templates and unsent guides that are based on that template.</span></span> <span data-ttu-id="cec07-119">Düzenlediğiniz şablonu temel alan gönderilmemiş bir kılavuz seçer ve kılavuzdaki **etkinlikler** sekmesini seçerseniz, kılavuzun değiştiğine ilişkin bir bildirim görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="cec07-119">If you select an unsent guide based on a template you edited and then select the **Activities** tab in the guide, you will see a notice that your guide has changed.</span></span> <span data-ttu-id="cec07-120">Bildirimi kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cec07-120">To dismiss the notification, select **OK**.</span></span> 

<span data-ttu-id="cec07-121">[![Değişiklik Bildirimi](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span><span class="sxs-lookup"><span data-stu-id="cec07-121">[![Change notification](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span></span>

<span data-ttu-id="cec07-122">Güncellenmiş etkinliklerin yanında siyah bir nokta göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="cec07-122">You'll see a black dot next to the updated activities.</span></span>

<span data-ttu-id="cec07-123">[![Değiştirilen faaliyet](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span><span class="sxs-lookup"><span data-stu-id="cec07-123">[![Changed activity](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span></span>

<span data-ttu-id="cec07-124">Faaliyetin sağ bölümüne atanan, son tarih veya başka bilgiler eklemek dışında, yönetilen faaliyetleri özgün şablon dışında düzenleyemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="cec07-124">You can't edit managed activities outside of the original template, except to add an assignee, due date, or other information in the right-hand section of the activity.</span></span>

<span data-ttu-id="cec07-125">Yönetilen bir aktiviteyi düzenlemek istiyorsanız veya bir etkinliğin geldiği şablondan gelen güncelleştirmeleri almasını istemiyorsanız, o faaliyetin **Kilit** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="cec07-125">If you want to edit a managed activity, or if you don't want an activity to receive updates from the template it came from, select the **Lock** button for that activity.</span></span> <span data-ttu-id="cec07-126">**Kilit** düğmesi kaybolur.</span><span class="sxs-lookup"><span data-stu-id="cec07-126">The **Lock** button will disappear.</span></span> <span data-ttu-id="cec07-127">Faaliyet artık özgün şablon tarafından yönetilmeyecek ve artık bu şablondan güncelleştirme almayacak.</span><span class="sxs-lookup"><span data-stu-id="cec07-127">The activity will no longer be managed by the original template, and it will no longer receive updates from that template.</span></span> <span data-ttu-id="cec07-128">Bir etkinlikte yaptığınız güncelleştirmeler özgün şablonu etkilemez.</span><span class="sxs-lookup"><span data-stu-id="cec07-128">Updates you make to an activity do not affect the original template.</span></span>

<span data-ttu-id="cec07-129">Bir kılavuzdan gelen bir aktiviteyi siler ve bu kılavuzun şablonundaki değişiklikleri gönder seçeneğini tıklattığınızda, etkinlik rehberde silinmiş olarak kalır.</span><span class="sxs-lookup"><span data-stu-id="cec07-129">If you delete an activity from a guide and push changes from that guide's template, the activity will remain deleted in the guide.</span></span>

> [!NOTE]
> <span data-ttu-id="cec07-130">İlgili kişiler ve kaynaklar şablonlar tarafından yönetilmiyor.</span><span class="sxs-lookup"><span data-stu-id="cec07-130">Contacts and resources aren't managed by templates.</span></span> <span data-ttu-id="cec07-131">Ayrıca, bölümler yönetilmez, bu nedenle bir şablona bölüm eklerseniz veya düzenlerseniz, değişiklikler bu şablonu kullanan tüm kılavuzlara veya şablonlara itilecektir.</span><span class="sxs-lookup"><span data-stu-id="cec07-131">In addition, sections aren't managed, so if you add or edit a section in a template, the changes won't be pushed to any guides or templates that use that template.</span></span>
> 
> <span data-ttu-id="cec07-132">Bir şablona yeni aktiviteler eklerseniz, yeni aktiviteler o şablonu temel alan kılavuzlara ve şablonlara itilir ve yeni aktiviteler en üstte görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="cec07-132">If you add new activities to a template, the new activities are pushed to guides and templates based on that template, and the new activities display at the top.</span></span>

## <a name="import-activities-from-another-template"></a><span data-ttu-id="cec07-133">Başka bir şablondan faaliyetleri içe aktar</span><span class="sxs-lookup"><span data-stu-id="cec07-133">Import activities from another template</span></span>

<span data-ttu-id="cec07-134">Bir veya daha fazla şablonu bir kılavuza veya şablona içe aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cec07-134">You can import activities from one or more templates into a guide or template.</span></span>

1. <span data-ttu-id="cec07-135">Düzenlemek istediğiniz kılavuzu veya şablonu seçin.</span><span class="sxs-lookup"><span data-stu-id="cec07-135">Select the guide or template you want to edit.</span></span>

2. <span data-ttu-id="cec07-136">**Faaliyetler** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="cec07-136">Select the **Activities** tab.</span></span>

3. <span data-ttu-id="cec07-137">Sağdaki bölümde **içe aktar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="cec07-137">Select the **Import** tab in the section on the right.</span></span>

   <span data-ttu-id="cec07-138">[![Faaliyetleri içe aktar](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span><span class="sxs-lookup"><span data-stu-id="cec07-138">[![Import activities](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span></span>

4. <span data-ttu-id="cec07-139">Görevleri tarayıcınızda yeni bir sekmede önizlemek için, herhangi bir şablonda **yeni sekme ile aç** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="cec07-139">To preview the tasks in a new tab in your browser, select the **Open in new tab** button on any template.</span></span>

   <span data-ttu-id="cec07-140">[![Faaliyetleri içe aktar](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span><span class="sxs-lookup"><span data-stu-id="cec07-140">[![Import activities](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span></span>

5. <span data-ttu-id="cec07-141">İstenen şablonu sürükleyip kılavuz şablonunda etkinliklerin görünmesini istediğiniz yere sürükleyin ve bırakın.</span><span class="sxs-lookup"><span data-stu-id="cec07-141">Drag and drop the desired template to the place in your guide template where you want the activities to appear.</span></span> <span data-ttu-id="cec07-142">Kılavuzunuz veya şablonunuzu düzenlemeye devam edin.</span><span class="sxs-lookup"><span data-stu-id="cec07-142">Continue editing your guide or template.</span></span>

<span data-ttu-id="cec07-143">İçe aktarılan faaliyetler, bu aktivitelerin içe aktardığınız şablon tarafından yönetildiğini gösteren bir **Kilit** düğmesi içerir.</span><span class="sxs-lookup"><span data-stu-id="cec07-143">The imported activities will contain a **Lock** button, which indicates those activities are managed by the template you imported from.</span></span> <span data-ttu-id="cec07-144">İçe aktardığınız şablonda değişiklik yaptığınızda, bu aktiviteler bunları içe aktardığınız şablonda güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="cec07-144">When you make changes to the template you imported, those activities will update in the template you imported them to.</span></span> <span data-ttu-id="cec07-145">Ancak değişiklikler, içe aktardığınız şablondan oluşturulan herhangi bir kılavuza otomatik olarak itilecektir.</span><span class="sxs-lookup"><span data-stu-id="cec07-145">However, the changes will not be pushed automatically to any guides created from the template you imported to.</span></span>

## <a name="push-changes-from-a-template-to-other-templates-or-guides"></a><span data-ttu-id="cec07-146">Değişiklikleri şablondan diğer şablonlara veya kılavuzlara gönderme</span><span class="sxs-lookup"><span data-stu-id="cec07-146">Push changes from a template to other templates or guides</span></span>

<span data-ttu-id="cec07-147">Başka şablon veya kılavuzlarda kullanılan etkinlikleri içeren bir şablonu düzenlerseniz, bunların diğer şablonlarda veya kılavuzlarda görünmesini istiyorsanız, değişiklikleri gönderin.</span><span class="sxs-lookup"><span data-stu-id="cec07-147">If you edit a template that contains activities that are used in other templates or guides, you must push the changes if you want them to appear in the other templates or guides.</span></span>

<span data-ttu-id="cec07-148">Şablonunuzun aktivitelerinin başka şablonlarda veya kılavuzlarda kullanıldığından emin değilseniz, bu etkinliklerin nerede göründüğünü görüntülemek için **Kullanılacak yer** sekmesinde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="cec07-148">If you're not sure whether your template's activities are used in other templates or guides, select the **Used in** tab to view where those activities appear.</span></span>

   <span data-ttu-id="cec07-149">[![Faaliyetlerin kullanıldığı kılavuzları ve şablonları görüntüle](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span><span class="sxs-lookup"><span data-stu-id="cec07-149">[![View guides and templates activities are used in](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span></span>

<span data-ttu-id="cec07-150">Değişikliklerinizi göndermek için:</span><span class="sxs-lookup"><span data-stu-id="cec07-150">To push your changes:</span></span>

1. <span data-ttu-id="cec07-151">**Kaydet** düğmesini seçerek değişikliklerinizi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="cec07-151">Save your changes by selecting the **Save** button.</span></span> <span data-ttu-id="cec07-152">Bunu yapmazsanız, sonraki adımda yaptığınız değişiklikleri kaydetmeniz istenecektir.</span><span class="sxs-lookup"><span data-stu-id="cec07-152">If you don't do this, you'll be prompted to save your changes in the next step.</span></span>

2. <span data-ttu-id="cec07-153">**Bu değişiklikleri gönder**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="cec07-153">Select **Push these changes**.</span></span>

   
## <a name="add-or-edit-an-introduction"></a><span data-ttu-id="cec07-154">Giriş ekleme veya düzenleme</span><span class="sxs-lookup"><span data-stu-id="cec07-154">Add or edit an introduction</span></span>

1. <span data-ttu-id="cec07-155">**Giriş** sekmesinde, kılavuzunuz ve bir açılış mesajı için bir başlık girin.</span><span class="sxs-lookup"><span data-stu-id="cec07-155">On the **Introduction** tab, enter a title for your guide and an opening message.</span></span> <span data-ttu-id="cec07-156">Örnek metni kullanmak için **Bu iletiyi kullan**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cec07-156">To use the sample text, select **Use this message**.</span></span>

    <span data-ttu-id="cec07-157">[![Onboard şablonunda giriş sekmesi](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span><span class="sxs-lookup"><span data-stu-id="cec07-157">[![Introduction tab in an Onboard template](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span></span>

2. <span data-ttu-id="cec07-158">Metni gerektiği gibi çağırmak veya görüntü ya da bağlantı eklemek için biçimlendirme düğmelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="cec07-158">Use the formatting buttons to call out text as you require, or to add images or links.</span></span>
3. <span data-ttu-id="cec07-159">İşinizi kaydetmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="cec07-159">Select **Save** to save your work.</span></span>

## <a name="add-or-edit-activities"></a><span data-ttu-id="cec07-160">Faaliyet ekle veya düzenle</span><span class="sxs-lookup"><span data-stu-id="cec07-160">Add or edit activities</span></span>

1. <span data-ttu-id="cec07-161">**Aktiviteler** sekmesinde, maddeleri sağdan düzenleme alanına sürükleyin.</span><span class="sxs-lookup"><span data-stu-id="cec07-161">On the **Activities** tab, drag items from the right to the editing area.</span></span>
2. <span data-ttu-id="cec07-162">Kılavuzunuz ile bölümler arasında düzenleme yapmak için, **Yeni bölüm** öğesini düzenleme alanına sürükleyin ve bölüm için bir ad ve isteğe bağlı açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="cec07-162">To organize your guide into sections, drag the **New section** item to the editing area, and enter a name and an optional description for the section.</span></span>

    ![[İşe alma kılavuzuna veya şablona yeni bölüm ekleme] (./media/onboard-edit-add-section.png)](./media/onboard-edit-add-section.png)

3. <span data-ttu-id="cec07-164">Yeni işe alma yaptığınız aktiviteleri tamamlamak için, **yeni aktivite** öğesini düzenleme alanına sürükleyin ve etkinliğin adını ve açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="cec07-164">To add activities for your new hire to complete, drag the **New activity** item to the editing area, and enter a name and description for the activity.</span></span>

    ![[Ekleme kılavuzuna veya şablona yeni faaliyet ekleme] (./media/onboard-edit-add-activity.png)](./media/onboard-edit-add-activity.png)

4. <span data-ttu-id="cec07-166">İşe alım kılavuzuna zengin içerik ekleyin:</span><span class="sxs-lookup"><span data-stu-id="cec07-166">Add rich content to your onboarding guide:</span></span>

    - <span data-ttu-id="cec07-167">YouTube videosu eklemek için, **YouTube** öğesini düzenleme alanına sürükleyin, etkinliğin adını ve açıklamasını girin ve YouTube videonun URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="cec07-167">To add a YouTube video, drag the **YouTube** item to the editing area, enter a name and description for the activity, and enter the URL for the YouTube video.</span></span>
    - <span data-ttu-id="cec07-168">Sway sunusu veya haber bülteni eklemek için, **Sway** öğesini düzenleme alanına sürükleyin, etkinliğin adını ve açıklamasını girin ve Sway sunusu veya Bülteninizin katıştırılmış URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="cec07-168">To add a Sway presentation or newsletter, drag the **Sway** item to the editing area, enter a name and description for the activity, and enter the embedded URL for the Sway presentation or newsletter.</span></span>
    - <span data-ttu-id="cec07-169">Bir PowerApps uygulaması eklemek için **PowerApps** öğesini düzenleme alanına sürükleyin, etkinliğin adını ve açıklamasını girin ve PowerApps uygulamasını seçin veya PowerApps uygulama kimliğini girin.</span><span class="sxs-lookup"><span data-stu-id="cec07-169">To add a PowerApps app, drag the **PowerApps** item to the editing area, enter a name and description for the activity, and either select the PowerApps app or enter the PowerApps app ID.</span></span>
    - <span data-ttu-id="cec07-170">Microsoft Stream videosu eklemek için, **Microsoft Stream** öğesini düzenleme alanına sürükleyin, etkinliğin adını ve açıklamasını girin ve Microsoft Stream videonun URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="cec07-170">To add a Microsoft Stream video, drag the **Microsoft Stream** item to the editing area, enter a name and description for the activity, and enter the URL for the Microsoft Stream video.</span></span>
    - <span data-ttu-id="cec07-171">Microsoft Forms formu eklemek için, **Microsoft Forms** öğesini düzenleme alanına sürükleyin, aktivitenin adını ve açıklamasını girin, Microsoft Forms form için URL'yi girin ve ekran alanının boyutunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="cec07-171">To add a Microsoft Forms form, drag the **Microsoft Forms** item to the editing area, enter a name and description for the activity, enter the URL for the Microsoft Forms form, and specify the size of the screen area.</span></span>
    - <span data-ttu-id="cec07-172">Web içeriği barındıran iframe eklemek için, **Web İçeriği (iframe)** öğesini düzenleme alanına sürükleyin, aktivitenin adını ve açıklamasını girin, web içeriği için URL'yi girin ve ekran alanının boyutunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="cec07-172">To add an iframe that contains web content, drag the **Web Content (iframe)** item to the editing area, enter a name and description for the activity, enter the URL for the web content, and specify the size of the screen area.</span></span>

    ![[Ekleme kılavuzuna veya şablona zengin içerik ekleme] (./media/onboard-edit-add-rich-content.png)](./media/onboard-edit-add-rich-content.png)

2. <span data-ttu-id="cec07-174">İsteğe bağlı: Her faaliyetin sağındaki alanda, aktiviteyi belirli bir kişiye veya role atayın, bir son tarih ve ilgili kişi ekleyin ve bir kategori rengi atayın.</span><span class="sxs-lookup"><span data-stu-id="cec07-174">Optional: In the area on the right of each activity, assign the activity to a specific person or role, add a due date and contact person, and assign a category color.</span></span> <span data-ttu-id="cec07-175">Bir kişiye veya role faaliyet atadığınızda, her birey için bir görev oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="cec07-175">When you assign an activity to a person or role, a task is created for each individual.</span></span> <span data-ttu-id="cec07-176">Bu görev, Onboard'da **Görevler** menüsünde görünür.</span><span class="sxs-lookup"><span data-stu-id="cec07-176">This task appears on the **Tasks** menu in Onboard.</span></span>

    <span data-ttu-id="cec07-177">[![Ekleme kılavuzunda veya şablonunda faaliyet atama](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span><span class="sxs-lookup"><span data-stu-id="cec07-177">[![Assigning an activity in an onboarding guide or template](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span></span>

3. <span data-ttu-id="cec07-178">İşinizi kaydetmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="cec07-178">Select **Save** to save your work.</span></span>

<span data-ttu-id="cec07-179">Bir aktivite veya bölümü silmek için, etkinliğin veya bölümün sağ üst köşesindeki **Sil** düğmesini (çöp tenekesi simgesi) seçin.</span><span class="sxs-lookup"><span data-stu-id="cec07-179">To delete an activity or section, select the **Delete** button (the trash can symbol) in the upper-right corner of the activity or section.</span></span>

<span data-ttu-id="cec07-180">Aktiviteleri ve bölümleri yeniden düzenlemek için, onları yeni bir konuma sürükleyin.</span><span class="sxs-lookup"><span data-stu-id="cec07-180">To rearrange activities and sections, drag them to a new location.</span></span>

## <a name="add-or-edit-contacts"></a><span data-ttu-id="cec07-181">Kişi ekle veya düzenle</span><span class="sxs-lookup"><span data-stu-id="cec07-181">Add or edit contacts</span></span>

<span data-ttu-id="cec07-182">Yeni işe alma sisteminizin ilk gününden başarılı olmasını sağlamaya yardımcı olabilecek kişileri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cec07-182">You can add contact people who can help your new hire succeed from day one.</span></span> <span data-ttu-id="cec07-183">Bu kişiler; işe alanlar, ekip üyeleri, işe alma ekibi, akıl hocaları, yöneticiler ve BT destek personeli olabilir.</span><span class="sxs-lookup"><span data-stu-id="cec07-183">These contacts can be recruiters, teammates, onboarding buddies, mentors, admins, and IT support staff.</span></span>

1. <span data-ttu-id="cec07-184">**Kişiler** sekmesinde, **Yeni kişi**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="cec07-184">On the **Contacts** tab, select **New contact**.</span></span>
2. <span data-ttu-id="cec07-185">**Takım üyesi ekle** iletişim kutusunda ilgili kişinin adını veya e-posta adresini girin, ilgili kişinin yeni işe alma konusunda nasıl yardımcı olduğunu açıklayan kısa bir açıklama girin ve sonra **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="cec07-185">In the **Add team member** dialog box, enter the contact person's name or email address, enter a short description that explains how the contact person can help the new hire, and then select **Add**.</span></span> 

    ![[Ekleme kılavuzuna veya şablona kişiler ekleme] (./media/onboard-edit-add-contact.png)](./media/onboard-edit-add-contact.png)

    <span data-ttu-id="cec07-187">Alternatif olarak, **Öneriler** altında bir veya daha fazla ilgili kişi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cec07-187">Alternately, you can select one or more contacts under **Suggestions**.</span></span>

3. <span data-ttu-id="cec07-188">İşinizi kaydetmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="cec07-188">Select **Save** to save your work.</span></span>

<span data-ttu-id="cec07-189">Bir ilgili kişiyi silmek için, ilgili kişinin sağındaki **Sil** düğmesini (çöp tenekesi simgesi) seçin.</span><span class="sxs-lookup"><span data-stu-id="cec07-189">To delete a contact, select the **Delete** button (the trash can symbol) to the right of the contact.</span></span>

<span data-ttu-id="cec07-190">Bir kişiyi düzenlemek için, ilgili kişinin sağındaki **Düzenle** düğmesini (kalem simgesi) seçin.</span><span class="sxs-lookup"><span data-stu-id="cec07-190">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the contact.</span></span>

## <a name="add-or-edit-resources"></a><span data-ttu-id="cec07-191">Kaynaklar ekle veya düzenle</span><span class="sxs-lookup"><span data-stu-id="cec07-191">Add or edit resources</span></span>

<span data-ttu-id="cec07-192">İşe alım kılavuzunun **Kaynaklar** bölümüne yararlı dosyalar, haritalar ve bağlantılar ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cec07-192">You can add useful files, maps, and links to the **Resources** section of your onboarding guide.</span></span>

1. <span data-ttu-id="cec07-193">**Kaynaklar** sekmesinde, **Yeni kaynak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cec07-193">On the **Resources** tab, select **New resource**.</span></span>
2. <span data-ttu-id="cec07-194">Şu adımlardan birini izleyin:</span><span class="sxs-lookup"><span data-stu-id="cec07-194">Follow one of these steps:</span></span>

    - <span data-ttu-id="cec07-195">Bir dosya eklemek için **Dosya** sekmesini seçin ve dosyayı belirtilen alana sürükleyin.</span><span class="sxs-lookup"><span data-stu-id="cec07-195">To add a file, select the **File** tab, and drag the file into the designated area.</span></span> <span data-ttu-id="cec07-196">(Alternatif olarak, bu alanda herhangi bir yeri tıklatarak dosyayı bilgisayarınızda bulun veya **OneDrive'a Gözat**'ı seçin.) Dosya için bir ad girin ve **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="cec07-196">(Alternatively, click anywhere in that area to browse for the file on your computer, or select **Browse OneDrive**.) Enter a name for the file, and then select **Add**.</span></span>
    - <span data-ttu-id="cec07-197">Bağlantı eklemek için **Bağlantı** sekmesini seçin, bağlantı için bir ad ve adres girin ve sonra **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="cec07-197">To add a link, select the **Link** tab, enter a name and address for the link, and then select **Add**.</span></span>
    - <span data-ttu-id="cec07-198">Harita eklemek için **Harita** sekmesini seçin, harita için bir ad ve adres girin ve sonra **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="cec07-198">To add a map, select the **Map** tab, enter a name and address for the map, and then select **Add**.</span></span> <span data-ttu-id="cec07-199">Onboard, belirttiğiniz adresin bir haritasını içerecektir.</span><span class="sxs-lookup"><span data-stu-id="cec07-199">Onboard will include a map of the address that you specify.</span></span>

    ![[Ekleme kılavuzuna veya şablona kaynak ekleme] (./media/onboard-edit-add-resource.png)](./media/onboard-edit-add-resource.png)

3. <span data-ttu-id="cec07-201">İşinizi kaydetmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="cec07-201">Select **Save** to save your work.</span></span>

<span data-ttu-id="cec07-202">Bir ilgili kaynağı silmek için, ilgili kaynağın sağındaki **Sil** düğmesini (çöp tenekesi simgesi) seçin.</span><span class="sxs-lookup"><span data-stu-id="cec07-202">To delete a resource, select the **Delete** button (the trash can symbol) to the right of the resource.</span></span>

<span data-ttu-id="cec07-203">Bir kişiyi düzenlemek için, ilgili kaynağın sağındaki **Düzenle** düğmesini (kalem simgesi) seçin.</span><span class="sxs-lookup"><span data-stu-id="cec07-203">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the resource.</span></span>

## <a name="next-steps"></a><span data-ttu-id="cec07-204">Sonraki adımlar</span><span class="sxs-lookup"><span data-stu-id="cec07-204">Next steps</span></span>

- [<span data-ttu-id="cec07-205">İçeriği diğer katkıda bulunanlarla paylaşın</span><span class="sxs-lookup"><span data-stu-id="cec07-205">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="cec07-206">Görevlerin ve işe alınan çalışanların durumunu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="cec07-206">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="cec07-207">Onboard'da işe alma ekipleri oluşturun</span><span class="sxs-lookup"><span data-stu-id="cec07-207">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="cec07-208">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="cec07-208">See also</span></span>

- [<span data-ttu-id="cec07-209">Onboard uygulamasını deneyin veya satın alın</span><span class="sxs-lookup"><span data-stu-id="cec07-209">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="cec07-210">Yenilikler</span><span class="sxs-lookup"><span data-stu-id="cec07-210">What's new</span></span>](./whats-new.md)
- [<span data-ttu-id="cec07-211">Sürüm notları</span><span class="sxs-lookup"><span data-stu-id="cec07-211">Release notes</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="cec07-212">Destek alma</span><span class="sxs-lookup"><span data-stu-id="cec07-212">Get support</span></span>](./talent-support.md)
