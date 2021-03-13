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
ms.openlocfilehash: f4ecb990cfe792e92142f922c43c71ef8494e117
ms.sourcegitcommit: da17648c296b22d517eadb2f71c7803672e5648d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031860"
---
# <a name="customize-transactional-emails-by-mode-of-delivery"></a><span data-ttu-id="9dda4-103">Teslimat şekline göre işlem tabanlı e-postaları özelleştirme</span><span class="sxs-lookup"><span data-stu-id="9dda4-103">Customize transactional emails by mode of delivery</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9dda4-104">Bu konu, Microsoft Dynamics 365 Commerce'ta belirli bildirim türleri ve teslimat modları için özel e-posta şablonları ayarlamayı açıklamaktadır .</span><span class="sxs-lookup"><span data-stu-id="9dda4-104">This topic describes how to set up custom email templates for specific notification types and modes of delivery in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="9dda4-105">İşlem e-postaları artık bildirim türü (örneğin, **sipariş oluşturuldu**, **sipariş edilen sipariş** veya **fatura kesilen sipariş**) ve teslimat modu (örneğin, fazla gece, mağaza içi teslim veya yol kenarı teslim) birleşimi için özelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="9dda4-105">Transactional emails can now be customized for a combination of a notification type (for example, **Order created**, **Order packed**, or **Order invoiced**) and a mode of delivery (for example, overnight, in-store pickup, or curbside pickup).</span></span> <span data-ttu-id="9dda4-106">Özel işlem e-postaları perakendecilerin, siparişin teslimat moduna göre tasarlanmış olan karşılama deneyimleriyle ilgili olarak müşterilerine sipariş vermalarını sağlar.</span><span class="sxs-lookup"><span data-stu-id="9dda4-106">Custom transactional emails let retailers provide their customers order with fulfillment experiences that are tailored to the order's mode of delivery.</span></span> <span data-ttu-id="9dda4-107">Örneğin, "sipariş edilen" olayı özelleştirilebilir bir yan malzeme çekme seçimi yapan müşteriler için yol kenarı teslim yönergeleri sağlar.</span><span class="sxs-lookup"><span data-stu-id="9dda4-107">For example, the "order packed" event can be customized so that it provides curbside pickup instructions for customers who choose curbside pickup.</span></span> <span data-ttu-id="9dda4-108">Alternatif olarak, siparişleri sevk edilmesini seçen müşteriler için sevkiyat taşıyıcısı ve teslimat bilgileri sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="9dda4-108">Alternatively, it can provide shipping carrier and delivery information for customers who choose to have their order shipped.</span></span>

> [!NOTE]
> <span data-ttu-id="9dda4-109">Özelleştirilmiş işlem e-postalarında işlevselliği kullanmak için, önce Commerce Headquarters'da **çalışma alanları \> Özellik Yönetimi**'ne giderek işlem e-posta şablonlarını, **teslimat moduna göre Özelleştir** seçeneğini etkinleştirmeniz gerekir .</span><span class="sxs-lookup"><span data-stu-id="9dda4-109">To use the functionality for customized transactional emails, you first must turn on the **Customize transactional email templates by mode of delivery** feature by going to **Workspaces \> Feature management** in Commerce headquarters.</span></span>

<span data-ttu-id="9dda4-110">E-postalar aşağıdaki bildirim türleri için teslimat modu ile özelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="9dda4-110">Emails can be customized by mode of delivery for the following notification types:</span></span>

- <span data-ttu-id="9dda4-111">**Sipariş iptali** – Bu e-posta bildirim türü yenidir.</span><span class="sxs-lookup"><span data-stu-id="9dda4-111">**Order cancellation** – This email notification type is new.</span></span>
- <span data-ttu-id="9dda4-112">**Sipariş oluşturuldu**</span><span class="sxs-lookup"><span data-stu-id="9dda4-112">**Order created**</span></span>
- <span data-ttu-id="9dda4-113">**Sipariş onaylandı**</span><span class="sxs-lookup"><span data-stu-id="9dda4-113">**Order confirmed**</span></span>
- <span data-ttu-id="9dda4-114">**Sipariş faturası kesildi** – Bu e-posta bildirim türü yenidir.</span><span class="sxs-lookup"><span data-stu-id="9dda4-114">**Order invoiced** – This email notification type is new.</span></span> <span data-ttu-id="9dda4-115">Sevk emri teslim modu (malzeme çekme, gerçekleştirme veya elektronik teslimat modu değil) olan herhangi bir fatura olayı için bildirim gönderecek bir **sipariş sevk** bildirim türü yerine kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9dda4-115">It can be used instead of the **Order shipped** notification type that will send a notification for any invoice event that has a shipped mode of delivery (not a pickup, carry out, or electronic mode of delivery).</span></span>
- <span data-ttu-id="9dda4-116">**Çekilen sipariş**</span><span class="sxs-lookup"><span data-stu-id="9dda4-116">**Order picked**</span></span>
- <span data-ttu-id="9dda4-117">**paketlenmiş sipariş**</span><span class="sxs-lookup"><span data-stu-id="9dda4-117">**Order packed**</span></span>
- <span data-ttu-id="9dda4-118">**Sipariş alma için hazır** – Bu bildirim türü yalnızca **Çoklu malzeme çekme dağıtım modları desteği** etkinse teslimat modu ile özelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="9dda4-118">**Order ready for pickup** – This notification type can be customized by mode of delivery only if the **Support for multiple pickup delivery modes** feature is turned on.</span></span> <span data-ttu-id="9dda4-119">Bu durumda, bu bildirim türü işlevsel olarak **sipariş edilen** bildirim türüne eşdeğerdir.</span><span class="sxs-lookup"><span data-stu-id="9dda4-119">In that case, this notification type is functionally equivalent to the **Order packed** notification type.</span></span>
- <span data-ttu-id="9dda4-120">**Ödeme yapılamadı**</span><span class="sxs-lookup"><span data-stu-id="9dda4-120">**Payment failed**</span></span>
- <span data-ttu-id="9dda4-121">**Değiştirme siparişi oluşturuldu**</span><span class="sxs-lookup"><span data-stu-id="9dda4-121">**Replacement order created**</span></span>

