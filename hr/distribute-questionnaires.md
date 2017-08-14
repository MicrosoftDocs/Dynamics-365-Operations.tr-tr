---
title: "Bir anketi dağıtın ve tamamlayın."
description: "Bu konu, tasarladığınız anketlerin onları tamamlayacak kişi veya kişi grubu için kullanılabilir olması için onları nasıl dağıtacağınızı açıklar."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: b2b1b99fd4c7c439ad89440827ad78173d371855
ms.openlocfilehash: c3afd12ed82935cd3d4b1c4ebeab62892cfe7178
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---

# <a name="distribute-and-complete-a-questionnaire"></a>Bir anketi dağıtın ve tamamlayın.

[!include[banner](includes/banner.md)]


Bu konu, tasarladığınız anketlerin onları tamamlayacak kişi veya kişi grubu için kullanılabilir olması için onları nasıl dağıtacağınızı açıklar. 

Bir anketi dağıtmanın birden çok yolu vardır:

-   Anketi aktif olarak işaretleyin. Ardından anket, erişimi kısıtlamak için bir anket grubu ayarlanmadığı sürece tüm çalışanlar tarafından kullanılabilir.
-   Bir anket grubuna haklar atayın. Anket daha sonra seçili grubun tüm üyeleri tarafından kullanılabilir.
-   Planlı yanıt oturumları oluşturun. Anket daha sonra yalnızca belirli bir kişi tarafından kullanılabilir.
-   Bir planlama oluşturun. Anket daha sonra birden çok kişi tarafından kullanılabilir.

## <a name="marking-a-questionnaire-as-active"></a>Anketi aktif olarak işaretlemek.
**Soru formları** sayfasındaki **Etkin** alanı **Evet** olarak ayarlayarak, soru formlarını tüm personelin tamamlamaları üzere kullanılabilir hale getirirsiniz. Yanıtlayanlar, soru formunu birden çok kez tamamlayabilirler. Bu işlev, yıl boyunca sürekli geribildirim toplamak istiyorsanız yararlıdır. Örneğin, çalışanların kafeteryadaki öğle yemeği hizmeti hakkında geribildirim vermek için kullanacağı bir anket yapabilirsiniz.

## <a name="questionnaire-groups"></a>Soru formu grupları
Anket grupları ayarlayabilir ve ardından anketin dağıtılması gereken yanıtlayanları ekleyebilirsiniz. 

Aşağıdaki sayfalardan anket grupları oluşturabilirsiniz:

-   **Anket grupları**– Yalnızca bir anket grubundaki bireyler seçili anketi tamamlayabilir. Örneğin, hedef kitleniz yüklenicilerse, bu yanıtlayanlara özel bir anket grubu oluşturursunuz.
-   **Anket grubu üyeleri** – Anket gruplarına kişiler ekleyebilirsiniz.

Bir soru formu grubunu bir soru formuna eklemek için **Soru formları** sayfasında, **Kullanıcı hakları** üzerine tıklayın. Soru formu etkin olarak kaydedildikten sonra, soru formu grubunun üyeleri, soru formunu tamamlayabilirler. Bu işlev, bir soru formunu daha büyük bir gruba açmadan önce seçili kişiler grubunda denemek istiyorsanız veya bir soru formunu çok özel bir hedef kitleye hedeflemek istiyorsanız yararlıdır.

## <a name="planned-answer-sessions-in-a-questionnaire"></a>Soru formu başına planlanan yanıt oturumu
Planlı yanıt oturumları tasarladığınız ve yanıtlayanlarını seçtiğiniz anketlerdir. 

> **Not** Planlı yanıt oturumları ayarlamadan önce bir anket tasarlamalısınız. 

**Planlı yanıt oturumu** sayfasında, tek bir çalışan için planlı bir yanıt oturumu oluşturabilirsiniz. Sayfadaki liste tüm planlı anketleri görüntüler. 

Planlı yanıt oturumları aynı zamanda **Anket planlamaları** sayfasında kullanılır, burada birden çok kişi için anketler planlayabilirsiniz:

-   Çalışanlar
-   Kurs katılımcıları
-   Organizasyon birimleri

Herkes anketi yalnızca bir kez yanıtlayabilir.

## <a name="scheduling-a-questionnaire"></a>Bir anket planlama
Birden fazla yanıtlayan için isteğe bağlı olarak bir anket planlayabilirsiniz.

