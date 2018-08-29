--- 
title: "Uygulama sınıfı yöntemlerini çağırmak için ER ifadeleri tasarlama"
description: "Bu kılavuz, ER ifadelerinde gerekli uygulama sınıfları yöntemlerini çağırarak Elektronik raporlama (ER) yapılandırmalarında mevcut uygulama mantığının nasıl yeniden kullanılabileceğiyle ilgili bilgiler sağlar."
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: fdacd852eeed33b443a3c79b96fc4c4af04bb6b2
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---
# <a name="design-er-expressions-to-call-application-class-methods"></a><span data-ttu-id="ca406-103">Uygulama sınıfı yöntemlerini çağırmak için ER ifadeleri tasarlama</span><span class="sxs-lookup"><span data-stu-id="ca406-103">Design ER expressions to call application class methods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ca406-104">Bu kılavuz, ER ifadelerinde gerekli uygulama sınıfları yöntemlerini çağırarak Elektronik raporlama (ER) yapılandırmalarında mevcut uygulama mantığının nasıl yeniden kullanılabileceğiyle ilgili bilgiler sağlar.</span><span class="sxs-lookup"><span data-stu-id="ca406-104">This guide provides information about how to reuse the existing application logic in Electronic reporting (ER) configurations by calling required methods of application classes in ER expressions.</span></span> <span data-ttu-id="ca406-105">Sınıfları çağırmak için bağımsız değişkenlerin değerleri, çalışma zamanında dinamik olarak (örneğin, doğruluğunu sağlamak için ayrıştırma belgesindeki bilgiye göre) tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="ca406-105">Values of arguments for calling classes can be defined dynamically at run-time: for example, based on information in the parsing document to ensure its correctness.</span></span> <span data-ttu-id="ca406-106">Bu kılavuzda, Litware, Inc. adlı örnek şirket için gerekli ER yapılandırmalarını oluşturacaksınız. Bu yordam, Sistem yöneticisi veya Elektronik raporlama geliştiricisi rolüne atanmış kullanıcılar için oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="ca406-106">In this guide, you will create the required ER configurations for the sample company, Litware, Inc. This procedure is created for users with the assigned role of System administrator or Electronic reporting developer.</span></span> 

<span data-ttu-id="ca406-107">Bu adımlar herhangi bir veri kümesi kullanılarak tamamlanabilir.</span><span class="sxs-lookup"><span data-stu-id="ca406-107">These steps can be completed using any data set.</span></span> <span data-ttu-id="ca406-108">Ayrıca şu dosyayı indirmeniz ve yerel olarak kaydetmeniz gerekir: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.</span><span class="sxs-lookup"><span data-stu-id="ca406-108">You must also download and save the following file locally: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.</span></span>

<span data-ttu-id="ca406-109">Bu adımları tamamlamak için ilk olarak "ER Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ca406-109">To complete these steps, you must first complete the steps in the procedure, “ER Create a configuration provider and mark it as active.”</span></span>

1. <span data-ttu-id="ca406-110">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="ca406-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="ca406-111">Örnek şirket Litware, Inc. için yapılandırma sağlayıcısının kullanılabilir olduğunu ve etkin olarak işaretlendiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-111">Verify that the configuration provider for sample company, Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="ca406-112">Bu yapılandırma sağlayıcısını göremiyorsanız öncelikle "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ca406-112">If you don’t see this configuration provider, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>   
    * <span data-ttu-id="ca406-113">Bir uygulamanın veri güncelleştirmesi için gelen banka ekstrekerini ayrıştırmak üzere bir işlem tasarladığınızı varsayalım.</span><span class="sxs-lookup"><span data-stu-id="ca406-113">Let’s assume that you are designing a process for parsing incoming bank statements for an application data update.</span></span> <span data-ttu-id="ca406-114">Gelen banka ekstrelerini IBAN kodlarını içeren TXT dosyaları olarak alacaksınız.</span><span class="sxs-lookup"><span data-stu-id="ca406-114">You will receive the incoming bank statements as TXT files that contain IBAN codes.</span></span> <span data-ttu-id="ca406-115">Banka ekstresini içe aktarma işleminin bir parçası olarak, halihazırda Dynamics 365 for Finance and Operations'da mevcut olan mantığı kullanarak bu IBAN kodlarının doğru olduklarını doğrulamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ca406-115">As part of the bank statement import process, you need to validate the correctness of this IBAN codes using the logic that is already available in Dynamics 365 for Finance and Operations.</span></span>   

