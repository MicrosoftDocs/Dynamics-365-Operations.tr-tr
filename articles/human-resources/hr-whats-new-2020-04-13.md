---
title: Dynamics 365 Human Resources'deki yenilikler veya değişiklikler (13 Nisan 2020)
description: Bu makalede, 13 Nisan 2020 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 4/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a7ea8348cfe1c66d6d0cfa39b46c8e69111fe185
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528533"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a><span data-ttu-id="cb737-103">Dynamics 365 Human Resources'deki yenilikler veya değişiklikler (13 Nisan 2020)</span><span class="sxs-lookup"><span data-stu-id="cb737-103">What's new or changed in Dynamics 365 Human Resources (April 13, 2020)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="cb737-104">Bu makalede Dynamics 365 Human Resources'te yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="cb737-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="cb737-105">Değişiklikler derleme numarası 8.1.3136 uygulanır.</span><span class="sxs-lookup"><span data-stu-id="cb737-105">Changes apply to build number 8.1.3136.</span></span> <span data-ttu-id="cb737-106">Bazı başlıklardaki parantez içindeki numaralar referans için LCS destek numaralarına referans verir.</span><span class="sxs-lookup"><span data-stu-id="cb737-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="new-production-release-cadence"></a><span data-ttu-id="cb737-107">Yeni üretim sürümü temposu</span><span class="sxs-lookup"><span data-stu-id="cb737-107">New production release cadence</span></span>

<span data-ttu-id="cb737-108">Bu haftanın sürümüyle, Human Resources sürüm temposu bir haftalık güncelleştirmeden iki haftada bir güncelleştirme olacak şekilde değişecektir.</span><span class="sxs-lookup"><span data-stu-id="cb737-108">With this week's release, the release cadence for Human Resources shifts from a weekly update to a biweekly update.</span></span> <span data-ttu-id="cb737-109">Güvenli dağıtım uygulamalarıyla uyumu sağlamak ve hizmette yüksek kararlılık ve güvenilirlik standartlarını korumak için, tüm bölgelere hizmet güncelleştirmelerini dağıtma işlemi artık iki haftalık bir dağıtım olacaktır.</span><span class="sxs-lookup"><span data-stu-id="cb737-109">To ensure alignment with safe deployment practices, and maintain high standards of stability and reliability in the service, the process of deploying service updates to all regions is now a two-week rollout.</span></span> <span data-ttu-id="cb737-110">İşlemin her aşamasında başarılı dağıtımı doğrulamak için ek test ve izleyiciler bulunur.</span><span class="sxs-lookup"><span data-stu-id="cb737-110">Additional testing and monitors are in place to verify successful deployment at each stage of the process.</span></span> <span data-ttu-id="cb737-111">Sürüm temposu hakkında daha fazla bilgi için bkz. [Güncelleştirme işlemi](hr-admin-setup-update-process.md).</span><span class="sxs-lookup"><span data-stu-id="cb737-111">For more information on the release cadence, see [Update process](hr-admin-setup-update-process.md).</span></span>

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a><span data-ttu-id="cb737-112">Yuvarlama hassasiyeti alanı bir Yuvarlama türü belirttikten sonra düzenlenemez (435616)</span><span class="sxs-lookup"><span data-stu-id="cb737-112">Rounding precision field isn't editable after specifying a Rounding type (435616)</span></span>

<span data-ttu-id="cb737-113">Bu değişiklikle, **Yuvarlama hassasiyeti** alanı şimdi **Yuvarlama türü** alanını güncelleştirdikten sonra kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="cb737-113">With this change, the **Rounding precision** field is now available after you update the **Rounding type** field.</span></span>

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a><span data-ttu-id="cb737-114">İzin planı tahakkuk dönemi içermiyorsa, izin kaydı bitiş tarihi düzenlenemiyor (413628)</span><span class="sxs-lookup"><span data-stu-id="cb737-114">Can't edit leave enrollment end date when the leave plan doesn't have accrual periods (413628)</span></span>

<span data-ttu-id="cb737-115">Artık kayıt bitiş tarihini, "Alan tahakkuk tarihi esası doldurulmalıdır" hatasını almadan düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb737-115">You can now edit the enrollment end date without getting the error "Field Accrual date basis must be filled in."</span></span>

## <a name="employment-entity-doesnt-sync-to-common-data-service-430834"></a><span data-ttu-id="cb737-116">İstihdam varlığı Common Data Service ile eşitlenmiyor (430834)</span><span class="sxs-lookup"><span data-stu-id="cb737-116">Employment entity doesn't sync to Common Data Service (430834)</span></span>

