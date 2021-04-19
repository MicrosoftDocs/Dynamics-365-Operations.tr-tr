---
title: Perakende kanalı ayarlama
description: Bu konuda, Microsoft Dynamics 365 Commerce'te yeni bir perakende kanalı oluşturma yöntemi açıklanmıştır.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 713cbe68c151b6893519843611089941cabf0e70
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800603"
---
# <a name="set-up-a-retail-channel"></a><span data-ttu-id="fe7ca-103">Perakende kanalını ayarlama</span><span class="sxs-lookup"><span data-stu-id="fe7ca-103">Set up a retail channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fe7ca-104">Bu konuda, Microsoft Dynamics 365 Commerce'te yeni bir perakende kanalı oluşturma yöntemi açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-104">This topic describes how to create a new retail channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="fe7ca-105">Dynamics 365 Commerce birden fazla perakende kanalı destekler.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-105">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="fe7ca-106">Bu perakende kanalları çevrimiçi mağazaları, çağrı merkezlerini ve perakende mağazalarını (tuğla dibek mağazalar olarak da bilinir) içerir.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-106">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="fe7ca-107">Her perakende mağaza kanalının kendi ödeme türleri, fiyat grupları, satış noktası (POS) kasaları, gelir hesapları ve gider hesapları ve personeli olabilir.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-107">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="fe7ca-108">Bir perakende mağaza kanalı oluşturabilmeniz için tüm bu öğeleri ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-108">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="fe7ca-109">Bir perakende kanalı oluşturulmadan önce, [kanal önkoşullarını izlediğinizden](channels-prerequisites.md) emin olun.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-109">Before a retail channel is created, ensure you follow the [channel prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-retail-channel"></a><span data-ttu-id="fe7ca-110">Yeni bir perakende kanalı oluşturma ve yapılandırma</span><span class="sxs-lookup"><span data-stu-id="fe7ca-110">Create and configure a new retail channel</span></span>

1. <span data-ttu-id="fe7ca-111">Gezinti bölmesinde **Modüller \> Kanallar \> Mağazalar \> Tüm mağazalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-111">In the navigation pane, go to **Modules \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="fe7ca-112">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="fe7ca-113">**Ad** alanına yeni kanal için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-113">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="fe7ca-114">**Mağaza numarası** alanına benzersiz bir mağaza numarası girin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-114">In the **Store number** field, provide a unique store number.</span></span> <span data-ttu-id="fe7ca-115">Numara yalnızca alfasayısal karakterlerden oluşabilir ve en fazla 10 karakter olabilir.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-115">The number can be alphanumeric with a maximum of 10 characters.</span></span>
1. <span data-ttu-id="fe7ca-116">**Tüzel kişilik** açılır listesinde, uygun tüzel kişiliği girin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-116">In the **Legal entity** drop-down list, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="fe7ca-117">**Ambar** açılır listesinde, ilgili ambarı girin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-117">In the **Warehouse** drop-down list, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="fe7ca-118">**Mağaza saati dilimi** alanında, ilgili saat dilimini seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-118">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="fe7ca-119">**Satış vergisi grubu** açılır listesinde, mağaza için uygun satış vergisi grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-119">In the **Sales tax group** drop-down list, select an appropriate sales tax group for the store.</span></span>
1. <span data-ttu-id="fe7ca-120">**Para birimi** alanında uygun para birimini seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-120">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="fe7ca-121">**Müşteri adres defteri** alanında, geçerli bir adres defteri girin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-121">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="fe7ca-122">**Varsayılan müşteri** alanında, geçerli bir varsayılan müşteri girin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-122">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="fe7ca-123">**İşlevsellik profili** alanında, varsa bir işlevsellik profili seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-123">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="fe7ca-124">**E-posta bildirimi profili** alanında, geçerli bir e-posta bildirimi profili girin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-124">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="fe7ca-125">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-125">On the action pane, select **Save**.</span></span>

