---
title: ER Tasarım etki alanına özel veri modeli
description: Aşağıdaki yordamda, Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının elektronik ödeme belgeleri için bir veri modeli içeren, yeni bir Elektronik Raporlama (ER) yapılandırmasını nasıl oluşturabileceği açıklanmıştır.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0debb7276c4f3e41c2e85ce6bc63b8df5bc159f8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "348423"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="49f7a-103">ER Tasarım etki alanına özel veri modeli</span><span class="sxs-lookup"><span data-stu-id="49f7a-103">ER Design domain specific data model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="49f7a-104">Aşağıdaki yordamda, Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının elektronik ödeme belgeleri için bir veri modeli içeren, yeni bir Elektronik Raporlama (ER) yapılandırmasını nasıl oluşturabileceği açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="49f7a-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="49f7a-105">Ödeme belgeleri için biçim oluşturduğunuzda, bu veri modeli daha sonra bir veri kaynağı olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="49f7a-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>



<span data-ttu-id="49f7a-106">Bu örnekte Litware, Inc. örnek şirketi için bir yapılandırma oluşturacaksınız. Bu adımlar, ER yapılandırmaları şirketler arasında paylaşımlı olduğundan herhangi bir şirkette gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="49f7a-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="49f7a-107">Bu adımları tamamlamak için, öncelikle "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="49f7a-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

1. <span data-ttu-id="49f7a-108">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="49f7a-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="49f7a-109">Örnek şirket 'Litware, Inc.' için yapılandırma sağlayıcısını seçin.</span><span class="sxs-lookup"><span data-stu-id="49f7a-109">Select the configuration provider for sample company, ‘Litware, Inc.’</span></span> <span data-ttu-id="49f7a-110">Bu yapılandırma sağlayıcısını göremiyorsanız, önce "Yapılandırma sağlayıcı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="49f7a-110">If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
2. <span data-ttu-id="49f7a-111">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-111">Click Reporting configurations.</span></span>
    * <span data-ttu-id="49f7a-112">Bir elektronik ödeme belgeleri için veri modeli içeren bir yapılandırma oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="49f7a-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="49f7a-113">Ödeme belgeleri için biçim oluşturduğunuzda, bu veri modeli daha sonra bir veri kaynağı olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="49f7a-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="49f7a-114">Yeni bir veri modeli yapılandırması oluşturun</span><span class="sxs-lookup"><span data-stu-id="49f7a-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="49f7a-115">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="49f7a-116">İsim alanında, 'Ödemeler (Basitleştirilmiş model)' yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-116">In the Name field, type 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="49f7a-117">Ödemeler (Basitleştirilmiş model)</span><span class="sxs-lookup"><span data-stu-id="49f7a-117">Payments (simplified model)</span></span>  
3. <span data-ttu-id="49f7a-118">Açıklama alanına, 'Ödeme modeli yapılandırması' yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-118">In the Description field, type 'Payment model configuration'.</span></span>
    * <span data-ttu-id="49f7a-119">Ödeme modeli konfigürasyonu</span><span class="sxs-lookup"><span data-stu-id="49f7a-119">Payment model configuration</span></span>  
    * <span data-ttu-id="49f7a-120">Etkin yapılandırma sağlayıcısı otomatik olarak buraya girilir.</span><span class="sxs-lookup"><span data-stu-id="49f7a-120">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="49f7a-121">Bu sağlayıcının, bu yapılandırmayı sürdürmesi mümkün olacaktır.</span><span class="sxs-lookup"><span data-stu-id="49f7a-121">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="49f7a-122">Diğer sağlayıcılar bu yapılandırmayı kullanabilir, ancak onu sürdüremezler.</span><span class="sxs-lookup"><span data-stu-id="49f7a-122">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
