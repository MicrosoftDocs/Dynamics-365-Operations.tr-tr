--- 
title: "ER Tasarım etki alanına özel veri modeli"
description: "Aşağıdaki yordamda, Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının elektronik ödeme belgeleri için bir veri modeli içeren, yeni bir Elektronik Raporlama (ER) yapılandırmasını nasıl oluşturabileceği açıklanmıştır."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 0debb7276c4f3e41c2e85ce6bc63b8df5bc159f8
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="e47a2-103">ER Tasarım etki alanına özel veri modeli</span><span class="sxs-lookup"><span data-stu-id="e47a2-103">ER Design domain specific data model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e47a2-104">Aşağıdaki yordamda, Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının elektronik ödeme belgeleri için bir veri modeli içeren, yeni bir Elektronik Raporlama (ER) yapılandırmasını nasıl oluşturabileceği açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="e47a2-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="e47a2-105">Ödeme belgeleri için biçim oluşturduğunuzda, bu veri modeli daha sonra bir veri kaynağı olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e47a2-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>



<span data-ttu-id="e47a2-106">Bu örnekte Litware, Inc. örnek şirketi için bir yapılandırma oluşturacaksınız. Bu adımlar, ER yapılandırmaları şirketler arasında paylaşımlı olduğundan herhangi bir şirkette gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="e47a2-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="e47a2-107">Bu adımları tamamlamak için, öncelikle "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e47a2-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

1. <span data-ttu-id="e47a2-108">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="e47a2-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="e47a2-109">Örnek şirket 'Litware, Inc.' için yapılandırma sağlayıcısını seçin.</span><span class="sxs-lookup"><span data-stu-id="e47a2-109">Select the configuration provider for sample company, ‘Litware, Inc.’</span></span> <span data-ttu-id="e47a2-110">Bu yapılandırma sağlayıcısını göremiyorsanız, önce "Yapılandırma sağlayıcı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="e47a2-110">If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
2. <span data-ttu-id="e47a2-111">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-111">Click Reporting configurations.</span></span>
    * <span data-ttu-id="e47a2-112">Bir elektronik ödeme belgeleri için veri modeli içeren bir yapılandırma oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="e47a2-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="e47a2-113">Ödeme belgeleri için biçim oluşturduğunuzda, bu veri modeli daha sonra bir veri kaynağı olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e47a2-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="e47a2-114">Yeni bir veri modeli yapılandırması oluşturun</span><span class="sxs-lookup"><span data-stu-id="e47a2-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="e47a2-115">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="e47a2-116">İsim alanında, 'Ödemeler (Basitleştirilmiş model)' yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-116">In the Name field, type 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="e47a2-117">Ödemeler (Basitleştirilmiş model)</span><span class="sxs-lookup"><span data-stu-id="e47a2-117">Payments (simplified model)</span></span>  
3. <span data-ttu-id="e47a2-118">Açıklama alanına, 'Ödeme modeli yapılandırması' yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-118">In the Description field, type 'Payment model configuration'.</span></span>
    * <span data-ttu-id="e47a2-119">Ödeme modeli konfigürasyonu</span><span class="sxs-lookup"><span data-stu-id="e47a2-119">Payment model configuration</span></span>  
    * <span data-ttu-id="e47a2-120">Etkin yapılandırma sağlayıcısı otomatik olarak buraya girilir.</span><span class="sxs-lookup"><span data-stu-id="e47a2-120">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="e47a2-121">Bu sağlayıcının, bu yapılandırmayı sürdürmesi mümkün olacaktır.</span><span class="sxs-lookup"><span data-stu-id="e47a2-121">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="e47a2-122">Diğer sağlayıcılar bu yapılandırmayı kullanabilir, ancak onu sürdüremezler.</span><span class="sxs-lookup"><span data-stu-id="e47a2-122">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