<span data-ttu-id="cb737-117">Bu değişiklik, mali boyutlar eklendikten sonra istihdam verilerinin Common Data Service eşitlenmemesine yol açan bir sorunu düzeltir.</span><span class="sxs-lookup"><span data-stu-id="cb737-117">This change corrects an issue where the employment data wasn't syncing to Common Data Service after adding financial dimensions.</span></span> 

## <a name="remove-multi-parenting-for-work-calendar-time-interval-entity-431775"></a><span data-ttu-id="cb737-118">İş Takvimi Zaman Aralığı varlığı için birden çok üst düzeyi kaldır (431775)</span><span class="sxs-lookup"><span data-stu-id="cb737-118">Remove multi-parenting for Work Calendar Time Interval entity (431775)</span></span>

<span data-ttu-id="cb737-119">Bu değişiklik, **İş Takvimi Zaman Aralığı** varlığı için birden çok üst düzeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cb737-119">This change removes multi-parenting for the **Work Calendar Time Interval** entity.</span></span>

## <a name="filter-with-cast-function-doesnt-work-on-odata-call-position-worker-assignment-entity-431699"></a><span data-ttu-id="cb737-120">CAST işlevi ile filtre uygulama OData çağrısı Pozisyona Çalışan Atama varlığı üzerinde çalışmıyor (431699)</span><span class="sxs-lookup"><span data-stu-id="cb737-120">Filter with CAST function doesn't work on OData call Position Worker Assignment entity (431699)</span></span>

<span data-ttu-id="cb737-121">Bu güncelleştirme, OData içindeki CAST işlevine **Pozisyon Çalışan Ataması** varlığı filtre uygulama izni veren bir değişiklik içerir.</span><span class="sxs-lookup"><span data-stu-id="cb737-121">This update includes a change to allow  filter with CAST function within OData for the **Position Worker Assignment** entity.</span></span>

## <a name="in-preview"></a><span data-ttu-id="cb737-122">Ön izlemede</span><span class="sxs-lookup"><span data-stu-id="cb737-122">In Preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="cb737-123">İzni askıya alma</span><span class="sxs-lookup"><span data-stu-id="cb737-123">Leave suspension</span></span>

<span data-ttu-id="cb737-124">Human Resources'ta bir çalışan için izin ve devamsızlığı askıya alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb737-124">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="cb737-125">İzni askıya alma, seçili izin türleri için izin tahakkuklarını durdurur.</span><span class="sxs-lookup"><span data-stu-id="cb737-125">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="cb737-126">Askıya alma bir tahakkuk işleminden sonra gerçekleştiyse, askıya alınan izin çalışanın izin bakiyesinde eşit dağıtılmış bir ayarlama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cb737-126">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="cb737-127">Daha fazla bilgi için bkz. [İzni askıya alma](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="cb737-127">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="cb737-128">Devretme kuralları</span><span class="sxs-lookup"><span data-stu-id="cb737-128">Carry forward rules</span></span>

