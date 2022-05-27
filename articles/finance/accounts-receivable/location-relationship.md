---
title: Konum ve taraf ilişkisi türlerini ekleme
description: Bu konu, yeni bir konum ve taraf ilişkisi türünün nasıl ekleneceğini açıklamaktadır.
author: ShivamPandey-msft
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 36c2c45c8f078abdc7e0bc40481a544491384245
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711506"
---
# <a name="add-location-and-party-relationship-types"></a>Konum ve taraf ilişkisi türlerini ekleme 

[!include [banner](../includes/banner.md)]

## <a name="add-location-roles"></a>Konum rolleri ekleme

Adres ve iletişim bilgileri için yeni konum rolleri eklemenin iki yolu vardır:

-  **Adres ve iletişim bilgileri amacı** sayfasından ekleyin. Yeni rol **LogisticsLocationRole** tablosuna tür = 0 ile kaydedilir (bu tür, rolün **LogisticsLocationRoleType** enum ve uzantılarında tanımlanmış bir sistem rolü olmadığını gösterir). Kullanıcı adres veya iletişim bilgilerini oluştururken bu rolü kullanabilir.

    ![Adres ve içerik bilgileri amacı.](media/Address-Contact.PNG)

-  Bunu **LogisticsLocationRoleType** enum uzantısına ekleyin ve veritabanı eşitleme işlemiyle doldurulmasını bekleyin.

    1.  **LogisticsLocationRoleType** enum'una bir uzantı oluşturun ve uzantıda yeni rolü ekleyin. 
  
        ![LogisticsLocationRoleType numaralandırmasının uzantısı.](media/Logistics.PNG)

    2. Yeni rol için yeni bir kaynak dosyası oluşturun ve özellikleri için bir değer atayın.
     
     ![Yeni kaynak dosyası.](media/Resource.PNG)
        
    3.  Bir veri popülasyon sınıfı oluşturun ve yeni rolü doldurmak için bir işleyici yöntemi belirtin. 

        ![Veri doldurma.](media/Dirdata.PNG)

    4.  Yeni konum rolü popülasyonunu test etmek için çalıştırılabilir bir sınıf oluşturup Main() işlevinde DirDataPopulation::insertLogisticsLocationRoles() çağırabilirsiniz. Bu işlem tamamlandıktan sonra **LogisticsLocationRole** tablosunda yeni rolün \>0 türüyle doldurulduğunu görmeniz gerekir. Yeni rol **Adres ve iletişim bilgileri amacı** sayfasında görünür.

        ![Yeni Konum Ekleme.](media/InsertNewLocation.PNG)

## <a name="add-party-relationship-types"></a>Taraf ilişkisi türleri ekleme 

Yeni bir ilişki türü eklemek için iki yol vardır:

-   **İlişki türleri** sayfasından ekleyin. Yeni ilişki **DirRelationshipTypeTable** tablosuna systemtype = 0 ile kaydedilir.

    ![İlişki türleri.](media/Relationship.PNG)

-  **DirSystemRelationshipType** enumunun uzantısına ekleyin ve veritabanı eşitleme işlemiyle doldurulmasını bekleyin.

    1.  Bir **DirSystemRelationshipType** enum uzantısı oluşturun ve yeni ilişki türünü ekleyin.

    2. Bu yeni tür için bir başlatıcı oluşturun. Temel kodda **DirRelationshipTypeChildInitialize** gibi çeşitli örnekler bulabilirsiniz. Bu "Child" taraf ilişkisi türü için bir başlatıcı sınıfıdır. Bu kodu kopyalayıp yapıştırarak ve ardından vurgulanan alanları güncelleştirerek başlatıcınızla çalışmaya başlayabilirsiniz.
    
    ![DirRelationshipChild başlatıcı.](media/DirRelationship.PNG)

    3.  Yeni ilişki türü popülasyonunu test etmek için çalıştırılabilir bir sınıf oluşturup Main() işlevinde DirDataPopulation::insertDirRelationshipTypes() çağırabilirsiniz. Yeni ilişki türünü **DirRelationshipTypeTable** tablosunda göreceksiniz ve bu yeni ilişki türü **İlişki türleri** sayfasında yer alacaktır.

        ![Çalıştırılabilir sınıf.](media/Runnable.PNG)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
