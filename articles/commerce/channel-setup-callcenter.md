---
title: Çağrı merkezi kanalı ayarlama
description: Bu konuda, Microsoft Dynamics 365 Commerce'te yeni bir çağrı merkezi kanalının nasıl oluşturulacağı açıklanmaktadır.
author: samjarawan
manager: annbe
ms.date: 03/13/2020
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
ms.openlocfilehash: 14cee020cc8aead627180343c82bf23534ae83c4
ms.sourcegitcommit: 0681a00d60c9f8cc8f7b9888b8c5ddf07279fc04
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/13/2020
ms.locfileid: "3131743"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="a2e29-103">Çağrı merkezi kanalı ayarlama</span><span class="sxs-lookup"><span data-stu-id="a2e29-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a2e29-104">Bu konuda, Microsoft Dynamics 365 Commerce'te yeni bir çağrı merkezi kanalının nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a2e29-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a2e29-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="a2e29-105">Overview</span></span>


<span data-ttu-id="a2e29-106">Dynamics 365 Commerce'te çağrı merkezi, uygulamada tanımlanabilen bir perakende kanalı türüdür.</span><span class="sxs-lookup"><span data-stu-id="a2e29-106">In Dynamics 365 Commerce, a call center is a type of retail channel that can be defined in the application.</span></span> <span data-ttu-id="a2e29-107">Çağrı merkezi varlıklarınız için bir kanal tanımlamak, sistemin belirli verileri ve sipariş işleme varsayılanlarını satış siparişlerine bağlamasına olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="a2e29-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="a2e29-108">Bir şirket Commerce'ta çok sayıda çağrı merkezi kanalı tanımlayabilmesine karşın, tek bir kullanıcının yalnızca tek bir çağrı merkezi kanalına bağlanabileceği unutulmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="a2e29-108">While a company can define multiple call center channels in Commerce, it is important to note that an individual user may only be linked to one call center channel.</span></span> 

