---
title: Human Resources parametrelerini yapılandırma
description: Bu konuda, Dynamics 365 Human Resources'da şirkete özel parametrelerin nasıl ayarlanacağı açıklanmaktadır.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 10f3c62925f6b951f88b990cb8b103dde54c27d1
ms.sourcegitcommit: 45d10d0c25b3ec585323709bb97ba1895b500429
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/05/2021
ms.locfileid: "5502952"
---
# <a name="configure-human-resources-parameters"></a><span data-ttu-id="ee231-103">Human Resources parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="ee231-103">Configure Human resources parameters</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ee231-104">Human Resources parametrelerinin ayarları şirketler arasında paylaşılır ancak diğer parametrelerin ayarları şirkete özeldir.</span><span class="sxs-lookup"><span data-stu-id="ee231-104">The settings of some Human resources parameters are shared across companies, while the settings of other parameters are company-specific.</span></span> <span data-ttu-id="ee231-105">Bu konu başlığında, şirkete özgü Human Resources parametrelerinin nasıl ayarlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ee231-105">This topic explains how to set up company-specific Human resources parameters.</span></span>

<span data-ttu-id="ee231-106">İki sayfa Human Resources parametrelerini ayarlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ee231-106">Two pages are used to set Human resources parameters.</span></span> <span data-ttu-id="ee231-107">Şirketler arasında paylaşılan parametreler için **İnsan Kaynakları paylaşılan parametreleri** sayfasını kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="ee231-107">For parameters that are shared across companies, you use the **Human resources shared parameters** page.</span></span> <span data-ttu-id="ee231-108">Şirkete özgü parametreler için (diğer bir deyişle, tek bir şirket için uygulanan ayarlar) **İnsan Kaynakları parametreleri** sayfasını kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="ee231-108">For parameters that are company-specific (in other words, the settings apply to a single company), you use the **Human resource parameters** page.</span></span>

