---
title: ER Tasarım etki alanına özel veri modeli
description: Bu konuda, elektronik ödeme belgeleri için bir veri modeli içeren yeni bir Elektronik raporlama (ER) yapılandırmasının nasıl oluşturulacağı açıklanmaktadır.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 284fad8b6646c35217789cc9936cbe9fe75a03d0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567822"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="03aec-103">ER Tasarım etki alanına özel veri modeli</span><span class="sxs-lookup"><span data-stu-id="03aec-103">ER Design domain specific data model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="03aec-104">Aşağıdaki yordamda, Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının elektronik ödeme belgeleri için bir veri modeli içeren, yeni bir Elektronik Raporlama (ER) yapılandırmasını nasıl oluşturabileceği açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="03aec-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="03aec-105">Ödeme belgeleri için biçim oluşturduğunuzda, bu veri modeli daha sonra bir veri kaynağı olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="03aec-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>

<span data-ttu-id="03aec-106">Bu örnekte Litware, Inc. örnek şirketi için bir yapılandırma oluşturacaksınız. Bu adımlar, ER yapılandırmaları şirketler arasında paylaşımlı olduğundan herhangi bir şirkette gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="03aec-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="03aec-107">Bu adımları tamamlamak için öncelikle "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="03aec-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

1. <span data-ttu-id="03aec-108">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="03aec-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="03aec-109">Örnek şirket 'Litware, Inc.' için yapılandırma sağlayıcısını seçin.</span><span class="sxs-lookup"><span data-stu-id="03aec-109">Select the configuration provider for sample company, 'Litware, Inc.'</span></span> <span data-ttu-id="03aec-110">Bu yapılandırma sağlayıcısını göremiyorsanız öncelikle "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="03aec-110">If you don't see this configuration provider, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>  
    
2. <span data-ttu-id="03aec-111">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-111">Click Reporting configurations.</span></span>

    <span data-ttu-id="03aec-112">Bir elektronik ödeme belgeleri için veri modeli içeren bir yapılandırma oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="03aec-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="03aec-113">Ödeme belgeleri için biçim oluşturduğunuzda, bu veri modeli daha sonra bir veri kaynağı olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="03aec-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="03aec-114">Yeni bir veri modeli yapılandırması oluşturun</span><span class="sxs-lookup"><span data-stu-id="03aec-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="03aec-115">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="03aec-116">İsim alanında, 'Ödemeler (Basitleştirilmiş model)' yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-116">In the Name field, type 'Payments (simplified model)'.</span></span>
3. <span data-ttu-id="03aec-117">Açıklama alanına, 'Ödeme modeli yapılandırması' yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-117">In the Description field, type 'Payment model configuration'.</span></span>

    <span data-ttu-id="03aec-118">Etkin yapılandırma sağlayıcısı otomatik olarak buraya girilir.</span><span class="sxs-lookup"><span data-stu-id="03aec-118">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="03aec-119">Bu sağlayıcının, bu yapılandırmayı sürdürmesi mümkün olacaktır.</span><span class="sxs-lookup"><span data-stu-id="03aec-119">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="03aec-120">Diğer sağlayıcılar bu yapılandırmayı kullanabilir, ancak onu sürdüremezler.</span><span class="sxs-lookup"><span data-stu-id="03aec-120">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

