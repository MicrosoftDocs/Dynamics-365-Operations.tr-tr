---
title: Nakledilen günlük girişlerini günlüğe aktarma
description: Bu yordamda, günlüğe kaydetme yoluyla günlük girişleri oluşturma gösterilir.
author: aprilolson
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5028db1db2359a54d565fc299c9a3353a4cf8297
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826166"
---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="96b51-103">Nakledilen günlük girişlerini günlüğe aktarma</span><span class="sxs-lookup"><span data-stu-id="96b51-103">Journalize posted journal entries</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="96b51-104">Bu yordamda, günlüğe kaydetme yoluyla günlük girişleri oluşturma gösterilir.</span><span class="sxs-lookup"><span data-stu-id="96b51-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="96b51-105">Bu yordam, USMF demo verisi şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="96b51-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="96b51-106">**Gezinti bölmesinde** **Modüller > Genel muhasebe > Genel muhasebe ayarı > Genel muhasebe parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="96b51-106">In the **Navigation pane**, go to **Modules > General ledger > Ledger setup > General ledger parameters**.</span></span>
2. <span data-ttu-id="96b51-107">**Genişletilmiş genel muhasebe günlüğü** alanı Evet veya Hayır olarak ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="96b51-107">The **Extended ledger journal** field can be set to Yes or No.</span></span> <span data-ttu-id="96b51-108">Evet ise, rapor çıktısı farklı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="96b51-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="96b51-109">Günlüğe kaydetme işlemi çalıştırılmazsa dönemin kapatılıp kapatılmayacağını seçin.</span><span class="sxs-lookup"><span data-stu-id="96b51-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span> <span data-ttu-id="96b51-110">Bu seçenek Evet olarak ayarlanırsa, günlüğe kaydetme işlemi söz konusu dönem için tamamlanana kadar dönem kapatılamaz.</span><span class="sxs-lookup"><span data-stu-id="96b51-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="96b51-111">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="96b51-111">Close the page.</span></span>
5. <span data-ttu-id="96b51-112">**Gezinti bölmesinde** **Modüller > Genel muhasebe > Periyodik görevler > Günlüğe kaydetme**'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="96b51-112">In the **Navigation pane**, go to **Modules > General ledger > Periodic tasks > Journalizing**.</span></span>
6. <span data-ttu-id="96b51-113">**Filtrele** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96b51-113">Click **Filter**.</span></span>
7. <span data-ttu-id="96b51-114">Tanımlamak istediğiniz filtre ölçütleriyle satırı vurgulayın.</span><span class="sxs-lookup"><span data-stu-id="96b51-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="96b51-115">**Ölçütler** alanında filtre ölçütlerini girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="96b51-115">In the **Criteria** field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="96b51-116">Filtre sayfasını kapatmak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96b51-116">Click **OK** to close the filter page.</span></span>
10. <span data-ttu-id="96b51-117">Günlüğe kaydetme işlemini başlatmak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96b51-117">Click **OK** to start the journalizing process.</span></span> <span data-ttu-id="96b51-118">İşlem tamamlandıktan sonra bir rapor oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="96b51-118">A report will be generated after the process is complete.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]