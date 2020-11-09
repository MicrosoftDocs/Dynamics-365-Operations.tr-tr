---
title: Sabit kıymet oluşturma
description: Bu konu, sabit kıymet listesi sayfasından yeni bir sabit kıymet kaydının nasıl oluşturulacağını açıklamaktadır.
author: saraschi2
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2b7d65a047251fa036242fb456725bc8cba957b9
ms.sourcegitcommit: 51e626675b0130fa32a84ce2d9119b68ea928018
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4000255"
---
# <a name="create-a-fixed-asset"></a><span data-ttu-id="0c2bf-103">Sabit kıymet oluşturma</span><span class="sxs-lookup"><span data-stu-id="0c2bf-103">Create a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0c2bf-104">Bu konu, **sabit kıymet** listesi sayfasından yeni bir sabit kıymet kaydının nasıl oluşturulacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="0c2bf-104">This topic explains how to create a new fixed asset record from the **Fixed asset** list page.</span></span>

<span data-ttu-id="0c2bf-105">Sistem sabit kıymet grubuna atanan numara serisine göre kıymet numarasını atar.</span><span class="sxs-lookup"><span data-stu-id="0c2bf-105">The system assigns the asset number, based on the number sequence that is assigned to the fixed asset group.</span></span> <span data-ttu-id="0c2bf-106">Microsoft Excel eklentisi aracılığıyla kıymetleri içe aktarmak için sabit kıymet şablonunu veya başka bir içe aktarma işini kullanırsanız sistem otomatik olarak sabit kıymet kayıtları oluşturur ve kıymet numarasını arttırır.</span><span class="sxs-lookup"><span data-stu-id="0c2bf-106">If you use the fixed asset template to import assets via the Microsoft Excel add-in, or if you use another import job, the system automatically creates fixed asset records and increments the asset number.</span></span>

<span data-ttu-id="0c2bf-107">Bir kıymet kaydını el ile oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="0c2bf-107">To manually create an asset record, follow these steps.</span></span>

1. <span data-ttu-id="0c2bf-108">**Gezinti bölmesi \> Modüller \> Sabit kıymetler \> Sabit kıymetler \> Sabit kıymetler** 'e gidin.</span><span class="sxs-lookup"><span data-stu-id="0c2bf-108">Go to **Navigation pane \> Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="0c2bf-109">**Eylem bölmesinde** **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0c2bf-109">On the **Action pane** , select **New**.</span></span>
3. <span data-ttu-id="0c2bf-110">**Sabit kıymet grubu** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="0c2bf-110">In **the Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="0c2bf-111">**Sabit kıymet parametreleri** 'nde ve **Sabit kıymet grubu** 'nda **Sabit kıymetleri otomatik numaralandır** işlevini etkinleştirdiyseniz **Numara** 'ya varsayılan değer atanır.</span><span class="sxs-lookup"><span data-stu-id="0c2bf-111">The **Number** field will default if you have enabled **Autonumber fixed assets functionality** in the **Fixed assets parameters** and the **Fixed asset group**.</span></span> <span data-ttu-id="0c2bf-112">Etkinleştirmediyseniz, sabit kıymeti tanımlayacak benzersiz bir numara girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="0c2bf-112">If not, you must enter a unique number to identify the fixed asset.</span></span>
4. <span data-ttu-id="0c2bf-113">**Ad** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="0c2bf-113">In the **Name** field, enter a value.</span></span> <span data-ttu-id="0c2bf-114">İşletmenizin bu kıymet için gereksinim duyacağı ek bilgileri girin.</span><span class="sxs-lookup"><span data-stu-id="0c2bf-114">Enter the additional information that your business needs for this asset.</span></span>
5. <span data-ttu-id="0c2bf-115">**Eylem Bölmesi** 'nde, **Defterler** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0c2bf-115">On the **Action pane** , select **Books**.</span></span>
6. <span data-ttu-id="0c2bf-116">**Alım tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="0c2bf-116">In the **Acquisition date** field, enter a date.</span></span>
7. <span data-ttu-id="0c2bf-117">**Alım fiyatı** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="0c2bf-117">In the **Acquisition price** field, enter a number.</span></span>

    - <span data-ttu-id="0c2bf-118">İşletmenizin bu defter için gereksinim duyacağı ek bilgileri girin.</span><span class="sxs-lookup"><span data-stu-id="0c2bf-118">Enter the additional information that your business needs for this book.</span></span>
    - <span data-ttu-id="0c2bf-119">İşletmenizin kalan defterler için gereksinim duyacağı ek bilgileri girin.</span><span class="sxs-lookup"><span data-stu-id="0c2bf-119">Enter the additional information that your business needs for the remaining books.</span></span>

8. <span data-ttu-id="0c2bf-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0c2bf-120">Close the page.</span></span>

<span data-ttu-id="0c2bf-121">Ayrıca, Excel eklentisini kullanarak veya **veri yönetimi** çalışma alanından içe aktarma işi çalıştırarak da sabit kıymetleri içe aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0c2bf-121">You can also import fixed assets by using the Excel add-in or by running an import job from the **Data management** workspace.</span></span> <span data-ttu-id="0c2bf-122">İçe aktarmayı çalıştırmadan önce, şablondaki gerekli alanların değerlerini girin.</span><span class="sxs-lookup"><span data-stu-id="0c2bf-122">Before you run the import, enter the values for required fields in the template.</span></span>

<span data-ttu-id="0c2bf-123">Bir sabit kıymet numarasını Excel eklentisinin şablonunda veya veri yönetimi'nde tanımlamadıysanız, sistem her içe aktarılan kıymet için bir sabit kıymet numarası oluşturur ve her birinin numara serisini otomatik olarak arttırır.</span><span class="sxs-lookup"><span data-stu-id="0c2bf-123">If you didn't define the fixed asset number in the template of the Excel add-in, or in Data management, the system creates a fixed asset number for each imported asset and automatically increments the number sequence for each.</span></span> <span data-ttu-id="0c2bf-124">Ancak, varlıkları içe aktarır ve şablonda kıymet numaralarını tanımlarsanız, sistem numara serisini otomatik olarak **artırmaz**.</span><span class="sxs-lookup"><span data-stu-id="0c2bf-124">However, if you import assets and define asset numbers in the template, the system does **not** automatically increment the number sequence.</span></span> <span data-ttu-id="0c2bf-125">Bu durumda bir yöneticinin numara serisini el ile güncelleştirmesi gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="0c2bf-125">In this case, an admin might have to manually update the number sequence.</span></span> <span data-ttu-id="0c2bf-126">Sabit kıymet numarasını Excel eklentisinin şablonunda tanımladıysanız, sistem tanımlanan sabit kıymet numarasını kullanır ve numara serisini arttırır.</span><span class="sxs-lookup"><span data-stu-id="0c2bf-126">If you defined the fixed asset number in the template of the Excel add-in, the system uses the defined fixed asset number and increments the number sequence.</span></span>