4. <span data-ttu-id="e47a2-123">Yapılandırma oluşturma görevini tamamlamak için 'Konfigürasyon oluştur' düğmesini tıklatın</span><span class="sxs-lookup"><span data-stu-id="e47a2-123">Click ‘Create configuration’ button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="e47a2-124">Bir veri modeli oluşturun</span><span class="sxs-lookup"><span data-stu-id="e47a2-124">Create a data model</span></span>
    * <span data-ttu-id="e47a2-125">Seçili yapılandırma için yeni bir veri modeli oluşturuyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="e47a2-125">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="e47a2-126">Bu yapılandırma sürümü Taslak durumuna sahip.</span><span class="sxs-lookup"><span data-stu-id="e47a2-126">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="e47a2-127">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-127">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="e47a2-128">Ödeme işlemine katılan bir tarafın yapısını tanımlama</span><span class="sxs-lookup"><span data-stu-id="e47a2-128">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="e47a2-129">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-129">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="e47a2-130">Ad alanına "Taraf" yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-130">In the Name field, type 'Party'.</span></span>
    * <span data-ttu-id="e47a2-131">Taraf</span><span class="sxs-lookup"><span data-stu-id="e47a2-131">Party</span></span>  
3. <span data-ttu-id="e47a2-132">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-132">Click Add.</span></span>
4. <span data-ttu-id="e47a2-133">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-133">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="e47a2-134">İsim alanında 'İsim' yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-134">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="e47a2-135">Dosya Adı</span><span class="sxs-lookup"><span data-stu-id="e47a2-135">Name</span></span>  
6. <span data-ttu-id="e47a2-136">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="e47a2-136">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="e47a2-137">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-137">Click Add.</span></span>
8. <span data-ttu-id="e47a2-138">Bul alanına "Taraf" yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-138">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="e47a2-139">Taraf</span><span class="sxs-lookup"><span data-stu-id="e47a2-139">Party</span></span>  
9. <span data-ttu-id="e47a2-140">Öncekini bul'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-140">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="e47a2-141">Bu model için banka yapısını tanımlama</span><span class="sxs-lookup"><span data-stu-id="e47a2-141">Define the bank structure for this model</span></span>
1. <span data-ttu-id="e47a2-142">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-142">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="e47a2-143">İsim alanına 'Agent' yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-143">In the Name field, type 'Agent'.</span></span>
    * <span data-ttu-id="e47a2-144">Temsilci</span><span class="sxs-lookup"><span data-stu-id="e47a2-144">Agent</span></span>  
3. <span data-ttu-id="e47a2-145">Madde türü alanında 'Kayıt'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e47a2-145">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="e47a2-146">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-146">Click Add.</span></span>
5. <span data-ttu-id="e47a2-147">Açıklama alanına "Tarafa (borçlu/alacaklı) hesap sağlayan mali kurum (örneğin banka)." yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-147">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>
    * <span data-ttu-id="e47a2-148">Tarafa (borçlu/alacaklı) hesap sağlayan mali kurum (örneğin banka).</span><span class="sxs-lookup"><span data-stu-id="e47a2-148">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  
6. <span data-ttu-id="e47a2-149">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-149">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="e47a2-150">İsim alanında 'İsim' yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-150">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="e47a2-151">Dosya Adı</span><span class="sxs-lookup"><span data-stu-id="e47a2-151">Name</span></span>  
8. <span data-ttu-id="e47a2-152">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="e47a2-152">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="e47a2-153">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-153">Click Add.</span></span>
10. <span data-ttu-id="e47a2-154">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-154">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="e47a2-155">İsim alanına 'SWIFT' yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-155">In the Name field, type 'SWIFT'.</span></span>
    * <span data-ttu-id="e47a2-156">SWIFT</span><span class="sxs-lookup"><span data-stu-id="e47a2-156">SWIFT</span></span>  
12. <span data-ttu-id="e47a2-157">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-157">Click Add.</span></span>
13. <span data-ttu-id="e47a2-158">Açıklama alanına, "Banka kimlik saptama kodu" yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-158">In the Description field, enter 'Bank identification code'.</span></span>
    * <span data-ttu-id="e47a2-159">Banka kimlik saptama kodu</span><span class="sxs-lookup"><span data-stu-id="e47a2-159">Bank identification code</span></span>  
