---
title: ER Tasarım etki alanına özel veri modeli
description: Bu konuda, elektronik ödeme belgeleri için bir veri modeli içeren yeni bir Elektronik raporlama (ER) yapılandırmasının nasıl oluşturulacağı açıklanmaktadır.
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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1eb2c6e5b5f186fb6db7c32a9982807274e5ea1b
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092703"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="fce92-103">ER Tasarım etki alanına özel veri modeli</span><span class="sxs-lookup"><span data-stu-id="fce92-103">ER Design domain specific data model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fce92-104">Aşağıdaki yordamda, Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının elektronik ödeme belgeleri için bir veri modeli içeren, yeni bir Elektronik Raporlama (ER) yapılandırmasını nasıl oluşturabileceği açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="fce92-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="fce92-105">Ödeme belgeleri için biçim oluşturduğunuzda, bu veri modeli daha sonra bir veri kaynağı olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fce92-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>

<span data-ttu-id="fce92-106">Bu örnekte Litware, Inc. örnek şirketi için bir yapılandırma oluşturacaksınız. Bu adımlar, ER yapılandırmaları şirketler arasında paylaşımlı olduğundan herhangi bir şirkette gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="fce92-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="fce92-107">Bu adımları tamamlamak için öncelikle "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="fce92-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

1. <span data-ttu-id="fce92-108">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="fce92-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="fce92-109">Örnek şirket 'Litware, Inc.' için yapılandırma sağlayıcısını seçin.</span><span class="sxs-lookup"><span data-stu-id="fce92-109">Select the configuration provider for sample company, 'Litware, Inc.'</span></span> <span data-ttu-id="fce92-110">Bu yapılandırma sağlayıcısını göremiyorsanız öncelikle "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="fce92-110">If you don't see this configuration provider, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>  
    
2. <span data-ttu-id="fce92-111">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-111">Click Reporting configurations.</span></span>

    <span data-ttu-id="fce92-112">Bir elektronik ödeme belgeleri için veri modeli içeren bir yapılandırma oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="fce92-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="fce92-113">Ödeme belgeleri için biçim oluşturduğunuzda, bu veri modeli daha sonra bir veri kaynağı olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fce92-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="fce92-114">Yeni bir veri modeli yapılandırması oluşturun</span><span class="sxs-lookup"><span data-stu-id="fce92-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="fce92-115">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="fce92-116">İsim alanında, 'Ödemeler (Basitleştirilmiş model)' yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-116">In the Name field, type 'Payments (simplified model)'.</span></span>
3. <span data-ttu-id="fce92-117">Açıklama alanına, 'Ödeme modeli yapılandırması' yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-117">In the Description field, type 'Payment model configuration'.</span></span>

    <span data-ttu-id="fce92-118">Etkin yapılandırma sağlayıcısı otomatik olarak buraya girilir.</span><span class="sxs-lookup"><span data-stu-id="fce92-118">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="fce92-119">Bu sağlayıcının, bu yapılandırmayı sürdürmesi mümkün olacaktır.</span><span class="sxs-lookup"><span data-stu-id="fce92-119">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="fce92-120">Diğer sağlayıcılar bu yapılandırmayı kullanabilir, ancak onu sürdüremezler.</span><span class="sxs-lookup"><span data-stu-id="fce92-120">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

