---
title: Günlük girişlerini veya hareketlerini görüntüleme
description: Bu yordam, günlük girişlerini veya hareketlerini aramak için Fiş hareketleri sorgusunun nasıl kullanılacağını gösterir.
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm, LedgerTransVoucher, LedgerTransBase, Originaldocuments
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8c72ea9b7b706e1dbd8e4261534f098589535886
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185923"
---
# <a name="view-journal-entries-or-transactions"></a><span data-ttu-id="62f81-103">Günlük girişlerini veya hareketlerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="62f81-103">View journal entries or transactions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="62f81-104">Bu yordam, günlük girişlerini veya hareketlerini aramak için Fiş hareketleri sorgusunun nasıl kullanılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="62f81-104">This procedure shows how to use the Voucher transactions inquiry to search for journal entries or transactions.</span></span>

1. <span data-ttu-id="62f81-105">**Gezinti bölmesi > Modüller > Genel muhasebe > Sorgular ve raporlar > Fiş hareketleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="62f81-105">Go to **Navigation pane > Modules > General ledger > Inquiries and reports > Voucher transactions**.</span></span>
2. <span data-ttu-id="62f81-106">Filtre ölçütleri tanımlamak istediğiniz alanı seçin.</span><span class="sxs-lookup"><span data-stu-id="62f81-106">Select the field for which you want to define a filter criteria.</span></span>
3. <span data-ttu-id="62f81-107">Seçili alan için filtre ölçütlerini girin.</span><span class="sxs-lookup"><span data-stu-id="62f81-107">Enter your filter critieria for the selected field.</span></span> <span data-ttu-id="62f81-108">Tek bir değeri veya bir aralığı filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="62f81-108">You could filter on a single value or a range.</span></span> <span data-ttu-id="62f81-109">Bir aralık tanımlarken doğru sözdiziminin kullanıldığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="62f81-109">When defining a range, make sure the correct syntax is used.</span></span> <span data-ttu-id="62f81-110">Değerler çift nokta (..) ile ayrılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="62f81-110">The values should be separated by a double period (..).</span></span>  
4. <span data-ttu-id="62f81-111">Filtrelemek için kullanacağınız ek tabloları eklemek için **Birleştirir** sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="62f81-111">Click the **Joins** tab to add additional tables from which to filter.</span></span>
5. <span data-ttu-id="62f81-112">Ağaçta, **Tablolar/Genel günlük girişi** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="62f81-112">In the tree, select **Tables/General journal entry**.</span></span>
6. <span data-ttu-id="62f81-113">**Birleştirme tablosu ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="62f81-113">Click **Add table join**.</span></span>
7. <span data-ttu-id="62f81-114">Ek bir tablo eklememeye karar verdiyseniz **İptal**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="62f81-114">Click **Cancel** if you decide not to add an additional table.</span></span>
8. <span data-ttu-id="62f81-115">**Aralık** sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="62f81-115">Click the **Range** tab.</span></span>
9. <span data-ttu-id="62f81-116">Sorguyu çalıştırmak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="62f81-116">Click **OK** to run the query.</span></span>
10. <span data-ttu-id="62f81-117">Eylem bölmesinde,  **Hareket kaynağı** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="62f81-117">On the Action pane, click **Transaction origin**.</span></span> <span data-ttu-id="62f81-118">Fişin seçilen kaydı hakkında ek bilgileri araştırmak için kılavuz hakkında çeşitli düğmeler kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="62f81-118">Various buttons about the grid can be used to research additional information about the selected record of the voucher.</span></span> <span data-ttu-id="62f81-119">Hareketin türüne ve özelliklerine bağlı olarak bazı düğmeler kullanılamayabilir.</span><span class="sxs-lookup"><span data-stu-id="62f81-119">Some buttons may not be available, depending on the type of transaction and characteristics of the transaction.</span></span>
11. <span data-ttu-id="62f81-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="62f81-120">Close the page.</span></span>
12. <span data-ttu-id="62f81-121">Eylem bölmesinde, **Orijinal belge** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="62f81-121">On the Action pane, Click **Original document**.</span></span>
13. <span data-ttu-id="62f81-122">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="62f81-122">Close the page.</span></span>