## <a name="import-a-new-er-model-configuration"></a><span data-ttu-id="ca406-116">Yeni bir ER modeli yapılandırmasını içe aktarma</span><span class="sxs-lookup"><span data-stu-id="ca406-116">Import a new ER model configuration</span></span>
1. <span data-ttu-id="ca406-117">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ca406-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ca406-118">Microsoft sağlayıcısı kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ca406-118">Select the Microsoft provider tile.</span></span>  
2. <span data-ttu-id="ca406-119">Depolar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-119">Click Repositories.</span></span>
3. <span data-ttu-id="ca406-120">Filtreleri göster'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-120">Click Show filters.</span></span>
4. <span data-ttu-id="ca406-121">‘Tür adı’ filtre alanını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="ca406-121">Add a filter field ‘Type name’.</span></span> <span data-ttu-id="ca406-122">Ad alanında, "kaynaklar" değerini girin, "içerir" filtre işlecini seçin ve sonra Uygula'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-122">In the Name field, enter the value “resources”, select the “contains” filter operator, and then click Apply.</span></span>
5. <span data-ttu-id="ca406-123">Aç'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-123">Click Open.</span></span>
6. <span data-ttu-id="ca406-124">Ağaçta 'Ödeme modeli' seçin.</span><span class="sxs-lookup"><span data-stu-id="ca406-124">In the tree, select 'Payment model'.</span></span>
    * <span data-ttu-id="ca406-125">Sürümler hızlı sekmesindeki İçe aktar düğmesi etkinleştirilmemişse, ER yapılandırma 'Ödeme modeli'nin bir sürüm 1'inin zaten içe aktarmışsınızdır.</span><span class="sxs-lookup"><span data-stu-id="ca406-125">If the Import button on the Versions FastTab is not enabled, you have already imported the version 1 one of the ER configuration ‘Payment model’.</span></span> <span data-ttu-id="ca406-126">Bu alt görevdeki kalan adımları atlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ca406-126">You can skip the rest steps in this sub-task.</span></span>   
7. <span data-ttu-id="ca406-127">İçe aktar'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ca406-127">Click Import.</span></span>
8. <span data-ttu-id="ca406-128">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ca406-128">Click Yes.</span></span>
9. <span data-ttu-id="ca406-129">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ca406-129">Close the page.</span></span>
10. <span data-ttu-id="ca406-130">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ca406-130">Close the page.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="ca406-131">Yeni bir ER biçim yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="ca406-131">Add a new ER format configuration</span></span>
1. <span data-ttu-id="ca406-132">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-132">Click Reporting configurations.</span></span>
    * <span data-ttu-id="ca406-133">TXT biçimindeki gelen banka ekstrelerini ayrıştırmak için yeni bir ER biçimi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="ca406-133">Add a new ER format to parse incoming bank statements in TXT format.</span></span>  
2. <span data-ttu-id="ca406-134">Ağaçta 'Ödeme modeli' seçin.</span><span class="sxs-lookup"><span data-stu-id="ca406-134">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="ca406-135">İletişim menüsünü açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-135">Click Create configuration to open the dialog menu.</span></span>
4. <span data-ttu-id="ca406-136">Yeni alanına, 'Biçim veri modeline PaymentModel dayalı' girin.</span><span class="sxs-lookup"><span data-stu-id="ca406-136">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
5. <span data-ttu-id="ca406-137">Ad alanına, 'Banka ekstresi içe aktarma biçimi (örnek)' yazın.</span><span class="sxs-lookup"><span data-stu-id="ca406-137">In the Name field, type 'Bank statement import format (sample)'.</span></span>
    * <span data-ttu-id="ca406-138">Banka ekstresi içe aktarma biçimi (örnek)</span><span class="sxs-lookup"><span data-stu-id="ca406-138">Bank statement import format (sample)</span></span>  
