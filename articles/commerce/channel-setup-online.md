---
title: Çevrimiçi kanal ayarlama
description: Bu konuda, Microsoft Dynamics 365 Commerce'te yeni bir çevrimiçi kanalın nasıl oluşturulacağı açıklanmaktadır.
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
ms.openlocfilehash: 9b7a2b8fd157df8b39e9e227d188a3802cacb4e3
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002439"
---
# <a name="set-up-an-online-channel"></a><span data-ttu-id="c8946-103">Çevrimiçi kanal ayarlama</span><span class="sxs-lookup"><span data-stu-id="c8946-103">Set up an online channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c8946-104">Bu konuda, Microsoft Dynamics 365 Commerce'te yeni bir çevrimiçi kanalın nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="c8946-104">This topic describes how to create a new online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c8946-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="c8946-105">Overview</span></span>

<span data-ttu-id="c8946-106">Dynamics 365 Commerce birden fazla perakende kanalı destekler.</span><span class="sxs-lookup"><span data-stu-id="c8946-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="c8946-107">Bu perakende kanalları çevrimiçi mağazaları, çağrı merkezlerini ve perakende mağazalarını (tuğla dibek mağazalar olarak da bilinir) içerir.</span><span class="sxs-lookup"><span data-stu-id="c8946-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="c8946-108">Çevrimiçi mağazalar müşterilere perakendecinin perakende mağazalarının yanı sıra çevrimiçi mağazasından da ürün satın alma seçeneği verir.</span><span class="sxs-lookup"><span data-stu-id="c8946-108">Online stores give customers the option of purchasing products from the retailer's online store in addition to its retail stores.</span></span>

<span data-ttu-id="c8946-109">Commerce'te bir çevrimiçi mağaza oluşturmak için önce bir çevrimiçi kanal oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="c8946-109">To create an online store in Commerce, you must first create an online channel.</span></span> 

<span data-ttu-id="c8946-110">Yeni bir çevrimiçi kanal oluşturmadan önce [Kanal kurulumu önkoşullarını](channels-prerequisites.md) tamamladığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="c8946-110">Before you create a new online channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-online-channel"></a><span data-ttu-id="c8946-111">Yeni bir çevrimiçi kanal oluşturma ve yapılandırma</span><span class="sxs-lookup"><span data-stu-id="c8946-111">Create and configure a new online channel</span></span>

<span data-ttu-id="c8946-112">Yeni bir çevrimiçi kanal oluşturmak ve yapılandırmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c8946-112">To create and configure a new online channel, follow these steps.</span></span>

1. <span data-ttu-id="c8946-113">Gezinti bölmesinde **Modüller \> Kanallar \> Çevrimiçi Mağazalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="c8946-113">In the navigation pane, go to **Modules \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="c8946-114">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c8946-114">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="c8946-115">**Ad** alanına yeni kanal için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="c8946-115">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="c8946-116">**Tüzel kişilik** açılır listesinde, uygun tüzel kişiliği girin.</span><span class="sxs-lookup"><span data-stu-id="c8946-116">In the **Legal entity** drop-down, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="c8946-117">**Ambar** açılır listesinde, ilgili ambarı girin.</span><span class="sxs-lookup"><span data-stu-id="c8946-117">In the **Warehouse** drop-down, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="c8946-118">**Mağaza saati dilimi** alanında, ilgili saat dilimini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8946-118">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="c8946-119">**Para birimi** alanında uygun para birimini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8946-119">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="c8946-120">**Varsayılan müşteri** alanında, geçerli bir varsayılan müşteri girin.</span><span class="sxs-lookup"><span data-stu-id="c8946-120">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="c8946-121">**Müşteri adres defteri** alanında, geçerli bir adres defteri girin.</span><span class="sxs-lookup"><span data-stu-id="c8946-121">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="c8946-122">**İşlevsellik profili** alanında, varsa bir işlevsellik profili seçin.</span><span class="sxs-lookup"><span data-stu-id="c8946-122">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="c8946-123">**E-posta bildirimi profili** alanında, geçerli bir e-posta bildirimi profili girin.</span><span class="sxs-lookup"><span data-stu-id="c8946-123">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="c8946-124">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c8946-124">On the action pane, select **Save**.</span></span>

<span data-ttu-id="c8946-125">Aşağıdaki resimde yeni bir çevrimiçi kanalın oluşturulması gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="c8946-125">The following image shows the creation of a new online channel.</span></span>

![Yeni çevrimiçi kanal](media/channel-setup-online-1.png)

<span data-ttu-id="c8946-127">Aşağıdaki resimde örnek bir çevrimiçi kanal gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="c8946-127">The following image shows an example online channel.</span></span>

