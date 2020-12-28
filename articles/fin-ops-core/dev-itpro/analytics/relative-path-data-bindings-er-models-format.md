---
title: ER model ve biçimlerinin veri bağlamalarında göreli yol kullanma
description: Elektronik raporlama (ER) aracı, kullanıcıların elektronik biçim yapılarını tanımlamasına ve sonra da içerdiği veri ve uygulamadaki algoritmaları kullanarak bu yapıların nasıl doldurulması gerektiğini açıklayabilmesine olanak tanır.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5e2554dc33514185fa16868ee239c3e44ff675dd
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687490"
---
# <a name="use-a-relative-path-in-data-bindings-of-er-models-and-formats"></a>ER model ve biçimlerinin veri bağlamalarında göreli yol kullanma

[!include[banner](../includes/banner.md)]

Elektronik raporlama (ER) aracı, kullanıcıların elektronik biçim yapılarını tanımlamasına ve sonra da içerdiği veri ve uygulamadaki algoritmaları kullanarak bu yapıların nasıl doldurulması gerektiğini açıklayabilmesine olanak tanır. Daha fazla bilgi için bkz: [Create Electronic reporting (ER) configurations](electronic-reporting-configuration.md). Finance and Operations verilerini almak ve bunu elektronik bir belge oluşturmak için kullanmak üzere veri akışını belirtmek için aşağıdakileri yapmanız gerekir:

- Yapılandırılmış veri kaynaklarını tasarlanan etki alanına özgü [veri modeli](general-electronic-reporting.md#data-model-and-model-mapping-components) öğelerine bağlayın. Model yapısı ve seçili veri kaynakları karmaşık hiyerarşik bir yapının parçası olabilir. Bu nedenle, son bağlamalar çok büyük olabilir ve farklı türlerde birçok öğe (örneğin, ilişkiler, tablolar ve yöntemler) içerebilir. Özellikle sahip olmayanlar için bağlamalar daha az okunabilir, incelenebilir ve anlaşılması çok karmaşık hale gelebilir. 
- Veri modelinden oluşturulan biçim çıktısına hangi verilerin doldurulduğunu tanımlamak için veri modeli öğelerini [biçim](general-electronic-reporting.md#FormatComponentOutbound) bileşenleri ile bağlayın.

ER eşleme tasarımcılarının kullanılabilirliğini iyileştirmek için [göreli yol](er-formula-language.md#relative-path) özelliği serbest bırakıldı. Varsayılan olarak, ER tasarım deneyiminin etkinleştirildiği her yeni uygulama örneği için göreli yol gösterimi seçeneği açıktır (Microsoft Dynamics 365 Finance, Microsoft Regulatory Configuration Service). Kullanıcıların bu ER bağlamalarıyla çalışırken tam yolu kullanmaya devam edebilmesi için göreli yol parametresi uyguladık.

[![Kullanıcı parametreleri](./media/relative-path-01.png)](./media/relative-path-01.png)

 
Göreli yol kullanım parametresi açıldığında, tek bir @ karakteri geçerli model öğesinin bağlamasında üst öğeye ilişkin yolu değiştirir. Tüm bağlama yolu daha kısalır bu da tüm eşlemeyi daha belirgin ve daha kolay anlaşılır yapar. Çoğu durumda, ER tasarımcısında veri modeli tüm bağlamalarını görüntülemek için ek kaydırma gerekmez.

[![Model eşleme tasarımcısı](./media/relative-path-02.png)](./media/relative-path-02.png)
 
Yeni bir ER ifadesi tasarlamaya başladığınızda, üst öğenin bir alanına bağlamayı tanımlamak için yalnızca bir karakter girmeniz gerekir.

[![Formül tasarımcısı](./media/relative-path-03.png)](./media/relative-path-03.png)
 
Üst model öğesinin veri kaynağını mutlak yol kullanımı ile değiştirmeye karar verirken, bu model öğesinin yanı sıra iç içe geçmiş öğelerin de yeni bir veri kaynağına el ile yeniden bağlamanız gerekir. Göreli yol kullanımı açık olduğunda ve üst öğeye bağlanacak yeni bir veri kaynağı seçtiğinizde, bu üst öğenin tüm iç içe öğelerini tek bir tıklama ile otomatik olarak yeniden bağlamak için bir seçenek sunulur.

[![Geçerli şema iletisini değiştir](./media/relative-path-04.png)](./media/relative-path-04.png)
 
İç içe yerleştirilmiş öğelerin yeniden bağlamasının onaylarsanız yeni ana öğe, varolan üst öğeyi içeren her iç içe öğenin yoluna yerleştirilir.
Bu özellik, ER çerçevesinin geriye dönük uyumluluğunu koparmaz. Daha önce tasarlamış olan tüm ER yapılandırmaları bu yeni özellik ile çalışacak; bunlara yükseltme veya dönüştürme gerekli değildir.

> [!NOTE]
> Model eşleştirmelerinde iç içe öğelerin bağlamalarının toplu değişikliği ile tanıtılan tüm değişiklikler bir yapılandırma farkı değişimlerinde doğru kaydedilir (değişiklikleri izleme). Bu, müşterilerin, bu yeni özellik kullanılarak değiştirilmiş olan model eşleştirmelerinin tüm yeni temel sürümlerini yeniden temellendirmelerine olanak sağlar.

## <a name="additional-resources"></a>Ek kaynaklar

[ER formül dili](er-formula-language.md)
