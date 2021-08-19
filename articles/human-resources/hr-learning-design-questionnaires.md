---
title: Anketler oluşturma
description: Bu makale bir anket oluşturma işlemini açıklar. İlk adım anketi tasarlamaktır. Bir anket tasarladığınızda, yalnızca soru ve yanıtları yazmayın, aynı zamanda yanıtların kaydedilip tablolar oluşturulmasını sağlayan yapıyı oluşturun.
author: andreabichsel
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KCMCollectionType, KMAnswerCollection, KMCollection, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 17341
ms.assetid: b27e2f12-c7a0-4a54-b8d8-17819f8a1c72
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: c2a8c156aa75b02b69da3ee70a1ee60ea9d73a8aa67c70babdaaad88d6eb81f4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755576"
---
# <a name="create-questionnaires"></a>Anketler oluşturma

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makale bir anket oluşturma işlemini açıklar. İlk adım anketi tasarlamaktır. Bir anket tasarladığınızda, yalnızca soru ve yanıtları yazmayın, aynı zamanda yanıtların kaydedilip tablolar oluşturulmasını sağlayan yapıyı oluşturun. 

Dikkatli şekilde tasarlanmış bir anket, topladığınız verilerin kalitesini artırabilir. Dikkatli tasarım ile bir anket için uygun zamanda uygun seçenekleri daha iyi seçebilirsiniz. Aşağıdaki noktalar etkili bir anket planlamanıza yardımcı olabilir:

-   Soruların amacı desteklemesini sağlanmasına yardımcı olmak için anketin amacını açıkça tanımlayın.
-   Soru formunu doldurması gereken kişi veya kişi grubunu belirleyin.
-   Ankette görünecek sorular yazın ve uygulanabilirse, cevap seçenekleri de ekleyin.
-   Yanıtlayanların bağlı kalmaları için anketin mantıksal olarak aktığından emin olun.
-   Sorular ve yanıtları yanıtlayanlara sunulacakları sırayla düzenleyin.
-   Eğer varsa, sonuçların nasıl değerlendirilmesi gerektiğine karar verin.
-   Ek özellikler gerek olup olmadığını belirleyin. Örneğin, sonuçların kategorilere ayrılıp ayrılmayacağını, nasıl kategorilere ayrılacağını, bir zaman sınırına gerek olup olmadığını veya tüm soruların zorunlu olup olmayacağını belirleyin.

Tasarım aşaması bu sırada tamamlamanız gereken görevleri dört görev kategorisi içerir:

1.  Gerektiği gibi ön koşullar ayarlayın.
2.  Eğer varsa, yanıt grupları ve cevaplar ayarlayın.
3.  Sorular ve bunların yanıt grupları ile ilişkilendirilmesini ayarlayın.
4.  Anketi ayarlayın ve sorular ekleyin.

## <a name="prerequisites"></a>Önkoşullar
Anketler, cevaplar ve sorular oluşturmadan önce bazı önkoşulların yerine getirilmesi gerekir. Ancak, tam işlevsellik için tüm önkoşullar gerekli değildir.

### <a name="required"></a>Gerekli

| Önkoşul        | Açıklama                |
|---------------------|----------------------------|
| Soru formu tipleri | Anketleri kategorilere ayırın. |
| Soru tipleri      | Soruları kategorilere ayırın.      |

### <a name="optional"></a>İsteğe bağlı

| Önkoşul             | Açıklama                                                    |
|--------------------------|----------------------------------------------------------------|
| Soru formu parametreleri | Anketler için temel denetimleri ve varsayılan ayarları değiştirin. |

### <a name="questionnaire-types"></a>Soru formu tipleri

Anket türleri gereklidir ve bir anket oluşturduğunuzda atanmalıdır. Anket türleri anketleri daha kolay yönetmenize ve sınıflandırmanıza yardımcı olur. Anketleri sınıflandırmak ve birbirinden ayırt etmek için anket türlerini kullanın. Örneğin, çok sayıda anketin içinden seçim yapmanız gerekiyorsa, belirli bir anketi bulmayı kolaylaştırmak için bunları filtreleyebilirsiniz. Aşağıda bazı anket türü örnekleri verilmiştir:

-   İnsan kaynakları gelişimi
-   Müşteri araştırmaları
-   Gözden geçirme süreci

### <a name="question-types"></a>Soru tipleri

Soru türleri gereklidir ve bir soru oluşturduğunuzda atanmalıdır. 

Raporlama için soruları kategorilere ayırmak için soru türlerini kullanın. Soru türleri aynı zamanda soruları bulmayı kolaylaştırır çünkü **Sorular** sayfasındaki türleri filtre olarak kullanabilirsiniz. Aşağıda bazı soru türü örnekleri verilmiştir:

