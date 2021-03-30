---
title: Teslimat şekline göre işlem tabanlı e-postaları özelleştirme
description: Bu konu, Microsoft Dynamics 365 Commerce'ta belirli bildirim türleri ve teslimat modları için özel e-posta şablonları ayarlamayı açıklamaktadır .
author: stuharg
manager: annbe
ms.date: 11/16/2020
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
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: d0d96ddb20b2b09751d8c0c0bf8af713de35279a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222645"
---
# <a name="customize-transactional-emails-by-mode-of-delivery"></a><span data-ttu-id="6a6f7-103">Teslimat şekline göre işlem tabanlı e-postaları özelleştirme</span><span class="sxs-lookup"><span data-stu-id="6a6f7-103">Customize transactional emails by mode of delivery</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6a6f7-104">Bu konu, Microsoft Dynamics 365 Commerce'ta belirli bildirim türleri ve teslimat modları için özel e-posta şablonları ayarlamayı açıklamaktadır .</span><span class="sxs-lookup"><span data-stu-id="6a6f7-104">This topic describes how to set up custom email templates for specific notification types and modes of delivery in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6a6f7-105">İşlem e-postaları artık bildirim türü (örneğin, **sipariş oluşturuldu**, **sipariş edilen sipariş** veya **fatura kesilen sipariş**) ve teslimat modu (örneğin, fazla gece, mağaza içi teslim veya yol kenarı teslim) birleşimi için özelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="6a6f7-105">Transactional emails can now be customized for a combination of a notification type (for example, **Order created**, **Order packed**, or **Order invoiced**) and a mode of delivery (for example, overnight, in-store pickup, or curbside pickup).</span></span> <span data-ttu-id="6a6f7-106">Özel işlem e-postaları perakendecilerin, siparişin teslimat moduna göre tasarlanmış olan karşılama deneyimleriyle ilgili olarak müşterilerine sipariş vermalarını sağlar.</span><span class="sxs-lookup"><span data-stu-id="6a6f7-106">Custom transactional emails let retailers provide their customers order with fulfillment experiences that are tailored to the order's mode of delivery.</span></span> <span data-ttu-id="6a6f7-107">Örneğin, "sipariş edilen" olayı özelleştirilebilir bir yan malzeme çekme seçimi yapan müşteriler için yol kenarı teslim yönergeleri sağlar.</span><span class="sxs-lookup"><span data-stu-id="6a6f7-107">For example, the "order packed" event can be customized so that it provides curbside pickup instructions for customers who choose curbside pickup.</span></span> <span data-ttu-id="6a6f7-108">Alternatif olarak, siparişleri sevk edilmesini seçen müşteriler için sevkiyat taşıyıcısı ve teslimat bilgileri sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="6a6f7-108">Alternatively, it can provide shipping carrier and delivery information for customers who choose to have their order shipped.</span></span>

> [!NOTE]
> <span data-ttu-id="6a6f7-109">Özelleştirilmiş işlem e-postalarında işlevselliği kullanmak için, önce Commerce Headquarters'da **çalışma alanları \> Özellik Yönetimi**'ne giderek işlem e-posta şablonlarını, **teslimat moduna göre Özelleştir** seçeneğini etkinleştirmeniz gerekir .</span><span class="sxs-lookup"><span data-stu-id="6a6f7-109">To use the functionality for customized transactional emails, you first must turn on the **Customize transactional email templates by mode of delivery** feature by going to **Workspaces \> Feature management** in Commerce headquarters.</span></span>

<span data-ttu-id="6a6f7-110">E-postalar aşağıdaki bildirim türleri için teslimat modu ile özelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="6a6f7-110">Emails can be customized by mode of delivery for the following notification types:</span></span>

- <span data-ttu-id="6a6f7-111">**Sipariş iptali** – Bu e-posta bildirim türü yenidir.</span><span class="sxs-lookup"><span data-stu-id="6a6f7-111">**Order cancellation** – This email notification type is new.</span></span>
- <span data-ttu-id="6a6f7-112">**Sipariş oluşturuldu**</span><span class="sxs-lookup"><span data-stu-id="6a6f7-112">**Order created**</span></span>
- <span data-ttu-id="6a6f7-113">**Sipariş onaylandı**</span><span class="sxs-lookup"><span data-stu-id="6a6f7-113">**Order confirmed**</span></span>
- <span data-ttu-id="6a6f7-114">**Sipariş faturası kesildi** – Bu e-posta bildirim türü yenidir.</span><span class="sxs-lookup"><span data-stu-id="6a6f7-114">**Order invoiced** – This email notification type is new.</span></span> <span data-ttu-id="6a6f7-115">Sevk emri teslim modu (malzeme çekme, gerçekleştirme veya elektronik teslimat modu değil) olan herhangi bir fatura olayı için bildirim gönderecek bir **sipariş sevk** bildirim türü yerine kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6a6f7-115">It can be used instead of the **Order shipped** notification type that will send a notification for any invoice event that has a shipped mode of delivery (not a pickup, carry out, or electronic mode of delivery).</span></span>
- <span data-ttu-id="6a6f7-116">**Çekilen sipariş**</span><span class="sxs-lookup"><span data-stu-id="6a6f7-116">**Order picked**</span></span>
- <span data-ttu-id="6a6f7-117">**paketlenmiş sipariş**</span><span class="sxs-lookup"><span data-stu-id="6a6f7-117">**Order packed**</span></span>
- <span data-ttu-id="6a6f7-118">**Sipariş alma için hazır** – Bu bildirim türü yalnızca **Çoklu malzeme çekme dağıtım modları desteği** etkinse teslimat modu ile özelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="6a6f7-118">**Order ready for pickup** – This notification type can be customized by mode of delivery only if the **Support for multiple pickup delivery modes** feature is turned on.</span></span> <span data-ttu-id="6a6f7-119">Bu durumda, bu bildirim türü işlevsel olarak **sipariş edilen** bildirim türüne eşdeğerdir.</span><span class="sxs-lookup"><span data-stu-id="6a6f7-119">In that case, this notification type is functionally equivalent to the **Order packed** notification type.</span></span>
- <span data-ttu-id="6a6f7-120">**Ödeme yapılamadı**</span><span class="sxs-lookup"><span data-stu-id="6a6f7-120">**Payment failed**</span></span>
- <span data-ttu-id="6a6f7-121">**Değiştirme siparişi oluşturuldu**</span><span class="sxs-lookup"><span data-stu-id="6a6f7-121">**Replacement order created**</span></span>

