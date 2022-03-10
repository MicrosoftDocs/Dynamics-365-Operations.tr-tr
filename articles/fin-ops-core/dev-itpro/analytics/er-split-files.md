---
title: Oluşturulan XML dosyalarını dosya boyutu ve içerik miktarına göre bölme
description: Bu konu, oluşturulan dosyaların dosya boyutuna ve içerik öğesi miktarına göre nasıl bölüneceği hakkında bilgi sağlamaktadır.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 3735bcb06eff966fc364a891b38d44e34e845e35f59314822d13eba40d51d5f4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769984"
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

- [ER modeli yapılandırması - XmlFilesSplittingModel.xml](https://download.microsoft.com/download/e/a/f/eaffe96a-22ec-4a32-898a-f4328c91c387/XmlFilesSplittingModel.xml)
- [ER biçimi yapılandırması - XmlFilesSplittingFormat.xml](https://download.microsoft.com/download/e/9/c/e9c5849b-8254-4cdf-bb00-4c2ebc72ddec/XmlFilesSplittingFormat.xml)

## <a name="additional-resources"></a>Ek kaynaklar
[Elektronik raporlama (ER) hedefleri](electronic-reporting-destinations.md)

[Elektronik raporlamada (ER) formül tasarımcısı](general-electronic-reporting-formula-designer.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
