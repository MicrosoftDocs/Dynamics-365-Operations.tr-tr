---
title: Genel muhasebe hesapları arasındaki hareketleri kapatma
description: Bu yordam, genel muhasebe hesapları arasındaki hareketlerin nasıl kapatılacağını ve bir genel muhasebe kapatmasının nasıl iptal edileceğini gösterir.
author: aprilolson
manager: AnnBe
ms.date: 10/03/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb53e9fee35712343f034389f00f3d4539cc652d
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144686"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="1d9ab-103">Genel muhasebe hesapları arasındaki hareketleri kapatma</span><span class="sxs-lookup"><span data-stu-id="1d9ab-103">Settle transactions between ledger accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1d9ab-104">Bu yordam, genel muhasebe hesapları arasındaki hareketlerin nasıl kapatılacağını ve bir genel muhasebe kapatmasının nasıl iptal edileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1d9ab-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="1d9ab-105">Bu yordam, USMF demo verisi şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="1d9ab-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="1d9ab-106">Genel muhasebe hesapları arasındaki hareketi kapatma</span><span class="sxs-lookup"><span data-stu-id="1d9ab-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="1d9ab-107">Genel muhasebe > Periyodik görevler > Genel muhasebe hesabı kapatmaları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="1d9ab-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="1d9ab-108">Listede, kapatmak istediğiniz hareketi bulun.</span><span class="sxs-lookup"><span data-stu-id="1d9ab-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="1d9ab-109">Tutar bakiyesi sıfırdan büyük olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1d9ab-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="1d9ab-110">İçerir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1d9ab-110">Click Include.</span></span>
4. <span data-ttu-id="1d9ab-111">Kabul et düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1d9ab-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="1d9ab-112">Hesap kapatmayı iptal etme</span><span class="sxs-lookup"><span data-stu-id="1d9ab-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="1d9ab-113">Genel muhasebe > Sorgular ve raporlar > Mizan'a gidin.</span><span class="sxs-lookup"><span data-stu-id="1d9ab-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="1d9ab-114">İletişim kutusunu açmak için Parametreler'i tıklatın</span><span class="sxs-lookup"><span data-stu-id="1d9ab-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="1d9ab-115">Güncelleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1d9ab-115">Click Update.</span></span>
4. <span data-ttu-id="1d9ab-116">Listede, hareketi kapatmak istediğiniz hesabı bulun.</span><span class="sxs-lookup"><span data-stu-id="1d9ab-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="1d9ab-117">Tüm hareketler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1d9ab-117">Click All transactions.</span></span>
6. <span data-ttu-id="1d9ab-118">Listede hareketi kolayca bulmak için bir filtre kullanın.</span><span class="sxs-lookup"><span data-stu-id="1d9ab-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="1d9ab-119">Genel muhasebe hesabı kapatmaları'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1d9ab-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="1d9ab-120">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1d9ab-120">In the list, mark the selected row.</span></span>

