---
title: Güncelleştirme işlemi
description: Microsoft Dynamics 365 Human Resources uygulama ve platform değişiklikleri için sürekli, temassız servis güncelleştirmeleri sağlayan gerçek bir hizmet olarak yazılımdır (SaaS).
author: andreabichsel
manager: AnnBe
ms.date: 02/27/2020
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
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 424027e82717b8636d59289b28978d6ce3c6db4d
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154517"
---
# <a name="update-process"></a><span data-ttu-id="d5638-103">Güncelleştirme işlemi</span><span class="sxs-lookup"><span data-stu-id="d5638-103">Update process</span></span>

<span data-ttu-id="d5638-104">Microsoft Dynamics 365 Human Resources, sürekli, temassız servis güncelleştirmeleri sağlayan gerçek bir hizmet olarak yazılımdır (SaaS).</span><span class="sxs-lookup"><span data-stu-id="d5638-104">Microsoft Dynamics 365 Human Resources is a true software as a service (SaaS) that provides continuous, touchless service updates.</span></span> <span data-ttu-id="d5638-105">Bu güncelleştirmeler, yasal güncelleştirmeler de dahil olmak üzere hizmette kritik geliştirmeler sağlayan uygulama ve platform değişikliklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="d5638-105">These updates contain both application and platform changes that often provide critical improvements to the service, including regulatory updates.</span></span>

## <a name="update-policy"></a><span data-ttu-id="d5638-106">Güncelleştirme ilkesi</span><span class="sxs-lookup"><span data-stu-id="d5638-106">Update policy</span></span>

<span data-ttu-id="d5638-107">Güncelleştirmeler düzenli aralıklarla yayımlanır ve tüm ortamlar için yapılır.</span><span class="sxs-lookup"><span data-stu-id="d5638-107">Updates are released on a regular cadence to all environments.</span></span> <span data-ttu-id="d5638-108">İnsan Kaynakları, ürün destek kullanılabilirliği hakkında düzenli ve öngörülebilir kılavuzlar sunan [Microsoft Lifecycle ilkesi](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy) ile uygun olarak desteklenir.</span><span class="sxs-lookup"><span data-stu-id="d5638-108">Human Resources is supported according to the [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), which provides consistent and predictable guidelines for the availability of support.</span></span>

## <a name="release-cadence"></a><span data-ttu-id="d5638-109">Sürüm temposu</span><span class="sxs-lookup"><span data-stu-id="d5638-109">Release cadence</span></span>

<span data-ttu-id="d5638-110">İnsan Kaynakları güncelleştirmeler otomatik olarak tüm ortamlara uygulanır.</span><span class="sxs-lookup"><span data-stu-id="d5638-110">Human Resources updates are applied to all environments automatically.</span></span> <span data-ttu-id="d5638-111">İnsan Kaynakları iki tür sürüm sağlar:</span><span class="sxs-lookup"><span data-stu-id="d5638-111">Human Resources provides two types of releases:</span></span>

