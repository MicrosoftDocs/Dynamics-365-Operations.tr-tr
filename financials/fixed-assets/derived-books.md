---
title: "Türetilen defterler"
description: "Bu makale, türetilmiş defter işlevselliğine genel bir bakış sağlar."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetBookTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: 9319fe95a25b38ca12cbc8633763b042e4086aea
ms.lasthandoff: 03/31/2017


---

# <a name="derived-books"></a>Türetilen defterler

Bu makale, türetilmiş defter işlevselliğine genel bir bakış sağlar.

Türetilmiş kitaplar amacı, düzenli aralıklarla planlanan sabit kıymet defteri hareketlerinin deftere nakil kolaylaştırmaktır.  Bir kitap birincil defteri seçmeniz gerekir. Bu, genellikle amortisman muhasebesi için kullanılan defterdir. Ardından, hareketleri birincil defterle aynı aralıklarda nakletmek için kurulan diğer defterlere eklersiniz. Vergi amortisman defterleri genellikle türetilmiş defterler olarak oluşturulur. 

Türetilmiş defterlere nakletmek için ayarlanan en yaygın hareketler alımlar, alım düzeltmeleri ve çıkışlardır. 

## <a name="example"></a>Örnek

Defter B ve defter C, Alım hareket türü için defter A'nın türetilmiş defterleri olarak ayarlanır. Defter A'da, kıymet 123 için alım hareketi olarak 1.500,00 girin. 

Hareket nakledildiğinde, defter B için kıymet 123 içinde bir alım hareketi oluşturulur ve nakledilir. Defter C için kıymet 123 içinde 1.500,00 tutarında bir alım hareketi oluşturulur ve nakledilir. Birincil defterin hareketlerini sabit kıymet günlüğüne nakletmek için hazırladığınızda, ayrıca türetilmiş defterlerin hareketlerini de görüntüleyebilir ve değiştirebilirsiniz. Birincil defter hareketlerini başka günlükte hazırlarsanız türetilmiş değer hareketleri görüntülenmez. Ancak, birincil defter hareketlerini naklettiğinizde uygun hesaplara ve nakil katmanlarına nakledilir.

> [!NOTE]                                                                                                                               
> Birincil defter aralıkları dışındaki aralıklarda hareketleri nakletmek için oluşturulan defterler türetilmiş defterler olarak değil, ayrı defterler olarak sabit kıymete eklenmelidir.  

Daha fazla bilgi için bkz: [türetilmiş Defterleriyle deftere nakil](post-derived-value-models.md).


