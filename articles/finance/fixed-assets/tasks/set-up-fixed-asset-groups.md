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
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee3cec5c6abf08c88a61af2ec4bde6a863de2f95
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224657"
---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="09df0-103">Sabit kıymet gruplarını ayarla</span><span class="sxs-lookup"><span data-stu-id="09df0-103">Set up fixed asset groups</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="09df0-104">Bu konu yeni bir sabit kıymet grubunun nasıl oluşturulacağı açıklar.</span><span class="sxs-lookup"><span data-stu-id="09df0-104">This topic explains how to create a new fixed asset group.</span></span> <span data-ttu-id="09df0-105">Kılavuzda Muhasebeci rolü ve USMF adlı tüzel kişilik için demo verileri kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="09df0-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="09df0-106">Gezinti bölmesinde **Modüller > Sabit kıymetler > Kurulum > Sabit kıymet grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="09df0-106">In the navigation pane, go to **Modules > Fixed assets > Setup > Fixed asset groups**.</span></span>
2. <span data-ttu-id="09df0-107">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="09df0-107">Select **New**.</span></span>
3. <span data-ttu-id="09df0-108">**Sabit kıymet grubu** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="09df0-108">In the **Fixed asset group** field, type a value.</span></span>
4. <span data-ttu-id="09df0-109">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="09df0-109">In the **Name** field, type a value.</span></span> <span data-ttu-id="09df0-110">**Sabit kıymet** grubundaki Sabit kıymetleri otomatik numaralandır ve Numara serisi kodu değerleri, Sabit kıymet parametrelerindeki ayarların üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="09df0-110">Autonumber fixed assets and Number sequence code on the **Fixed asset** group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="09df0-111">Bu sabit kıymet grubundaki kıymetlerin diğer gruplardan farklı numaralandırması olacaksa, numaralandırmayı burada değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="09df0-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="09df0-112">**Defterler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="09df0-112">Select **Books**.</span></span>
6. <span data-ttu-id="09df0-113">**Defter** alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="09df0-113">In the **Book** field, enter or select a value.</span></span> <span data-ttu-id="09df0-114">**Amortismanı hesapla** alanı **Evet** olarak ayarlanırsa kıymet defteri amortisman tekliflerine dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="09df0-114">The **Calculate depreciation** field is set to **Yes**, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="09df0-115">**Amortismanı hesapla** ayarı **Hayır** yapılırsa, kıymete otomatik olarak amortisman uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="09df0-115">If **Calculate depreciation** is set to **No**, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="09df0-116">Kıymetin Servis ömrünü yıl cinsinden ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="09df0-116">Set the Service life of the asset, in years.</span></span> <span data-ttu-id="09df0-117">**Amortisman dönemleri** alanı değerinin Servis ömrü ayarlandıktan sonra hesaplandığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="09df0-117">Note that the **Depreciation periods** field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="09df0-118">**Amortisman yöntemi** alanında bir seçenek belirtin.</span><span class="sxs-lookup"><span data-stu-id="09df0-118">In the **Depreciation convention** field, select an option.</span></span>
9. <span data-ttu-id="09df0-119">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="09df0-119">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]