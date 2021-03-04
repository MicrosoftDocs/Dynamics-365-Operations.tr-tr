---
title: Yalın imalat için alt sözleşmeli iş hücresi oluşturma
description: Yalın imalat için taşeron işi modellemek için işi sağlayan satıcı ile ilişkilendirilmiş bir iş hücresi oluşturmanız gerekir.
author: cvocph
manager: tfehr
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2bc1e8551bbebd11cad18d47f9e74a2dedcb908d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439010"
---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a>Yalın imalat için alt sözleşmeli iş hücresi oluşturma

[!include [banner](../../includes/banner.md)]

Yalın imalat için taşeron işi modellemek için işi sağlayan satıcı ile ilişkilendirilmiş bir iş hücresi oluşturmanız gerekir. Taşeron iş hücresi satıcıya Satıcı türündeki bir kaynağın ilişkilendirilmesi aracılığıyla atanmıştır. Bu kaydın USMF demo şirketinde yürütürseniz, satıcı hesap kodu 1002 ve tesis 1'i seçebilirsiniz.


## <a name="create-a-vendor-resource"></a>Bir satıcı kaynağı oluştur
1. Kaynaklar'a gidin.
2. Yeni'ye tıklayın.
3. Kaynak alanına bir değer yazın.
4. Açıklama alanına bir değer girin.
5. Tür alanında 'Satıcı' seçin.
6. Satıcı alanında, aramayı açmak için açılır menü düğmesine tıklayın.

## <a name="create-the-resource-group"></a>Bir kaynak grubu oluştur
1. Kaynak grupları'na gidin.
2. Yeni'ye tıklayın.
3. Kaynak grubu alanına bir değer yazın.
4. Açıklama alanına bir değer girin.
5. Tesis alanında, aramayı açmak için açılır menü düğmesine tıklayın.
    * İş hücrelerinin tahsis edileceği tesisi seçin. Bir tesis teorik olarak bir satıcı tarafından çalıştırılan tek bir tesisi temsil edebilir. Ancak pek çok durumda taşeron kaynaklar, taşeron verilen işlerin siparişinin verildiği tesise tahsis edilir. Taşeron iş hücrelerinin giren ve çıkan ambarlarının aynı tesiste olması gerektiğini unutmayın.  
6. Tesis alanına bir değer yazın.
7. @SysTaskRecorder:_RequestClose
8. İş hücresi onay kutusunu seçin veya temizleyin.
9. Giriş ambarı alanında, aramayı açmak için açılır menü düğmesini tıklatın.
    * Satıcı tarafından yönetilen iş hücresi için malzemeyi hazırlamak amacıyla kullanılan ambar ve konumu seçin. Pek çok durumda ambar ve konum, satıcı başına ayrı bir ambar ve iş hücresi başına bir konum kullanılarak modellenir.  
10. Giriş yerleşimi alanında, aramayı açmak için açılır menü düğmesini tıklatın.
11. Çıkış ambarı alanında, aramayı açmak için açılır menü düğmesini tıklatın.
    * İş hücresinin taşeron işlemleri gönderildiğinde malzemenin gönderildiği ambarı ve konumu tanımlayın. Satıcı kanban işlerini raporluyorsa, ambar ve konum satıcının tesisinde olabilir. Alternatif olarak, ambar konum üretim akışının bir sonraki adımıyla ilişkilendirilmiş alma konumu olabilir.  
12. Çıkış yerleşimi alanında, aramayı açmak için açılır menü düğmesini tıklatın.
13. Takvimler bölümünü genişletin veya daraltın.
14. Ekle öğesini tıklatın.
15. Takvim alanında, açılır menü düğmesine tıklayarak aramayı açın.
    * İş hücresinin çalışma zamanı takvimini kaynak grubu ile ilişkilendirin. Kritik kaynaklar için, iş hücresi veya satıcı tesisinin tam çalışma zamanlarını ve ilişkili kapasitelerini temsil eden belirli takvimler tanımlamanızı öneririz.  
16. Kaynaklar bölümünü genişletin veya daraltın.
17. Ekle öğesini tıklatın.
    * Bir taşeron kaynak grubu, kaynak grubunu satıcı hesabına bağlayan Satıcı türünde bir ilişkilendirilmiş kaynağa sahip olmalıdır.  
18. Kaynak alanında, aramayı açmak için açılır menü düğmesine tıklayın.
    * Önceki alt görevde oluşturmuş olduğunuz satıcı kaynağını seçin veya girin.  
19. İş hücresi kapasitesi bölümünü genişletin veya daraltın.
20. Ekle öğesini tıklatın.
    * Bir iş hücresi tanımlanmış bir kapasiteye sahip olmalıdır. Bu örnekte, standart bir iş günü için 100 parçalık çıkış kapasitesi oluştururuz.  
21. Üretim akışı modeli alanında, aramayı açmak için açılır menü düğmesini tıklatın.
22. Kapasite dönemi alanında bir seçenek belirtin.
23. Ortalama iş çıkarma yeteneği miktarı alanında bir sayı girin.
24. Birim alanında, aramayı açmak için açılır menü düğmesini tıklatın.
25. Birimi ResolveChanges.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]