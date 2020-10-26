---
title: Hub ilave masraflarını ve ana ilaveleri ayarlama
description: Bu yordam bir hub için ana ilavenin nasıl oluşturulacağını ve onu hub ilave masrafı olarak kullanmayı gösterir.
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSHubAccessorial,TMSAccessorialMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 82cd18c7109b5a0287ee2eb8b7adf901c97ec7c7
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982636"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a><span data-ttu-id="e3eed-103">Hub ilave masraflarını ve ana ilaveleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="e3eed-103">Set up hub accessorial charges and accessorial masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e3eed-104">Bu yordam bir hub için ana ilavenin nasıl oluşturulacağını ve onu hub ilave masrafı olarak kullanmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="e3eed-104">This procedure shows how to create an accessorial master for a hub and use that master to create a hub accessorial charge.</span></span> <span data-ttu-id="e3eed-105">Bu yordam USMF veri kümesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="e3eed-105">The procedure uses the USMF dataset.</span></span> <span data-ttu-id="e3eed-106">Bu ayar genellikle taşımacılık düzenleyicisi tarafından yapılır.</span><span class="sxs-lookup"><span data-stu-id="e3eed-106">This set up will typically be done by a transportation coordinator.</span></span>


## <a name="set-up-a-hub-master"></a><span data-ttu-id="e3eed-107">Bir ana hub ayarla</span><span class="sxs-lookup"><span data-stu-id="e3eed-107">Set up a hub master</span></span>
1. <span data-ttu-id="e3eed-108">Taşıma yönetimi > Kurulum > Derecelendirme > Ana ilaveler öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="e3eed-108">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="e3eed-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e3eed-109">Click New.</span></span>
3. <span data-ttu-id="e3eed-110">Ana ilaveler alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="e3eed-110">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="e3eed-111">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="e3eed-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="e3eed-112">İlave türü alanında, 'Hub'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e3eed-112">In the Accessorial type field, select 'Hub'.</span></span>
6. <span data-ttu-id="e3eed-113">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e3eed-113">Click Save.</span></span>
7. <span data-ttu-id="e3eed-114">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e3eed-114">Close the page.</span></span>

## <a name="set-up-a-hub-accessorial-charge"></a><span data-ttu-id="e3eed-115">Hub ilave masrafı ayarla</span><span class="sxs-lookup"><span data-stu-id="e3eed-115">Set up a hub accessorial charge</span></span>
1. <span data-ttu-id="e3eed-116">Taşıma yönetimi > Kurulum > Derecelendirme > Hub ilave masrafları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="e3eed-116">Go to Transportation management > Setup > Rating > Hub accessorial charges.</span></span>
2. <span data-ttu-id="e3eed-117">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e3eed-117">Click New.</span></span>
3. <span data-ttu-id="e3eed-118">Hub ilave numarası alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="e3eed-118">In the Hub accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="e3eed-119">Hub alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e3eed-119">In the Hub field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="e3eed-120">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="e3eed-120">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="e3eed-121">Hub konumu alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="e3eed-121">In the Hub position field, select an option.</span></span>
    * <span data-ttu-id="e3eed-122">Gideri malzeme çekme ya da teslim olarak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e3eed-122">You can either create the charge as a pickup or drop-off.</span></span> <span data-ttu-id="e3eed-123">Seçiminize bağlı olarak, rotanız üzerindeki karşılık gelen ulaştırma kesimine gider olarak uygulanacaktır.</span><span class="sxs-lookup"><span data-stu-id="e3eed-123">Depending on your selection the charge will be applied to the corresponding transportation segment on your route.</span></span>  
7. <span data-ttu-id="e3eed-124">Ana ilaveler alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e3eed-124">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="e3eed-125">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e3eed-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e3eed-126">Yeni oluşturduğunuz kalıbı seçin.</span><span class="sxs-lookup"><span data-stu-id="e3eed-126">Select the master you just created.</span></span>  
9. <span data-ttu-id="e3eed-127">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e3eed-127">Click Save.</span></span>
10. <span data-ttu-id="e3eed-128">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e3eed-128">Close the page.</span></span>

