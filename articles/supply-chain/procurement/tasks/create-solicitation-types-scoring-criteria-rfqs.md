---
title: RFQ'lar için talep türleri ve puanlama ölçütleri oluşturma
description: Bu kılavuzda bir talep türünün nasıl oluşturulacağı ve bunun puanlama yöntemi ile nasıl ilişkilendirileceği gösterilir.
author: kamaybac
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2d28cb4bf20ba50aae6b85e835339e2df711c99d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812074"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a>RFQ'lar için talep türleri ve puanlama ölçütleri oluşturma

[!include [banner](../../includes/banner.md)]

Bu kılavuzda bir talep türünün nasıl oluşturulacağı ve bunun puanlama yöntemi ile nasıl ilişkilendirileceği gösterilir. Ayrıca, sonrasında varsayılan puanlama yöntemini ayarlamak üzere talep türünün resmi teklif talebinde (RFQ) nasıl kullanılacağı gösterilir. Bu görevler genellikle satınalma yöneticisi tarafından yerine getirilir. Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz. Başlamadan önce kullanılabilir bir puanlama yöntemi gerekir.


## <a name="create-a-solicitation-type"></a>Bir talep türü oluşturun.
1. Tedarik ve kaynak atama > Ayarlar > Teklif talebi > Talep türü'ne gidin.
2. Yeni'ye tıklayın.
3. İsim alanına bir değer yazın.
4. Açıklama alanına bir değer girin.
5. Puanlama yöntemi alanında, talep türü için kullanmak istediğiniz puanlama yöntemini seçin.
6. Kaydet'e tıklayın.
7. Sayfayı kapatın.

## <a name="use-the-solicitation-type"></a>Talep türünü kullanın
1. Tedarik ve kaynak atama > Teklif talepleri > Tüm teklif talepleri öğesine gidin.
2. Yeni'ye tıklayın.
3. Talep türü alanında yeni oluşturduğunuz talep türünü seçin. 
    *   
4. Tamam'a tıklayın.
5. Puanlama ölçütü'ne tıklayın.
    * Gösterilen puanlama ölçütü, talep türüyle ilişkili puanlama yönteminden olanlardır. Bu sayfadan ölçüt ekleyebilir veya silebilirsiniz. Diğer puanlama yöntemlerinden kopyalayarak yeni ölçüt eklemek de mümkündür.  
6. Ölçütü kopyala'ya tıklayın.
7. Puanlama yöntemi alanına bir değer girin veya buradan bir değer seçin.
8. Tamam'a tıklayın.
9. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]