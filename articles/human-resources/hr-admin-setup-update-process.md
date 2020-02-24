---
title: Güncelleştirme işlemi
description: ''
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
ms.openlocfilehash: 1817e072805bafbf0d5a9eb2698ef75abc75ad68
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/07/2020
ms.locfileid: "3031102"
---
# <a name="update-process"></a><span data-ttu-id="ac74b-102">Güncelleştirme işlemi</span><span class="sxs-lookup"><span data-stu-id="ac74b-102">Update process</span></span>

<span data-ttu-id="ac74b-103">Microsoft Dynamics 365 Human Resources, sürekli, temassız servis güncelleştirmeleri sağlayan gerçek bir hizmet olarak yazılımdır (SaaS).</span><span class="sxs-lookup"><span data-stu-id="ac74b-103">Microsoft Dynamics 365 Human Resources is a true software as a service (SaaS) that provides continuous, touchless service updates.</span></span> <span data-ttu-id="ac74b-104">Bu güncelleştirmeler, yasal güncelleştirmeler de dahil olmak üzere hizmette kritik geliştirmeler sağlayan uygulama ve platform değişikliklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="ac74b-104">These updates contain both application and platform changes that often provide critical improvements to the service, including regulatory updates.</span></span>

## <a name="update-policy"></a><span data-ttu-id="ac74b-105">Güncelleştirme ilkesi</span><span class="sxs-lookup"><span data-stu-id="ac74b-105">Update policy</span></span>

<span data-ttu-id="ac74b-106">Güncelleştirmeler düzenli aralıklarla yayımlanır ve tüm ortamlar için yapılır.</span><span class="sxs-lookup"><span data-stu-id="ac74b-106">Updates are released on a regular cadence to all environments.</span></span> <span data-ttu-id="ac74b-107">İnsan Kaynakları, ürün destek kullanılabilirliği hakkında düzenli ve öngörülebilir kılavuzlar sunan [Microsoft Lifecycle ilkesi](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy) ile uygun olarak desteklenir.</span><span class="sxs-lookup"><span data-stu-id="ac74b-107">Human Resources is supported according to the [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), which provides consistent and predictable guidelines for the availability of support.</span></span>

## <a name="release-cadence"></a><span data-ttu-id="ac74b-108">Sürüm temposu</span><span class="sxs-lookup"><span data-stu-id="ac74b-108">Release cadence</span></span>

<span data-ttu-id="ac74b-109">İnsan Kaynakları güncelleştirmeler otomatik olarak tüm ortamlara uygulanır.</span><span class="sxs-lookup"><span data-stu-id="ac74b-109">Human Resources updates are applied to all environments automatically.</span></span> <span data-ttu-id="ac74b-110">İnsan Kaynakları iki tür sürüm sağlar:</span><span class="sxs-lookup"><span data-stu-id="ac74b-110">Human Resources provides two types of releases:</span></span>