### <a name="planning-types"></a>Planlama tipleri

Birden fazla yanıtlayan için planlı yanıt oturumları planlamak istiyorsanız planlama türleri gereklidir. Planlama tipleri, anket planlamalarını sınıflandırmak için kullanılır. Örneğin, aşağıdaki amaçlarla anketler planlayabilirsiniz:

-   Değerlendirme
-   Anket
-   Test etme

Bir naket planlaması için planlama türlerini **Anket planlamaları** sayfasında belirtebilirsiniz.

### <a name="reference-types-for-questionnaire"></a>Anket için referans türleri

Bir anket planlarken seçebileceğiniz yanıtlayanlar için ölçütleri girmek için referans türlerini kullanabilirsiniz. 

**Referans türleri** sayfasını kullanarak bir anket için referans türleri ayarlayın. Her referans türü Microsoft Dynamics 365 for Finance and Operations'ta bir tabloya karşılık gelir. Anket planlamaları oluşturduğunuzda, anketin ilişkilendirileceği bir dizi kayıt veya tek tek kayıtları belirtebilirsiniz. 

Örneğin, kurslar tablo seçerseniz, anketin hangi özel kurs için olacağına karar verebilirsiniz. Kurslar tablosu için bir referans belirlerken, **Kurslar** sayfasındaki bazı alanlar ve düğmeler kullanılabilir hale gelir.

### <a name="questionnaire-schedules"></a>Soru formu planlamaları

Soru formu tablolarını, bir kullanıcı grubu için bir referans türüne dayalı olarak çoklu planlı yanıt oturumları oluşturmak için kullanabilirsiniz. **Soru formu tabloları** sayfasında zamanlamayı oluşturmak. Zamanlamayı kategorize etmek için planlama türünü ve sistemi, belirli kullanıcılar için sorgulamak üzere referans türünü seçin. Örneğin, referans türünü Kurslar tablosu olarak ayarlarsanız, **Referans** alanında belirli bir kursu seçebilirsiniz. 

Anketi ve diğer ölçütleri seçmek için **Kurulum ayrıntıları** seçeneğini tıklatın. Örneğin, soru formu bir eğitmenin değerlendirmesiyse, eğitmenin adını bir kriter olarak belirleyin. Kurulum ayarlarını girmeyi bitirdikten sonra, sistem planlanmış yanıtlama oturumlarını, bu sorguya dahil edilmiş kullanıcılar için oluşturur. 

Bir zamanlama için yanıt oturumlarını görüntülemek için **Planlı yanıt oturumları** seçeneğini tıklatın. Ardından ek planlı yanıt oturumlarını el ile oluşturabilir veya yanıtlanmamış olan planlı yanıt oturumlarını silebilirsiniz. 

Anketi ilgili planlı yanıt oturumlarındaki kullanıcılar için kullanılabilir hale getirmek için **İşlevler** &gt; **Başlat** seçeneğini tıklatın. Anketin tamamlanmış yanıtlarını görüntülemek için **Yanıtlar** seçeneğini tıklatın. İsteğe bağlı olarak, anket zamanlama ayarlarını, Planlı yanıt oturumlarını ve yeni bir anket zamanlama yanıtlarını kopyalayabilirsiniz.

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a>Yanıtlayanları onlar için kullanılabilir olan anketler hakkında bilgilendirin
Bir anketi dağıttığınızda, yanıtlayanları anketlerin onlar için kullanılabilir olduğu hakkında bilgilendirmelisiniz. 

### <a name="notifying-respondents-about-a-planned-answer-session"></a>Yanıtlayanları planlı bir yanıt oturumu hakkında bilgilendirin

Planlı bir yanıt oturumu kullanıyorsanız, kişiyi telefon ya da e-postayla doğrudan bilgilendirmeniz gerekir.

### <a name="notifying-respondents-about-a-scheduling"></a>Yanıtlayanları bir planlama hakkında bilgilendirin

Bir ankete atanmış olan tüm yanıtlayanlara bir e-posta hazırlamak ve göndermek için **Anket planlamaları** sayfasını kullanın. E-postayı **Çalışan self-servis için e-posta** sekmesinde girin. Zamanlama başladıktan sonra yanıt verenlere e-postalar oluşturmak ve göndermek için **İşlevler** &gt; **E-posta gönder** üzerine tıklayın. Yanıtlayanlar web sitesinde oturum açarak soru formunu doldurabilirler. 