6. <span data-ttu-id="ca406-139">Veri içe aktarmayı destekler alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ca406-139">Select Yes in the Supports data import field.</span></span>
7. <span data-ttu-id="ca406-140">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ca406-140">Click Create configuration.</span></span>

## <a name="design-the-er-format-configuration---format"></a><span data-ttu-id="ca406-141">ER biçimi yapılandırması tasarlama - biçim</span><span class="sxs-lookup"><span data-stu-id="ca406-141">Design the ER format configuration - format</span></span>
1. <span data-ttu-id="ca406-142">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ca406-142">Click Designer.</span></span>
    * <span data-ttu-id="ca406-143">Tasarlanan biçim, harici dosyanın TXT biçimindeki beklenen yapısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ca406-143">The designed format represents the expected structure of the external file in TXT format.</span></span>  
2. <span data-ttu-id="ca406-144">İletişim kutusu menüsünü açmak için Kök ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-144">Click Add root to open the dialog menu.</span></span>
3. <span data-ttu-id="ca406-145">Ağaçta, "Metin\Sıra" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ca406-145">In the tree, select 'Text\Sequence'.</span></span>
4. <span data-ttu-id="ca406-146">Ad alanına 'Kök' yazın.</span><span class="sxs-lookup"><span data-stu-id="ca406-146">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="ca406-147">Kök</span><span class="sxs-lookup"><span data-stu-id="ca406-147">Root</span></span>  
5. <span data-ttu-id="ca406-148">Özel karakterler alanında "Yeni satır - Windows (CR LF)" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ca406-148">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
    * <span data-ttu-id="ca406-149">'Özel karakterler' alanında 'Yeni satır - Windows (CR LF)' seçeneği seçilmiştir.</span><span class="sxs-lookup"><span data-stu-id="ca406-149">The option ‘New line - Windows (CR LF)’ has been selected in the ‘Special characters’ field.</span></span> <span data-ttu-id="ca406-150">Bu ayarı temel alarak, ayrıştırma dosyasındaki her satır ayrı bir kayıt olarak ele alınır.</span><span class="sxs-lookup"><span data-stu-id="ca406-150">Based on this setting, each line in the parsing file is considered a separate record.</span></span>  
6. <span data-ttu-id="ca406-151">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-151">Click OK.</span></span>
7. <span data-ttu-id="ca406-152">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ca406-152">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="ca406-153">Ağaçta, "Metin\Sıra" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ca406-153">In the tree, select 'Text\Sequence'.</span></span>
9. <span data-ttu-id="ca406-154">Ad alanına 'Satırlar' yazın.</span><span class="sxs-lookup"><span data-stu-id="ca406-154">In the Name field, type 'Rows'.</span></span>
    * <span data-ttu-id="ca406-155">Satırlar</span><span class="sxs-lookup"><span data-stu-id="ca406-155">Rows</span></span>  
10. <span data-ttu-id="ca406-156">Çokluluk alanında 'Bir fazla'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="ca406-156">In the Multiplicity field, select 'One many'.</span></span>
    * <span data-ttu-id="ca406-157">‘Çok katlılık’ alanında 'Bir çok' seçeneği seçilmiştir.</span><span class="sxs-lookup"><span data-stu-id="ca406-157">The option ‘One many’ has been selected in the ‘Multiplicity’ field.</span></span> <span data-ttu-id="ca406-158">Bu ayara bağlı olarak, ayrıştırma dosyasında en az bir satır sunulması beklenir.</span><span class="sxs-lookup"><span data-stu-id="ca406-158">Based on this setting, it is expected that at least one line will be presented in the parsing file.</span></span>  
