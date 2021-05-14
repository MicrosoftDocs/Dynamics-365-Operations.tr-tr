---
title: Perakende kanalı ayarlama
description: Bu konuda, Microsoft Dynamics 365 Commerce'te yeni bir perakende kanalı oluşturma yöntemi açıklanmıştır.
author: samjarawan
ms.date: 04/23/2021
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
ms.openlocfilehash: 3f1f5dc2c8402d9b6b68a049f804932812eb74c0
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937546"
---
# <a name="set-up-a-retail-channel"></a><span data-ttu-id="4712f-103">Perakende kanalını ayarlama</span><span class="sxs-lookup"><span data-stu-id="4712f-103">Set up a retail channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4712f-104">Bu konuda, Microsoft Dynamics 365 Commerce'te yeni bir perakende kanalı oluşturma yöntemi açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="4712f-104">This topic describes how to create a new retail channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4712f-105">Dynamics 365 Commerce birden fazla perakende kanalı destekler.</span><span class="sxs-lookup"><span data-stu-id="4712f-105">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="4712f-106">Bu perakende kanalları çevrimiçi mağazaları, çağrı merkezlerini ve perakende mağazalarını (tuğla dibek mağazalar olarak da bilinir) içerir.</span><span class="sxs-lookup"><span data-stu-id="4712f-106">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="4712f-107">Her perakende mağaza kanalının kendi ödeme türleri, fiyat grupları, satış noktası (POS) kasaları, gelir hesapları ve gider hesapları ve personeli olabilir.</span><span class="sxs-lookup"><span data-stu-id="4712f-107">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="4712f-108">Bir perakende mağaza kanalı oluşturabilmeniz için tüm bu öğeleri ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="4712f-108">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="4712f-109">Bir perakende kanalı oluşturulmadan önce, [kanal önkoşullarını izlediğinizden](channels-prerequisites.md) emin olun.</span><span class="sxs-lookup"><span data-stu-id="4712f-109">Before a retail channel is created, ensure you follow the [channel prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-retail-channel"></a><span data-ttu-id="4712f-110">Yeni bir perakende kanalı oluşturma ve yapılandırma</span><span class="sxs-lookup"><span data-stu-id="4712f-110">Create and configure a new retail channel</span></span>

1. <span data-ttu-id="4712f-111">Gezinti bölmesinde **Modüller \> Kanallar \> Mağazalar \> Tüm mağazalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="4712f-111">In the navigation pane, go to **Modules \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="4712f-112">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4712f-112">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="4712f-113">**Ad** alanına yeni kanal için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="4712f-113">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="4712f-114">**Mağaza numarası** alanına benzersiz bir mağaza numarası girin.</span><span class="sxs-lookup"><span data-stu-id="4712f-114">In the **Store number** field, provide a unique store number.</span></span> <span data-ttu-id="4712f-115">Numara yalnızca alfasayısal karakterlerden oluşabilir ve en fazla 10 karakter olabilir.</span><span class="sxs-lookup"><span data-stu-id="4712f-115">The number can be alphanumeric with a maximum of 10 characters.</span></span>
1. <span data-ttu-id="4712f-116">**Tüzel kişilik** açılır listesinde, uygun tüzel kişiliği girin.</span><span class="sxs-lookup"><span data-stu-id="4712f-116">In the **Legal entity** drop-down list, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="4712f-117">**Ambar** açılır listesinde, ilgili ambarı girin.</span><span class="sxs-lookup"><span data-stu-id="4712f-117">In the **Warehouse** drop-down list, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="4712f-118">**Mağaza saati dilimi** alanında, ilgili saat dilimini seçin.</span><span class="sxs-lookup"><span data-stu-id="4712f-118">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="4712f-119">**Satış vergisi grubu** açılır listesinde, mağaza için uygun satış vergisi grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="4712f-119">In the **Sales tax group** drop-down list, select an appropriate sales tax group for the store.</span></span>
1. <span data-ttu-id="4712f-120">**Para birimi** alanında uygun para birimini seçin.</span><span class="sxs-lookup"><span data-stu-id="4712f-120">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="4712f-121">**Müşteri adres defteri** alanında, geçerli bir adres defteri girin.</span><span class="sxs-lookup"><span data-stu-id="4712f-121">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="4712f-122">**Varsayılan müşteri** alanında, geçerli bir varsayılan müşteri girin.</span><span class="sxs-lookup"><span data-stu-id="4712f-122">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="4712f-123">**İşlevsellik profili** alanında, varsa bir işlevsellik profili seçin.</span><span class="sxs-lookup"><span data-stu-id="4712f-123">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="4712f-124">**E-posta bildirimi profili** alanında, geçerli bir e-posta bildirimi profili girin.</span><span class="sxs-lookup"><span data-stu-id="4712f-124">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="4712f-125">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4712f-125">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="4712f-126">Aşağıdaki resimde yeni bir perakende kanalının oluşturulması gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="4712f-126">The following image shows the creation of a new retail channel.</span></span>