<span data-ttu-id="fe7ca-126">Aşağıdaki resimde yeni bir perakende kanalının oluşturulması gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-126">The following image shows the creation of a new retail channel.</span></span>

![Yeni perakende kanalı](media/channel-setup-retail-1.png)

<span data-ttu-id="fe7ca-128">Aşağıdaki resimde örnek bir perakende kanalı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-128">The following image shows an example retail channel.</span></span>

![Örnek perakende kanalı](media/channel-setup-retail-2.png)

## <a name="other-settings"></a><span data-ttu-id="fe7ca-130">Diğer ayarlar</span><span class="sxs-lookup"><span data-stu-id="fe7ca-130">Other settings</span></span>

<span data-ttu-id="fe7ca-131">Perakende mağazasının gereksinimlerine göre **Ekstre/kapanış** ve **Çeşitli** bölümlerinde ayarlanabilecek isteğe bağlı birçok başka ayar vardır.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-131">There are numerous other optional settings that can be set in the **Statement/closing** and **Miscellaneous** sections, based on the needs of the retail store.</span></span>

<span data-ttu-id="fe7ca-132">Ek olarak, **Ekran düzeni** bölümünde varsayılan ekran düzenini ayarlama hakkında bilgi için bkz. [Satış noktası (POS) için ekran düzenlerine](pos-screen-layouts.md) ve **Donanım istasyonları** bölümü hakkında kurulum bilgileri için bkz. [Retail Hardware Station'ı yapılandırma ve yükleme](retail-hardware-station-configuration-installation.md).</span><span class="sxs-lookup"><span data-stu-id="fe7ca-132">In addition, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information on setting up the default screen layout in the **Screen layout** section and [Configure and install Retail hardware station](retail-hardware-station-configuration-installation.md) for setup information about the **Hardware stations** section.</span></span>

<span data-ttu-id="fe7ca-133">Aşağıdaki resimde örnek bir perakende kanalı kurulum yapılandırması gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-133">The following image shows an example retail channel setup configuration.</span></span>

![Örnek perakende kanalı yapılandırması](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a><span data-ttu-id="fe7ca-135">Ek kanal ayarları</span><span class="sxs-lookup"><span data-stu-id="fe7ca-135">Additional channel set up</span></span>

<span data-ttu-id="fe7ca-136">Bir kanal için, **Ayarla** bölümünün altındaki **Eylem bölmesinde** bulunabilecek, kanal için ayarlanması gereken ek öğeler vardır.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-136">There are additional items that need to be set up for a channel that can be found on the **Action pane** under the **Set up** section.</span></span>

<span data-ttu-id="fe7ca-137">Çevrimiçi kanal kurulumu için gerekli ek görevler şunların ayarlanmasını içerir: Ödeme yöntemleri, kasa bildirimi, teslimat şekilleri, gelir/gider hesabı, bölümler, karşılama grubu ataması ve kasalar.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-137">Additional tasks required for online channel setup include setting up payment methods, cash declaration, modes of delivery, income/expense account, sections, the fulfillment group assignment, and safes.</span></span>

<span data-ttu-id="fe7ca-138">Aşağıdaki resimde, **Ayarla** sekmesindeki çeşitli ek perakende kanal kurulum seçenekleri gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-138">The following image shows various additional retail channel setup options on the **Set up** tab.</span></span>

![Kanalı ayarlama](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="fe7ca-140">Ödeme yöntemlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="fe7ca-140">Set up payment methods</span></span>

<span data-ttu-id="fe7ca-141">Ödeme yöntemlerini ayarlamak için, bu kanalda desteklenen her ödeme türü için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-141">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="fe7ca-142">Eylem bölmesinde, **Ayarla** sekmesini ve ardından **Ödeme yöntemleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-142">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="fe7ca-143">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-143">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="fe7ca-144">Gezinti bölmesinde, istediğiniz bir ödeme yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-144">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="fe7ca-145">**Genel** bölümünde bir **İşlem adı** belirtin ve istediğiniz diğer ayarları yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-145">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="fe7ca-146">Ödeme türü için gereken ek ayarları yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-146">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="fe7ca-147">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="fe7ca-148">Aşağıdaki resimde bir nakit ödeme yöntemi örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-148">The following image shows an example of a cash payment method.</span></span>

![Örnek ödeme yöntemleri](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a><span data-ttu-id="fe7ca-150">Kasa bildirimini ayarlama</span><span class="sxs-lookup"><span data-stu-id="fe7ca-150">Set up cash declaration</span></span>

1. <span data-ttu-id="fe7ca-151">Eylem bölmesinde, **Ayarla** sekmesini ve ardından **Kasa bildirimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-151">On the action pane, select the **Set Up** tab, and then select **Cash declaration**.</span></span>
1. <span data-ttu-id="fe7ca-152">Eylem bölmesinde, **Yeni**'yi seçin ve tüm mevcut **Bozuk para** ve **Banknot** para birimlerini oluşturun.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-152">On the action pane, select **New**, and then create all **Coin** and **Note** denominations that are applicable.</span></span>

<span data-ttu-id="fe7ca-153">Aşağıdaki resimde bir kasa bildirimi örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-153">The following image shows an example of a cash declaration.</span></span>

![Kasa bildirimlerini ayarlama](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="fe7ca-155">Teslimat şekillerini ayarla</span><span class="sxs-lookup"><span data-stu-id="fe7ca-155">Set up modes of delivery</span></span>

<span data-ttu-id="fe7ca-156">Yapılandırılan teslimat şekillerini, **Eylem bölmesindeki** **Ayarla** sekmesinden **Teslimat şekilleri**'ni seçerek görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-156">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="fe7ca-157">Bir teslimat şekli eklemek veya değiştirmek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-157">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="fe7ca-158">Gezinti bölmesinde **Modüller \> Stok yönetimi \> Teslimat şekilleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-158">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="fe7ca-159">Eylem bölmesinde, yeni bir teslimat şekli oluşturmak için **Yeni**'yi seçin veya varolan bir şekli seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-159">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="fe7ca-160">**Perakende kanalları** bölümünde, kanalı eklemek için **Satır ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-160">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="fe7ca-161">Kanalları tek tek eklemek yerine kuruluş düğümleri kullanarak eklemek, kanal eklemeyi kolaylaştırabilir.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-161">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="fe7ca-162">Aşağıdaki resimde bir teslimat şekli örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-162">The following image shows an example of a mode of delivery.</span></span>

![Teslimat şekillerini ayarla](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a><span data-ttu-id="fe7ca-164">Gelir/gider hesabını ayarlama</span><span class="sxs-lookup"><span data-stu-id="fe7ca-164">Set up income/expense account</span></span>

<span data-ttu-id="fe7ca-165">Gelir/gider hesabını ayarlamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-165">To set up income/expense account, follow these steps.</span></span>

1. <span data-ttu-id="fe7ca-166">Eylem bölmesinde, **Ayarla** sekmesini ve ardından **Gelir/Gider hesabı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-166">On the action pane, select the **Set Up** tab, and then select **Income/Expense account**.</span></span>
1. <span data-ttu-id="fe7ca-167">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-167">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="fe7ca-168">**Ad** altında bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-168">Under **Name**, enter a name.</span></span>
1. <span data-ttu-id="fe7ca-169">**Arama adı** altında bir arama adı girin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-169">Under **Search name**, enter a search name.</span></span>
1. <span data-ttu-id="fe7ca-170">**Hesap türü** altında bir hesap türü girin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-170">Under **Account type**, enter the account type.</span></span>
1. <span data-ttu-id="fe7ca-171">**İleti satırı 1**, **İleti satırı 2**, **İrsaliye metni 1** ve **İrsaliye metni 2** için metni gerektiği şekilde girin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-171">Enter text for **Message line 1**, **Message line 2**, **Slip text 1**, and **Slip text 2** as needed.</span></span>
1. <span data-ttu-id="fe7ca-172">**Deftere nakil** altında, deftere nakil bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-172">Under **Posting**, enter posting information.</span></span>
1. <span data-ttu-id="fe7ca-173">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-173">On the action pane, select **Save**.</span></span>

<span data-ttu-id="fe7ca-174">Aşağıdaki resimde bir gelir/gider hesabı örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-174">The following image shows an example of an income/expense account.</span></span>

![Gelir/gider hesaplarını ayarlama](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a><span data-ttu-id="fe7ca-176">Bölümleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="fe7ca-176">Set up sections</span></span>

<span data-ttu-id="fe7ca-177">Bölümleri ayarlamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-177">To set up sections, follow these steps.</span></span>

1. <span data-ttu-id="fe7ca-178">Eylem bölmesinde, **Ayarla** sekmesini seçin ve ardından **Bölümler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-178">On the action pane, select the **Set Up** tab and click **Sections**.</span></span>
1. <span data-ttu-id="fe7ca-179">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-179">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="fe7ca-180">**Bölüm numarası** altında bir bölüm numarası girin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-180">Under **Section number**, enter a section number.</span></span>
1. <span data-ttu-id="fe7ca-181">**Açıklama** altında bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-181">Under **Description**, enter a description.</span></span>
1. <span data-ttu-id="fe7ca-182">**Bölüm boyutu** altında bir bölüm boyutu girin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-182">Under **Section size**, enter a section size.</span></span>
1. <span data-ttu-id="fe7ca-183">Gerekirse **Genel** ve **Satış istatistikleri** için ek ayarlar yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-183">Configure additional settings for **General** and **Sales statistics** as needed.</span></span>
1. <span data-ttu-id="fe7ca-184">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-184">On the action pane, select **Save**.</span></span>

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="fe7ca-185">Karşılama grubu atamasını ayarlama</span><span class="sxs-lookup"><span data-stu-id="fe7ca-185">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="fe7ca-186">Bir karşılama grubu ataması ayarlamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-186">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="fe7ca-187">Eylem bölmesinde, **Ayarla** sekmesini ve ardından **Karşılama grubu ataması**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-187">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="fe7ca-188">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-188">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="fe7ca-189">**Karşılama grubu** açılır listesinde bir karşılama grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-189">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="fe7ca-190">**Açıklama** açılır listesinde bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-190">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="fe7ca-191">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-191">On the action pane, select **Save**</span></span>

<span data-ttu-id="fe7ca-192">Aşağıdaki resimde, bir karşılama grubu ataması kurulum örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-192">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Karşılama grubu atamalarını ayarlama](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a><span data-ttu-id="fe7ca-194">Kasaları ayarlama</span><span class="sxs-lookup"><span data-stu-id="fe7ca-194">Set up safes</span></span>

<span data-ttu-id="fe7ca-195">Kasaları ayarlamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-195">To set up safes, follow these steps.</span></span>

1. <span data-ttu-id="fe7ca-196">Eylem bölmesinde, **Ayarla** sekmesini seçin ve **Kasalar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-196">On the action pane, select the **Set Up** tab and click **Safes**.</span></span>
1. <span data-ttu-id="fe7ca-197">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-197">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="fe7ca-198">Kasa için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-198">Enter a name for the safe.</span></span>
1. <span data-ttu-id="fe7ca-199">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-199">On the action pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fe7ca-200">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="fe7ca-200">Additional resources</span></span>

[<span data-ttu-id="fe7ca-201">Kanallara genel bakış</span><span class="sxs-lookup"><span data-stu-id="fe7ca-201">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="fe7ca-202">Kanal kurulum önkoşulları</span><span class="sxs-lookup"><span data-stu-id="fe7ca-202">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="fe7ca-203">Çevrimiçi kanal ayarlama</span><span class="sxs-lookup"><span data-stu-id="fe7ca-203">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="fe7ca-204">Çağrı merkezi kanalını ayarlama</span><span class="sxs-lookup"><span data-stu-id="fe7ca-204">Set up a call center channel</span></span>](channel-setup-callcenter.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
