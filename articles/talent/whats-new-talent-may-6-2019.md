---
title: Dynamics 365 for Talent'daki yenilikler veya değişiklikler (6 Mayız 2019)
description: Bu konuda, Microsoft Dynamics 365 for Talent'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 05/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c541bac532e878c8493a60d95c05c9104d4b96e1
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741556"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-may-6-2019"></a><span data-ttu-id="047c8-103">Dynamics 365 for Talent'daki yenilikler veya değişiklikler (6 Mayız 2019)</span><span class="sxs-lookup"><span data-stu-id="047c8-103">What's new or changed in Dynamics 365 for Talent (May 6, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="047c8-104">Bu konuda, Dynamics 365 for Talent'daki yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="047c8-104">This topic describes features that are either new or changed in Dynamics 365 for Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="047c8-105">Attract'te değişiklikler</span><span class="sxs-lookup"><span data-stu-id="047c8-105">Changes in Attract</span></span>

### <a name="select-optional-documents-upon-offer-creation"></a><span data-ttu-id="047c8-106">Teklif oluşturma üzerine isteğe bağlı belgeleri seçme</span><span class="sxs-lookup"><span data-stu-id="047c8-106">Select optional documents upon offer creation</span></span>

<span data-ttu-id="047c8-107">Bir teklif paketi şablonu seçtiğinizde, Attract artık o paket şablonundan uygun, isteğe bağlı belgeleri seçmenizi ister.</span><span class="sxs-lookup"><span data-stu-id="047c8-107">When you select an offer package template, Attract now prompts you to select the applicable, optional documents from that package template.</span></span> <span data-ttu-id="047c8-108">Teklifi hazırlarken başka isteğe bağlı belgeleri de ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="047c8-108">You can add other optional documents while preparing the offer.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="047c8-109">Onboard'daki değişiklikler</span><span class="sxs-lookup"><span data-stu-id="047c8-109">Changes in Onboard</span></span>

<span data-ttu-id="047c8-110">Bu sürüm, Dynamics 365 Talent: Onboard için küçük hata düzeltmeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="047c8-110">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="047c8-111">Core HR içindeki değişiklikler</span><span class="sxs-lookup"><span data-stu-id="047c8-111">Changes in Core HR</span></span>

<span data-ttu-id="047c8-112">Bu bölümde açıklanan değişiklikler sürüm numarası 8.1.2282 için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="047c8-112">Changes described in this section apply to build number 8.1.2282.</span></span> <span data-ttu-id="047c8-113">Bazı başlıklardaki parantez içindeki numaralar Microsoft Dynamics Lifecycle Services (LCS) destek numaralarına referans verir.</span><span class="sxs-lookup"><span data-stu-id="047c8-113">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="platform-update-26"></a><span data-ttu-id="047c8-114">Platform güncelleştirmesi 26</span><span class="sxs-lookup"><span data-stu-id="047c8-114">Platform update 26</span></span>

<span data-ttu-id="047c8-115">Platform güncelleştirmesi 26 hakkında diğer ayrıntılar için bkz. [Dynamics 365 for Finance and Operations platform güncelleştirmesi 26 (Mayıs 2019) içindeki önizleme özellikleri](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-26).</span><span class="sxs-lookup"><span data-stu-id="047c8-115">For additional details about Platform update 26, see [Preview features in Dynamics 365 for Finance and Operations platform update 26 (May 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-26).</span></span> 

### <a name="common-data-service-entity-support-for-custom-fields"></a><span data-ttu-id="047c8-116">Özel alanlar için Common Data Service varlığı desteği</span><span class="sxs-lookup"><span data-stu-id="047c8-116">Common Data Service entity support for custom fields</span></span>

<span data-ttu-id="047c8-117">Bu haftaki sürümde şu varlık artık özel alanları destekliyor: Kazanç hesaplama sıklığı, Kazanç hesaplama oranı, Kazanç türü, İş takvimi, İş takvimi tatili, Ödeme döngüsü ve Çalışan tanımlama tipleri.</span><span class="sxs-lookup"><span data-stu-id="047c8-117">In this week's release, the following entities now support custom fields: Benefit calc frequency, Benefit calc rate, Benefit type, Work calendar, Work calendar holiday, Pay cycle, and Worker identification types.</span></span>

### <a name="leave-mass-enrollment-changing-the-tier-basis-to-seniority-date-doesnt-refresh-the-initial-accrual-rate-318526"></a><span data-ttu-id="047c8-118">İzin toplu kaydı, katman temeli "Kıdem tarihi" olarak değiştirildiğinde başlangıçtaki tahakkuk oranını yenilemiyor (318526)</span><span class="sxs-lookup"><span data-stu-id="047c8-118">Leave mass enrollment, changing the tier basis to "Seniority date" doesn't refresh the initial accrual rate (318526)</span></span>

<span data-ttu-id="047c8-119">Çalışanları toplu kaydedip katman temelini değiştirdiğinizde, başlangıç tahakkuku artık seçmiş olduğunuz katman temelini yansıtıyor.</span><span class="sxs-lookup"><span data-stu-id="047c8-119">When you mass enroll employees and change the tier basis, the initial accrual now reflects the tier basis that you selected.</span></span>

### <a name="workflow-showing-duplicate-place-holders-313636"></a><span data-ttu-id="047c8-120">Yinelenen yer tutucuları gösteren iş akışı (313636)</span><span class="sxs-lookup"><span data-stu-id="047c8-120">Workflow showing duplicate place holders (313636)</span></span>

<span data-ttu-id="047c8-121">Bu sürümdeki değişiklikler iş akışı bildirimleri gönderildiğinde yer tutucuların yinelenmesini ortadan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="047c8-121">Changes in this release eliminate duplication of placeholders when workflow notifications are sent.</span></span>

### <a name="dimension-fields-arent-updated-when-using-open-in-excel-176261"></a><span data-ttu-id="047c8-122">"Excel 'de aç" kullanılırken boyut alanları güncelleştirilmiyor (176261)</span><span class="sxs-lookup"><span data-stu-id="047c8-122">Dimension fields aren't updated when using "Open in Excel" (176261)</span></span>

<span data-ttu-id="047c8-123">Bu sürümle birlikte artık mali boyutları **Çalışan** sayfasından **Excel'de Aç**'ı kullanarak güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="047c8-123">With this release, you can now update financial dimension using **Open in Excel** from the **Worker** page.</span></span> 

### <a name="worker-address-created-in-common-data-service-isnt-synced-to-talent-317555"></a><span data-ttu-id="047c8-124">Common Data Service'te oluşturulan çalışan adresi Talent ile eşitlenmiyor (317555)</span><span class="sxs-lookup"><span data-stu-id="047c8-124">Worker address created in Common Data Service isn't synced to Talent (317555)</span></span>

<span data-ttu-id="047c8-125">Bu değişiklikle birlikte Common Data Service'te oluşturulan adresler Talent Core HR'de güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="047c8-125">With this change, addresses created in Common Data Service are updated in Talent Core HR.</span></span>


## <a name="in-preview"></a><span data-ttu-id="047c8-126">Ön izlemede</span><span class="sxs-lookup"><span data-stu-id="047c8-126">In preview</span></span>

### <a name="new-page-to-validate-position-hierarchy-data"></a><span data-ttu-id="047c8-127">Konum hiyerarşisi verilerini doğrulamak için yeni sayfa</span><span class="sxs-lookup"><span data-stu-id="047c8-127">New page to validate position hierarchy data</span></span>

<span data-ttu-id="047c8-128">İnsan kaynakları (İK) ve yöneticiler artık yanlışlıkla içe aktarılmış olabilecek herhangi bir döngüsel referans için yönetim hiyerarşisini doğrulayabilir.</span><span class="sxs-lookup"><span data-stu-id="047c8-128">Human resources (HR) and administrators can now validate the managerial hierarchy for any circular references that might have inadvertently been imported.</span></span> <span data-ttu-id="047c8-129">Bu yeni sayfaya **Kuruluş yönetimi > Bağlantılar > Pozisyonlar > Pozisyon hiyerarşisi doğrulaması** üzerinden erişebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="047c8-129">You can access this new page from **Organizational administration > Links > Positions > Position hierarchy validation**.</span></span>

### <a name="specify-reason-codes-on-leave-types"></a><span data-ttu-id="047c8-130">İzin türlerinde neden kodları belirtme</span><span class="sxs-lookup"><span data-stu-id="047c8-130">Specify reason codes on leave types</span></span>

<span data-ttu-id="047c8-131">Kuruluşlar izin istekleri hakkında ek bilgiler gerektirebilir.</span><span class="sxs-lookup"><span data-stu-id="047c8-131">Organizations might require additional information about time-off requests.</span></span> <span data-ttu-id="047c8-132">Belirli bir izin türü ile ilişkili sebep kodlarını artık belirtebilir ve çalışanların izin taleplerinde bir sebep kodu seçmelerine olanak sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="047c8-132">You can now specify reason codes for leave types and let employees select a reason code on their time-off requests.</span></span>

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a><span data-ttu-id="047c8-133">İzin talepleri üzerindeki belirli izin türleri için sebep kodları gerektir</span><span class="sxs-lookup"><span data-stu-id="047c8-133">Require reason codes for specific leave types on time-off requests</span></span>

<span data-ttu-id="047c8-134">Kuruluşlar, bir çalışan izin talepleri gönderdiğinde belirli izin türleri için sebep kodlarının ayarlanmasını gerektirebilir.</span><span class="sxs-lookup"><span data-stu-id="047c8-134">Organizations might require reason codes for specific leave types when employees submit time-off requests.</span></span> <span data-ttu-id="047c8-135">Şirket ilkesi veya mevzuat gereksinimleri nedeniyle bu gereksinim bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="047c8-135">This requirement might exist because of company policy or regulatory requirements.</span></span> <span data-ttu-id="047c8-136">Artık hangi izin türlerini bir sebep koduna ihtiyaç duyduğunu belirtebilir ve personelin, izin taleplerinde bu izin türleri için sebep kodu sağlamalarını gerektirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="047c8-136">You can now specify which leave types require a reason code, and you can require that employees provide a reason code for the leave type on their time-off requests.</span></span>

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a><span data-ttu-id="047c8-137">İK için izin ve devamsızlık hareket listesi sağlama</span><span class="sxs-lookup"><span data-stu-id="047c8-137">Provide a leave and absence transaction list for HR</span></span>

<span data-ttu-id="047c8-138">Çalışan iznini takip etme ve iznin nasıl hesaplandığını anlama özelliği, yalnızca İK'nın çalışan sorularına yanıt vermesine yardımcı olmaz, aynı zamanda çalışanlar için doğru izin ödülleri verilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="047c8-138">The ability to track employee time off and understand how time off is calculated not only helps HR answer employee questions, but also helps ensure accurate time-off awards for employees.</span></span> <span data-ttu-id="047c8-139">İK artık hareketlere (izinler, tahakkuklar, ayarlamalar ve talepler) erişimine sahiptir ve böylece İK personeli bakiyeler arkasındaki nedenleri görebilir.</span><span class="sxs-lookup"><span data-stu-id="047c8-139">HR now has a new view into the transactions (grants, accruals, adjustments, and requests), so that HR staff can view the reasons behind balances.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="047c8-140">Çok yakında</span><span class="sxs-lookup"><span data-stu-id="047c8-140">Coming soon</span></span>

### <a name="indicate-instance-type-when-provisioning-talent"></a><span data-ttu-id="047c8-141">Talent'ta sağlarken örnek türünü gösterme</span><span class="sxs-lookup"><span data-stu-id="047c8-141">Indicate instance type when provisioning Talent</span></span>

<span data-ttu-id="047c8-142">Talent'ın yeni bir örneğini sağlarken yeni özelliklerin erken sınanmasına izin vererek örnek türünün **Üretim** veya **Korumalı alan** olduğunu belirtebileceksiniz.</span><span class="sxs-lookup"><span data-stu-id="047c8-142">When provisioning a new instance of Talent, you will be able to indicate whether the instance type is **Production** or **Sandbox**, allowing for early testing of new features.</span></span> <span data-ttu-id="047c8-143">Varolan tüm Talent örnekleri Üretim örneği türüne güncelleştirilecek.</span><span class="sxs-lookup"><span data-stu-id="047c8-143">All existing Talent instances will be updated to the Production instance type.</span></span> <span data-ttu-id="047c8-144">Varolan örneklerden birinin Korumalı alan örneği türüne güncelleştirilmesini istiyorsanız, lütfen değişiklik isteğini başlatmak için Desteğe başvurun.</span><span class="sxs-lookup"><span data-stu-id="047c8-144">If you want one of your existing instances to be updated to the Sandbox instance type, please contact Support to initiate the change request.</span></span>
