---
title: Konum ve taraf ilişkisi türlerini ekleme
description: Bu konu, yeni bir konum ve taraf ilişkisi türünün nasıl ekleneceğini açıklamaktadır.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 8c359c5c33bed5b5abe7fc0c8e362c3399e9051a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180390"
---
# <a name="add-location-roles-and-party-relationship-types"></a><span data-ttu-id="0da66-103">Konum rolleri ve taraf ilişkisi türleri ekleme</span><span class="sxs-lookup"><span data-stu-id="0da66-103">Add location roles and party relationship types</span></span> 

[!include [banner](../includes/banner.md)]

## <a name="add-location-roles"></a><span data-ttu-id="0da66-104">Konum rolleri ekleme</span><span class="sxs-lookup"><span data-stu-id="0da66-104">Add location roles</span></span>

<span data-ttu-id="0da66-105">Adres ve iletişim bilgileri için yeni konum rolleri eklemenin iki yolu vardır:</span><span class="sxs-lookup"><span data-stu-id="0da66-105">There are two ways to add a new location roles for address and contact information:</span></span>

-  <span data-ttu-id="0da66-106">**Adres ve iletişim bilgileri amacı** sayfasından ekleyin.</span><span class="sxs-lookup"><span data-stu-id="0da66-106">Add it through the **Address and contact information purpose** page.</span></span> <span data-ttu-id="0da66-107">Yeni rol **LogisticsLocationRole** tablosuna tür = 0 ile kaydedilir (bu tür, rolün **LogisticsLocationRoleType** enum ve uzantılarında tanımlanmış bir sistem rolü olmadığını gösterir).</span><span class="sxs-lookup"><span data-stu-id="0da66-107">The new role will be saved to the **LogisticsLocationRole** table with type = 0, which indicates that the role is not a system role defined in the **LogisticsLocationRoleType** enum and its extensions.</span></span> <span data-ttu-id="0da66-108">Kullanıcı adres veya iletişim bilgilerini oluştururken bu rolü kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="0da66-108">A user will be able to use this role when creating address or contact information.</span></span>

    ![Adres ve içerik bilgileri amacı](media/Address-Contact.PNG)

-  <span data-ttu-id="0da66-110">Bunu **LogisticsLocationRoleType** enum uzantısına ekleyin ve veritabanı eşitleme işlemiyle doldurulmasını bekleyin.</span><span class="sxs-lookup"><span data-stu-id="0da66-110">Add it to the **LogisticsLocationRoleType** enum extension, and let it populate through the database sync process.</span></span>

    1.  <span data-ttu-id="0da66-111">**LogisticsLocationRoleType** enum'una bir uzantı oluşturun ve uzantıda yeni rolü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="0da66-111">Create an extension to the **LogisticsLocationRoleType** enum and add the new role in the extension.</span></span> 
  
        ![LogisticsLocationRoleType](media/Logistics.PNG)

    2. <span data-ttu-id="0da66-113">Yeni rol için yeni bir kaynak dosyası oluşturun ve özellikleri için bir değer atayın.</span><span class="sxs-lookup"><span data-stu-id="0da66-113">Create a new resource file for the new role, and then assign a value for its properties.</span></span>
     
     ![Yeni kaynak dosyası](media/Resource.PNG)
        
    3.  <span data-ttu-id="0da66-115">Bir veri popülasyon sınıfı oluşturun ve yeni rolü doldurmak için bir işleyici yöntemi belirtin.</span><span class="sxs-lookup"><span data-stu-id="0da66-115">Create a data population class and provide a handler method to populate the new role.</span></span> 

        ![Veri popülasyonu](media/Dirdata.PNG)

    4.  <span data-ttu-id="0da66-117">Yeni konum rolü popülasyonunu test etmek için çalıştırılabilir bir sınıf oluşturup Main() işlevinde DirDataPopulation::insertLogisticsLocationRoles() çağırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0da66-117">To test populating the new location role, you can create a runnable class, and call DirDataPopulation::insertLogisticsLocationRoles() in Main().</span></span> <span data-ttu-id="0da66-118">Bu işlem tamamlandıktan sonra **LogisticsLocationRole** tablosunda yeni rolün \>0 türüyle doldurulduğunu görmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="0da66-118">After this process is complete, you should see the new role populated in the **LogisticsLocationRole** table with type \> 0.</span></span> <span data-ttu-id="0da66-119">Yeni rol **Adres ve iletişim bilgileri amacı** sayfasında görünür.</span><span class="sxs-lookup"><span data-stu-id="0da66-119">The new role will display on the **Address and contact information purpose** page.</span></span>

        ![Yeni Konum Ekleme](media/InsertNewLocation.PNG)