4. <span data-ttu-id="03aec-121">Yapılandırma oluşturma görevini tamamlamak için 'Konfigürasyon oluştur' düğmesini tıklatın</span><span class="sxs-lookup"><span data-stu-id="03aec-121">Click 'Create configuration' button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="03aec-122">Bir veri modeli oluşturun</span><span class="sxs-lookup"><span data-stu-id="03aec-122">Create a data model</span></span>
<span data-ttu-id="03aec-123">Seçili yapılandırma için yeni bir veri modeli oluşturuyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="03aec-123">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="03aec-124">Bu yapılandırma sürümü Taslak durumuna sahip.</span><span class="sxs-lookup"><span data-stu-id="03aec-124">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="03aec-125">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="03aec-125">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="03aec-126">Ödeme işlemine katılan bir tarafın yapısını tanımlama</span><span class="sxs-lookup"><span data-stu-id="03aec-126">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="03aec-127">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-127">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="03aec-128">Ad alanına "Taraf" yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-128">In the Name field, type 'Party'.</span></span>
3. <span data-ttu-id="03aec-129">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-129">Click Add.</span></span>
4. <span data-ttu-id="03aec-130">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-130">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="03aec-131">İsim alanında 'İsim' yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-131">In the Name field, type 'Name'.</span></span>
6. <span data-ttu-id="03aec-132">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="03aec-132">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="03aec-133">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-133">Click Add.</span></span>
8. <span data-ttu-id="03aec-134">Bul alanına "Taraf" yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-134">In the Find field, type 'Party'.</span></span>
9. <span data-ttu-id="03aec-135">Öncekini bul'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-135">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="03aec-136">Bu model için banka yapısını tanımlama</span><span class="sxs-lookup"><span data-stu-id="03aec-136">Define the bank structure for this model</span></span>
1. <span data-ttu-id="03aec-137">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-137">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="03aec-138">İsim alanına 'Agent' yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-138">In the Name field, type 'Agent'.</span></span>
3. <span data-ttu-id="03aec-139">Madde türü alanında 'Kayıt'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="03aec-139">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="03aec-140">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-140">Click Add.</span></span>
5. <span data-ttu-id="03aec-141">Açıklama alanına "Tarafa (borçlu/alacaklı) hesap sağlayan mali kurum (örneğin banka)." yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-141">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>

    <span data-ttu-id="03aec-142">Tarafa (borçlu/alacaklı) hesap sağlayan mali kurum (örneğin banka).</span><span class="sxs-lookup"><span data-stu-id="03aec-142">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  

6. <span data-ttu-id="03aec-143">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-143">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="03aec-144">İsim alanında 'İsim' yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-144">In the Name field, type 'Name'.</span></span> 
8. <span data-ttu-id="03aec-145">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="03aec-145">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="03aec-146">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-146">Click Add.</span></span>
10. <span data-ttu-id="03aec-147">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-147">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="03aec-148">İsim alanına 'SWIFT' yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-148">In the Name field, type 'SWIFT'.</span></span>
12. <span data-ttu-id="03aec-149">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-149">Click Add.</span></span>
13. <span data-ttu-id="03aec-150">Açıklama alanına, "Banka kimlik saptama kodu" yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-150">In the Description field, enter 'Bank identification code'.</span></span> 
14. <span data-ttu-id="03aec-151">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-151">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="03aec-152">İsim alanına 'RoutingNumber' yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-152">In the Name field, type 'RoutingNumber'.</span></span>
16. <span data-ttu-id="03aec-153">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-153">Click Add.</span></span>
17. <span data-ttu-id="03aec-154">Açıklama alanına "Rota numarası" yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-154">In the Description field, enter 'Routing number'.</span></span>
18. <span data-ttu-id="03aec-155">Öncekini bul'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-155">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="03aec-156">Bu model için hesap yapısını tanımlama</span><span class="sxs-lookup"><span data-stu-id="03aec-156">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="03aec-157">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-157">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="03aec-158">İsim alanına 'Hesap' yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-158">In the Name field, type 'Account'.</span></span> 
3. <span data-ttu-id="03aec-159">Madde türü alanında 'Kayıt'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="03aec-159">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="03aec-160">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-160">Click Add.</span></span>
5. <span data-ttu-id="03aec-161">Açıklama alanına "Tarafın bir mali kuruluştaki (örneğin, bir banka) hesap kimliği." yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-161">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>

    <span data-ttu-id="03aec-162">Tarafın bir mali kuruluştaki (örneğin, bir banka) hesap kimliği.</span><span class="sxs-lookup"><span data-stu-id="03aec-162">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  

