---
title: Muhasebe kaynağı gezgini
description: Bu makalede, genel muhasebe girişleri arkasındaki kaynak bilgilerinin ayrıntılı analizi için kullanabileceğiniz Muhasebe kaynağı gezgini hakkında bilgiler verilmektedir.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingSourceExplorer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 904f1f9fb139248205b426aec5a0372f2edb1e59
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837530"
---
# <a name="accounting-source-explorer"></a>Muhasebe kaynağı gezgini

[!include [banner](../includes/banner.md)]

Bu makalede, genel muhasebe girişleri arkasındaki kaynak bilgilerinin ayrıntılı analizi için kullanabileceğiniz Muhasebe kaynağı gezgini hakkında bilgiler verilmektedir.

Muhasebe kaynağı gezgini, kaynak bilgilerini gösteren yeni bir sayfadır. Muhasebe kaynak gezginin, ister bir tek başına araç isterseniz de genel muhasebe defteri muhasebe girişleri arkasındaki ayrıntıları analiz etmek için bir araç olarak kullanabilirsiniz. Örneğin, Muhasebe kaynak gezginini, Mizan içindeki bir bakiye veya fiş hareketindeki en ayrıntılı bilgiyi edinmek için kullanabilirsiniz. Ardından, bilgilerini Microsoft Excel programında ayrıntılı şekilde değerlendirmek (örneğin PivotTable raporu içinde veya üzerinde kullanmak) için MS Excel'e Aktar özelliğini kullanabilirsiniz.

Muhasebe kaynağı gezgini daima genel muhasebe hesabı için tutarı Genel defterde gösterildiği şekilde (örneğin Mizan) aynı olarak gösterir. Mizanda olduğu gibi segmentleri ayrı sütunlarda görüntüleyebilirsiniz. Sadece uygun mali boyut kümesini seçmeniz yeterlidir. 

Analiz için bir tarih aralığını tanımlamak için parametreleri kullanabilirsiniz. Bu işlev ayrıca Mizandaki işlevlere benzerdir.

Kaynak belge çerçevesini kullanan tüm belgeler için, Muhasebe kaynak gezgini, muhasebe dağılımlarına dayanarak ve mevcutsa, proje muhasebe dağılımlarına dayanarak ek bilgiyi gösterir. Bu bilgilere, parasal tutar türü, proje, faaliyet, kategori ve satır özelliği dahildir. Burada, gerçekleştirebileceğiniz analizlere bazı örnekler verilmiştir:

-   Satın alma emirleri ile satıcı faturaları arasındaki farklar, çünkü her bir fark örneğin masraf farkı vb. gibi bir parasal tutar türüyle temsil edilir
-   Proje, ticari birim ve ana hesap başına faturalanabilir - faturalanamayan saatler ve masraflar karşılaştırması

Kaynak belgesi referans kimlikleri konseptini kullanan kaynak belgeler için, Muhasebe kaynağı gezgini örneğin müşteri, satıcı, çalışan, ürün, miktar, birim metni ve açıklamalar gibi daha fazla ayrıntıyı gösterir. Burada, gerçekleştirebileceğiniz analizlere bazı örnekler verilmiştir:

-   Bir mali dönem için maliyet raporlarına dayalı olarak ticari birim ve otel markası başına otel masrafları
-   Satıcı, ürün, departman başına iskontolar

Bu belgeler için, Muhasebe kaynağı gezgininden ayrıca mevcut kaynak belgesine geçiş yapabilirsiniz.



