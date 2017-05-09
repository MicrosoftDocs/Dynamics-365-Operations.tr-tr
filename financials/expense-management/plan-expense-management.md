---
title: "Gider yönetimini yapılandır"
description: "Bu makalede, Microsoft Dynamics AX&quot;te Gider yönetimini yapılandırmadan önce planlama sürecinde değerlendirmeniz gereken noktalar ve almanız gereken kararlar açıklanmaktadır. Gider yönetimi alanında, ödeme yöntemleri, seyahat talepleri, gider raporları, ilkeler vb. hakkındaki bilgileri saklayabilirsiniz."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: af7e7288f741b3c519227e2778c4c4311c3a2012
ms.openlocfilehash: 88cdf531b6da615034f9982d3503b9add0100479
ms.lasthandoff: 03/31/2017


---

# <a name="configure-expense-management"></a>Gider yönetimini yapılandır

[!include[banner](../includes/banner.md)]


Bu makalede, Microsoft Dynamics AX'te Gider yönetimini yapılandırmadan önce planlama sürecinde değerlendirmeniz gereken noktalar ve almanız gereken kararlar açıklanmaktadır. Gider yönetimi alanında, ödeme yöntemleri, seyahat talepleri, gider raporları, ilkeler vb. hakkındaki bilgileri saklayabilirsiniz. 

Gider yönetiminizin yapılandırmasını planlarken aldığınız pek çok karar kuruluşunuzun hiyerarşisi ve mali yapısına dayandığından, bu alanlar için planlama belgelerine başvurmalısınız.

## <a name="intercompany-expenses"></a>Şirketlerarası giderler
Şirketlerarası giderleri etkinleştirdiğinizde, kuruluşunuz içindeki tüzel kişiliklere ve çalışanlara, kuruluşunuzdaki başka tüzel kişilikler adına masraf yapma ve ödeme tahsil etme izni verirsiniz. Örneğin, A tüzel kişiliğindeki bir çalışan, B tüzel kişiliği için bir projeyi tamamlar. Eğer şirketlerarası giderler etkinse, çalışan daha sonra bir zaman çizelgesi oluşturabilir ve tüzel kişilik B tarafından ödeme alabilir. Eğer kuruluşunuzun çok sayıda tüzel kişiliği yoksa, şirketlerarası giderleri etkinleştirmenize ihtiyaç yoktur. **Karar:** Şirketlerarası giderleri etkinleştirmek istiyor musunuz?

## <a name="financial-management"></a>Mali yönetim
Gider Yönetimi, organizasyonunuzun mali yönetimi ile sıkı sıkıya tümleşiktir. Gider yönetimi yapılandırmanızın büyük bölümü, kuruluşunuzun mali yapısı hakkında almış olduğunuz kararları temel alır. Aşağıdaki bölümler kuruluşunuzun mali kararları ve liderlik ekibinizin yönlendirmesi ile planlamaya ve karar almaya ihtiyaç duyulan çeşitli alanları açıklamaktadır.

### <a name="per-diems"></a>Harcırahlar

Kuruluşunuzun sağladığı çalışan harcırahlarını tanımlamanız gerekir. Harcırahlar genellikle yemek, konaklama ve diğer arızi giderler gibi giderleri karşılamak için kullanıldığından, kuruluşunuzun sunduğu harcırah tahsisatları için kurallar oluşturabilirsiniz. Harcırah oranları seyahatin yılın hangi döneminde yapıldığı, seyahat yeri veya her ikisine dayanarak ayarlanabilir. Bir harcırah kuralı tanımlarken, harcırahın çalışana ek yemek veya hizmetler sunulduğunda stopaj uygulanacak bir yüzdesini seçebilirsiniz. Ayrıca, çalışan seyahat ettiği durumlarda uygulanacak, harcırahın sağlanacağı minimum ve maksimum saatler için harcırah katmanları tanımlayabilirsiniz. **Kararlar: **