14. <span data-ttu-id="e47a2-160">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-160">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="e47a2-161">İsim alanına 'RoutingNumber' yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-161">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="e47a2-162">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="e47a2-162">RoutingNumber</span></span>  
16. <span data-ttu-id="e47a2-163">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-163">Click Add.</span></span>
17. <span data-ttu-id="e47a2-164">Açıklama alanına "Rota numarası" yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-164">In the Description field, enter 'Routing number'.</span></span>
    * <span data-ttu-id="e47a2-165">Rota numarası</span><span class="sxs-lookup"><span data-stu-id="e47a2-165">Routing number</span></span>  
18. <span data-ttu-id="e47a2-166">Öncekini bul'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-166">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="e47a2-167">Bu model için hesap yapısını tanımlama</span><span class="sxs-lookup"><span data-stu-id="e47a2-167">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="e47a2-168">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-168">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="e47a2-169">İsim alanına 'Hesap' yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-169">In the Name field, type 'Account'.</span></span>
    * <span data-ttu-id="e47a2-170">Hesap</span><span class="sxs-lookup"><span data-stu-id="e47a2-170">Account</span></span>  
3. <span data-ttu-id="e47a2-171">Madde türü alanında 'Kayıt'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e47a2-171">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="e47a2-172">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-172">Click Add.</span></span>
5. <span data-ttu-id="e47a2-173">Açıklama alanına "Tarafın bir mali kuruluştaki (örneğin, bir banka) hesap kimliği." yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-173">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>
    * <span data-ttu-id="e47a2-174">Tarafın bir mali kuruluştaki (örneğin, bir banka) hesap kimliği.</span><span class="sxs-lookup"><span data-stu-id="e47a2-174">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  
6. <span data-ttu-id="e47a2-175">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-175">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="e47a2-176">İsim alanına 'Para birimi' yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-176">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="e47a2-177">Para birimi</span><span class="sxs-lookup"><span data-stu-id="e47a2-177">Currency</span></span>  
8. <span data-ttu-id="e47a2-178">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="e47a2-178">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="e47a2-179">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-179">Click Add.</span></span>
10. <span data-ttu-id="e47a2-180">Açıklama alanına "Para birimi kodu" yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-180">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="e47a2-181">Para birimi kodu</span><span class="sxs-lookup"><span data-stu-id="e47a2-181">Currency code</span></span>  
11. <span data-ttu-id="e47a2-182">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-182">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="e47a2-183">İsim alanına 'Numara' yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-183">In the Name field, type 'Number'.</span></span>
    * <span data-ttu-id="e47a2-184">Sayı</span><span class="sxs-lookup"><span data-stu-id="e47a2-184">Number</span></span>  
13. <span data-ttu-id="e47a2-185">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-185">Click Add.</span></span>
14. <span data-ttu-id="e47a2-186">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-186">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="e47a2-187">İsim alanına 'IBAN' yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-187">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="e47a2-188">IBAN</span><span class="sxs-lookup"><span data-stu-id="e47a2-188">IBAN</span></span>  
16. <span data-ttu-id="e47a2-189">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-189">Click Add.</span></span>
17. <span data-ttu-id="e47a2-190">Açıklama alanına, "Uluslararası banka hesap numarası" yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-190">In the Description field, enter 'International bank account number'.</span></span>
    * <span data-ttu-id="e47a2-191">Uluslararası banka hesap numarası</span><span class="sxs-lookup"><span data-stu-id="e47a2-191">International bank account number</span></span>  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="e47a2-192">Kredi transferi ödeme türü için ödeme iletisi yapısını tanımlama</span><span class="sxs-lookup"><span data-stu-id="e47a2-192">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="e47a2-193">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-193">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="e47a2-194">Yeni düğüm biçimi alanına "Model kökü" girin.</span><span class="sxs-lookup"><span data-stu-id="e47a2-194">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="e47a2-195">İsim alanında 'CustomerCreditTransferInitiation' yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-195">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="e47a2-196">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="e47a2-196">CustomerCreditTransferInitiation</span></span>  
