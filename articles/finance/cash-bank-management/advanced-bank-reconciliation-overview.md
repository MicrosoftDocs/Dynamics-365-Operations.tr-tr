---
title: Gelişmiş banka mutabakatına genel bakış
description: Bu makale gelişmiş banka mutabakat işleminin akışını açıklar. Gelişmiş banka mutabakatı özelliği, banka hareketleri içinden otomatik olarak mutabakatı alınan banka ekstrelerini içe aktarmanıza izin verir.
author: panolte
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b26b6e1e50e5a9b53ca6b5315de760f5bcec4769
ms.sourcegitcommit: 74b10104338222a945684d841d60ab4b8e570168
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3899409"
---
# <a name="advanced-bank-reconciliation-overview"></a><span data-ttu-id="28461-104">Gelişmiş banka mutabakatına genel bakış</span><span class="sxs-lookup"><span data-stu-id="28461-104">Advanced bank reconciliation overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28461-105">Bu makale gelişmiş banka mutabakat işleminin akışını açıklar.</span><span class="sxs-lookup"><span data-stu-id="28461-105">This article describes the flow for the advanced bank reconciliation process.</span></span> <span data-ttu-id="28461-106">Gelişmiş banka mutabakatı özelliği, banka hareketleri içinden otomatik olarak mutabakatı alınan banka ekstrelerini içe aktarmanıza izin verir.</span><span class="sxs-lookup"><span data-stu-id="28461-106">The advanced bank reconciliation feature lets you import bank statements that can be automatically reconciled from within bank transactions.</span></span>

<span data-ttu-id="28461-107">Gelişmiş banka mutabakatı özelliği banka ekstrelerini içe aktarmanıza izin verir.</span><span class="sxs-lookup"><span data-stu-id="28461-107">The advanced bank reconciliation feature lets you import bank statements.</span></span> <span data-ttu-id="28461-108">İçe aktarılan banka ekstresi için daha sonra banka hareketleri içinde otomatik olarak mutabakat sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="28461-108">The imported bank statement can then be automatically reconciled from within bank transactions.</span></span> <span data-ttu-id="28461-109">Burada, gelişmiş banka mutabakatı akış içindeki adımlar açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="28461-109">Here are the steps in the advanced bank reconciliation flow.</span></span>

1.  <span data-ttu-id="28461-110">Bir banka ekstresini içe aktarın.</span><span class="sxs-lookup"><span data-stu-id="28461-110">Set up a bank statement import.</span></span>
    -   <span data-ttu-id="28461-111">Banka ekstrelerini veri varlığı çerçevesiyle içe aktarın.</span><span class="sxs-lookup"><span data-stu-id="28461-111">Import bank statements through the data entity framework.</span></span>
    -   <span data-ttu-id="28461-112">Üç tipik banka ekstresi formatı oluşturulur: ISO20022, BAI2 ve MT940.</span><span class="sxs-lookup"><span data-stu-id="28461-112">Three typical bank statement formats are built in: ISO20022, BAI2, and MT940.</span></span>
    -   <span data-ttu-id="28461-113">Bu işlev herhangi bir formata genişletilebilir.</span><span class="sxs-lookup"><span data-stu-id="28461-113">The functionality can be extended to any format.</span></span>

2.  <span data-ttu-id="28461-114">Gelişmiş banka mutabakatı için kullanılacak bir numara sırası oluşturun ve banka mutabakatı eşleştirme kurallarını tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="28461-114">Set up a number sequence to use for advanced bank reconciliation, and define the bank reconciliation matching rules.</span></span>
    -   <span data-ttu-id="28461-115">Bir mutabakat eşleştirme kuralı, mutabakat süreci sırasında banka ekstresi satırlarını ve Microsoft Dynamics 365 Finance banka hareketi satırlarını filtrelemek için kullanılan bir ölçüt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="28461-115">A reconciliation matching rule is a set of criteria that are used to filter bank statement lines and Microsoft Dynamics 365 Finance bank transaction lines during the reconciliation process.</span></span> <span data-ttu-id="28461-116">İş yönteminize bağlı olarak, birden fazla eşleşme kuralını, mutabakat sürecinizi otomatikleştirme ve optimize etmek için ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="28461-116">Depending on your business practice, you can set up more than one matching rule to automate and optimize your reconciliation process.</span></span>

3.  <span data-ttu-id="28461-117">Banka ekstrelerinin Finance banka hareketleriyle mutabakatını sağlayın.</span><span class="sxs-lookup"><span data-stu-id="28461-117">Reconcile bank statements with Finance bank transactions.</span></span>
    -   <span data-ttu-id="28461-118">Mutabakat günlükleri için otomatik eşleştirme ve oluşturma işlemleri yürütün.</span><span class="sxs-lookup"><span data-stu-id="28461-118">Perform automatic matching and creation of reconciliation journals.</span></span>
    -   <span data-ttu-id="28461-119">Banka ekstrelerini ve Finance banka hareketlerini yan yana görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="28461-119">View bank statements and Finance bank transactions side by side.</span></span>
    -   <span data-ttu-id="28461-120">Bir banka ekstresinde görüntülenmesine karşın Finance uygulamasında görüntülenmiyorsa, Finance banka hareketlerini otomatik olarak nakledin.</span><span class="sxs-lookup"><span data-stu-id="28461-120">Automatically post Finance bank transactions if they appear on a bank statement but don't appear in the Finance app.</span></span>
    -   <span data-ttu-id="28461-121">Bir mutabakat tablosu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="28461-121">Generate a reconciliation statement.</span></span>