![Yeni perakende kanalı](media/channel-setup-retail-1.png)

<span data-ttu-id="4712f-128">Aşağıdaki resimde örnek bir perakende kanalı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="4712f-128">The following image shows an example retail channel.</span></span>

![Örnek perakende kanalı](media/channel-setup-retail-2.png)

## <a name="other-settings"></a><span data-ttu-id="4712f-130">Diğer ayarlar</span><span class="sxs-lookup"><span data-stu-id="4712f-130">Other settings</span></span>

<span data-ttu-id="4712f-131">Perakende mağazasının gereksinimlerine göre **Ekstre/kapanış** ve **Çeşitli** bölümlerinde ayarlanabilecek isteğe bağlı birçok başka ayar vardır.</span><span class="sxs-lookup"><span data-stu-id="4712f-131">There are numerous other optional settings that can be set in the **Statement/closing** and **Miscellaneous** sections, based on the needs of the retail store.</span></span>

<span data-ttu-id="4712f-132">Ek olarak, **Ekran düzeni** bölümünde varsayılan ekran düzenini ayarlama hakkında bilgi için bkz. [Satış noktası (POS) için ekran düzenlerine](pos-screen-layouts.md) ve **Donanım istasyonları** bölümü hakkında kurulum bilgileri için bkz. [Retail Hardware Station'ı yapılandırma ve yükleme](retail-hardware-station-configuration-installation.md).</span><span class="sxs-lookup"><span data-stu-id="4712f-132">In addition, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information on setting up the default screen layout in the **Screen layout** section and [Configure and install Retail hardware station](retail-hardware-station-configuration-installation.md) for setup information about the **Hardware stations** section.</span></span>

<span data-ttu-id="4712f-133">Aşağıdaki resimde örnek bir perakende kanalı kurulum yapılandırması gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="4712f-133">The following image shows an example retail channel setup configuration.</span></span>

![Örnek perakende kanalı yapılandırması](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a><span data-ttu-id="4712f-135">Ek kanal ayarları</span><span class="sxs-lookup"><span data-stu-id="4712f-135">Additional channel set up</span></span>

<span data-ttu-id="4712f-136">Bir kanal için, **Ayarla** bölümünün altındaki Eylem Bölmesi'nde bulunabilecek, kanal için ayarlanması gereken ek öğeler vardır.</span><span class="sxs-lookup"><span data-stu-id="4712f-136">There are additional items that need to be set up for a channel that can be found on the Action Pane under the **Set up** section.</span></span>

<span data-ttu-id="4712f-137">Çevrimiçi kanal kurulumu için gerekli ek görevler şunların ayarlanmasını içerir: Ödeme yöntemleri, kasa bildirimi, teslimat şekilleri, gelir/gider hesabı, bölümler, karşılama grubu ataması ve kasalar.</span><span class="sxs-lookup"><span data-stu-id="4712f-137">Additional tasks required for online channel setup include setting up payment methods, cash declaration, modes of delivery, income/expense account, sections, the fulfillment group assignment, and safes.</span></span>

<span data-ttu-id="4712f-138">Aşağıdaki resimde, **Ayarla** sekmesindeki çeşitli ek perakende kanal kurulum seçenekleri gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="4712f-138">The following image shows various additional retail channel setup options on the **Set up** tab.</span></span>

![Kanalı ayarlama](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="4712f-140">Ödeme yöntemlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="4712f-140">Set up payment methods</span></span>

<span data-ttu-id="4712f-141">Ödeme yöntemlerini ayarlamak için, bu kanalda desteklenen her ödeme türü için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4712f-141">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="4712f-142">Eylem Bölmesi'nde, **Ayarla** sekmesini ve ardından **Ödeme yöntemleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="4712f-142">On the Action Pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="4712f-143">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4712f-143">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="4712f-144">Gezinti bölmesinde, istediğiniz bir ödeme yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="4712f-144">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="4712f-145">**Genel** bölümünde bir **İşlem adı** belirtin ve istediğiniz diğer ayarları yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="4712f-145">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="4712f-146">Ödeme türü için gereken ek ayarları yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="4712f-146">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="4712f-147">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4712f-147">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="4712f-148">Aşağıdaki resimde bir nakit ödeme yöntemi örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="4712f-148">The following image shows an example of a cash payment method.</span></span>

![Örnek ödeme yöntemleri](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a><span data-ttu-id="4712f-150">Kasa bildirimini ayarlama</span><span class="sxs-lookup"><span data-stu-id="4712f-150">Set up cash declaration</span></span>

1. <span data-ttu-id="4712f-151">Eylem Bölmesi'nde, **Ayarla** sekmesini ve ardından **Kasa bildirimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="4712f-151">On the Action Pane, select the **Set Up** tab, and then select **Cash declaration**.</span></span>
1. <span data-ttu-id="4712f-152">Eylem Bölmesi'nde, **Yeni**'yi seçin ve tüm mevcut **Bozuk para** ve **Banknot** para birimlerini oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4712f-152">On the Action Pane, select **New**, and then create all **Coin** and **Note** denominations that are applicable.</span></span>

<span data-ttu-id="4712f-153">Aşağıdaki resimde bir kasa bildirimi örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="4712f-153">The following image shows an example of a cash declaration.</span></span>

![Kasa bildirimlerini ayarlama](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="4712f-155">Teslimat şekillerini ayarla</span><span class="sxs-lookup"><span data-stu-id="4712f-155">Set up modes of delivery</span></span>

<span data-ttu-id="4712f-156">Yapılandırılan teslimat şekillerini, Eylem Bölmesi'ndeki **Ayarla** sekmesinden **Teslimat şekilleri**'ni seçerek görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4712f-156">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the Action Pane.</span></span>  

<span data-ttu-id="4712f-157">Bir teslimat şekli eklemek veya değiştirmek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4712f-157">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="4712f-158">Gezinti bölmesinde **Modüller \> Stok yönetimi \> Teslimat şekilleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="4712f-158">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="4712f-159">Eylem Bölmesi'nde, yeni bir teslimat şekli oluşturmak için **Yeni**'yi seçin veya varolan bir şekli seçin.</span><span class="sxs-lookup"><span data-stu-id="4712f-159">On the Action Pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="4712f-160">**Perakende kanalları** bölümünde, kanalı eklemek için **Satır ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4712f-160">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="4712f-161">Kanalları tek tek eklemek yerine kuruluş düğümleri kullanarak eklemek, kanal eklemeyi kolaylaştırabilir.</span><span class="sxs-lookup"><span data-stu-id="4712f-161">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="4712f-162">Aşağıdaki resimde bir teslimat şekli örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="4712f-162">The following image shows an example of a mode of delivery.</span></span>

![Teslimat şekillerini ayarla](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a><span data-ttu-id="4712f-164">Gelir/gider hesabını ayarlama</span><span class="sxs-lookup"><span data-stu-id="4712f-164">Set up income/expense account</span></span>

<span data-ttu-id="4712f-165">Gelir/gider hesabını ayarlamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4712f-165">To set up income/expense account, follow these steps.</span></span>

1. <span data-ttu-id="4712f-166">Eylem Bölmesi'nde, **Ayarla** sekmesini ve ardından **Gelir/Gider hesabı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="4712f-166">On the Action Pane, select the **Set Up** tab, and then select **Income/Expense account**.</span></span>
1. <span data-ttu-id="4712f-167">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4712f-167">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="4712f-168">**Ad** altında bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="4712f-168">Under **Name**, enter a name.</span></span>
1. <span data-ttu-id="4712f-169">**Arama adı** altında bir arama adı girin.</span><span class="sxs-lookup"><span data-stu-id="4712f-169">Under **Search name**, enter a search name.</span></span>
1. <span data-ttu-id="4712f-170">**Hesap türü** altında bir hesap türü girin.</span><span class="sxs-lookup"><span data-stu-id="4712f-170">Under **Account type**, enter the account type.</span></span>
1. <span data-ttu-id="4712f-171">**İleti satırı 1**, **İleti satırı 2**, **İrsaliye metni 1** ve **İrsaliye metni 2** için metni gerektiği şekilde girin.</span><span class="sxs-lookup"><span data-stu-id="4712f-171">Enter text for **Message line 1**, **Message line 2**, **Slip text 1**, and **Slip text 2** as needed.</span></span>
1. <span data-ttu-id="4712f-172">**Deftere nakil** altında, deftere nakil bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="4712f-172">Under **Posting**, enter posting information.</span></span>
1. <span data-ttu-id="4712f-173">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4712f-173">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="4712f-174">Aşağıdaki resimde bir gelir/gider hesabı örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="4712f-174">The following image shows an example of an income/expense account.</span></span>

![Gelir/gider hesaplarını ayarlama](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a><span data-ttu-id="4712f-176">Bölümleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="4712f-176">Set up sections</span></span>

<span data-ttu-id="4712f-177">Bölümleri ayarlamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4712f-177">To set up sections, follow these steps.</span></span>

1. <span data-ttu-id="4712f-178">Eylem Bölmesi'nde, **Ayarla** sekmesini seçin ve ardından **Bölümler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4712f-178">On the Action Pane, select the **Set Up** tab and click **Sections**.</span></span>
1. <span data-ttu-id="4712f-179">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4712f-179">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="4712f-180">**Bölüm numarası** altında bir bölüm numarası girin.</span><span class="sxs-lookup"><span data-stu-id="4712f-180">Under **Section number**, enter a section number.</span></span>
1. <span data-ttu-id="4712f-181">**Açıklama** altında bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="4712f-181">Under **Description**, enter a description.</span></span>
1. <span data-ttu-id="4712f-182">**Bölüm boyutu** altında bir bölüm boyutu girin.</span><span class="sxs-lookup"><span data-stu-id="4712f-182">Under **Section size**, enter a section size.</span></span>
1. <span data-ttu-id="4712f-183">Gerekirse **Genel** ve **Satış istatistikleri** için ek ayarlar yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="4712f-183">Configure additional settings for **General** and **Sales statistics** as needed.</span></span>
1. <span data-ttu-id="4712f-184">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4712f-184">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="4712f-185">Karşılama grubu atamasını ayarlama</span><span class="sxs-lookup"><span data-stu-id="4712f-185">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="4712f-186">Bir karşılama grubu ataması ayarlamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4712f-186">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="4712f-187">Eylem Bölmesi'nde, **Ayarla** sekmesini ve ardından **Karşılama grubu ataması**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="4712f-187">On the Action Pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="4712f-188">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4712f-188">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="4712f-189">**Karşılama grubu** açılır listesinde bir karşılama grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="4712f-189">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="4712f-190">**Açıklama** açılır listesinde bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="4712f-190">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="4712f-191">Eylem Bölmesi'nde, **Kaydet**'i seçin</span><span class="sxs-lookup"><span data-stu-id="4712f-191">On the Action Pane, select **Save**</span></span>

<span data-ttu-id="4712f-192">Aşağıdaki resimde, bir karşılama grubu ataması kurulum örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="4712f-192">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Karşılama grubu atamalarını ayarlama](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a><span data-ttu-id="4712f-194">Kasaları ayarlama</span><span class="sxs-lookup"><span data-stu-id="4712f-194">Set up safes</span></span>

<span data-ttu-id="4712f-195">Kasaları ayarlamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4712f-195">To set up safes, follow these steps.</span></span>

1. <span data-ttu-id="4712f-196">Eylem Bölmesi'nde, **Ayarla** sekmesini seçin ve **Kasalar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4712f-196">On the Action Pane, select the **Set Up** tab and click **Safes**.</span></span>
1. <span data-ttu-id="4712f-197">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4712f-197">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="4712f-198">Kasa için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="4712f-198">Enter a name for the safe.</span></span>
1. <span data-ttu-id="4712f-199">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4712f-199">On the Action Pane, select **Save**.</span></span>

### <a name="ensure-unique-transaction-ids"></a><span data-ttu-id="4712f-200">Hareket kodlarının benzersiz olduğundan emin olun</span><span class="sxs-lookup"><span data-stu-id="4712f-200">Ensure unique transaction IDs</span></span>

<span data-ttu-id="4712f-201">Commerce sürüm 10.0.18 itibariyle, satış noktası (POS) için oluşturulan hareket kodları sıralıdır ve aşağıdaki bölümleri içerir:</span><span class="sxs-lookup"><span data-stu-id="4712f-201">As of the Commerce version 10.0.18 , transaction IDs generated for the point of sale (POS) are sequential and include the following parts:</span></span>

- <span data-ttu-id="4712f-202">Mağaza kodu ve terminal kodu birleşimi olan sabit bir bölüm.</span><span class="sxs-lookup"><span data-stu-id="4712f-202">A fixed part, which is a concatenation of store ID and terminal ID.</span></span> 
- <span data-ttu-id="4712f-203">Bir numara serisi olan sıralı bölüm.</span><span class="sxs-lookup"><span data-stu-id="4712f-203">A sequential part, which is a number sequence.</span></span> 

<span data-ttu-id="4712f-204">Biçim şöyledir: *{store}-{terminal}-{numbersequence}*.</span><span class="sxs-lookup"><span data-stu-id="4712f-204">Specifically, the format is *{store}-{terminal}-{numbersequence}*.</span></span> 

<span data-ttu-id="4712f-205">Hareket kodları hem çevrimdışı hem çevrimiçi modlarda oluşturulabildiğinden, oluşturulan hareket kodlarında yineleme olduğu görülmüştür.</span><span class="sxs-lookup"><span data-stu-id="4712f-205">Because transaction IDs can be generated in offline and online modes, there have been instances of duplicate transaction IDs being generated.</span></span> <span data-ttu-id="4712f-206">Yinelenen hareket kodlarının ortadan kaldırılması, uzun süren el ile veri düzeltmeyi gerektirir.</span><span class="sxs-lookup"><span data-stu-id="4712f-206">Eliminating duplicate transaction IDs requires a lot of manual data fixing.</span></span> 

<span data-ttu-id="4712f-207">Commerce sürüm 10.0.19 ile birlikte hareket kodu biçimi, sıralı bölümü kaldıracak şekilde güncelleştirilmiştir. Bunun yerine, 1970'den beri zamanı milisaniye cinsinde hesaplayarak oluşturulan 13 basamaklı bir sayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="4712f-207">With Commerce version 10.0.19, the transaction ID format has been updated to remove the sequential part and instead uses a 13-digit number generated by calculating the time in milliseconds since 1970.</span></span> <span data-ttu-id="4712f-208">Bu değişiklikle birlikte yeni hareket kodu biçimi şöyle olmuştur: *{store}-{terminal}-{millisecondsSince1970}*.</span><span class="sxs-lookup"><span data-stu-id="4712f-208">With this change, the new transaction ID format is *{store}-{terminal}-{millisecondsSince1970}*.</span></span> <span data-ttu-id="4712f-209">Bu güncelleştirme, hareket kodunun sıralı olmamasını sağlar ve hareket kodlarının her zaman benzersiz olmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="4712f-209">This update makes the transaction ID non-sequential and ensures that transaction IDs are always unique.</span></span> 

> [!NOTE]
> <span data-ttu-id="4712f-210">Hareket kodları yalnızca dahili sistem kullanımına yöneliktir, bu nedenle sıralı olmaları gerekmez.</span><span class="sxs-lookup"><span data-stu-id="4712f-210">Transaction IDs are meant for internal system use only, so they are not required to be sequential.</span></span> <span data-ttu-id="4712f-211">Ancak, birçok ülke giriş kodlarının sıralı olmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="4712f-211">However, many countries require receipt IDs to be sequential.</span></span>

<span data-ttu-id="4712f-212">Yeni hareket kodu biçim özelliği, **Özellik yönetimi** çalışma alanından etkinleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="4712f-212">The new transaction ID format feature can be enabled from the **Feature management** workspace.</span></span> 

<span data-ttu-id="4712f-213">Yeni hareket kodlarının kullanımını etkinleştirmek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="4712f-213">To enable the use of new transaction IDs, follow these steps:</span></span>

1. <span data-ttu-id="4712f-214">Commerce genel merkezinde, **Sistem yönetimi \> Çalışma alanları \> Özellik yönetimi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="4712f-214">In Commerce headquarters, go to **System administration \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="4712f-215">"Reatil ve Commerce" modülüne göre filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="4712f-215">Filter for the "retail and commerce" module.</span></span>
1. <span data-ttu-id="4712f-216">**Yinelenen hareket kodlarından kaçınmak için yeni hareket kodunu etkinleştir** özellik adını arayın.</span><span class="sxs-lookup"><span data-stu-id="4712f-216">Search for the **Enable new transaction id to avoid duplicate transaction ids** feature name.</span></span>
1. <span data-ttu-id="4712f-217">Özelliği seçin, daha sonra sağ bölmede yer alan **Şimdi Etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4712f-217">Select the feature, and then select **Enable Now** in the right pane.</span></span>  
1. <span data-ttu-id="4712f-218">**Retail and Commerce \> Retail and Commerce IT \> Dağıtım planı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="4712f-218">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="4712f-219">Etkinleştirilen özelliği depolarla eşitlemek için **1070 Kanal yapılandırması** ve **1170 POS görev kaydedici** işlerini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="4712f-219">Run the **1070 Channel configuration** and **1170 POS task recorder** jobs to synchronize the enabled feature to the stores.</span></span>
1. <span data-ttu-id="4712f-220">Değişiklikler mağazalara gönderildikten sonra, yeni hareket kodu biçiminin kullanılabilmesi için POS terminallerinin kapatılıp yeniden açılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="4712f-220">After the changes have been sent to the stores, POS terminals must be closed and reopened to use the new transaction ID format.</span></span> 

> [!NOTE]
> <span data-ttu-id="4712f-221">Yeni hareket kodu biçimi özelliği etkinleştirildikten sonra bu özelliği devre dışı bırakamazsınız.</span><span class="sxs-lookup"><span data-stu-id="4712f-221">After the new transaction ID format feature is enabled, you will not be able to disable this feature.</span></span> <span data-ttu-id="4712f-222">Devre dışı bırakılması gerekiyorsa lütfen Commerce destek ekibiyle iletişime geçin.</span><span class="sxs-lookup"><span data-stu-id="4712f-222">If it must be disabled, please contact Commerce Support.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4712f-223">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="4712f-223">Additional resources</span></span>

[<span data-ttu-id="4712f-224">Kanallara genel bakış</span><span class="sxs-lookup"><span data-stu-id="4712f-224">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="4712f-225">Kanal kurulum önkoşulları</span><span class="sxs-lookup"><span data-stu-id="4712f-225">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="4712f-226">Çevrimiçi kanal ayarlama</span><span class="sxs-lookup"><span data-stu-id="4712f-226">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="4712f-227">Çağrı merkezi kanalını ayarlama</span><span class="sxs-lookup"><span data-stu-id="4712f-227">Set up a call center channel</span></span>](channel-setup-callcenter.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