11. <span data-ttu-id="ca406-159">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-159">Click OK.</span></span>
12. <span data-ttu-id="ca406-160">Ağaçta, 'Kök\Satırlar' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ca406-160">In the tree, select 'Root\Rows'.</span></span>
13. <span data-ttu-id="ca406-161">Sıra ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-161">Click Add Sequence.</span></span>
14. <span data-ttu-id="ca406-162">Ad alanına 'Alanlar' yazın.</span><span class="sxs-lookup"><span data-stu-id="ca406-162">In the Name field, type 'Fields'.</span></span>
    * <span data-ttu-id="ca406-163">Alanlar</span><span class="sxs-lookup"><span data-stu-id="ca406-163">Fields</span></span>  
15. <span data-ttu-id="ca406-164">Çokluluk alanında 'Tam bir'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ca406-164">In the Multiplicity field, select 'Exactly one'.</span></span>
16. <span data-ttu-id="ca406-165">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-165">Click OK.</span></span>
17. <span data-ttu-id="ca406-166">Ağaçta, 'Kök\Satırlar\Alanlar' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ca406-166">In the tree, select 'Root\Rows\Fields'.</span></span>
18. <span data-ttu-id="ca406-167">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ca406-167">Click Add to open the drop dialog.</span></span>
19. <span data-ttu-id="ca406-168">Ağaçta seçin 'Text\String'.</span><span class="sxs-lookup"><span data-stu-id="ca406-168">In the tree, select 'Text\String'.</span></span>
20. <span data-ttu-id="ca406-169">İsim alanına 'IBAN' yazın.</span><span class="sxs-lookup"><span data-stu-id="ca406-169">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="ca406-170">IBAN</span><span class="sxs-lookup"><span data-stu-id="ca406-170">IBAN</span></span>  
21. <span data-ttu-id="ca406-171">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-171">Click OK.</span></span>
    * <span data-ttu-id="ca406-172">Ayrıştırma dosyasındaki her satırı yalnızca IBAN kodunu içerecek şekilde yapılandırıldı.</span><span class="sxs-lookup"><span data-stu-id="ca406-172">It has been configured that each line in the parsing file contains the only IBAN code.</span></span>  
22. <span data-ttu-id="ca406-173">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-173">Click Save.</span></span>

## <a name="design-the-er-format-configuration--mapping-to-data-model"></a><span data-ttu-id="ca406-174">ER biçimi yapılandırması tasarlama – veri modeliyle eşleme</span><span class="sxs-lookup"><span data-stu-id="ca406-174">Design the ER format configuration – mapping to data model</span></span>
1. <span data-ttu-id="ca406-175">Biçimi modelle eşle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-175">Click Map format to model.</span></span>
2. <span data-ttu-id="ca406-176">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-176">Click New.</span></span>
3. <span data-ttu-id="ca406-177">Tanım alanına 'BankToCustomerDebitCreditNotificationInitiation' yazın.</span><span class="sxs-lookup"><span data-stu-id="ca406-177">In the Definition field, type 'BankToCustomerDebitCreditNotificationInitiation'.</span></span>
    * <span data-ttu-id="ca406-178">BankToCustomerDebitCreditNotificationInitiation</span><span class="sxs-lookup"><span data-stu-id="ca406-178">BankToCustomerDebitCreditNotificationInitiation</span></span>  
4. <span data-ttu-id="ca406-179">Tanımı ResolveChanges.</span><span class="sxs-lookup"><span data-stu-id="ca406-179">ResolveChanges the Definition.</span></span>
5. <span data-ttu-id="ca406-180">Ad alanına 'Veri modeliyle eşleme' yazın.</span><span class="sxs-lookup"><span data-stu-id="ca406-180">In the Name field, type 'Mapping to data model'.</span></span>
    * <span data-ttu-id="ca406-181">Veri modeline eşleme</span><span class="sxs-lookup"><span data-stu-id="ca406-181">Mapping to data model</span></span>  
