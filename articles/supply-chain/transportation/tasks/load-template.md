---
title: Şablonları yükle
description: Bu konuda, yük şablonlarının nasıl ayarlanacağı ve yük şablonunun yeni bir yük ile nasıl ilişkilendirileceği açıklanmaktadır.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1ea7f5244b483a1b9d6c55227c676a3878a71d83
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646444"
---
# <a name="load-templates"></a><span data-ttu-id="21c7b-103">Şablonları yükle</span><span class="sxs-lookup"><span data-stu-id="21c7b-103">Load templates</span></span>

<span data-ttu-id="21c7b-104">Yeni bir yük oluştururken bir yük şablonu atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="21c7b-104">When you create a new load, you can assign a load template.</span></span> <span data-ttu-id="21c7b-105">Yük şablonu, ekipmanlarla ve yükün yüksekliği, genişliği, derinliği ve hacmi gibi ölçülerle ilgili bilgileri içerir.</span><span class="sxs-lookup"><span data-stu-id="21c7b-105">The load template contains information about equipment, and about measures such as the height, width, depth, and volume of the load.</span></span>

<span data-ttu-id="21c7b-106">Bu konuda, yük şablonlarının nasıl ayarlanacağı ve yük şablonunun yeni bir yük ile nasıl ilişkilendirileceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="21c7b-106">This topic describes how to set up load templates, and how to associate a load template with a new load.</span></span>

## <a name="set-up-a-load-template"></a><span data-ttu-id="21c7b-107">Yük şablonu ayarlama</span><span class="sxs-lookup"><span data-stu-id="21c7b-107">Set up a load template</span></span>

1. <span data-ttu-id="21c7b-108">**Taşıma yönetimi \> Kurulum \>Yük Oluşturma \> Yük şablonu**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="21c7b-108">Go to **Transportation management \> Setup \> Load Building \> Load template**.</span></span>
1. <span data-ttu-id="21c7b-109">Eylem bölmesinde, yeni şablon eklemek için **Yeni**'yi veya var olan bir şablonu düzenlemek için **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="21c7b-109">On the Action Pane, select **New** to add a new template or **Edit** to edit an existing template.</span></span>
1. <span data-ttu-id="21c7b-110">Yeni veya var olan şablon satırında, aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="21c7b-110">In the row for the new or existing template, set the following fields:</span></span>

    - <span data-ttu-id="21c7b-111">**Yük şablonu kodu**: Yük şablonu için benzersiz bir tanımlayıcı (kod) girin.</span><span class="sxs-lookup"><span data-stu-id="21c7b-111">**Load template ID** – Enter a unique identifier (ID) for the load template.</span></span>
    - <span data-ttu-id="21c7b-112">**Ekipman**: Yükü sevk etmek için kullanılması gereken ekipmanı seçin.</span><span class="sxs-lookup"><span data-stu-id="21c7b-112">**Equipment** – Select the equipment that should be used to ship the load.</span></span>
    - <span data-ttu-id="21c7b-113">**Yük yüksekliği**, **Yük genişliği** ve **Yük derinliği**: Yükün boyutlarını girin.</span><span class="sxs-lookup"><span data-stu-id="21c7b-113">**Load height**, **Load width**, and **Load depth** – Enter the dimensions of the load.</span></span>
    - <span data-ttu-id="21c7b-114">**İzin verilen maksimum yük hacmi** ve **İzin verilen maksimum yük ağırlığı**: İzin verilen maksimum yük hacmi ve yük ağırlığını girin.</span><span class="sxs-lookup"><span data-stu-id="21c7b-114">**Max. allowed load volume** and **Max. allowed load weight** – Enter the maximum allowed volume and weight of the load.</span></span>
    - <span data-ttu-id="21c7b-115">**İzin verilen maksimum brüt ağırlık**: Yük için izin verilen maksimum brüt ağırlığını girin.</span><span class="sxs-lookup"><span data-stu-id="21c7b-115">**Maximum allowed gross weight** – Enter the maximum allowed gross weight of the load.</span></span> <span data-ttu-id="21c7b-116">Yükün brüt ağırlığına dara ağırlığı ve yük ağırlığı dahildir.</span><span class="sxs-lookup"><span data-stu-id="21c7b-116">A load's gross weight includes both its tare weight and its loading weight.</span></span>
    - <span data-ttu-id="21c7b-117">**İzin verilen maksimum navlun parçası sayısı**: Yükün içerebileceği maksimum navlun parçası sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="21c7b-117">**Maximum number of freight pieces allowed** – Enter the maximum number of freight pieces that the load can contain.</span></span>
    - <span data-ttu-id="21c7b-118">**Yükü zemine yığ**: Zeminden yüklemeyi kullanmak için bu onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="21c7b-118">**Stack load on floor** – Select this check box to use floor loading.</span></span> <span data-ttu-id="21c7b-119">Bir kat yükleme senaryosunda, kapasiteyi maksimum düzeye çıkartmak için kutular konteyner içinde yerden tavana kadar ve duvardan duvara yığılır.</span><span class="sxs-lookup"><span data-stu-id="21c7b-119">In a floor loading scenario, boxes are stacked floor to ceiling and wall to wall inside the container, to maximize capacity.</span></span>

1. <span data-ttu-id="21c7b-120">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="21c7b-120">On the Action Pane, select **Save**.</span></span>

## <a name="associate-a-load-template-with-a-new-load"></a><span data-ttu-id="21c7b-121">Yeni bir yük ile bir yük şablonunu ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="21c7b-121">Associate a load template with a new load</span></span>

1. <span data-ttu-id="21c7b-122">**Taşıma yönetimi \> Planlama \> Yük planlama çalışma ekranı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="21c7b-122">Go to **Transportation management \> Planning \> Load planning workbench**.</span></span>
1. <span data-ttu-id="21c7b-123">Sayfanın üst kısmından, yük oluşturduğunuz kaynak belgenin türüne göre aşağıdaki sekmelerden birini seçin: **Sevkiyatlar**, **Satış satırları**, **Transfer satırları** veya **Satın alma siparişi satırları**.</span><span class="sxs-lookup"><span data-stu-id="21c7b-123">In the upper part of the page, select one of the following tabs, depending on the type of source document that you're creating a load for: **Shipments**, **Sales lines**, **Transfer lines**, or **Purchase order lines**.</span></span> 
1. <span data-ttu-id="21c7b-124">Yükü planlamak için belirli bir belge seçin.</span><span class="sxs-lookup"><span data-stu-id="21c7b-124">Select the specific document to plan the load for.</span></span>
1. <span data-ttu-id="21c7b-125">Eylem Bölmesinde **Arz ve talep** sekmesindeki **Ekle** grubunda **Yeni yüke**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="21c7b-125">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span>
1. <span data-ttu-id="21c7b-126">**Yük şablonu** iletişim kutusunda **Yük şablonu kodu** alanından, uygulanacak şablonu seçin.</span><span class="sxs-lookup"><span data-stu-id="21c7b-126">In the **Load template** dialog box, in the **Load template ID** field, select the template to apply.</span></span>
1. <span data-ttu-id="21c7b-127">Şablonu uygulamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="21c7b-127">Select **OK** to apply the template.</span></span>