6. <span data-ttu-id="03aec-163">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-163">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="03aec-164">İsim alanına 'Para birimi' yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-164">In the Name field, type 'Currency'.</span></span> 
8. <span data-ttu-id="03aec-165">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="03aec-165">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="03aec-166">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-166">Click Add.</span></span>
10. <span data-ttu-id="03aec-167">Açıklama alanına "Para birimi kodu" yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-167">In the Description field, enter 'Currency code'.</span></span>
11. <span data-ttu-id="03aec-168">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-168">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="03aec-169">İsim alanına 'Numara' yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-169">In the Name field, type 'Number'.</span></span> 
13. <span data-ttu-id="03aec-170">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-170">Click Add.</span></span>
14. <span data-ttu-id="03aec-171">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-171">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="03aec-172">İsim alanına 'IBAN' yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-172">In the Name field, type 'IBAN'.</span></span> 
16. <span data-ttu-id="03aec-173">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-173">Click Add.</span></span>
17. <span data-ttu-id="03aec-174">Açıklama alanına, "Uluslararası banka hesap numarası" yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-174">In the Description field, enter 'International bank account number'.</span></span>

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="03aec-175">Kredi transferi ödeme türü için ödeme iletisi yapısını tanımlama</span><span class="sxs-lookup"><span data-stu-id="03aec-175">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="03aec-176">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-176">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="03aec-177">Yeni düğüm biçimi alanına "Model kökü" girin.</span><span class="sxs-lookup"><span data-stu-id="03aec-177">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="03aec-178">İsim alanında 'CustomerCreditTransferInitiation' yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-178">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
4. <span data-ttu-id="03aec-179">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-179">Click Add.</span></span>
5. <span data-ttu-id="03aec-180">Bul alanına "CustomerCreditTransferInitiation" yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-180">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span> 
6. <span data-ttu-id="03aec-181">Öncekini bul'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-181">Click Find previous.</span></span>
7. <span data-ttu-id="03aec-182">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-182">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="03aec-183">İsim alanına 'MessageIdentification' yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-183">In the Name field, type 'MessageIdentification'.</span></span> 
9. <span data-ttu-id="03aec-184">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-184">Click Add.</span></span>
10. <span data-ttu-id="03aec-185">Açıklama alanına "Bir iletinin kimliğini belirlemek için talimatı veren tarafça atanan noktadan noktaya referans." yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-185">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>

    <span data-ttu-id="03aec-186">Bir iletinin kimliğini belirlemek için talimatı veren tarafça atanan noktadan noktaya referans.</span><span class="sxs-lookup"><span data-stu-id="03aec-186">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  

11. <span data-ttu-id="03aec-187">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-187">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="03aec-188">İsim alanına 'ProcessingDateTime' yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-188">In the Name field, type 'ProcessingDateTime'.</span></span>
13. <span data-ttu-id="03aec-189">Madde türü alanında 'DateTime' seçin.</span><span class="sxs-lookup"><span data-stu-id="03aec-189">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="03aec-190">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-190">Click Add.</span></span>
15. <span data-ttu-id="03aec-191">Açıklama alanına, "Ödeme iletisinin oluşturulduğu tarih ve saat." yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-191">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span> 
16. <span data-ttu-id="03aec-192">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-192">Click New to open the drop dialog.</span></span>

    <span data-ttu-id="03aec-193">Bu model için ödeme hareketi yapısını tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-193">Define the payment transaction structure for this model.</span></span>  

