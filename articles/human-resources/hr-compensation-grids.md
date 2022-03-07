---
title: Ücreti kademeleri ayarlama
description: Ücret kılavuzları, sabit ücret planları için ödeme yapıları tanımlamak ve sağlamak için kullanılır.
author: twheeloc
ms.date: 01/03/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompGridView, HcmCompensationWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 51b98320eac539e49787d352f32683efadc11f41
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071512"
---
# <a name="set-up-compensation-grids"></a>Ücreti kademeleri ayarlama


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Ücret kılavuzları, sabit ücret planları için ödeme yapıları tanımlamak ve sağlamak için kullanılır. Ücret kılavuzları, birden çok plan arasında paylaşılır veya yeni bir ücret planı oluştururken kopyalanabilir.  Bir ücret kılavuzu oluşturmadan önce Düzeyler ve Referans noktaları ayarlanmalıdır. Bu örnek, Düzeyler ve Referans noktaları için demo verilerini kullanarak yeni bir ücret Derece türü oluşturur. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.


## <a name="set-up-information-about-the-compensation-grid"></a>Ücret kılavuzuyla ilgili bilgileri ayarlama
1. **İnsan kaynakları** > **Ücret** > **Sabit ücret** > **Ücret ızgaraları**'na gidin.
2. **Yeni**'ye tıklayın.
3. **Izgara** alanına bir değer yazın.
4. **Tanım** alanına bir değer girin.
5. **Tür** alanında, bir seçenek belirtin.
6. **Referans** ayarı alanında bir değer girin veya seçin.
7. **Para birimi** alanında bir değer girin veya bir değer seçin.
8. **Yürürlük tarihi** alanına bir tarih girin.

## <a name="add-levels-to-the-compensation-structure"></a>Ücret yapısına düzey ekleme
1. **Ücret yapısı**'na tıklayın.
2. Listede, seçili satırı işaretleyin.
3. **Düzey** alanında bir değer girin veya seçin.
4. **Yeni**'ye tıklayın.
5. Listede, seçili satırı işaretleyin.
6. **Düzey** alanında bir değer girin veya seçin.
7. **Yeni**'ye tıklayın.
8. Listede, seçili satırı işaretleyin.
9. **Düzey** alanında bir değer girin veya seçin.
10. **Yeni**'ye tıklayın.
11. Listede, seçili satırı işaretleyin.
12. **Düzey** alanında bir değer girin veya seçin.
13. **Yeni**'ye tıklayın.
14. Listede, seçili satırı işaretleyin.
15. **Düzey** alanında bir değer girin veya seçin.

## <a name="fill-in-the-compensation-structure-with-values"></a>Ücret yapısını değerlerle doldurma
1. Listede, seçili satırı işaretleyin.
    * Bu noktada, ücret değerleri tablodaki her bir alanda el ile girilebilir ya da Toplu değiştirme işlevi kullanılarak birden fazla alan kolayca doldurabilir ve temel hesaplamalar gerçekleştirilebilir.  
2. **Toplu değişiklik**'e tıklayın.
    * Bu kılavuz için, ilk önce birinci düzeyin orta noktasının değeri tablodaki tüm alanlara uygulanır. Bu, ücret matrisi için esas alınacaktır.  
3. **Ayarlama türü** alanında bir seçenek belirleyin.
4. **Ayarlama tutarı** alanına bir sayı girin.
5. Listede, tüm satırları işaretleyin veya tüm satırların işaretlerini kaldırın.
6. **Kılavuza uygula**'ya tıklayın.
    * Ardından, miktarları sonraki her düzeyde belirli bir yüzde veya miktarda artırmak için toplu değiştirme işlevi kullanılır. Bu örnekte, her derecenin kendi orta noktaları arasında %12,5'luk bir fark olacaktır.  
7. **Ayarlama türü** alanında bir seçenek belirleyin.
8. **Ayarlama tutarı** alanına bir sayı girin.
9. Listede, istenen kaydı bulun ve seçin.
10. **Kılavuza uygula**'ya tıklayın.
    * Her düzey için Minimum ve Maksimum referans noktaları ayarlamak üzere toplu değiştirme işlevi kullanılır. Bu örnek %50 fark değeri kullanır, böylece Minimum referans noktası - %20 ve Maksimum referans noktası olarak +%20 olarak ayarlanır.  
11. **Ayarlama tutarı** alanına bir sayı girin.
12. **Referans noktası** alanında bir değer girin veya seçin.
13. Listede, tüm satırları işaretleyin veya tüm satırların işaretlerini kaldırın.
14. **Kılavuza uygula**'ya tıklayın.
15. **Ayarlama tutarı** alanına bir sayı girin.
16. **Referans noktası** alanında bir değer girin veya seçin.
17. Listede, tüm satırları işaretleyin veya tüm satırların işaretlerini kaldırın.
18. **Kılavuza uygula**'ya tıklayın.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
