--- 
title: "Nakledilen günlük girişlerini günlüğe aktarma"
description: "Bu yordamda, günlüğe kaydetme yoluyla günlük girişleri oluşturma gösterilir."
author: aprilolson
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 94849370d10ddfeedeee0d51e62afdd975ef69ac
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="89e11-103">Nakledilen günlük girişlerini günlüğe aktarma</span><span class="sxs-lookup"><span data-stu-id="89e11-103">Journalize posted journal entries</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="89e11-104">Bu yordamda, günlüğe kaydetme yoluyla günlük girişleri oluşturma gösterilir.</span><span class="sxs-lookup"><span data-stu-id="89e11-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="89e11-105">Bu yordam, USMF demo verisi şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="89e11-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="89e11-106">Günlüğe kaydetme işlemi için Genel muhasebe > Genel muhasebe ayarı > Genel muhasebe parametreleri altındaki ayarları doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="89e11-106">Validate the settings for journalizing under General ledger > Ledger setup > General ledger parameters.</span></span>
2. <span data-ttu-id="89e11-107">Genişletilmiş genel muhasebe günlüğü alanı Evet veya Hayır olarak ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="89e11-107">The Extended ledger journal field can be set to Yes or No.</span></span> <span data-ttu-id="89e11-108">Evet ise, rapor çıktısı farklı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="89e11-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="89e11-109">Günlüğe kaydetme işlemi çalıştırılmazsa dönemin kapatılıp kapatılmayacağını seçin.</span><span class="sxs-lookup"><span data-stu-id="89e11-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span>
    * <span data-ttu-id="89e11-110">Bu seçenek Evet olarak ayarlanırsa, günlüğe kaydetme işlemi söz konusu dönem için tamamlanana kadar dönem kapatılamaz.</span><span class="sxs-lookup"><span data-stu-id="89e11-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="89e11-111">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="89e11-111">Close the page.</span></span>
5. <span data-ttu-id="89e11-112">Genel muhasebe > Periyodik görevler > Günlüğe aktarma'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="89e11-112">Go to General ledger > Periodic tasks > Journalizing.</span></span>
6. <span data-ttu-id="89e11-113">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89e11-113">Click Filter.</span></span>
7. <span data-ttu-id="89e11-114">Tanımlamak istediğiniz filtre ölçütleriyle satırı vurgulayın.</span><span class="sxs-lookup"><span data-stu-id="89e11-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="89e11-115">Ölçütler alanında filtre ölçütlerini girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="89e11-115">In the Criteria field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="89e11-116">Filtre sayfasını kapatmak için Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89e11-116">Click OK to close the filter page.</span></span>
10. <span data-ttu-id="89e11-117">Günlüğe kaydetme işlemini başlatmak için Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89e11-117">Click OK to start the journalizing process.</span></span>
    * <span data-ttu-id="89e11-118">İşlem tamamlandıktan sonra bir rapor oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="89e11-118">A report will be generated after the process is complete.</span></span>  


