--- 
title: "Sabit kıymeti transfer etme"
description: "Bu görev kılavuzu, bir mali boyut kümesinden alınan sabit kıymet defterine ait mali bilgileri yeni bir mali boyut kümesine transfer eder."
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: bb8a5b94d9a0bb510daa2a698524e0c380597991
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---
# <a name="transfer-a-fixed-asset"></a><span data-ttu-id="d827a-103">Sabit kıymeti transfer etme</span><span class="sxs-lookup"><span data-stu-id="d827a-103">Transfer a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d827a-104">Bu görev kılavuzu, bir mali boyut kümesinden alınan sabit kıymet defterine ait mali bilgileri yeni bir mali boyut kümesine transfer eder.</span><span class="sxs-lookup"><span data-stu-id="d827a-104">This task guide will transfer the financial information for a fixed asset book from one financial dimension set to a new financial dimension set.</span></span>  <span data-ttu-id="d827a-105">Kılavuzda Muhasebeci rolü ve USMF adlı tüzel kişilik için demo verileri kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d827a-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="d827a-106">Sabit kıymetler > Sabit kıymetler > Sabit kıymetler menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="d827a-106">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="d827a-107">Listede, transfer edilecek sabit kıymeti bulup seçin.</span><span class="sxs-lookup"><span data-stu-id="d827a-107">In the list, find and select the fixed asset to transfer.</span></span>
3. <span data-ttu-id="d827a-108">Eylem Bölmesinde, Sabit kıymet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d827a-108">On the Action Pane, click Fixed asset.</span></span>
4. <span data-ttu-id="d827a-109">Sabit kıymetleri transfer et'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d827a-109">Click Transfer fixed assets.</span></span>
5. <span data-ttu-id="d827a-110">Transfer tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="d827a-110">In the Transfer date field, enter a date.</span></span>
6. <span data-ttu-id="d827a-111">Transferi açıklayan yorumları girin.</span><span class="sxs-lookup"><span data-stu-id="d827a-111">Enter comments to describe the transfer.</span></span>
    * <span data-ttu-id="d827a-112">Bu liste, sabit kıymet için tüm defterleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="d827a-112">This list shows all books for the fixed asset.</span></span>  
7. <span data-ttu-id="d827a-113">Yeni bir mali boyut kümesine transfer etmek istediğiniz defterleri işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="d827a-113">Mark the books you want to transfer to a new financial dimension set.</span></span>
    * <span data-ttu-id="d827a-114">Bu liste, seçili defter için mevcut mali boyut değerlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="d827a-114">This list shows the existing financial dimension values for the selected book.</span></span>  
    * <span data-ttu-id="d827a-115">Seçili sabit kıymet defteri için güncelleştirmek istediğiniz mali boyutu seçin.</span><span class="sxs-lookup"><span data-stu-id="d827a-115">Select the financial dimension you want to update for the selected fixed asset book.</span></span>  
8. <span data-ttu-id="d827a-116">Mali boyut alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="d827a-116">In the Financial dimension field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="d827a-117">Diğer mali boyut değerlerini Uygun olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d827a-117">Set other financial dimension values as appropriate.</span></span>  
    * <span data-ttu-id="d827a-118">Bir transfer yapıldığında bir değer girilmesine veya boş bırakılmasına bağlı olarak tüm mali boyut değerleri değişir.</span><span class="sxs-lookup"><span data-stu-id="d827a-118">All financial dimension values change when a transfer occurs, whether a value has been entered or left blank.</span></span> <span data-ttu-id="d827a-119">Örneğin, BusinessUnit için bir değer girdiyseniz ve CostCenter ve Department mali boyutlarını boş bıraktığınız zaman.</span><span class="sxs-lookup"><span data-stu-id="d827a-119">For example, if you entered a value for the BusinessUnit and left the CostCenter and Department financial dimensions blank.</span></span> <span data-ttu-id="d827a-120">Hesap yapınız CostCenter ve Department için boş değerlere izin veriyorsa, transfer sonucunda her değer modeli BusinessUnit için yeni değer, CostCenter ve Department için boş değer alır.</span><span class="sxs-lookup"><span data-stu-id="d827a-120">If your account structure allows blank values for CostCenter and Department, the transfer would result in each value model having the new value for BusinessUnit and a blank value for CostCenter and Department.</span></span>  
9. <span data-ttu-id="d827a-121">Güncelleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d827a-121">Click Update.</span></span>
    * <span data-ttu-id="d827a-122">Transfer tamamlamadan önce değişiklikleri önizleme fırsatınız olacaktır.</span><span class="sxs-lookup"><span data-stu-id="d827a-122">You have the opportunity to preview the changes before finalizing the transfer.</span></span>  
    * <span data-ttu-id="d827a-123">Sabit kıymet defterlerini transfer etmeden önce sonuçları gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="d827a-123">Review results before transferring the fixed asset books.</span></span>  
10. <span data-ttu-id="d827a-124">Transfer et seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d827a-124">Click Transfer.</span></span>


