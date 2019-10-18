---
title: Sağdan sola doğru okunan dillerde mali boyutlar ve ana hesaplar
description: Bu konu, sağdan sola doğru okunan bir dil kullandığınızda ve finansal boyutlar ve ana hesaplar ayarlamanız gerektiğinde değerlendirmeniz gereken bazı uygulama kararlarını açıklar.
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 36e0af4f1b4fa0013490a2acc2bfcac0de05f5dd
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185348"
---
# <a name="financial-dimensions-and-main-accounts-in-right-to-left-languages"></a><span data-ttu-id="84440-103">Sağdan sola doğru okunan dillerde mali boyutlar ve ana hesaplar</span><span class="sxs-lookup"><span data-stu-id="84440-103">Financial dimensions and main accounts in right-to-left languages</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="84440-104">Bu konu, sağdan sola doğru okunan bir dil kullandığınızda ve finansal boyutlar ve ana hesaplar ayarlamanız gerektiğinde değerlendirmeniz gereken bazı uygulama kararlarını açıklar.</span><span class="sxs-lookup"><span data-stu-id="84440-104">This topic describes some of the implementation decisions that you should consider when you use a right-to-left language, and you must set up financial dimensions and main accounts.</span></span>

<span data-ttu-id="84440-105">Mali boyutları ve ana hesaplar bir uygulama için planlama aşamasının anahtar bileşenleridir.</span><span class="sxs-lookup"><span data-stu-id="84440-105">Financial dimensions and main accounts are key components of the planning phase for an implementation.</span></span> <span data-ttu-id="84440-106">Mali boyutlar ve ana hesaplar sistemde oluşturulduktan sonra **Hesap yapıları yapılandır**, **Gelişmiş kural yapıları** ve **Uygulamaları tümleştirmek için mali boyut yapılandırması** sayfalarında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="84440-106">After financial dimensions and main accounts are created in the system, they are used on the **Configure account structures**, **Advanced rule structures**, and **Financial dimension configuration for integrating applications** pages.</span></span> <span data-ttu-id="84440-107">Bu sayfalarda tanımlanan sıra, sistemde veri girişi ve tüketim için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="84440-107">The order that is defined on those pages is used in the system for data entry and consumption.</span></span> <span data-ttu-id="84440-108">Sistemdeki bazı yerlerde mali boyutlar ve ana hesaplar ayrı alanlarda görünür.</span><span class="sxs-lookup"><span data-stu-id="84440-108">In some places in the system, the financial dimensions and main accounts appear in separate fields.</span></span> <span data-ttu-id="84440-109">Ancak, günlükler gibi diğer yerlerde mali boyutlar ve ana hesaplar tek bir dize olarak görünür.</span><span class="sxs-lookup"><span data-stu-id="84440-109">However, in other places, such as journals, the financial dimensions and main accounts appear as a single string.</span></span>

### <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a><span data-ttu-id="84440-110">Sağdan sola doğru okunan bir sistemde mali boyutları ve ana hesapları ayarlamanın en iyi yöntemleri</span><span class="sxs-lookup"><span data-stu-id="84440-110">Best practices for setting up financial dimensions and main accounts in a right-to-left system</span></span>

-   <span data-ttu-id="84440-111">Hesap planları için ayraç seçtiğinizde çift ayraç seçeneklerinden birini belirleyin: çift tire (--), çift çubuk (||) veya çift nokta (..) veya çift alt çizgi (\_\_).</span><span class="sxs-lookup"><span data-stu-id="84440-111">When you select the delimiter for charts of accounts, select one of the double delimiter options: double hyphen (--), double bar (||) or double period (..), or double underscore (\_\_).</span></span>
-   <span data-ttu-id="84440-112">Mali boyut ve ana hesap değerleri oluşturduğunuzda yalnızca sayıları ve sağdan sola dil karakterlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="84440-112">When you create financial dimension and main account values, use only numbers and right-to-left language characters.</span></span>
-   <span data-ttu-id="84440-113">Seçili hesap planı ayracını mali boyut ve ana hesap değerlerinde kullanmaktan kaçının.</span><span class="sxs-lookup"><span data-stu-id="84440-113">Avoid using the selected chart of accounts delimiter in financial dimension and main account values.</span></span>

<span data-ttu-id="84440-114">Bu en iyi yöntemleri izleyerek sistemde kullanıcı tanımlı sıranın tutarlı gösterimini garanti altına almaya yardımcı olursunuz.</span><span class="sxs-lookup"><span data-stu-id="84440-114">By following these best practices, you help guarantee consistent representation of the user defined-order throughout the system.</span></span>