4. <span data-ttu-id="49f7a-123">Yapılandırma oluşturma görevini tamamlamak için 'Konfigürasyon oluştur' düğmesini tıklatın</span><span class="sxs-lookup"><span data-stu-id="49f7a-123">Click ‘Create configuration’ button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="49f7a-124">Bir veri modeli oluşturun</span><span class="sxs-lookup"><span data-stu-id="49f7a-124">Create a data model</span></span>
    * <span data-ttu-id="49f7a-125">Seçili yapılandırma için yeni bir veri modeli oluşturuyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="49f7a-125">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="49f7a-126">Bu yapılandırma sürümü Taslak durumuna sahip.</span><span class="sxs-lookup"><span data-stu-id="49f7a-126">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="49f7a-127">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-127">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="49f7a-128">Ödeme işlemine katılan bir tarafın yapısını tanımlama</span><span class="sxs-lookup"><span data-stu-id="49f7a-128">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="49f7a-129">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-129">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="49f7a-130">Ad alanına "Taraf" yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-130">In the Name field, type 'Party'.</span></span>
    * <span data-ttu-id="49f7a-131">Taraf</span><span class="sxs-lookup"><span data-stu-id="49f7a-131">Party</span></span>  
3. <span data-ttu-id="49f7a-132">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-132">Click Add.</span></span>
4. <span data-ttu-id="49f7a-133">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-133">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="49f7a-134">İsim alanında 'İsim' yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-134">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="49f7a-135">Dosya Adı</span><span class="sxs-lookup"><span data-stu-id="49f7a-135">Name</span></span>  
6. <span data-ttu-id="49f7a-136">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="49f7a-136">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="49f7a-137">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-137">Click Add.</span></span>
8. <span data-ttu-id="49f7a-138">Bul alanına "Taraf" yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-138">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="49f7a-139">Taraf</span><span class="sxs-lookup"><span data-stu-id="49f7a-139">Party</span></span>  
9. <span data-ttu-id="49f7a-140">Öncekini bul'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-140">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="49f7a-141">Bu model için banka yapısını tanımlama</span><span class="sxs-lookup"><span data-stu-id="49f7a-141">Define the bank structure for this model</span></span>
1. <span data-ttu-id="49f7a-142">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-142">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="49f7a-143">İsim alanına 'Agent' yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-143">In the Name field, type 'Agent'.</span></span>
    * <span data-ttu-id="49f7a-144">Temsilci</span><span class="sxs-lookup"><span data-stu-id="49f7a-144">Agent</span></span>  
3. <span data-ttu-id="49f7a-145">Madde türü alanında 'Kayıt'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="49f7a-145">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="49f7a-146">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-146">Click Add.</span></span>
5. <span data-ttu-id="49f7a-147">Açıklama alanına "Tarafa (borçlu/alacaklı) hesap sağlayan mali kurum (örneğin banka)." yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-147">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>
    * <span data-ttu-id="49f7a-148">Tarafa (borçlu/alacaklı) hesap sağlayan mali kurum (örneğin banka).</span><span class="sxs-lookup"><span data-stu-id="49f7a-148">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  
6. <span data-ttu-id="49f7a-149">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-149">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="49f7a-150">İsim alanında 'İsim' yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-150">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="49f7a-151">Dosya Adı</span><span class="sxs-lookup"><span data-stu-id="49f7a-151">Name</span></span>  
8. <span data-ttu-id="49f7a-152">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="49f7a-152">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="49f7a-153">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-153">Click Add.</span></span>
10. <span data-ttu-id="49f7a-154">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-154">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="49f7a-155">İsim alanına 'SWIFT' yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-155">In the Name field, type 'SWIFT'.</span></span>
    * <span data-ttu-id="49f7a-156">SWIFT</span><span class="sxs-lookup"><span data-stu-id="49f7a-156">SWIFT</span></span>  
12. <span data-ttu-id="49f7a-157">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-157">Click Add.</span></span>
13. <span data-ttu-id="49f7a-158">Açıklama alanına, "Banka kimlik saptama kodu" yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-158">In the Description field, enter 'Bank identification code'.</span></span>
    * <span data-ttu-id="49f7a-159">Banka kimlik saptama kodu</span><span class="sxs-lookup"><span data-stu-id="49f7a-159">Bank identification code</span></span>  
