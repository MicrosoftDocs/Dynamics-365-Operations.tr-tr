---
title: Kanal için iade ve para iadesi ilkesi oluşturma ve güncelleştirme
description: Bu konu, bir kanal için iade ve para iadesi ilkesinin nasıl ayarlanacağını açıklar.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: 66bb9bbd338561315f2f69ae4aff86a67513b190
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024399"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a><span data-ttu-id="fc73b-103">Kanal için iade ve para iadesi ilkesi oluşturma ve güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="fc73b-103">Create and update a returns and refunds policy for a channel</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]


## <a name="overview"></a><span data-ttu-id="fc73b-104">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="fc73b-104">Overview</span></span>

<span data-ttu-id="fc73b-105">Dynamics 365 Commerce'deki kanal iade ilkesi, perakendecilerin, bir satış noktasında (POS) iadeyi işleme için izin verilen, tüm ödeme faaliyetlerde zorlayıcı olarak ayarlanmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="fc73b-105">The channel return policy in Dynamics 365 Commerce enables retailers to set enforcements on which payment tenders can be allowed for processing a return on a point of sale (POS) device.</span></span>  

<span data-ttu-id="fc73b-106">Bu konu, bir kanal için iade ve para iadesi ilkesinin nasıl ayarlanacağı adımlarını açıklar.</span><span class="sxs-lookup"><span data-stu-id="fc73b-106">This topic describes the steps to set up a returns and refunds policy for a channel.</span></span>

<span data-ttu-id="fc73b-107">İlkenin kapsamı şu anda bir kanal için izin verilmeyen ödeme koşullarını ayarlama ile sınırlı.</span><span class="sxs-lookup"><span data-stu-id="fc73b-107">The scope of the policy is currently limited to setting the payment tenders that can be allowed for a channel.</span></span> <span data-ttu-id="fc73b-108">"İzin verildi" listesi, satın alma işlemi yapmak için kullanılan ödeme yöntemlerine dayanır.</span><span class="sxs-lookup"><span data-stu-id="fc73b-108">The "allowed" list is based on the payment methods used to make the purchase.</span></span> <span data-ttu-id="fc73b-109">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="fc73b-109">For example:</span></span>

- <span data-ttu-id="fc73b-110">Bir satın alma, hediye kartı kullanılarak yapılmışsa, mağaza ilkesi para iadelerini yalnızca yeni bir hediye kartına veya mağaza kredisi vermeye yönelik olarak işler.</span><span class="sxs-lookup"><span data-stu-id="fc73b-110">If a purchase was made using a gift card, the store policy is to process refunds only to a new gift card or to give store credit.</span></span> 
- <span data-ttu-id="fc73b-111">Nakit olarak satış yapıldığında, para iadesi için izin verilen seçenekler nakit, hediye kartı ve müşteri hesabı olmasına karşın kredi kartınının yer aldığı bir hesaptır.</span><span class="sxs-lookup"><span data-stu-id="fc73b-111">If a sale is made using cash, the options allowed for refund are cash, gift card, and customer account, but not credit card.</span></span> 


## <a name="enable-return-policy"></a><span data-ttu-id="fc73b-112">İade İlkesini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="fc73b-112">Enable return policy</span></span>

<span data-ttu-id="fc73b-113">Kanal iade ilkesi işlevini etkinleştirmek için aşağıdakileri yapın:</span><span class="sxs-lookup"><span data-stu-id="fc73b-113">To enable the channel return policy functionality, do the following:</span></span>

1. <span data-ttu-id="fc73b-114">Dynamics 365 Commerce'de **Özellik yönetimi** çalışma alanına gidin.</span><span class="sxs-lookup"><span data-stu-id="fc73b-114">Go to the **Feature Management** workspace in Dynamics 365 Commerce.</span></span>
2. <span data-ttu-id="fc73b-115">**Kanal iade ilkelerini etkinleştirme** özelliğini, özellik adları listesinde arayın.</span><span class="sxs-lookup"><span data-stu-id="fc73b-115">Search for the **Enable channel return policies** feature in the list of feature names.</span></span>
3. <span data-ttu-id="fc73b-116">**Şimdi etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="fc73b-116">Select **Enable now**.</span></span> 

## <a name="configure-return-policy"></a><span data-ttu-id="fc73b-117">İade İlkesi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="fc73b-117">Configure return policy</span></span>

<span data-ttu-id="fc73b-118">Bir perakende mağaza veya çevrimiçi perakende kanalında iade ilkesi konfigüre etmek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="fc73b-118">Follow these steps to configure a return policy for a retail store or online retail channel.</span></span>

