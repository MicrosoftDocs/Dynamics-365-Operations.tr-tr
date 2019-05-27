---
title: Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (23 Ocak 2019)
description: Bu konuda, Microsoft Dynamics 365 for Talent Core HR'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 01/23/2019
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
ms.search.validFrom: 2019-01-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f27698c257301f52e5c77eaa8a04ca13a0315825
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1519279"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-january-23-2019"></a><span data-ttu-id="faab3-103">Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (23 Ocak 2019)</span><span class="sxs-lookup"><span data-stu-id="faab3-103">What's new or changed in Dynamics 365 for Talent Core HR (January 23, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="faab3-104">**Derleme 8.1.2121**</span><span class="sxs-lookup"><span data-stu-id="faab3-104">**Build 8.1.2121**</span></span>

<span data-ttu-id="faab3-105">Bu konuda, Core HR'deki yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="faab3-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="faab3-106">Değişiklikler</span><span class="sxs-lookup"><span data-stu-id="faab3-106">Changes</span></span>

### <a name="import-of-employee-fixed-compensation-not-working-when-creating-new-fixed-compensation-records"></a><span data-ttu-id="faab3-107">Çalışan sabit ücret içe aktarması yeni sabit ücret kayıtları oluşturulurken çalışmıyor</span><span class="sxs-lookup"><span data-stu-id="faab3-107">Import of employee fixed compensation not working when creating new fixed compensation records</span></span>
<span data-ttu-id="faab3-108">İçe aktarmadan sonra ücret düzeyini almak için çalışan sabit ücret varlığında bir değişiklik yapıldı.</span><span class="sxs-lookup"><span data-stu-id="faab3-108">A change has been made to the employee fixed compensation entity to retrieve the compensation level upon import.</span></span> <span data-ttu-id="faab3-109">Bu sürümden önce, bir ileti, gerekli düzeyi belirtmek için görüntüleniyordu.</span><span class="sxs-lookup"><span data-stu-id="faab3-109">Prior to this release, a message was displayed indicating that the level was required.</span></span>

### <a name="remove-the-minimum-balance-field-from-the-time-off-request-dialog-box"></a><span data-ttu-id="faab3-110">Minimum bakiye alanını izin süresi talep iletişim kutusundan kaldırın</span><span class="sxs-lookup"><span data-stu-id="faab3-110">Remove the minimum balance field from the time off request dialog box</span></span>
<span data-ttu-id="faab3-111">**Minimum bakiye** alanı, **İzin talebi** iletişim kutusundan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="faab3-111">The **Minimum balance** field has been removed from the **Time off request** dialog box.</span></span> <span data-ttu-id="faab3-112">Bu değişiklik, çalışılmayan nerede istenmesi tüm alanları etkiler.</span><span class="sxs-lookup"><span data-stu-id="faab3-112">This change affects all areas where time off can be requested.</span></span>

### <a name="data-upgrade-for-compensation-levels-not-updating-in-all-scenarios"></a><span data-ttu-id="faab3-113">Maaş düzeylerini güncelleştirmemeyi tüm senaryolar için verileri yükselt</span><span class="sxs-lookup"><span data-stu-id="faab3-113">Data upgrade for compensation levels not updating in all scenarios</span></span>
<span data-ttu-id="faab3-114">Sabit maaş planları üzerinde maaş düzeyi güncelleştirmek için bir değişiklik yapıldı.</span><span class="sxs-lookup"><span data-stu-id="faab3-114">A change has been made to update the compensation level on fixed compensation plans.</span></span> <span data-ttu-id="faab3-115">Bu değişiklik maaş sabit plan çalışana atanmış iş düzeyinde doldurulur.</span><span class="sxs-lookup"><span data-stu-id="faab3-115">This change will populate the compensation level on fixed plans for the job assigned to the employee.</span></span>

### <a name="payroll-information-in-the-manage-changes-page-is-only-available-when-logged-in-as-system-administrator"></a><span data-ttu-id="faab3-116">Bordro bilgileri Değişiklikleri yönet sayfasında, yalnızca Sistem Yöneticisi olarak oturum açıldığında kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="faab3-116">Payroll information in the Manage changes page is only available when logged in as System Administrator</span></span>
<span data-ttu-id="faab3-117">Bu değişiklik, Bordro Yöneticisi rolüne sahip çalışanların **Değişiklikler zaman çizelgesi > Değişiklikleri yönet** sayfasında konum için bordro bilgisine erişmelerine olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="faab3-117">This change allows employees with the Payroll Administrator role access to the payroll information on the **Changes timeline > Manage changes** page for the position.</span></span>

### <a name="job-fields-default-to-positions"></a><span data-ttu-id="faab3-118">Konumlara varsayılan iş alanları</span><span class="sxs-lookup"><span data-stu-id="faab3-118">Job fields default to positions</span></span>
<span data-ttu-id="faab3-119">Konumdaki işi değiştirirken, iş alanları konuma varsayılır.</span><span class="sxs-lookup"><span data-stu-id="faab3-119">When changing the job on a position, job fields will default to the position.</span></span> <span data-ttu-id="faab3-120">Bir uyarı iletisi, geçerli değerleri kabul etme seçeneği verir veya bu alanlar için geçerli değerleri tutma seçeneği verir.</span><span class="sxs-lookup"><span data-stu-id="faab3-120">An alert message will appear giving an option to accept the default values or keep the existing values for those fields.</span></span>

### <a name="probation-period-and-calendar-are-not-displayed-for-future-hired-employees"></a><span data-ttu-id="faab3-121">Deneme süresi ve takvim, gelecekte işe alınan çalışanlar için görüntülenmez.</span><span class="sxs-lookup"><span data-stu-id="faab3-121">Probation period and calendar are not displayed for future hired employees.</span></span>
<span data-ttu-id="faab3-122">Bu değişiklikle **Deneme süresi** ve **Takvim** alanları, **Değişiklikleri yönet** sayfasına gelecekteki ve geçmişteki çalışanlara veri girişine izin vermek için eklenir.</span><span class="sxs-lookup"><span data-stu-id="faab3-122">With this change, **Probation period** and **Calendar** fields have been added to the **Manage changes** page to allow for data entry for future and past employees.</span></span>

### <a name="platform-update-23"></a><span data-ttu-id="faab3-123">Platform güncelleştirmesi 23</span><span class="sxs-lookup"><span data-stu-id="faab3-123">Platform update 23</span></span>
<span data-ttu-id="faab3-124">Küçük hata gidermeleri Platform güncelleştirmesi 23'ün parçası olarak dahil edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="faab3-124">Minor bug fixes have been included as part of Platform update 23.</span></span> <span data-ttu-id="faab3-125">Daha fazla bilgi için bkz [Dynamics 365 for Finance and Operations platform güncelleştirmesi 23'te neler yeni veya değişti (Ocak 2019) 23](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span><span class="sxs-lookup"><span data-stu-id="faab3-125">For more information, see [What's new or changed in Dynamics 365 for Finance and Operations platform update 23 (January 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span></span> 