<span data-ttu-id="a2e29-109">Yeni bir çağrı merkezi kanalı oluşturmadan önce [Kanal kurulumu önkoşullarını](channels-prerequisites.md) tamamladığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="a2e29-109">Before you create a new call center channel, ensure that you have completed the [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="a2e29-110">Yeni bir çağrı merkezi kanalı oluşturma ve yapılandırma</span><span class="sxs-lookup"><span data-stu-id="a2e29-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="a2e29-111">Yeni bir çağrı merkez kanalı oluşturmak ve yapılandırmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="a2e29-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="a2e29-112">Gezinti bölmesinde, **Retail ve Commerce \> Kanallar \> Çağrı merkezleri \> Tüm çağrı merkezleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="a2e29-112">In the navigation pane, go to **Retail and Commerce \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="a2e29-113">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a2e29-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="a2e29-114">**Ad** alanına yeni kanal için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="a2e29-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="a2e29-115">Açılır listeden uygun **Tüzel kişiliği** seçin.</span><span class="sxs-lookup"><span data-stu-id="a2e29-115">Select the appropriate **Legal entity** from the drop-down.</span></span>
1. <span data-ttu-id="a2e29-116">Açılır listeden uygun **Ambar** yerleşimini seçin.</span><span class="sxs-lookup"><span data-stu-id="a2e29-116">Select the appropriate **Warehouse** location from the drop-down.</span></span> <span data-ttu-id="a2e29-117">Müşteri veya madde düzeyinde başka varsayılanlar tanımlanmadıkça, bu yerleşim bu çağrı merkezi kanalı için oluşturulan satış siparişlerinde varsayılan olarak kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="a2e29-117">This location will be used as the default on sales orders created for this call center channel, unless other defaults have been defined at the customer or item level.</span></span>
1. <span data-ttu-id="a2e29-118">**Varsayılan müşteri** alanında, geçerli bir varsayılan müşteri girin.</span><span class="sxs-lookup"><span data-stu-id="a2e29-118">In the **Default customer** field, provide a valid default customer.</span></span> <span data-ttu-id="a2e29-119">Bu veriler, yeni müşteri kayıtları oluşturulurken varsayılanları otomatik olarak doldurma işlemine yardımcı olmak üzere kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a2e29-119">This data is used to assist in auto-populating defaults when new customer records are created.</span></span> <span data-ttu-id="a2e29-120">Çağrı merkezi siparişleri oluştururken, varsayılan müşteri için sipariş oluşturmanız önerilmez.</span><span class="sxs-lookup"><span data-stu-id="a2e29-120">When creating call center orders, it is not advisable to create orders for the default customer.</span></span>
1. <span data-ttu-id="a2e29-121">**E-posta bildirimi profili** alanında, geçerli bir e-posta bildirimi profili girin.</span><span class="sxs-lookup"><span data-stu-id="a2e29-121">In the **Email notification profile** field, provide a valid email notification profile.</span></span> <span data-ttu-id="a2e29-122">Çağrı merkezi siparişleri oluşturulup işlendiğinde, e-posta bildirim profili otomatik e-posta uyarılarını müşterilere sipariş durumları hakkında bilgi verecek şekilde tetikleyebilmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a2e29-122">As call center orders are created and processed, the email notification profile is used to trigger automated email alerts to customers with information about their order status.</span></span>
1. <span data-ttu-id="a2e29-123">Bir **Fiyat geçersiz kılma** bilgi kodu belirtin.</span><span class="sxs-lookup"><span data-stu-id="a2e29-123">Provide a **Price override** info code.</span></span> <span data-ttu-id="a2e29-124">Bunun için önce bir bilgi kodu oluşturmanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="a2e29-124">You may need to create an info code for this first.</span></span> <span data-ttu-id="a2e29-125">Bu bilgi kodu, bir çağrı merkezi siparişinde fiyat geçersiz kılma işlevi kullanılırken kullanıcıdan aralarından seçim yapması istenecek bir neden kodları kümesi sağlar.</span><span class="sxs-lookup"><span data-stu-id="a2e29-125">This info code provides the set of reason codes that the user will be prompted to choose from when using the price override functionality on a call center order.</span></span>
1. <span data-ttu-id="a2e29-126">Bir **Tutma kodu** bilgi kodu belirtin.</span><span class="sxs-lookup"><span data-stu-id="a2e29-126">Provide a **Hold code** info code.</span></span> <span data-ttu-id="a2e29-127">Bunun için önce bir bilgi kodu oluşturmanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="a2e29-127">You may need to create an info code for this first.</span></span> <span data-ttu-id="a2e29-128">Bu bilgi kodu, beklemede bir sipariş düzenlerken kullanıcıdan aralarından seçim yapması istenecek isteğe bağlı neden kodları kümesi sağlar.</span><span class="sxs-lookup"><span data-stu-id="a2e29-128">This info code provides the set of optional reason codes that the user will be prompted to choose from when placing an order on hold.</span></span>
1. <span data-ttu-id="a2e29-129">Bir **Kredi** bilgi kodu belirtin.</span><span class="sxs-lookup"><span data-stu-id="a2e29-129">Provide a **Credit** info code.</span></span> <span data-ttu-id="a2e29-130">Bunun için önce bir bilgi kodu oluşturmanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="a2e29-130">You may need to create an info code for this first.</span></span> <span data-ttu-id="a2e29-131">Bu bilgi kodu, kullanıcının müşteri hizmetleri nedenleriyle müşteriye sair para iadeleri sağlamak amacıyla çağrı merkezinin sipariş alacak işlevini kullanırken aralarından seçim yapılabileceği neden kodları kümesi sağlar.</span><span class="sxs-lookup"><span data-stu-id="a2e29-131">This info code provides the set of reason codes that the user can choose from when using the order credit functionality of call center to give misc refunds to the customer for customer service reasons.</span></span>
1. <span data-ttu-id="a2e29-132">İsteğe bağlı: **Mali boyutlar** hızlı sekmesinde mali boyutları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a2e29-132">Optional: set up financial dimensions on the **Financial dimensions** FastTab.</span></span> <span data-ttu-id="a2e29-133">Buraya girilen boyutlar, bu çağrı merkezi kanalında oluşturulan herhangi bir satış siparişinde varsayılan olarak yer alır.</span><span class="sxs-lookup"><span data-stu-id="a2e29-133">The dimensions entered here will default on any sales order created in this call center channel.</span></span>
1. <span data-ttu-id="a2e29-134">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2e29-134">Click **Save**.</span></span>

<span data-ttu-id="a2e29-135">Aşağıdaki resimde yeni bir çağrı merkezi kanalının oluşturulması gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="a2e29-135">The following image shows the creation of a new call center channel.</span></span>

![Yeni çağrı merkezi kanalı](media/channel-setup-callcenter-1.png)

<span data-ttu-id="a2e29-137">Aşağıdaki resimde örnek bir çağrı merkezi kanalı gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="a2e29-137">The following image shows an example call center channel.</span></span>

![Örnek çağrı merkezi kanalı](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="a2e29-139">Ek kanal ayarları</span><span class="sxs-lookup"><span data-stu-id="a2e29-139">Additional channel setup</span></span>

<span data-ttu-id="a2e29-140">Çağrı merkezi kanalı kurulumu için gereken ek görevler ödeme yöntemlerini ve teslimat şekillerini ayarlamayı içerir.</span><span class="sxs-lookup"><span data-stu-id="a2e29-140">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="a2e29-141">Aşağıdaki resimde, **Kurulum** sekmesindeki **Teslimat şekilleri** ve **Ödeme yöntemleri** ayarlama seçenekleri gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="a2e29-141">The following image shows **Modes of delivery** and **Payment methods** setup options on the **Set up** tab.</span></span>

![Ek çağrı merkezi kanal kurulumu eylemleri](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="a2e29-143">Ödeme yöntemlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="a2e29-143">Set up payment methods</span></span>

<span data-ttu-id="a2e29-144">Ödeme yöntemleri ayarlamak için, bu kanalda desteklenen her ödeme türü için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="a2e29-144">To set up payment methods, follow these steps for each payment type supported on this channel.</span></span> <span data-ttu-id="a2e29-145">Kullanıcıların çağrı merkezi kanalına bağlanması için önceden tanımlanmış ödeme yöntemleri arasından seçim yapması istenir.</span><span class="sxs-lookup"><span data-stu-id="a2e29-145">Users will be required to select from pre-defined payment methods to link them to the call center channel.</span></span> <span data-ttu-id="a2e29-146">Çağrı merkezi ödeme yöntemlerinizi ayarlamadan önce **Retail ve Commerce \> Kanal kurulumu \> Ödeme yöntemleri \> Ödeme yöntemleri** altında ana ödeme yöntemlerinizi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a2e29-146">Before setting up your call center payment methods, first set up your master methods of payment in **Retail and Commerce \> Channel setup \> Payment methods \> Payment methods**.</span></span>

1. <span data-ttu-id="a2e29-147">Eylem bölmesinde, **Ayarla** sekmesini ve ardından **Ödeme yöntemleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="a2e29-147">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="a2e29-148">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a2e29-148">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="a2e29-149">Gezinti bölmesinde, kullanılabilir önceden tanımlanmış ödemelerden bir ödeme yöntemi seçin.</span><span class="sxs-lookup"><span data-stu-id="a2e29-149">In the navigation pane, select a payment method from the pre-defined payments available.</span></span>
1. <span data-ttu-id="a2e29-150">Ödeme türü için gereken ek ayarları yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="a2e29-150">Configure any additional settings as required for the payment type.</span></span> <span data-ttu-id="a2e29-151">Kredi kartları, hediye kartları veya bağlılık programı kartları için **Kart kurulumu** işlevi seçilerek ek kurulum yapılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="a2e29-151">For credit cards, gift cards, or loyalty cards, additional setup is required by selecting the **Card setup** function.</span></span> 
1. <span data-ttu-id="a2e29-152">Ödeme türü için uygun deftere nakil hesaplarını **Deftere nakil** bölümünde yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="a2e29-152">Configure proper posting accounts for the payment type in the **Posting** section.</span></span>
1. <span data-ttu-id="a2e29-153">Eylem bölmesi'nde, **Kaydet** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2e29-153">On the action pane, click **Save**.</span></span>

<span data-ttu-id="a2e29-154">Aşağıdaki resimde bir nakit ödeme yöntemi örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="a2e29-154">The following image shows an example of a cash payment method.</span></span>

![Örnek ödeme yöntemleri](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="a2e29-156">Teslimat şekillerini ayarla</span><span class="sxs-lookup"><span data-stu-id="a2e29-156">Set up modes of delivery</span></span>

<span data-ttu-id="a2e29-157">Yapılandırılan teslimat şekillerini, **Eylem bölmesindeki** **Ayarla** sekmesinden **Teslimat şekilleri**'ni seçerek görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a2e29-157">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="a2e29-158">Çağrı merkezi kanalıyla ilişkilendirilecek bir teslimat modu eklemek veya değiştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="a2e29-158">To change or add a mode of delivery to be associated to the call center channel, follow these steps.</span></span>

1. <span data-ttu-id="a2e29-159">Çağrı merkezi teslimat şekilleri formunda, **Teslimat şekillerini yönet**'i seçin</span><span class="sxs-lookup"><span data-stu-id="a2e29-159">From the Call center modes of delivery form, select **Manage modes of delivery**</span></span>
1. <span data-ttu-id="a2e29-160">Eylem bölmesinde, yeni bir teslimat şekli oluşturmak için **Yeni**'yi seçin veya varolan bir şekli seçin.</span><span class="sxs-lookup"><span data-stu-id="a2e29-160">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="a2e29-161">**Perakende kanalları** bölümünde, çağrı merkezi kanalı eklemek için **Satır ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2e29-161">In the **Retail channels** section, click **Add line** to add the call center channel.</span></span> <span data-ttu-id="a2e29-162">Kanalları tek tek eklemek yerine kuruluş düğümleri kullanarak eklemek, kanal eklemeyi kolaylaştırabilir.</span><span class="sxs-lookup"><span data-stu-id="a2e29-162">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>
1. <span data-ttu-id="a2e29-163">Teslimat şeklinin **Ürünler** hızlı sekmesi ve **Adresler** hızlı sekmesindeki verilerle yapılandırıldığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="a2e29-163">Ensure the mode of delivery has been configured with data on the **Products** FastTab and the **Addresses** FastTab.</span></span> <span data-ttu-id="a2e29-164">Teslimat şekli için herhangi bir ürün veya teslimat adresi geçerli değilse, sipariş girişi sırasında bunu seçmek hatalara neden olur.</span><span class="sxs-lookup"><span data-stu-id="a2e29-164">If no products or delivery addresses are valid for the mode of delivery, choosing it during order entry will result in errors.</span></span>
1. <span data-ttu-id="a2e29-165">Çağrı merkezi teslimat şekli yapılandırmalarında herhangi bir değişiklik yapıldıktan sonra, değişiklik matrisini açmak için **Teslimat şekillerini işle** işi çalıştırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a2e29-165">After any changes have been made to the call center mode of delivery configurations, the **Process delivery modes** job must be run to explode the change matrix.</span></span> <span data-ttu-id="a2e29-166">Bu işi **Retail ve Commerce \> Retail ve Commerce BT \>Teslimar şekillerini işle**'ye giderek bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a2e29-166">This job can be found by navigating to **Retail and Commerce \> Retail and Commerce IT \> Process delivery modes**.</span></span>

<span data-ttu-id="a2e29-167">Aşağıdaki resimde bir teslimat şekli örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="a2e29-167">The following image shows an example of a mode of delivery.</span></span>

![Teslimat şekillerini ayarla](media/channel-setup-retail-7.png)

### <a name="set-up-channel-users"></a><span data-ttu-id="a2e29-169">Kanal kullanıcıları ayarlama</span><span class="sxs-lookup"><span data-stu-id="a2e29-169">Set up channel users</span></span>

<span data-ttu-id="a2e29-170">Commerce Headquarters'dan çağrı merkezi kanalına bağlanan bir satış siparişi oluşturmak için satış siparişini oluşturan kullanıcının çağrı merkezi kanalına bağlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="a2e29-170">To create a sales order that is linked to the call center channel from Commerce Headquarters, the user creating the sales order must be linked to the call center channel.</span></span> <span data-ttu-id="a2e29-171">Kullanıcı, Commerce Headquarters'da oluşturulan bir satış siparişini çağrı merkezi kanalına el ile bağlayamaz.</span><span class="sxs-lookup"><span data-stu-id="a2e29-171">The user can not manually link a sales order created in Commerce Headquarters to the call center channel.</span></span> <span data-ttu-id="a2e29-172">Bağlantı sistematik bir şekilde yapılır ve kullanıcıyı ve kullanıcının çağrı merkezi kanalıyla olan ilişkisini temel alır.</span><span class="sxs-lookup"><span data-stu-id="a2e29-172">The link is systematic, and is based on the user and the user's relationship to the call center channel.</span></span> <span data-ttu-id="a2e29-173">Bir kullanıcı yalnızca bir çağrı merkezi kanalına bağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="a2e29-173">A user may only be linked to one call center channel.</span></span>

1. <span data-ttu-id="a2e29-174">Eylem bölmesinde, **Kanal** sekmesini ve ardından **Kanal kullanıcıları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="a2e29-174">On the action pane, select the **Channel** tab, and then select **Channel users**.</span></span>
1. <span data-ttu-id="a2e29-175">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a2e29-175">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="a2e29-176">Bu kullanıcıyı çağrı merkezi kanalına bağlamak için açılır seçim listesinden mevcut bir **kullanıcı kimliği** seçin</span><span class="sxs-lookup"><span data-stu-id="a2e29-176">Choose an existing **User ID** from the dropdown selection list to link this user to the call center channel</span></span>

<span data-ttu-id="a2e29-177">Kanal kullanıcısı ayarı yapıldıktan ve kullanıcı Commerce Headquarters'da yeni bir satış siparişi oluşturduktan sonra, satış siparişi oluşturan kullanıcının ilişkili çağrı merkezi kanalına bağlanır.</span><span class="sxs-lookup"><span data-stu-id="a2e29-177">After the channel user setup is done and the user creates a new sales order in Commerce Headquarters, the sales order will be linked to their associated call center channel.</span></span> <span data-ttu-id="a2e29-178">Bu kanalla ilgili tüm yapılandırmalar sistematik olarak satış siparişine uygulanacaktır.</span><span class="sxs-lookup"><span data-stu-id="a2e29-178">Any configurations for this channel will be applied systematically to the sales order.</span></span> <span data-ttu-id="a2e29-179">Bir kullanıcı satış siparişi başlığındaki kanal adı referansını görüntüleyerek satış siparişinin hangi çağrı merkezi kanalına bağlandığını onaylayabilir.</span><span class="sxs-lookup"><span data-stu-id="a2e29-179">A user can confirm which call center channel the sales order is linked to by viewing the channel name reference on the sales order header.</span></span>


### <a name="set-up-price-groups"></a><span data-ttu-id="a2e29-180">Fiyat grupları ayarlama</span><span class="sxs-lookup"><span data-stu-id="a2e29-180">Set up price groups</span></span>

<span data-ttu-id="a2e29-181">Fiyat grupları isteğe bağlıdır, ancak kullanılması durumunda, çağrı merkezi kanalında sipariş veren müşterilere hangi satış fiyatlarının sunulacağını kontrol edilebilir.</span><span class="sxs-lookup"><span data-stu-id="a2e29-181">Price groups are optional, but if used, can control which sales prices will be offered to customers placing orders in the call center channel.</span></span> <span data-ttu-id="a2e29-182">Müşteri için bir fiyat grubu yapılandırılmamış veya katalog fiyat grupları satış siparişine uygulanmamışsa (çağrı merkezi sipariş başlığındaki **Kaynak kod kimliği** alanını kullanarak), madde fiyatlarını bulmak için kanal fiyat grubu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a2e29-182">If a price group has not been configured for the customer, or if catalog price groups are not being applied to the sales order (using the **Source code ID** field on the call center order header), then the channel price group is used to locate item prices.</span></span> <span data-ttu-id="a2e29-183">Çağrı merkezi kanalında bir fiyat grubu bulunamazsa, varsayılan madde ana fiyatları kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a2e29-183">If a price group is not found on the call center channel, the default item master prices are used.</span></span> 

<span data-ttu-id="a2e29-184">Fiyat grubu ayarlamak için aşağıdakileri yapın.</span><span class="sxs-lookup"><span data-stu-id="a2e29-184">To set up a price group, do the following.</span></span>

1. <span data-ttu-id="a2e29-185">Eylem bölmesinde, **Kanal** sekmesine ve ardından **Fiyat grupları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2e29-185">On the action pane, click the **Channel** tab, and then select **Price groups**.</span></span>
1. <span data-ttu-id="a2e29-186">Eylem bölmesinde **Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2e29-186">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="a2e29-187">Açılır seçim listesinden bir **Perakende fiyat grubu** seçin.</span><span class="sxs-lookup"><span data-stu-id="a2e29-187">Select a **Retail price group** from the dropdown selection list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a2e29-188">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="a2e29-188">Additional resources</span></span>

[<span data-ttu-id="a2e29-189">Kanal kurulum önkoşulları</span><span class="sxs-lookup"><span data-stu-id="a2e29-189">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="a2e29-190">Çağrı merkezi satış işlevi</span><span class="sxs-lookup"><span data-stu-id="a2e29-190">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="a2e29-191">Çağrı merkezi sipariş işleme seçeneklerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="a2e29-191">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="a2e29-192">Çağrı merkezi katalogları</span><span class="sxs-lookup"><span data-stu-id="a2e29-192">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="a2e29-193">Sahtekarlık uyarılarını ayarlama ve bunlarla çalışma</span><span class="sxs-lookup"><span data-stu-id="a2e29-193">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="a2e29-194">Çağrı merkezleri için süreklilik programları ayarlama</span><span class="sxs-lookup"><span data-stu-id="a2e29-194">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
