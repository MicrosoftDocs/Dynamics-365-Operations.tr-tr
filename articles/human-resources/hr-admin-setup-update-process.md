---
title: Güncelleştirme işlemi
description: Microsoft Dynamics 365 Human Resources uygulama ve platform değişiklikleri için sürekli, temassız servis güncelleştirmeleri sağlayan gerçek bir hizmet olarak yazılımdır (SaaS).
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 267682f4497bacf70f93840a948d0e525dfa4aa1
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092213"
---
# <a name="update-process"></a><span data-ttu-id="caf26-103">Güncelleştirme işlemi</span><span class="sxs-lookup"><span data-stu-id="caf26-103">Update process</span></span>

<span data-ttu-id="caf26-104">Microsoft Dynamics 365 Human Resources, sürekli, temassız servis güncelleştirmeleri sağlayan gerçek bir hizmet olarak yazılımdır (SaaS).</span><span class="sxs-lookup"><span data-stu-id="caf26-104">Microsoft Dynamics 365 Human Resources is a true software as a service (SaaS) that provides continuous, touchless service updates.</span></span> <span data-ttu-id="caf26-105">Bu güncelleştirmeler, yasal güncelleştirmeler de dahil olmak üzere hizmette kritik geliştirmeler sağlayan uygulama ve platform değişikliklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="caf26-105">These updates contain both application and platform changes that often provide critical improvements to the service, including regulatory updates.</span></span>

## <a name="update-policy"></a><span data-ttu-id="caf26-106">Güncelleştirme ilkesi</span><span class="sxs-lookup"><span data-stu-id="caf26-106">Update policy</span></span>

<span data-ttu-id="caf26-107">Güncelleştirmeler düzenli aralıklarla yayımlanır ve tüm ortamlar için yapılır.</span><span class="sxs-lookup"><span data-stu-id="caf26-107">Updates are released on a regular cadence to all environments.</span></span> <span data-ttu-id="caf26-108">İnsan Kaynakları, ürün destek kullanılabilirliği hakkında düzenli ve öngörülebilir kılavuzlar sunan [Microsoft Lifecycle ilkesi](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy) ile uygun olarak desteklenir.</span><span class="sxs-lookup"><span data-stu-id="caf26-108">Human Resources is supported according to the [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), which provides consistent and predictable guidelines for the availability of support.</span></span>

## <a name="release-cadence"></a><span data-ttu-id="caf26-109">Sürüm temposu</span><span class="sxs-lookup"><span data-stu-id="caf26-109">Release cadence</span></span>

<span data-ttu-id="caf26-110">İnsan Kaynakları güncelleştirmeler otomatik olarak tüm ortamlara uygulanır.</span><span class="sxs-lookup"><span data-stu-id="caf26-110">Human Resources updates are applied to all environments automatically.</span></span> <span data-ttu-id="caf26-111">İnsan Kaynakları iki tür sürüm sağlar:</span><span class="sxs-lookup"><span data-stu-id="caf26-111">Human Resources provides two types of releases:</span></span>