## <a name="add-party-relationship-types"></a><span data-ttu-id="0da66-121">Taraf ilişkisi türleri ekleme</span><span class="sxs-lookup"><span data-stu-id="0da66-121">Add party relationship types</span></span> 

<span data-ttu-id="0da66-122">Yeni bir ilişki türü eklemek için iki yol vardır:</span><span class="sxs-lookup"><span data-stu-id="0da66-122">There are two ways to add a new relationship type:</span></span>

-   <span data-ttu-id="0da66-123">**İlişki türleri** sayfasından ekleyin.</span><span class="sxs-lookup"><span data-stu-id="0da66-123">Add it through the **Relationship types** page.</span></span> <span data-ttu-id="0da66-124">Yeni ilişki **DirRelationshipTypeTable** tablosuna systemtype = 0 ile kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="0da66-124">The new relationship will be saved to **DirRelationshipTypeTable** with systemtype = 0.</span></span>

    ![İlişki türleri](media/Relationship.PNG)

-  <span data-ttu-id="0da66-126">**DirSystemRelationshipType** enumunun uzantısına ekleyin ve veritabanı eşitleme işlemiyle doldurulmasını bekleyin.</span><span class="sxs-lookup"><span data-stu-id="0da66-126">Add it to the extension of the **DirSystemRelationshipType** enum, and let it populate through database sync process.</span></span>

    1.  <span data-ttu-id="0da66-127">Bir **DirSystemRelationshipType** enum uzantısı oluşturun ve yeni ilişki türünü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="0da66-127">Create an extension to the **DirSystemRelationshipType** enum and add the new relationship type.</span></span>

    2. <span data-ttu-id="0da66-128">Bu yeni tür için bir başlatıcı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0da66-128">Create an initializer for this new type.</span></span> <span data-ttu-id="0da66-129">Temel kodda **DirRelationshipTypeChildInitialize** gibi çeşitli örnekler bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0da66-129">You can find several examples in the core code, one of them is  **DirRelationshipTypeChildInitialize**.</span></span> <span data-ttu-id="0da66-130">Bu "Child" taraf ilişkisi türü için bir başlatıcı sınıfıdır.</span><span class="sxs-lookup"><span data-stu-id="0da66-130">This is an initializer class for party relationship type “Child”.</span></span> <span data-ttu-id="0da66-131">Bu kodu kopyalayıp yapıştırarak ve ardından vurgulanan alanları güncelleştirerek başlatıcınızla çalışmaya başlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0da66-131">You can start with your initializer by copying and pasting this code and then update the highlighted areas.</span></span>
    
    ![DirRelationshipChild](media/DirRelationship.PNG)

    3.  <span data-ttu-id="0da66-133">Yeni ilişki türü popülasyonunu test etmek için çalıştırılabilir bir sınıf oluşturup Main() işlevinde DirDataPopulation::insertDirRelationshipTypes() çağırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0da66-133">To test populating the new relationship type, you can create a runnable class, and call DirDataPopulation::insertDirRelationshipTypes() in Main().</span></span> <span data-ttu-id="0da66-134">Yeni ilişki türünü **DirRelationshipTypeTable** tablosunda göreceksiniz ve bu yeni ilişki türü **İlişki türleri** sayfasında yer alacaktır.</span><span class="sxs-lookup"><span data-stu-id="0da66-134">You should see the new relationship type in the **DirRelationshipTypeTable**, and the new relationship type will be available on the **Relationship types** page.</span></span>

        ![Çalıştırılabilir sınıf](media/Runnable.PNG)