-   İlk ve son günler için varsayılan harcırah kuralları:
    -   Çalışanın bir gün için talep edebileceği ve yine de harcırah alabileceği en az saat sayısı kaçtır?
    -   Yemek için ilk ve son günde teklif edilen tutarda bir düşüş var mıdır? Öyleyse, azaltmanın yüzdesi nedir?
    -   Otel için ilk ve son günde teklif edilen tutarda bir düşüş var mıdır? Öyleyse, azaltmanın yüzdesi nedir?
    -   İlk ve son günlerde oluşabilecek diğer masraflar için tutarda yapılacak bir düşüş var mıdır? Öyleyse, azaltmanın yüzdesi nedir?
-   Varsayılan harcırah kuralları:
    -   Örneğin yemek ücretsiz ise, her bir öğün için harcırahta yapılacak bir indirim yüzdesi mevcut mudur? Öyleyse, her bir öğün için azaltma yüzdesi nedir?
    -   Yiyecek indirimi günlük, seyahat başına veya günlük öğün sayısına göre mi hesaplanır?
    -   Harcırah tutarları normal mi yuvarlanır yukarıya mı yuvarlanır?
    -   Harcırahlar 24 saatlik dönemlere göre mi takvim gününe göre mi hesaplanır?
-   Konuma bağlı harcırah kuralları:
    -   Harcırah oranları konuma bağlı mıdır ve hangi konumlar dahildir?
    -   Harcırah oranı konuma bağlı olarak farklılık gösteriyorsa, her konum için hangi yüzdelik tutarın sağlandığı:
        -   yemekler
        -   otel
        -   diğer giderler

### <a name="expense-management-journals-and-accounts"></a>Gider yönetimi günlükleri ve hesapları

Gider Yönetimi birden fazla günlükler ve hesaplar kullanmanızı gerektirir. Örneğin nakit avanslar veya kredi kartı anlaşmazlıkları için aynı hesabın mı kullanılacağına karar vermeniz gerekir. **Kararlar:**

-   Hangi genel muhasebe günlükleri gider raporlarının nakledilmesi için onaylanmıştır?
-   Nakit avanslar için hangi hesap kullanılır?
-   Nakit avanslar deftere hemen nakledilmeli mi?

### <a name="payment-methods"></a>Ödeme yöntemleri

Çalışanlarınızın işletmeniz adına giderde bulunmasına izin verirseniz, çalışanlarınızın kullanabileceği ödeme yöntemlerini tanımlamanız gerekir. Örneğin, çalışanların nakit veya şirket kredi kartını kullanmasına izin verebilir. Ayrıca çalışanların kişisel kredi kartları kullanıp bunları geri ödemesini daha sonra almalarına da izin verebilirsiniz. İzin verdiğininiz her ödeme yöntemi için aşağıdaki kararları almanız gerekir. **Kararlar:**

-   Hangi ödeme yöntemlerine izin verilir?
-   Ödeme yöntemi giderlerine kim sahiptir?
-   Mahsup hesap türü var mıdır? Öyleyse, nedir?
-   Mahsup hesap varsa, hesap nedir?
-   Ödeme yöntemi kredi kartı ise, ödeme yöntemi sadece içe aktarılan hareketler ile mi kullanılacaktır?

### <a name="expense-categories-and-shared-categories"></a>Gider kategorileri ve paylaşılan kategoriler

Çalışanlar bir gider raporu oluşturduklarında, kaydettikleri her gider bir gider kategorisi ile ilişkilendirilmelidir. Gider kategorileri, kuruluşunuzdaki tüzel kişilikler arasında paylaşılabilen Paylaşımlı kategorilerden türetilmiştir. Bu kategoriler ayrıca Proje yönetimi ve muhasebede de paylaşılmış olabilir, kuruluşunuzun nasıl tanımlı olduğuna bağlı olarak. Kuruluşunuzun tanımına ve uygulama ekibinin rehberliği doğrultusunda, gider yönetiminde kullanılan kategorilerin sadece giderler için mi yoksa Proje ve Gider ile paylaşımlı olarak mı kullanılacağını belirleyin. Bu kategorilerin Proje ve Gider veya Proje ve Üretim arasında paylaşılmış olabileceğini unutmayın, Gider ve Üretim arasında değil. Her gider kategorisi için aşağıdaki kararları almanız gerekir. **Kararlar:**

