---
title: Sabit kıymet oluşturma
description: Bu konu, sabit kıymet listesi sayfasından yeni bir sabit kıymet kaydının nasıl oluşturulacağını açıklamaktadır.
author: moaamer
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 770390092342e2db496dde850a75b2f7736bd4c0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817113"
---
# <a name="create-a-fixed-asset"></a><span data-ttu-id="c7509-103">Sabit kıymet oluşturma</span><span class="sxs-lookup"><span data-stu-id="c7509-103">Create a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c7509-104">Bu konu, **sabit kıymet** listesi sayfasından yeni bir sabit kıymet kaydının nasıl oluşturulacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="c7509-104">This topic explains how to create a new fixed asset record from the **Fixed asset** list page.</span></span>

<span data-ttu-id="c7509-105">Sistem sabit kıymet grubuna atanan numara serisine göre kıymet numarasını atar.</span><span class="sxs-lookup"><span data-stu-id="c7509-105">The system assigns the asset number, based on the number sequence that is assigned to the fixed asset group.</span></span> <span data-ttu-id="c7509-106">Microsoft Excel eklentisi aracılığıyla kıymetleri içe aktarmak için sabit kıymet şablonunu veya başka bir içe aktarma işini kullanırsanız sistem otomatik olarak sabit kıymet kayıtları oluşturur ve kıymet numarasını arttırır.</span><span class="sxs-lookup"><span data-stu-id="c7509-106">If you use the fixed asset template to import assets via the Microsoft Excel add-in, or if you use another import job, the system automatically creates fixed asset records and increments the asset number.</span></span>

<span data-ttu-id="c7509-107">Bir kıymet kaydını el ile oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c7509-107">To manually create an asset record, follow these steps.</span></span>

1. <span data-ttu-id="c7509-108">**Gezinti bölmesi \> Modüller \> Sabit kıymetler \> Sabit kıymetler \> Sabit kıymetler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="c7509-108">Go to **Navigation pane \> Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="c7509-109">**Eylem bölmesinde** **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c7509-109">On the **Action pane**, select **New**.</span></span>
3. <span data-ttu-id="c7509-110">**Sabit kıymet grubu** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="c7509-110">In **the Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="c7509-111">**Sabit kıymet parametreleri**'nde ve **Sabit kıymet grubu**'nda **Sabit kıymetleri otomatik numaralandır** işlevini etkinleştirdiyseniz **Numara**'ya varsayılan değer atanır.</span><span class="sxs-lookup"><span data-stu-id="c7509-111">The **Number** field will default if you have enabled **Autonumber fixed assets functionality** in the **Fixed assets parameters** and the **Fixed asset group**.</span></span> <span data-ttu-id="c7509-112">Etkinleştirmediyseniz, sabit kıymeti tanımlayacak benzersiz bir numara girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="c7509-112">If not, you must enter a unique number to identify the fixed asset.</span></span>
4. <span data-ttu-id="c7509-113">**Ad** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="c7509-113">In the **Name** field, enter a value.</span></span> <span data-ttu-id="c7509-114">İşletmenizin bu kıymet için gereksinim duyacağı ek bilgileri girin.</span><span class="sxs-lookup"><span data-stu-id="c7509-114">Enter the additional information that your business needs for this asset.</span></span>
5. <span data-ttu-id="c7509-115">**Eylem Bölmesi**'nde, **Defterler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c7509-115">On the **Action pane**, select **Books**.</span></span>
6. <span data-ttu-id="c7509-116">**Alım tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="c7509-116">In the **Acquisition date** field, enter a date.</span></span>
7. <span data-ttu-id="c7509-117">**Alım fiyatı** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="c7509-117">In the **Acquisition price** field, enter a number.</span></span>

    - <span data-ttu-id="c7509-118">İşletmenizin bu defter için gereksinim duyacağı ek bilgileri girin.</span><span class="sxs-lookup"><span data-stu-id="c7509-118">Enter the additional information that your business needs for this book.</span></span>
    - <span data-ttu-id="c7509-119">İşletmenizin kalan defterler için gereksinim duyacağı ek bilgileri girin.</span><span class="sxs-lookup"><span data-stu-id="c7509-119">Enter the additional information that your business needs for the remaining books.</span></span>

8. <span data-ttu-id="c7509-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c7509-120">Close the page.</span></span>

<span data-ttu-id="c7509-121">Ayrıca, Excel eklentisini kullanarak veya **veri yönetimi** çalışma alanından içe aktarma işi çalıştırarak da sabit kıymetleri içe aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7509-121">You can also import fixed assets by using the Excel add-in or by running an import job from the **Data management** workspace.</span></span> <span data-ttu-id="c7509-122">İçe aktarmayı çalıştırmadan önce, şablondaki gerekli alanların değerlerini girin.</span><span class="sxs-lookup"><span data-stu-id="c7509-122">Before you run the import, enter the values for required fields in the template.</span></span>

<span data-ttu-id="c7509-123">Bir sabit kıymet numarasını Excel eklentisinin şablonunda veya veri yönetimi'nde tanımlamadıysanız, sistem her içe aktarılan kıymet için bir sabit kıymet numarası oluşturur ve her birinin numara serisini otomatik olarak arttırır.</span><span class="sxs-lookup"><span data-stu-id="c7509-123">If you didn't define the fixed asset number in the template of the Excel add-in, or in Data management, the system creates a fixed asset number for each imported asset and automatically increments the number sequence for each.</span></span> <span data-ttu-id="c7509-124">Ancak, varlıkları içe aktarır ve şablonda kıymet numaralarını tanımlarsanız, sistem numara serisini otomatik olarak **artırmaz**.</span><span class="sxs-lookup"><span data-stu-id="c7509-124">However, if you import assets and define asset numbers in the template, the system does **not** automatically increment the number sequence.</span></span> <span data-ttu-id="c7509-125">Bu durumda bir yöneticinin numara serisini el ile güncelleştirmesi gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="c7509-125">In this case, an admin might have to manually update the number sequence.</span></span> <span data-ttu-id="c7509-126">Sabit kıymet numarasını Excel eklentisinin şablonunda tanımladıysanız, sistem tanımlanan sabit kıymet numarasını kullanır ve numara serisini arttırır.</span><span class="sxs-lookup"><span data-stu-id="c7509-126">If you defined the fixed asset number in the template of the Excel add-in, the system uses the defined fixed asset number and increments the number sequence.</span></span>

> [!NOTE]                                                                                                         
> <span data-ttu-id="c7509-127">Amortismanı deftere naklettikten sonra **Hizmete giriş** ve **İlk amortisman göreceği tarih** alanları **Defter** sayfasında kilitli olur.</span><span class="sxs-lookup"><span data-stu-id="c7509-127">After posting the depreciation, the **Placed in service** and **Depreciation run date** fields will be locked on the **Book** page.</span></span> <span data-ttu-id="c7509-128">Ayrıca her iki alan da veri varlığından güncelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="c7509-128">Also, both neither field will be updated from the data entity.</span></span>

> [!WARNING]
> <span data-ttu-id="c7509-129">Hareketler ilişkili deftere nakledilirse veya yeni oluşturulan sabit varlık günlük satırına girilir ancak deftere nakledilmezse sabit varlık kaydı silinmez.</span><span class="sxs-lookup"><span data-stu-id="c7509-129">The fixed asset record won't be deleted if transactions were posted to the associated book, or if the newly created fixed asset is entered on a journal line but not posted.</span></span> 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]