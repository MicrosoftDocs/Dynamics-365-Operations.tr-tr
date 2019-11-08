---
title: Hesap planı ayırıcısını benzersiz yapma
description: Bu konu nasıl hesap planı ve boyut için aynı sınırlayıcıya sahip olamayacağınızı açıklar. Yükseltmeden sonra sınırlayıcı değerlerini değiştirmeniz gerekir.
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 5861bcaa42f7bc5ec20916fe1a44418bdd9c2ffe
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550920"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a><span data-ttu-id="b725f-104">Hesap planı ayırıcısını benzersiz yapma</span><span class="sxs-lookup"><span data-stu-id="b725f-104">Make the chart of accounts delimiter unique</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b725f-105">Microsoft Dynamics AX 2012'de, hesap planı ve boyut değerleri için aynı sınırlayıcı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b725f-105">In Microsoft Dynamics AX 2012, you could use the same delimiter for your chart of accounts and dimension values.</span></span> <span data-ttu-id="b725f-106">Finance and Operations'ın geçerli sürümlerinde hesap planı ve boyut değerleri için aynı sınırlayıcıya sahip olamazsınız.</span><span class="sxs-lookup"><span data-stu-id="b725f-106">In current versions of Finance and Operations, you cannot have the same delimiter for the chart of accounts and dimension values.</span></span> <span data-ttu-id="b725f-107">Yinelenen bir sınırlayıcı varsa, yükseltme işleminden sonra değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b725f-107">If there is a duplicate delimiter, you can change it after upgrade.</span></span> 

<span data-ttu-id="b725f-108">Bu özellik aşağıdaki sürümlerde kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="b725f-108">This feature is available in the following versions:</span></span>
- <span data-ttu-id="b725f-109">Finance and Operations sürüm 8.0</span><span class="sxs-lookup"><span data-stu-id="b725f-109">Finance and Operations version 8.0</span></span>
- <span data-ttu-id="b725f-110">Finance and Operations sürüm 7.1, KB 4094701 Boyut değerleri hesap planı sınırlayıcısını içerdiğinde mali boyutlar girilemez</span><span class="sxs-lookup"><span data-stu-id="b725f-110">Finance and Operations version 7.1, KB 4094701 Cannot enter the financial dimensions when the dimension values contain the chart of accounts delimiter</span></span>
- <span data-ttu-id="b725f-111">Finance and Operations sürüm 7.2, KB 4092967 Alt proje biçimi boyut sınırlayıcıyı içerdiğinde alt proje boyut olarak seçilemez</span><span class="sxs-lookup"><span data-stu-id="b725f-111">Finance and Operations version 7.2, KB 4092967 Cannot choose sub-project as dimension when sub-project format contains the dimension delimiter</span></span>

## <a name="update-delimiter"></a><span data-ttu-id="b725f-112">Sınırlayıcıyı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="b725f-112">Update delimiter</span></span>
<span data-ttu-id="b725f-113">Hesap planıyla bir çakışma varsa, hesap planı sınırlayıcısı ve proje/alt proje kodu biçimi değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="b725f-113">If there is a conflict with the chart of accounts, the chart of accounts delimiter and the project/subproject ID format can be changed.</span></span> <span data-ttu-id="b725f-114">Diğer boyut sınırlayıcılar değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="b725f-114">No other dimension delimiters can be changed.</span></span> 
- <span data-ttu-id="b725f-115">Yükseltme yaptıktan sonra hesap planı sınırlayıcısını **Genel muhasebe parametreleri** > **Hesap planı ve boyutlar** > **Sınırlayıcıyı değiştir** altından değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b725f-115">You can change the chart of accounts delimiter after upgrade in **General ledger parameters** > **Chart of accounts and dimensions** > **Change delimiter**.</span></span> 
- <span data-ttu-id="b725f-116">Tek çakışma proje/alt proje kodu biçimiyle olduğunda, bu değeri **Proje yönetimi ve muhasebe parametreleri** > **Genel** > **Alt proje biçimini değiştir** altından değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b725f-116">If the only conflict is with the project/subproject ID format, you can change that value in **Project management and accounting parameters** > **General** > **Modify subproject format**.</span></span> 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a><span data-ttu-id="b725f-117">Güncelleştirilen sınırlayıcıların ortamınız için gerekip gerekmediğini belirleme</span><span class="sxs-lookup"><span data-stu-id="b725f-117">How to determine if your environment requires updated delimiters</span></span> 
<span data-ttu-id="b725f-118">Yükseltilen ortamınızdaki sınırlayıcılarda çakışma varsa, bölümlenmiş giriş denetimi veya boyut giriş denetimine değer girerken tutarsızlıkla karşılaşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b725f-118">If delimiters in your upgraded environment are conflicting, you may experience instability when entering values in a segmented entry control or dimension entry control.</span></span> <span data-ttu-id="b725f-119">Bunun anlamı, hesap ve boyut birleşimleri girerken, daima aramaları veya bir açılır menüyü kullanmanız gerekeceğidir.</span><span class="sxs-lookup"><span data-stu-id="b725f-119">This means that you will need to always use lookups or a flyout menu when entering account and dimension combinations.</span></span>