6. <span data-ttu-id="ca406-182">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-182">Click Save.</span></span>
7. <span data-ttu-id="ca406-183">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ca406-183">Click Designer.</span></span>
8. <span data-ttu-id="ca406-184">Ağaçta, 'Dynamics 365 for Operations\Sınıf' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ca406-184">In the tree, select 'Dynamics 365 for Operations\Class'.</span></span>
9. <span data-ttu-id="ca406-185">Kök ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-185">Click Add root.</span></span>
    * <span data-ttu-id="ca406-186">IBAN kodları doğrulaması için mevcut uygulama mantığını çağırmak üzere yeni veri kaynağı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="ca406-186">Add a new data source to call the existing application logic for IBAN codes validation.</span></span>  
10. <span data-ttu-id="ca406-187">Ad alanına, 'check_codes' yazın.</span><span class="sxs-lookup"><span data-stu-id="ca406-187">In the Name field, type 'check_codes'.</span></span>
    * <span data-ttu-id="ca406-188">çek kodları</span><span class="sxs-lookup"><span data-stu-id="ca406-188">check_codes</span></span>  
11. <span data-ttu-id="ca406-189">Sınıf alanına 'ISO7064' yazın.</span><span class="sxs-lookup"><span data-stu-id="ca406-189">In the Class field, type 'ISO7064'.</span></span>
    * <span data-ttu-id="ca406-190">ISO7064</span><span class="sxs-lookup"><span data-stu-id="ca406-190">ISO7064</span></span>  
12. <span data-ttu-id="ca406-191">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-191">Click OK.</span></span>
13. <span data-ttu-id="ca406-192">Ağaçta, 'biçim' metnini genişletin.</span><span class="sxs-lookup"><span data-stu-id="ca406-192">In the tree, expand 'format'.</span></span>
14. <span data-ttu-id="ca406-193">Ağaçta, 'biçim\Kök: Sıra(Kök)' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ca406-193">In the tree, expand 'format\Root: Sequence(Root)'.</span></span>
15. <span data-ttu-id="ca406-194">Ağaçta, 'biçim\Kök: Sıra(Kök)\Satırlar: Sıra 1..\* (Satırlar)' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ca406-194">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
16. <span data-ttu-id="ca406-195">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-195">Click Bind.</span></span>
17. <span data-ttu-id="ca406-196">Ağaçta, 'biçim\Kök: Sıra(Kök)\Satırlar: Sıra 1..\* (Satırlar)' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="ca406-196">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
18. <span data-ttu-id="ca406-197">Ağaçta, 'biçim\Kök: Sıra(Kök)\Satırlar: Sıra 1..\* (Satırlar)\Alanlar: Sıra 1..1 (Alanlar)' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="ca406-197">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)'.</span></span>
19. <span data-ttu-id="ca406-198">Ağaçta, 'biçim\Kök: Sıra(Kök)\Satırlar: Sıra 1..\* (Satırlar)\Alanlar: Sıra 1..1 (Alanlar)\IBAN: Dize(IBAN)' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ca406-198">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)'.</span></span>
20. <span data-ttu-id="ca406-199">Ağaçta 'Ödemeler = biçim.Kök.Satırlar' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="ca406-199">In the tree, expand 'Payments = format.Root.Rows'.</span></span>
21. <span data-ttu-id="ca406-200">Ağaçta, 'Ödemeler = format.Root.Rows\Alacaklı Hesabı(CreditorAccount)' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="ca406-200">In the tree, expand 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)'.</span></span>
22. <span data-ttu-id="ca406-201">Ağaçta, 'Ödemeler = format.Root.Rows\Alacaklı Hesabı(CreditorAccount)\Kimlik Saptama' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="ca406-201">In the tree, expand 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification'.</span></span>
23. <span data-ttu-id="ca406-202">Ağaçta, 'Ödemeler = format.Root.Rows\Alacaklı Hesabı(CreditorAccount)\Kimlik Saptama\IBAN' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ca406-202">In the tree, select 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification\IBAN'.</span></span>
24. <span data-ttu-id="ca406-203">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-203">Click Bind.</span></span>
25. <span data-ttu-id="ca406-204">Doğrulamalar sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-204">Click the Validations tab.</span></span>
26. <span data-ttu-id="ca406-205">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-205">Click New.</span></span>
    * <span data-ttu-id="ca406-206">Geçersiz IBAN kodu içeren ayrıştırma dosyasındaki herhangi bir satır için bir hata görüntüleyen yeni bir doğrulama kuralı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="ca406-206">Add a new validation rule that displays an error for any line in the parsing file that contains invalid IBAN code.</span></span>  
