---
title: "Gider yönetimini yapılandır"
description: "Bu makale, Microsoft Dynamics 365 for Finance and Operations'ta Gider yönetimini yapılandırmadan önce planlama sürecinde değerlendirmeniz gereken noktaları ve almanız gereken kararları açıklar."
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: c87909d9eb3a4d717e0c40289353da0267a51f60
ms.contentlocale: tr-tr
ms.lasthandoff: 03/26/2018

---

# <a name="configure-expense-management"></a>Gider yönetimini yapılandır

[!include [banner](../includes/banner.md)]

Bu konu, Microsoft Dynamics 365 for Finance and Operations'ta Gider yönetimini yapılandırmadan önce planlama sürecinde değerlendirmeniz gereken noktaları ve almanız gereken kararları açıklar. Gider yönetiminde, ödeme yöntemleri, seyahat talepleri, gider raporları, ilkeler vb. hakkındaki bilgileri saklayabilirsiniz.

Gider yönetiminizin yapılandırmasını planlarken aldığınız pek çok karar kuruluşunuzun hiyerarşisi ve mali yapısına dayandığından, bu alanlar için planlama belgelerine başvurmalısınız.

## <a name="intercompany-expenses"></a>Şirketlerarası giderler

Şirketlerarası giderleri etkinleştirdiğinizde, kuruluşunuz içindeki istihdam tüzel kişiliğine ve çalışanlara, kuruluşunuzdaki başka tüzel kişilikler adına masraf yapma ve ödeme tahsil etme izni verirsiniz. Örneğin, tüzel kişilik A içindeki bir çalışan, tüzel kişilik B için bir projeyi tamamlar ve proje, seyahate ilişkin giderlerde ortaya çıkarır. Şirketlerarası giderler etkinleştirilmişse, çalışan gideri tüzel kişilik B'ye nakledecek bir gider raporu oluşturabilir ve gider tüzel varlık A tarafından ödenmelidir. Eğer kuruluşunuzun çok sayıda tüzel kişiliği yoksa, şirketlerarası giderleri etkinleştirmenize ihtiyaç yoktur.

**Karar:** Şirketlerarası giderleri etkinleştirmek istiyor musunuz?

## <a name="financial-management"></a>Mali yönetim

Gider Yönetimi, organizasyonunuzun mali yönetimi ile sıkı sıkıya tümleşiktir. Gider yönetimi yapılandırmanızın pek çoğu, kuruluşunuzun mali yapısı hakkında almış olduğunuz kararları temel alır. Aşağıdaki bölümler kuruluşunuzun mali kararları ve liderlik ekibinizin yönlendirmesi ile planlamaya ve karar almaya ihtiyaç duyulan çeşitli alanları açıklamaktadır.

### <a name="per-diems"></a>Harcırahlar

Kuruluşunuzun sağladığı çalışan harcırahlarını tanımlamanız gerekir. Harcırahlar genellikle yemek, konaklama ve diğer arızi giderler gibi giderleri karşılamak için kullanıldığından, kuruluşunuzun sunduğu harcırah tahsisatları için kurallar oluşturabilirsiniz. harcırah oranları seyahatin yılın hangi döneminde yapıldığı, seyahat yeri veya her ikisine dayanarak ayarlanabilir. Bir harcırah kuralı tanımlarken, harcırahın çalışana ek yemek veya hizmetler sunulduğunda stopaj uygulanacak bir yüzdesini seçebilirsiniz. Ayrıca, çalışan seyahat ettiği durumlarda uygulanacak, harcırahın sağlanacağı minimum ve maksimum saatler için harcırah katmanları tanımlayabilirsiniz.

**Kararlar:**

