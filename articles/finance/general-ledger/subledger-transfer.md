---
title: Yardımcı defterden Genel muhasebeye transfer
description: Bu konu, Microsoft Dynamics 365 Finance içindeki genel muhasebe transfer işlemiyle ilgili olan yetenekleri açıklar.
author: roschlom
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 1efdf095e379b73d553ca3525abbeee8ca35bcbb
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897516"
---
# <a name="subledger-transfer-to-the-general-ledger"></a><span data-ttu-id="0b7ca-103">Yardımcı defterden Genel muhasebeye transfer</span><span class="sxs-lookup"><span data-stu-id="0b7ca-103">Subledger transfer to the General ledger</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b7ca-104">Bu konuda, Microsoft Dynamics 365 Finance'un, alt genel muhasebe günlük girişleri toplu işleri aktarma kurallarıyla ilişkili özellikleri açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="0b7ca-104">This topic describes capabilities in Microsoft Dynamics 365 Finance that are related to the rules for transferring batches of subledger journal entries.</span></span>

<span data-ttu-id="0b7ca-105">Sürüm 8.1'de kuralların aktarılmasına izin vermek için değişiklikler yapıldı ve **Zaman Uyumlu** seçeneği kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0b7ca-105">In version 8.1, changes were made to allow the transfer of rules, which deprecated the **Synchronous** option.</span></span> <span data-ttu-id="0b7ca-106">Daha fazla bilgi için bkz. [Finance and Operations için kaldırılan veya artık kullanılmayan özellikler](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).</span><span class="sxs-lookup"><span data-stu-id="0b7ca-106">For more information, see [Removed or deprecated features for Finance and Operations](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).</span></span>

<span data-ttu-id="0b7ca-107">Alt genel muhasebe toplu işlemlerine transfer için aşağıdaki seçenekler kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0b7ca-107">The following options are available for transferring subledger batches.</span></span> 

 - <span data-ttu-id="0b7ca-108">Zaman uyumsuz – Bu seçenek, hemen, genel muhasebe hesap girişlerinin transfer zamanlamasını General muhasebeye nakleder.</span><span class="sxs-lookup"><span data-stu-id="0b7ca-108">Asynchronous – This option will immediately schedule the transfer of the subledger accounting entries to the general ledger.</span></span> <span data-ttu-id="0b7ca-109">Kaynaklar bu isteği sunucuda işlemek için serbest bırakılır bırakılmaz, genel muhasebe fişi kaydedilecektir.</span><span class="sxs-lookup"><span data-stu-id="0b7ca-109">The general ledger voucher will be recorded as soon as resources are free to process this request on the server.</span></span> 

- <span data-ttu-id="0b7ca-110">Planlanan toplu iş-bu seçenek, girişlerin teslim alındığı sırada işleneceği genel muhasebede işleme sırasına aktarılan alt genel muhasebe hesap girişlerini ekler.</span><span class="sxs-lookup"><span data-stu-id="0b7ca-110">Scheduled batch – This option will add the subledger accounting entries that are being transferred to the processing queue in the general ledger, where the entries will be processed in order received.</span></span> <span data-ttu-id="0b7ca-111">Kaynaklar bu isteği sunucuda işlemek için serbest bırakılır bırakılmaz, genel muhasebe fişi kaydedilecektir.</span><span class="sxs-lookup"><span data-stu-id="0b7ca-111">The general ledger voucher will be recorded at the scheduled time if resources are free to process this batch job on the server.</span></span> 
 
<span data-ttu-id="0b7ca-112">Sürüm 10.0.8'de Zaman uyumsuz seçeneğinin performansını artırmak için iyileştirmeler yapılmıştır.</span><span class="sxs-lookup"><span data-stu-id="0b7ca-112">In version 10.0.8, improvements were made to enhance the performance of the Asynchronous option.</span></span> <span data-ttu-id="0b7ca-113">Bu özellik, performansın en iyi duruma getirilmesi **Genel muhasebe Özellik adı alt genel muhasebe aktarımı** altında etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="0b7ca-113">This feature is enabled under the feature name **Subledger transfer to General Ledger performance optimization**.</span></span> 
 
<span data-ttu-id="0b7ca-114">Bu işlevsellik, alt iş defterindeki verilerin genel muhasebeye aktarılmasını geliştirir.</span><span class="sxs-lookup"><span data-stu-id="0b7ca-114">This functionality improves the transfer of data from the subledger to the general ledger.</span></span> <span data-ttu-id="0b7ca-115">Sürecin daha etkili olmasını sağlar ve transfer için birlikte daha küçük hareket kümeleri gruplandırır.</span><span class="sxs-lookup"><span data-stu-id="0b7ca-115">It allows the process to be more efficient, and it groups together sets of smaller transactions to transfer.</span></span> <span data-ttu-id="0b7ca-116">Bu, toplu iş sunucusunun daha etkili bir şekilde kullanılmasına olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="0b7ca-116">This allows for a more efficient use of the batch server.</span></span> <span data-ttu-id="0b7ca-117">Bu işlevsellik, Zaman Uyumsuz transfer seçeneğinin çalışması için toplu iş sunucusunun ayarlanmış, çevrimiçi ve çalışır durumda olmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="0b7ca-117">This functionality requires that the batch server be set up, online, and functioning in order for the Asynchronous transfer option to work.</span></span> 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]