4. <span data-ttu-id="e47a2-197">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-197">Click Add.</span></span>
5. <span data-ttu-id="e47a2-198">Bul alanına "CustomerCreditTransferInitiation" yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-198">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="e47a2-199">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="e47a2-199">CustomerCreditTransferInitiation</span></span>  
6. <span data-ttu-id="e47a2-200">Öncekini bul'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-200">Click Find previous.</span></span>
7. <span data-ttu-id="e47a2-201">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-201">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="e47a2-202">İsim alanına 'MessageIdentification' yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-202">In the Name field, type 'MessageIdentification'.</span></span>
    * <span data-ttu-id="e47a2-203">MessageIdentification</span><span class="sxs-lookup"><span data-stu-id="e47a2-203">MessageIdentification</span></span>  
9. <span data-ttu-id="e47a2-204">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-204">Click Add.</span></span>
10. <span data-ttu-id="e47a2-205">Açıklama alanına "Bir iletinin kimliğini belirlemek için talimatı veren tarafça atanan noktadan noktaya referans." yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-205">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>
    * <span data-ttu-id="e47a2-206">Bir iletinin kimliğini belirlemek için talimatı veren tarafça atanan noktadan noktaya referans.</span><span class="sxs-lookup"><span data-stu-id="e47a2-206">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  
11. <span data-ttu-id="e47a2-207">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-207">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="e47a2-208">İsim alanına 'ProcessingDateTime' yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-208">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="e47a2-209">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="e47a2-209">ProcessingDateTime</span></span>  
13. <span data-ttu-id="e47a2-210">Madde türü alanında 'DateTime' seçin.</span><span class="sxs-lookup"><span data-stu-id="e47a2-210">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="e47a2-211">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-211">Click Add.</span></span>
15. <span data-ttu-id="e47a2-212">Açıklama alanına, "Ödeme iletisinin oluşturulduğu tarih ve saat." yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-212">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span>
    * <span data-ttu-id="e47a2-213">Ödeme iletisinin oluşturulduğu tarih ve saat.</span><span class="sxs-lookup"><span data-stu-id="e47a2-213">Date and time at which the payment message was created.</span></span>  
16. <span data-ttu-id="e47a2-214">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-214">Click New to open the drop dialog.</span></span>
    * <span data-ttu-id="e47a2-215">Bu model için ödeme hareketi yapısını tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-215">Define the payment transaction structure for this model.</span></span>  
17. <span data-ttu-id="e47a2-216">İsim alanına 'Ödemeler' yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-216">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="e47a2-217">Ödemeler</span><span class="sxs-lookup"><span data-stu-id="e47a2-217">Payments</span></span>  
18. <span data-ttu-id="e47a2-218">Madde türü alanında 'Kayıt listesi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="e47a2-218">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="e47a2-219">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-219">Click Add.</span></span>
20. <span data-ttu-id="e47a2-220">Açıklama alanına, 'Geçerli iletinin ödeme satırları' girin.</span><span class="sxs-lookup"><span data-stu-id="e47a2-220">In the Description field, enter 'Payment lines of the current message'.</span></span>
    * <span data-ttu-id="e47a2-221">Geçerli iletinin ödeme satırları</span><span class="sxs-lookup"><span data-stu-id="e47a2-221">Payment lines of the current message</span></span>  
21. <span data-ttu-id="e47a2-222">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-222">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="e47a2-223">İsim alanına 'Alacaklı' yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-223">In the Name field, type 'Creditor'.</span></span>
    * <span data-ttu-id="e47a2-224">Alacaklı</span><span class="sxs-lookup"><span data-stu-id="e47a2-224">Creditor</span></span>  
