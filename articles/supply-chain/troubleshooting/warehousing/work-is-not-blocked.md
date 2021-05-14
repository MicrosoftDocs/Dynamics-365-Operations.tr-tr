---
title: Çalışma durdurulmadı
description: Çalışma durdurulmamış
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d64ab282972e46e8857581b59e5705dd15667328
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924216"
---
# <a name="work-isnt-blocked"></a><span data-ttu-id="5d4da-103">Çalışma durdurulmamış</span><span class="sxs-lookup"><span data-stu-id="5d4da-103">Work isn't blocked</span></span>

<span data-ttu-id="5d4da-104">Hata kodu: WHSUnblockNotBlockedWorkErrorMessage</span><span class="sxs-lookup"><span data-stu-id="5d4da-104">Error code: WHSUnblockNotBlockedWorkErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="5d4da-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="5d4da-105">Symptoms</span></span>

<span data-ttu-id="5d4da-106">Sistem, aşağıdaki hata iletisini gösterir:</span><span class="sxs-lookup"><span data-stu-id="5d4da-106">The system shows the following error message:</span></span>

> <span data-ttu-id="5d4da-107">%1 koduna sahip çalışma durdurulmadı.</span><span class="sxs-lookup"><span data-stu-id="5d4da-107">Work with Id %1 is not blocked.</span></span>

## <a name="cause"></a><span data-ttu-id="5d4da-108">Nedeni</span><span class="sxs-lookup"><span data-stu-id="5d4da-108">Cause</span></span>

<span data-ttu-id="5d4da-109">Dalgadaki, **Dalga durduruldu** seçeneği *Hayır* olarak ayarlı.</span><span class="sxs-lookup"><span data-stu-id="5d4da-109">The **Blocked wave** option on the wave is set to *No*.</span></span> <span data-ttu-id="5d4da-110">İşin durdurulması, iş durdurulmuş olmadığından kaldırılamıyor.</span><span class="sxs-lookup"><span data-stu-id="5d4da-110">The work can't be unblocked because it isn't currently blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="5d4da-111">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="5d4da-111">Resolution</span></span>

 <span data-ttu-id="5d4da-112">Yalnızca **Dalga durduruldu** seçeneğinin *Evet* olarak ayarlandığı işlerin durdurulması kaldırılabilir.</span><span class="sxs-lookup"><span data-stu-id="5d4da-112">Only work where the **Blocked wave** option is set to *Yes* can be unblocked.</span></span>