14. <span data-ttu-id="49f7a-160">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-160">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="49f7a-161">İsim alanına 'RoutingNumber' yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-161">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="49f7a-162">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="49f7a-162">RoutingNumber</span></span>  
16. <span data-ttu-id="49f7a-163">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-163">Click Add.</span></span>
17. <span data-ttu-id="49f7a-164">Açıklama alanına "Rota numarası" yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-164">In the Description field, enter 'Routing number'.</span></span>
    * <span data-ttu-id="49f7a-165">Rota numarası</span><span class="sxs-lookup"><span data-stu-id="49f7a-165">Routing number</span></span>  
18. <span data-ttu-id="49f7a-166">Öncekini bul'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-166">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="49f7a-167">Bu model için hesap yapısını tanımlama</span><span class="sxs-lookup"><span data-stu-id="49f7a-167">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="49f7a-168">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-168">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="49f7a-169">İsim alanına 'Hesap' yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-169">In the Name field, type 'Account'.</span></span>
    * <span data-ttu-id="49f7a-170">Hesap</span><span class="sxs-lookup"><span data-stu-id="49f7a-170">Account</span></span>  
3. <span data-ttu-id="49f7a-171">Madde türü alanında 'Kayıt'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="49f7a-171">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="49f7a-172">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-172">Click Add.</span></span>
5. <span data-ttu-id="49f7a-173">Açıklama alanına "Tarafın bir mali kuruluştaki (örneğin, bir banka) hesap kimliği." yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-173">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>
    * <span data-ttu-id="49f7a-174">Tarafın bir mali kuruluştaki (örneğin, bir banka) hesap kimliği.</span><span class="sxs-lookup"><span data-stu-id="49f7a-174">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  
6. <span data-ttu-id="49f7a-175">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-175">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="49f7a-176">İsim alanına 'Para birimi' yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-176">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="49f7a-177">Para birimi</span><span class="sxs-lookup"><span data-stu-id="49f7a-177">Currency</span></span>  
8. <span data-ttu-id="49f7a-178">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="49f7a-178">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="49f7a-179">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-179">Click Add.</span></span>
10. <span data-ttu-id="49f7a-180">Açıklama alanına "Para birimi kodu" yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-180">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="49f7a-181">Para birimi kodu</span><span class="sxs-lookup"><span data-stu-id="49f7a-181">Currency code</span></span>  
11. <span data-ttu-id="49f7a-182">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-182">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="49f7a-183">İsim alanına 'Numara' yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-183">In the Name field, type 'Number'.</span></span>
    * <span data-ttu-id="49f7a-184">Sayı</span><span class="sxs-lookup"><span data-stu-id="49f7a-184">Number</span></span>  
13. <span data-ttu-id="49f7a-185">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-185">Click Add.</span></span>
14. <span data-ttu-id="49f7a-186">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-186">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="49f7a-187">İsim alanına 'IBAN' yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-187">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="49f7a-188">IBAN</span><span class="sxs-lookup"><span data-stu-id="49f7a-188">IBAN</span></span>  
16. <span data-ttu-id="49f7a-189">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-189">Click Add.</span></span>
17. <span data-ttu-id="49f7a-190">Açıklama alanına, "Uluslararası banka hesap numarası" yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-190">In the Description field, enter 'International bank account number'.</span></span>
    * <span data-ttu-id="49f7a-191">Uluslararası banka hesap numarası</span><span class="sxs-lookup"><span data-stu-id="49f7a-191">International bank account number</span></span>  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="49f7a-192">Kredi transferi ödeme türü için ödeme iletisi yapısını tanımlama</span><span class="sxs-lookup"><span data-stu-id="49f7a-192">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="49f7a-193">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-193">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="49f7a-194">Yeni düğüm biçimi alanına "Model kökü" girin.</span><span class="sxs-lookup"><span data-stu-id="49f7a-194">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="49f7a-195">İsim alanında 'CustomerCreditTransferInitiation' yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-195">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="49f7a-196">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="49f7a-196">CustomerCreditTransferInitiation</span></span>  
