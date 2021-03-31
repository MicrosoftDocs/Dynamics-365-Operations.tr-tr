---
title: RFQ'lar için puanlama yöntemi oluşturma
description: Bu prosedür, size bir puanlama yönteminin nasıl oluşturulacağını göstermektedir.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQScoringMethod
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba3f0b2be16c02129616025c0ee6258996189c6a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211826"
---
# <a name="create-a-scoring-method-for-rfqs"></a>RFQ'lar için puanlama yöntemi oluşturma

[!include [banner](../../includes/banner.md)]

Bu prosedür, size bir puanlama yönteminin nasıl oluşturulacağını göstermektedir. Puanlama yöntemi resmi teklif talebine (RFQ) yanıt olarak gönderilen tekliflerin karşılaştırılabilmesi için kullanılan bir ölçüt kümesidir. Örneğin, bir satıcıyı geçmiş performansı üzerinden değerlendirmek veya şirketin çevre dostu veya iyi bir işbirlikçi olup olmadığını değerlendirmek isteyebilir veya fiyata göre teklifleri karşılaştırmak isteyebilirsiniz. Bu türe ait RFQ'ler için varsayılan puanlama yöntemi olduğundan talep türüyle bir puanlama yöntemini ilişkilendirebilirsiniz. Bu görevler genellikle satınalma yöneticisi tarafından yerine getirilir. Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.

1. Tedarik ve kaynak atama > Ayarlar > Teklif talebi > Skor yöntemi'ne gidin.
2. Yeni'ye tıklayın.
3. İsim alanına bir değer yazın.
4. Açıklama alanına bir değer girin.
5. Kaydet'e tıklayın.
6. Yeni'ye tıklayın.
7. İsim alanına bir değer yazın.
8. Açıklama alanına bir değer girin.
    * RFQ için bir puanlama yöntemi seçildiğinde bu tanım puanlama yöntemi adı ile birlikte görüntülenir.  
9. Aralık başlangıcı alanına bir sayı girin.
    * Aralık, tedarik profesyonelinin puan olarak girebileceği değerleri sınırlar. RFQ üzerinde birden çok puanlama kriteri varsa girilen puanlar birbirlerine eklenir ve toplam, tekliflerin karşılaştırılmasını sağlayacak şekilde kullanılabilir duruma getirilir.  
10. Aralık bitişi alanına bir sayı girin.
11. Yeni'ye tıklayın.
12. İsim alanına bir değer yazın.
13. Açıklama alanına bir değer girin.
14. Aralık başlangıcı alanına bir sayı girin.
15. Aralık bitişi alanına bir sayı girin.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]