> **Not** E-posta işlevlerini kullanmadan önce BT yöneticiniz e-posta ayarlarını **E-posta parametreleri** sayfasında girmelidir.

## <a name="ending-a-scheduled-questionnaire"></a>Planlanmış bir anketi sonlandırma
Tüm yanıtlayan kişiler kendilerine atanmış soru oturumlarını tamamladıktan sonra çizelgelenmiş bir soru formunu sonlandırabilirsiniz. Planlamış bir anket sonlandırıldıktan sonra, ayarlarını yeni bir planlamaya kopyalayamazsınız. 

> **Not** Bir veya daha fazla yanıtlayan anketi tamamlamadıysa, buna rağmen planlamayı sonlandırmak istiyorsanız, öncelikle bu yanıtlayanları  **Planlı yanıt oturumu** sayfasından silmeniz gerekir. Ardından planlamayı sonlandırabilirsiniz.

## <a name="completing-questionnaires"></a>Soru formlarını tamamlama
Bir anketi tasarladıktan ve dağıttıktan sonra, anket seçili yanıtlayanlar tarafından tamamlanabilir. İki yerleşimden kullanabileceğiniz soru formlarını tamamlayabilirsiniz:

-   Gezinti bölmesinde **Anketler** &gt; **Dağıt** &gt; **Bir anketi tamamlamak** seçeneğini tıklatın.
-   Çalışan Self-Servisinde **Tamamlanacak anketler** seçeneğini tıklatın.

Anketler belirli kullanıcılar veya kullanıcı grupları ya da bir ağdaki tüm kullanıcılar için kullanıma sunulabilir.

<a name="see-also"></a>Ayrıca bkz.
--------

[Soru formları tasarlama](design-questionnaires.md)

[Soru formlarını kullanma](questionnaires.md)

[Soru formlarının sonuçlarını görüntüleyin ve değerlendirin](evaluate-questionnaire-results.md)



<a name=""></a>=======
---
# <a name="required-metadata"></a>gerek meta veri

başlık: Bir anketi dağıtmak ve tamamlamak açıklama: Bu konu, tasarladığınız anketlerin onları tamamlayacak kişi veya kişi grubu için kullanılabilir olması için onları nasıl dağıtacağınızı açıklar. yazar: twheeloc yönetici: AnnBe ms.date: 06/20/2017 ms.topic: makale ms.prod: ms.service: Dynamics365Operations ms.technology: 

# <a name="optional-metadata"></a>isteğe bağlı meta veriler

ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
# <a name="robots"></a>ROBOTLAR: 
hedef kitle: Uygulama Kullanıcısı
# <a name="msdevlang"></a>ms.devlang: 
ms.reviewer: twheeloc ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
# <a name="mstgtpltfrm"></a>ms.tgt_pltfrm: 
ms.custom: 17424 ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470 ms.search.region: Global
# <a name="mssearchindustry"></a>ms.search.industry: 
MS.Author: twheeloc ms.search.validFrom: 2016-02-28 ms.dyn365.ops.version: 7.0.0, beceri AX Temmuz 2017 güncelleştir

---

# <a name="distribute-and-complete-a-questionnaire"></a>Soru formunu dağıtma ve doldurma

Bu konu, tasarladığınız anketlerin onları tamamlayacak kişi veya kişi grubu için kullanılabilir olması için onları nasıl dağıtacağınızı açıklar. 

Bir anketi dağıtmanın birden çok yolu vardır:

-   Anketi aktif olarak işaretleyin. Ardından anket, erişimi kısıtlamak için bir anket grubu ayarlanmadığı sürece tüm çalışanlar tarafından kullanılabilir.
-   Bir anket grubuna haklar atayın. Anket daha sonra seçili grubun tüm üyeleri tarafından kullanılabilir.
-   Planlı yanıt oturumları oluşturun. Anket daha sonra yalnızca belirli bir kişi tarafından kullanılabilir.
-   Bir planlama oluşturun. Anket daha sonra birden çok kişi tarafından kullanılabilir.

## <a name="marking-a-questionnaire-as-active"></a>Anketi aktif olarak işaretlemek.
**Soru formları** sayfasındaki **Etkin** alanı **Evet** olarak ayarlayarak, soru formlarını tüm personelin tamamlamaları üzere kullanılabilir hale getirirsiniz. Yanıtlayanlar, soru formunu birden çok kez tamamlayabilirler. Bu işlev, yıl boyunca sürekli geribildirim toplamak istiyorsanız yararlıdır. Örneğin, çalışanların kafeteryadaki öğle yemeği hizmeti hakkında geribildirim vermek için kullanacağı bir anket yapabilirsiniz.

