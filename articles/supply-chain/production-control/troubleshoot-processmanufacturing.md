---
title: Süreç üretimi ile ilgili sorunları giderme
description: Bu konuda, süreç üretimi ile çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklanmaktadır.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 63993fca2164301d31dbfa1474a4cf5eb16273e6
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516891"
---
# <a name="troubleshoot-process-manufacturing"></a><span data-ttu-id="3bac2-103">Süreç üretimi ile ilgili sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="3bac2-103">Troubleshoot process manufacturing</span></span>

<span data-ttu-id="3bac2-104">Bu konuda, süreç üretimi ile çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="3bac2-104">This topic describes how to fix issues that you might encounter while you work with process manufacturing.</span></span>

## <a name="when-i-use-the-job-card-device-to-report-a-partial-quantity-on-the-last-job-in-a-production-order-all-the-previous-jobs-on-that-order-that-have-a-status-of-in-progress-are-automatically-ended"></a><span data-ttu-id="3bac2-105">Bir üretim emrindeki son projedeki kısmi miktarı raporlamak için iş kartı cihazını kullandığımda, Devam ediyor durumundaki tüm önceki işler otomatik olarak sonlandırılıyor.</span><span class="sxs-lookup"><span data-stu-id="3bac2-105">When I use the job card device to report a partial quantity on the last job in a production order, all the previous jobs on that order that have a status of In progress are automatically ended.</span></span>

<span data-ttu-id="3bac2-106">Bu davranış tasarımdan kaynaklanır.</span><span class="sxs-lookup"><span data-stu-id="3bac2-106">This behavior is by design.</span></span> <span data-ttu-id="3bac2-107">**Üretim emri Varsayılanları** sayfasında, **Tamamlandı olarak bildir** sekmesinde, **Rotaya bitiş işareti yerleştir** adlı bir seçenek vardır.</span><span class="sxs-lookup"><span data-stu-id="3bac2-107">On the **Production order defaults** page, on the **Report as finished** tab, there is an option that is named **End-mark route**.</span></span> <span data-ttu-id="3bac2-108">Bu seçenek *Evet* olarak ayarlanırsa bir çalışan son işlemi bildirmek üzere iş kartı cihazını veya iş kartı terminalini kullandığında rota kartı günlüğü deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="3bac2-108">If this topic is set to *Yes*, a route card journal is posted when a worker uses the job card device or job card terminal to report the last operation.</span></span> <span data-ttu-id="3bac2-109">Bu günlük tüm işlemleri tamamlandı olarak işaretler ve tüm üretim işlerini sonlandırır.</span><span class="sxs-lookup"><span data-stu-id="3bac2-109">This journal marks all the operations as completed and ends all the production jobs.</span></span> <span data-ttu-id="3bac2-110">**Rotaya bitiş işareti ekle** seçeneği *Evet* olarak ayarlandığında sistem, çalışanın son işlemi bildirdiğinde seçtiği iş durumunu dikkate almaz.</span><span class="sxs-lookup"><span data-stu-id="3bac2-110">When the **End-mark route** option is set to *Yes*, the system doesn't consider the job status that the worker selected when they reported the last operation.</span></span> <span data-ttu-id="3bac2-111">Sistem aynı zamanda çalışanın tam mı yoksa kısmi bir miktar mı bildirdiğini de dikkate almaz.</span><span class="sxs-lookup"><span data-stu-id="3bac2-111">The system also doesn't consider whether the worker is reporting a full or partial quantity.</span></span>

## <a name="when-i-attempt-a-stock-closing-i-receive-the-following-warning-message-no-execution-of-backflush-costing-calculation-with-a-date-1-matching-period-end-has-been-registered"></a><span data-ttu-id="3bac2-112">Stok kapanışı yapmaya çalıştığımda, aşağıdaki uyarı iletisini alıyorum: "Bir %1 tarihi eşleştirme dönemi sonuyla hiçbir geriye dönük maliyet hesaplama yürütmesi kaydedilmedi."</span><span class="sxs-lookup"><span data-stu-id="3bac2-112">When I attempt a stock closing, I receive the following warning message: "No execution of Backflush costing calculation with a date %1 matching period end has been registered."</span></span>

<span data-ttu-id="3bac2-113">10.0.13 öncesi sürümlerde, stok kapatma sırasında aşağıdaki hatalı uyarı iletisini alırsınız:</span><span class="sxs-lookup"><span data-stu-id="3bac2-113">In releases before release 10.0.13, if you aren't using the lean production costing flow, you receive the following erroneous warning message during inventory closing:</span></span>

> <span data-ttu-id="3bac2-114">Bir stok kapanışını bir %1 tarihiyle yürütmek üzeresiniz.</span><span class="sxs-lookup"><span data-stu-id="3bac2-114">You are about to execute an Inventory close with a date %1.</span></span> <span data-ttu-id="3bac2-115">Bir %1 tarihi eşleştirme dönemi sonuyla hiçbir geriye dönük maliyet hesaplama yürütmesi kaydedilmedi.</span><span class="sxs-lookup"><span data-stu-id="3bac2-115">No execution of Backflush costing calculation with a date %1 matching period end has been registered.</span></span> <span data-ttu-id="3bac2-116">Bir %1 tarihi eşleştirme dönemi sonuyla bir geriye dönük maliyet hesaplaması yürütmeyi unutmayın.</span><span class="sxs-lookup"><span data-stu-id="3bac2-116">Please remember to execute a Backflush costing calculation with a date of %1 matching period end.</span></span> <span data-ttu-id="3bac2-117">Stok değerlemesi, satılan malların maliyeti ve varyantlar, bu işlem yürütülünceye kadar Yardımcı Kayıt Defteri veya Genel Kayıt Defteri'nde doğru olmayabilir.</span><span class="sxs-lookup"><span data-stu-id="3bac2-117">The valuation of inventories, cost of goods sold and variances might not be correct in Subledger or General ledger until this has been executed.</span></span>

<span data-ttu-id="3bac2-118">Bu sorun 10.0.13 ve sonraki sürümlerde giderilmiştir.</span><span class="sxs-lookup"><span data-stu-id="3bac2-118">This issue has been fixed in release 10.0.13 and later.</span></span> <span data-ttu-id="3bac2-119">Daha fazla bilgi için bkz. [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).</span><span class="sxs-lookup"><span data-stu-id="3bac2-119">For more information, see [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).</span></span>