4. <span data-ttu-id="fce92-121">Yapılandırma oluşturma görevini tamamlamak için 'Konfigürasyon oluştur' düğmesini tıklatın</span><span class="sxs-lookup"><span data-stu-id="fce92-121">Click 'Create configuration' button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="fce92-122">Bir veri modeli oluşturun</span><span class="sxs-lookup"><span data-stu-id="fce92-122">Create a data model</span></span>
<span data-ttu-id="fce92-123">Seçili yapılandırma için yeni bir veri modeli oluşturuyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="fce92-123">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="fce92-124">Bu yapılandırma sürümü Taslak durumuna sahip.</span><span class="sxs-lookup"><span data-stu-id="fce92-124">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="fce92-125">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fce92-125">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="fce92-126">Ödeme işlemine katılan bir tarafın yapısını tanımlama</span><span class="sxs-lookup"><span data-stu-id="fce92-126">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="fce92-127">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-127">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="fce92-128">Ad alanına "Taraf" yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-128">In the Name field, type 'Party'.</span></span>
3. <span data-ttu-id="fce92-129">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-129">Click Add.</span></span>
4. <span data-ttu-id="fce92-130">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-130">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="fce92-131">İsim alanında 'İsim' yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-131">In the Name field, type 'Name'.</span></span>
6. <span data-ttu-id="fce92-132">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="fce92-132">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="fce92-133">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-133">Click Add.</span></span>
8. <span data-ttu-id="fce92-134">Bul alanına "Taraf" yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-134">In the Find field, type 'Party'.</span></span>
9. <span data-ttu-id="fce92-135">Öncekini bul'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-135">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="fce92-136">Bu model için banka yapısını tanımlama</span><span class="sxs-lookup"><span data-stu-id="fce92-136">Define the bank structure for this model</span></span>
1. <span data-ttu-id="fce92-137">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-137">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="fce92-138">İsim alanına 'Agent' yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-138">In the Name field, type 'Agent'.</span></span>
3. <span data-ttu-id="fce92-139">Madde türü alanında 'Kayıt'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="fce92-139">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="fce92-140">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-140">Click Add.</span></span>
5. <span data-ttu-id="fce92-141">Açıklama alanına "Tarafa (borçlu/alacaklı) hesap sağlayan mali kurum (örneğin banka)." yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-141">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>

    <span data-ttu-id="fce92-142">Tarafa (borçlu/alacaklı) hesap sağlayan mali kurum (örneğin banka).</span><span class="sxs-lookup"><span data-stu-id="fce92-142">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  

6. <span data-ttu-id="fce92-143">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-143">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="fce92-144">İsim alanında 'İsim' yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-144">In the Name field, type 'Name'.</span></span> 
8. <span data-ttu-id="fce92-145">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="fce92-145">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="fce92-146">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-146">Click Add.</span></span>
10. <span data-ttu-id="fce92-147">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-147">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="fce92-148">İsim alanına 'SWIFT' yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-148">In the Name field, type 'SWIFT'.</span></span>
12. <span data-ttu-id="fce92-149">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-149">Click Add.</span></span>
13. <span data-ttu-id="fce92-150">Açıklama alanına, "Banka kimlik saptama kodu" yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-150">In the Description field, enter 'Bank identification code'.</span></span> 
14. <span data-ttu-id="fce92-151">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-151">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="fce92-152">İsim alanına 'RoutingNumber' yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-152">In the Name field, type 'RoutingNumber'.</span></span>
16. <span data-ttu-id="fce92-153">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-153">Click Add.</span></span>
17. <span data-ttu-id="fce92-154">Açıklama alanına "Rota numarası" yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-154">In the Description field, enter 'Routing number'.</span></span>
18. <span data-ttu-id="fce92-155">Öncekini bul'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-155">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="fce92-156">Bu model için hesap yapısını tanımlama</span><span class="sxs-lookup"><span data-stu-id="fce92-156">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="fce92-157">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-157">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="fce92-158">İsim alanına 'Hesap' yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-158">In the Name field, type 'Account'.</span></span> 
3. <span data-ttu-id="fce92-159">Madde türü alanında 'Kayıt'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="fce92-159">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="fce92-160">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-160">Click Add.</span></span>
5. <span data-ttu-id="fce92-161">Açıklama alanına "Tarafın bir mali kuruluştaki (örneğin, bir banka) hesap kimliği." yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-161">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>

    <span data-ttu-id="fce92-162">Tarafın bir mali kuruluştaki (örneğin, bir banka) hesap kimliği.</span><span class="sxs-lookup"><span data-stu-id="fce92-162">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  