23. <span data-ttu-id="e47a2-225">Madde türü alanında 'Kayıt'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e47a2-225">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="e47a2-226">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-226">Click Add.</span></span>
25. <span data-ttu-id="e47a2-227">Açıklama alanına "Belli bir tutardaki paranın ödenmesi gereken taraf." yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-227">In the Description field, enter 'Party to which an amount of money is due.'.</span></span>
    * <span data-ttu-id="e47a2-228">Belli bir tutardaki paranın ödenmesi gereken taraf.</span><span class="sxs-lookup"><span data-stu-id="e47a2-228">Party to which an amount of money is due.</span></span>  
26. <span data-ttu-id="e47a2-229">Madde referansını değiştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-229">Click Switch item reference.</span></span>
27. <span data-ttu-id="e47a2-230">Bul alanına "Taraf" yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-230">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="e47a2-231">Taraf</span><span class="sxs-lookup"><span data-stu-id="e47a2-231">Party</span></span>  
28. <span data-ttu-id="e47a2-232">Sonrakini bul'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-232">Click Find next.</span></span>
29. <span data-ttu-id="e47a2-233">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-233">Click OK.</span></span>
30. <span data-ttu-id="e47a2-234">Bul alanına "Ödemeler" yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-234">In the Find field, type 'Payments'.</span></span>
    * <span data-ttu-id="e47a2-235">Ödemeler</span><span class="sxs-lookup"><span data-stu-id="e47a2-235">Payments</span></span>  
31. <span data-ttu-id="e47a2-236">Sonrakini bul'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-236">Click Find next.</span></span>
32. <span data-ttu-id="e47a2-237">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-237">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="e47a2-238">İsim alanına 'Borçlu' yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-238">In the Name field, type 'Debtor'.</span></span>
    * <span data-ttu-id="e47a2-239">Borçlu</span><span class="sxs-lookup"><span data-stu-id="e47a2-239">Debtor</span></span>  
34. <span data-ttu-id="e47a2-240">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-240">Click Add.</span></span>
35. <span data-ttu-id="e47a2-241">Açıklama alanına "Alacaklıya (son) belli bir tutarda para borçlu olan taraf." yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-241">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
    * <span data-ttu-id="e47a2-242">Alacaklıya (son) belli bir tutarda para borçlu olan taraf.</span><span class="sxs-lookup"><span data-stu-id="e47a2-242">Party that owes an amount of money to the (ultimate) creditor.</span></span>  
36. <span data-ttu-id="e47a2-243">Madde referansını değiştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-243">Click Switch item reference.</span></span>
37. <span data-ttu-id="e47a2-244">Bul alanına "Taraf" yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-244">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="e47a2-245">Taraf</span><span class="sxs-lookup"><span data-stu-id="e47a2-245">Party</span></span>  
38. <span data-ttu-id="e47a2-246">Sonrakini bul'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-246">Click Find next.</span></span>
39. <span data-ttu-id="e47a2-247">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-247">Click OK.</span></span>
40. <span data-ttu-id="e47a2-248">Sonrakini bul'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-248">Click Find next.</span></span>
41. <span data-ttu-id="e47a2-249">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-249">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="e47a2-250">İsim alanına 'Açıklama' yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-250">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="e47a2-251">Açıklama</span><span class="sxs-lookup"><span data-stu-id="e47a2-251">Description</span></span>  
43. <span data-ttu-id="e47a2-252">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="e47a2-252">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="e47a2-253">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-253">Click Add.</span></span>
45. <span data-ttu-id="e47a2-254">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-254">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="e47a2-255">İsim alanına 'Para birimi' yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-255">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="e47a2-256">Para birimi</span><span class="sxs-lookup"><span data-stu-id="e47a2-256">Currency</span></span>  
47. <span data-ttu-id="e47a2-257">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-257">Click Add.</span></span>
48. <span data-ttu-id="e47a2-258">Açıklama alanına "Para birimi kodu" yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-258">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="e47a2-259">Para birimi kodu</span><span class="sxs-lookup"><span data-stu-id="e47a2-259">Currency code</span></span>  
49. <span data-ttu-id="e47a2-260">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-260">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="e47a2-261">İsim alanına, 'TransactionDate' yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-261">In the Name field, type 'TransactionDate'.</span></span>
    * <span data-ttu-id="e47a2-262">TransactionDate</span><span class="sxs-lookup"><span data-stu-id="e47a2-262">TransactionDate</span></span>  
