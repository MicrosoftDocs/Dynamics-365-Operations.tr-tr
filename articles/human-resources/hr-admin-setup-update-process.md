---
title: Güncelleştirme işlemi
description: Microsoft Dynamics 365 Human Resources uygulama ve platform değişiklikleri için sürekli, temassız servis güncelleştirmeleri sağlayan gerçek bir hizmet olarak yazılımdır (SaaS).
author: andreabichsel
manager: tfehr
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 27561bfd9cb4f115cc507954c837ea93f9c93b72
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466844"
---
# <a name="update-process"></a><span data-ttu-id="d41f4-103">Güncelleştirme işlemi</span><span class="sxs-lookup"><span data-stu-id="d41f4-103">Update process</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d41f4-104">Microsoft Dynamics 365 Human Resources, sürekli, temassız servis güncelleştirmeleri sağlayan gerçek bir hizmet olarak yazılımdır (SaaS).</span><span class="sxs-lookup"><span data-stu-id="d41f4-104">Microsoft Dynamics 365 Human Resources is a true software as a service (SaaS) that provides continuous, touchless service updates.</span></span> <span data-ttu-id="d41f4-105">Bu güncelleştirmeler, yasal güncelleştirmeler de dahil olmak üzere hizmette kritik geliştirmeler sağlayan uygulama ve platform değişikliklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="d41f4-105">These updates contain both application and platform changes that often provide critical improvements to the service, including regulatory updates.</span></span>

## <a name="update-policy"></a><span data-ttu-id="d41f4-106">Güncelleştirme ilkesi</span><span class="sxs-lookup"><span data-stu-id="d41f4-106">Update policy</span></span>

<span data-ttu-id="d41f4-107">Güncelleştirmeler düzenli aralıklarla yayımlanır ve tüm ortamlar için yapılır.</span><span class="sxs-lookup"><span data-stu-id="d41f4-107">Updates are released on a regular cadence to all environments.</span></span> <span data-ttu-id="d41f4-108">İnsan Kaynakları, ürün destek kullanılabilirliği hakkında düzenli ve öngörülebilir kılavuzlar sunan [Microsoft Lifecycle ilkesi](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy) ile uygun olarak desteklenir.</span><span class="sxs-lookup"><span data-stu-id="d41f4-108">Human Resources is supported according to the [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), which provides consistent and predictable guidelines for the availability of support.</span></span>

## <a name="release-cadence"></a><span data-ttu-id="d41f4-109">Sürüm temposu</span><span class="sxs-lookup"><span data-stu-id="d41f4-109">Release cadence</span></span> 

<span data-ttu-id="d41f4-110">İnsan Kaynakları güncelleştirmeler otomatik olarak tüm ortamlara uygulanır.</span><span class="sxs-lookup"><span data-stu-id="d41f4-110">Human Resources updates are applied to all environments automatically.</span></span> <span data-ttu-id="d41f4-111">İnsan Kaynakları iki tür sürüm sağlar:</span><span class="sxs-lookup"><span data-stu-id="d41f4-111">Human Resources provides two types of releases:</span></span>

