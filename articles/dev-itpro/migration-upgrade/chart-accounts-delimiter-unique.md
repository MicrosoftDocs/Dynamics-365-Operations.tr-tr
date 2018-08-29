---
title: "Hesap planı ayırıcısını benzersiz yapma"
description: "Dynamics 365 for Finance and Operations'da hesap planı ve boyut değerleri için aynı sınırlayıcıya sahip olamazsınız. Yükseltmeden sonra sınırlayıcı değerlerini değiştirmeniz gerekir."
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: e197a1b44e038a97b8bf6db692dcc2eef2bc5f7b
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---

# <a name="make-the-chart-of-accounts-delimiter-unique"></a><span data-ttu-id="e9ac6-104">Hesap planı ayırıcısını benzersiz yapma</span><span class="sxs-lookup"><span data-stu-id="e9ac6-104">Make the chart of accounts delimiter unique</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e9ac6-105">Microsoft Dynamics AX 2012'de, hesap planı ve boyut değerleri için aynı sınırlayıcı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e9ac6-105">In Microsoft Dynamics AX 2012, you could use the same delimiter for your chart of accounts and dimension values.</span></span> <span data-ttu-id="e9ac6-106">Dynamics 365 for Finance and Operations'da hesap planı ve boyut değerleri için aynı sınırlayıcıya sahip olamazsınız.</span><span class="sxs-lookup"><span data-stu-id="e9ac6-106">In Dynamics 365 for Finance and Operations, you cannot have the same delimiter for the chart of accounts and dimension values.</span></span> <span data-ttu-id="e9ac6-107">Yinelenen bir sınırlayıcı varsa, yükseltme işleminden sonra değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e9ac6-107">If there is a duplicate delimiter, you can change it after upgrade.</span></span> 

<span data-ttu-id="e9ac6-108">Bu özellik aşağıdakilerde kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="e9ac6-108">This feature is available in:</span></span>
- <span data-ttu-id="e9ac6-109">Dynamics 365 for Finance and Operations sürüm 8.0</span><span class="sxs-lookup"><span data-stu-id="e9ac6-109">Dynamics 365 for Finance and Operations version 8.0</span></span>
- <span data-ttu-id="e9ac6-110">Dynamics 365 for Finance and Operations sürüm 7.1, KB 4094701 Boyut değerleri hesap planı sınırlayıcısını içerdiğinde mali boyutlar girilemez</span><span class="sxs-lookup"><span data-stu-id="e9ac6-110">Dynamics 365 for Finance and Operations version 7.1, KB 4094701 Cannot enter the financial dimensions when the dimension values contain the chart of accounts delimiter</span></span>
- <span data-ttu-id="e9ac6-111">Dynamics 365 for Finance and Operations sürüm 7.2, KB 4092967 Alt proje biçimi boyut sınırlayıcıyı içerdiğinde alt proje boyut olarak seçilemez</span><span class="sxs-lookup"><span data-stu-id="e9ac6-111">Dynamics 365 for Finance and Operations version 7.2, KB 4092967 Cannot choose sub-project as dimension when sub-project format contains the dimension delimiter</span></span>

## <a name="update-delimiter"></a><span data-ttu-id="e9ac6-112">Sınırlayıcıyı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="e9ac6-112">Update delimiter</span></span>
<span data-ttu-id="e9ac6-113">Hesap Planıyla bir çakışma varsa, Hesap planı sınırlayıcısı ve proje/alt proje kodu biçimi değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="e9ac6-113">If there is a conflict with the Chart of Accounts, the Chart of accounts delimiter and the project/subproject ID format can be changed.</span></span> <span data-ttu-id="e9ac6-114">Diğer boyut sınırlayıcılar değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="e9ac6-114">No other dimension delimiters can be changed.</span></span> 
- <span data-ttu-id="e9ac6-115">Finance and Operations'a yükseltme yaptıktan sonra hesap planı sınırlayıcısını **Genel muhasebe parametreleri** > **Hesap planı ve boyutlar** > **Sınırlayıcıyı değiştir** altından değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e9ac6-115">You can change the chart of accounts delimiter after upgrade to Finance and Operations in **General ledger parameters** > **Chart of accounts and dimensions** > **Change delimiter**.</span></span> 
- <span data-ttu-id="e9ac6-116">Tek çakışma proje/alt proje kodu biçimiyle olduğunda, bu değeri **Proje yönetimi ve muhasebe parametreleri** > **Genel** > **Alt proje biçimini değiştir** altından değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e9ac6-116">If the only conflict is with the project/subproject ID format, you can change that value in **Project management and accounting parameters** > **General** > **Modify subproject format**.</span></span> 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a><span data-ttu-id="e9ac6-117">Güncelleştirilen sınırlayıcıların ortamınız için gerekip gerekmediğini belirleme</span><span class="sxs-lookup"><span data-stu-id="e9ac6-117">How to determine if your environment requires updated delimiters</span></span> 
<span data-ttu-id="e9ac6-118">Yükseltilen ortamınızdaki sınırlayıcılarda çakışma varsa, bölümlenmiş giriş denetimi veya boyut giriş denetimine değer girerken tutarsızlıkla karşılaşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e9ac6-118">If delimiters in your upgraded environment are conflicting, you may experience instability when entering values in a segmented entry control or dimension entry control.</span></span> <span data-ttu-id="e9ac6-119">Bunun anlamı, hesap ve boyut birleşimleri girerken, daima aramaları veya bir açılır menüyü kullanmanız gerekeceğidir.</span><span class="sxs-lookup"><span data-stu-id="e9ac6-119">This means that you will need to always use lookups or a flyout menu when entering account and dimension combinations.</span></span>

