---
title: Oluşturulan XML dosyalarını dosya boyutu ve içerik miktarına göre bölme
description: Bu konu, oluşturulan dosyaların dosya boyutuna ve içerik öğesi miktarına göre nasıl bölüneceği hakkında bilgi sağlamaktadır.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 8c3899d5c6602b3afe13b447b40f0b4dcc701448
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554081"
---
# <a name="split-generated-xml-files-based-on-file-size-and-content-quantity"></a>Oluşturulan XML dosyalarını dosya boyutu ve içerik miktarına göre bölme

[!include[banner](../includes/banner.md)]

XML biçiminde giden belgeler oluşturmak için Elektronik raporlama (ER) biçimleri tasarlayabilirsiniz. Bazen bu belgeler yalnızca belirli ölçütleri (maksimum dosya boyutu, bazı XML düğümlerinin maksimum sayısı vb.) karşıladıkları zaman kabul edilebilir. Bu belgelerin alıcılarının belirttiği gereksinimleri karşılayan elektronik belgeler oluşturmak için ER biçimleri tasarlayabilirsiniz.

- FILE biçim öğesi için, ER ifadesi olarak bir dosya boyutu sınırı tanımlayabilirsiniz. Bir ER raporu oluşturulurken, tanımlanan sınır aşılırsa, ER o geçerli dosyayı oluşturmayı bitirir ve sonraki dosyayı oluşturmaya geçer.
- Herhangi bir XML ELEMENT biçimi için, ER ifadesi olarak bir öğe sayısı sınırı tanımlayabilirsiniz. Bir ER raporu çalıştırılırken, oluşturulan dosyadaki XML düğümü sayısı aşılırsa, ER o geçerli dosyayı oluşturmayı bitirir ve sonraki dosyayı oluşturmaya geçer.
- Herhangi bir XML SEQUENCE biçim öğesi için, ER ifadesi olarak bir alt öğe sayısı sınırı tanımlayabilirsiniz. Bir ER raporu çalıştırılırken, oluşturulan dosyadaki biçim öğesinin iç içe XML düğümü sayısı aşılırsa, ER o geçerli dosyayı oluşturmayı bitirir ve sonraki dosyayı oluşturmaya geçer.
- Bir XML ELEMENT biçim öğesini bölünemez olarak işaretleyebilirsiniz. Bu sayede, biçim öğesi altında oluşturulan XML düğümlerinin iç içe öğelerini, oluşturulan tek bir dosyada tutabilirsiniz.

Oluşturulan dosyaya XML düğümleri eklemek için XML ELEMENT ve XML SEQUENCE biçim öğelerinin yanı sıra, RAW XML biçim öğesini kullanabilirsiniz. Ancak, öğe sayısındaki sınırları değerlendirmek için düğüm sayısı hesaplanırken, RAW XML biçim öğesini kullanarak eklediğiniz düğümler hesaba katılmaz.

Belirlenen sınırlar her aşıldığında, oluşturulan çıktıyı bölmek için yapılandırılmış bir FILE biçim öğesine ilişkin dosya hedefleri yapılandırdıysanız, oluşturulan çıktının her bir parçası ayrı birer dosya olarak, yapılandırılan dosya hedefine gönderilir. Çıktının bölünmesiyle oluşturulan dosyalara benzersiz adlar vermek için, FILE biçim öğesine ilişkin bir ER ifadesi yapılandırmanız gerekir. NUMBER SEQUENCE türünde bir ER veri kaynağı eklerseniz, bölünen çıktının her bir parçası için, artan düzende sıra numarası eklenir.

Bu özellik hakkında daha fazla bilgi için, **7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş sürecinin bir parçası olan ve [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684)'dan indirilebilen **ER - XML dosyalarını dosya boyutu ve içerik miktarına göre bölme** görev kılavuzunu oynatın. Bu görev kılavuzu, oluşturulan dosyaları dosya boyutu ve içerik öğesi miktarı sınırlarına göre bölmek için bir ER biçimi yapılandırma işleminde size yol gösterir. Görev kılavuzunu tamamlamak için aşağıdaki dosyaları indirmeniz gerekir:

- [ER modeli yapılandırması - XmlFilesSplittingModel.xml](https://go.microsoft.com/fwlink/?linkid=874111)
- [ER biçimi yapılandırması - XmlFilesSplittingFormat.xml](https://go.microsoft.com/fwlink/?linkid=874111)

## <a name="additional-resources"></a>Ek kaynaklar
[Elektronik raporlama hedefleri](electronic-reporting-destinations.md)

[Elektronik raporlamada formül tasarımcısı](general-electronic-reporting-formula-designer.md)
