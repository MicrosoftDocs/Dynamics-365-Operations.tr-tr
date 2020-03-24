---
title: E-posta bildirimi profili ayarlama
description: Bu konuda, Microsoft Dynamics 365 Commerce'ta bir e-posta bildirimi profilinin nasıl oluşturulacağı açıklanmaktadır.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9e5d90eaf1815bbe54b0bea40d92a0a993a23b75
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113817"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="ac0c2-103">E-posta bildirimi profili ayarlama</span><span class="sxs-lookup"><span data-stu-id="ac0c2-103">Set up an email notification profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ac0c2-104">Bu konuda, Microsoft Dynamics 365 Commerce'ta bir e-posta bildirimi profilinin nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ac0c2-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="ac0c2-105">Overview</span></span>

<span data-ttu-id="ac0c2-106">Kanalları oluşturmadan önce, sipariş oluşturma, sipariş sevkiyat durumu ve ödeme hatası gibi çeşitli olaylar için e-posta bildirimleri gönderilebilmesini sağlamak amacıyla bir profil ayarlamanız iyi olacaktır.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-106">Before creating channels, you'll want to set up a profile to ensure that email notifications can be sent out for various events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="ac0c2-107">E-posta yapılandırma hakkında daha fazla bilgi için bkz. [E-posta yapılandırma ve gönderme](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="ac0c2-107">For additional email configuration information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="ac0c2-108">E-posta bildirimi profili oluşturma</span><span class="sxs-lookup"><span data-stu-id="ac0c2-108">Create an email notification profile</span></span>

<span data-ttu-id="ac0c2-109">E-posta bildirim profili oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="ac0c2-110">Gezinti bölmesinde **Modüller \> Retail and commerce \> Headquarters kurulumu \> Commerce E-posta bildirimi profili**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="ac0c2-111">Eylem bölmesinde **Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="ac0c2-112">**E-posta bildirimi profili** alanında, profili tanımlayacak bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="ac0c2-113">**Açıklama** alanına ilgili bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="ac0c2-114">**Etkin** anahtarını **Evet**'e çevirin.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="ac0c2-115">Bir e-posta şablonu oluştur</span><span class="sxs-lookup"><span data-stu-id="ac0c2-115">Create an email template</span></span>

<span data-ttu-id="ac0c2-116">Bir e-posta bildirimi oluşturulmadan önce, gönderen e-posta bilgilerini ve e-posta şablonunu içeren bir kuruluş e-postası şablonu oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-116">Before an email notification can be created, you must create an organization email template which contains the senders email information and the email template.</span></span>

<span data-ttu-id="ac0c2-117">Yeni bir e-posta şablonu oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-117">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="ac0c2-118">Gezinti bölmesinde **Modüller \> Retail and commerce \> Headquarters kurulumu \> Parametreler \> Kuruluş e-posta şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-118">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="ac0c2-119">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="ac0c2-120">**E-posta kodu** alanına, bu şablonu tanımaya yardımcı olacak bir kod girin.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-120">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="ac0c2-121">**Gönderenin adı** alanına, gönderenin adını girin.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-121">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="ac0c2-122">**E-posta Açıklaması** alanına, anlamlı bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-122">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="ac0c2-123">**Gönderen e-postası** alanına, gönderenin e-posta adresini girin.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-123">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="ac0c2-124">**Genel** bölümünde, gerekli olan isteğe bağlı bilgileri (örneğin e-posta önceliği) doldurun.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-124">In the **General** section, fill out any optional information needed (such as the email priority).</span></span>
1. <span data-ttu-id="ac0c2-125">**E-posta iletisi içeriği** bölümünü genişletin ve şablon içeriğini oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-125">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="ac0c2-126">Her bir içerik öğesi için, dili seçin ve e-posta konu satırını belirtin.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-126">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="ac0c2-127">E-postanın gövde metni varsa, **Gövde metni var** kutusunun işaretlendiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-127">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="ac0c2-128">Eylem bölmesinde, e-posta gövde şablonu sağlamak için **E-posta iletisi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-128">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="ac0c2-129">Aşağıdaki resimde bazı örnek e-posta şablonu ayarları gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-129">The following image shows some example email template settings.</span></span>

![E-posta şablonu ayarları](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="ac0c2-131">Bir e-posta olayı oluşturma</span><span class="sxs-lookup"><span data-stu-id="ac0c2-131">Create an email event</span></span>

<span data-ttu-id="ac0c2-132">Bir e-posta olayı oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-132">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="ac0c2-133">Gezinti bölmesinde **Modüller \> Retail and commerce \> Headquarters kurulumu \> Commerce E-posta bildirimi profili**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-133">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="ac0c2-134">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-134">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="ac0c2-135">**E-posta kodu** açılır listesinden e-posta şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-135">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="ac0c2-136">Açılır listeden uygun **E-posta bildirimi türünü** seçin.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-136">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="ac0c2-137">**Etkin** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-137">Select the **Active** check box.</span></span>
1. <span data-ttu-id="ac0c2-138">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-138">On the action pane, select **Save**.</span></span>

<span data-ttu-id="ac0c2-139">Aşağıdaki resimde bazı örnek olay bildirimi ayarları gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-139">The following image shows some example event notification settings.</span></span>

![Olay bildirim ayarları](media/email-notification-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="ac0c2-141">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ac0c2-141">Additional resources</span></span>

[<span data-ttu-id="ac0c2-142">E-posta yapılandırma ve gönderme</span><span class="sxs-lookup"><span data-stu-id="ac0c2-142">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="ac0c2-143">Kanallara genel bakış</span><span class="sxs-lookup"><span data-stu-id="ac0c2-143">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="ac0c2-144">Kanal kurulum önkoşulları</span><span class="sxs-lookup"><span data-stu-id="ac0c2-144">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="ac0c2-145">Kuruluşlar ve kuruluş hiyerarşilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="ac0c2-145">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
