---
title: Bir kullanıcıdaki çalışmayı iptal edemezsiniz
description: Bir kullanıcıdaki çalışmayı iptal edemezsiniz
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
ms.openlocfilehash: e5f6912cfb1d5be8e46b7989856af99f8a611c11
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924413"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a><span data-ttu-id="9416e-103">Bir kullanıcıdaki çalışmayı iptal edemezsiniz</span><span class="sxs-lookup"><span data-stu-id="9416e-103">You can't cancel work that is on a user</span></span>

<span data-ttu-id="9416e-104">Hata kodu: WAX708</span><span class="sxs-lookup"><span data-stu-id="9416e-104">Error code: WAX708</span></span>

## <a name="symptoms"></a><span data-ttu-id="9416e-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="9416e-105">Symptoms</span></span>

<span data-ttu-id="9416e-106">Sistem, aşağıdaki hata iletisini gösterir:</span><span class="sxs-lookup"><span data-stu-id="9416e-106">The system shows the following error message:</span></span>

> <span data-ttu-id="9416e-107">Kullanıcı üzerindeki bir işi iptal edemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="9416e-107">You cannot cancel work that is on a user.</span></span>

## <a name="cause"></a><span data-ttu-id="9416e-108">Nedeni</span><span class="sxs-lookup"><span data-stu-id="9416e-108">Cause</span></span>

<span data-ttu-id="9416e-109">İş, bir kullanıcı tarafından kilitlenmiş ve iptal edilemiyor.</span><span class="sxs-lookup"><span data-stu-id="9416e-109">The work is locked by a user and can't be canceled.</span></span> <span data-ttu-id="9416e-110">Bunu onaylamak için, iş kodunu açın ve **Genel** sekmesini açın. İş kilitliyse, **İş durumu** alanı *Devam ediyor* olarak ayarlıdır ve **Kilitleyen** alanında bir kullanıcı kimliği bulunur.</span><span class="sxs-lookup"><span data-stu-id="9416e-110">To confirm this, open the work ID and then open the **General** tab. If the work is locked, the **Work status** field will be set to *In progress*, and the **Locked by** field will be set to a user ID.</span></span>

## <a name="resolution"></a><span data-ttu-id="9416e-111">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="9416e-111">Resolution</span></span>

<span data-ttu-id="9416e-112">İşi iptal etmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="9416e-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="9416e-113">**Ambar yönetimi \> Periyodik görevler \> Temizleme \>Çalışmayı iptal et**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="9416e-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="9416e-114">**İş kimliği** alanında, iptal etmek istediğiniz iş kaydının kodunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="9416e-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="9416e-115">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="9416e-115">Select **OK**.</span></span>
1. <span data-ttu-id="9416e-116">Çalışmayı iptal etmek istediğinizi onaylamak için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9416e-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="9416e-117">Daha fazla bilgi için bkz. [Özel durum işleme için ambar işini iptal etme](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="9416e-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