-   İnsan kaynakları
-   İşi yönetme
-   Kurs değerlendirmesi

### <a name="questionnaire-parameters"></a>Soru formu parametreleri

Anket parametreleri isteğe bağlıdır. Şirketinizin gereksinimlerine bağlı olarak, onları kullanmayabilirsiniz. 

Anket parametreleri bir anketin gizliliğini, numara seri kodlarını ve referans türlerini tanımlar. Bir kuruluş bir anket dağıttığında, yanıtlayanların gizli kalması seçeneği söz konusu olabilir. 

Numara seri kodları sorular ve yanıtlar düzenlemek için kullanılır. Bu numara serisi kodlarına bağlı olarak, değerler öğelere otomatik olarak atanır. 

Verilerinizi oluşturmaya başlamadan önce tüm parametreleri tanımlamanız gerekir. Anket parametre ayarlarını istediğiniz zaman değiştirebilirsiniz.

## <a name="questionnaire-components"></a>Anket bileşenleri
Soru formlar üç ana öğeden oluşur: çoktan seçmeli sorular için cevapları içeren cevap grupları, sorular ve soru formunun kendisi. İsteğe bağlı olarak, bir soru formundaki soruları sonuç sayfalarına da gruplandırabilirsiniz. Sonuç grupları soruları kategorilere ayırmanızı sağlar ve anket hakkında daha fazla analiz sağlar. 

[![QuestionnaireComponents.](./media/questionnairecomponents-1024x615.png)](./media/questionnairecomponents.png)

### <a name="answer-groups-and-answers"></a>Yanıt grupları ve yanıtlar

Yanıtlayanlar sorunun konusuna bağlı olarak, bir soruyu iki şekilde yanıtlayabilir:

-   Açık uçlu soruların belirli bir biçimde yanıt gerektirmez. Yanıtlayanlar yanıtı bir metin, sayı veya tarih ya da saat olarak yazabilir. Bu sorular genellikle yanıtlayanın cevabında bir fikir, tanım, değerlendirme veya tahmin gibi öznel bilgiler sağlamasını gerektirir.
-   Kapalı uçlu sorular, yanıtlayanın olası doğru cevap listesindeki bir yanıtı seçmesini gerektirir.

Kapalı-uçlu sorular için olası yanıt listesi sağlamak için, cevapları **Yanıt grupları** sayfasında oluşturabilirsiniz. 

Yanıt grupları ve yanıtlar soruların oluşturulduğu bilgilerin ana gövdesini oluşturan bileşenlerdir. Bir yanıt grubu oluşturduktan sonra, yanıt grubunu **Sorular** sayfasındaki **Yanıt grubu** alanındaki bir soruyla ilişkilendirebilirsiniz. 

Bir yanıt grubu aynı anketteki birden çok soru için kullanılabilir ve aynı zamanda birden çok anket üzerinde kullanılabilir. 

> [!NOTE]
> Tamamlanmış anketlerde zaten kullanılmış olarak bir yanıt grubundaki yanıt metnini değiştirirseniz veriyi değerlendirmek zorlaşabilir ve anket sonuçları geçersiz olabilir. Bir yanıt grubunu değiştirmeniz gerekiyorsa varo lanı değiştirmek yerine yeni bir yanıt grubu oluşturmayı göz önünde bulundurun. Bir soruya veya yanıta eklenmiş olan veya yanıtlanmış olan yanıt gruplarını silemezsiniz.

### <a name="questions"></a>Sorular

Bir anket sorular içermelidir. Sorular, açık uçlu veya kapalı uçlu olabilir.

-   Açık uçlu soruların yanıtları kontrol edilmez ve yanıtlayanlar kendi cevaplarını yazabilir.
-   Kapalı uçlu soruların önceden tanımlanmış yanıt seçenekleri listesi olması gerekir ve sorular yanıtlayanın çok sayıda yanıtı seçebileceği şekilde oluşturulmalıdır. Sorular yanıtlayandan belirli bilgiler alacak şekilde tasarlanmalıdır ve her kapalı uçlu soru için yanıt seçenekleri sağlayan bir yanıt grubuyla bağlanmalıdır. 

    > [!NOTE]
    > Kapalı uçlu sorular belirlemeden önce yanıt grupları ve yanıtlar oluşturmalısınız.

Sorular koşullu soru hiyerarşisi içinde düzenlenebilir, böylece ikincil sorular yanıtlayanın önceki soru için seçtiği cevaba bağlıdır. Önce soruları yazıp ardından bunları daha sonra hiyerarşiye göre düzenleyebilirsiniz.

## <a name="setting-up-questionnaires"></a>Anketler ayarlama

> [!NOTE]
> Bir anket ayarlamadan önce yanıtları, soruları ve önkoşulları ayarlamanız gerekir. 

