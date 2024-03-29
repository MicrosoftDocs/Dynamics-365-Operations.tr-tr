---
title: Türetilmiş defterlerle deftere nakletme
description: Bu makale, türetilmiş defterlerin nasıl kullanılacağını açıklar.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: kfend
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0270ad1e66193832fb1139fca4439b36b5ffb84
ms.sourcegitcommit: dca54dd3afc7c94795d89c63050b105df2c48e3f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/15/2022
ms.locfileid: "9682920"
---
# <a name="post-with-derived-books"></a>Türetilmiş defterlerle deftere nakletme

[!include [banner](../includes/banner.md)]

Bu makale, türetilmiş defterlerin nasıl kullanılacağını açıklar.

Türetilmiş defterler içeren bir defter için hareketleri deftere naklettiğinizde, türetilmiş defter hareketleri otomatik olarak günlüklerde, satınalma siparişlerinde ve serbest metin faturalarında deftere nakledilir. Ancak birincil defter hareketlerini Sabit kıymetler günlüğünde hazırlarsanız türetilmiş hareketlere ait miktarları deftere nakletmeden önce görüntüleyebilir ve değiştirebilirsiniz.
-   Satış vergisi ve müşteri veya satıcı hesapları gibi birtakım hesaplar yalnızca bir kez birincil defterin deftere nakilleriyle güncelleştirilir. Türetilmiş defter hareketleri, Sabit kıymet nakil profilleri sayfasındaki türetilmiş defter için tanımlanmış hesaplardaki deftere nakledilir.
-   Alım, çoğu zaman türetilmiş defter için hareket türü olarak kullanılır. Bunu, defter ile türetilmiş defterin, sabit kıymetin alım zamanından başlanarak sabit kıymete uygulanması gerektiği durumlarda kullanırsınız.
-   Hareket türü bilgisine ait diğer değerler de uygulanabilir. Örneğin, birincil defter ve türetilmiş defterler satış veya elden çıkarma açısından aynı aralıklara sahipse bir türetilmiş defterin kurulumunda tüm sabit kıymet hareket türleri kullanılabilir.

> [!WARNING]
> Türetilmiş defterde deftere nakledilen amortisman, birincil defter için deftere nakledilen tutarın aynısı olur. Amortisman yöntemleri defterler arasında farklılık gösteriyorsa türetilmiş işlemini kullanarak amortisman hareketleri oluşturmamanız gerekir. 

## <a name="example"></a>Örnek 
Aşağıdaki bilgiler, türetilmiş defter işleviyle alım hareketlerinin nasıl ayarlanacağını açıklar.

1.  Defterler sayfasında defterler oluşturun.
    -   Muhasebeye yönelik defter: VM 1, Geçerli deftere nakil katmanı
    -   Vergi amaçlı defter: VM 2, Vergi deftere nakil katmanı

2.  VM 1'de, Türetilen defterler sekmesine tıklayın. VM 2'yi Defter alanından ve Hareket türü alnından Satınalma'yı seçin.

Ardından, defterler belirli sabit kıymetlere eklenebilir. 

Bir alım, defter VM 1'e sahip bir sabit kıymet için deftere nakledildiğinde, alım yalnızca VM 1'de değil, aynı zamanda türetilmiş defter VM 2'de de deftere nakledilmiştir. Her iki sabit kıymet defterinin durumu da Açık olarak güncelleştirilir.

> [!NOTE]                                                                                                         
> Türetilmiş defterleri kullanmıyorsanız sabit kıymet alımını hem VM 1 defteri, hem de VM 2 defteri için deftere nakletmeniz gerekir.

Daha fazla bilgi için bkz. [Türetilmiş defterler](derived-books.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
