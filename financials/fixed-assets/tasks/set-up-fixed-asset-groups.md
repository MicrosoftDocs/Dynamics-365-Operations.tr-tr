--- 
title: "Sabit kıymet gruplarını ayarla"
description: "Bu prosedürde yeni bir sabit kıymet grubunun nasıl oluşturulacağı gösterilmektedir."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c44ce1219c0fc860d621aa32c8eec7c5d640fa03
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="a7a19-103">Sabit kıymet gruplarını ayarla</span><span class="sxs-lookup"><span data-stu-id="a7a19-103">Set up fixed asset groups</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a7a19-104">Bu prosedürde yeni bir sabit kıymet grubunun nasıl oluşturulacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="a7a19-104">This procedure shows how to create a new fixed asset group.</span></span> <span data-ttu-id="a7a19-105">Kılavuzda Muhasebeci rolü ve USMF adlı tüzel kişilik için demo verileri kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a7a19-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="a7a19-106">Sabit kıymetler > Kurulum > Sabit kıymet grupları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="a7a19-106">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="a7a19-107">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a7a19-107">Click New.</span></span>
3. <span data-ttu-id="a7a19-108">Sabit kıymet grubu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a7a19-108">In the Fixed asset group field, type a value.</span></span>
4. <span data-ttu-id="a7a19-109">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="a7a19-109">In the Name field, type a value.</span></span>
    * <span data-ttu-id="a7a19-110">Sabit kıymet grubundaki Sabit kıymetleri otomatik numaralandır ve Numara serisi kodu değerleri, Sabit kıymet parametrelerindeki ayarların üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="a7a19-110">Autonumber fixed assets and Number sequence code on the Fixed asset group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="a7a19-111">Bu sabit kıymet grubundaki kıymetlerin diğer gruplardan farklı numaralandırması olacaksa, numaralandırmayı burada değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a7a19-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="a7a19-112">Defterler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a7a19-112">Click Books.</span></span>
6. <span data-ttu-id="a7a19-113">Defter alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="a7a19-113">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="a7a19-114">Amortismanı hesapla alanı Evet olarak ayarlanırsa kıymet defteri amortisman tekliflerine dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="a7a19-114">The Calculate depreciation field is set to Yes, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="a7a19-115">Amortismanı hesapla ayarı Hayır yapılırsa, kıymete otomatik olarak amortisman uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="a7a19-115">If Calculate depreciation is set to No, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="a7a19-116">Kıymetin Servis ömrünü yıl cinsinden ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a7a19-116">Set the Service life of the asset, in years.</span></span>
    * <span data-ttu-id="a7a19-117">Amortisman dönemleri alanı değerinin Servis ömrü ayarlandıktan sonra hesaplandığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="a7a19-117">Note that the Depreciation periods field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="a7a19-118">Amortisman yöntemi alanında bir seçenek belirtin.</span><span class="sxs-lookup"><span data-stu-id="a7a19-118">In the Depreciation convention field, select an option.</span></span>
9. <span data-ttu-id="a7a19-119">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a7a19-119">Close the page.</span></span>