<span data-ttu-id="cb737-129">Örneğin, devretme ayarlamalarının transfer edildiği devir bakiyeleri için bir devretme izin türü belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb737-129">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="cb737-130">Örneğin, bir çalışan 10 günü ileri taşıyorsa, bu 10 gün için farklı bir izin türü seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb737-130">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="cb737-131">Daha fazla bilgi için bkz. [İzin ve devamsızlık türleri yapılandırma](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="cb737-131">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="cb737-132">Bilinen sorunlar</span><span class="sxs-lookup"><span data-stu-id="cb737-132">Known issues</span></span>

## <a name="employment-details-entity"></a><span data-ttu-id="cb737-133">İstihdam Ayrıntıları varlığı</span><span class="sxs-lookup"><span data-stu-id="cb737-133">Employment Details entity</span></span>

<span data-ttu-id="cb737-134">**İstihdam Ayrıntısı** varlığı aşağıdaki alanlarla güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="cb737-134">The **Employment Detail** entity has been updated with the following fields:</span></span>

- <span data-ttu-id="cb737-135">**PayFrequency**</span><span class="sxs-lookup"><span data-stu-id="cb737-135">**PayFrequency**</span></span>
- <span data-ttu-id="cb737-136">**İstihdam Kategorisi Kodu**</span><span class="sxs-lookup"><span data-stu-id="cb737-136">**Employment Category ID**</span></span>
- <span data-ttu-id="cb737-137">**İstihdam Türü**</span><span class="sxs-lookup"><span data-stu-id="cb737-137">**Employment Type**</span></span>
- <span data-ttu-id="cb737-138">**EmploymentType Kodu**</span><span class="sxs-lookup"><span data-stu-id="cb737-138">**EmploymentType ID**</span></span>
- <span data-ttu-id="cb737-139">**Kazanç İstihdam Durumu**</span><span class="sxs-lookup"><span data-stu-id="cb737-139">**Benefit Employment Status**</span></span>

<span data-ttu-id="cb737-140">Bu alanların kurulum verileri, **Özellik yönetimi** çalışma alanında etkinleştirilen kazanç yönetimine bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="cb737-140">The setup data for these fields rely on benefits management being enabled in the **Feature management** workspace.</span></span> <span data-ttu-id="cb737-141">İçe aktarma sırasında hatalara neden olacağından, bu alanları **İstihdam Ayrıntısı** varlığında doldurmayın veya güncelleştirmeyin.</span><span class="sxs-lookup"><span data-stu-id="cb737-141">Don't populate or update these fields in the **Employment Detail** entity, because it will result in errors during import.</span></span>

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a><span data-ttu-id="cb737-142">SharePoint Önizleme bazı ortamlarda çalışmıyor</span><span class="sxs-lookup"><span data-stu-id="cb737-142">SharePoint preview doesn't work in some environments</span></span>

<span data-ttu-id="cb737-143">SharePoint'te depolanan belgelere ait belge önizlemesi çalışmazsa, aşağıdaki yordamı deneyin:</span><span class="sxs-lookup"><span data-stu-id="cb737-143">If document preview for documents stored in SharePoint doesn't work, try the following procedure:</span></span>

1. <span data-ttu-id="cb737-144">Yönetici Kullanıcı hesabının kullanıcı kaydıyla ilişkili bir e-posta olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="cb737-144">Verify the Admin user account has an email associated with the user record.</span></span> <span data-ttu-id="cb737-145">Bu bilgileri **Kullanıcı** sayfasında görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb737-145">You can view this information in the **User** page.</span></span> <span data-ttu-id="cb737-146">E-posta ayarlanmamışsa, OData Excel eklentisi ile e-posta ve sağlayıcı eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="cb737-146">If email isn't set up, you need to add the email and provider with the OData Excel add-in.</span></span> <span data-ttu-id="cb737-147">Varsayılan olarak, e-posta adresi Excel tasarımında bulunmaz.</span><span class="sxs-lookup"><span data-stu-id="cb737-147">By default, the email address isn't present in the Excel design.</span></span> <span data-ttu-id="cb737-148">Excel tasarımını düzenlemeniz, tüm alanları eklemeniz, uygulamanız ve yenilemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="cb737-148">You'll need to edit the Excel design, add all fields, apply, and refresh.</span></span> <span data-ttu-id="cb737-149">Bu adımları tamamladıktan sonra, yönetici hesabını güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb737-149">Once you've completed those steps, you can update the admin account.</span></span>

2. <span data-ttu-id="cb737-150">Yönetici hesabının ilişkili bir e-posta hesabı varsa, yönetici kimlik bilgileriyle İnsan Kaynakları için oturum açın.</span><span class="sxs-lookup"><span data-stu-id="cb737-150">After the Admin account has an associated email account, sign in to Human Resources with Admin credentials.</span></span>

3. <span data-ttu-id="cb737-151">Belge önizlemesini başlatmak için SharePoint ' deki bir eke erişin.</span><span class="sxs-lookup"><span data-stu-id="cb737-151">Access an attachment in SharePoint to start the document preview.</span></span>

4. <span data-ttu-id="cb737-152">Eklere erişimi olan başka bir kullanıcı hesabıyla oturum açın ve önizlemenin beklendiği gibi çalıştığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="cb737-152">Sign in with another user account that has access to attachments and verify that the preview works as expected.</span></span>

## <a name="see-also"></a><span data-ttu-id="cb737-153">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="cb737-153">See also</span></span>

[<span data-ttu-id="cb737-154">Human Resources'taki yenilikler veya değişiklikler</span><span class="sxs-lookup"><span data-stu-id="cb737-154">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="cb737-155">Dynamics 365 Human Resources 2019 sürüm 2'ye genel bakış</span><span class="sxs-lookup"><span data-stu-id="cb737-155">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="cb737-156">Güncelleştirme işlemi</span><span class="sxs-lookup"><span data-stu-id="cb737-156">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="cb737-157">Özellikleri yönetme</span><span class="sxs-lookup"><span data-stu-id="cb737-157">Manage features</span></span>](hr-admin-manage-features.md)