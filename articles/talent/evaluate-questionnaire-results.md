---
title: "Bir anketin sonuçlarını görüntüleyin ve değerlendirin"
description: "Bu konu yanıtlayanların tamamladığı anketlerin sonuçlarını nasıl görüntüleyeceğinizi ve değerlendireceğinizi açıklar."
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KMCollection, KMKnowledgeCollectorCollection, KMKnowledgeCollectorUserResults
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 17444
ms.assetid: 6570206a-b2c4-4025-8715-432fe6652b78
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9b6357288f340e4248cd5a87c2c3f773e0c32aec
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="view-and-evaluate-the-results-of-a-questionnaire"></a>Bir anketin sonuçlarını görüntüleyin ve değerlendirin

Bu konu yanıtlayanların tamamladığı anketlerin sonuçlarını nasıl görüntüleyeceğinizi ve değerlendireceğinizi açıklar. 

Yanıtlayanlar bir anketi tamamladıktan sonra, anket sonuçlarını aşağıdaki yollardan görüntüleyebilir ve değerlendirebilirsiniz:

-   **Tamamlanan yanıt oturumları** – Yanıtlayanların tamamladığı anketler hakkındaki ayrıntıları görüntüleyin ve yanıtları ve kazanılan puanları özetleyen raporlar üretin.
-   **Sonuç grupları** – Anketler için sonuç grubu detayları ve istatistiklerini görüntüleyin. Sonuç grubu istatistikleri ya bir anketin tek bir yanıt oturumu veya tüm yanıt oturumları için oluşturulabilir.
-   **Anket istatistikleri** – Belirli bir yanıtlayan grubu için istatistik hesaplamak için ölçütleri belirleyin.

Ayrıca kişi, yanıt oturumu veya sonuç grubuna göre sıralanmış sonuçları görüntülemek için çeşitli raporlar oluşturabilirsiniz. Tamamlanmış anketlerle ilgili aşağıdaki raporlar kullanılabilir:

-   Yanıtlar
-   Soru formu başına yanıt sayısı
-   Kişi başına yanıt sayısı
-   Geribildirim analizi

## <a name="answer-session-results"></a>Yanıt oturumu sonuçları
Yanıtlayanlar bir anketi tamamladıktan sonra, tamamlanan yanıt oturumlarının sonuçlarını görüntüleyebilirsiniz. Bir yanıt oturumu kullanıcının bir ankete yanıtıdır. Tamamlanmış yanıt oturumları hakkındaki ayrıntıları **Yanıtlar** sayfasında görüntüleyebilirsiniz.  **Yanıtlar** sayfasına dahil edilen yanıt oturumları sayfayı nasıl açtığınıza bağlı olarak çeşitli yollarla filtrelenir:

-   Tüm anketler
-   Belirli bir anket
-   Belirli bir kişi

**Yanıtlar** sayfasından, yanıtlar hakkındaki ayrıntıları, kazanılan puanları, bir yanıtlayanın her yanıt grubundaki yanıtlarını ve eğer bir soru hiyerarşisi kullanıldıysa, seçili ankette kullanılan soru hiyerarşisini görüntüleyebilirsiniz. Ayrıca aşağıdaki raporları oluşturabilir ve yazdırabilirsiniz:

-   **Sonuç raporu** – Bu rapor, seçili yanıt oturumu için sonuç grubu başına kazanılan puanların grafik gösterimini gösterir.
-   **Yanıt raporu** – Bu rapor, anketteki her soru için yanıtlayanın seçtiği cevapları gösterir.
-   **Yanlış yanıtlar** – Bu rapor yanıtlayanın seçtiği yanlış yanıtlarla ilgili bilgileri gösterir.

**Not:** **Sonuçlar** raporu, yalnızca anketteki sonuç gruplarını kullanıyorsanız ve **Anketler** sayfasındaki **Sonuçlar sayfasını** seçtiyseniz kullanılabilir. **Yanıt** raporu ve **Yanlış yanıtlar** raporu yalnızca **Anketler** sayfasındaki **Yanıt raporu** seçeneğini seçtiyseniz kullanılabilir.

## <a name="questionnaire-statistics"></a>Soru formu istatistikleri
Tamamlanmış bir anketin sonuçlarını tanımladığınız hesaplamalara göre analiz etmek için anket istatistiklerini kullanabilirsiniz. Hesaplamaları tanımlamak için, aşağıdaki görevleri tamamlamalısınız:

-   İstatistikleri hesaplamak ve görüntülemek için ölçüt seçin.
    -   Anket, sorular, soru satırları veya sonuç gruplarına göre istatistikleri görüntüleyebilirsiniz.
    -   Sonuçları görüntülerken kullanılacak grafik türünü seçin.
    -   Yanıtları dahil etmek için ağdan, çalışanlar, iletişim kişileri veya başvuranlar gibi kişi türlerini seçin. Aynı zamanda anonim olarak tamamlanmış anketlerden yanıtları dahil edebilirsiniz.
    -   Sonuçları analiz etmek için yaş veya kıdeme dayanan aralıklar ayarlayın.
-   İstatistiklerin konusunu yenileyen ayarları seçin veya doğrulayın. Örneğin, bir posta kodu seçerek belirli bir coğrafi bölge içindeki tüm yanıtlayanlar için sonuçları analiz edebilirsiniz.
-   Yanıtlayan veya anket özelliklerine göre sonuçları analiz etmek için ölçütleri seçin veya doğrulayın. Örneğin, **Posta kodu**, seçeneğini seçerek, yanıtlayanın konumu ve doğru yanıtlar arasındaki korelasyonu analiz edebilirsiniz.

Tanımladığınız ayarlar kaydedilir ve sonuçları yeniden hesaplamak için periyodik olarak kullanılabilir.

<a name="see-also"></a>Ayrıca bkz.
--------

[Soru formları tasarlama](design-questionnaires.md)

[Soru formlarını kullanma](questionnaires.md)

[Soru formlarını dağıtma ve tamamlama](distribute-questionnaires.md)