51. <span data-ttu-id="e47a2-263">Madde türü alanında 'Tarih' seçin.</span><span class="sxs-lookup"><span data-stu-id="e47a2-263">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="e47a2-264">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-264">Click Add.</span></span>
53. <span data-ttu-id="e47a2-265">Açıklama alanına, "Hareket tarihi" yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-265">In the Description field, enter 'Transaction date'.</span></span>
    * <span data-ttu-id="e47a2-266">Hareket tarihi</span><span class="sxs-lookup"><span data-stu-id="e47a2-266">Transaction date</span></span>  
54. <span data-ttu-id="e47a2-267">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-267">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="e47a2-268">İsim alanına 'InstructedAmount' yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-268">In the Name field, type 'InstructedAmount'.</span></span>
    * <span data-ttu-id="e47a2-269">InstructedAmount</span><span class="sxs-lookup"><span data-stu-id="e47a2-269">InstructedAmount</span></span>  
56. <span data-ttu-id="e47a2-270">Madde türü alanında 'Gerçek' seçin.</span><span class="sxs-lookup"><span data-stu-id="e47a2-270">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="e47a2-271">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-271">Click Add.</span></span>
58. <span data-ttu-id="e47a2-272">Açıklama alanına "Masraflar düşülmeden önce, borçlu ve alacaklı arasında taşınacak olan para tutarı" yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-272">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="e47a2-273">Tutar, başlatan tarafın sipariş ettiği para birimi cinsinden ifade edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="e47a2-273">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>
    * <span data-ttu-id="e47a2-274">Tasraflar düşülmeden önce, borçlu ve alacaklı arasında taşınacak olan para tutarı.</span><span class="sxs-lookup"><span data-stu-id="e47a2-274">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="e47a2-275">Tutar, başlatan tarafın sipariş ettiği para birimi cinsinden ifade edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="e47a2-275">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  
59. <span data-ttu-id="e47a2-276">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-276">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="e47a2-277">İsim alanına 'End2EndID' yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-277">In the Name field, type 'End2EndID'.</span></span>
    * <span data-ttu-id="e47a2-278">End2EndID</span><span class="sxs-lookup"><span data-stu-id="e47a2-278">End2EndID</span></span>  
61. <span data-ttu-id="e47a2-279">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="e47a2-279">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="e47a2-280">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-280">Click Add.</span></span>
63. <span data-ttu-id="e47a2-281">Açıklama alanına "Başlatan tarafça atanan benzersiz kimlik" yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-281">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="e47a2-282">Bu kimlik, tüm uçtan uca zinciri boyunca değişmeden geçirilir.</span><span class="sxs-lookup"><span data-stu-id="e47a2-282">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span>
    * <span data-ttu-id="e47a2-283">Başlatan tarafça atanan benzersiz kimlik.</span><span class="sxs-lookup"><span data-stu-id="e47a2-283">The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="e47a2-284">Bu kimlik, tüm uçtan uca zinciri boyunca değişmeden geçirilir.</span><span class="sxs-lookup"><span data-stu-id="e47a2-284">This identification is passed on, unchanged, throughout the entire end-to-end chain.</span></span>  
64. <span data-ttu-id="e47a2-285">İsim alanında 'PaymentModel' yazın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-285">In the Name field, type 'PaymentModel'.</span></span>
    * <span data-ttu-id="e47a2-286">PaymentModel adı önceden tanımlanmış ödeme formları arabirimleriyle hizalanır.</span><span class="sxs-lookup"><span data-stu-id="e47a2-286">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  
65. <span data-ttu-id="e47a2-287">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-287">Click Save.</span></span>
66. <span data-ttu-id="e47a2-288">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e47a2-288">Close the page.</span></span>