6. <span data-ttu-id="fce92-163">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-163">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="fce92-164">İsim alanına 'Para birimi' yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-164">In the Name field, type 'Currency'.</span></span> 
8. <span data-ttu-id="fce92-165">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="fce92-165">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="fce92-166">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-166">Click Add.</span></span>
10. <span data-ttu-id="fce92-167">Açıklama alanına "Para birimi kodu" yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-167">In the Description field, enter 'Currency code'.</span></span>
11. <span data-ttu-id="fce92-168">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-168">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="fce92-169">İsim alanına 'Numara' yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-169">In the Name field, type 'Number'.</span></span> 
13. <span data-ttu-id="fce92-170">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-170">Click Add.</span></span>
14. <span data-ttu-id="fce92-171">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-171">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="fce92-172">İsim alanına 'IBAN' yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-172">In the Name field, type 'IBAN'.</span></span> 
16. <span data-ttu-id="fce92-173">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-173">Click Add.</span></span>
17. <span data-ttu-id="fce92-174">Açıklama alanına, "Uluslararası banka hesap numarası" yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-174">In the Description field, enter 'International bank account number'.</span></span>

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="fce92-175">Kredi transferi ödeme türü için ödeme iletisi yapısını tanımlama</span><span class="sxs-lookup"><span data-stu-id="fce92-175">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="fce92-176">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-176">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="fce92-177">Yeni düğüm biçimi alanına "Model kökü" girin.</span><span class="sxs-lookup"><span data-stu-id="fce92-177">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="fce92-178">İsim alanında 'CustomerCreditTransferInitiation' yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-178">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
4. <span data-ttu-id="fce92-179">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-179">Click Add.</span></span>
5. <span data-ttu-id="fce92-180">Bul alanına "CustomerCreditTransferInitiation" yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-180">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span> 
6. <span data-ttu-id="fce92-181">Öncekini bul'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-181">Click Find previous.</span></span>
7. <span data-ttu-id="fce92-182">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-182">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="fce92-183">İsim alanına 'MessageIdentification' yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-183">In the Name field, type 'MessageIdentification'.</span></span> 
9. <span data-ttu-id="fce92-184">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-184">Click Add.</span></span>
10. <span data-ttu-id="fce92-185">Açıklama alanına "Bir iletinin kimliğini belirlemek için talimatı veren tarafça atanan noktadan noktaya referans." yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-185">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>

    <span data-ttu-id="fce92-186">Bir iletinin kimliğini belirlemek için talimatı veren tarafça atanan noktadan noktaya referans.</span><span class="sxs-lookup"><span data-stu-id="fce92-186">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  

11. <span data-ttu-id="fce92-187">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-187">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="fce92-188">İsim alanına 'ProcessingDateTime' yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-188">In the Name field, type 'ProcessingDateTime'.</span></span>
13. <span data-ttu-id="fce92-189">Madde türü alanında 'DateTime' seçin.</span><span class="sxs-lookup"><span data-stu-id="fce92-189">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="fce92-190">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-190">Click Add.</span></span>
15. <span data-ttu-id="fce92-191">Açıklama alanına, "Ödeme iletisinin oluşturulduğu tarih ve saat." yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-191">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span> 
16. <span data-ttu-id="fce92-192">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-192">Click New to open the drop dialog.</span></span>

    <span data-ttu-id="fce92-193">Bu model için ödeme hareketi yapısını tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-193">Define the payment transaction structure for this model.</span></span>  