![Human Resources parametrelerini yapılandır'a gidin](./media/hr-employee-self-service-human-resources-parameters.png)

<span data-ttu-id="ee231-110">**İnsan Kaynakları parametreleri** sayfasında ayarlar altı sekmeye ayrılır:</span><span class="sxs-lookup"><span data-stu-id="ee231-110">On the **Human resources parameters** page, the settings are divided among six tabs:</span></span>

- <span data-ttu-id="ee231-111">**Genel**</span><span class="sxs-lookup"><span data-stu-id="ee231-111">**General**</span></span>
- <span data-ttu-id="ee231-112">**İşe alım** (bu sekme Dynamics 365 Human Resources'a dahil değildir)</span><span class="sxs-lookup"><span data-stu-id="ee231-112">**Recruitment** (this tab isn't included in Dynamics 365 Human Resources)</span></span>
- <span data-ttu-id="ee231-113">**Maaş**</span><span class="sxs-lookup"><span data-stu-id="ee231-113">**Compensation**</span></span>
- <span data-ttu-id="ee231-114">**Numara serileri**</span><span class="sxs-lookup"><span data-stu-id="ee231-114">**Number sequences**</span></span>
- <span data-ttu-id="ee231-115">**FMLA**</span><span class="sxs-lookup"><span data-stu-id="ee231-115">**FMLA**</span></span>
- <span data-ttu-id="ee231-116">**Personel self servisi**</span><span class="sxs-lookup"><span data-stu-id="ee231-116">**Employee self service**</span></span>
- <span data-ttu-id="ee231-117">**Yönetici self servisi**</span><span class="sxs-lookup"><span data-stu-id="ee231-117">**Manager self service**</span></span>
- <span data-ttu-id="ee231-118">**Kazanç yönetimi**</span><span class="sxs-lookup"><span data-stu-id="ee231-118">**Benefits management**</span></span>
- <span data-ttu-id="ee231-119">**İzin ve devamsızlık**</span><span class="sxs-lookup"><span data-stu-id="ee231-119">**Leave and absence**</span></span>
- <span data-ttu-id="ee231-120">**Ödeme yöntemleri**</span><span class="sxs-lookup"><span data-stu-id="ee231-120">**Payment methods**</span></span>

<span data-ttu-id="ee231-121">Her sekme, tek bir şirketle ilgili bilgileri içerir.</span><span class="sxs-lookup"><span data-stu-id="ee231-121">Each tab contains information that pertains to a single company.</span></span>

## <a name="general"></a><span data-ttu-id="ee231-122">Genel</span><span class="sxs-lookup"><span data-stu-id="ee231-122">General</span></span>

<span data-ttu-id="ee231-123">**genel** sekmesindeki ayarlar, Devamsızlık, yaralanma ve hastalık ve yeni işe alma hakkında bilgi görünümünü belirler.</span><span class="sxs-lookup"><span data-stu-id="ee231-123">The settings on the **General** tab define the appearance of information about absence, injury and illness, and new hires.</span></span> <span data-ttu-id="ee231-124">Bu sekmedeki ayarlar, çalışırken görünen bazı varsayılan girdileri de tanımlar.</span><span class="sxs-lookup"><span data-stu-id="ee231-124">The settings on this tab also define some default entries that appear as you work.</span></span> <span data-ttu-id="ee231-125">Özellikle, bu sekme şunları sağlar:</span><span class="sxs-lookup"><span data-stu-id="ee231-125">Specifically, this tab lets you:</span></span>

- <span data-ttu-id="ee231-126">Açık devamsızlık hareketlerine uygulanacak rengi seçme</span><span class="sxs-lookup"><span data-stu-id="ee231-126">Select a color to apply to open absence transactions</span></span>
- <span data-ttu-id="ee231-127">Raporlar için kullanılacak stil sayfasını belirtme</span><span class="sxs-lookup"><span data-stu-id="ee231-127">Specify the style sheet to use for reports</span></span>
- <span data-ttu-id="ee231-128">Eğitim kursları ve devamsızlık kaydı arasındaki tümleştirmeyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="ee231-128">Enable the integration between training courses and absence registration</span></span>
- <span data-ttu-id="ee231-129">Bu tümleştirmeyi denetlemek için kullanılan devamsızlık kodunu seçme.</span><span class="sxs-lookup"><span data-stu-id="ee231-129">Select the absence code that is used to control this integration.</span></span>
- <span data-ttu-id="ee231-130">Yaralanma ve hastalık durumlarının ne kadar süreyle saklanılacağını belirtme.</span><span class="sxs-lookup"><span data-stu-id="ee231-130">Indicate how long to keep injury and illness case incidents.</span></span>
- <span data-ttu-id="ee231-131">Yeni bir çalışan işe alındığında gösterilen varsayılan kimlik numarasını belirtme.</span><span class="sxs-lookup"><span data-stu-id="ee231-131">Specify the default identification number shown when a new worker is hired.</span></span>

![Genel sekmesi](./media/hr-setup-parameters-general.png)

## <a name="recruitment"></a><span data-ttu-id="ee231-133">İşe alma</span><span class="sxs-lookup"><span data-stu-id="ee231-133">Recruitment</span></span>

<span data-ttu-id="ee231-134">**İşe Alım** sekmesindeki ayarlar, başvuru sahiplerine otomatik olarak gönderilen yazışmalar için kullanılan belge türlerini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="ee231-134">The settings on the **Recruitment** tab define the document types used for correspondence automatically sent to applicants.</span></span> <span data-ttu-id="ee231-135">Talep edilmemiş başvurular için kullanılan işe alım projesini de belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ee231-135">You can also indicate the recruitment project used for unsolicited applications.</span></span>

<span data-ttu-id="ee231-136">İşe alma projesi eskimesi için tanımlanan dönem, **İşe alma yönetimi** çalışma alanındaki **Eskiyen projeler** kutucuğuna dahil edilen işe alma projesini belirleyen işe alma projeleri belirler.</span><span class="sxs-lookup"><span data-stu-id="ee231-136">The period defined for recruitment project aging determines the recruitment projects included on the **Aging projects** tile in the **Recruitment management** workspace.</span></span> <span data-ttu-id="ee231-137">Uygulama son başvuru tarihi uyarısı için tanımlanan dönem **işe alma** çalışma alanındaki **son başvuru tarihi yaklaşan** döşemesindeki son başvuru tarihi yaklaşan işe alma projeleri görüntülemek için kullanılan uygulama son uyarısı için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ee231-137">The period defined for the application deadline warning is used to display recruitment projects that are approaching their application deadline on the **Application deadline approaching** tile in the **Recruitment** workspace.</span></span>

<span data-ttu-id="ee231-138">İşe alma hakkında daha fazla bilgi için bkz. [İş adaylarını işe alma](hr-personnel-recruit.md).</span><span class="sxs-lookup"><span data-stu-id="ee231-138">For more information about recruiting, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="compensation"></a><span data-ttu-id="ee231-139">Maaş</span><span class="sxs-lookup"><span data-stu-id="ee231-139">Compensation</span></span>

<span data-ttu-id="ee231-140">Dynamics 365 Finance'te **Ücret** sekmesindeki ayarlar, kullanıcının bir sabit veya değişken ücret planı bilgilerini kaydetmek istediklerini onaylamaları gerekip gerekmediğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="ee231-140">In Dynamics 365 Finance, the settings on the **Compensation** tab define whether users must confirm that they want to save information for a fixed or variable compensation plan.</span></span> <span data-ttu-id="ee231-141">**Kaydetme doğrulamasını etkinleştir**'i işaretlerseniz kullanıcılar ücretle ilgili bir sayfayı kapatmak istediklerinde kaydı kaydetmek isteyip istemediklerini soran bir ileti alır.</span><span class="sxs-lookup"><span data-stu-id="ee231-141">If you select **Enable save validation**, when users close a compensation-related page, they receive a message that asks whether they want to save the record.</span></span> <span data-ttu-id="ee231-142">Ücret yönetimindeki bazı sayfalar kullanıcıların bilgileri silmesine izin vermez.</span><span class="sxs-lookup"><span data-stu-id="ee231-142">Some pages in Compensation management don't let users delete information.</span></span> <span data-ttu-id="ee231-143">Kullanıcılardan bilgilerinin kaydedilmesini istediklerini doğrulamalarını isteyerek, kaydedilen daha sonra silinemez bilgi miktarını sınırlama olanağınız olabilir.</span><span class="sxs-lookup"><span data-stu-id="ee231-143">By prompting users to verify that they want to save information, you might be able to limit the amount of information that is saved but can't be deleted later.</span></span> <span data-ttu-id="ee231-144">**Kaydetme doğrulamasını etkinleştir** seçimini kaldırırsanız kayıtlar, büyük olasılıkla kullanıcı hazır olmadan önce hemen kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="ee231-144">If you clear **Enable save validation**, records save immediately, possibly before the user is ready.</span></span> <span data-ttu-id="ee231-145">Performans yönetimi'ni kullanıyorsanız **Ücret** sekmesi performansı değerlendirirken tazminat planlarına atanan model yerine bir değerlendirme modeli kullanmayı seçmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="ee231-145">If you're using Performance management, the **Compensation** tab also lets you select a rating model to use instead of the model assigned to compensation plans when rating performance.</span></span>

<span data-ttu-id="ee231-146">Human Resources'da, ücret planlarına erişimi kısıtlamayı ve varsayılan bir para birimi ayarlamayı seçmek için **Ücret** sekmesini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ee231-146">In Human Resources, you can use the **Compensation** tab to choose to restrict access to compensation plans and to set a default currency.</span></span>

<span data-ttu-id="ee231-147">Ücret hakkında daha fazla bilgi için bkz. [Ücret planlarına genel bakış](hr-compensation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ee231-147">For more information about compensation, see [Compensation plans overview](hr-compensation-overview.md).</span></span>

![Ücret sekmesi](./media/hr-setup-parameters-compensation.png)

## <a name="number-sequences"></a><span data-ttu-id="ee231-149">Numara serileri</span><span class="sxs-lookup"><span data-stu-id="ee231-149">Number sequences</span></span>

<span data-ttu-id="ee231-150">**Numara serisi** sekmesindeki ayarlar, Human Resources'daki öğelere otomatik olarak kimlik atamak için kullanılan sıraları belirler. Örneğin:</span><span class="sxs-lookup"><span data-stu-id="ee231-150">The settings on the **Number sequence** tab determine the sequences used to automatically assign IDs to items in Human Resources, such as:</span></span>

- <span data-ttu-id="ee231-151">Başvurular</span><span class="sxs-lookup"><span data-stu-id="ee231-151">Applications</span></span>
- <span data-ttu-id="ee231-152">Devamsızlık kayıtları</span><span class="sxs-lookup"><span data-stu-id="ee231-152">Absence registrations</span></span>
- <span data-ttu-id="ee231-153">Ücret işlemi sonuçları</span><span class="sxs-lookup"><span data-stu-id="ee231-153">Compensation process results</span></span>
- <span data-ttu-id="ee231-154">Servis talebi numaraları</span><span class="sxs-lookup"><span data-stu-id="ee231-154">Case numbers</span></span>
- <span data-ttu-id="ee231-155">Kurslar</span><span class="sxs-lookup"><span data-stu-id="ee231-155">Courses</span></span>
- <span data-ttu-id="ee231-156">Kurs konu başlıkları</span><span class="sxs-lookup"><span data-stu-id="ee231-156">Course agendas</span></span>

<span data-ttu-id="ee231-157">Numara serisi referanslarını ve kodlarını korumak için **Numara serileri** listesi sayfasını kullanın (**Kuruluş yönetimi > Numara serileri > Numara serileri**'ni seçin).</span><span class="sxs-lookup"><span data-stu-id="ee231-157">To maintain number sequence references and codes, use the **Number sequences** list page (select **Organization administration > Number sequences > Number sequences**).</span></span>

<span data-ttu-id="ee231-158">Daha fazla bilgi için bkz. [Numara serilerine genel bakış](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/human-resources/toc.json).</span><span class="sxs-lookup"><span data-stu-id="ee231-158">For more information, see [Number sequences overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/human-resources/toc.json).</span></span>

> [!NOTE]
> <span data-ttu-id="ee231-159">Çalışılan saat sayısı 1250'yi aşamaz ve 12 ay İstihdam uzunluğunu aşamaz.</span><span class="sxs-lookup"><span data-stu-id="ee231-159">The number of hours that are worked can't exceed 1,250, and the length of employment can't exceed 12 months.</span></span> <span data-ttu-id="ee231-160">Bu en büyük değerler Amerika Birleşik Devletleri'nde federal yasalara uygundur.</span><span class="sxs-lookup"><span data-stu-id="ee231-160">These maximum values are in accordance with federal law in the United States.</span></span>

![Numara serileri sekmesi](./media/hr-setup-parameters-number-sequences.png)

## <a name="fmla"></a><span data-ttu-id="ee231-162">FMLA</span><span class="sxs-lookup"><span data-stu-id="ee231-162">FMLA</span></span>

<span data-ttu-id="ee231-163">FMLA sekmesinde FMLA uygunluk gereksinimlerini ve FMLA destek hakkı saatlerini ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="ee231-163">On the FMLA tab, you set FMLA eligibility requirements and FMLA entitlement hours.</span></span> <span data-ttu-id="ee231-164">Daha fazla bilgi için bkz. [İzin ve devamsızlık parametreleri yapılandırma](hr-leave-and-absence-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ee231-164">For more information, see [Configure leave and absence parameters](hr-leave-and-absence-parameters.md).</span></span>

![FMLA sekmesi](./media/hr-setup-parameters-fmla.png)

## <a name="employee-self-service"></a><span data-ttu-id="ee231-166">Personel self servisi</span><span class="sxs-lookup"><span data-stu-id="ee231-166">Employee self service</span></span>

<span data-ttu-id="ee231-167">**Personel self servisi** sekmesindeki ayarlar, Personel self servisi'nin personele nasıl görüneceğine etki eder.</span><span class="sxs-lookup"><span data-stu-id="ee231-167">The settings on the **Employee self service** tab affect how Employee self service appears to employees.</span></span> <span data-ttu-id="ee231-168">Bu sekmede şunları yapabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="ee231-168">On this tab, you can:</span></span>

- <span data-ttu-id="ee231-169">Personel self servisi çalışma alanı için ad girme</span><span class="sxs-lookup"><span data-stu-id="ee231-169">Enter a name for the Employee self service workspace</span></span>
- <span data-ttu-id="ee231-170">Yöneticinin çalışanlar için hangi bilgileri girebileceğini seçme</span><span class="sxs-lookup"><span data-stu-id="ee231-170">Select which information a manager can enter for employees</span></span>
- <span data-ttu-id="ee231-171">Çalışanlar için yararlı bağlantılar ekleme</span><span class="sxs-lookup"><span data-stu-id="ee231-171">Add useful links for employees</span></span>
- <span data-ttu-id="ee231-172">Çalışanların iletişim bilgilerini eklemelerini veya düzenlemelerini kısıtlama.</span><span class="sxs-lookup"><span data-stu-id="ee231-172">Restrict employees from adding or editing business contact details.</span></span> <span data-ttu-id="ee231-173">Daha fazla bilgi için bkz. [Kişisel bilgileri düzenlemeyi kısıtlama](hr-employee-self-service-restrict-editing.md).</span><span class="sxs-lookup"><span data-stu-id="ee231-173">For more information, see [Restrict editing of personal information](hr-employee-self-service-restrict-editing.md).</span></span>

<span data-ttu-id="ee231-174">Personel self servisi'ni ayarlama hakkında daha fazla bilgi için bkz. [Personel ve Yönetici self servisi'ne genel bakış](hr-employee-manager-self-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ee231-174">For more information about setting up Employee self service, see [Employee and Manager self service overview](hr-employee-manager-self-service-overview.md).</span></span>

![Personel self servisi sekmesi](./media/hr-setup-parameters-employee-self-service.png)

## <a name="manager-self-service"></a><span data-ttu-id="ee231-176">Yönetici self servis</span><span class="sxs-lookup"><span data-stu-id="ee231-176">Manager self service</span></span>

<span data-ttu-id="ee231-177">**Yönetici self servisi** sekmesindeki ayarlar, yöneticilerin Yönetici self servisinde neler gördüğünü etkiler.</span><span class="sxs-lookup"><span data-stu-id="ee231-177">The settings on the **Manager self service** tab affect what managers see in Manager self service.</span></span> <span data-ttu-id="ee231-178">Bu sekmede aşağıdaki seçenekleri yapılandırabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="ee231-178">On this tab, you can configure the following options:</span></span>

- <span data-ttu-id="ee231-179">Süresi dolan kayıtlar için aralık</span><span class="sxs-lookup"><span data-stu-id="ee231-179">The range for expiring records</span></span>
- <span data-ttu-id="ee231-180">Bilgi yöneticileri süresi dolan kayıtları görüntüleyebilir</span><span class="sxs-lookup"><span data-stu-id="ee231-180">Information managers can view in expiring records</span></span>
- <span data-ttu-id="ee231-181">Yöneticilerin genişletilmiş raporlar için açık pozisyonları görüntüleyip görüntüleyemeyeceği</span><span class="sxs-lookup"><span data-stu-id="ee231-181">Whether managers can view open positions for extended reports</span></span>
- <span data-ttu-id="ee231-182">Çıkış yapan çalışanların görünümleri</span><span class="sxs-lookup"><span data-stu-id="ee231-182">Views of exiting workers</span></span>
- <span data-ttu-id="ee231-183">Yöneticiler için yararlı bağlantılar</span><span class="sxs-lookup"><span data-stu-id="ee231-183">Useful links for managers</span></span>

<span data-ttu-id="ee231-184">Yönetici self servisi'ni ayarlama hakkında daha fazla bilgi için bkz. [Personel ve Yönetici self servisi'ne genel bakış](hr-employee-manager-self-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ee231-184">For more information about setting up Manager self service, see [Employee and Manager self service overview](hr-employee-manager-self-service-overview.md).</span></span>

![Yönetici self servisi sekmesi](./media/hr-setup-parameters-manager-self-service.png)

## <a name="benefits-management"></a><span data-ttu-id="ee231-186">Kazanç yönetimi</span><span class="sxs-lookup"><span data-stu-id="ee231-186">Benefits management</span></span>

<span data-ttu-id="ee231-187">Kazanç yönetimi sekmesinde, Kazanç yönetimi için e-posta seçeneklerini yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ee231-187">On the Benefits management tab, you can configure email options for Benefits management.</span></span> <span data-ttu-id="ee231-188">Kazanç yönetimini ayarlama ve kullanma hakkında bilgi için bkz. [Kazanç yönetimine genel bakış](hr-benefits-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ee231-188">For information about setting up and using Benefits management, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

![Kazanç yönetimi sekmesi](./media/hr-setup-parameters-benefits-management.png)

## <a name="leave-and-absence"></a><span data-ttu-id="ee231-190">İzin ve devamsızlık</span><span class="sxs-lookup"><span data-stu-id="ee231-190">Leave and absence</span></span>

<span data-ttu-id="ee231-191">İzin ve devamsızlığı ayarlama ve kullanma hakkında daha fazla bilgi için bkz. [İzin ve devamsızlığa genel bakış](hr-leave-and-absence-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ee231-191">For information about setting up and using Leave and absence, see [Leave and absence overview](hr-leave-and-absence-overview.md).</span></span>

## <a name="payment-methods"></a><span data-ttu-id="ee231-192">Ödeme yöntemleri</span><span class="sxs-lookup"><span data-stu-id="ee231-192">Payment methods</span></span>

<span data-ttu-id="ee231-193">**Ödeme yöntemleri** sekmesinde, kuruluşunuz tarafından desteklenen ödeme yöntemlerini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ee231-193">On the **Payment methods** tab, you can select the payment methods supported by your organization.</span></span> <span data-ttu-id="ee231-194">Ücretleri yapılandırma hakkında daha fazla bilgi için bkz. [Ücret planlarına genel bakış](hr-compensation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ee231-194">For more information about configuring compensation, see [Compensation plans overview](hr-compensation-overview.md).</span></span>

![Ödeme yöntemleri sekmesi](./media/hr-setup-parameters-payment-methods.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]