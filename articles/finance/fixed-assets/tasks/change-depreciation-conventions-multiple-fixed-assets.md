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
ms.openlocfilehash: 2c64e4f7117c4ca70236a02b4d36a88e9f2a9906
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210035"
---
# <a name="change-depreciation-conventions-for-multiple-fixed-assets"></a><span data-ttu-id="ae797-103">Birden çok sabit kıymete yönelik amortisman yöntemlerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="ae797-103">Change depreciation conventions for multiple fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ae797-104">Bu görev, belirli bir sabit kıymetler grubunun amortisman yöntemini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ae797-104">This task updates the depreciation convention for a specified fixed asset group.</span></span> <span data-ttu-id="ae797-105">Bu görev kılavuzunda USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ae797-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="ae797-106">Sabit kıymetler > Dönemsel görevler > Toplu güncelleştirme'ye gidin</span><span class="sxs-lookup"><span data-stu-id="ae797-106">Go to Fixed assets > Periodic tasks > Mass update</span></span>
2. <span data-ttu-id="ae797-107">Amortisman defteri alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="ae797-107">In the Depreciation book field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="ae797-108">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae797-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ae797-109">Hizmete giriş başlangıcı alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ae797-109">In the Placed in service start field, enter a date.</span></span>
5. <span data-ttu-id="ae797-110">Hizmete giriş bitişi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ae797-110">In the Placed in service end field, enter a date.</span></span>
    * <span data-ttu-id="ae797-111">Yalnızca, seçili amortisman defterinin bir parçası olan ve bu tarihler arasında hizmete girmiş olan kıymetler güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ae797-111">Only assets that are a part of the select depreciation book and that have been placed in service between these dates will be updated.</span></span>  
6. <span data-ttu-id="ae797-112">Geçerli amortisman yöntemi alanında bir seçenek belirtin.</span><span class="sxs-lookup"><span data-stu-id="ae797-112">In the Current depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="ae797-113">Yalnızca, geçerli amortisman yöntemi olan kıymetler güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ae797-113">Only assets that have the current depreciation convention will be updated.</span></span>  
7. <span data-ttu-id="ae797-114">Yeni amortisman yöntemi alanında bir seçenek belirtin.</span><span class="sxs-lookup"><span data-stu-id="ae797-114">In the New depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="ae797-115">Raporun istediğiniz seçili hedefe yazdırılacağını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="ae797-115">Verify the report will print to the desired destination.</span></span>  
8. <span data-ttu-id="ae797-116">Eklenecek kayıtlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="ae797-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="ae797-117">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae797-117">Click Filter.</span></span>
10. <span data-ttu-id="ae797-118">Listede Sabit kıymet grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ae797-118">In the list, select the Fixed asset group.</span></span>
11. <span data-ttu-id="ae797-119">Ölçütler alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="ae797-119">In the Criteria field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="ae797-120">İstediğiniz Sabit kıymet grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ae797-120">Select the desired Fixed asset group.</span></span>
13. <span data-ttu-id="ae797-121">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae797-121">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="ae797-122">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae797-122">Click OK.</span></span>
15. <span data-ttu-id="ae797-123">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae797-123">Click OK.</span></span>
    *  <span data-ttu-id="ae797-124">İşlemin sonuçları Toplu güncelleştirme raporunda gösterilir.</span><span class="sxs-lookup"><span data-stu-id="ae797-124">Results of the process are shown on the Mass update report.</span></span>     



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]