Her anket için, aşağıdaki bilgileri belirtebilirsiniz:

-   Zorunlu soruları yanıtlamak için geçerli olan toplam süre veya süre sınırı.
-   Tüm soruların zorunlu olup olmadığı.
-   Bir anketteki maksimum puan sayısının hesaplanıp hesaplanmayacağı.
-   Sonuçların kategorilere nasıl ayrılacağı.
-   Anketin kısıtlı bir yanıtlayan kümesi için geçerli olup olmayacağı.
-   Bir form şablonunun soru formundaki her sayfanın arkasında bir arka plan olarak görüntülenip görüntülenmeyeceği.
-   Yanıtlayanlar için anketin içeriğini netleştirmek üzere ek notların gerekli olup olmayacağı.
-   Soruların belirlenmiş bir sıraya göre veya bir havuzdan gelişigüzel seçerek görüntüleneceği.
-   Soruların yalnızca önceki yanıtlar için belirli cevaplar verildiğinde sorulması.

### <a name="set-up-a-questionnaire"></a>Bir anket ayarlayın

Bir anket ayarlamak için kullandığınız birincil sayfa **Anketler** sayfasıdır. Bir anket ayarlamak için, aşağıdaki görevleri sırasıyla tamamlayın:

1.  Bir anket oluşturun.
2.  Ankete sorular eklemek için şu adımlardan birini izleyin:
    -   Sonuç grupları kullanıyorsanız, sonuç gruplarını kullanarak bir ankete sorular ekleyebilirsiniz. Öncelikle anket için sonuç gruplarını ayarlayın, ve ardından sonuç gruplarına soru ekleyin.
    -   Sonuç grupları kullanmıyorsanız, ankete doğrudan sorular ekleyebilirsiniz.

3.  Eğer gerekiyorsa, koşullu soru hiyerarşisi ayarlayın.
4.  Anketi test edin.

**Anketler** sayfasında, anketin doğru şekilde derlenip derlenmediğini test etmek için **Doğrula** seçeneğine tıklayın. Ancak, bir anketi dağıtmadan önce anketi tamamlamak ve kendiniz test etmek iyi bir fikirdir.

### <a name="modify-a-questionnaire"></a>Bir anketi değiştirin

**Anketler** sayfasında aşağıdaki görevleri tamamlayabilirsiniz:

-   Anketteki sonuç grupları ve sorular gibi bilgileri değiştirin.
-   Soru silin ve ekleyin.
-   Sonuç gruplarında ve numara serisinde değişiklikler yapmak. 

> [!CAUTION]
> Yanıtlanmış olan anketleri değiştirirken dikkatli olun. Değişiklikler istatistiklerin doğruluğunu azaltabilir ve bu nedenle onları değerlendirme açısından zayıf bir temel yapar. Yanıtlanmış olan bir soruyu değiştirmek yerine yeni bir soru oluşturmayı düşünün.

Bir ankette, aşağıdaki soru türlerini silemezsiniz:

-   Bir ankete eklenmiş olan sorular
-   Daha önceden yanıtlanmış olan ve bu nedenle **Cevaplar** iletişim kutusunda görünen sorular.

### <a name="result-groups"></a>Sonuç grupları

Bir ankete sorular eklediğinizde sonuç grupları isteğe bağlıdır. 

Bir sonuç grubu puanları hesaplamak ve bir anketin sonuçlarını kategorilere ayırmak için kullanılır. Sonuç grupları kullanırsanız, aşağıdaki görevleri gerçekleştirebilirsiniz:

-   Puan istatistiklerini temel alarak anket sonuçlarını değerlendirin.
-   Ayarladığınız her sonuç grubu için bir yanıtlayanın puanını değerlendirin.
-   Sonuçları analiz etmenize yardımcı olması için her sonuç grubu için istatistikler oluşturmak.
-   Her sonuç grubu için sonuçları gösteren bir rapor ve aynı zamanda her sonuç grubunda kazanılan puanlara dayanan isteğe bağlı puanları/metinleri yazdırın.

> [!NOTE]
> Sonuç grupları ayarlamadan önce aşağıdaki görevleri tamamlamanız gerekir:

-   Kapalı uçlu soruları ayarlayın. Kapalı uçlu bir soru için, **Sorular** sayfasındaki giriş türü **Onay kutusu**, **Alternatif düğme** veya **Birleşik giriş kutusu** olmalıdır.
-   Her soruya atanmış olan yanıt grubundaki yanıtlar için puanları tanımlayın.
-   Bir anket ayarlayın.

Bir ankete sonuç gruplarını kullanarak sorular eklemek için, öncelikle anket için sonuç gruplarını ayarlayın ve sonra sonuç gruplarına sorular ekleyin. Sonuç grupları kullanmıyorsanız, bir ankete doğrudan sorular ekleyebilirsiniz. 

