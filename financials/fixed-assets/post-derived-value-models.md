---
title: "Türetilmiş defterlerle deftere nakletme"
description: "Bu makale, türetilmiş defterlerin nasıl kullanılacağını açıklar."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: ca077727910059878fb16a3f78c5b9133c6c741f
ms.lasthandoff: 03/31/2017


---

# <a name="post-with-derived-books"></a>Türetilmiş defterlerle deftere nakletme

[!include[banner](../includes/banner.md)]


Bu makale, türetilmiş defterlerin nasıl kullanılacağını açıklar.

Türetilmiş defterler içeren bir defter için hareketleri deftere naklettiğinizde, türetilmiş defter hareketleri otomatik olarak günlüklerde, satınalma siparişlerinde ve serbest metin faturalarında deftere nakledilir. Ancak birincil defter hareketlerini Sabit kıymetler günlüğünde hazırlarsanız türetilmiş hareketlere ait miktarları deftere nakletmeden önce görüntüleyebilir ve değiştirebilirsiniz.
-   Satış vergisi ve müşteri veya satıcı hesapları gibi birtakım hesaplar yalnızca bir kez birincil defterin deftere nakilleriyle güncelleştirilir. Türetilmiş defter hareketleri, Sabit kıymet nakil profilleri sayfasındaki türetilmiş defter için tanımlanmış hesaplardaki deftere nakledilir.
-   Alım, çoğu zaman türetilmiş defter için hareket türü olarak kullanılır. Bunu, defter ile türetilmiş defterin, sabit kıymetin alım zamanından başlanarak sabit kıymete uygulanması gerektiği durumlarda kullanırsınız.
-   Hareket türü bilgisine ait diğer değerler de uygulanabilir. Örneğin, birincil defter ve türetilmiş defterler satış veya elden çıkarma açısından aynı aralıklara sahipse bir türetilmiş defterin kurulumunda tüm sabit kıymet hareket türleri kullanılabilir.

> [!WARNING]
> Türetilmiş defterde deftere nakledilen amortisman, birincil defter için deftere nakledilen tutarın aynısı olur. Amortisman yöntemleri defterler arasında farklılık gösteriyorsa türetilmiş işlemini kullanarak amortisman hareketleri oluşturmamanız gerekir. |

## <a name="example"></a>Örnek 
Aşağıdaki bilgiler, türetilmiş defter işleviyle alım hareketlerinin nasıl ayarlanacağını açıklar.

1.  Defterler sayfasında defterler oluşturun.
    -   Muhasebeye yönelik defter: VM 1, Geçerli deftere nakil katmanı
    -   Vergi amaçlı defter: VM 2, Vergi deftere nakil katmanı

2.  VM 1'de, Türetilmiş defterler sekmesine tıklayın. Defter alanında VM 2'yi ve Hareket türü alanında Alım'ı seçin.

Ardından, defterler belirli sabit kıymetlere eklenebilir. 

Bir alım, defter VM 1'e sahip bir sabit kıymet için deftere nakledildiğinde, alım yalnızca VM 1'de değil, aynı zamanda türetilmiş defter VM 2'de de deftere nakledilmiştir. Her iki sabit kıymet defterinin durumu da Açık olarak güncelleştirilir.

> [!NOTE]                                                                                                         
> Türetilmiş defterleri kullanmıyorsanız sabit kıymet alımını hem VM 1 defteri, hem de VM 2 defteri için deftere nakletmeniz gerekir.

Daha fazla bilgi için bkz. [Türetilmiş defterler](derived-books.md).




