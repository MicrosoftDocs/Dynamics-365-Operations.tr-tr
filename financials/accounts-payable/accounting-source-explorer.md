---
title: "Muhasebe kaynağı gezgini"
description: "Bu makalede, genel muhasebe girişleri arkasındaki kaynak bilgilerinin ayrıntılı analizi için kullanabileceğiniz Muhasebe kaynağı gezgini hakkında bilgiler verilmektedir."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: 8913e61285d5d180883471991b659ddcb260afe3
ms.lasthandoff: 03/31/2017


---

# <a name="accounting-source-explorer"></a>Muhasebe kaynağı gezgini

Bu makalede, genel muhasebe girişleri arkasındaki kaynak bilgilerinin ayrıntılı analizi için kullanabileceğiniz Muhasebe kaynağı gezgini hakkında bilgiler verilmektedir.

Muhasebe kaynağı gezgini, kaynak bilgilerini gösteren yeni bir sayfadır. Hesap kaynak Gezgini ya da tek başına bir araç olarak veya genel muhasebe girişlerini arkasındaki detayları analiz etmek için kullanabilirsiniz. Örneğin, bir defter-i Kebir bakiyesi veya fiş hareketi için en ayrıntılı kaynak bilgileri almak için hesap kaynak Gezgini'ni kullanabilirsiniz. Ardından, bilgilerini Microsoft Excel programında ayrıntılı şekilde değerlendirmek (örneğin PivotTable raporu içinde veya üzerinde kullanmak) için MS Excel'e Aktar özelliğini kullanabilirsiniz.

Muhasebe kaynağı gezgini daima genel muhasebe hesabı için tutarı Genel defterde gösterildiği şekilde (örneğin Mizan) aynı olarak gösterir. Mizanda olduğu gibi segmentleri ayrı sütunlarda görüntüleyebilirsiniz. Sadece uygun mali boyut kümesini seçmeniz yeterlidir. 

Analiz için bir tarih aralığını tanımlamak için parametreleri kullanabilirsiniz. Bu işlev ayrıca Mizandaki işlevlere benzerdir.

Hesap kaynağı, kaynak belge framework kullanan tüm belgeler için explorer üzerinde hesap dağıtımları tabanlı ek bilgi gösterir ve, uygunsa, proje dağıtımları hesap. Bu bilgiler, parasal tutar türü, proje, faaliyet, kategori ve satır özelliği içerir. Burada, gerçekleştirebileceğiniz analizlere bazı örnekler verilmiştir:

-   Satın alma emirleri ile satıcı faturaları arasındaki farklar, çünkü her bir fark örneğin masraf farkı vb. gibi bir parasal tutar türüyle temsil edilir
-   Proje, ticari birim ve ana hesap başına faturalanabilir - faturalanamayan saatler ve masraflar karşılaştırması

Kaynak belgesi referans kimlikleri konseptini kullanan kaynak belgeler için, Muhasebe kaynağı gezgini örneğin müşteri, satıcı, çalışan, ürün, miktar, birim metni ve açıklamalar gibi daha fazla ayrıntıyı gösterir. Burada, gerçekleştirebileceğiniz analizlere bazı örnekler verilmiştir:

-   Bir mali dönem için maliyet raporlarına dayalı olarak ticari birim ve otel markası başına otel masrafları
-   Satıcı, ürün, departman başına iskontolar

Bu belgeler için, Muhasebe kaynağı gezgininden ayrıca mevcut kaynak belgesine geçiş yapabilirsiniz.


