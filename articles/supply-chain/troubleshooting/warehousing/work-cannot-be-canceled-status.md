---
title: İş, durumu nedeniyle iptal edilemiyor
description: İş, durumu nedeniyle iptal edilemiyor
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
ms.openlocfilehash: 60b4da44ca5e6790302e0797640317cef8493db7
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924267"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a><span data-ttu-id="a51ce-103">İş, durumu nedeniyle iptal edilemiyor</span><span class="sxs-lookup"><span data-stu-id="a51ce-103">Work can't be canceled because of its status</span></span>

<span data-ttu-id="a51ce-104">Hata kodu: WAX2190</span><span class="sxs-lookup"><span data-stu-id="a51ce-104">Error code: WAX2190</span></span>

## <a name="symptoms"></a><span data-ttu-id="a51ce-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="a51ce-105">Symptoms</span></span>

<span data-ttu-id="a51ce-106">Sistem, aşağıdaki hata iletisini gösterir:</span><span class="sxs-lookup"><span data-stu-id="a51ce-106">The system shows the following error message:</span></span>

> <span data-ttu-id="a51ce-107">İş %1 %2 durumunda olduğu için, iptal edemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="a51ce-107">You cannot cancel work %1 because it has a status of %2.</span></span>

## <a name="cause"></a><span data-ttu-id="a51ce-108">Nedeni</span><span class="sxs-lookup"><span data-stu-id="a51ce-108">Cause</span></span>

<span data-ttu-id="a51ce-109">İş, geçerli durumunda iptal edilemez.</span><span class="sxs-lookup"><span data-stu-id="a51ce-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="a51ce-110">İş başlığı veya iş satırları, beklenen **İş durumu** değerine sahip değil.</span><span class="sxs-lookup"><span data-stu-id="a51ce-110">The work header or work lines don't have the expected **Work status** value.</span></span> <span data-ttu-id="a51ce-111">İş başlığındaki **İş durumu** alanı *Açık* veya *Devam ediyor* olarak ayarlı değil.</span><span class="sxs-lookup"><span data-stu-id="a51ce-111">The **Work status** field on the work header isn't set to *Open* or *In progress*.</span></span>

## <a name="resolution"></a><span data-ttu-id="a51ce-112">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="a51ce-112">Resolution</span></span>

<span data-ttu-id="a51ce-113">İşi iptal etmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="a51ce-113">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="a51ce-114">**Ambar yönetimi \> Periyodik görevler \> Temizleme \>Çalışmayı iptal et**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="a51ce-114">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="a51ce-115">**İş kimliği** alanında, iptal etmek istediğiniz iş kaydının kodunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="a51ce-115">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="a51ce-116">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a51ce-116">Select **OK**.</span></span>
1. <span data-ttu-id="a51ce-117">Çalışmayı iptal etmek istediğinizi onaylamak için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a51ce-117">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="a51ce-118">Daha fazla bilgi için bkz. [Özel durum işleme için ambar işini iptal etme](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="a51ce-118">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
