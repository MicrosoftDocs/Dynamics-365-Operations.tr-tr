---
title: Kapatılan son iş satırı, yerine koy olmalıdır
description: Kapatılan son iş satırı, yerine koy olmalıdır
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a5b78154b51252b3ac96ba28c254e823caf87019
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924387"
---
# <a name="the-last-closed-work-line-must-be-a-put"></a><span data-ttu-id="7e32a-103">Kapatılan son iş satırı, yerine koy olmalıdır</span><span class="sxs-lookup"><span data-stu-id="7e32a-103">The last closed work line must be a put</span></span>

<span data-ttu-id="7e32a-104">Hata kodu: WAX1285</span><span class="sxs-lookup"><span data-stu-id="7e32a-104">Error code: WAX1285</span></span>

## <a name="symptoms"></a><span data-ttu-id="7e32a-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="7e32a-105">Symptoms</span></span>

<span data-ttu-id="7e32a-106">Sistem, aşağıdaki hata iletisini gösterir:</span><span class="sxs-lookup"><span data-stu-id="7e32a-106">The system shows the following error message:</span></span>

> <span data-ttu-id="7e32a-107">Kapatılan son iş satırı, yerine koy olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7e32a-107">The last closed work line must be a put.</span></span>

## <a name="cause"></a><span data-ttu-id="7e32a-108">Nedeni</span><span class="sxs-lookup"><span data-stu-id="7e32a-108">Cause</span></span>

<span data-ttu-id="7e32a-109">İş, geçerli durumunda iptal edilemez.</span><span class="sxs-lookup"><span data-stu-id="7e32a-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="7e32a-110">Son iş satırında, **İş durumu** alanı *Kapalı* olarak ayarlı ancak **İş türü** alanı *Yerine koy* olarak ayarlanmamış.</span><span class="sxs-lookup"><span data-stu-id="7e32a-110">On the last work line, the **Work status** field is set to *Closed*, but the **Work type** field isn't set to *Put*.</span></span>

## <a name="resolution"></a><span data-ttu-id="7e32a-111">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="7e32a-111">Resolution</span></span>

<span data-ttu-id="7e32a-112">İşi iptal etmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="7e32a-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="7e32a-113">**Ambar yönetimi \> Periyodik görevler \> Temizleme \>Çalışmayı iptal et**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="7e32a-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="7e32a-114">**İş kimliği** alanında, iptal etmek istediğiniz iş kaydının kodunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="7e32a-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="7e32a-115">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7e32a-115">Select **OK**.</span></span>
1. <span data-ttu-id="7e32a-116">Çalışmayı iptal etmek istediğinizi onaylamak için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7e32a-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="7e32a-117">Daha fazla bilgi için bkz. [Özel durum işleme için ambar işini iptal etme](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="7e32a-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