1. <span data-ttu-id="fc73b-119">**Retail ve Commerce** \> **Kanal kurulumu** \> **İadeler** \> **Kanal iade ilkesine** gidin.</span><span class="sxs-lookup"><span data-stu-id="fc73b-119">Go to **Retail and Commerce** \> **Channel Setup** \> **Returns** \> **Channel return policy**.</span></span>

2. <span data-ttu-id="fc73b-120">Yeni bir iade politikası şablonu oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fc73b-120">Select **New** to create a new return policy template.</span></span> <span data-ttu-id="fc73b-121">Varolan bir şablonu kullanmak için, sol bölmedeki şablonu seçin.</span><span class="sxs-lookup"><span data-stu-id="fc73b-121">To use an existing template, select the template in the left pane.</span></span> <span data-ttu-id="fc73b-122">Yeni şablonlar için, kanala uygulandığında ilkeyi tanımlamanıza yardımcı olacak bir ad ve açıklama ekleyin.</span><span class="sxs-lookup"><span data-stu-id="fc73b-122">For new templates, add a name and description that will help you identify the policy when it is being applied to the channel.</span></span>

   <span data-ttu-id="fc73b-123">![Yeni iade ilkesi Ekle](media/Return-policy-page1.png "Yeni iade ilkesi Ekle")</span><span class="sxs-lookup"><span data-stu-id="fc73b-123">![Add new return policy](media/Return-policy-page1.png "Add new return rolicy")</span></span>
     
   
3. <span data-ttu-id="fc73b-124">**İzin verilen iade ödeme yöntemleri** bölümünde, her bir ödeme yöntemine özgü olan **izin verilen** iade ödeme yöntemlerini tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="fc73b-124">In the **Allowed refund payment methods** section, define **Allowed** return payment tenders that are specific to each payment method.</span></span>
   <span data-ttu-id="fc73b-125">![Ödeme yöntemleri ekle](media/Return-policy-page2.PNG "Ödeme türü başına izin verilen ödeme yöntemlerini ayarla")</span><span class="sxs-lookup"><span data-stu-id="fc73b-125">![Add payment methods](media/Return-policy-page2.PNG "Set allowed payment methods per payment type")</span></span>
   
    > [!IMPORTANT]
    > - <span data-ttu-id="fc73b-126">Ödeme yöntemleri, organizasyon için ayarlanan ödeme yöntemlerinden türetilir.</span><span class="sxs-lookup"><span data-stu-id="fc73b-126">The payment methods are derived from the payment methods set for the organization.</span></span>
    > - <span data-ttu-id="fc73b-127">Listelenen her ödeme yöntemine izin verilen bir ödeme türü eklenmesi, iadenin izin verilen iade ödeme tipine yapılabilmesi için bunların yapılmasına olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="fc73b-127">Adding an allowed return tender type for each listed payment method will ensure that returns can be made to the allowed return tender type.</span></span>
    
