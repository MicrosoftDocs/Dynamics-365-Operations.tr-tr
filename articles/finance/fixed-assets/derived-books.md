---
title: Türetilen defterler
description: Bu makale, türetilmiş defter işlevselliğine genel bir bakış sağlar.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 911bb476a696facfad9dec177261821724d2bfe0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994927"
---
# <a name="derived-books"></a>Türetilen defterler

[!include [banner](../includes/banner.md)]

Bu makale, türetilmiş defter işlevselliğine genel bir bakış sağlar.

Türetilmiş kitapların amacı, düzenli aralıklarla planlanan sabit kıymet kitap hareketlerinin nakledilmesini kolaylaştırmaktır.  Bir kitabı birincil kitap olarak seçebilirsiniz. Bu, genellikle amortisman muhasebesi için kullanılan defterdir. Ardından, hareketleri birincil defterle aynı aralıklarda nakletmek için kurulan diğer defterlere eklersiniz. Vergi amortisman defterleri genellikle türetilmiş defterler olarak oluşturulur. 

Türetilmiş defterlere nakletmek için ayarlanan en yaygın hareketler alımlar, alım düzeltmeleri ve çıkışlardır. 

## <a name="example"></a>Örnek

Defter B ve defter C, Alım hareket türü için defter A'nın türetilmiş defterleri olarak ayarlanır. Defter A'da, kıymet 123 için alım hareketi olarak 1.500,00 girin. 

Hareket nakledildiğinde, defter B için kıymet 123 içinde bir alım hareketi oluşturulur ve nakledilir. Defter C için kıymet 123 içinde 1.500,00 tutarında bir alım hareketi oluşturulur ve nakledilir. Birincil defterin hareketlerini sabit kıymet günlüğüne nakletmek için hazırladığınızda, ayrıca türetilmiş defterlerin hareketlerini de görüntüleyebilir ve değiştirebilirsiniz. Birincil defter hareketlerini başka günlükte hazırlarsanız türetilmiş değer hareketleri görüntülenmez. Ancak, birincil defter hareketlerini naklettiğinizde uygun hesaplara ve nakil katmanlarına nakledilir.

> [!NOTE]                                                                                                                               
> Birincil defter aralıkları dışındaki aralıklarda hareketleri nakletmek için oluşturulan defterler türetilmiş defterler olarak değil, ayrı defterler olarak sabit kıymete eklenmelidir.  

Daha fazla bilgi için bkz: [Türetilmiş defterlerle deftere nakletme](post-derived-value-models.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]