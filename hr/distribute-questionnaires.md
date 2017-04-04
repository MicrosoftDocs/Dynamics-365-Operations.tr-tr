---
title: "Bir anketi dağıtın ve tamamlayın."
description: "Bu konu açıklar nasıl kişi veya grup kişilerin bunları tamamlamak için kullanılabilir olduklarından emin, tasarım, soru formu dağıtmak."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: a76ec0cd86bcc810b42ae3cd8efd8a584e6c4da3
ms.openlocfilehash: 8e09c6b042d557e3b2d608fb5e278169fc3c1d88
ms.lasthandoff: 03/31/2017


---

# <a name="distribute-and-complete-a-questionnaire"></a>Bir anketi dağıtın ve tamamlayın.

Bu konu açıklar nasıl kişi veya grup kişilerin bunları tamamlamak için kullanılabilir olduklarından emin, tasarım, soru formu dağıtmak. 

Bir anketi dağıtmanın birden çok yolu vardır:

-   Anketi aktif olarak işaretleyin. Ardından anket, erişimi kısıtlamak için bir anket grubu ayarlanmadığı sürece tüm çalışanlar tarafından kullanılabilir.
-   Bir anket grubuna haklar atayın. Anket daha sonra seçili grubun tüm üyeleri tarafından kullanılabilir.
-   Planlı yanıt oturumları oluşturun. Anket daha sonra yalnızca belirli bir kişi tarafından kullanılabilir.
-   Bir planlama oluşturun. Anket daha sonra birden çok kişi tarafından kullanılabilir.

## <a name="marking-a-questionnaire-as-active"></a>Anketi aktif olarak işaretlemek.
Ayarlayarak **etkin** alanı **Evet** üzerinde **soru** sayfasında kullanılabilir duruma getirdiğiniz soru formunu tamamlamak tüm çalışanlar için. Yanıt verenlerin anketi birden çok kez tamamlayabilirsiniz. Bu işlev, yıl boyunca sürekli geribildirim toplamak istiyorsanız yararlıdır. Örneğin, çalışanların kafeteryadaki öğle yemeği hizmeti hakkında geribildirim vermek için kullanacağı bir anket yapabilirsiniz.

## <a name="questionnaire-groups"></a>Soru formu grupları
Anket grupları ayarlayabilir ve ardından anketin dağıtılması gereken yanıtlayanları ekleyebilirsiniz. 

Aşağıdaki sayfalardan anket grupları oluşturabilirsiniz:

-   **Anket grupları **– Yalnızca bir anket grubundaki bireyler seçili anketi tamamlayabilir. Örneğin, hedef kitleniz yüklenicilerse, bu yanıtlayanlara özel bir anket grubu oluşturursunuz.
-   **Anket grubu üyeleri** – Anket gruplarına kişiler ekleyebilirsiniz.

Üzerinde bir anket soru grubuna atamak için **soru** sayfasında,'ı **kullanıcı hakları**. Soru formu etkin olarak kaydedildikten sonra Anket grubunun üyeleri Soru formu tamamlayabilirsiniz. Bu işlev, bir soru formundaki bir kişi grubunu seçmek, onu daha büyük bir grup için Top önce test etmek istediğiniz veya bir soru çok özel bir izleyici kitlesine hedeflemek istediğiniz yararlı olur.

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

**Referans türleri** sayfasını kullanarak bir anket için referans türleri ayarlayın. Her başvuru türü Microsoft Dynamics 365 işlemleri için bir tablosundaki karşılık gelir. Anket planlamaları oluşturduğunuzda, anketin ilişkilendirileceği bir dizi kayıt veya tek tek kayıtları belirtebilirsiniz. 

Örneğin, kurslar tablo seçerseniz, anketin hangi özel kurs için olacağına karar verebilirsiniz. Kurslar tablosu için bir referans belirlerken, **Kurslar** sayfasındaki bazı alanlar ve düğmeler kullanılabilir hale gelir.

### <a name="questionnaire-schedules"></a>Soru formu planlamaları

Soru formu tabloları, başvuru türüne bağlı olarak bir kullanıcı grubu için birden fazla planlı yanıt oturumları oluşturmak için kullanabilirsiniz. Zamanlama oluşturmak **soru formu tabloları** sayfa. Zamanlamayı kategorize etmek için planlama türünü seçin ve ayrıca belirli kullanıcılar için sistem sorgulamak için kullanılması gereken başvuru tipi seçin. Kurslar tabloya başvuru tipi ayarlarsanız, örneğin, belirli bir kursa seçebilirsiniz **başvuru** alan. 