- <span data-ttu-id="d41f4-112">**Hizmet güncelleştirmeleri**: Güncellemeler, hata düzeltmeleri ve yeni özellikler içererek iki haftada bir yapılır.</span><span class="sxs-lookup"><span data-stu-id="d41f4-112">**Service updates**: Updates occur every two weeks that include bug fixes and new features.</span></span> <span data-ttu-id="d41f4-113">Hizmet güncelleştirmeleri, serbest bıraktıklarında uygun platform güncelleştirmelerini de içerir.</span><span class="sxs-lookup"><span data-stu-id="d41f4-113">Service updates also include applicable Platform updates when they release.</span></span> <span data-ttu-id="d41f4-114">Platform güncelleştirmelerinin ne zaman yayınlanacaklarını öğrenmek için [Tablo 3: Platform yayımları](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases)'na bakın.</span><span class="sxs-lookup"><span data-stu-id="d41f4-114">To get an idea of when Platform updates are released, see [Table 3: Platform releases](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span></span> <span data-ttu-id="d41f4-115">İki Haftalık Güncelleştirmeler, bölgeler arasında aşamalı genel bir piyasaya sahiptir.</span><span class="sxs-lookup"><span data-stu-id="d41f4-115">Biweekly updates have a staged global rollout across regions.</span></span> <span data-ttu-id="d41f4-116">İki Haftalık güncellemeler hakkında daha fazla bilgi için bkz. [Dynamics 365 Human Resources'ta yenilikler veya değişiklikler](hr-admin-whats-new.md).</span><span class="sxs-lookup"><span data-stu-id="d41f4-116">For more information about biweekly updates, see [What's new or changed in Dynamics 365 Human Resources](hr-admin-whats-new.md).</span></span>

    <span data-ttu-id="d41f4-117">Aksi belirtilmedikçe, tüm desteklenen veri merkezleri iki haftalık olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="d41f4-117">All supported data centers update every two weeks, unless otherwise noted.</span></span> <span data-ttu-id="d41f4-118">ABD, Avustralya, Avrupa, Birleşik Krallık, Asya ve Kanada bölgeleri iki haftalık güncelleştirmelere dahil edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="d41f4-118">US, Australia, Europe, UK, Asia, and Canada regions are included in biweekly updates.</span></span> 

- <span data-ttu-id="d41f4-119">**Dataverse çözüm güncelleştirmeleri**: Bu güncelleştirmeler gerektiğinde yaklaşık altı haftada bir gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="d41f4-119">**Dataverse solution updates**: These updates occur approximately every six weeks, as needed.</span></span> <span data-ttu-id="d41f4-120">Bunlar yeni varlıkları ve Dataverse'deki varolan varlıklara yapılan değişiklikleri içerir.</span><span class="sxs-lookup"><span data-stu-id="d41f4-120">They include new entities and changes to existing entities in Dataverse.</span></span> <span data-ttu-id="d41f4-121">Bu güncelleştirmeler iki haftalık güncelleştirmelerle aynı bölgeler için serbest çalışırlar ve tüm veri merkezleri arasında yineleme yapmak için altı hafta sürer.</span><span class="sxs-lookup"><span data-stu-id="d41f4-121">These updates release to the same regions as the biweekly updates, and they take about six weeks to replicate through all data centers.</span></span> <span data-ttu-id="d41f4-122">Çözüm güncelleştirmeleri iki haftalık hizmet güncelleştirmelerine göre hizalanmayabilir veya bunları hizalamayabilir.</span><span class="sxs-lookup"><span data-stu-id="d41f4-122">Solution updates may or may not align with biweekly service updates.</span></span>

> [!NOTE]
> <span data-ttu-id="d41f4-123">Çözüm güncelleştirmeleri, serbest bırakıldıktan sonra tüm veri merkezlerinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d41f4-123">Solution updates are available on all data centers once they're released.</span></span> <span data-ttu-id="d41f4-124">Güncelleştirmelerin otomatik olarak çoğaltılmasını beklemek istemezseniz, bu güncelleştirmeleri herhangi bir veri merkezindeki herhangi bir ortama el ile uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d41f4-124">If you don't want to wait for the updates to replicate automatically, you can manually apply these updates on any environment in any data center.</span></span>

<span data-ttu-id="d41f4-125">Gerektiğinde, İnsan Kaynakları aşağıdaki düzeltme türlerini de sağlar:</span><span class="sxs-lookup"><span data-stu-id="d41f4-125">When needed, Human Resources also provides the following types of fixes:</span></span>

- <span data-ttu-id="d41f4-126">**Düzeltme (düzeltme)**: İki haftada bir hizmet güncelleştirme sürümü ile veya bu sürümden ayrı olarak oluşabilecek hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="d41f4-126">**Revision (hotfix)**: Bug fixes that can occur either with or apart from a biweekly service update release</span></span>

- <span data-ttu-id="d41f4-127">**Acil durum düzeltmesi**: tek başına yapıdaki proaktif ve reaktif düzeltmeler, canlı site sorunlarını gidermek için yalnızca konfigürasyon veya kod değişikliklerini içerebilir ve iki haftalık bir Servis Güncelleştirmesi sürümünden ayrı olarak oluşabilir</span><span class="sxs-lookup"><span data-stu-id="d41f4-127">**Emergency fix**: Proactive and reactive hotfixes that are standalone in nature, can include configuration-only or code changes to resolve live site issues, and can occur apart from a biweekly service update release</span></span>

<span data-ttu-id="d41f4-128">Sürümler bir iç ortam üzerinde gözden geçirilip test edildiğini ve doğrulanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d41f4-128">Releases are reviewed, tested, and validated on an internal environment.</span></span> <span data-ttu-id="d41f4-129">Yapılar imzalandıktan sonra üretime dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="d41f4-129">After builds are signed off, they're then deployed to production.</span></span>

## <a name="release-cadence-exceptions-in-2020"></a><span data-ttu-id="d41f4-130">2020 içinde sürüm temposu özel durumları</span><span class="sxs-lookup"><span data-stu-id="d41f4-130">Release cadence exceptions in 2020</span></span>

<span data-ttu-id="d41f4-131">Tatilleri hesaba eklemek için, Kasım ve Aralık 2020 için sürüm planı aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="d41f4-131">To account for holidays, the release schedule for November and December 2020 is as follows:</span></span>

- <span data-ttu-id="d41f4-132">Kasım sürümü: 2 Kasım - 13 Kasım</span><span class="sxs-lookup"><span data-stu-id="d41f4-132">November release: November 2 - November 13</span></span>
- <span data-ttu-id="d41f4-133">Aralık sürümü: 30 Kasım - 11 Aralık</span><span class="sxs-lookup"><span data-stu-id="d41f4-133">December release: November 30 - December 11</span></span>
 
<span data-ttu-id="d41f4-134">İki haftalık sürüm temposu 11 Ocak 2021'de her zamanki gibi devam ettirilecektir.</span><span class="sxs-lookup"><span data-stu-id="d41f4-134">The two-week release cadence will resume as usual on January 11, 2021.</span></span>

## <a name="communications"></a><span data-ttu-id="d41f4-135">İletişim</span><span class="sxs-lookup"><span data-stu-id="d41f4-135">Communications</span></span>

<span data-ttu-id="d41f4-136">İnsan Kaynaklarıyla ilgili neler olduğunu ve aşağıdaki konumlarda yayımladığımız neleri öğrenebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="d41f4-136">You can find out what's in the works for Human Resources and what we've released in the following locations:</span></span>

- [<span data-ttu-id="d41f4-137">Dynamics 365 Human Resources Yol haritası</span><span class="sxs-lookup"><span data-stu-id="d41f4-137">Dynamics 365 Human Resources roadmap</span></span>](https://dynamics.microsoft.com/roadmap/human-resources/)

- [<span data-ttu-id="d41f4-138">Dynamics 365 sürüm planları</span><span class="sxs-lookup"><span data-stu-id="d41f4-138">Dynamics 365 Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans/)

- [<span data-ttu-id="d41f4-139">Dynamics 365 Human Resources'teki yenilikler veya değişiklikler</span><span class="sxs-lookup"><span data-stu-id="d41f4-139">What's new or changed in Dynamics 365 Human Resources</span></span>](hr-admin-whats-new.md)

- <span data-ttu-id="d41f4-140">[Lifecycle Services'de (LCS) Sorun arama](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (yalnızca platform ile ilgili hatalar için)</span><span class="sxs-lookup"><span data-stu-id="d41f4-140">[Issue search in Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (for Platform-related bugs only)</span></span>

- [<span data-ttu-id="d41f4-141">İnsan kaynakları blogu</span><span class="sxs-lookup"><span data-stu-id="d41f4-141">Human Resources blog</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [<span data-ttu-id="d41f4-142">İnsan Kaynakları Yammer topluluğu</span><span class="sxs-lookup"><span data-stu-id="d41f4-142">Human Resources Yammer community</span></span>](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a><span data-ttu-id="d41f4-143">Korumalı alan ortamındaki Önizleme özellikleri</span><span class="sxs-lookup"><span data-stu-id="d41f4-143">Preview features in a sandbox environment</span></span>

<span data-ttu-id="d41f4-144">Bir korumalı alan ortamındaki Önizleme özelliklerini, üretim ortamınızda etkinleştirmeden önce doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d41f4-144">You can validate preview features in a sandbox environment before enabling them in your production environment.</span></span> <span data-ttu-id="d41f4-145">Yeni özellikleri etkinleştirme hakkında daha fazla bilgi için [Özellik yönetimine genel bakış](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)'a bakın.</span><span class="sxs-lookup"><span data-stu-id="d41f4-145">For more information about enabling features, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>

<span data-ttu-id="d41f4-146">Tüm yeni özellikler en az 30 gün boyunca ve genellikle 30-60 gün önizlemede kalır.</span><span class="sxs-lookup"><span data-stu-id="d41f4-146">All new features remain in preview for at least 30 days, and typically 30-60 days.</span></span> <span data-ttu-id="d41f4-147">Önemli özellikler genellikle önizleme dönemini izleyen her yılın Ekim ve Nisan ayında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d41f4-147">Major features are generally available in October and April of each year following the preview period.</span></span> <span data-ttu-id="d41f4-148">Özellik yönetimi çalışma alanında yeni yetenekleri gördüğünüz anda bunları açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d41f4-148">As soon as you see new capabilities in the Feature management workspace, you can turn them on.</span></span> <span data-ttu-id="d41f4-149">Bazı özellikler varsayılan olarak açık olabilir.</span><span class="sxs-lookup"><span data-stu-id="d41f4-149">Some features may be on by default.</span></span>

<span data-ttu-id="d41f4-150">Bazen bir tümleştirme özelliği varsayılan olarak açıktır ve kapatılamaz (örneğin, Özellik yönetimi çalışma alanı).</span><span class="sxs-lookup"><span data-stu-id="d41f4-150">At times, an integral feature will be on by default and can't be turned off (for example, the Feature management workspace).</span></span>

<span data-ttu-id="d41f4-151">Bir özellik genel olarak kullanılabilir olduğunda üretim ortamlarında açılıp kapatılamayabilir.</span><span class="sxs-lookup"><span data-stu-id="d41f4-151">Once a feature is generally available, it may be turned on or off in production environments.</span></span> <span data-ttu-id="d41f4-152">Özellik yönetimi çalışma alanı bir önizleme özelliğinin zorunlu hale gelme zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d41f4-152">The Feature management workspace indicates when a preview feature will become mandatory.</span></span> <span data-ttu-id="d41f4-153">Bu tarih genellikle yarıyıllık sürüm planlarına uygun olacak şekilde 1 Ekim veya 1 Nisandır.</span><span class="sxs-lookup"><span data-stu-id="d41f4-153">This date is usually on October 1 or April 1 to align with the semiannual release plans.</span></span> <span data-ttu-id="d41f4-154">Zorunlu özellikleri kapatamazsınız.</span><span class="sxs-lookup"><span data-stu-id="d41f4-154">You can't turn off mandatory features.</span></span> <span data-ttu-id="d41f4-155">Bir özelliği zorunlu olana kadar tüm ortamlarda kapatıp açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d41f4-155">Until it becomes mandatory, you can turn a feature on and off in all environments.</span></span>

<span data-ttu-id="d41f4-156">Korumalı alan veya deneme ortamındaki özelliklerin önizlenmesini önemle öneririz.</span><span class="sxs-lookup"><span data-stu-id="d41f4-156">We highly recommend previewing features in a sandbox or trial environment.</span></span> <span data-ttu-id="d41f4-157">Verileriniz ile yeni özelliklerin eksiksiz deneyimini elde edebilmeniz için, geçerli üretim ortamınızın veya veritabanınızın bir kopyasını bir sandbox ortamına oluşturmak en iyisidir.</span><span class="sxs-lookup"><span data-stu-id="d41f4-157">It's best to create a copy of your current production environment or database into a sandbox environment so you can get the complete experience of the new features with your data.</span></span>

<span data-ttu-id="d41f4-158">Korumalı alan ortamının sağlanması hakkında daha fazla bilgi için, bkz. [İnsan Kaynakları projesi hazırlama](hr-admin-setup-provision.md).</span><span class="sxs-lookup"><span data-stu-id="d41f4-158">For more information about provisioning a sandbox environment, see [Provision a Human Resources project](hr-admin-setup-provision.md).</span></span> <span data-ttu-id="d41f4-159">Test ortamını kaldırmak için, bkz. [Örnek kaldırma](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span><span class="sxs-lookup"><span data-stu-id="d41f4-159">To remove a test environment, see [Remove an instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span></span> 

## <a name="report-bugs"></a><span data-ttu-id="d41f4-160">Hataları raporla</span><span class="sxs-lookup"><span data-stu-id="d41f4-160">Report bugs</span></span>

<span data-ttu-id="d41f4-161">Önizleme özellikleri test edilirken veya yeni yetenekler denerken, beklendiği gibi çalışmayan maddeler bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="d41f4-161">While testing preview features or trying new capabilities, you might find items that don't work as expected.</span></span> <span data-ttu-id="d41f4-162">Lütfen [Microsoft Dynamics 365 desteğiyle](https://dynamics.microsoft.com/support/) tüm hataları bildirin.</span><span class="sxs-lookup"><span data-stu-id="d41f4-162">Please report any bugs through [Microsoft Dynamics 365 support](https://dynamics.microsoft.com/support/).</span></span>

## <a name="see-also"></a><span data-ttu-id="d41f4-163">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="d41f4-163">See also</span></span>

[<span data-ttu-id="d41f4-164">Dynamics 365 ve Power Platform sürüm planları</span><span class="sxs-lookup"><span data-stu-id="d41f4-164">Dynamics 365 and Power Platform Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans)</br>
[<span data-ttu-id="d41f4-165">Dynamics 365 Human Resources'daki yenilikler veya değişiklikler</span><span class="sxs-lookup"><span data-stu-id="d41f4-165">What's new or changed in Dynamics 365 Human Resource</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="d41f4-166">Yazılım yaşam döngüsü ilkesi</span><span class="sxs-lookup"><span data-stu-id="d41f4-166">Software lifecycle policy</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)



[!INCLUDE[footer-include](../includes/footer-banner.md)]