---
title: Ücreti kademeleri ayarlama
description: Ücret kılavuzları, sabit ücret planları için ödeme yapıları tanımlamak ve sağlamak için kullanılır.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompGridView
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f0caebb2dfbff12545610aa6438dccbec84db3f9
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/19/2019
ms.locfileid: "856773"
---
# <a name="set-up-compensation-grids"></a>Ücreti kademeleri ayarlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ücret kılavuzları, sabit ücret planları için ödeme yapıları tanımlamak ve sağlamak için kullanılır. Ücret kılavuzları, birden çok plan arasında paylaşılır veya yeni bir ücret planı oluştururken kopyalanabilir.  Bir ücret kılavuzu oluşturmadan önce Düzeyler ve Referans noktaları ayarlanmalıdır. Bu örnek, Düzeyler ve Referans noktaları için demo verilerini kullanarak yeni bir ücret Derece türü oluşturur. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.


## <a name="set-up-information-about-the-compensation-grid"></a>Ücret kılavuzuyla ilgili bilgileri ayarlama
1. İnsan kaynakları > Ücret > Sabit ücret > Ücret kılavuzları'na gidin.
2. Yeni'ye tıklayın.
3. Kılavuz alanında bir değer girin.
4. Açıklama alanına bir değer girin.
5. Tür alanında, bir seçenek seçin.
6. Referans ayarı alanında bir değer girin veya bir değer seçin.
7. Para birimi alanında bir değer girin veya bir değer seçin.
8. Para birimi alanına bir değer yazın.
9. Yürürlük tarihi alanına bir tarih girin.

## <a name="add-levels-to-the-compensation-structure"></a>Ücret yapısına düzey ekleme
1. Ücret yapısı'nı tıklatın.
2. Listede, seçili satırı işaretleyin.
3. Düzey alanında bir değer girin veya bir değer seçin.
4. Yeni'yi tıklatın.
5. Listede, seçili satırı işaretleyin.
6. Düzey alanında bir değer girin veya bir değer seçin.
7. Yeni'yi tıklatın.
8. Listede, seçili satırı işaretleyin.
9. Düzey alanında bir değer girin veya bir değer seçin.
10. Yeni'yi tıklatın.
11. Listede, seçili satırı işaretleyin.
12. Düzey alanında bir değer girin veya bir değer seçin.
13. Yeni'yi tıklatın.
14. Listede, seçili satırı işaretleyin.
15. Düzey alanında bir değer girin veya bir değer seçin.

## <a name="fill-in-the-compensation-structure-with-values"></a>Ücret yapısını değerlerle doldurma
1. Listede, seçili satırı işaretleyin.
    * Bu noktada, ücret değerleri tablodaki her bir alanda el ile girilebilir ya da Toplu değiştirme işlevi kullanılarak birden fazla alan kolayca doldurabilir ve temel hesaplamalar gerçekleştirilebilir.  
2. Toplu değişiklik seçeneğine tıklayın.
    * Bu kılavuz için, ilk önce birinci düzeyin orta noktasının değeri tablodaki tüm alanlara uygulanır. Bu, ücret matrisi için esas alınacaktır.  
3. Ayarlama türü alanında bir seçenek belirleyin.
4. Ayarlama tutarı alanına bir sayı girin.
5. Listede, tüm satırları işaretleyin veya tüm satırların işaretlerini kaldırın.
6. Kılavuza uygula'ya tıklayın.
    * Ardından, miktarları sonraki her düzeyde belirli bir yüzde veya miktarda artırmak için toplu değiştirme işlevi kullanılır. Bu örnekte, her derecenin kendi orta noktaları arasında %12,5'luk bir fark olacaktır.  
7. Ayarlama türü alanında bir seçenek belirleyin.
8. Ayarlama tutarı alanına bir sayı girin.
9. Listede, istenen kaydı bulun ve seçin.
10. Listede, istenen kaydı bulun ve seçin.
11. Listede, istenen kaydı bulun ve seçin.
12. Listede, istenen kaydı bulun ve seçin.
13. Kılavuza uygula'ya tıklayın.
14. Listede, istenen kaydı bulun ve seçin.
15. Listede, istenen kaydı bulun ve seçin.
16. Listede, istenen kaydı bulun ve seçin.
17. Kılavuza uygula'ya tıklayın.
18. Listede, istenen kaydı bulun ve seçin.
19. Listede, istenen kaydı bulun ve seçin.
20. Kılavuza uygula'ya tıklayın.
21. Listede, istenen kaydı bulun ve seçin.
22. Kılavuza uygula'ya tıklayın.
    * Her düzey için Minimum ve Maksimum referans noktaları ayarlamak üzere toplu değiştirme işlevi kullanılır. Bu örnek %50 fark değeri kullanır, böylece Minimum referans noktası - %20 ve Maksimum referans noktası olarak +%20 olarak ayarlanır.  
23. Ayarlama tutarı alanına bir sayı girin.
24. Referans noktası alanında bir değer girin veya bir değer seçin.
25. Listede, tüm satırları işaretleyin veya tüm satırların işaretlerini kaldırın.
26. Kılavuza uygula'ya tıklayın.
27. Ayarlama tutarı alanına bir sayı girin.
28. Referans noktası alanında bir değer girin veya bir değer seçin.
29. Listede, tüm satırları işaretleyin veya tüm satırların işaretlerini kaldırın.
30. Kılavuza uygula'ya tıklayın.

