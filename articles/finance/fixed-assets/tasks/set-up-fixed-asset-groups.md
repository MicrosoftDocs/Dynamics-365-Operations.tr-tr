---
title: Sabit kıymet gruplarını ayarla
description: Bu konu yeni bir sabit kıymet grubunun nasıl oluşturulacağı açıklar.
author: saraschi2
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetGroup, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 246502f66c0cfcd4b4ed3c4b9f2ae616e71a1c50
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186889"
---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="0ed3d-103">Sabit kıymet gruplarını ayarla</span><span class="sxs-lookup"><span data-stu-id="0ed3d-103">Set up fixed asset groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0ed3d-104">Bu konu yeni bir sabit kıymet grubunun nasıl oluşturulacağı açıklar.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-104">This topic explains how to create a new fixed asset group.</span></span> <span data-ttu-id="0ed3d-105">Kılavuzda Muhasebeci rolü ve USMF adlı tüzel kişilik için demo verileri kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="0ed3d-106">Gezinti bölmesinde **Modüller > Sabit kıymetler > Kurulum > Sabit kıymet grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-106">In the navigation pane, go to **Modules > Fixed assets > Setup > Fixed asset groups**.</span></span>
2. <span data-ttu-id="0ed3d-107">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-107">Select **New**.</span></span>
3. <span data-ttu-id="0ed3d-108">**Sabit kıymet grubu** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-108">In the **Fixed asset group** field, type a value.</span></span>
4. <span data-ttu-id="0ed3d-109">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-109">In the **Name** field, type a value.</span></span> <span data-ttu-id="0ed3d-110">**Sabit kıymet** grubundaki Sabit kıymetleri otomatik numaralandır ve Numara serisi kodu değerleri, Sabit kıymet parametrelerindeki ayarların üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-110">Autonumber fixed assets and Number sequence code on the **Fixed asset** group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="0ed3d-111">Bu sabit kıymet grubundaki kıymetlerin diğer gruplardan farklı numaralandırması olacaksa, numaralandırmayı burada değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="0ed3d-112">**Defterler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-112">Select **Books**.</span></span>
6. <span data-ttu-id="0ed3d-113">**Defter** alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-113">In the **Book** field, enter or select a value.</span></span> <span data-ttu-id="0ed3d-114">**Amortismanı hesapla** alanı **Evet** olarak ayarlanırsa kıymet defteri amortisman tekliflerine dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-114">The **Calculate depreciation** field is set to **Yes**, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="0ed3d-115">**Amortismanı hesapla** ayarı **Hayır** yapılırsa, kıymete otomatik olarak amortisman uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-115">If **Calculate depreciation** is set to **No**, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="0ed3d-116">Kıymetin Servis ömrünü yıl cinsinden ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-116">Set the Service life of the asset, in years.</span></span> <span data-ttu-id="0ed3d-117">**Amortisman dönemleri** alanı değerinin Servis ömrü ayarlandıktan sonra hesaplandığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-117">Note that the **Depreciation periods** field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="0ed3d-118">**Amortisman yöntemi** alanında bir seçenek belirtin.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-118">In the **Depreciation convention** field, select an option.</span></span>
9. <span data-ttu-id="0ed3d-119">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-119">Close the page.</span></span>