## <a name="configure-email-templates-for-specific-modes-of-delivery"></a><span data-ttu-id="6a6f7-122">E-posta şablonlarını belirli teslimat şekilleri için konfigüre et</span><span class="sxs-lookup"><span data-stu-id="6a6f7-122">Configure email templates for specific modes of delivery</span></span>

<span data-ttu-id="6a6f7-123">Bu yordam için, yeni, özel e-posta şablonlarınızı oluşturmuş ve bunları **organizasyon e-posta şablonları sayfasına eklemiş olduğunuz varsayımıyla belirtilir**.</span><span class="sxs-lookup"><span data-stu-id="6a6f7-123">For this procedure, the assumption is that you've already created your new, custom email templates and added them to the **Organization email templates** page.</span></span> <span data-ttu-id="6a6f7-124">E-posta şablonlarının nasıl oluşturulacağı ve karşıya yükleneceği hakkında bilgi için, bkz [İşlem olayları için e-posta şablonları oluşturun](email-templates-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="6a6f7-124">For information about how to create and upload email templates, see [Create email templates for transactional events](email-templates-transactions.md).</span></span>

<span data-ttu-id="6a6f7-125">Commerce Headquarters 'da belirli teslimat şekilleri için e-posta şablonlarını konfigüre etmek amacıyla aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6a6f7-125">To configure email templates for specific modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="6a6f7-126">**Commerce e-posta bildirim profili**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="6a6f7-126">Go to **Commerce email notification profile**.</span></span>
1. <span data-ttu-id="6a6f7-127">**Perakende olay bildirimi ayarları**'nda, varolan bir bildirim türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6f7-127">Under **Retail event notification settings**, select an existing notification type.</span></span>
1. <span data-ttu-id="6a6f7-128">Bildirim türü hala seçiliyken, **Teslimat şekillerini konfigüre et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6f7-128">While the notification type is still selected, select **Configure modes of delivery**.</span></span>
1. <span data-ttu-id="6a6f7-129">**Teslimat şekilleri** iletişim kutusunda, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6f7-129">In the **Modes of delivery** dialog box, select **New**.</span></span>
1. <span data-ttu-id="6a6f7-130">Yeni satırda **Teslimat şekli** alanında, teslimat şeklini seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6f7-130">In the new row, in the **Mode of delivery** field, select a mode of delivery.</span></span>
1. <span data-ttu-id="6a6f7-131">**E-posta kimliği** alanında, teslimat moduyla eşlenecek e-posta şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6f7-131">In the **Email ID** field, select the email template to map to the mode of delivery.</span></span>
1. <span data-ttu-id="6a6f7-132">**Etkin** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="6a6f7-132">Select the **Active** check box.</span></span>
1. <span data-ttu-id="6a6f7-133">Daha fazla teslimat şekli eklemek için 4 ile 7 arasındaki adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="6a6f7-133">Repeat steps 4 through 7 to add more modes of delivery.</span></span>
1. <span data-ttu-id="6a6f7-134">Tamamladıktan sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6f7-134">When you've finished, select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="6a6f7-135">Bir satış siparişindeki satırlar arasında birden fazla teslimat modu varsa, varsayılan şablon kullanılacak.</span><span class="sxs-lookup"><span data-stu-id="6a6f7-135">When more than one mode of delivery is present across lines in a sales order, the default template will be used.</span></span> <span data-ttu-id="6a6f7-136">Varsayılan şablon, **Commerce e-posta bildirim profili** sayfasındaki bildirim türüyle eşlenen şablondur.</span><span class="sxs-lookup"><span data-stu-id="6a6f7-136">The default template is the template that is mapped to the notification type on the **Commerce email notification profile** page.</span></span>
> - <span data-ttu-id="6a6f7-137">Satış siparişinin özel bir e-posta şablonu için konfigüre edilmemiş bir teslimat modu varsa, varsayılan e-posta şablonu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6a6f7-137">If a sales order has a mode of delivery that hasn't been configured for a custom email template, the default email template will be used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6a6f7-138">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="6a6f7-138">Additional resources</span></span>

[<span data-ttu-id="6a6f7-139">Çağrı merkezi siparişleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="6a6f7-139">Create call center orders</span></span>](tasks/create-call-center-orders.md)

[<span data-ttu-id="6a6f7-140">Satış noktasında teslimat şeklini değiştirme</span><span class="sxs-lookup"><span data-stu-id="6a6f7-140">Change mode of delivery in POS</span></span>](pos-change-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]