17. <span data-ttu-id="fce92-194">İsim alanına 'Ödemeler' yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-194">In the Name field, type 'Payments'.</span></span>
18. <span data-ttu-id="fce92-195">Madde türü alanında 'Kayıt listesi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="fce92-195">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="fce92-196">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-196">Click Add.</span></span>
20. <span data-ttu-id="fce92-197">Açıklama alanına, 'Geçerli iletinin ödeme satırları' girin.</span><span class="sxs-lookup"><span data-stu-id="fce92-197">In the Description field, enter 'Payment lines of the current message'.</span></span>
21. <span data-ttu-id="fce92-198">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-198">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="fce92-199">İsim alanına 'Alacaklı' yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-199">In the Name field, type 'Creditor'.</span></span> 
23. <span data-ttu-id="fce92-200">Madde türü alanında 'Kayıt'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="fce92-200">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="fce92-201">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-201">Click Add.</span></span>
25. <span data-ttu-id="fce92-202">Açıklama alanına "Belli bir tutardaki paranın ödenmesi gereken taraf." yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-202">In the Description field, enter 'Party to which an amount of money is due.'.</span></span> 
26. <span data-ttu-id="fce92-203">Madde referansını değiştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-203">Click Switch item reference.</span></span>
27. <span data-ttu-id="fce92-204">Bul alanına "Taraf" yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-204">In the Find field, type 'Party'.</span></span>
28. <span data-ttu-id="fce92-205">Sonrakini bul'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-205">Click Find next.</span></span>
29. <span data-ttu-id="fce92-206">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-206">Click OK.</span></span>
30. <span data-ttu-id="fce92-207">Bul alanına "Ödemeler" yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-207">In the Find field, type 'Payments'.</span></span>
31. <span data-ttu-id="fce92-208">Sonrakini bul'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-208">Click Find next.</span></span>
32. <span data-ttu-id="fce92-209">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-209">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="fce92-210">İsim alanına 'Borçlu' yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-210">In the Name field, type 'Debtor'.</span></span> 
34. <span data-ttu-id="fce92-211">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-211">Click Add.</span></span>
35. <span data-ttu-id="fce92-212">Açıklama alanına "Alacaklıya (son) belli bir tutarda para borçlu olan taraf." yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-212">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
36. <span data-ttu-id="fce92-213">Madde referansını değiştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-213">Click Switch item reference.</span></span>
37. <span data-ttu-id="fce92-214">Bul alanına "Taraf" yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-214">In the Find field, type 'Party'.</span></span>
38. <span data-ttu-id="fce92-215">Sonrakini bul'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-215">Click Find next.</span></span>
39. <span data-ttu-id="fce92-216">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-216">Click OK.</span></span>
40. <span data-ttu-id="fce92-217">Sonrakini bul'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-217">Click Find next.</span></span>
41. <span data-ttu-id="fce92-218">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-218">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="fce92-219">İsim alanına 'Açıklama' yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-219">In the Name field, type 'Description'.</span></span>
43. <span data-ttu-id="fce92-220">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="fce92-220">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="fce92-221">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-221">Click Add.</span></span>
45. <span data-ttu-id="fce92-222">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-222">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="fce92-223">İsim alanına 'Para birimi' yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-223">In the Name field, type 'Currency'.</span></span>
47. <span data-ttu-id="fce92-224">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-224">Click Add.</span></span>
48. <span data-ttu-id="fce92-225">Açıklama alanına "Para birimi kodu" yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-225">In the Description field, enter 'Currency code'.</span></span>
49. <span data-ttu-id="fce92-226">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-226">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="fce92-227">İsim alanına, 'TransactionDate' yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-227">In the Name field, type 'TransactionDate'.</span></span> 
51. <span data-ttu-id="fce92-228">Madde türü alanında 'Tarih' seçin.</span><span class="sxs-lookup"><span data-stu-id="fce92-228">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="fce92-229">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-229">Click Add.</span></span>
53. <span data-ttu-id="fce92-230">Açıklama alanına, "Hareket tarihi" yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-230">In the Description field, enter 'Transaction date'.</span></span> 
54. <span data-ttu-id="fce92-231">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-231">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="fce92-232">İsim alanına 'InstructedAmount' yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-232">In the Name field, type 'InstructedAmount'.</span></span>  
56. <span data-ttu-id="fce92-233">Madde türü alanında 'Gerçek' seçin.</span><span class="sxs-lookup"><span data-stu-id="fce92-233">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="fce92-234">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-234">Click Add.</span></span>
58. <span data-ttu-id="fce92-235">Açıklama alanına "Masraflar düşülmeden önce, borçlu ve alacaklı arasında taşınacak olan para tutarı" yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-235">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="fce92-236">Tutar, başlatan tarafın sipariş ettiği para birimi cinsinden ifade edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="fce92-236">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>

    <span data-ttu-id="fce92-237">Tasraflar düşülmeden önce, borçlu ve alacaklı arasında taşınacak olan para tutarı.</span><span class="sxs-lookup"><span data-stu-id="fce92-237">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="fce92-238">Tutar, başlatan tarafın sipariş ettiği para birimi cinsinden ifade edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="fce92-238">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  

59. <span data-ttu-id="fce92-239">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-239">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="fce92-240">İsim alanına 'End2EndID' yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-240">In the Name field, type 'End2EndID'.</span></span> 
61. <span data-ttu-id="fce92-241">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="fce92-241">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="fce92-242">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-242">Click Add.</span></span>
63. <span data-ttu-id="fce92-243">Açıklama alanına "Başlatan tarafça atanan benzersiz kimlik" yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-243">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="fce92-244">Bu kimlik, tüm uçtan uca zinciri boyunca değişmeden geçirilir.</span><span class="sxs-lookup"><span data-stu-id="fce92-244">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span> 
64. <span data-ttu-id="fce92-245">İsim alanında 'PaymentModel' yazın.</span><span class="sxs-lookup"><span data-stu-id="fce92-245">In the Name field, type 'PaymentModel'.</span></span>

    <span data-ttu-id="fce92-246">PaymentModel adı önceden tanımlanmış ödeme formları arabirimleriyle hizalanır.</span><span class="sxs-lookup"><span data-stu-id="fce92-246">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  

65. <span data-ttu-id="fce92-247">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fce92-247">Click Save.</span></span>
66. <span data-ttu-id="fce92-248">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="fce92-248">Close the page.</span></span>