-   Gider kategorisi nedir? Örneğin, uçuşlar, otel veya mesafe.
-   Bu gider kategorisi ayrıca Proje yönetimi ve muhasebede de kullanılabilir mi?
-   Gider türü nedir?
-   Gider kategorisi için varsayılan ödeme yöntemi nedir?
-   Bu kategorideki giderlerin maddeler haline getirilmiş olması gerekli midir?
-   Gider kategorisi için ana varsayılan hesap nedir?
-   Gider kategorisi için varsayılan madde satış vergi grubu nedir?
-   Gider kategorisi için ek ödeme yöntemlerine izin verilir mi? Öyleyse, nelerdir?
-   Bu gider kategorisi içinde alt kategoriler var mıdır? Öyleyse:
    -   Herhangi bir alt kategori vergiden düşmeye hariç midir?
    -   Alt kategorilerin madde satış vergi grubu nedir?

    Eğer bu gider kategorisi ayrıca Proje yönetimi ve muhasebede de kullanılıyorsa, kalan soruları da yanıtlayın. Aksi takdirde, bu bölümle işiniz bitti demektir.
-   Aşağıdakiler için hangi maliyet hesapları kullanılacaktır?
    -   Maliyet
    -   Bordro tahsisatı
    -   Süren iş - maliyet değeri
    -   Maliyet-madde
    -   Süren iş - maliyet değeri - madde
    -   Tahakkuk eden zarar
    -   Süren iş - tahakkuk eden zarar
-   Aşağıdakiler için hangi gelir hesapları kullanılacaktır.
    -   Faturalanmış gelir
    -   Tahakkuk eden gelir - satış değeri
    -   Süren iş - satış değeri
    -   Tahakkuk eden gelir - üretim
    -   Süren iş - üretim
    -   Tahakkuk eden gelir - kar
    -   Süren iş - kar
    -   Tahakkuk eden gelir - abonelik
    -   Süren iş - abonelik

 

### <a name="taxes"></a>Vergiler

Giderlerle ilgili vergiler için, gider raporlarına nelerin dahil edileceğini veya etkinleştirileceğini belirlemeniz gerekir. **Kararlar:**

-   Gider tutarlarına satış vergisi dahil midir?
-   Giderler üzerinde vergiden düşme etkinleştirilecek midir?

Genel muhasebe planlama sırasında sizin uygulamak ABD satış vergisi ve vergi kanunlarını kullanma karar verdiyseniz, ki bu ** Satış vergisi vergilendirme kurallarını uygula** seçeneğini Evet olarak işaretleyerek yapılır, giderler üzerinde vergiden düşmeyi etkinleştiremezsiniz.

## <a name="policies"></a>İlkeler
Çalışanlar tüzel kişilik adına gider oluşturduklarında vakit ve para tasarrufu sağlayacak gider raporlama ilkeleri oluşturabilirsiniz. İlkeler çalışanların bir bütçeye sadık kalmalarını, gerekli tüm bilgileri sağlamalarını ve sadece gerektiğinde para harcamalarını sağlar. Her bir gider raporu ilkesini ve gider raporu onay ilkesini oluşturduğunuzda aşağıdaki kararları almanız gerekir. **Kararlar: **

-   İlkenin adı nedir?
-   Gider ilkesi ne içindir?
-   Eğer daha önceden şirketlerarası giderleri etkinleştirme kararı aldıysanız, bu ilke kuruluşunuzdaki hangi şirketlere uygulanır?
-   İlke zaman etkili olur?
-   İlke ne zaman sona?
-   İlke kuralı nedir?
-   İlke kuralının sonucu nedir?