4. <span data-ttu-id="49f7a-197">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-197">Click Add.</span></span>
5. <span data-ttu-id="49f7a-198">Bul alanına "CustomerCreditTransferInitiation" yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-198">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="49f7a-199">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="49f7a-199">CustomerCreditTransferInitiation</span></span>  
6. <span data-ttu-id="49f7a-200">Öncekini bul'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-200">Click Find previous.</span></span>
7. <span data-ttu-id="49f7a-201">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-201">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="49f7a-202">İsim alanına 'MessageIdentification' yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-202">In the Name field, type 'MessageIdentification'.</span></span>
    * <span data-ttu-id="49f7a-203">MessageIdentification</span><span class="sxs-lookup"><span data-stu-id="49f7a-203">MessageIdentification</span></span>  
9. <span data-ttu-id="49f7a-204">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-204">Click Add.</span></span>
10. <span data-ttu-id="49f7a-205">Açıklama alanına "Bir iletinin kimliğini belirlemek için talimatı veren tarafça atanan noktadan noktaya referans." yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-205">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>
    * <span data-ttu-id="49f7a-206">Bir iletinin kimliğini belirlemek için talimatı veren tarafça atanan noktadan noktaya referans.</span><span class="sxs-lookup"><span data-stu-id="49f7a-206">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  
11. <span data-ttu-id="49f7a-207">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-207">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="49f7a-208">İsim alanına 'ProcessingDateTime' yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-208">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="49f7a-209">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="49f7a-209">ProcessingDateTime</span></span>  
13. <span data-ttu-id="49f7a-210">Madde türü alanında 'DateTime' seçin.</span><span class="sxs-lookup"><span data-stu-id="49f7a-210">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="49f7a-211">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-211">Click Add.</span></span>
15. <span data-ttu-id="49f7a-212">Açıklama alanına, "Ödeme iletisinin oluşturulduğu tarih ve saat." yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-212">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span>
    * <span data-ttu-id="49f7a-213">Ödeme iletisinin oluşturulduğu tarih ve saat.</span><span class="sxs-lookup"><span data-stu-id="49f7a-213">Date and time at which the payment message was created.</span></span>  
16. <span data-ttu-id="49f7a-214">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-214">Click New to open the drop dialog.</span></span>
    * <span data-ttu-id="49f7a-215">Bu model için ödeme hareketi yapısını tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-215">Define the payment transaction structure for this model.</span></span>  
17. <span data-ttu-id="49f7a-216">İsim alanına 'Ödemeler' yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-216">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="49f7a-217">Ödemeler</span><span class="sxs-lookup"><span data-stu-id="49f7a-217">Payments</span></span>  
18. <span data-ttu-id="49f7a-218">Madde türü alanında 'Kayıt listesi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="49f7a-218">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="49f7a-219">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-219">Click Add.</span></span>
20. <span data-ttu-id="49f7a-220">Açıklama alanına, 'Geçerli iletinin ödeme satırları' girin.</span><span class="sxs-lookup"><span data-stu-id="49f7a-220">In the Description field, enter 'Payment lines of the current message'.</span></span>
    * <span data-ttu-id="49f7a-221">Geçerli iletinin ödeme satırları</span><span class="sxs-lookup"><span data-stu-id="49f7a-221">Payment lines of the current message</span></span>  
21. <span data-ttu-id="49f7a-222">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-222">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="49f7a-223">İsim alanına 'Alacaklı' yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-223">In the Name field, type 'Creditor'.</span></span>
    * <span data-ttu-id="49f7a-224">Alacaklı</span><span class="sxs-lookup"><span data-stu-id="49f7a-224">Creditor</span></span>  
