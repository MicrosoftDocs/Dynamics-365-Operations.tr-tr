---
title: RFQ'lar için puanlama yöntemi oluşturma
description: Bu prosedür, size bir puanlama yönteminin nasıl oluşturulacağını göstermektedir.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQScoringMethod
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 98bcffdf63e20a0a620aa87b44449ce13a5df2fe
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565289"
---
# <a name="create-a-scoring-method-for-rfqs"></a>RFQ'lar için puanlama yöntemi oluşturma

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

