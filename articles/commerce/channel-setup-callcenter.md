---
title: Çağrı merkezi kanalı ayarlama
description: Bu konuda, Microsoft Dynamics 365 Commerce'te yeni bir çağrı merkezi kanalının nasıl oluşturulacağı açıklanmaktadır.
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
ms.openlocfilehash: 42448bd54c00b8642b158f422e17d2b46ee25579
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057891"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="20550-103">Çağrı merkezi kanalı ayarlama</span><span class="sxs-lookup"><span data-stu-id="20550-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="20550-104">Bu konuda, Microsoft Dynamics 365 Commerce'te yeni bir çağrı merkezi kanalının nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="20550-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="20550-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="20550-105">Overview</span></span>

<span data-ttu-id="20550-106">Dynamics 365 Commerce'te çağrı merkezi, uygulamada tanımlanabilen bir kanal türüdür.</span><span class="sxs-lookup"><span data-stu-id="20550-106">In Dynamics 365 Commerce, a call center is a type of channel that can be defined in the application.</span></span> <span data-ttu-id="20550-107">Çağrı merkezi varlıklarınız için bir kanal tanımlamak, sistemin belirli verileri ve sipariş işleme varsayılanlarını satış siparişlerine bağlamasına olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="20550-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="20550-108">Bir şirket, Commerce'te birden fazla çağrı merkezi kanalı tanımlayabilir.</span><span class="sxs-lookup"><span data-stu-id="20550-108">A company can define multiple call center channels in Commerce.</span></span> 

<span data-ttu-id="20550-109">Yeni bir çağrı merkezi kanalı oluşturmadan önce [Kanal kurulumu önkoşullarını](channels-prerequisites.md) tamamladığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="20550-109">Before you create a new call center channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="20550-110">Yeni bir çağrı merkezi kanalı oluşturma ve yapılandırma</span><span class="sxs-lookup"><span data-stu-id="20550-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="20550-111">Yeni bir çağrı merkez kanalı oluşturmak ve yapılandırmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="20550-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="20550-112">Gezinti bölmesinde **Modüller \> Kanallar \> Çağrı merkezleri \> Tüm çağrı merkezleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="20550-112">In the navigation pane, go to **Modules \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="20550-113">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="20550-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="20550-114">**Ad** alanına yeni kanal için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="20550-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="20550-115">Açılır listeden uygun **Tüzel kişiliği** seçin.</span><span class="sxs-lookup"><span data-stu-id="20550-115">Select the appropriate **Legal entity** from the drop down.</span></span>
1. <span data-ttu-id="20550-116">Açılır listeden uygun **Ambar** yerleşimini seçin.</span><span class="sxs-lookup"><span data-stu-id="20550-116">Select the appropriate **Warehouse** location from the drop down.</span></span>
1. <span data-ttu-id="20550-117">**Varsayılan müşteri** alanında, geçerli bir varsayılan müşteri girin.</span><span class="sxs-lookup"><span data-stu-id="20550-117">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="20550-118">**E-posta bildirimi profili** alanında, geçerli bir e-posta bildirimi profili girin.</span><span class="sxs-lookup"><span data-stu-id="20550-118">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="20550-119">Bir **Fiyat geçersiz kılma** bilgi kodu belirtin.</span><span class="sxs-lookup"><span data-stu-id="20550-119">Provide a **Price override** info code.</span></span> <span data-ttu-id="20550-120">Bunun için önce bir bilgi kodu oluşturmanız gerekebileceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="20550-120">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="20550-121">Bir **Tutma kodu** bilgi kodu belirtin.</span><span class="sxs-lookup"><span data-stu-id="20550-121">Provide a **Hold code** info code.</span></span> <span data-ttu-id="20550-122">Bunun için önce bir bilgi kodu oluşturmanız gerekebileceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="20550-122">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="20550-123">Bir **Kredi** bilgi kodu belirtin.</span><span class="sxs-lookup"><span data-stu-id="20550-123">Provide a **Credit** info code.</span></span> <span data-ttu-id="20550-124">Bunun için önce bir bilgi kodu oluşturmanız gerekebileceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="20550-124">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="20550-125">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="20550-125">Select **Save**.</span></span>

<span data-ttu-id="20550-126">Aşağıdaki resimde yeni bir çağrı merkezi kanalının oluşturulması gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="20550-126">The following image shows the creation of a new call center channel.</span></span>

