---
title: İlk müşteri ödeme tahmini modelini değerlendirme
description: Bu makalede, müşteri ödeme tahmin modelini anlamak ve verimliliğini değerlendirmek için gerçekleştirebileceğiniz adımlar açıklanmaktadır.
author: ShivamPandey-msft
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: fcdf276505cf58267a38e9d6174a155ad307653b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847016"
---
# <a name="evaluate-the-initial-customer-payment-prediction-model"></a>İlk müşteri ödeme tahmini modelini değerlendirme

[!include [banner](../includes/banner.md)]

Bu makalede, Finance Insights'ı etkinleştirdikten ve ilk modelinizi oluşturup eğittikten sonra bir tahmin modelinin nasıl değerlendirileceği açıklanmaktadır. Bu makalede, müşteri ödemelerini tahmin etmeye yönelik modeller ele alınmaktadır. Müşteri ödeme tahmin modelini anlamak ve verimliliğini değerlendirmek için gerçekleştirebileceğiniz adımları açıklamaktadır.

## <a name="getting-details-about-the-model"></a>Model hakkında ayrıntıları öğrenme

Microsoft Dynamics 365 Finance'teki **Finance Insights parametreleri** sayfasında, doğruluk puanının yanında bir **Model doğruluğunu iyileştir** bağlantısı gösterilir.

[![Model doğruluğunu iyileştir bağlantısı.](./media/prediction-model.png)](./media/prediction-model.png)

Bu bağlantı sizi, geçerli model hakkında daha fazla bilgi edinebileceğiniz AI Builder'a götürür ve modeli iyileştirmeye yönelik adımları içerir. Aşağıdaki şekilde açılan sayfa gösterilir.

[![AI Builder.](./media/what-to-predict.png)](./media/what-to-predict.png)

Açılan sayfada aşağıdaki bilgiler gösterilir:

- **Performans** bölümünde, model performans derecesi modelin kalitesiyle ilgili bir bakış açısı sağlar. Bu derece hakkında daha fazla bilgi için AI Builder belgelerindeki [Tahmin modeli performansı](/ai-builder/prediction-performance) konusuna bakın.
- **En etkili veri** bölümü modeliniz için farklı giriş türlerinin ne kadar önemli olduğunu gösterir. Bu listeyi ve ilgili yüzdeleri, bilgilerin işletmeniz ve pazarınızla ilgili olarak mevcut bilgilerinizle tutarlı olup olmadığını belirlemek için değerlendirebilirsiniz.

    [![Tahmin modeli için Performans ve En etkili veri bölümleri.](./media/models.png)](./media/models.png)

- **Performans** bölümünde, derece ve diğer hususlar hakkında daha fazla bilgi edinmek için **Ayrıntıları göster**'i seçin. Aşağıdaki şekilde, ayrıntılar modelin önerilenden daha az bilgi kullandığını göstermektedir. Bu nedenle, sistem bir uyarı iletisi oluşturmuştur.

    [![Model performansı ile ilgili uyarılar.](./media/details.png)](./media/details.png)

## <a name="digging-deeper"></a>Daha ayrıntılı bilgi

Doğruluk modeli değerlendirmek için iyi bir başlangıç noktası olsa da, performans derecesi bakış açısı sunar, AI Builder değerlendirme için kullanabileceğiniz daha ayrıntılı ölçümler sunar. Ayrıntıları indirmek için **Performans** bölümünde **Modeli kullan** düğmesinin yanındaki üç nokta düğmesini (**...**) seçin ve ardından **Ayrıntılı ölçümleri indir**'i seçin.

[![Ayrıntılı ölçümleri indir komutu.](./media/performance.png)](./media/performance.png)

Aşağıdaki şekilde, verileri indirebileceğiniz biçim gösterilmektedir.

[![İndirilen verilerin biçimi.](./media/data-format.png)](./media/data-format.png)

Sonuçların daha ayrıntılı analizi için "Karışıklık Matrisi" ölçümünü incelemek iyi bir başlangıç noktasıdır. Örneğin, bir önceki şekildeki bu ölçüm için gösterilen verileri burada görebilirsiniz.

`{"name": "Confusion Matrix", "value": {"schema_type": "confusion_matrix", "schema_version": "1.0.0", "data": {"class_labels": ["0", "1", "2"], "matrix": [[71, 9, 21], [5, 0, 27], [2, 0, 45]]}}, "type": "dictionaryNumericalList", "isGlobalScore": false}`

Bu verileri aşağıdaki şekilde genişletebilirsiniz.

