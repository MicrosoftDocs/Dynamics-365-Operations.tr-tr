---
title: Belirli ürünler için satıcıları onaylama
description: Bu yordam, belirli ürünler için satıcıları onaylamayı gösterir.
author: mkirknel
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, PdsApprovedVendorList, VendTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 815d968b37cf285544799735fdd3f00f0c7ebffb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838178"
---
# <a name="approve-vendors-for-specific-products"></a>Belirli ürünler için satıcıları onaylama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, belirli ürünler için satıcıları onaylamayı gösterir. Bu, bir ürün satınalma siparişine eklendiğinde hangi satıcıların kullanılabileceğini denetlemenize olanak sağlar. Bu yordamı, demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz. Genellikle bu görev bir Satınalma yöneticisi tarafından gerçekleştirilir.

1. Gezinti bölmesi'nde **Modüller > Ürün bilgileri yönetimi > Ürünler > Serbest bırakılan ürünler**'e gidin.
2. Listede, istenen kaydı bulun ve seçin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. **Satınalma** hızlı sekmesini genişletin. **Satıcı** alanında gösterilen birincil bir satıcı var ise bu satıcıyı aşağıdaki adımlarla onaylı bir satıcı olarak eklemeniz gerekir. Eğer gösterilen varsa, satıcı numarasını not alın.  
5. Eylem Bölmesinde, **Satınalma** öğesine tıklayın.
6. **Kurulum**’a tıklayın.
7. **Ekle** öğesine tıklayın.
8. Satıcı alanına bir değer girin veya buradan bir değer seçin. Onaylanan satıcıyı seçin. En az bir satırın birincil satıcı olması gerekir, eğer ürün kaydında bir tane varsa. Daha önce satıcı numarasını not ettiyseniz, burada seçin.  
9. **Bitiş** alanına bir tarih girin. Bir kaç ay sonraki bir tarihi seçin.  
10. **Ekle** öğesine tıklayın.
11. **Satıcı** alanına bir değer girin veya buradan bir değer seçin.
12. **Bitiş** alanına bir tarih girin. Önceki sona erme tarihinden farklı bir tarihi seçin.  
13. Sayfayı kapatın.
14. Eylem Bölmesinde, **Onaylanan satıcılar** öğesine tıklayın.
15. **Bitiş** alanına bir tarih girin. Bu tarih, belirli bir tarihe kadar olan onaylanan satıcıları görebilmeniz için bir filtre görevi görür.  
16. Sayfayı kapatın.
17. Eylem Bölmesinde, **Yürürlük dönemi** öğesine tıklayın.
18. **Satıcılar tarafından alan süresi** alanına bir tarih girin. Belirli bir tarihten sonra onay durumunu sona erecek satıcıları tanımlamak için bu sayfayı kullanabilirsiniz.  
19. Sayfayı kapatın.
20. **Düzenle**'yi tıklatın.
21. **Onaylanmış satıcı çeki yöntemi** alanında, bir seçeneği işaretleyin. Bu alan, bir satınalma siparişi satırına eklenen bir ürünün, satıcı onaylanmış bir satıcı olmadığında ne olacağını belirleyecek ilkeyi seçmenize olanak verir.  
22. **Kaydet**'e tıklayın.
23. Sayfayı kapatın.
24. Sayfayı kapatın.
25. Gezinti Bölmesi'nde **Modüller > Tedarik ve kaynak atama > Satıcılar > Satıcı/madde ilişkileri > Maddeye göre onaylı satıcı listesi öğesi**'ne gidin. Bu sayfa, tüm ürünler ve onaylı satıcılara genel bir bakış sağlar.  
26. Sayfayı kapatın.
27. Gezinti Bölmesi'nde **Modüller > Tedarik ve kaynak atama > Satıcılar > Tüm satıcılar**'a gidin. Ayrıca bir satıcıdan başlatabilir ve o satıcı hesabı için onaylanan ürünler listesine gidebilirsiniz.  
28. Listede, istenen kaydı bulun ve seçin.
29. Eylem Bölmesinde, **Tedarik** öğesine tıklayın.
30. **Satıcıya göre onaylı satıcı listesi**'ne tıklayın.
31. Sayfayı kapatın.
32. Sayfayı kapatın.

