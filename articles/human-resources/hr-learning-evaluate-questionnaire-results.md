---
title: Soru formlarının sonuçlarını görüntüleme ve değerlendirme
description: Bu makale yanıtlayanların tamamladığı anketlerin sonuçlarını nasıl görüntüleyeceğinizi ve değerlendireceğinizi açıklar.
author: andreabichsel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMCollection, KMKnowledgeCollectorCollection, KMKnowledgeCollectorUserResults, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 17444
ms.assetid: 6570206a-b2c4-4025-8715-432fe6652b78
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 54530a8735cb8ce4b21688eae86fda83035133ed
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464970"
---
# <a name="view-and-evaluate-the-results-of-questionnaires"></a>Soru formlarının sonuçlarını görüntüleme ve değerlendirme

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makale yanıtlayanların tamamladığı anketlerin sonuçlarını nasıl görüntüleyeceğinizi ve değerlendireceğinizi açıklar. 

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

Yanıtlayanlar bir anketi tamamladıktan sonra, tamamlanan yanıt oturumlarının sonuçlarını görüntüleyebilirsiniz. Bir yanıt oturumu kullanıcının bir ankete yanıtıdır. Tamamlanmış yanıt oturumları hakkındaki ayrıntıları **Yanıtlar** sayfasında görüntüleyebilirsiniz. **Yanıtlar** sayfasına dahil edilen yanıt oturumları sayfayı nasıl açtığınıza bağlı olarak çeşitli yollarla filtrelenir:

-   Tüm anketler
-   Belirli bir anket
-   Belirli bir kişi

**Yanıtlar** sayfasından, yanıtlar hakkındaki ayrıntıları, kazanılan puanları, bir yanıtlayanın her yanıt grubundaki yanıtlarını ve eğer bir soru hiyerarşisi kullanıldıysa, seçili ankette kullanılan soru hiyerarşisini görüntüleyebilirsiniz. Ayrıca aşağıdaki raporları oluşturabilir ve yazdırabilirsiniz:

-   **Sonuçlar raporu**: Bu rapor, seçili yanıt oturumu için sonuç grubu başına kazanılan puanların grafik gösterimini gösterir.
-   **Yanıt raporu** – Bu rapor, anketteki her soru için yanıtlayanın seçtiği cevapları gösterir.
-   **Yanlış yanıtlar**: Bu rapor yanıtlayanın seçtiği yanlış yanıtlarla ilgili bilgileri gösterir.

> [!NOTE]
> **Sonuçlar** raporu, yalnızca anketteki sonuç gruplarını kullanıyorsanız ve **Anketler** sayfasındaki **Sonuçlar sayfasını** seçtiyseniz kullanılabilir. **Yanıt** raporu ve **Yanlış yanıtlar** raporu yalnızca **Anketler** sayfasındaki **Yanıt raporu** seçeneğini seçtiyseniz kullanılabilir.

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

[!INCLUDE[footer-include](../includes/footer-banner.md)]