- İlk ve son günler için varsayılan harcırah kuralları:

    - Çalışanın bir gün için talep edebileceği ve yine de harcırah alabileceği en az saat sayısı kaçtır?
    - Yemek için ilk gün ve son günde teklif edilen tutarda bir düşüş var mıdır? Bir azaltma varsa, azaltmanın yüzdesi nedir?
    - Otel için ilk gün ve son günde teklif edilen tutarda bir düşüş var mıdır? Bir azaltma varsa, azaltmanın yüzdesi nedir?
    - İlk günde ve son günde oluşabilecek diğer masraflar için tutarda yapılacak bir düşüş var mıdır? Bir azaltma varsa, azaltmanın yüzdesi nedir?

- Varsayılan harcırah kuralları:

    - Örneğin yemek ücretsiz ise, her bir öğün için harcırahta yapılacak bir indirim yüzdesi mevcut mudur? Bir azaltma varsa, her bir öğün için azaltmanın yüzdesi nedir?
    - Yiyecek indirimi günlük, seyahat başına veya günlük öğün sayısına göre mi hesaplanır?
    - Harcırah tutarları normal biçimde mi yukarı mı yuvarlanacaktır?
    - Harcırahlar 24 saatlik dönemlere göre mi takvim gününe göre mi hesaplanır?

- Konuma bağlı harcırah kuralları:

    - Harcırah oranlarını konuma göre farklılık gösterir mi? Hangi konumlar dahildir?
    - Harcırah oranları konuma göre değişiyorsa, her konum için, aşağıdaki türde maliyetler için hangi yüzde tutarı sağlanır:

        - Yemekler
        - Otel
        - Diğer giderler

### <a name="expense-management-journals-and-accounts"></a>Gider yönetimi günlükleri ve hesapları

Gider Yönetimi birden fazla günlükler ve hesaplar kullanmanızı gerektirir. Örneğin nakit avanslar veya kredi kartı anlaşmazlıkları için aynı hesabın mı kullanılacağına karar vermeniz gerekir.

**Kararlar:**

- Hangi genel muhasebe günlükleri gider raporlarının nakledilmesi için onaylanmıştır?
- Nakit avanslar için hangi hesap kullanılır?
- Nakit avanslar deftere hemen nakledilmeli mi?

### <a name="payment-methods"></a>Ödeme yöntemleri

Çalışanlarınızın işletmeniz adına giderde bulunmasına izin verirseniz, çalışanlarınızın kullanabileceği ödeme yöntemlerini tanımlamanız gerekir. Örneğin, çalışanların nakit veya şirket kredi kartını kullanmasına izin verebilir. Ayrıca çalışanların kişisel kredi kartları kullanıp bunları geri ödemesini daha sonra almalarına da izin verebilirsiniz. İzin verdiğininiz her ödeme yöntemi için aşağıdaki kararları almanız gerekir.

**Kararlar:**

- Hangi ödeme yöntemlerine izin verilir?
- Ödeme yöntemi giderlerine kim sahiptir?
- Mahsup hesap türü var mıdır? Mahsup hesap türü varsa, hesap nedir?
- Mahsup hesap varsa, hesap nedir?
- Ödeme yöntemi kredi kartı ise, ödeme yöntemi sadece içe aktarılan hareketler ile mi kullanılacaktır?

### <a name="expense-categories-and-shared-categories"></a>Gider kategorileri ve paylaşılan kategoriler

Çalışanlar bir gider raporu oluşturduklarında, kaydettikleri her gider bir gider kategorisi ile ilişkilendirilmelidir. Gider kategorileri, kuruluşunuzdaki tüzel kişilikler arasında paylaşılabilen paylaşımlı kategorilerden türetilmiştir. Bu kategoriler ayrıca Proje yönetimi ve muhasebede de paylaşılmış olabilir, kuruluşunuzun nasıl tanımlı olduğuna bağlı olarak. Kuruluşunuzun tanımına ve uygulama ekibinin rehberliği doğrultusunda, Gider yönetiminde kullanılan kategorilerin sadece Gider yönetimi için mi yoksa Proje yönetimi ve muhasebe ve Gider yönetimi ile paylaşımlı olarak mı kullanılacağını belirleyin. Bu kategorilerin Proje ve Gider veya Proje ve Üretim arasında paylaşılmış olabileceğini unutmayın, Gider ve Üretim arasında değil. Her gider kategorisi için aşağıdaki kararları almanız gerekir.