![Örnek çevrimiçi kanal](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a><span data-ttu-id="c8946-129">Dilleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="c8946-129">Set up languages</span></span>

<span data-ttu-id="c8946-130">E-ticaret siteniz birden çok dili destekleyecekse **Diller** bölümünü genişletin ve gereken dilleri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c8946-130">If your e-Commerce site will support multiple languages, expand the **Languages** section and add additional languages as needed.</span></span>

## <a name="set-up-payment-account"></a><span data-ttu-id="c8946-131">Ödeme hesabını ayarlama</span><span class="sxs-lookup"><span data-stu-id="c8946-131">Set up payment account</span></span>

<span data-ttu-id="c8946-132">**Ödeme hesabı** bölümünün içinden, üçüncü taraf ödeme sağlayıcı ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c8946-132">From within the **Payment account** section, you can add a third-party payment provider.</span></span> <span data-ttu-id="c8946-133">Adyen ödeme bağlayıcısı ayarlama hakkında bilgi için bkz. [Adyen için Dynamics 365 Ödeme Bağlayıcı](../retail/dev-itpro/adyen-connector.md).</span><span class="sxs-lookup"><span data-stu-id="c8946-133">For information on settting up an Adyen payment connector, see [Dynamics 365 Payment Connector for Adyen](../retail/dev-itpro/adyen-connector.md).</span></span>

## <a name="additional-channel-set-up"></a><span data-ttu-id="c8946-134">Ek kanal ayarları</span><span class="sxs-lookup"><span data-stu-id="c8946-134">Additional channel set up</span></span>

<span data-ttu-id="c8946-135">Çevrimiçi kanal kurulumu için gereken ek görevler ödeme yöntemleri, teslimat şekilleri ve karşılama grubu ataması ayarlamayı içerir.</span><span class="sxs-lookup"><span data-stu-id="c8946-135">Additional tasks required for online channel setup include setting up payment methods, modes of delivery, and the fulfillment group assignment.</span></span>

<span data-ttu-id="c8946-136">Aşağıdaki resimde, **Ayarla** sekmesindeki **Teslimat şekilleri**, **Ödeme yöntemleri** ve **Karşılama grubu ataması** ayarlama seçenekleri gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="c8946-136">The following image shows **Modes of delivery**, **Payment methods**, and **Fulfillment group assignment** setup options on the **Set up** tab.</span></span>

![Ek çevrimiçi kanal kurulumu eylemleri](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="c8946-138">Ödeme yöntemlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="c8946-138">Set up payment methods</span></span>

<span data-ttu-id="c8946-139">Ödeme yöntemlerini ayarlamak için, bu kanalda desteklenen her ödeme türü için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c8946-139">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="c8946-140">Eylem bölmesinde, **Ayarla** sekmesini ve ardından **Ödeme yöntemleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="c8946-140">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="c8946-141">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c8946-141">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="c8946-142">Gezinti bölmesinde, istediğiniz bir ödeme yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8946-142">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="c8946-143">**Genel** bölümünde bir **İşlem adı** belirtin ve istediğiniz diğer ayarları yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="c8946-143">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="c8946-144">Ödeme türü için gereken ek ayarları yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="c8946-144">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="c8946-145">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c8946-145">On the action pane, select **Save**.</span></span>

<span data-ttu-id="c8946-146">Aşağıdaki resimde bir nakit ödeme yöntemi örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="c8946-146">The following image shows an example of a cash payment method.</span></span>

![Örnek ödeme yöntemleri](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="c8946-148">Teslimat şekillerini ayarla</span><span class="sxs-lookup"><span data-stu-id="c8946-148">Set up modes of delivery</span></span>

<span data-ttu-id="c8946-149">Yapılandırılan teslimat şekillerini, **Eylem bölmesindeki** **Ayarla** sekmesinden **Teslimat şekilleri**'ni seçerek görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c8946-149">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="c8946-150">Bir teslimat şekli eklemek veya değiştirmek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c8946-150">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="c8946-151">Gezinti bölmesinde **Modüller \> Stok yönetimi \> Teslimat şekilleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="c8946-151">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="c8946-152">Eylem bölmesinde, yeni bir teslimat şekli oluşturmak için **Yeni**'yi seçin veya varolan bir şekli seçin.</span><span class="sxs-lookup"><span data-stu-id="c8946-152">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="c8946-153">**Perakende kanalları** bölümünde, kanalı eklemek için **Satır ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c8946-153">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="c8946-154">Kanalları tek tek eklemek yerine kuruluş düğümleri kullanarak eklemek, kanal eklemeyi kolaylaştırabilir.</span><span class="sxs-lookup"><span data-stu-id="c8946-154">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="c8946-155">Aşağıdaki resimde bir teslimat şekli örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="c8946-155">The following image shows an example of a mode of delivery.</span></span>

![Teslimat şekillerini ayarla](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="c8946-157">Karşılama grubu atamasını ayarlama</span><span class="sxs-lookup"><span data-stu-id="c8946-157">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="c8946-158">Bir karşılama grubu ataması ayarlamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c8946-158">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="c8946-159">Eylem bölmesinde, **Ayarla** sekmesini ve ardından **Karşılama grubu ataması**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="c8946-159">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="c8946-160">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c8946-160">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="c8946-161">**Karşılama grubu** açılır listesinde bir karşılama grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="c8946-161">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="c8946-162">**Açıklama** açılır listesinde bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="c8946-162">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="c8946-163">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c8946-163">On the action pane, select **Save**.</span></span>

<span data-ttu-id="c8946-164">Aşağıdaki resimde, bir karşılama grubu ataması kurulum örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="c8946-164">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Karşılama grubu atamasını ayarlama](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a><span data-ttu-id="c8946-166">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="c8946-166">Additional resources</span></span>

[<span data-ttu-id="c8946-167">Kanallara genel bakış</span><span class="sxs-lookup"><span data-stu-id="c8946-167">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="c8946-168">Kanal kurulum önkoşulları</span><span class="sxs-lookup"><span data-stu-id="c8946-168">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="c8946-169">Perakende kanalını ayarlama</span><span class="sxs-lookup"><span data-stu-id="c8946-169">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="c8946-170">Çağrı merkezi kanalını ayarlama</span><span class="sxs-lookup"><span data-stu-id="c8946-170">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="c8946-171">Adyen için Dynamics 365 Ödeme Bağlayıcısı</span><span class="sxs-lookup"><span data-stu-id="c8946-171">Dynamics 365 Payment Connector for Adyen</span></span>](../retail/dev-itpro/adyen-connector.md)