17. <span data-ttu-id="03aec-194">İsim alanına 'Ödemeler' yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-194">In the Name field, type 'Payments'.</span></span>
18. <span data-ttu-id="03aec-195">Madde türü alanında 'Kayıt listesi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="03aec-195">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="03aec-196">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-196">Click Add.</span></span>
20. <span data-ttu-id="03aec-197">Açıklama alanına, 'Geçerli iletinin ödeme satırları' girin.</span><span class="sxs-lookup"><span data-stu-id="03aec-197">In the Description field, enter 'Payment lines of the current message'.</span></span>
21. <span data-ttu-id="03aec-198">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-198">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="03aec-199">İsim alanına 'Alacaklı' yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-199">In the Name field, type 'Creditor'.</span></span> 
23. <span data-ttu-id="03aec-200">Madde türü alanında 'Kayıt'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="03aec-200">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="03aec-201">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-201">Click Add.</span></span>
25. <span data-ttu-id="03aec-202">Açıklama alanına "Belli bir tutardaki paranın ödenmesi gereken taraf." yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-202">In the Description field, enter 'Party to which an amount of money is due.'.</span></span> 
26. <span data-ttu-id="03aec-203">Madde referansını değiştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-203">Click Switch item reference.</span></span>
27. <span data-ttu-id="03aec-204">Bul alanına "Taraf" yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-204">In the Find field, type 'Party'.</span></span>
28. <span data-ttu-id="03aec-205">Sonrakini bul'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-205">Click Find next.</span></span>
29. <span data-ttu-id="03aec-206">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-206">Click OK.</span></span>
30. <span data-ttu-id="03aec-207">Bul alanına "Ödemeler" yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-207">In the Find field, type 'Payments'.</span></span>
31. <span data-ttu-id="03aec-208">Sonrakini bul'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-208">Click Find next.</span></span>
32. <span data-ttu-id="03aec-209">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-209">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="03aec-210">İsim alanına 'Borçlu' yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-210">In the Name field, type 'Debtor'.</span></span> 
34. <span data-ttu-id="03aec-211">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-211">Click Add.</span></span>
35. <span data-ttu-id="03aec-212">Açıklama alanına "Alacaklıya (son) belli bir tutarda para borçlu olan taraf." yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-212">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
36. <span data-ttu-id="03aec-213">Madde referansını değiştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-213">Click Switch item reference.</span></span>
37. <span data-ttu-id="03aec-214">Bul alanına "Taraf" yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-214">In the Find field, type 'Party'.</span></span>
38. <span data-ttu-id="03aec-215">Sonrakini bul'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-215">Click Find next.</span></span>
39. <span data-ttu-id="03aec-216">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-216">Click OK.</span></span>
40. <span data-ttu-id="03aec-217">Sonrakini bul'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-217">Click Find next.</span></span>
41. <span data-ttu-id="03aec-218">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-218">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="03aec-219">İsim alanına 'Açıklama' yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-219">In the Name field, type 'Description'.</span></span>
43. <span data-ttu-id="03aec-220">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="03aec-220">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="03aec-221">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-221">Click Add.</span></span>
45. <span data-ttu-id="03aec-222">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-222">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="03aec-223">İsim alanına 'Para birimi' yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-223">In the Name field, type 'Currency'.</span></span>
47. <span data-ttu-id="03aec-224">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-224">Click Add.</span></span>
48. <span data-ttu-id="03aec-225">Açıklama alanına "Para birimi kodu" yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-225">In the Description field, enter 'Currency code'.</span></span>
49. <span data-ttu-id="03aec-226">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-226">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="03aec-227">İsim alanına, 'TransactionDate' yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-227">In the Name field, type 'TransactionDate'.</span></span> 
51. <span data-ttu-id="03aec-228">Madde türü alanında 'Tarih' seçin.</span><span class="sxs-lookup"><span data-stu-id="03aec-228">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="03aec-229">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-229">Click Add.</span></span>
53. <span data-ttu-id="03aec-230">Açıklama alanına, "Hareket tarihi" yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-230">In the Description field, enter 'Transaction date'.</span></span> 
54. <span data-ttu-id="03aec-231">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-231">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="03aec-232">İsim alanına 'InstructedAmount' yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-232">In the Name field, type 'InstructedAmount'.</span></span>  
56. <span data-ttu-id="03aec-233">Madde türü alanında 'Gerçek' seçin.</span><span class="sxs-lookup"><span data-stu-id="03aec-233">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="03aec-234">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-234">Click Add.</span></span>
58. <span data-ttu-id="03aec-235">Açıklama alanına "Masraflar düşülmeden önce, borçlu ve alacaklı arasında taşınacak olan para tutarı" yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-235">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="03aec-236">Tutar, başlatan tarafın sipariş ettiği para birimi cinsinden ifade edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="03aec-236">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>

    <span data-ttu-id="03aec-237">Tasraflar düşülmeden önce, borçlu ve alacaklı arasında taşınacak olan para tutarı.</span><span class="sxs-lookup"><span data-stu-id="03aec-237">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="03aec-238">Tutar, başlatan tarafın sipariş ettiği para birimi cinsinden ifade edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="03aec-238">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  

59. <span data-ttu-id="03aec-239">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-239">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="03aec-240">İsim alanına 'End2EndID' yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-240">In the Name field, type 'End2EndID'.</span></span> 
61. <span data-ttu-id="03aec-241">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="03aec-241">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="03aec-242">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-242">Click Add.</span></span>
63. <span data-ttu-id="03aec-243">Açıklama alanına "Başlatan tarafça atanan benzersiz kimlik" yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-243">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="03aec-244">Bu kimlik, tüm uçtan uca zinciri boyunca değişmeden geçirilir.</span><span class="sxs-lookup"><span data-stu-id="03aec-244">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span> 
64. <span data-ttu-id="03aec-245">İsim alanında 'PaymentModel' yazın.</span><span class="sxs-lookup"><span data-stu-id="03aec-245">In the Name field, type 'PaymentModel'.</span></span>

    <span data-ttu-id="03aec-246">PaymentModel adı önceden tanımlanmış ödeme formları arabirimleriyle hizalanır.</span><span class="sxs-lookup"><span data-stu-id="03aec-246">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  

65. <span data-ttu-id="03aec-247">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03aec-247">Click Save.</span></span>
66. <span data-ttu-id="03aec-248">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="03aec-248">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]