![Yeni çağrı merkezi kanalı](media/channel-setup-callcenter-1.png)

<span data-ttu-id="20550-128">Aşağıdaki resimde örnek bir çağrı merkezi kanalı gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="20550-128">The following image shows an example call center channel.</span></span>

![Örnek çağrı merkezi kanalı](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="20550-130">Ek kanal ayarları</span><span class="sxs-lookup"><span data-stu-id="20550-130">Additional channel setup</span></span>

<span data-ttu-id="20550-131">Çağrı merkezi kanalı kurulumu için gereken ek görevler ödeme yöntemlerini ve teslimat şekillerini ayarlamayı içerir.</span><span class="sxs-lookup"><span data-stu-id="20550-131">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="20550-132">Aşağıdaki resimde, **Ayarla** sekmesindeki **Teslimat şekilleri** ve **Ödeme yöntemleri** ayarlama seçenekleri gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="20550-132">The following image shows **Modes of delivery** and **Payment methods** set up options on the **Set up** tab.</span></span>

![Ek çağrı merkezi kanal kurulumu eylemleri](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="20550-134">Ödeme yöntemlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="20550-134">Set up payment methods</span></span>

<span data-ttu-id="20550-135">Ödeme yöntemlerini ayarlamak için, bu kanalda desteklenen her ödeme türü için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="20550-135">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="20550-136">Eylem bölmesinde, **Ayarla** sekmesini ve ardından **Ödeme yöntemleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="20550-136">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="20550-137">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="20550-137">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="20550-138">Gezinti bölmesinde, istediğiniz bir ödeme yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="20550-138">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="20550-139">**Genel** bölümünde bir **İşlem adı** belirtin ve istediğiniz diğer ayarları yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="20550-139">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="20550-140">Ödeme türü için gereken ek ayarları yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="20550-140">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="20550-141">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="20550-141">On the action pane, select **Save**.</span></span>

<span data-ttu-id="20550-142">Aşağıdaki resimde bir nakit ödeme yöntemi örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="20550-142">The following image shows an example of a cash payment method.</span></span>

![Örnek ödeme yöntemleri](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="20550-144">Teslimat şekillerini ayarla</span><span class="sxs-lookup"><span data-stu-id="20550-144">Set up modes of delivery</span></span>

<span data-ttu-id="20550-145">Yapılandırılan teslimat şekillerini, **Eylem bölmesindeki** **Ayarla** sekmesinden **Teslimat şekilleri**'ni seçerek görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="20550-145">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="20550-146">Bir teslimat şekli eklemek veya değiştirmek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="20550-146">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="20550-147">Gezinti bölmesinde **Modüller \> Stok yönetimi \> Teslimat şekilleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="20550-147">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="20550-148">Eylem bölmesinde, yeni bir teslimat şekli oluşturmak için **Yeni**'yi seçin veya varolan bir şekli seçin.</span><span class="sxs-lookup"><span data-stu-id="20550-148">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="20550-149">**Perakende kanalları** bölümünde, kanalı eklemek için **Satır ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="20550-149">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="20550-150">Kanalları tek tek eklemek yerine kuruluş düğümleri kullanarak eklemek, kanal eklemeyi kolaylaştırabilir.</span><span class="sxs-lookup"><span data-stu-id="20550-150">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="20550-151">Aşağıdaki resimde bir teslimat şekli örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="20550-151">The following image shows an example of a mode of delivery.</span></span>

![Teslimat şekillerini ayarla](media/channel-setup-retail-7.png)

## <a name="additional-resources"></a><span data-ttu-id="20550-153">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="20550-153">Additional resources</span></span>

[<span data-ttu-id="20550-154">Kanal kurulum önkoşulları</span><span class="sxs-lookup"><span data-stu-id="20550-154">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="20550-155">Çağrı merkezi satış işlevi</span><span class="sxs-lookup"><span data-stu-id="20550-155">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="20550-156">Çağrı merkezi sipariş işleme seçeneklerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="20550-156">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="20550-157">Çağrı merkezi katalogları</span><span class="sxs-lookup"><span data-stu-id="20550-157">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="20550-158">Sahtekarlık uyarılarını ayarlama ve bunlarla çalışma</span><span class="sxs-lookup"><span data-stu-id="20550-158">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="20550-159">Çağrı merkezleri için süreklilik programları ayarlama</span><span class="sxs-lookup"><span data-stu-id="20550-159">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