| &nbsp;                   | Zamanında tahmini | Geç tahmini | Çok geç tahmini |
|--------------------------|-------------------|----------------|---------------------|
| Gerçek zamanında ödeme   | **71**            | 0              | 21                  |
| Gerçek geç ödeme      | 5                 | **0**          | 27                  |
| Gerçek çok geç ödeme | 2                 | 0              | **45**              |

Karışıklıklar matrisi, eğitim sürecinden rastgele seçilmiş bir test veri kümesinin sonuçlarını gösterir. Bu kapalı faturalar modeli eğitmek için kullanılmadığından, model için iyi bir test örneği oluştururlar. Ek olarak, faturanın gerçek durumu bilindiğinden, modelin performansı da görülebilir.

Bakılacak ilk şey en yaygın gerçek değerdir. Bu değer genel veri kümesiyle mükemmel şekilde eşleşmese de makul bir tahmindir. Bu durumda, **Gerçek zamanında ödeme** 171 toplam faturanın 92'sinde gerçekleştir ve en yaygın gerçek değerdir. Bu nedenle, modeliniz için iyi bir referans noktasıdır. Tüm faturaların zamanında olacağını tahmin ettiyseniz 171 kezden 92'sinde doğru tahmin etmiş olursunuz (diğer bir ifadeyle tahminleri yüzde 54'ü).

Veri kümenizin ne kadar dengeli olduğunu anlamanız önemlidir. Örneğin, 171 faturadan 92'si zamanında ödenmiş, 32'si geç ödenmiş ve 47'si çok geç ödenmiştir. Her sınıflandırmada önemsiz olmayan sonuçlar bulunduğundan, bu değerler makul bir şekilde dengeli bir veri kümesi olduğuna işaret eder. Durumlardan birinde çok az sonucun olduğu bir test makine öğrenimi modeli için zorlayacı olabilir.

Modelin doğruluğu test veri kümesi için doğru tahminlerin sayısını gösterir. Bu doğru tahminler önceki örnekte kalın olarak gösterilen değerlerdir. Bu durumda; değerlerin hesaplanan doğruluğu yüzde 67,8'dir (= \[71 + 0 + 45\] ÷ 171). Bu değer yüzde 54 olan referans çizgisi tahmininden yüzde 14 oranında iyileşme gösterir ve model kalitesinin bir göstergesidir.

Karışıklık matrisini daha ayrıntılı incelerseniz modelin, zamanında ve çok geç fatura ödemelerini tahmin etmede iyi bir iş çıkardığını fark edersiniz. Ancak, gerçekte geç ödenen (çok geç değil) 32 faturanın tümü hakkında yanlış tahminde bulunmuştur. Bu sonuç, modelin ek araştırma ve iyileştirmeye ihtiyaç duyduğunu gösterir.

Modelin performansını doğruluktan daha iyi gösteren değer F1 Makro puanıdır. Bu puan, her bir sınıflandırma durumunun (zamanında, geç ve çok geç) sonuçlarını dikkate alır. Örneğin, bir önceki şekildeki "F1 Macro" ölçümü için gösterilen verileri burada görebilirsiniz.

`{"name": "F1 Macro", "value": 0.4927170868347339, "type": "percentage", "isGlobalScore": false}`

Bu durumda, yaklaşık yüzde 49,3 oranındaki F1 Makro puanı modelin, makul ölçüde yüksek görünen toplam doğruluk puanına rağmen her durumda etkili tahminler yapmadığını gösterir.

## <a name="improving-the-model"></a>Modeli geliştirme

İlk modelinizin sonuçlarını daha iyi anladıktan sonra, özellik sütunları ekleyerek veya kaldırarak veya veri kümesinin doğru tahminleri desteklemeyen bölümlerine filtre uygulayarak modeli iyileştirmek isteyebilirsiniz. AI Builder'ı kapatın ve ardından AI Builder işlemini yeniden başlatmak için Dynamics 365 Finance'teki **Modeli iyileştir** bağlantısını kullanın. Yayımlanmış modeli etkilemeden farklı özelliklerle denemeler yapabilirsiniz. Yayımlamış model yalnızca **Yayımla**'yı seçtiğinizde etkilenir. Dynamics 365 Finance kurulumunuz için tek bir modelin kullanıldığını unutmayın. Bu nedenle, yayımlamadan önce tüm yeni modelleri dikkatli bir şekilde incelemeniz gerekir.

## <a name="for-more-information"></a>Daha fazla bilgi için

Tahmin modellerinin nasıl değerlendirileceği hakkında daha fazla bilgi için: [Makine öğrenimi modellerinin sonuçları](confusion-matrix.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
