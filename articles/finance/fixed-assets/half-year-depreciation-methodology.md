---
title: Yarı yıl amortisman yöntemi
description: Bu makale, bir kıymetin ilk ve son yılı sırasında altı aylık amortismanı hesaplayan yarı yıl kuralını kullanarak amortismanı hesaplamak üzere sabit kıymetlerde kullanılan yöntemi açıklamaktadır.
author: moaamer
ms.date: 08/17/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-08-17
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: fac20f7a31eca7922ed079f9554437f28448620d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879609"
---
# <a name="half-year-depreciation-convention-methodology"></a>Yarı yıl amortisman yöntemi

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu makale, yarı yıl kuralını kullanarak amortismanı hesaplamak üzere sabit kıymetlerde kullanılan yöntemi açıklamaktadır. Yarım yıl kuralı, bir kıymetin ilk ve son yılındaki hizmeti için altı aylık amortismanı hesaplar. Amortisman kuralları hakkında daha fazla bilgi için bkz. [Amortisman yöntemleri ve kuralları](Fixed-asset-depreciation-conventions.md). 

Altı aylık amortisman kuralını kullandığınızda, sistem kıymetin satın alındığı yılı veya servise verildiği yılı kullanır, sonra bu yıldan beş yıllık amortismanı hesaplar ve sonra altı ay ekler. Bu süreci görmek için, 50.000'lik bir fiyata alınmış ve 2020 Nisan ayında servise sokulmuş bir varlık düşünün. Ayrıca, kıymetin beş yıllık servis ömrüne sahip olduğunu varsayın.

İlk servis yılı Aralık 2020'de sona erer ve bu da kıymetin beş yıllık servis ömrünün bitişinin Aralık 2024 olacağı anlamına gelir. Yarım yıl amortisman kuralı, kıymetin ömrüne altı ay ekler, yani servis ömrü 2025 Haziran 'da sona erer. 

> Yıllık amortisman 50.000/5 = 10.000 ve aylık amortisman 10000/12 = 833,33 <br>
> İlk yıl yıpranma 10.000/2 = 5.000 ve sonraki aylık amortisman 5.000/9 = 555,56

   [![Yarım yıl amortisman kuralı için amortisman planı.](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)

Yarım yıl kuralı ile eklenen uzatılmış amortisman dönemleri, amortismanın daha doğru tahsisatını sağlar. Altı aylık kural, amortisman giderlerini daha eşit şekilde temsil eder ve kar ve zarar raporunun bildirilmesinde yararlı olur.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
