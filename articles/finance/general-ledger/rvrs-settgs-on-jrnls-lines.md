---
title: Günlükler ve satırlardaki ayarları tersine çevirme
description: Bu konuda, yevmiye defterindeki bir ters işlem girişinin deftere nakledilmiş işleme neden dahil edilemediği ele alınmaktadır.
author: kweekley
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 74020f6fc9b0fa8e05a1e2a09fd13dcd60490dc0
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028590"
---
# <a name="reverse-settings-on-journals-and-lines"></a><span data-ttu-id="aefc5-103">Günlükler ve satırlardaki ayarları tersine çevirme</span><span class="sxs-lookup"><span data-stu-id="aefc5-103">Reverse settings on journals and lines</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aefc5-104">Bu konuda, yevmiye defterindeki bir ters işlem girişinin deftere nakledilmiş işleme neden dahil edilemediği ele alınmaktadır.</span><span class="sxs-lookup"><span data-stu-id="aefc5-104">This topic addresses why a reversing entry that was entered on a general journal might not be included on the posted transaction.</span></span>  

## <a name="symptom"></a><span data-ttu-id="aefc5-105">Belirti</span><span class="sxs-lookup"><span data-stu-id="aefc5-105">Symptom</span></span>

<span data-ttu-id="aefc5-106">Yevmiye defteri, günlükte bir ters işlem girişi ve ters işlem tarihi içerir.</span><span class="sxs-lookup"><span data-stu-id="aefc5-106">A general journal includes a reversing entry and reversing date on the journal.</span></span> <span data-ttu-id="aefc5-107">Günlüğü gönderdiğinizde fişlerin hiçbiri tersine çevrilmez.</span><span class="sxs-lookup"><span data-stu-id="aefc5-107">When you post the journal, none of the vouchers are reversed.</span></span> <span data-ttu-id="aefc5-108">Bu neden gerçekleşir?</span><span class="sxs-lookup"><span data-stu-id="aefc5-108">Why does this happen?</span></span>

## <a name="resolution"></a><span data-ttu-id="aefc5-109">Çözüm</span><span class="sxs-lookup"><span data-stu-id="aefc5-109">Resolution</span></span>

<span data-ttu-id="aefc5-110">Günlük gönderildiğinde ters işlem yalnızca fişin **Satırlar** bölümündeki **Ters işlem girişi** ve **Ters işlem tarihi** ayarlarında görünür.</span><span class="sxs-lookup"><span data-stu-id="aefc5-110">When the journal is posted, the reversing process looks only at the **Revering entry** and **Reversing date** settings on the **Lines** section of the voucher.</span></span> <span data-ttu-id="aefc5-111">Bu yaklaşım, günlüğün ters işlem için işaretlenmiş bazı fişlerin ve işaretlenmemiş diğer fişlerin dahil edilmesine olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="aefc5-111">This approach allows a journal to include some vouchers that are marked for reversing, and others that are not.</span></span>

<span data-ttu-id="aefc5-112">Günlükteki değerler yalnızca *yeni* satırlar eklenirken varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="aefc5-112">The values from the journal are only used as defaults when adding *new* lines.</span></span> <span data-ttu-id="aefc5-113">Günlükteki değerleri değiştirdiğinizde mevcut satırlar etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="aefc5-113">Changing the values on the journal doesn’t affect existing lines.</span></span> <span data-ttu-id="aefc5-114">Bu örnekte, ilk olarak fiş satırları girilmiştir.</span><span class="sxs-lookup"><span data-stu-id="aefc5-114">In this example, the voucher lines were entered first.</span></span> <span data-ttu-id="aefc5-115">Günlüğü ters işlem olarak atamadan önce satır ayrıntısını girdiğinizde atama, ters işlem girişi ve tarihi olarak mevcut satırlara uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="aefc5-115">When you enter the line detail before designating the journal as reversing, the designation as a reversing entry and date won't be applied to any existing lines.</span></span>

<span data-ttu-id="aefc5-116">Mevcut bir satırdaki ters işlem girişini veya ters işlem tarihini değiştirdiğinizde bu değişiklik aynı fişteki diğer satırlara yayılır.</span><span class="sxs-lookup"><span data-stu-id="aefc5-116">Changing the reversing entry or reversing date on an existing line propagates that change to other lines in the same voucher.</span></span> <span data-ttu-id="aefc5-117">Performansı en iyi duruma getirmek için ızgara, değişiklikler diğer satırlara yayıldıktan sonra yenilenmez.</span><span class="sxs-lookup"><span data-stu-id="aefc5-117">To optimize performance, the grid is not refreshed after propagating changes to other Lines.</span></span> <span data-ttu-id="aefc5-118">Izgarayı yenileyerek güncelleştirilmiş değerleri görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aefc5-118">You can display the updated values by refreshing the grid.</span></span>