Anketi ve diğer ölçütleri seçmek için**Kurulum ayrıntıları** seçeneğini tıklatın. Örneğin, anket Eğitmen değerlendirilmesi ise Eğitmen adının bir ölçüt olarak belirtin. Kurulum Ayrıntıları girerek bitirdikten sonra sistem sorguda bulunan kullanıcılar için planlı yanıt oturumları oluşturur. 

Bir zamanlama için yanıt oturumlarını görüntülemek için **Planlı yanıt oturumları** seçeneğini tıklatın. Ardından ek planlı yanıt oturumlarını el ile oluşturabilir veya yanıtlanmamış olan planlı yanıt oturumlarını silebilirsiniz. 

' I **işlevler**&gt;**Başlat** soru kullanılabilir kullanıcılar ilgili planlı yanıt oturumları sağlamak için. Anketin tamamlanmış yanıtlarını görüntülemek için **Yanıtlar** seçeneğini tıklatın. İsteğe bağlı olarak, anket zamanlama ayarlarını, Planlı yanıt oturumlarını ve yeni bir anket zamanlama yanıtlarını kopyalayabilirsiniz.

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a>Yanıtlayanları onlar için kullanılabilir olan anketler hakkında bilgilendirin
Bir anketi dağıttığınızda, yanıtlayanları anketlerin onlar için kullanılabilir olduğu hakkında bilgilendirmelisiniz. 

**Not:** katılımcıların kullanıcıları Microsoft Dynamics 365 işlemlerinde bir soru formunu tamamlamak olması gerekir.

### <a name="notifying-respondents-about-a-planned-answer-session"></a>Yanıtlayanları planlı bir yanıt oturumu hakkında bilgilendirin

Planlı bir yanıt oturumu kullanıyorsanız, kişiyi telefon ya da e-postayla doğrudan bilgilendirmeniz gerekir.

### <a name="notifying-respondents-about-a-scheduling"></a>Yanıtlayanları bir planlama hakkında bilgilendirin

Bir ankete atanmış olan tüm yanıtlayanlara bir e-posta hazırlamak ve göndermek için **Anket planlamaları** sayfasını kullanın. E-postayı **Çalışan self-servis için e-posta** sekmesinde girin. Zamanlamayı başlatıldıktan sonra'ı **işlevler**&gt;**e-posta Gönder** oluşturmak ve katılımcılara e-posta göndermek için. Katılımcıların daha sonra Web sitesine oturum açmak ve soru formunu tamamlamak. 

**Not:** E-posta işlevlerini kullanmadan önce BT yöneticiniz e-posta ayarlarını **E-posta parametreleri** sayfasında girmelidir.

## <a name="ending-a-scheduled-questionnaire"></a>Planlanmış bir anketi sonlandırma
Tüm yanıtlayan kişiler kendilerine atanmış soru oturumlarını tamamladıktan sonra çizelgelenmiş bir soru formunu sonlandırabilirsiniz. Planlamış bir anket sonlandırıldıktan sonra, ayarlarını yeni bir planlamaya kopyalayamazsınız. 

**Not:** Bir veya daha fazla yanıtlayan anketi tamamlamadıysa, buna rağmen planlamayı sonlandırmak istiyorsanız, öncelikle bu yanıtlayanları  **Planlı yanıt oturumu** sayfasından silmeniz gerekir. Ardından planlamayı sonlandırabilirsiniz.

## <a name="completing-questionnaires"></a>Soru formlarını tamamlama
Bir anketi tasarladıktan ve dağıttıktan sonra, anket seçili yanıtlayanlar tarafından tamamlanabilir. İki yerleşimden kullanabileceğiniz soru formlarını tamamlayabilirsiniz:

-   Gezinti Bölmesi'nde,'ı **soru**&gt;**Dağıt**&gt;**bir soru formunu tamamlamak**.
-   Çalışan Self-Servisinde **Tamamlanacak anketler** seçeneğini tıklatın.

Anketler belirli kullanıcılar veya kullanıcı grupları ya da bir ağdaki tüm kullanıcılar için kullanıma sunulabilir.

<a name="see-also"></a>Ayrıca bkz.
--------

[Soru formları tasarlama](design-questionnaires.md)

[Soru formlarını kullanma](questionnaires.md)

[Soru formlarının sonuçlarını değerlendirmek ve görüntüleme](evaluate-questionnaire-results.md)