23. <span data-ttu-id="49f7a-225">Madde türü alanında 'Kayıt'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="49f7a-225">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="49f7a-226">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-226">Click Add.</span></span>
25. <span data-ttu-id="49f7a-227">Açıklama alanına "Belli bir tutardaki paranın ödenmesi gereken taraf." yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-227">In the Description field, enter 'Party to which an amount of money is due.'.</span></span>
    * <span data-ttu-id="49f7a-228">Belli bir tutardaki paranın ödenmesi gereken taraf.</span><span class="sxs-lookup"><span data-stu-id="49f7a-228">Party to which an amount of money is due.</span></span>  
26. <span data-ttu-id="49f7a-229">Madde referansını değiştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-229">Click Switch item reference.</span></span>
27. <span data-ttu-id="49f7a-230">Bul alanına "Taraf" yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-230">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="49f7a-231">Taraf</span><span class="sxs-lookup"><span data-stu-id="49f7a-231">Party</span></span>  
28. <span data-ttu-id="49f7a-232">Sonrakini bul'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-232">Click Find next.</span></span>
29. <span data-ttu-id="49f7a-233">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-233">Click OK.</span></span>
30. <span data-ttu-id="49f7a-234">Bul alanına "Ödemeler" yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-234">In the Find field, type 'Payments'.</span></span>
    * <span data-ttu-id="49f7a-235">Ödemeler</span><span class="sxs-lookup"><span data-stu-id="49f7a-235">Payments</span></span>  
31. <span data-ttu-id="49f7a-236">Sonrakini bul'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-236">Click Find next.</span></span>
32. <span data-ttu-id="49f7a-237">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-237">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="49f7a-238">İsim alanına 'Borçlu' yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-238">In the Name field, type 'Debtor'.</span></span>
    * <span data-ttu-id="49f7a-239">Borçlu</span><span class="sxs-lookup"><span data-stu-id="49f7a-239">Debtor</span></span>  
34. <span data-ttu-id="49f7a-240">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-240">Click Add.</span></span>
35. <span data-ttu-id="49f7a-241">Açıklama alanına "Alacaklıya (son) belli bir tutarda para borçlu olan taraf." yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-241">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
    * <span data-ttu-id="49f7a-242">Alacaklıya (son) belli bir tutarda para borçlu olan taraf.</span><span class="sxs-lookup"><span data-stu-id="49f7a-242">Party that owes an amount of money to the (ultimate) creditor.</span></span>  
36. <span data-ttu-id="49f7a-243">Madde referansını değiştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-243">Click Switch item reference.</span></span>
37. <span data-ttu-id="49f7a-244">Bul alanına "Taraf" yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-244">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="49f7a-245">Taraf</span><span class="sxs-lookup"><span data-stu-id="49f7a-245">Party</span></span>  
38. <span data-ttu-id="49f7a-246">Sonrakini bul'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-246">Click Find next.</span></span>
39. <span data-ttu-id="49f7a-247">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-247">Click OK.</span></span>
40. <span data-ttu-id="49f7a-248">Sonrakini bul'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-248">Click Find next.</span></span>
41. <span data-ttu-id="49f7a-249">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-249">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="49f7a-250">İsim alanına 'Açıklama' yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-250">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="49f7a-251">Açıklama</span><span class="sxs-lookup"><span data-stu-id="49f7a-251">Description</span></span>  
43. <span data-ttu-id="49f7a-252">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="49f7a-252">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="49f7a-253">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-253">Click Add.</span></span>
45. <span data-ttu-id="49f7a-254">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-254">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="49f7a-255">İsim alanına 'Para birimi' yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-255">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="49f7a-256">Para birimi</span><span class="sxs-lookup"><span data-stu-id="49f7a-256">Currency</span></span>  
47. <span data-ttu-id="49f7a-257">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-257">Click Add.</span></span>
48. <span data-ttu-id="49f7a-258">Açıklama alanına "Para birimi kodu" yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-258">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="49f7a-259">Para birimi kodu</span><span class="sxs-lookup"><span data-stu-id="49f7a-259">Currency code</span></span>  
49. <span data-ttu-id="49f7a-260">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-260">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="49f7a-261">İsim alanına, 'TransactionDate' yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-261">In the Name field, type 'TransactionDate'.</span></span>
    * <span data-ttu-id="49f7a-262">TransactionDate</span><span class="sxs-lookup"><span data-stu-id="49f7a-262">TransactionDate</span></span>  