## <a name="questionnaire-groups"></a>Soru formu grupları
Anket grupları ayarlayabilir ve ardından anketin dağıtılması gereken yanıtlayanları ekleyebilirsiniz. 

Aşağıdaki sayfalardan anket grupları oluşturabilirsiniz:

-   **Anket grupları**– Yalnızca bir anket grubundaki bireyler seçili anketi tamamlayabilir. Örneğin, hedef kitleniz yüklenicilerse, bu yanıtlayanlara özel bir anket grubu oluşturursunuz.
-   **Anket grubu üyeleri** – Anket gruplarına kişiler ekleyebilirsiniz.

Bir soru formu grubunu bir soru formuna eklemek için **Soru formları** sayfasında, **Kullanıcı hakları** üzerine tıklayın. Soru formu etkin olarak kaydedildikten sonra, soru formu grubunun üyeleri, soru formunu tamamlayabilirler. Bu işlev, bir soru formunu daha büyük bir gruba açmadan önce seçili kişiler grubunda denemek istiyorsanız veya bir soru formunu çok özel bir hedef kitleye hedeflemek istiyorsanız yararlıdır.

## <a name="planned-answer-sessions-in-a-questionnaire"></a>Soru formu başına planlanan yanıt oturumu
Planlı yanıt oturumları tasarladığınız ve yanıtlayanlarını seçtiğiniz anketlerdir. 

**Not:** Planlı yanıt oturumları ayarlamadan önce bir anket tasarlamalısınız. 

**Planlı yanıt oturumu** sayfasında, tek bir çalışan için planlı bir yanıt oturumu oluşturabilirsiniz. Sayfadaki liste tüm planlı anketleri görüntüler. 

Planlı yanıt oturumları aynı zamanda **Anket planlamaları** sayfasında kullanılır, burada birden çok kişi için anketler planlayabilirsiniz:

-   Çalışanlar
-   Kurs katılımcıları
-   Organizasyon birimleri

Herkes anketi yalnızca bir kez yanıtlayabilir.

## <a name="scheduling-a-questionnaire"></a>Bir anket planlama
Birden fazla yanıtlayan için isteğe bağlı olarak bir anket planlayabilirsiniz.

### <a name="planning-types"></a>Planlama tipleri

Birden fazla yanıtlayan için planlı yanıt oturumları planlamak istiyorsanız planlama türleri gereklidir. Planlama tipleri, anket planlamalarını sınıflandırmak için kullanılır. Örneğin, aşağıdaki amaçlarla anketler planlayabilirsiniz:

-   Değerlendirme
-   Anket
-   Test etme

Bir naket planlaması için planlama türlerini **Anket planlamaları** sayfasında belirtebilirsiniz.

### <a name="reference-types-for-questionnaire"></a>Anket için referans türleri

Bir anket planlarken seçebileceğiniz yanıtlayanlar için ölçütleri girmek için referans türlerini kullanabilirsiniz. 

**Referans türleri** sayfasını kullanarak bir anket için referans türleri ayarlayın. Her referans türü Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'da bir tabloya karşılık gelir. Anket planlamaları oluşturduğunuzda, anketin ilişkilendirileceği bir dizi kayıt veya tek tek kayıtları belirtebilirsiniz. 

Örneğin, kurslar tablo seçerseniz, anketin hangi özel kurs için olacağına karar verebilirsiniz. Kurslar tablosu için bir referans belirlerken, **Kurslar** sayfasındaki bazı alanlar ve düğmeler kullanılabilir hale gelir.

### <a name="questionnaire-schedules"></a>Soru formu planlamaları

Soru formu tablolarını, bir kullanıcı grubu için bir referans türüne dayalı olarak çoklu planlı yanıt oturumları oluşturmak için kullanabilirsiniz. **Soru formu tabloları** sayfasında zamanlamayı oluşturmak. Zamanlamayı kategorize etmek için planlama türünü ve sistemi, belirli kullanıcılar için sorgulamak üzere referans türünü seçin. Örneğin, referans türünü Kurslar tablosu olarak ayarlarsanız, **Referans** alanında belirli bir kursu seçebilirsiniz. 