27. <span data-ttu-id="ca406-207">Koşulu düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-207">Click Edit condition.</span></span>
28. <span data-ttu-id="ca406-208">Ağaçta 'check_codes' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="ca406-208">In the tree, expand 'check_codes'.</span></span>
29. <span data-ttu-id="ca406-209">Ağaçta, 'check_codes\verifyMOD1271_36' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ca406-209">In the tree, select 'check_codes\verifyMOD1271_36'.</span></span>
30. <span data-ttu-id="ca406-210">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-210">Click Add data source.</span></span>
31. <span data-ttu-id="ca406-211">Formül alanına 'check_codes.verifyMOD1271_36(' yazın.</span><span class="sxs-lookup"><span data-stu-id="ca406-211">In the Formula field, enter 'check_codes.verifyMOD1271_36('.</span></span>
    * <span data-ttu-id="ca406-212">check_codes.verifyMOD1271_36(</span><span class="sxs-lookup"><span data-stu-id="ca406-212">check_codes.verifyMOD1271_36(</span></span>  
32. <span data-ttu-id="ca406-213">Ağaçta, 'biçim' metnini genişletin.</span><span class="sxs-lookup"><span data-stu-id="ca406-213">In the tree, expand 'format'.</span></span>
33. <span data-ttu-id="ca406-214">Ağaçta, 'biçim\Kök: Sıra(Kök)' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ca406-214">In the tree, expand 'format\Root: Sequence(Root)'.</span></span>
34. <span data-ttu-id="ca406-215">Ağaçta, 'biçim\Kök: Sıra(Kök)\Satırlar: Sıra 1..\* (Satırlar)' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="ca406-215">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
35. <span data-ttu-id="ca406-216">Ağaçta, 'biçim\Kök: Sıra(Kök)\Satırlar: Sıra 1..\* (Satırlar)\Alanlar: Sıra 1..1 (Alanlar)' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="ca406-216">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)'.</span></span>
36. <span data-ttu-id="ca406-217">Ağaçta, 'biçim\Kök: Sıra(Kök)\Satırlar: Sıra 1..\* (Satırlar)\Alanlar: Sıra 1..1 (Alanlar)\IBAN: Dize(IBAN)' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ca406-217">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)'.</span></span>
37. <span data-ttu-id="ca406-218">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-218">Click Add data source.</span></span>
38. <span data-ttu-id="ca406-219">Formül alanına 'check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)' yazın.</span><span class="sxs-lookup"><span data-stu-id="ca406-219">In the Formula field, enter 'check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)'.</span></span>
    * <span data-ttu-id="ca406-220">check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)</span><span class="sxs-lookup"><span data-stu-id="ca406-220">check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)</span></span>  