51. <span data-ttu-id="49f7a-263">Madde türü alanında 'Tarih' seçin.</span><span class="sxs-lookup"><span data-stu-id="49f7a-263">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="49f7a-264">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-264">Click Add.</span></span>
53. <span data-ttu-id="49f7a-265">Açıklama alanına, "Hareket tarihi" yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-265">In the Description field, enter 'Transaction date'.</span></span>
    * <span data-ttu-id="49f7a-266">Hareket tarihi</span><span class="sxs-lookup"><span data-stu-id="49f7a-266">Transaction date</span></span>  
54. <span data-ttu-id="49f7a-267">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-267">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="49f7a-268">İsim alanına 'InstructedAmount' yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-268">In the Name field, type 'InstructedAmount'.</span></span>
    * <span data-ttu-id="49f7a-269">InstructedAmount</span><span class="sxs-lookup"><span data-stu-id="49f7a-269">InstructedAmount</span></span>  
56. <span data-ttu-id="49f7a-270">Madde türü alanında 'Gerçek' seçin.</span><span class="sxs-lookup"><span data-stu-id="49f7a-270">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="49f7a-271">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-271">Click Add.</span></span>
58. <span data-ttu-id="49f7a-272">Açıklama alanına "Masraflar düşülmeden önce, borçlu ve alacaklı arasında taşınacak olan para tutarı" yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-272">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="49f7a-273">Tutar, başlatan tarafın sipariş ettiği para birimi cinsinden ifade edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="49f7a-273">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>
    * <span data-ttu-id="49f7a-274">Tasraflar düşülmeden önce, borçlu ve alacaklı arasında taşınacak olan para tutarı.</span><span class="sxs-lookup"><span data-stu-id="49f7a-274">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="49f7a-275">Tutar, başlatan tarafın sipariş ettiği para birimi cinsinden ifade edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="49f7a-275">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  
59. <span data-ttu-id="49f7a-276">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-276">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="49f7a-277">İsim alanına 'End2EndID' yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-277">In the Name field, type 'End2EndID'.</span></span>
    * <span data-ttu-id="49f7a-278">End2EndID</span><span class="sxs-lookup"><span data-stu-id="49f7a-278">End2EndID</span></span>  
61. <span data-ttu-id="49f7a-279">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="49f7a-279">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="49f7a-280">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-280">Click Add.</span></span>
63. <span data-ttu-id="49f7a-281">Açıklama alanına "Başlatan tarafça atanan benzersiz kimlik" yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-281">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="49f7a-282">Bu kimlik, tüm uçtan uca zinciri boyunca değişmeden geçirilir.</span><span class="sxs-lookup"><span data-stu-id="49f7a-282">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span>
    * <span data-ttu-id="49f7a-283">Başlatan tarafça atanan benzersiz kimlik.</span><span class="sxs-lookup"><span data-stu-id="49f7a-283">The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="49f7a-284">Bu kimlik, tüm uçtan uca zinciri boyunca değişmeden geçirilir.</span><span class="sxs-lookup"><span data-stu-id="49f7a-284">This identification is passed on, unchanged, throughout the entire end-to-end chain.</span></span>  
64. <span data-ttu-id="49f7a-285">İsim alanında 'PaymentModel' yazın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-285">In the Name field, type 'PaymentModel'.</span></span>
    * <span data-ttu-id="49f7a-286">PaymentModel adı önceden tanımlanmış ödeme formları arabirimleriyle hizalanır.</span><span class="sxs-lookup"><span data-stu-id="49f7a-286">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  
65. <span data-ttu-id="49f7a-287">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-287">Click Save.</span></span>
66. <span data-ttu-id="49f7a-288">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="49f7a-288">Close the page.</span></span>

