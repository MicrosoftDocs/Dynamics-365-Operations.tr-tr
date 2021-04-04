---
title: E-posta bildirimi profili ayarlama
description: Bu konuda, Microsoft Dynamics 365 Commerce'ta bir e-posta bildirimi profilinin nasıl oluşturulacağı açıklanmaktadır.
author: bicyclingfool
manager: annbe
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: d82a1abe68ff6e162acb75c6fdc1e207af11c279
ms.sourcegitcommit: 88babb2fffe97e93bbde543633fc492120f2a4fc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/06/2021
ms.locfileid: "5555319"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="fa0d7-103">E-posta bildirimi profili ayarlama</span><span class="sxs-lookup"><span data-stu-id="fa0d7-103">Set up an email notification profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fa0d7-104">Bu konuda, Microsoft Dynamics 365 Commerce'ta bir e-posta bildirimi profilinin nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="fa0d7-105">Kanalları oluştururken, bir e-posta bildirim profili ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-105">When you create channels, you can set up an email notification profile.</span></span> <span data-ttu-id="fa0d7-106">Bu şekilde, sipariş oluşturma, sipariş Sevkiyat durumu ve ödeme hatası gibi çeşitli işlem olayları için müşterilere e-postalar gönderilebilir.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-106">In that way, emails can be sent to customers for various transactional events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="fa0d7-107">E-posta yapılandırma hakkında daha fazla bilgi için bkz. [E-posta yapılandırma ve gönderme](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="fa0d7-107">For additional email configuration information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="fa0d7-108">E-posta bildirimi profili oluşturma</span><span class="sxs-lookup"><span data-stu-id="fa0d7-108">Create an email notification profile</span></span>

<span data-ttu-id="fa0d7-109">E-posta bildirim profili oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="fa0d7-110">Gezinti bölmesinde **Modüller \> Retail and commerce \> Headquarters kurulumu \> Commerce E-posta bildirimi profili**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="fa0d7-111">Eylem bölmesinde **Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="fa0d7-112">**E-posta bildirimi profili** alanında, profili tanımlayacak bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="fa0d7-113">**Açıklama** alanına ilgili bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="fa0d7-114">**Etkin** anahtarını **Evet**'e çevirin.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="fa0d7-115">Bir e-posta şablonu oluştur</span><span class="sxs-lookup"><span data-stu-id="fa0d7-115">Create an email template</span></span>

<span data-ttu-id="fa0d7-116">Bir e-posta bildirim türünü etkinleştirmeden önce, Commerce genel merkezinde bir kuruluş e-posta şablonu oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-116">Before an email notification type can be enabled, you must create an organization email template in Commerce headquarters.</span></span> <span data-ttu-id="fa0d7-117">Bu şablon, desteklemek istediğiniz her bir dil için e-posta konusu, gönderen, varsayılan dil ve e-posta gövdesini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-117">This template defines the email subject, sender, default language, and email body for each language that you want to support.</span></span>

<span data-ttu-id="fa0d7-118">Yeni bir e-posta şablonu oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-118">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="fa0d7-119">Gezinti bölmesinde **Modüller \> Retail and commerce \> Headquarters kurulumu \> Parametreler \> Kuruluş e-posta şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-119">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="fa0d7-120">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-120">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="fa0d7-121">**E-posta kodu** alanına, bu şablonu tanımaya yardımcı olacak bir kod girin.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-121">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="fa0d7-122">**Gönderenin adı** alanına, gönderenin adını girin.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-122">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="fa0d7-123">**E-posta Açıklaması** alanına, anlamlı bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-123">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="fa0d7-124">**Gönderen e-postası** alanına, gönderenin e-posta adresini girin.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-124">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="fa0d7-125">**Genel** bölümünde, e-posta şablonu için varsayılan dili seçin.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-125">In the **General** section, select a default language for the email template.</span></span> <span data-ttu-id="fa0d7-126">Belirtilen dil için yerelleştirilmiş şablon yoksa, varsayılan dil kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-126">The default language will be used when no localized template exists for the specified language.</span></span>
1. <span data-ttu-id="fa0d7-127">**E-posta iletisi içeriği** bölümünü genişletin ve şablon içeriğini oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-127">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="fa0d7-128">Her bir içerik öğesi için, dili seçin ve e-posta konu satırını belirtin.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-128">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="fa0d7-129">E-postanın gövde metni varsa, **Gövde metni var** kutusunun işaretlendiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-129">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="fa0d7-130">Eylem bölmesinde, e-posta gövde şablonu sağlamak için **E-posta iletisi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-130">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="fa0d7-131">Aşağıdaki resimde bazı örnek e-posta şablonu ayarları gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-131">The following image shows some example email template settings.</span></span>

![E-posta şablonu ayarları](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="fa0d7-133">Bir e-posta olayı oluşturma</span><span class="sxs-lookup"><span data-stu-id="fa0d7-133">Create an email event</span></span>

<span data-ttu-id="fa0d7-134">Bir e-posta olayı oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-134">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="fa0d7-135">Gezinti bölmesinde **Modüller \> Retail and commerce \> Headquarters kurulumu \> Commerce E-posta bildirimi profili**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-135">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="fa0d7-136">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-136">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="fa0d7-137">**E-posta kodu** açılır listesinden e-posta şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-137">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="fa0d7-138">Açılır listeden uygun **E-posta bildirimi türünü** seçin.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-138">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="fa0d7-139">**Etkin** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-139">Select the **Active** check box.</span></span>
1. <span data-ttu-id="fa0d7-140">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-140">On the action pane, select **Save**.</span></span>

<span data-ttu-id="fa0d7-141">Aşağıdaki resimde bazı örnek olay bildirimi ayarları gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-141">The following image shows some example event notification settings.</span></span>

![Olay bildirim ayarları](media/email-notification-profile.png)

### <a name="next-steps"></a><span data-ttu-id="fa0d7-143">Sonraki adımlar</span><span class="sxs-lookup"><span data-stu-id="fa0d7-143">Next steps</span></span>

<span data-ttu-id="fa0d7-144">Posta gönderebilmek için önce giden posta hizmetinizi yapılandırmanız ve bir toplu iş ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-144">Before you can send mails, you must configure your outgoing mail service and set up a batch job.</span></span> <span data-ttu-id="fa0d7-145">Daha fazla bilgi için bkz. [E-posta yapılandırma ve gönderme](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="fa0d7-145">For more information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="fa0d7-146">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="fa0d7-146">Additional resources</span></span>

[<span data-ttu-id="fa0d7-147">E-posta yapılandırma ve gönderme</span><span class="sxs-lookup"><span data-stu-id="fa0d7-147">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="fa0d7-148">Kanallara genel bakış</span><span class="sxs-lookup"><span data-stu-id="fa0d7-148">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="fa0d7-149">Kanal kurulum önkoşulları</span><span class="sxs-lookup"><span data-stu-id="fa0d7-149">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="fa0d7-150">Kuruluşlar ve kuruluş hiyerarşilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="fa0d7-150">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
