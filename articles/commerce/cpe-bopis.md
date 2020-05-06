---
title: Dynamics 365 Commerce ortamında BOPIS yapılandırma
description: Bu konu çevrimiçi satın al, mağazadan teslim al (BOPIS) işleminin, sağlandıktan sonra Microsoft Dynamics 365 Commerce ortamında nasıl yapılandırılacağını açıklar.
author: rubendel
manager: annbe
ms.date: 04/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: rubendel
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 956d66d09885d4d54655ce25b3aa7ba6a9c34cf4
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282808"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="20a2b-103">Dynamics 365 Commerce ortamında BOPIS yapılandırma</span><span class="sxs-lookup"><span data-stu-id="20a2b-103">Configure BOPIS in a Dynamics 365 Commerce environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="20a2b-104">Bu konu çevrimiçi satın al, mağazadan teslim al (BOPIS) işleminin, ortam sağlandıktan sonra Microsoft Dynamics 365 Commerce ortamında nasıl yapılandırılacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="20a2b-104">This topic explains how to configure buy online, pickup in store (BOPIS) in a Microsoft Dynamics 365 Commerce environment after the environment has been provisioned.</span></span>

## <a name="prerequisite"></a><span data-ttu-id="20a2b-105">Önkoşul</span><span class="sxs-lookup"><span data-stu-id="20a2b-105">Prerequisite</span></span>

<span data-ttu-id="20a2b-106">Bu konudaki yordamları yalnızca Commerce önizleme ortamınızı sağlandıktan ve yapılandırdıktan sonra tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="20a2b-106">Complete the procedures in this topic only after your Commerce preview environment has been provisioned and configured.</span></span> <span data-ttu-id="20a2b-107">Ortamınızı sağlama ve yapılandırma hakkında bilgi için bkz. [Dynamics 365 Commerce önizleme ortamı sağlama](provisioning-guide.md) ve [Dynamics 365 Commerce önizleme ortamı yapılandırma](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning).</span><span class="sxs-lookup"><span data-stu-id="20a2b-107">For information about how to provision and configure your environment, see [Provision a Dynamics 365 Commerce preview environment](provisioning-guide.md) and [Configure a Dynamics 365 Commerce preview environment](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning).</span></span>

<span data-ttu-id="20a2b-108">Commerce ortamınız sağlandıktan ve uçtan uca yapılandırıldıktan sonra, bu konuyu BOPIS senaryolarını etkinleştirmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="20a2b-108">After your Commerce environment has been provisioned and configured end to end, you can use this topic to enable BOPIS scenarios.</span></span>

## <a name="configure-the-pos"></a><span data-ttu-id="20a2b-109">POS yapılandırma</span><span class="sxs-lookup"><span data-stu-id="20a2b-109">Configure the POS</span></span>

### <a name="configure-modern-pos"></a><span data-ttu-id="20a2b-110">Modern POS yapılandırma</span><span class="sxs-lookup"><span data-stu-id="20a2b-110">Configure Modern POS</span></span>

<span data-ttu-id="20a2b-111">Kredi kartı ödemesi içeren BOPIS senaryoları bir donanım istasyonu gerektirir.</span><span class="sxs-lookup"><span data-stu-id="20a2b-111">BOPIS scenarios that involve a credit card payment require a hardware station.</span></span> <span data-ttu-id="20a2b-112">Donanım istasyonu Windows ve Android istemcileri için Modern POS'a yerleşik olarak bulunur.</span><span class="sxs-lookup"><span data-stu-id="20a2b-112">The hardware station is built into Modern POS for Windows and Android clients.</span></span> <span data-ttu-id="20a2b-113">iOS için Cloud POS veya Modern POS kullanıyorsanız, satış noktası (POS) istemcisi paylaşılan bir donanım istasyonuyla eşleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="20a2b-113">If you're using Cloud POS or Modern POS for iOS, the point of sale (POS) client must be paired with a shared hardware station.</span></span> <span data-ttu-id="20a2b-114">Bu konu, Windows ve Android istemcileri için BOPIS'in nasıl yapılandırılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="20a2b-114">This topic explains how to configure BOPIS for Windows and Android clients.</span></span> <span data-ttu-id="20a2b-115">Paylaşılan donanım istasyonu ayarlama hakkında daha fazla bilgi için bkz. [Retail hardware station'ı yapılandırma ve yükleme](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).</span><span class="sxs-lookup"><span data-stu-id="20a2b-115">For information about how to set up a shared hardware station, see [Configure and install Retail hardware station](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).</span></span>

