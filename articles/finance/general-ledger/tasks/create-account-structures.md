---
title: Hesap yapıları oluşturma
description: Bu yordam, hesap yapısı oluşturmayı açıklar.
author: aprilolson
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 04c22fce0c6b510e7e02036d9bf84f33d3c71e8c
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2022
ms.locfileid: "8716845"
---
# <a name="create-account-structures"></a>Hesap yapıları oluşturma

[!include [banner](../../includes/banner.md)]

Bu yordam, hesap yapısı oluşturmayı açıklar. Adımlarda demo veri şirketi USMF kullanılmaktadır.

1. **Gezinti bölmesi > Modüller > Genel muhasebe > Hesap planı > Yapılar > Hesap yapılarını yapılandır**'a gidin.
2. **Eylem bölmesi**'nde, bırakma iletişim kutusunu açmak için **Yeni**'yi seçin.
3. **Hesap yapısı** alanında, hesap yapısının amacını açıklayan bir ad girin.
4. **Açıklama** alanında, hesap yapısının amacını belirten bir açıklama girin.
5. **Oluştur**'a tıklayın.
6. **Segmentler ve izin verilen değerler**'de **Segment ekle**'ye tıklayın.
7. Boyutlar listesinde, hesap yapısına eklenecek boyutu seçin.
8. Listenin sonunda **Segment ekle**'ye tıklayın.
9. 6-9 arası adımları gerektiği şekilde yineleyin.
10. **İzin verilen değerler** bölümünde izin verilen değerlerini düzenlemek istediğiniz segmenti seçin.
    Örneğin, **Ana Hesap** alanına tıklayın.  
11. **İşleç** alanında, arasında ve içerir gibi bir seçenek belirleyin.
12. **Değer** alanına bir değer yazın. Örneğin, 600000.  
13. **Aracılığıyla** alanında bir değer girin. Örneğin, 699999.  
14. **İzin verilen değer ayrıntıları** bölümünde, **Uygula**'ya tıklayın.
15. 10-15 arası adımları gerektiği şekilde yineleyin.  
16. **İzin verilen değer ayrıntıları** bölümünde, **Yeni ölçüt ekle**'ye tıklayın.
17. İşleç alanında, arasında ve içerir gibi bir seçenek belirleyin.
18. **Değer** alanına bir değer yazın. Örneğin, 033.  
19. **Aracılığıyla** alanında bir değer girin. Örneğin, 034.  
20. **Uygula**'ya tıklayın.
21. Kılavuzda, izin verilen değerleri düzenlemek istediğiniz segmenti seçin. Örneğin, Maliyet Merkezi.  
22. **Maliyet Merkezi** alanında bir değer girin. Örneğin, 007..021.  
23. **Segmentler ve izin verilen değerler**'de **Ekle**'ye tıklayın.
24. **Ana Hesap** alanında bir değer girin. Örneğin, 600000..699999  
25. Kılavuzda, izin verilen değerleri düzenlemek istediğiniz segmenti seçin. Örneğin, Departman.  
26. Departman alanında bir değer girin. Örneğin, 032.  
27. Maliyet Merkezi alanında bir değer girin. Örneğin, 086.  
28. **Eylem Bölmesinde**,  **Doğrula** öğesine tıklayın.
29. **Eylem Bölmesinde** **Etkinleştir** öğesine tıklayın.
30. **Etkinleştir**'e tıklayın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