- <span data-ttu-id="caf26-112">**Hizmet güncelleştirmeleri**: Hata düzeltmeleri ve yeni özellikler içeren Haftalık Güncelleştirmeler.</span><span class="sxs-lookup"><span data-stu-id="caf26-112">**Service updates**: Weekly updates that include bug fixes and new features.</span></span> <span data-ttu-id="caf26-113">Hizmet güncelleştirmeleri, serbest bıraktıklarında uygun platform güncelleştirmelerini de içerir.</span><span class="sxs-lookup"><span data-stu-id="caf26-113">Service updates also include applicable Platform updates when they release.</span></span> <span data-ttu-id="caf26-114">Platform güncelleştirmelerinin ne zaman yayınlanacaklarını öğrenmek için [Tablo 3: Platform yayımları](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases)'na bakın.</span><span class="sxs-lookup"><span data-stu-id="caf26-114">To get an idea of when Platform updates are released, see [Table 3: Platform releases](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span></span> <span data-ttu-id="caf26-115">Haftalık Güncelleştirmeler genellikle çarşamba günleri yayınlanır.</span><span class="sxs-lookup"><span data-stu-id="caf26-115">Weekly updates usually release on Wednesdays.</span></span> <span data-ttu-id="caf26-116">Haftalık güncellemeler hakkında daha fazla bilgi için bkz. [Dynamics 365 Human Resources'ta yenilikler veya değişiklikler](https://docs.microsoft.com/dynamics365/talent/whats-new).</span><span class="sxs-lookup"><span data-stu-id="caf26-116">For more information about weekly updates, see [What's new or changed in Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365/talent/whats-new).</span></span>

    <span data-ttu-id="caf26-117">Aksi belirtilmedikçe, tüm desteklenen veri merkezleri haftalık olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="caf26-117">All supported data centers update weekly, unless otherwise noted.</span></span> <span data-ttu-id="caf26-118">Haftalık Güncelleştirmeler tipik olarak Çarşamba günü başlar ve Pazar ile tamamlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="caf26-118">Weekly updates typically begin on Wednesday and complete by Sunday.</span></span> <span data-ttu-id="caf26-119">ABD, Avustralya, Avrupa, Birleşik Krallık, Asya ve Kanada bölgeleri haftalık güncelleştirmelere dahil edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="caf26-119">US, Australia, Europe, UK, Asia, and Canada regions are included in weekly updates.</span></span> 

- <span data-ttu-id="caf26-120">**Common Data Service çözüm güncelleştirmeleri**: Bu güncelleştirmeler gerektiğinde yaklaşık altı haftada bir gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="caf26-120">**Common Data Service solution updates**: These updates occur approximately every six weeks, as needed.</span></span> <span data-ttu-id="caf26-121">Bunlar yeni varlıkları ve Common Data Service'deki varolan varlıklara yapılan değişiklikleri içerir.</span><span class="sxs-lookup"><span data-stu-id="caf26-121">They include new entities and changes to existing entities in Common Data Service.</span></span> <span data-ttu-id="caf26-122">Bu güncelleştirmeler haftalık güncelleştirmelerle aynı bölgeler için serbest çalışırlar ve tüm veri merkezleri arasında yineleme yapmak için altı hafta sürer.</span><span class="sxs-lookup"><span data-stu-id="caf26-122">These updates release to the same regions as the weekly updates, and they take about six weeks to replicate through all data centers.</span></span> <span data-ttu-id="caf26-123">Çözüm güncelleştirmeleri haftalık hizmet güncelleştirmelerine göre hizalanmayabilir veya bunları hizalamayabilir.</span><span class="sxs-lookup"><span data-stu-id="caf26-123">Solution updates may or may not align with weekly service updates.</span></span>

<span data-ttu-id="caf26-124">Aşağıdaki tabloda örnek bir zamanlama gösterilmektedir:</span><span class="sxs-lookup"><span data-stu-id="caf26-124">The following table shows a sample schedule:</span></span>

| <span data-ttu-id="caf26-125">Hafta</span><span class="sxs-lookup"><span data-stu-id="caf26-125">Week</span></span> | <span data-ttu-id="caf26-126">Güncelleştirme türü</span><span class="sxs-lookup"><span data-stu-id="caf26-126">Update type</span></span> |
| --- | --- |
| <span data-ttu-id="caf26-127">1</span><span class="sxs-lookup"><span data-stu-id="caf26-127">1</span></span> | <span data-ttu-id="caf26-128">Hizmet güncelleştirmesi (tüm bölgeler)</span><span class="sxs-lookup"><span data-stu-id="caf26-128">Service update (all regions)</span></span> |
| <span data-ttu-id="caf26-129">2</span><span class="sxs-lookup"><span data-stu-id="caf26-129">2</span></span> | <span data-ttu-id="caf26-130">Hizmet güncelleştirmesi (tüm bölgeler) + çözüm Güncelleştirmesi (haftalık 1 bölge)</span><span class="sxs-lookup"><span data-stu-id="caf26-130">Service update (all regions) + Solution update (Week 1 regions)</span></span> |
| <span data-ttu-id="caf26-131">3</span><span class="sxs-lookup"><span data-stu-id="caf26-131">3</span></span> | <span data-ttu-id="caf26-132">Hizmet güncelleştirmesi (tüm bölgeler) + çözüm Güncelleştirmesi (haftalık 2 bölge)</span><span class="sxs-lookup"><span data-stu-id="caf26-132">Service update (all regions) + Solution update (Week 2 regions)</span></span> |
| <span data-ttu-id="caf26-133">4</span><span class="sxs-lookup"><span data-stu-id="caf26-133">4</span></span> | <span data-ttu-id="caf26-134">Hizmet güncelleştirmesi (tüm bölgeler) + çözüm Güncelleştirmesi (haftalık 3 bölge)</span><span class="sxs-lookup"><span data-stu-id="caf26-134">Service update (all regions) + Solution update (Week 3 regions)</span></span> |
| <span data-ttu-id="caf26-135">5</span><span class="sxs-lookup"><span data-stu-id="caf26-135">5</span></span> | <span data-ttu-id="caf26-136">Hizmet güncelleştirmesi (tüm bölgeler) + çözüm Güncelleştirmesi (haftalık 4 bölge)</span><span class="sxs-lookup"><span data-stu-id="caf26-136">Service update (all regions) + Solution update (Week 4 regions)</span></span> |
| <span data-ttu-id="caf26-137">6</span><span class="sxs-lookup"><span data-stu-id="caf26-137">6</span></span> | <span data-ttu-id="caf26-138">Hizmet güncelleştirmesi (tüm bölgeler) + çözüm Güncelleştirmesi (haftalık 5 bölge)</span><span class="sxs-lookup"><span data-stu-id="caf26-138">Service update (all regions) + Solution update (Week 5 regions)</span></span> |
| <span data-ttu-id="caf26-139">7</span><span class="sxs-lookup"><span data-stu-id="caf26-139">7</span></span> | <span data-ttu-id="caf26-140">Hizmet güncelleştirmesi (tüm bölgeler) + çözüm Güncelleştirmesi (haftalık 6 bölge)</span><span class="sxs-lookup"><span data-stu-id="caf26-140">Service update (all regions) + Solution update (Week 6 regions)</span></span> |
| <span data-ttu-id="caf26-141">8</span><span class="sxs-lookup"><span data-stu-id="caf26-141">8</span></span> | <span data-ttu-id="caf26-142">Hizmet güncelleştirmesi (tüm bölgeler)</span><span class="sxs-lookup"><span data-stu-id="caf26-142">Service update (all regions)</span></span> |

> [!NOTE]
> <span data-ttu-id="caf26-143">Çözüm güncelleştirmeleri, serbest bırakıldıktan sonra tüm veri merkezlerinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="caf26-143">Solution updates are available on all data centers once they're released.</span></span> <span data-ttu-id="caf26-144">Güncelleştirmelerin otomatik olarak çoğaltılmasını beklemek istemezseniz, bu güncelleştirmeleri herhangi bir veri merkezindeki herhangi bir ortama el ile uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="caf26-144">If you don't want to wait for the updates to replicate automatically, you can manually apply these updates on any environment in any data center.</span></span>

<span data-ttu-id="caf26-145">Gerektiğinde, İnsan Kaynakları aşağıdaki düzeltme türlerini de sağlar:</span><span class="sxs-lookup"><span data-stu-id="caf26-145">When needed, Human Resources also provides the following types of fixes:</span></span>

- <span data-ttu-id="caf26-146">**Düzeltme (düzeltme)**: haftada bir hizmet güncelleştirme sürümü ile veya bu sürümden ayrı olarak oluşabilecek hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="caf26-146">**Revision (hotfix)**: bug fixes that can occur either with or apart from a weekly service update release</span></span>

- <span data-ttu-id="caf26-147">**Acil durum düzeltmesi**: tek başına yapıdaki proaktif ve reaktif düzeltmeler, canlı site sorunlarını gidermek için yalnızca konfigürasyon veya kod değişikliklerini içerebilir ve haftalık bir Servis Güncelleştirmesi sürümünden ayrı olarak oluşabilir</span><span class="sxs-lookup"><span data-stu-id="caf26-147">**Emergency fix**: proactive and reactive hotfixes that are standalone in nature, can include configuration-only or code changes to resolve live site issues, and can occur apart from a weekly service update release</span></span>

<span data-ttu-id="caf26-148">Sürümler bir iç ortam üzerinde gözden geçirilip test edildiğini ve doğrulanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="caf26-148">Releases are reviewed, tested, and validated on an internal environment.</span></span> <span data-ttu-id="caf26-149">Yapılar imzalandıktan sonra üretime dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="caf26-149">After builds are signed off, they're then deployed to production.</span></span>

## <a name="exceptions-in-2019"></a><span data-ttu-id="caf26-150">2019'daki istisnalar</span><span class="sxs-lookup"><span data-stu-id="caf26-150">Exceptions in 2019</span></span>

<span data-ttu-id="caf26-151">Aşağıdaki tarihler, normal serbest bırakma zamanlamasının özel durumlardır:</span><span class="sxs-lookup"><span data-stu-id="caf26-151">The following dates are exceptions to the regular release schedule:</span></span>

| <span data-ttu-id="caf26-152">Tarih</span><span class="sxs-lookup"><span data-stu-id="caf26-152">Date</span></span> | <span data-ttu-id="caf26-153">Tanım</span><span class="sxs-lookup"><span data-stu-id="caf26-153">Description</span></span> |
| --- | --- |
| <span data-ttu-id="caf26-154">25 Kasım haftası</span><span class="sxs-lookup"><span data-stu-id="caf26-154">Week of November 25</span></span> | <span data-ttu-id="caf26-155">Güncelleştirme yok</span><span class="sxs-lookup"><span data-stu-id="caf26-155">No updates</span></span> |
| <span data-ttu-id="caf26-156">16 Aralık haftası</span><span class="sxs-lookup"><span data-stu-id="caf26-156">Week of December 16</span></span> | <span data-ttu-id="caf26-157">Yalnızca küçük güncelleştirmeleri</span><span class="sxs-lookup"><span data-stu-id="caf26-157">Minor updates only</span></span> |
| <span data-ttu-id="caf26-158">23 Aralık haftası</span><span class="sxs-lookup"><span data-stu-id="caf26-158">Week of December 23</span></span> | <span data-ttu-id="caf26-159">Güncelleştirme yok</span><span class="sxs-lookup"><span data-stu-id="caf26-159">No updates</span></span> |
| <span data-ttu-id="caf26-160">30 Aralık haftası</span><span class="sxs-lookup"><span data-stu-id="caf26-160">Week of December 30</span></span> | <span data-ttu-id="caf26-161">Güncelleştirme yok</span><span class="sxs-lookup"><span data-stu-id="caf26-161">No updates</span></span> |

## <a name="communications"></a><span data-ttu-id="caf26-162">İletişim</span><span class="sxs-lookup"><span data-stu-id="caf26-162">Communications</span></span>

<span data-ttu-id="caf26-163">İnsan Kaynaklarıyla ilgili neler olduğunu ve aşağıdaki konumlarda yayımladığımız neleri öğrenebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="caf26-163">You can find out what's in the works for Human Resources and what we've released in the following locations:</span></span>

- [<span data-ttu-id="caf26-164">Dynamics 365 Human Resources Yol haritası</span><span class="sxs-lookup"><span data-stu-id="caf26-164">Dynamics 365 Human Resources roadmap</span></span>](https://dynamics.microsoft.com/roadmap/talent/)

- [<span data-ttu-id="caf26-165">Dynamics 365 sürüm planları</span><span class="sxs-lookup"><span data-stu-id="caf26-165">Dynamics 365 Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans/)

- [<span data-ttu-id="caf26-166">Dynamics 365 Human Resources'teki yenilikler veya değişiklikler</span><span class="sxs-lookup"><span data-stu-id="caf26-166">What's new or changed in Dynamics 365 Human Resources</span></span>](hr-admin-whats-new.md)

- <span data-ttu-id="caf26-167">[Lifecycle Services'de (LCS) Sorun arama](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (yalnızca platform ile ilgili hatalar için)</span><span class="sxs-lookup"><span data-stu-id="caf26-167">[Issue search in Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (for Platform-related bugs only)</span></span>

- [<span data-ttu-id="caf26-168">İnsan kaynakları blogu</span><span class="sxs-lookup"><span data-stu-id="caf26-168">Human Resources blog</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [<span data-ttu-id="caf26-169">İnsan Kaynakları Yammer topluluğu</span><span class="sxs-lookup"><span data-stu-id="caf26-169">Human Resources Yammer community</span></span>](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a><span data-ttu-id="caf26-170">Korumalı alan ortamındaki Önizleme özellikleri</span><span class="sxs-lookup"><span data-stu-id="caf26-170">Preview features in a sandbox environment</span></span>

<span data-ttu-id="caf26-171">Bir korumalı alan ortamındaki Önizleme özelliklerini, üretim ortamınızda etkinleştirmeden önce doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="caf26-171">You can validate preview features in a sandbox environment before enabling them in your production environment.</span></span> <span data-ttu-id="caf26-172">Yeni özellikleri etkinleştirme hakkında daha fazla bilgi için [Özellik yönetimine genel bakış](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)'a bakın.</span><span class="sxs-lookup"><span data-stu-id="caf26-172">For more information about enabling features, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>

<span data-ttu-id="caf26-173">Tüm yeni özellikler en az 30 gün boyunca ve genellikle 30-60 gün önizlemede kalır.</span><span class="sxs-lookup"><span data-stu-id="caf26-173">All new features remain in preview for at least 30 days, and typically 30-60 days.</span></span> <span data-ttu-id="caf26-174">Önemli özellikler genellikle önizleme dönemini izleyen her yılın Ekim ve Nisan ayında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="caf26-174">Major features are generally available in October and April of each year following the preview period.</span></span> <span data-ttu-id="caf26-175">Özellik yönetimi çalışma alanında yeni yetenekleri gördüğünüz anda bunları açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="caf26-175">As soon as you see new capabilities in the Feature management workspace, you can turn them on.</span></span> <span data-ttu-id="caf26-176">Bazı özellikler varsayılan olarak açık olabilir.</span><span class="sxs-lookup"><span data-stu-id="caf26-176">Some features may be on by default.</span></span>

<span data-ttu-id="caf26-177">Bazen bir tümleştirme özelliği varsayılan olarak açıktır ve kapatılamaz (örneğin, Özellik yönetimi çalışma alanı).</span><span class="sxs-lookup"><span data-stu-id="caf26-177">At times, an integral feature will be on by default and can't be turned off (for example, the Feature management workspace).</span></span>

<span data-ttu-id="caf26-178">Bir özellik genel olarak kullanılabilir olduğunda üretim ortamlarında açılıp kapatılamayabilir.</span><span class="sxs-lookup"><span data-stu-id="caf26-178">Once a feature is generally available, it may be turned on or off in production environments.</span></span> <span data-ttu-id="caf26-179">Özellik yönetimi çalışma alanı bir önizleme özelliğinin zorunlu hale gelme zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="caf26-179">The Feature management workspace indicates when a preview feature will become mandatory.</span></span> <span data-ttu-id="caf26-180">Bu tarih genellikle yarıyıllık sürüm planlarına uygun olacak şekilde 1 Ekim veya 1 Nisandır.</span><span class="sxs-lookup"><span data-stu-id="caf26-180">This date is usually on October 1 or April 1 to align with the semiannual release plans.</span></span> <span data-ttu-id="caf26-181">Zorunlu özellikleri kapatamazsınız.</span><span class="sxs-lookup"><span data-stu-id="caf26-181">You can't turn off mandatory features.</span></span> <span data-ttu-id="caf26-182">Bir özelliği zorunlu olana kadar tüm ortamlarda kapatıp açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="caf26-182">Until it becomes mandatory, you can turn a feature on and off in all environments.</span></span>

<span data-ttu-id="caf26-183">Korumalı alan veya deneme ortamındaki özelliklerin önizlenmesini önemle öneririz.</span><span class="sxs-lookup"><span data-stu-id="caf26-183">We highly recommend previewing features in a sandbox or trial environment.</span></span> <span data-ttu-id="caf26-184">Verileriniz ile yeni özelliklerin eksiksiz deneyimini elde edebilmeniz için, geçerli üretim ortamınızın veya veritabanınızın bir kopyasını bir sandbox ortamına oluşturmak en iyisidir.</span><span class="sxs-lookup"><span data-stu-id="caf26-184">It's best to create a copy of your current production environment or database into a sandbox environment so you can get the complete experience of the new features with your data.</span></span>

<span data-ttu-id="caf26-185">Korumalı alan ortamının sağlanması hakkında daha fazla bilgi için, bkz. [İnsan Kaynakları projesi hazırlama](hr-admin-setup-provision.md).</span><span class="sxs-lookup"><span data-stu-id="caf26-185">For more information about provisioning a sandbox environment, see [Provision a Human Resources project](hr-admin-setup-provision.md).</span></span> <span data-ttu-id="caf26-186">Test ortamını kaldırmak için, bkz. [Örnek kaldırma](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span><span class="sxs-lookup"><span data-stu-id="caf26-186">To remove a test environment, see [Remove an instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span></span> 

## <a name="report-bugs"></a><span data-ttu-id="caf26-187">Hataları raporla</span><span class="sxs-lookup"><span data-stu-id="caf26-187">Report bugs</span></span>

<span data-ttu-id="caf26-188">Önizleme özellikleri test edilirken veya yeni yetenekler denerken, beklendiği gibi çalışmayan maddeler bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="caf26-188">While testing preview features or trying new capabilities, you might find items that don't work as expected.</span></span> <span data-ttu-id="caf26-189">Lütfen [Microsoft Dynamics 365 desteğiyle](https://dynamics.microsoft.com/support/) tüm hataları bildirin.</span><span class="sxs-lookup"><span data-stu-id="caf26-189">Please report any bugs through [Microsoft Dynamics 365 support](https://dynamics.microsoft.com/support/).</span></span>

## <a name="see-also"></a><span data-ttu-id="caf26-190">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="caf26-190">See also</span></span>

- [<span data-ttu-id="caf26-191">Dynamics 365 ve Power Platform sürüm planları</span><span class="sxs-lookup"><span data-stu-id="caf26-191">Dynamics 365 and Power Platform Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans)
- [<span data-ttu-id="caf26-192">Dynamics 365 Human Resources'taki yenilikler veya değişiklikler</span><span class="sxs-lookup"><span data-stu-id="caf26-192">What's new or changed in Dynamics 365 Human Resource</span></span>](hr-admin-whats-new.md)
- [<span data-ttu-id="caf26-193">Yazılım yaşam döngüsü ilkesi</span><span class="sxs-lookup"><span data-stu-id="caf26-193">Software lifecycle policy</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)