1. <span data-ttu-id="20a2b-116">**Retail ve Commerce \> Kanal kurulumu \> POS kurulumu \> Kasalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-116">Go to **Retail and Commerce \> Channel setup \> POS setup \> Registers**.</span></span>
2. <span data-ttu-id="20a2b-117">**SANFRAN-5** kasasını ve ardından **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-117">Select register **SANFRAN-5**, and then select **Edit**.</span></span>
3. <span data-ttu-id="20a2b-118">**HW002** olan **Donanım profili** alanının değerini **HW001** olarak değiştirin ve **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-118">Change the value of the **Hardware profile** field from **HW002** to **HW001**, and then select **Save**.</span></span>
4. <span data-ttu-id="20a2b-119">Değişiklikleri eşitlemek için **Retail ve Commerce \> Retail ve Commerce BT \> Dağıtım zamanlaması**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-119">To synchronize the changes, go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
5. <span data-ttu-id="20a2b-120">**1090** dağıtım zamanlamasını seçin ve ardından Eylem Bölmesinde **Şimdi çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-120">Select distribution schedule **1090**, and then, on the Action Pane, select **Run now**.</span></span>
6. <span data-ttu-id="20a2b-121">Veri eşitlemeyi başlatmak için **Evet**'i ve sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-121">Select **Yes** and then **OK** to initiate data synchronization.</span></span> 

### <a name="install-modern-pos"></a><span data-ttu-id="20a2b-122">Modern POS yükleme</span><span class="sxs-lookup"><span data-stu-id="20a2b-122">Install Modern POS</span></span>

1. <span data-ttu-id="20a2b-123">**Retail ve Commerce \> Kanal kurulumu \> POS kurulumu \> Cihazlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-123">Go to **Retail and Commerce \> Channel setup \> POS setup \> Devices**.</span></span>
2. <span data-ttu-id="20a2b-124">**SANFRANCIS-5** cihazını seçin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-124">Select device **SANFRANCIS-5**.</span></span>
3. <span data-ttu-id="20a2b-125">Eylem Bölmesinde, **İndir**'i ve sonra **Yapılandırma dosyası**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-125">On the Action Pane, select **Download**, and then select **Configuration file**.</span></span>
4. <span data-ttu-id="20a2b-126">**İndir**'i ve ardından **Retail Modern POS** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-126">Select **Download**, and then select **Retail Modern POS**.</span></span> 
5. <span data-ttu-id="20a2b-127">**ModernPOSSetup.exe** dosyasının indirilmesi tamamlandığında **Dosyayı aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-127">When download of the **ModernPOSSetup.exe** file is completed, select **Open file**.</span></span>

    ![Dosya aç](./dev-itpro/media/PAYMENTS/openfile.png)

6. <span data-ttu-id="20a2b-129">Yükleme işlemine devam etmek için **İleri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-129">Select **Next** to go through the installation process.</span></span> <span data-ttu-id="20a2b-130">Yükleme tamamlandığında **Kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-130">When installation is completed, select **Close**.</span></span>

### <a name="activate-modern-pos"></a><span data-ttu-id="20a2b-131">Modern POS'u etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="20a2b-131">Activate Modern POS</span></span>