- <span data-ttu-id="ac74b-111">**Hizmet güncelleştirmeleri**: Hata düzeltmeleri ve yeni özellikler içeren Haftalık Güncelleştirmeler.</span><span class="sxs-lookup"><span data-stu-id="ac74b-111">**Service updates**: Weekly updates that include bug fixes and new features.</span></span> <span data-ttu-id="ac74b-112">Hizmet güncelleştirmeleri, serbest bıraktıklarında uygun platform güncelleştirmelerini de içerir.</span><span class="sxs-lookup"><span data-stu-id="ac74b-112">Service updates also include applicable Platform updates when they release.</span></span> <span data-ttu-id="ac74b-113">Platform güncelleştirmelerinin ne zaman yayınlanacaklarını öğrenmek için [Tablo 3: Platform yayımları](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases)'na bakın.</span><span class="sxs-lookup"><span data-stu-id="ac74b-113">To get an idea of when Platform updates are released, see [Table 3: Platform releases](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span></span> <span data-ttu-id="ac74b-114">Haftalık Güncelleştirmeler genellikle çarşamba günleri yayınlanır.</span><span class="sxs-lookup"><span data-stu-id="ac74b-114">Weekly updates usually release on Wednesdays.</span></span> <span data-ttu-id="ac74b-115">Haftalık güncellemeler hakkında daha fazla bilgi için bkz. [Dynamics 365 Human Resources'ta yenilikler veya değişiklikler](https://docs.microsoft.com/dynamics365/talent/whats-new).</span><span class="sxs-lookup"><span data-stu-id="ac74b-115">For more information about weekly updates, see [What's new or changed in Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365/talent/whats-new).</span></span>

    <span data-ttu-id="ac74b-116">Aksi belirtilmedikçe, tüm desteklenen veri merkezleri haftalık olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ac74b-116">All supported data centers update weekly, unless otherwise noted.</span></span> <span data-ttu-id="ac74b-117">Haftalık Güncelleştirmeler tipik olarak Çarşamba günü başlar ve Pazar ile tamamlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="ac74b-117">Weekly updates typically begin on Wednesday and complete by Sunday.</span></span> <span data-ttu-id="ac74b-118">ABD, Avustralya, Avrupa, Birleşik Krallık, Asya ve Kanada bölgeleri haftalık güncelleştirmelere dahil edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="ac74b-118">US, Australia, Europe, UK, Asia, and Canada regions are included in weekly updates.</span></span> 

- <span data-ttu-id="ac74b-119">**Common Data Service çözüm güncelleştirmeleri**: Bu güncelleştirmeler gerektiğinde yaklaşık altı haftada bir gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="ac74b-119">**Common Data Service solution updates**: These updates occur approximately every six weeks, as needed.</span></span> <span data-ttu-id="ac74b-120">Bunlar yeni varlıkları ve Common Data Service'deki varolan varlıklara yapılan değişiklikleri içerir.</span><span class="sxs-lookup"><span data-stu-id="ac74b-120">They include new entities and changes to existing entities in Common Data Service.</span></span> <span data-ttu-id="ac74b-121">Bu güncelleştirmeler haftalık güncelleştirmelerle aynı bölgeler için serbest çalışırlar ve tüm veri merkezleri arasında yineleme yapmak için altı hafta sürer.</span><span class="sxs-lookup"><span data-stu-id="ac74b-121">These updates release to the same regions as the weekly updates, and they take about six weeks to replicate through all data centers.</span></span> <span data-ttu-id="ac74b-122">Çözüm güncelleştirmeleri haftalık hizmet güncelleştirmelerine göre hizalanmayabilir veya bunları hizalamayabilir.</span><span class="sxs-lookup"><span data-stu-id="ac74b-122">Solution updates may or may not align with weekly service updates.</span></span>

<span data-ttu-id="ac74b-123">Aşağıdaki tabloda örnek bir zamanlama gösterilmektedir:</span><span class="sxs-lookup"><span data-stu-id="ac74b-123">The following table shows a sample schedule:</span></span>

| <span data-ttu-id="ac74b-124">Hafta</span><span class="sxs-lookup"><span data-stu-id="ac74b-124">Week</span></span> | <span data-ttu-id="ac74b-125">Güncelleştirme türü</span><span class="sxs-lookup"><span data-stu-id="ac74b-125">Update type</span></span> |
| --- | --- |
| <span data-ttu-id="ac74b-126">1</span><span class="sxs-lookup"><span data-stu-id="ac74b-126">1</span></span> | <span data-ttu-id="ac74b-127">Hizmet güncelleştirmesi (tüm bölgeler)</span><span class="sxs-lookup"><span data-stu-id="ac74b-127">Service update (all regions)</span></span> |
| <span data-ttu-id="ac74b-128">2</span><span class="sxs-lookup"><span data-stu-id="ac74b-128">2</span></span> | <span data-ttu-id="ac74b-129">Hizmet güncelleştirmesi (tüm bölgeler) + çözüm Güncelleştirmesi (haftalık 1 bölge)</span><span class="sxs-lookup"><span data-stu-id="ac74b-129">Service update (all regions) + Solution update (Week 1 regions)</span></span> |
| <span data-ttu-id="ac74b-130">3</span><span class="sxs-lookup"><span data-stu-id="ac74b-130">3</span></span> | <span data-ttu-id="ac74b-131">Hizmet güncelleştirmesi (tüm bölgeler) + çözüm Güncelleştirmesi (haftalık 2 bölge)</span><span class="sxs-lookup"><span data-stu-id="ac74b-131">Service update (all regions) + Solution update (Week 2 regions)</span></span> |
| <span data-ttu-id="ac74b-132">4</span><span class="sxs-lookup"><span data-stu-id="ac74b-132">4</span></span> | <span data-ttu-id="ac74b-133">Hizmet güncelleştirmesi (tüm bölgeler) + çözüm Güncelleştirmesi (haftalık 3 bölge)</span><span class="sxs-lookup"><span data-stu-id="ac74b-133">Service update (all regions) + Solution update (Week 3 regions)</span></span> |
| <span data-ttu-id="ac74b-134">5</span><span class="sxs-lookup"><span data-stu-id="ac74b-134">5</span></span> | <span data-ttu-id="ac74b-135">Hizmet güncelleştirmesi (tüm bölgeler) + çözüm Güncelleştirmesi (haftalık 4 bölge)</span><span class="sxs-lookup"><span data-stu-id="ac74b-135">Service update (all regions) + Solution update (Week 4 regions)</span></span> |
| <span data-ttu-id="ac74b-136">6</span><span class="sxs-lookup"><span data-stu-id="ac74b-136">6</span></span> | <span data-ttu-id="ac74b-137">Hizmet güncelleştirmesi (tüm bölgeler) + çözüm Güncelleştirmesi (haftalık 5 bölge)</span><span class="sxs-lookup"><span data-stu-id="ac74b-137">Service update (all regions) + Solution update (Week 5 regions)</span></span> |
| <span data-ttu-id="ac74b-138">7</span><span class="sxs-lookup"><span data-stu-id="ac74b-138">7</span></span> | <span data-ttu-id="ac74b-139">Hizmet güncelleştirmesi (tüm bölgeler) + çözüm Güncelleştirmesi (haftalık 6 bölge)</span><span class="sxs-lookup"><span data-stu-id="ac74b-139">Service update (all regions) + Solution update (Week 6 regions)</span></span> |
| <span data-ttu-id="ac74b-140">8</span><span class="sxs-lookup"><span data-stu-id="ac74b-140">8</span></span> | <span data-ttu-id="ac74b-141">Hizmet güncelleştirmesi (tüm bölgeler)</span><span class="sxs-lookup"><span data-stu-id="ac74b-141">Service update (all regions)</span></span> |

> [!NOTE]
> <span data-ttu-id="ac74b-142">Çözüm güncelleştirmeleri, serbest bırakıldıktan sonra tüm veri merkezlerinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ac74b-142">Solution updates are available on all data centers once they're released.</span></span> <span data-ttu-id="ac74b-143">Güncelleştirmelerin otomatik olarak çoğaltılmasını beklemek istemezseniz, bu güncelleştirmeleri herhangi bir veri merkezindeki herhangi bir ortama el ile uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac74b-143">If you don't want to wait for the updates to replicate automatically, you can manually apply these updates on any environment in any data center.</span></span>

<span data-ttu-id="ac74b-144">Gerektiğinde, İnsan Kaynakları aşağıdaki düzeltme türlerini de sağlar:</span><span class="sxs-lookup"><span data-stu-id="ac74b-144">When needed, Human Resources also provides the following types of fixes:</span></span>

- <span data-ttu-id="ac74b-145">**Düzeltme (düzeltme)**: haftada bir hizmet güncelleştirme sürümü ile veya bu sürümden ayrı olarak oluşabilecek hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="ac74b-145">**Revision (hotfix)**: bug fixes that can occur either with or apart from a weekly service update release</span></span>

- <span data-ttu-id="ac74b-146">**Acil durum düzeltmesi**: tek başına yapıdaki proaktif ve reaktif düzeltmeler, canlı site sorunlarını gidermek için yalnızca konfigürasyon veya kod değişikliklerini içerebilir ve haftalık bir Servis Güncelleştirmesi sürümünden ayrı olarak oluşabilir</span><span class="sxs-lookup"><span data-stu-id="ac74b-146">**Emergency fix**: proactive and reactive hotfixes that are standalone in nature, can include configuration-only or code changes to resolve live site issues, and can occur apart from a weekly service update release</span></span>

<span data-ttu-id="ac74b-147">Sürümler bir iç ortam üzerinde gözden geçirilip test edildiğini ve doğrulanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ac74b-147">Releases are reviewed, tested, and validated on an internal environment.</span></span> <span data-ttu-id="ac74b-148">Yapılar imzalandıktan sonra üretime dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="ac74b-148">After builds are signed off, they're then deployed to production.</span></span>

## <a name="exceptions-in-2019"></a><span data-ttu-id="ac74b-149">2019'daki istisnalar</span><span class="sxs-lookup"><span data-stu-id="ac74b-149">Exceptions in 2019</span></span>

<span data-ttu-id="ac74b-150">Aşağıdaki tarihler, normal serbest bırakma zamanlamasının özel durumlardır:</span><span class="sxs-lookup"><span data-stu-id="ac74b-150">The following dates are exceptions to the regular release schedule:</span></span>

| <span data-ttu-id="ac74b-151">Tarih</span><span class="sxs-lookup"><span data-stu-id="ac74b-151">Date</span></span> | <span data-ttu-id="ac74b-152">Tanım</span><span class="sxs-lookup"><span data-stu-id="ac74b-152">Description</span></span> |
| --- | --- |
| <span data-ttu-id="ac74b-153">25 Kasım haftası</span><span class="sxs-lookup"><span data-stu-id="ac74b-153">Week of November 25</span></span> | <span data-ttu-id="ac74b-154">Güncelleştirme yok</span><span class="sxs-lookup"><span data-stu-id="ac74b-154">No updates</span></span> |
| <span data-ttu-id="ac74b-155">16 Aralık haftası</span><span class="sxs-lookup"><span data-stu-id="ac74b-155">Week of December 16</span></span> | <span data-ttu-id="ac74b-156">Yalnızca küçük güncelleştirmeleri</span><span class="sxs-lookup"><span data-stu-id="ac74b-156">Minor updates only</span></span> |
| <span data-ttu-id="ac74b-157">23 Aralık haftası</span><span class="sxs-lookup"><span data-stu-id="ac74b-157">Week of December 23</span></span> | <span data-ttu-id="ac74b-158">Güncelleştirme yok</span><span class="sxs-lookup"><span data-stu-id="ac74b-158">No updates</span></span> |
| <span data-ttu-id="ac74b-159">30 Aralık haftası</span><span class="sxs-lookup"><span data-stu-id="ac74b-159">Week of December 30</span></span> | <span data-ttu-id="ac74b-160">Güncelleştirme yok</span><span class="sxs-lookup"><span data-stu-id="ac74b-160">No updates</span></span> |

## <a name="communications"></a><span data-ttu-id="ac74b-161">İletişim</span><span class="sxs-lookup"><span data-stu-id="ac74b-161">Communications</span></span>

<span data-ttu-id="ac74b-162">İnsan Kaynaklarıyla ilgili neler olduğunu ve aşağıdaki konumlarda yayımladığımız neleri öğrenebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="ac74b-162">You can find out what's in the works for Human Resources and what we've released in the following locations:</span></span>

- [<span data-ttu-id="ac74b-163">Dynamics 365 Human Resources Yol haritası</span><span class="sxs-lookup"><span data-stu-id="ac74b-163">Dynamics 365 Human Resources roadmap</span></span>](https://dynamics.microsoft.com/roadmap/talent/)

- [<span data-ttu-id="ac74b-164">Dynamics 365 sürüm planları</span><span class="sxs-lookup"><span data-stu-id="ac74b-164">Dynamics 365 Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans/)

- [<span data-ttu-id="ac74b-165">Dynamics 365 Human Resources'teki yenilikler veya değişiklikler</span><span class="sxs-lookup"><span data-stu-id="ac74b-165">What's new or changed in Dynamics 365 Human Resources</span></span>](hr-admin-whats-new.md)

- <span data-ttu-id="ac74b-166">[Lifecycle Services'de (LCS) Sorun arama](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (yalnızca platform ile ilgili hatalar için)</span><span class="sxs-lookup"><span data-stu-id="ac74b-166">[Issue search in Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (for Platform-related bugs only)</span></span>

- [<span data-ttu-id="ac74b-167">İnsan kaynakları blogu</span><span class="sxs-lookup"><span data-stu-id="ac74b-167">Human Resources blog</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [<span data-ttu-id="ac74b-168">İnsan Kaynakları Yammer topluluğu</span><span class="sxs-lookup"><span data-stu-id="ac74b-168">Human Resources Yammer community</span></span>](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a><span data-ttu-id="ac74b-169">Korumalı alan ortamındaki Önizleme özellikleri</span><span class="sxs-lookup"><span data-stu-id="ac74b-169">Preview features in a sandbox environment</span></span>

<span data-ttu-id="ac74b-170">Bir korumalı alan ortamındaki Önizleme özelliklerini, üretim ortamınızda etkinleştirmeden önce doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac74b-170">You can validate preview features in a sandbox environment before enabling them in your production environment.</span></span> <span data-ttu-id="ac74b-171">Yeni özellikleri etkinleştirme hakkında daha fazla bilgi için [Özellik yönetimine genel bakış](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)'a bakın.</span><span class="sxs-lookup"><span data-stu-id="ac74b-171">For more information about enabling features, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>

<span data-ttu-id="ac74b-172">Tüm yeni özellikler en az 30 gün boyunca ve genellikle 30-60 gün önizlemede kalır.</span><span class="sxs-lookup"><span data-stu-id="ac74b-172">All new features remain in preview for at least 30 days, and typically 30-60 days.</span></span> <span data-ttu-id="ac74b-173">Önemli özellikler genellikle önizleme dönemini izleyen her yılın Ekim ve Nisan ayında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ac74b-173">Major features are generally available in October and April of each year following the preview period.</span></span> <span data-ttu-id="ac74b-174">Özellik yönetimi çalışma alanında yeni yetenekleri gördüğünüz anda bunları açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac74b-174">As soon as you see new capabilities in the Feature management workspace, you can turn them on.</span></span> <span data-ttu-id="ac74b-175">Bazı özellikler varsayılan olarak açık olabilir.</span><span class="sxs-lookup"><span data-stu-id="ac74b-175">Some features may be on by default.</span></span>

<span data-ttu-id="ac74b-176">Bazen bir tümleştirme özelliği varsayılan olarak açıktır ve kapatılamaz (örneğin, Özellik yönetimi çalışma alanı).</span><span class="sxs-lookup"><span data-stu-id="ac74b-176">At times, an integral feature will be on by default and can't be turned off (for example, the Feature management workspace).</span></span>

<span data-ttu-id="ac74b-177">Bir özellik genel olarak kullanılabilir olduğunda üretim ortamlarında açılıp kapatılamayabilir.</span><span class="sxs-lookup"><span data-stu-id="ac74b-177">Once a feature is generally available, it may be turned on or off in production environments.</span></span> <span data-ttu-id="ac74b-178">Özellik yönetimi çalışma alanı bir önizleme özelliğinin zorunlu hale gelme zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac74b-178">The Feature management workspace indicates when a preview feature will become mandatory.</span></span> <span data-ttu-id="ac74b-179">Bu tarih genellikle yarıyıllık sürüm planlarına uygun olacak şekilde 1 Ekim veya 1 Nisandır.</span><span class="sxs-lookup"><span data-stu-id="ac74b-179">This date is usually on October 1 or April 1 to align with the semiannual release plans.</span></span> <span data-ttu-id="ac74b-180">Zorunlu özellikleri kapatamazsınız.</span><span class="sxs-lookup"><span data-stu-id="ac74b-180">You can't turn off mandatory features.</span></span> <span data-ttu-id="ac74b-181">Bir özelliği zorunlu olana kadar tüm ortamlarda kapatıp açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac74b-181">Until it becomes mandatory, you can turn a feature on and off in all environments.</span></span>

<span data-ttu-id="ac74b-182">Korumalı alan veya deneme ortamındaki özelliklerin önizlenmesini önemle öneririz.</span><span class="sxs-lookup"><span data-stu-id="ac74b-182">We highly recommend previewing features in a sandbox or trial environment.</span></span> <span data-ttu-id="ac74b-183">Verileriniz ile yeni özelliklerin eksiksiz deneyimini elde edebilmeniz için, geçerli üretim ortamınızın veya veritabanınızın bir kopyasını bir sandbox ortamına oluşturmak en iyisidir.</span><span class="sxs-lookup"><span data-stu-id="ac74b-183">It's best to create a copy of your current production environment or database into a sandbox environment so you can get the complete experience of the new features with your data.</span></span>

<span data-ttu-id="ac74b-184">Korumalı alan ortamının sağlanması hakkında daha fazla bilgi için, bkz. [İnsan Kaynakları projesi hazırlama](hr-admin-setup-provision.md).</span><span class="sxs-lookup"><span data-stu-id="ac74b-184">For more information about provisioning a sandbox environment, see [Provision a Human Resources project](hr-admin-setup-provision.md).</span></span> <span data-ttu-id="ac74b-185">Test ortamını kaldırmak için, bkz. [Örnek kaldırma](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span><span class="sxs-lookup"><span data-stu-id="ac74b-185">To remove a test environment, see [Remove an instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span></span> 

## <a name="report-bugs"></a><span data-ttu-id="ac74b-186">Hataları raporla</span><span class="sxs-lookup"><span data-stu-id="ac74b-186">Report bugs</span></span>

<span data-ttu-id="ac74b-187">Önizleme özellikleri test edilirken veya yeni yetenekler denerken, beklendiği gibi çalışmayan maddeler bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="ac74b-187">While testing preview features or trying new capabilities, you might find items that don't work as expected.</span></span> <span data-ttu-id="ac74b-188">Lütfen [Microsoft Dynamics 365 desteğiyle](https://dynamics.microsoft.com/support/) tüm hataları bildirin.</span><span class="sxs-lookup"><span data-stu-id="ac74b-188">Please report any bugs through [Microsoft Dynamics 365 support](https://dynamics.microsoft.com/support/).</span></span>

## <a name="see-also"></a><span data-ttu-id="ac74b-189">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="ac74b-189">See also</span></span>

- [<span data-ttu-id="ac74b-190">Dynamics 365 ve Power Platform sürüm planları</span><span class="sxs-lookup"><span data-stu-id="ac74b-190">Dynamics 365 and Power Platform Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans)
- [<span data-ttu-id="ac74b-191">Dynamics 365 Human Resources'taki yenilikler veya değişiklikler</span><span class="sxs-lookup"><span data-stu-id="ac74b-191">What's new or changed in Dynamics 365 Human Resource</span></span>](hr-admin-whats-new.md)
- [<span data-ttu-id="ac74b-192">Yazılım yaşam döngüsü ilkesi</span><span class="sxs-lookup"><span data-stu-id="ac74b-192">Software lifecycle policy</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)

