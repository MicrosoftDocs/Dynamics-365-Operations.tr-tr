---
title: Birden çok sabit kıymete yönelik amortisman yöntemlerini değiştirme
description: Bu görev, belirli bir sabit kıymetler grubunun amortisman yöntemini güncelleştirir.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9744f8a9abe16955b397f85ba731c4723c20b4ee
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985174"
---
# <a name="change-depreciation-conventions-for-multiple-fixed-assets"></a><span data-ttu-id="0d7c1-103">Birden çok sabit kıymete yönelik amortisman yöntemlerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="0d7c1-103">Change depreciation conventions for multiple fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0d7c1-104">Bu görev, belirli bir sabit kıymetler grubunun amortisman yöntemini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0d7c1-104">This task updates the depreciation convention for a specified fixed asset group.</span></span> <span data-ttu-id="0d7c1-105">Bu görev kılavuzunda USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="0d7c1-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="0d7c1-106">Sabit kıymetler > Dönemsel görevler > Toplu güncelleştirme'ye gidin</span><span class="sxs-lookup"><span data-stu-id="0d7c1-106">Go to Fixed assets > Periodic tasks > Mass update</span></span>
2. <span data-ttu-id="0d7c1-107">Amortisman defteri alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="0d7c1-107">In the Depreciation book field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="0d7c1-108">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0d7c1-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0d7c1-109">Hizmete giriş başlangıcı alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="0d7c1-109">In the Placed in service start field, enter a date.</span></span>
5. <span data-ttu-id="0d7c1-110">Hizmete giriş bitişi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="0d7c1-110">In the Placed in service end field, enter a date.</span></span>
    * <span data-ttu-id="0d7c1-111">Yalnızca, seçili amortisman defterinin bir parçası olan ve bu tarihler arasında hizmete girmiş olan kıymetler güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="0d7c1-111">Only assets that are a part of the select depreciation book and that have been placed in service between these dates will be updated.</span></span>  
6. <span data-ttu-id="0d7c1-112">Geçerli amortisman yöntemi alanında bir seçenek belirtin.</span><span class="sxs-lookup"><span data-stu-id="0d7c1-112">In the Current depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="0d7c1-113">Yalnızca, geçerli amortisman yöntemi olan kıymetler güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="0d7c1-113">Only assets that have the current depreciation convention will be updated.</span></span>  
7. <span data-ttu-id="0d7c1-114">Yeni amortisman yöntemi alanında bir seçenek belirtin.</span><span class="sxs-lookup"><span data-stu-id="0d7c1-114">In the New depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="0d7c1-115">Raporun istediğiniz seçili hedefe yazdırılacağını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="0d7c1-115">Verify the report will print to the desired destination.</span></span>  
8. <span data-ttu-id="0d7c1-116">Eklenecek kayıtlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="0d7c1-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="0d7c1-117">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0d7c1-117">Click Filter.</span></span>
10. <span data-ttu-id="0d7c1-118">Listede Sabit kıymet grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="0d7c1-118">In the list, select the Fixed asset group.</span></span>
11. <span data-ttu-id="0d7c1-119">Ölçütler alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="0d7c1-119">In the Criteria field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="0d7c1-120">İstediğiniz Sabit kıymet grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="0d7c1-120">Select the desired Fixed asset group.</span></span>
13. <span data-ttu-id="0d7c1-121">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0d7c1-121">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="0d7c1-122">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0d7c1-122">Click OK.</span></span>
15. <span data-ttu-id="0d7c1-123">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0d7c1-123">Click OK.</span></span>
    *  <span data-ttu-id="0d7c1-124">İşlemin sonuçları Toplu güncelleştirme raporunda gösterilir.</span><span class="sxs-lookup"><span data-stu-id="0d7c1-124">Results of the process are shown on the Mass update report.</span></span>     