4. <span data-ttu-id="fc73b-128">İade politikası şablonunu, kullanılacak mağazalar ile ilişkilendirin.</span><span class="sxs-lookup"><span data-stu-id="fc73b-128">Associate the return policy template with the stores where it will be used.</span></span> <span data-ttu-id="fc73b-129">**Perakende kanalları** sekmesinde **Ekle**'yi seçin ve kullanılabilir kanalları ilişkilendirin.</span><span class="sxs-lookup"><span data-stu-id="fc73b-129">Select **Add** in the **Retail Channels** tab and associate the available channels.</span></span> 

    - <span data-ttu-id="fc73b-130">**Kuruluş düğümlerini Seç** iletişim kutusunda, şablonun ilişkilendirilmesi gereken depoları, bölgeleri ve organizasyonları seçin.</span><span class="sxs-lookup"><span data-stu-id="fc73b-130">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>
    - <span data-ttu-id="fc73b-131">Her bir mağaza ile yalnızca bir iade ilkesi şablonu ilişkilendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="fc73b-131">Only one return policy template can be associated with each store.</span></span>
    - <span data-ttu-id="fc73b-132">Mağaza, bölge veya organizasyon seçmek için ok düğmelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="fc73b-132">Use the arrow buttons to select stores, regions, or organizations.</span></span>
    - <span data-ttu-id="fc73b-133">İlkedeki yürürlülük tarihi ilkelerin kanallara uygulandığı ve kanal işlerinin çalıştırıldığı tarih olacaktır.</span><span class="sxs-lookup"><span data-stu-id="fc73b-133">The effective date on the policy will be the date on which the policies are applied to the channels and the channel jobs are run.</span></span> 

    <span data-ttu-id="fc73b-134">![Organizasyon kırılımını seç iletişim kutusu](media/Return-policy-page3.PNG "Organizasyon kırılımını seç iletişim kutusu")</span><span class="sxs-lookup"><span data-stu-id="fc73b-134">![Choose organization nodes dialog box](media/Return-policy-page3.PNG "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="fc73b-135">**Dağıtım zamanlaması** sayfasında, POS'un kanal iade ilkesini kullanabilmesini sağlamak için, **1070** işini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="fc73b-135">On the **Distribution schedule** page, run the **1070** job to make the channel return policy available to the POS.</span></span>

## <a name="preview-the-channel-return-policy-in-the-pos"></a><span data-ttu-id="fc73b-136">POS 'ta kanal iade ilkesini Önizle</span><span class="sxs-lookup"><span data-stu-id="fc73b-136">Preview the channel return policy in the POS</span></span>

<span data-ttu-id="fc73b-137">POS 'ta izin verilen iade ödeme tiplerini görüntülemek için aşağıdaki örneklerden birinde bulunan adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="fc73b-137">Follow the steps in either of the following examples to view the allowed return tender types in POS.</span></span>

1. <span data-ttu-id="fc73b-138">POS'ta kasiyer veya yönetici olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="fc73b-138">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="fc73b-139">**Üst karakter ve çekmece** altında **günlüğü göster**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="fc73b-139">Under **Shift and Drawer**, select **Show journal**.</span></span>
3. <span data-ttu-id="fc73b-140">İade işleminin parçası olan hareketi seçin.</span><span class="sxs-lookup"><span data-stu-id="fc73b-140">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="fc73b-141">Para iadesi yapılacak maddeleri seçin ve ödeme yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="fc73b-141">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="fc73b-142">Seçilen ödeme, izin verilen iade ödeme tipleri listesinde ise, kasiyer hareketi tamamlayabilir.</span><span class="sxs-lookup"><span data-stu-id="fc73b-142">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="fc73b-143">Ödeme ödemesine izin verilmiyorsa, bir hata mesajı görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="fc73b-143">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="fc73b-144">Tüm izin verilen iade ödeme tiplerinin listesini görüntülemek için **tutar vadesini** seçin.</span><span class="sxs-lookup"><span data-stu-id="fc73b-144">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="fc73b-145">-veya-</span><span class="sxs-lookup"><span data-stu-id="fc73b-145">-or-</span></span>

1. <span data-ttu-id="fc73b-146">POS'ta kasiyer veya yönetici olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="fc73b-146">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="fc73b-147">**İade hareketi** seçin ve barkod taraması veya el ile giriş kullanarak giriş kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="fc73b-147">Select **Return Transaction** and enter the receipt ID using a barcode scan or by manual entry.</span></span> 
3. <span data-ttu-id="fc73b-148">İade işleminin parçası olan hareketi seçin.</span><span class="sxs-lookup"><span data-stu-id="fc73b-148">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="fc73b-149">Para iadesi yapılacak maddeleri seçin ve ödeme yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="fc73b-149">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="fc73b-150">Seçilen ödeme, izin verilen iade ödeme tipleri listesinde ise, kasiyer hareketi tamamlayabilir.</span><span class="sxs-lookup"><span data-stu-id="fc73b-150">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="fc73b-151">Ödeme ödemesine izin verilmiyorsa, bir hata mesajı görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="fc73b-151">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="fc73b-152">Tüm izin verilen iade ödeme tiplerinin listesini görüntülemek için **tutar vadesini** seçin.</span><span class="sxs-lookup"><span data-stu-id="fc73b-152">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="fc73b-153">![Geri ödemeye izin verilmiyor](media/Return-policy-page6.png "Geri ödeme türüne izin verilmiyor")</span><span class="sxs-lookup"><span data-stu-id="fc73b-153">![Refund not allowed](media/Return-policy-page6.png "Refund type not allowed")</span></span>



<span data-ttu-id="fc73b-154">![Ödeme yöntemleri listesi](media/Return-policy-page5.PNG "Geri ödeme türlerine izin veriliyor")</span><span class="sxs-lookup"><span data-stu-id="fc73b-154">![List of payment methods](media/Return-policy-page5.PNG "Refund types allowed")</span></span>