Yanıtlayanın her kategoride kazandığı puanları değerlendirmek için birden fazla sonuç grubu ayarlayabilirsiniz. Bir anket tamamlandıktan sonra, her sonuç grubu için elde edilen puanları görüntüleyebilirsiniz. 

> [!TIP]
> Bir anketi ayrı kategoriler yerine puanları kullanarak değerlendirmek için tüm soruları tek bir sonuç grubuna ekleyebilirsiniz. 

Her bir sonuç grubu için yanıtlayanların bir anketi tamamladıktan sonra aldıkları bir veya daha fazla puan tabanlı mesaj ekleyebilirsiniz. Görüntülenen metin, yanıtlayanın bir sonuç grubunda elde ettiği puana göre değişebilir. Puan tabanlı mesajları kullanmak için, puan aralıkları ve her aralık için bir açıklama tanımlamalısınız. Yanıtlayan belirli bir aralıkta bir puan aldığında, aralık için metin, sonuç raporuna eklenir. 

Bir sonuç grubu bir anketteki belirli soru gruplarıyla ilişkili olan puanlarla ilgili olduğundan, bir anket için yalnızca belirli bir sonuç grubu kullanabilirsiniz.

#### <a name="example-pointstexts-for-result-group-3"></a>Örnek: Sonuç grubu 3 için puanlar/metinler

Üç kategoride 15 sorudan oluşan bir liderlik testi için bir anket kullanıyorsunuz. Üç sonuç grubu oluşturun ve her sonuç grubuna beş soru ekleyin. Puanlar daha sonra üç grupta toplanır. Üç sonuç grubu aşağıdaki gibidir:

-   Yaratıcı yetenekler
-   Liderlik yetenekleri
-   Teknik yetenekler

Puan tabanlı mesajları kullanmak için, her sonuç grubu için metin aralıkları ayarlayın. Her soruya iki puan atanır. Bu nedenle, her sonuç grubundaki maksimum puan toplamı 10'dur. 

Aşağıdaki tablo "liderlik yetenekleri" sonuç grubu için tanımladığınız puan tabanlı mesajları gösterir.

| Puan aralığı | Açıklama eki                                       |
|----------------|--------------------------------------------|
| 1-3 arası         | Ortalama liderlik yetenekleriniz var.     |
| 4-7 arası         | İyi liderlik yetenekleriniz var.        |
| 8 -10 arası        | Çok iyi liderlik yetenekleriniz var. |

Bir anketteki her sonuç grubu için puan aralıkları ve metinler ayarlayabilirsiniz. Her yanıtlayan puanına karşılık gelen metinler her bir sonuç grubu için görüntülenir. 

> [!NOTE]
> Aralıkları ve metinleri değiştirebilirsiniz. Ancak bir anket tamamlanmışsa, değişiklikler eski ve yeni sonuç raporları arasında farklılıklara neden olabilir.

### <a name="conditional-question-hierarchies"></a>Koşullu soru hiyerarşileri

Koşullu soru hiyerarşileri, bir anketi kurduğunuz sırada isteğe bağlıdır. 

> [!NOTE]
> Koşullu soru hiyerarşisi ayarlamadan önce ankete atanmış yanıt grupları olan sorular eklemelisiniz. 

Bir ankette bir soru hiyerarşisi oluşturmak için koşullu sorular kullanmak için, sırayı soruların yanıtlayanın her soru için seçeceği cevaba dayanarak sunulacağı şekilde oluşturabilirsiniz. Soru sırasını yanıtlayanın cevabına dayanacak şekilde oluşturarak, yanıtlayan anketi tamamladığında anketi değiştirebilirsiniz.

#### <a name="examples"></a>Örnekler

Tüzel kişilik müşterilerine hem öğeler hem de hizmetler sunar. Bu gibi durumlarda genellikle olduğu gibi, bazı müşteriler yalnızca öğeleri satın alırken, bazıları yalnızca hizmetleri ve bazıları da hem öğeleri hem hizmetleri satın alır. Bu nedenle, tüzel kişilik bir müşteri memnuniyeti anketi dağıttığında, ankete koşullu bir yapı uygular, böylece yalnızca hizmetleri satın alan müşterilerin öğeler hakkındaki soruları yanıtlaması gerekmez. 

Alternatif olarak, bir yanıtlayan soru 1 için cevap A'yı seçtiğinde soru sırasında soru 2'nin gelmesini sağlamak için bir anket ayarlayın. Ancak yanıtlayan soru 1 için cevap B'yi seçerse, sıradaki soru soru 5'tir.

[!INCLUDE[footer-include](../includes/footer-banner.md)]