## <a name="configure-email-templates-for-specific-modes-of-delivery"></a><span data-ttu-id="9dda4-122">E-posta şablonlarını belirli teslimat şekilleri için konfigüre et</span><span class="sxs-lookup"><span data-stu-id="9dda4-122">Configure email templates for specific modes of delivery</span></span>

<span data-ttu-id="9dda4-123">Bu yordam için, yeni, özel e-posta şablonlarınızı oluşturmuş ve bunları **organizasyon e-posta şablonları sayfasına eklemiş olduğunuz varsayımıyla belirtilir**.</span><span class="sxs-lookup"><span data-stu-id="9dda4-123">For this procedure, the assumption is that you've already created your new, custom email templates and added them to the **Organization email templates** page.</span></span> <span data-ttu-id="9dda4-124">E-posta şablonlarının nasıl oluşturulacağı ve karşıya yükleneceği hakkında bilgi için, bkz [İşlem olayları için e-posta şablonları oluşturun](email-templates-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="9dda4-124">For information about how to create and upload email templates, see [Create email templates for transactional events](email-templates-transactions.md).</span></span>

<span data-ttu-id="9dda4-125">Commerce Headquarters 'da belirli teslimat şekilleri için e-posta şablonlarını konfigüre etmek amacıyla aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="9dda4-125">To configure email templates for specific modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="9dda4-126">**Commerce e-posta bildirim profili**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="9dda4-126">Go to **Commerce email notification profile**.</span></span>
1. <span data-ttu-id="9dda4-127">**Perakende olay bildirimi ayarları**'nda, varolan bir bildirim türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="9dda4-127">Under **Retail event notification settings**, select an existing notification type.</span></span>
1. <span data-ttu-id="9dda4-128">Bildirim türü hala seçiliyken, **Teslimat şekillerini konfigüre et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9dda4-128">While the notification type is still selected, select **Configure modes of delivery**.</span></span>
1. <span data-ttu-id="9dda4-129">**Teslimat şekilleri** iletişim kutusunda, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="9dda4-129">In the **Modes of delivery** dialog box, select **New**.</span></span>
1. <span data-ttu-id="9dda4-130">Yeni satırda **Teslimat şekli** alanında, teslimat şeklini seçin.</span><span class="sxs-lookup"><span data-stu-id="9dda4-130">In the new row, in the **Mode of delivery** field, select a mode of delivery.</span></span>
1. <span data-ttu-id="9dda4-131">**E-posta kimliği** alanında, teslimat moduyla eşlenecek e-posta şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="9dda4-131">In the **Email ID** field, select the email template to map to the mode of delivery.</span></span>
1. <span data-ttu-id="9dda4-132">**Etkin** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="9dda4-132">Select the **Active** check box.</span></span>
1. <span data-ttu-id="9dda4-133">Daha fazla teslimat şekli eklemek için 4 ile 7 arasındaki adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="9dda4-133">Repeat steps 4 through 7 to add more modes of delivery.</span></span>
1. <span data-ttu-id="9dda4-134">Tamamladıktan sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="9dda4-134">When you've finished, select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="9dda4-135">Bir satış siparişindeki satırlar arasında birden fazla teslimat modu varsa, varsayılan şablon kullanılacak.</span><span class="sxs-lookup"><span data-stu-id="9dda4-135">When more than one mode of delivery is present across lines in a sales order, the default template will be used.</span></span> <span data-ttu-id="9dda4-136">Varsayılan şablon, **Commerce e-posta bildirim profili** sayfasındaki bildirim türüyle eşlenen şablondur.</span><span class="sxs-lookup"><span data-stu-id="9dda4-136">The default template is the template that is mapped to the notification type on the **Commerce email notification profile** page.</span></span>
> - <span data-ttu-id="9dda4-137">Satış siparişinin özel bir e-posta şablonu için konfigüre edilmemiş bir teslimat modu varsa, varsayılan e-posta şablonu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9dda4-137">If a sales order has a mode of delivery that hasn't been configured for a custom email template, the default email template will be used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9dda4-138">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="9dda4-138">Additional resources</span></span>

[<span data-ttu-id="9dda4-139">Çağrı merkezi siparişleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="9dda4-139">Create call center orders</span></span>](tasks/create-call-center-orders.md)

[<span data-ttu-id="9dda4-140">Satış noktasında teslimat şeklini değiştirme</span><span class="sxs-lookup"><span data-stu-id="9dda4-140">Change mode of delivery in POS</span></span>](pos-change-delivery-mode.md)