Anketi ve diğer ölçütleri seçmek için **Kurulum ayrıntıları** seçeneğini tıklatın. Örneğin, soru formu bir eğitmenin değerlendirmesiyse, eğitmenin adını bir kriter olarak belirleyin. Kurulum ayarlarını girmeyi bitirdikten sonra, sistem planlanmış yanıtlama oturumlarını, bu sorguya dahil edilmiş kullanıcılar için oluşturur. 

Bir zamanlama için yanıt oturumlarını görüntülemek için **Planlı yanıt oturumları** seçeneğini tıklatın. Ardından ek planlı yanıt oturumlarını el ile oluşturabilir veya yanıtlanmamış olan planlı yanıt oturumlarını silebilirsiniz. 

Anketi ilgili planlı yanıt oturumlarındaki kullanıcılar için kullanılabilir hale getirmek için **İşlevler** &gt; **Başlat** seçeneğini tıklatın. Anketin tamamlanmış yanıtlarını görüntülemek için **Yanıtlar** seçeneğini tıklatın. İsteğe bağlı olarak, anket zamanlama ayarlarını, Planlı yanıt oturumlarını ve yeni bir anket zamanlama yanıtlarını kopyalayabilirsiniz.

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a>Yanıtlayanları onlar için kullanılabilir olan anketler hakkında bilgilendirin
Bir anketi dağıttığınızda, yanıtlayanları anketlerin onlar için kullanılabilir olduğu hakkında bilgilendirmelisiniz. 

**Not:** Yanıtlayanların bir anketi tamamlaması için Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition'daki kullanıcılar olması gerekir.

### <a name="notifying-respondents-about-a-planned-answer-session"></a>Yanıtlayanları planlı bir yanıt oturumu hakkında bilgilendirin

Planlı bir yanıt oturumu kullanıyorsanız, kişiyi telefon ya da e-postayla doğrudan bilgilendirmeniz gerekir.

### <a name="notifying-respondents-about-a-scheduling"></a>Yanıtlayanları bir planlama hakkında bilgilendirin

Bir ankete atanmış olan tüm yanıtlayanlara bir e-posta hazırlamak ve göndermek için **Anket planlamaları** sayfasını kullanın. E-postayı **Çalışan self-servis için e-posta** sekmesinde girin. Zamanlama başladıktan sonra yanıt verenlere e-postalar oluşturmak ve göndermek için **İşlevler** &gt; **E-posta gönder** üzerine tıklayın. Yanıtlayanlar web sitesinde oturum açarak soru formunu doldurabilirler. 

**Not:** E-posta işlevlerini kullanmadan önce BT yöneticiniz e-posta ayarlarını **E-posta parametreleri** sayfasında girmelidir.

## <a name="ending-a-scheduled-questionnaire"></a>Planlanmış bir anketi sonlandırma
Tüm yanıtlayan kişiler kendilerine atanmış soru oturumlarını tamamladıktan sonra çizelgelenmiş bir soru formunu sonlandırabilirsiniz. Planlamış bir anket sonlandırıldıktan sonra, ayarlarını yeni bir planlamaya kopyalayamazsınız. 

**Not:** Bir veya daha fazla yanıtlayan anketi tamamlamadıysa, buna rağmen planlamayı sonlandırmak istiyorsanız, öncelikle bu yanıtlayanları  **Planlı yanıt oturumu** sayfasından silmeniz gerekir. Ardından planlamayı sonlandırabilirsiniz.

## <a name="completing-questionnaires"></a>Soru formlarını tamamlama
Bir anketi tasarladıktan ve dağıttıktan sonra, anket seçili yanıtlayanlar tarafından tamamlanabilir. İki yerleşimden kullanabileceğiniz soru formlarını tamamlayabilirsiniz:

-   Gezinti bölmesinde **Anketler** &gt; **Dağıt** &gt; **Bir anketi tamamlamak** seçeneğini tıklatın.
-   Çalışan Self-Servisinde **Tamamlanacak anketler** seçeneğini tıklatın.

Anketler belirli kullanıcılar veya kullanıcı grupları ya da bir ağdaki tüm kullanıcılar için kullanıma sunulabilir.

<a name="see-also"></a>Ayrıca bkz.
--------

[Soru formları tasarlama](design-questionnaires.md)

[Soru formlarını kullanma](questionnaires.md)

[Soru formlarının sonuçlarını görüntüleyin ve değerlendirin](evaluate-questionnaire-results.md)

ana

