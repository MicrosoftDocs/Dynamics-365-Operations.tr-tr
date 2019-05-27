---
title: Dynamics 365 for Talent'daki yenilikler veya değişiklikler (31 Ocak 2019)
description: Bu konuda, Microsoft Dynamics 365 for Talent'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 01/31/2019
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
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d4504cebb7702c7163c94badeeb06d9af0e5467e
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1519272"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-january-31-2019"></a><span data-ttu-id="a572a-103">Dynamics 365 for Talent'daki yenilikler veya değişiklikler (31 Ocak 2019)</span><span class="sxs-lookup"><span data-stu-id="a572a-103">What's new or changed in Dynamics 365 for Talent (January 31, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a572a-104">Bu konuda, Dynamics 365 for Talent'daki yeni veya değişen özellikler açıklanmaktadır</span><span class="sxs-lookup"><span data-stu-id="a572a-104">This topic describes features that are either new or changed in Dynamics 365 for Talent</span></span>

<span data-ttu-id="a572a-105">**Derleme 8.1.2128**</span><span class="sxs-lookup"><span data-stu-id="a572a-105">**Build 8.1.2128**</span></span>

## <a name="core-hr-changes"></a><span data-ttu-id="a572a-106">Core HR Değişiklikleri</span><span class="sxs-lookup"><span data-stu-id="a572a-106">Core HR Changes</span></span>

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a><span data-ttu-id="a572a-107">Alına izin kişi kartı, izin planı tarihlerini dikkate almaz.</span><span class="sxs-lookup"><span data-stu-id="a572a-107">Time off taken on leave people card doesn't consider leave plan dates</span></span>
<span data-ttu-id="a572a-108">Takvim yılında yürütülmeyen izin planlarına sahip olanlar için **Alınan** kartı artık plan tanımlı izin yılında alınan izinleri görüntüler.</span><span class="sxs-lookup"><span data-stu-id="a572a-108">For those that have leave plans that don’t run on a calendar year, the **Taken** card now displays time off that’s been taken in the plan-defined leave year.</span></span> <span data-ttu-id="a572a-109">Örneğin, bir kuruluşun izin yılı 1 Haziran ile 30 Mayıs arasındaysa ve bir çalışan Aralıkta 3 gün izin aldıysa, 15 Ocaktaki **Alındı** kartı 3 gün görüntüleyecektir.</span><span class="sxs-lookup"><span data-stu-id="a572a-109">For example, if an organization’s leave year is June 1 through May 30 and an employee has taken 3 days off in December, the **Taken** card on January 15, will display 3 days.</span></span> 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a><span data-ttu-id="a572a-110">Tahakkuk tutarları katman tarihi esasıyla eşleşmiyor</span><span class="sxs-lookup"><span data-stu-id="a572a-110">Accrual amounts not matching tier date basis</span></span>
<span data-ttu-id="a572a-111">Müşterilerin, çalışanların hizmet aylarının etkin olduğunu belirlemeleri için İzin ve devamsızlık (**İnsan kaynakları** parametreleri) eklemek için yeni seçenekler eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="a572a-111">New options have been added to leave and absence (**Human resources** parameters) to enable customers to determine when employees’ months of service date are effective.</span></span> <span data-ttu-id="a572a-112">Bazı kuruluşlar için tarih ay sonundadır, ancak diğerleri için diğer ayın başında olabilir.</span><span class="sxs-lookup"><span data-stu-id="a572a-112">For some organizations, the date is the end of the month, but for others it may be the start of the next month.</span></span> <span data-ttu-id="a572a-113">Örneğin, bir kuruluş 31 Aralıkta izin verebilirken bir başkası 1 Ocakta verebilir.</span><span class="sxs-lookup"><span data-stu-id="a572a-113">For example, one organization may award time off on December 31, while another may award time off on January 1.</span></span> <span data-ttu-id="a572a-114">Bu seçenek, ödüllendirmenin ne zaman gerçekleşeceğini seçmenize izin verir.</span><span class="sxs-lookup"><span data-stu-id="a572a-114">This option will allow you to choose when the award should occur.</span></span> 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a><span data-ttu-id="a572a-115">Çalışan işe alma işlemleri "İş akışı tamamlandı" durumunda takıldı</span><span class="sxs-lookup"><span data-stu-id="a572a-115">Worker hire actions are stuck in "Workflow complete" state</span></span>
<span data-ttu-id="a572a-116">Az sayıda iş akışının "İş akışı tamamlandı" durumu ile sonlandırılmış olduğu bir hatayı düzeltmek için değişiklikler yapıldı.</span><span class="sxs-lookup"><span data-stu-id="a572a-116">Changes have been made to correct an issue where a small number of workflows finished with a "Workflow complete" status.</span></span> <span data-ttu-id="a572a-117">Yeni iş akışları şimdi bir iş akışı tamamlandığında "Tamamlandı" durumuna geçecektir.</span><span class="sxs-lookup"><span data-stu-id="a572a-117">New workflows should now move to a "Completed" state when the workflow finishes.</span></span> <span data-ttu-id="a572a-118">Bir iş akışı tamamlandı durumu içindeki tüm iş akışları, gerektiği taktirde güncelleştirme veya kaldırılması için bir hata durumuna geçirilecektir.</span><span class="sxs-lookup"><span data-stu-id="a572a-118">Any workflows in a workflow completed status will be transitioned to an error status to allow for updating or removal if required.</span></span> 
