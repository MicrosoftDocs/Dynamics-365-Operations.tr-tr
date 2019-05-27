---
title: Günlük girişlerini veya hareketlerini görüntüleme
description: Bu yordam, günlük girişlerini veya hareketlerini aramak için Fiş hareketleri sorgusunun nasıl kullanılacağını gösterir.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm, LedgerTransVoucher, LedgerTransBase, Originaldocuments
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 53e966a4caf6ee8907b05b5fd9c0978187d64f1d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566852"
---
# <a name="view-journal-entries-or-transactions"></a><span data-ttu-id="ce2e2-103">Günlük girişlerini veya hareketlerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="ce2e2-103">View journal entries or transactions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ce2e2-104">Bu yordam, günlük girişlerini veya hareketlerini aramak için Fiş hareketleri sorgusunun nasıl kullanılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce2e2-104">This procedure shows how to use the Voucher transactions inquiry to search for journal entries or transactions.</span></span>

1. <span data-ttu-id="ce2e2-105">General ledger > Inquiries and reports > Voucher transactions (Genel muhasebe > Sorgular ve raporlar > Fiş hareketleri) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="ce2e2-105">Go to General ledger > Inquiries and reports > Voucher transactions.</span></span>
2. <span data-ttu-id="ce2e2-106">Filtre ölçütleri tanımlamak istediğiniz alanı seçin.</span><span class="sxs-lookup"><span data-stu-id="ce2e2-106">Select the field for which you want to define a filter criteria.</span></span>
3. <span data-ttu-id="ce2e2-107">Seçili alan için filtre ölçütlerini girin.</span><span class="sxs-lookup"><span data-stu-id="ce2e2-107">Enter your filter critieria for the selected field.</span></span>
    * <span data-ttu-id="ce2e2-108">Tek bir değeri veya bir aralığı filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce2e2-108">You could filter on a single value or a range.</span></span> <span data-ttu-id="ce2e2-109">Bir aralık tanımlarken doğru sözdiziminin kullanıldığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="ce2e2-109">When defining a range, make sure the correct syntax is used.</span></span> <span data-ttu-id="ce2e2-110">Değerler çift nokta (..) ile ayrılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ce2e2-110">The values should be separated by a double period (..).</span></span>  
4. <span data-ttu-id="ce2e2-111">Filtrelemek için kullanacağınız ek tabloları eklemek için Birleştirir sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce2e2-111">Click the Joins tab to add additional tables from which to filter.</span></span>
5. <span data-ttu-id="ce2e2-112">Ağaçta, "Tablolar\Genel yevmiye defteri girişi" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ce2e2-112">In the tree, select 'Tables\General journal entry'.</span></span>
6. <span data-ttu-id="ce2e2-113">Birleştirme tablosu ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce2e2-113">Click Add table join.</span></span>
7. <span data-ttu-id="ce2e2-114">Ek bir tablo eklememeye karar verdiyseniz İptal'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce2e2-114">Click Cancel if you decide not to add an additional table.</span></span>
8. <span data-ttu-id="ce2e2-115">Aralık sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce2e2-115">Click the Range tab.</span></span>
9. <span data-ttu-id="ce2e2-116">Sorguyu çalıştırmak için Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce2e2-116">Click OK to run the query.</span></span>
10. <span data-ttu-id="ce2e2-117">Hareket matrahı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce2e2-117">Click Transaction origin.</span></span>
    * <span data-ttu-id="ce2e2-118">Fişin seçilen kaydı hakkında ek bilgileri araştırmak için kılavuz hakkında çeşitli düğmeler kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ce2e2-118">Various buttons about the grid can be used to research additional information about the selected record of the voucher.</span></span> <span data-ttu-id="ce2e2-119">Hareketin türüne ve özelliklerine bağlı olarak bazı düğmeler kullanılamayabilir.</span><span class="sxs-lookup"><span data-stu-id="ce2e2-119">Some buttons may not be available, depending on the type of transaction and characteristics of the transaction.</span></span>  
11. <span data-ttu-id="ce2e2-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ce2e2-120">Close the page.</span></span>
12. <span data-ttu-id="ce2e2-121">Orijinal belgeye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce2e2-121">Click Original document.</span></span>
13. <span data-ttu-id="ce2e2-122">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ce2e2-122">Close the page.</span></span>