39. <span data-ttu-id="ca406-221">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-221">Click Save.</span></span>
40. <span data-ttu-id="ca406-222">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ca406-222">Close the page.</span></span>
    * <span data-ttu-id="ca406-223">Doğrulama koşulu herhangi bir geçersiz IBAN kodu için ‘ISO7064’ uygulama sınıfının mevcut ‘verifyMOD1271_36’ yöntemini çağırarak YANLIŞ değeri döndürecek şekilde yapılandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="ca406-223">The validation condition has been configured to return FALSE for any invalid IBAN code by calling the existing method ‘verifyMOD1271_36’ of the application class ‘ISO7064’.</span></span> <span data-ttu-id="ca406-224">IBAN kodu değerinin çalışma zamanında çağırma yönteminin bağımsız değişkeni olarak ayrıştırma TXT dosyası içeri temel alınarak dinamik şekilde tanımlandığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-224">Note that the value of the IBAN code is defined dynamically at run-time as the argument of the calling method based on the content of the parsing TXT file.</span></span>   
41. <span data-ttu-id="ca406-225">İletiyi düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-225">Click Edit message.</span></span>
42. <span data-ttu-id="ca406-226">Formül alanına 'CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)' girin.</span><span class="sxs-lookup"><span data-stu-id="ca406-226">In the Formula field, enter 'CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)'.</span></span>
    * <span data-ttu-id="ca406-227">CONCATENATE("Geçersiz IBAN kodu bulundu:  ", format.Root.Rows.Fields.IBAN)</span><span class="sxs-lookup"><span data-stu-id="ca406-227">CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)</span></span>  
43. <span data-ttu-id="ca406-228">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-228">Click Save.</span></span>
44. <span data-ttu-id="ca406-229">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ca406-229">Close the page.</span></span>
45. <span data-ttu-id="ca406-230">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-230">Click Save.</span></span>
46. <span data-ttu-id="ca406-231">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ca406-231">Close the page.</span></span>

## <a name="run-the-format-mapping"></a><span data-ttu-id="ca406-232">Biçim eşlemeyi çalıştırma</span><span class="sxs-lookup"><span data-stu-id="ca406-232">Run the format mapping</span></span>
<span data-ttu-id="ca406-233">Sınama amacıyla, daha önce yüklediğiniz SampleIncomingMessage.txt dosyasını kullanarak biçim eşlemesi yürütün.</span><span class="sxs-lookup"><span data-stu-id="ca406-233">For testing purposes, execute the format mapping using the SampleIncomingMessage.txt file that you downloaded.</span></span> <span data-ttu-id="ca406-234">Oluşturulan çıktı, seçilen TXT dosyasından içeri aktarılacak verileri içerir ve gerçek içe aktarma sırasında özel veri modelini doldurur.</span><span class="sxs-lookup"><span data-stu-id="ca406-234">The generated output includes data that will be imported from the selected TXT file and populated to the custom data model during the real import.</span></span>   
1. <span data-ttu-id="ca406-235">Çalıştır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-235">Click Run.</span></span>
    * <span data-ttu-id="ca406-236">Gözat düğmesine tıklayın ve önceden indirdiğiniz SampleIncomingMessage.txt dosyasına gidin.</span><span class="sxs-lookup"><span data-stu-id="ca406-236">Click Browse and navigate to the SampleIncomingMessage.txt file that you previously downloaded.</span></span>  
2. <span data-ttu-id="ca406-237">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-237">Click OK.</span></span>
    * <span data-ttu-id="ca406-238">Seçili dosyadan içeri aktarılan ve veri modeline taşınan verileri temsil eden XML biçimindeki çıktıyı gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="ca406-238">Review the output in XML format that represents the data that has been imported from the selected file and ported to the data model.</span></span> <span data-ttu-id="ca406-239">İçe aktarılan TXT dosyasındaki yalnızca 3 satırın işlendiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="ca406-239">Note that only 3 lines of the imported TXT file were processed.</span></span> <span data-ttu-id="ca406-240">Satır 4'teki geçersiz IBAN kodu atlandı ve Bilgi günlüğünde bir hata iletisi sağlandı.</span><span class="sxs-lookup"><span data-stu-id="ca406-240">The IBAN code on line 4 that is not valid was skipped and an error message is provided in the Infolog.</span></span>  