1. <span data-ttu-id="20a2b-132">Windows masaüstünde, **Başlat** düğmesini seçin ve **Retail Modern POS** girin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-132">On the Windows desktop, select the **Start** button, and enter **Retail Modern POS**.</span></span>
2. <span data-ttu-id="20a2b-133">Etkinleştirmeyi başlatmak için **Retail Modern POS** uygulamasını seçin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-133">Select the **Retail Modern POS** application to initiate activation.</span></span>
3. <span data-ttu-id="20a2b-134">**Sonraki**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-134">Select **Next**.</span></span> <span data-ttu-id="20a2b-135">**Sunucu URL'si**, **Cihaz kodu** ve **Kayıt numarası** alanları, önceki yordamda karşıdan yüklediğiniz yapılandırma dosyasındaki bilgileri kullanarak önceden ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="20a2b-135">The **Server URL**, **Device ID**, and **Register number** fields should be preset by using information from the configuration file that you downloaded in the previous procedure.</span></span>
4. <span data-ttu-id="20a2b-136">**Etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-136">Select **Activate**.</span></span>
5. <span data-ttu-id="20a2b-137">Bir kimlik doğrulama iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="20a2b-137">An authentication dialog box appears.</span></span> <span data-ttu-id="20a2b-138">Daha önce çalışan **000713-Andrew Collette** ile ilişkilendirilmiş olan e-posta adresini kullanan hesabı seçin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-138">Select the account that uses the email address that was previously associated with worker **000713 - Andrew Collette**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="20a2b-139">Bir çalışanı kimliğinize henüz ilişkilendirmediyseniz, etkinleştirme başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="20a2b-139">If you haven't yet associated a worker with your identity, activation will be unsuccessful.</span></span> <span data-ttu-id="20a2b-140">Bu durumda, [Dynamics 365 Commerce önizleme ortamını yapılandırma](cpe-post-provisioning.md#associate-a-worker-with-your-identity) konusundaki "Çalışanı kimliğinizle ilişkilendirme" bölümünde anlatılan adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-140">In this case, follow the steps under the "Associate a worker with your identity" section in the [Configure a Dynamics 365 Commerce preview environment](cpe-post-provisioning.md#associate-a-worker-with-your-identity) topic.</span></span>
    
6. <span data-ttu-id="20a2b-141">Kuruluşunuzun cihazı yönetmesine izin vermek isteyip istemediğiniz sorulduğunda **Yalnızca bu uygulama**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-141">When you're prompted to let your organization manage the device, select **This app only**.</span></span>
7. <span data-ttu-id="20a2b-142">Etkinleştirme tamamlandığında **Başlarken**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-142">When activation is completed, select **Get started**.</span></span>

### <a name="enable-bopis-in-modern-pos"></a><span data-ttu-id="20a2b-143">Modern POS'ta BOPIS'i etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="20a2b-143">Enable BOPIS in Modern POS</span></span>

1. <span data-ttu-id="20a2b-144">Modern POS'ta operatör kodu olarak **000713** ve parola olarak **123** kullanarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="20a2b-144">Sign in to Modern POS by using **000713** as the operator ID and **123** as the password.</span></span>
2. <span data-ttu-id="20a2b-145">Tanıtıcı rehberlik videosu oynatılırken, iletişim kutusunun sol alt köşesindeki iki onay kutusunu işaretleyin ve ardından iletişim kutusunu kapatın.</span><span class="sxs-lookup"><span data-stu-id="20a2b-145">While the introductory walkthrough video is playing, select the two check boxes in the lower-left corner of the dialog box, and then close the dialog box.</span></span>
3. <span data-ttu-id="20a2b-146">Vardiyayı kapatmak isteyip istemediğiniz sorulmazda, sağdaki **Karşılama** sayfasına kaydırın,**Vardiyayı kapat**'ı seçin ve ardından POS'ta yeniden oturum açın.</span><span class="sxs-lookup"><span data-stu-id="20a2b-146">If you aren't prompted to close the shift, scroll to the right on the **Welcome** page, select **Close shift**, and then sign back in to the POS.</span></span>
4. <span data-ttu-id="20a2b-147">Oturum açtıktan sonra, istendiğinde, **Çekmece işlemi olmayan bir işlem gerçekleştir** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-147">After you're signed in, when you're prompted, select **Perform a non-drawer operation**.</span></span>
5. <span data-ttu-id="20a2b-148">**Karşılama** sayfasında sağa kaydırın ve **Donanım istasyonu seç** işlemini seçin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-148">On the **Welcome** page, scroll to the right, and select the **Select hardware station** operation.</span></span>
6. <span data-ttu-id="20a2b-149">**Yönet**'i seçin, **Donanım istasyonu kullan** seçeneğini **Açık** olarak ayarlayın ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-149">Select **Manage**, set the **Use hardware station** option to **On**, and then select **OK**.</span></span>
7. <span data-ttu-id="20a2b-150">POS oturumunu kapatın ve tekrar oturum açın.</span><span class="sxs-lookup"><span data-stu-id="20a2b-150">Sign out of the POS, and then sign back in.</span></span>
8. <span data-ttu-id="20a2b-151">Oturum açtıktan sonra **Yeni vardiya aç**'ı ve sonra **Çekmece**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-151">After you're signed in, select **Open a new shift**, and then select **Drawer**.</span></span>

## <a name="complete-a-bopis-scenario"></a><span data-ttu-id="20a2b-152">BOPIS senaryosu tamamlama</span><span class="sxs-lookup"><span data-stu-id="20a2b-152">Complete a BOPIS scenario</span></span>

### <a name="create-a-storefront-order-for-in-store-pickup"></a><span data-ttu-id="20a2b-153">Mağazadan alma için bir mağaza siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="20a2b-153">Create a storefront order for in-store pickup</span></span>

1. <span data-ttu-id="20a2b-154">Ortam yapılandırması sırasında [e-Ticareti başlat](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) adımında belirttiğiniz URL'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-154">Go to the URL that you specified in the [Initialize e-Commerce](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) step during environment configuration.</span></span>
2. <span data-ttu-id="20a2b-155">Bir madde seçin ve **Sepete ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-155">Select an item, and select **Add to cart**.</span></span>
3. <span data-ttu-id="20a2b-156">Alışveriş çantası sayfasında, yeni eklediğiniz sipariş satır için **Bunu çek**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-156">On the shopping bag page, select **Pick this up** for the order line that you just added.</span></span>
4. <span data-ttu-id="20a2b-157">**Mağaza seç** iletişim kutusunda, **San Francisco** girin ve ardından **Ara** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-157">In the **Select a store** dialog box, enter **San Francisco**, and then select the **Search** button.</span></span>
5. <span data-ttu-id="20a2b-158">Sonuç listesinde, San Francisco mağazasını bulun ve **Buradan çek**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-158">In the list of results, find the San Francisco store, and select **Pick up here**.</span></span>
6. <span data-ttu-id="20a2b-159">Alışveriş çantası sayfasında, **Misafir olarak ödeme yap**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-159">On the shopping bag page, select **Checkout as Guest**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="20a2b-160">Ödeme işlemine devam etmek için tanımlama bilgisi bildirimini kabul etmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="20a2b-160">To continue with checkout, you must accept the cookie notice.</span></span> <span data-ttu-id="20a2b-161">Bu bildirim, ödeme sayfasının en üstünde bir başlık olarak görünür.</span><span class="sxs-lookup"><span data-stu-id="20a2b-161">This notice appears as a banner at the top of the checkout page.</span></span>

7. <span data-ttu-id="20a2b-162">Kredi kartı ödeme yöntemi için aşağıdaki ayrıntıları girin:</span><span class="sxs-lookup"><span data-stu-id="20a2b-162">For the credit card payment method, enter the following details:</span></span>

    - <span data-ttu-id="20a2b-163">**Kart sahibi adı:** Herhangi bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-163">**Cardholder name:** Enter any name.</span></span>
    - <span data-ttu-id="20a2b-164">**Kart numarası:** **4111-1111-1111-1111** girin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-164">**Card number:** Enter **4111-1111-1111-1111**.</span></span>
    - <span data-ttu-id="20a2b-165">**Son kullanma tarihi:** **10/20** girin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-165">**Expiration date:** Enter **10/20**.</span></span>
    - <span data-ttu-id="20a2b-166">**Kart doğrulama değeri (CVV) kodu:** **737** girin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-166">**Card verification value (CVV) code:** Enter **737**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="20a2b-167">Herhangi bir koşulda test sitesinde gerçek kredi kartı bilgilerini kullanmaya çalışmayın!</span><span class="sxs-lookup"><span data-stu-id="20a2b-167">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

8. <span data-ttu-id="20a2b-168">Fatura adresinin ayrıntılarını girerek ödeme işlemine devam edin ve **Kaydet ve devam et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-168">Continue with checkout by entering details of the billing address, and then select **Save and continue**.</span></span>
9. <span data-ttu-id="20a2b-169">Sipariş verilmeye hazır olduğunda, **Ödeme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-169">When the order is ready to be placed, select **Checkout**.</span></span>

### <a name="synchronize-online-orders-to-the-back-office"></a><span data-ttu-id="20a2b-170">Çevrimiçi siparişleri arka ofisle eşitleme</span><span class="sxs-lookup"><span data-stu-id="20a2b-170">Synchronize online orders to the back office</span></span>

<span data-ttu-id="20a2b-171">Çevrimiçi siparişleri eşitleme hakkında bilgi için bkz. [Çevrimiçi satışları ve ödemeleri deftere nakletme](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments).</span><span class="sxs-lookup"><span data-stu-id="20a2b-171">For information about how to synchronize online orders, see [Posting of online sales and payments](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments).</span></span>

### <a name="pick-up-an-order-in-the-store"></a><span data-ttu-id="20a2b-172">Bir siparişi mağazadan alma</span><span class="sxs-lookup"><span data-stu-id="20a2b-172">Pick up an order in the store</span></span>

1. <span data-ttu-id="20a2b-173">POS'ta oturum açın.</span><span class="sxs-lookup"><span data-stu-id="20a2b-173">Sign in to the POS.</span></span>
2. <span data-ttu-id="20a2b-174">**Karşılama** ekranında, **Sipariş karşılama**'yı seçin</span><span class="sxs-lookup"><span data-stu-id="20a2b-174">On the **Welcome** screen, select **Order fulfillment**</span></span>
3. <span data-ttu-id="20a2b-175">Çekilecek madde listesinde, çevrimiçi olarak verilen siparişte bulunan satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-175">In the list of items for pickup, select the line from the order that was placed online.</span></span>
4. <span data-ttu-id="20a2b-176">Sipariş satırı seçiliyken, **Malzeme çek** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-176">While the order line is selected, select **Pick up**.</span></span>

    <span data-ttu-id="20a2b-177">Satır maddesi hareket ekranına eklenir ve vadesi gelen bakiye olarak **$0,00** görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="20a2b-177">The line item is added to the transaction screen, and **$0.00** is shown as the balance that is due.</span></span>

5. <span data-ttu-id="20a2b-178">**$0,00** tutarındaki vadesi gelen bakiyeyi seçin veya hareketi sonuçlandırmak için herhangi bir ödeme yöntemi seçin.</span><span class="sxs-lookup"><span data-stu-id="20a2b-178">Select the balance due of **$0.00**, or select any payment method to conclude the transaction.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="20a2b-179">Sorun giderme</span><span class="sxs-lookup"><span data-stu-id="20a2b-179">Troubleshooting</span></span>

### <a name="online-orders-that-are-retrieved-in-the-pos-have-a-non-zero-balance-due"></a><span data-ttu-id="20a2b-180">POS'ta alınan çevrimiçi siparişlerde sıfır olmayan bir bakiye bulunur</span><span class="sxs-lookup"><span data-stu-id="20a2b-180">Online orders that are retrieved in the POS have a non-zero balance due</span></span>

<span data-ttu-id="20a2b-181">Bir sipariş mağazadan teslim alma için alındığında, ödenecek bakiye 0 (sıfır) değilse, Modern POS 'un kullanıldığından ve donanım istasyonunun etkin olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="20a2b-181">When an order is retrieved for in-store pickup, if the balance due isn't 0 (zero), make sure that Modern POS is being used, and that the hardware station is active.</span></span> <span data-ttu-id="20a2b-182">Bulut POS veya iOS için Modern POS kullanılıyorsa, paylaşılan bir donanım istasyonunun etkin olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="20a2b-182">If Cloud POS or Modern POS for iOS is being used, make sure that a shared hardware station is active.</span></span> <span data-ttu-id="20a2b-183">Çevrimiçi olarak yapılan ödemeleri almak için bir çeşit etkin donanım istasyonu gerekir.</span><span class="sxs-lookup"><span data-stu-id="20a2b-183">Some form of active hardware station is required to retrieve payments that were made online.</span></span>

### <a name="general-issues-with-payment-capture"></a><span data-ttu-id="20a2b-184">Ödeme yakalamayla ilgili genel sorunlar</span><span class="sxs-lookup"><span data-stu-id="20a2b-184">General issues with payment capture</span></span>

<span data-ttu-id="20a2b-185">Tüm genel sorunlar için, her zaman öncelikle Modern POS veya İnternet Bilgi Hizmetleri (IIS) Hardware Station olay günlüklerine başvurmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="20a2b-185">For all general issues, you should always consult the Modern POS or Internet Information Services (IIS) Hardware Station event logs as a first step.</span></span> <span data-ttu-id="20a2b-186">Bu günlükleri, Windows olay günlüğünde aşağıdaki düğümlerde bulabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="20a2b-186">You can find these logs under the following nodes in the Windows event log:</span></span>

- <span data-ttu-id="20a2b-187">Uygulama ve Hizmet Günlükleri \> Microsoft \> Dynamics \> Commerce-ModernPOS</span><span class="sxs-lookup"><span data-stu-id="20a2b-187">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-ModernPOS</span></span>
- <span data-ttu-id="20a2b-188">Uygulama ve Hizmet Günlükleri \> Microsoft \> Dynamics \> Commerce-Hardware Station</span><span class="sxs-lookup"><span data-stu-id="20a2b-188">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-Hardware Station</span></span>

## <a name="additional-resources"></a><span data-ttu-id="20a2b-189">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="20a2b-189">Additional resources</span></span>

[<span data-ttu-id="20a2b-190">Dynamics 365 Commerce önizleme ortamına genel bakış</span><span class="sxs-lookup"><span data-stu-id="20a2b-190">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="20a2b-191">Dynamics 365 Commerce önizleme ortamını hazırlama</span><span class="sxs-lookup"><span data-stu-id="20a2b-191">Provision a Dynamics 365 Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="20a2b-192">Dynamics 365 Commerce önizleme ortamı için isteğe bağlı özellikleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="20a2b-192">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="20a2b-193">Dynamics 365 Commerce önizleme ortamıyla ilgili SSS</span><span class="sxs-lookup"><span data-stu-id="20a2b-193">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="20a2b-194">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="20a2b-194">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="20a2b-195">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="20a2b-195">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="20a2b-196">Microsoft Azure portalı</span><span class="sxs-lookup"><span data-stu-id="20a2b-196">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="20a2b-197">Dynamics 365 Commerce web sitesi</span><span class="sxs-lookup"><span data-stu-id="20a2b-197">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="20a2b-198">Adyen ödeme bağlayıcısı</span><span class="sxs-lookup"><span data-stu-id="20a2b-198">Adyen payment connector</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)

[<span data-ttu-id="20a2b-199">Adyen bağlayıcısı ile çevrimiçi ödeme araçlarını kaydetme</span><span class="sxs-lookup"><span data-stu-id="20a2b-199">Saving online payment instruments with the Adyen connector</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector-listpi)

[<span data-ttu-id="20a2b-200">Çok yönlü kanal ödemelerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="20a2b-200">Omni-channel payments overview</span></span>](https://docs.microsoft.com/dynamics365/commerce/omni-channel-payments)