- <span data-ttu-id="d5638-112">**Hizmet güncelleştirmeleri**: Güncellemeler, hata düzeltmeleri ve yeni özellikler içererek iki haftada bir yapılır.</span><span class="sxs-lookup"><span data-stu-id="d5638-112">**Service updates**: Updates occur every two weeks that include bug fixes and new features.</span></span> <span data-ttu-id="d5638-113">Hizmet güncelleştirmeleri, serbest bıraktıklarında uygun platform güncelleştirmelerini de içerir.</span><span class="sxs-lookup"><span data-stu-id="d5638-113">Service updates also include applicable Platform updates when they release.</span></span> <span data-ttu-id="d5638-114">Platform güncelleştirmelerinin ne zaman yayınlanacaklarını öğrenmek için [Tablo 3: Platform yayımları](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases)'na bakın.</span><span class="sxs-lookup"><span data-stu-id="d5638-114">To get an idea of when Platform updates are released, see [Table 3: Platform releases](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span></span> <span data-ttu-id="d5638-115">İki Haftalık Güncelleştirmeler, bölgeler arasında aşamalı genel bir piyasaya sahiptir.</span><span class="sxs-lookup"><span data-stu-id="d5638-115">Biweekly updates have a staged global rollout across regions.</span></span> <span data-ttu-id="d5638-116">İki Haftalık güncellemeler hakkında daha fazla bilgi için bkz. [Dynamics 365 Human Resources'ta yenilikler veya değişiklikler](hr-admin-whats-new.md).</span><span class="sxs-lookup"><span data-stu-id="d5638-116">For more information about biweekly updates, see [What's new or changed in Dynamics 365 Human Resources](hr-admin-whats-new.md).</span></span>

    <span data-ttu-id="d5638-117">Aksi belirtilmedikçe, tüm desteklenen veri merkezleri iki haftalık olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="d5638-117">All supported data centers update every two weeks, unless otherwise noted.</span></span> <span data-ttu-id="d5638-118">ABD, Avustralya, Avrupa, Birleşik Krallık, Asya ve Kanada bölgeleri iki haftalık güncelleştirmelere dahil edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="d5638-118">US, Australia, Europe, UK, Asia, and Canada regions are included in biweekly updates.</span></span> 

- <span data-ttu-id="d5638-119">**Common Data Service çözüm güncelleştirmeleri**: Bu güncelleştirmeler gerektiğinde yaklaşık altı haftada bir gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="d5638-119">**Common Data Service solution updates**: These updates occur approximately every six weeks, as needed.</span></span> <span data-ttu-id="d5638-120">Bunlar yeni varlıkları ve Common Data Service'deki varolan varlıklara yapılan değişiklikleri içerir.</span><span class="sxs-lookup"><span data-stu-id="d5638-120">They include new entities and changes to existing entities in Common Data Service.</span></span> <span data-ttu-id="d5638-121">Bu güncelleştirmeler iki haftalık güncelleştirmelerle aynı bölgeler için serbest çalışırlar ve tüm veri merkezleri arasında yineleme yapmak için altı hafta sürer.</span><span class="sxs-lookup"><span data-stu-id="d5638-121">These updates release to the same regions as the biweekly updates, and they take about six weeks to replicate through all data centers.</span></span> <span data-ttu-id="d5638-122">Çözüm güncelleştirmeleri iki haftalık hizmet güncelleştirmelerine göre hizalanmayabilir veya bunları hizalamayabilir.</span><span class="sxs-lookup"><span data-stu-id="d5638-122">Solution updates may or may not align with biweekly service updates.</span></span>

> [!NOTE]
> <span data-ttu-id="d5638-123">Çözüm güncelleştirmeleri, serbest bırakıldıktan sonra tüm veri merkezlerinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d5638-123">Solution updates are available on all data centers once they're released.</span></span> <span data-ttu-id="d5638-124">Güncelleştirmelerin otomatik olarak çoğaltılmasını beklemek istemezseniz, bu güncelleştirmeleri herhangi bir veri merkezindeki herhangi bir ortama el ile uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d5638-124">If you don't want to wait for the updates to replicate automatically, you can manually apply these updates on any environment in any data center.</span></span>

<span data-ttu-id="d5638-125">Gerektiğinde, İnsan Kaynakları aşağıdaki düzeltme türlerini de sağlar:</span><span class="sxs-lookup"><span data-stu-id="d5638-125">When needed, Human Resources also provides the following types of fixes:</span></span>

- <span data-ttu-id="d5638-126">**Düzeltme (düzeltme)**: İki haftada bir hizmet güncelleştirme sürümü ile veya bu sürümden ayrı olarak oluşabilecek hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="d5638-126">**Revision (hotfix)**: Bug fixes that can occur either with or apart from a biweekly service update release</span></span>

- <span data-ttu-id="d5638-127">**Acil durum düzeltmesi**: tek başına yapıdaki proaktif ve reaktif düzeltmeler, canlı site sorunlarını gidermek için yalnızca konfigürasyon veya kod değişikliklerini içerebilir ve iki haftalık bir Servis Güncelleştirmesi sürümünden ayrı olarak oluşabilir</span><span class="sxs-lookup"><span data-stu-id="d5638-127">**Emergency fix**: Proactive and reactive hotfixes that are standalone in nature, can include configuration-only or code changes to resolve live site issues, and can occur apart from a biweekly service update release</span></span>

<span data-ttu-id="d5638-128">Sürümler bir iç ortam üzerinde gözden geçirilip test edildiğini ve doğrulanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d5638-128">Releases are reviewed, tested, and validated on an internal environment.</span></span> <span data-ttu-id="d5638-129">Yapılar imzalandıktan sonra üretime dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="d5638-129">After builds are signed off, they're then deployed to production.</span></span>

## <a name="release-cadence-exceptions-in-2020"></a><span data-ttu-id="d5638-130">2020 içinde sürüm temposu özel durumları</span><span class="sxs-lookup"><span data-stu-id="d5638-130">Release cadence exceptions in 2020</span></span>

<span data-ttu-id="d5638-131">Aşağıdaki tarihler, normal serbest bırakma zamanlamasının özel durumlardır:</span><span class="sxs-lookup"><span data-stu-id="d5638-131">The following dates are exceptions to the regular release schedule:</span></span>

| <span data-ttu-id="d5638-132">Date</span><span class="sxs-lookup"><span data-stu-id="d5638-132">Date</span></span> | <span data-ttu-id="d5638-133">Tanım</span><span class="sxs-lookup"><span data-stu-id="d5638-133">Description</span></span> |
| --- | --- |
| <span data-ttu-id="d5638-134">23 Kasım haftası</span><span class="sxs-lookup"><span data-stu-id="d5638-134">Week of November 23</span></span> | <span data-ttu-id="d5638-135">Güncelleştirme yok</span><span class="sxs-lookup"><span data-stu-id="d5638-135">No updates</span></span> |
| <span data-ttu-id="d5638-136">14 Aralık haftası</span><span class="sxs-lookup"><span data-stu-id="d5638-136">Week of December 14</span></span> | <span data-ttu-id="d5638-137">Yalnızca küçük güncelleştirmeleri</span><span class="sxs-lookup"><span data-stu-id="d5638-137">Minor updates only</span></span> |
| <span data-ttu-id="d5638-138">21 Aralık haftası</span><span class="sxs-lookup"><span data-stu-id="d5638-138">Week of December 21</span></span> | <span data-ttu-id="d5638-139">Güncelleştirme yok</span><span class="sxs-lookup"><span data-stu-id="d5638-139">No updates</span></span> |
| <span data-ttu-id="d5638-140">28 Aralık haftası</span><span class="sxs-lookup"><span data-stu-id="d5638-140">Week of December 28</span></span> | <span data-ttu-id="d5638-141">Güncelleştirme yok</span><span class="sxs-lookup"><span data-stu-id="d5638-141">No updates</span></span> |

## <a name="communications"></a><span data-ttu-id="d5638-142">İletişim</span><span class="sxs-lookup"><span data-stu-id="d5638-142">Communications</span></span>

<span data-ttu-id="d5638-143">İnsan Kaynaklarıyla ilgili neler olduğunu ve aşağıdaki konumlarda yayımladığımız neleri öğrenebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="d5638-143">You can find out what's in the works for Human Resources and what we've released in the following locations:</span></span>

- [<span data-ttu-id="d5638-144">Dynamics 365 Human Resources Yol haritası</span><span class="sxs-lookup"><span data-stu-id="d5638-144">Dynamics 365 Human Resources roadmap</span></span>](https://dynamics.microsoft.com/roadmap/human-resources/)

- [<span data-ttu-id="d5638-145">Dynamics 365 sürüm planları</span><span class="sxs-lookup"><span data-stu-id="d5638-145">Dynamics 365 Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans/)

- [<span data-ttu-id="d5638-146">Dynamics 365 Human Resources'teki yenilikler veya değişiklikler</span><span class="sxs-lookup"><span data-stu-id="d5638-146">What's new or changed in Dynamics 365 Human Resources</span></span>](hr-admin-whats-new.md)

- <span data-ttu-id="d5638-147">[Lifecycle Services'de (LCS) Sorun arama](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (yalnızca platform ile ilgili hatalar için)</span><span class="sxs-lookup"><span data-stu-id="d5638-147">[Issue search in Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (for Platform-related bugs only)</span></span>

- [<span data-ttu-id="d5638-148">İnsan kaynakları blogu</span><span class="sxs-lookup"><span data-stu-id="d5638-148">Human Resources blog</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [<span data-ttu-id="d5638-149">İnsan Kaynakları Yammer topluluğu</span><span class="sxs-lookup"><span data-stu-id="d5638-149">Human Resources Yammer community</span></span>](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a><span data-ttu-id="d5638-150">Korumalı alan ortamındaki Önizleme özellikleri</span><span class="sxs-lookup"><span data-stu-id="d5638-150">Preview features in a sandbox environment</span></span>

<span data-ttu-id="d5638-151">Bir korumalı alan ortamındaki Önizleme özelliklerini, üretim ortamınızda etkinleştirmeden önce doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d5638-151">You can validate preview features in a sandbox environment before enabling them in your production environment.</span></span> <span data-ttu-id="d5638-152">Yeni özellikleri etkinleştirme hakkında daha fazla bilgi için [Özellik yönetimine genel bakış](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)'a bakın.</span><span class="sxs-lookup"><span data-stu-id="d5638-152">For more information about enabling features, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>

<span data-ttu-id="d5638-153">Tüm yeni özellikler en az 30 gün boyunca ve genellikle 30-60 gün önizlemede kalır.</span><span class="sxs-lookup"><span data-stu-id="d5638-153">All new features remain in preview for at least 30 days, and typically 30-60 days.</span></span> <span data-ttu-id="d5638-154">Önemli özellikler genellikle önizleme dönemini izleyen her yılın Ekim ve Nisan ayında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d5638-154">Major features are generally available in October and April of each year following the preview period.</span></span> <span data-ttu-id="d5638-155">Özellik yönetimi çalışma alanında yeni yetenekleri gördüğünüz anda bunları açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d5638-155">As soon as you see new capabilities in the Feature management workspace, you can turn them on.</span></span> <span data-ttu-id="d5638-156">Bazı özellikler varsayılan olarak açık olabilir.</span><span class="sxs-lookup"><span data-stu-id="d5638-156">Some features may be on by default.</span></span>

<span data-ttu-id="d5638-157">Bazen bir tümleştirme özelliği varsayılan olarak açıktır ve kapatılamaz (örneğin, Özellik yönetimi çalışma alanı).</span><span class="sxs-lookup"><span data-stu-id="d5638-157">At times, an integral feature will be on by default and can't be turned off (for example, the Feature management workspace).</span></span>

<span data-ttu-id="d5638-158">Bir özellik genel olarak kullanılabilir olduğunda üretim ortamlarında açılıp kapatılamayabilir.</span><span class="sxs-lookup"><span data-stu-id="d5638-158">Once a feature is generally available, it may be turned on or off in production environments.</span></span> <span data-ttu-id="d5638-159">Özellik yönetimi çalışma alanı bir önizleme özelliğinin zorunlu hale gelme zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5638-159">The Feature management workspace indicates when a preview feature will become mandatory.</span></span> <span data-ttu-id="d5638-160">Bu tarih genellikle yarıyıllık sürüm planlarına uygun olacak şekilde 1 Ekim veya 1 Nisandır.</span><span class="sxs-lookup"><span data-stu-id="d5638-160">This date is usually on October 1 or April 1 to align with the semiannual release plans.</span></span> <span data-ttu-id="d5638-161">Zorunlu özellikleri kapatamazsınız.</span><span class="sxs-lookup"><span data-stu-id="d5638-161">You can't turn off mandatory features.</span></span> <span data-ttu-id="d5638-162">Bir özelliği zorunlu olana kadar tüm ortamlarda kapatıp açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d5638-162">Until it becomes mandatory, you can turn a feature on and off in all environments.</span></span>

<span data-ttu-id="d5638-163">Korumalı alan veya deneme ortamındaki özelliklerin önizlenmesini önemle öneririz.</span><span class="sxs-lookup"><span data-stu-id="d5638-163">We highly recommend previewing features in a sandbox or trial environment.</span></span> <span data-ttu-id="d5638-164">Verileriniz ile yeni özelliklerin eksiksiz deneyimini elde edebilmeniz için, geçerli üretim ortamınızın veya veritabanınızın bir kopyasını bir sandbox ortamına oluşturmak en iyisidir.</span><span class="sxs-lookup"><span data-stu-id="d5638-164">It's best to create a copy of your current production environment or database into a sandbox environment so you can get the complete experience of the new features with your data.</span></span>

<span data-ttu-id="d5638-165">Korumalı alan ortamının sağlanması hakkında daha fazla bilgi için, bkz. [İnsan Kaynakları projesi hazırlama](hr-admin-setup-provision.md).</span><span class="sxs-lookup"><span data-stu-id="d5638-165">For more information about provisioning a sandbox environment, see [Provision a Human Resources project](hr-admin-setup-provision.md).</span></span> <span data-ttu-id="d5638-166">Test ortamını kaldırmak için, bkz. [Örnek kaldırma](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span><span class="sxs-lookup"><span data-stu-id="d5638-166">To remove a test environment, see [Remove an instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span></span> 

## <a name="report-bugs"></a><span data-ttu-id="d5638-167">Hataları raporla</span><span class="sxs-lookup"><span data-stu-id="d5638-167">Report bugs</span></span>

<span data-ttu-id="d5638-168">Önizleme özellikleri test edilirken veya yeni yetenekler denerken, beklendiği gibi çalışmayan maddeler bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="d5638-168">While testing preview features or trying new capabilities, you might find items that don't work as expected.</span></span> <span data-ttu-id="d5638-169">Lütfen [Microsoft Dynamics 365 desteğiyle](https://dynamics.microsoft.com/support/) tüm hataları bildirin.</span><span class="sxs-lookup"><span data-stu-id="d5638-169">Please report any bugs through [Microsoft Dynamics 365 support](https://dynamics.microsoft.com/support/).</span></span>

## <a name="see-also"></a><span data-ttu-id="d5638-170">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="d5638-170">See also</span></span>

[<span data-ttu-id="d5638-171">Dynamics 365 ve Power Platform sürüm planları</span><span class="sxs-lookup"><span data-stu-id="d5638-171">Dynamics 365 and Power Platform Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans)</br>
[<span data-ttu-id="d5638-172">Dynamics 365 Human Resources'taki yenilikler veya değişiklikler</span><span class="sxs-lookup"><span data-stu-id="d5638-172">What's new or changed in Dynamics 365 Human Resource</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="d5638-173">Yazılım yaşam döngüsü ilkesi</span><span class="sxs-lookup"><span data-stu-id="d5638-173">Software lifecycle policy</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)