**Kararlar:**

- Gider kategorisi nedir? Örneklere uçuşlar, otel ve mesafe kategorileri dahildir.
- Gider kategorisi ayrıca Proje yönetimi ve muhasebede de kullanılabilir mi?
- Gider türü nedir?
- Gider kategorisi için varsayılan ödeme yöntemi nedir?
- Gider kategorisindeki maliyetlerin maddeleştirilmesi gerekiyor mu?
- Gider kategorisi için ana varsayılan hesap nedir?
- Gider kategorisi için varsayılan madde satış vergi grubu nedir?
- Gider kategorisi için ek ödeme yöntemlerine izin verilir mi? Ek ödeme yöntemlerine izin veriliyorsa, bunlar nedir?
- Bu gider kategorisinde alt kategoriler var mıdır? Alt kategoriler varsa, aşağıdaki kararları vermeniz gerekir:

    - Herhangi bir alt kategori vergiden düşmeye hariç midir?
    - Alt kategorilerin madde satış vergi grubu nedir?

Gider kategorisi ayrıca Proje yönetimi ve muhasebede de kullanılıyorsa, kalan soruları da yanıtlayın. Aksi taktirde, sonraki bölüme geçin.

- Aşağıdaki giderler için hangi maliyet hesapları kullanılacaktır?

    - Maliyet
    - Bordro tahsisatı
    - Süren iş - maliyet değeri
    - Maliyet-madde
    - Süren iş - maliyet değeri - madde
    - Tahakkuk eden zarar
    - Süren iş - tahakkuk eden zarar

- Aşağıdakiler için hangi gelir hesapları kullanılacaktır.

    - Faturalanmış gelir
    - Tahakkuk eden gelir - satış değeri
    - Süren iş - satış değeri
    - Tahakkuk eden gelir - üretim
    - Süren iş - üretim
    - Tahakkuk eden gelir - kar
    - Süren iş - kar
    - Tahakkuk eden gelir - abonelik
    - Süren iş - abonelik

### <a name="taxes"></a>Vergiler

Giderlerle ilgili vergiler için, gider raporlarına nelerin dahil edileceğini veya etkinleştirileceğini belirlemeniz gerekir.

**Kararlar:**

- Gider tutarlarına satış vergisi dahil midir?
- Giderler üzerinde vergiden düşme etkinleştirilecek midir?

    > [!NOTE]
    > Genel muhasebeyi planladığınızda, ABD satış vergisi ve kullanım vergisi kurallarını uygulamaya karar verdiyseniz, giderler üzerinde vergiden düşmeyi etkinleştiremezsiniz. (ABD satış vergisi ve kullanım vergisi kurallarını uygulamak için **Satış vergisi vergilendirme kuralları uygula** seçeneğini **Evet** olarak ayarlayın.)

## <a name="policies"></a>İlkeler

Gider raporu ilkeleri oluşturarak kuruluşunuzun, çalışanlar kendisi adına giderler oluşturduklarında vakit ve paradan tasarruf etmesine yardımcı olabilirsiniz. İlkeler çalışanların bir bütçeye sadık kalmalarını, gerekli tüm bilgileri sağlamalarını ve sadece gerektiğinde para harcamalarını garanti etmeye yardımcı olur. Her bir gider raporu ilkesini ve gider raporu onay ilkesini oluşturduğunuzda aşağıdaki kararları almanız gerekir.

**Kararlar:**

- İlkenin adı nedir?
- Gider ilkesi ne içindir?
- Eğer daha önceden şirketlerarası giderleri etkinleştirme kararı aldıysanız, bu ilke kuruluşunuzdaki hangi şirketlere uygulanır?
- İlke zaman etkili olur?
- İlke ne zaman sona?
- İlke kuralı nedir?
- İlke kuralının sonucu nedir?

