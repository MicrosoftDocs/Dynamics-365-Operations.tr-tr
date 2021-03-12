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
ms.openlocfilehash: 4eead36e1274194b151b230767a4d6385173b12f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994852"
---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="8b327-103">Sabit kıymet gruplarını ayarla</span><span class="sxs-lookup"><span data-stu-id="8b327-103">Set up fixed asset groups</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8b327-104">Bu konu yeni bir sabit kıymet grubunun nasıl oluşturulacağı açıklar.</span><span class="sxs-lookup"><span data-stu-id="8b327-104">This topic explains how to create a new fixed asset group.</span></span> <span data-ttu-id="8b327-105">Kılavuzda Muhasebeci rolü ve USMF adlı tüzel kişilik için demo verileri kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="8b327-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="8b327-106">Gezinti bölmesinde **Modüller > Sabit kıymetler > Kurulum > Sabit kıymet grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="8b327-106">In the navigation pane, go to **Modules > Fixed assets > Setup > Fixed asset groups**.</span></span>
2. <span data-ttu-id="8b327-107">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8b327-107">Select **New**.</span></span>
3. <span data-ttu-id="8b327-108">**Sabit kıymet grubu** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="8b327-108">In the **Fixed asset group** field, type a value.</span></span>
4. <span data-ttu-id="8b327-109">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="8b327-109">In the **Name** field, type a value.</span></span> <span data-ttu-id="8b327-110">**Sabit kıymet** grubundaki Sabit kıymetleri otomatik numaralandır ve Numara serisi kodu değerleri, Sabit kıymet parametrelerindeki ayarların üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="8b327-110">Autonumber fixed assets and Number sequence code on the **Fixed asset** group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="8b327-111">Bu sabit kıymet grubundaki kıymetlerin diğer gruplardan farklı numaralandırması olacaksa, numaralandırmayı burada değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8b327-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="8b327-112">**Defterler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8b327-112">Select **Books**.</span></span>
6. <span data-ttu-id="8b327-113">**Defter** alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="8b327-113">In the **Book** field, enter or select a value.</span></span> <span data-ttu-id="8b327-114">**Amortismanı hesapla** alanı **Evet** olarak ayarlanırsa kıymet defteri amortisman tekliflerine dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="8b327-114">The **Calculate depreciation** field is set to **Yes**, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="8b327-115">**Amortismanı hesapla** ayarı **Hayır** yapılırsa, kıymete otomatik olarak amortisman uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="8b327-115">If **Calculate depreciation** is set to **No**, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="8b327-116">Kıymetin Servis ömrünü yıl cinsinden ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="8b327-116">Set the Service life of the asset, in years.</span></span> <span data-ttu-id="8b327-117">**Amortisman dönemleri** alanı değerinin Servis ömrü ayarlandıktan sonra hesaplandığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="8b327-117">Note that the **Depreciation periods** field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="8b327-118">**Amortisman yöntemi** alanında bir seçenek belirtin.</span><span class="sxs-lookup"><span data-stu-id="8b327-118">In the **Depreciation convention** field, select an option.</span></span>
9. <span data-ttu-id="8b327-119">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8b327-119">Close the page.</span></span>

