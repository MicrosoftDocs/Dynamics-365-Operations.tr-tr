---
title: Kurslara genel bakış
description: Bu makalede, İnsan Kaynakları yöneticilerinin, çalışanlara sunulan kurslarla ilgili bilgileri korumak için kurs özelliklerini nasıl kullanabilecekleri açıklanmaktadır.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable, HcmLearningWorkspace
audience: Application User
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a1fd00fb9feea9ab426f67095770389696452215
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/25/2022
ms.locfileid: "9716346"
---
# <a name="courses-overview"></a>Kurslara genel bakış

Microsoft Dynamics 365 Human Resources, kuruluşunuzun öğrenme gereksinimlerine yönelik bir çözüm sağlar. Bu çözüm iki öğrenme kursu yolu sunar: *sanal* ve *eğitmen liderliğinde*.

*Sanal öğrenme*, çevrimiçi kaynaklar aracılığıyla geliştirilmiş bir öğrenme deneyimidir. *Eğitmen liderliğinde eğitimde* bir eğitmen bir çalışan veya öğrenci grubu için eğitim oturumunu yönetir.

Öğrenme modülümüzde, İnsan Kaynakları uzmanları, yöneticiler ve eğitim yöneticileri çalışanlar için her iki öğrenme kursu yolunu da oluşturabilir ve atayabilir.

> [!NOTE]
> Sanal kursları kullanmak için Özellik yönetiminde **Kurs iyileştirmeleri** özelliğini etkinleştirmeniz gerekir.

## <a name="set-up-virtual-courses"></a>Sanal kursları ayarlama

Sanal kursları yapılandırmak için Özellik yönetiminde **Kurs iyileştirmeleri** özelliğini etkinleştirmeniz gerekir. **Kurslar \> Yeni**'ye gidin ve **Sanal** seçeneğini **Evet** olarak ayarlayın. Özellik etkinleştirildikten sonra bir kurs bağlantısı gerekir. **Kurs durumu** alanı **Açık** olarak ayarlanır. **Personelin kendi kendine kayıt olmasına izin ver** seçeneği **Evet** olarak ayarlanır ancak **Hayır** olarak da ayarlanabilir.

**Kurs iyileştirmeleri** özelliği Özellik yönetiminde etkinleştirildikten sonra aşağıdaki değişiklikler gerçekleşir:

- Kurs ataması için bir son tarih tanımlanmalıdır.
- Kurs bağlantısı gereklidir.
- **Personel self servisi**, **Kurslar** içinde personele genel bakışı gösterir. Kullanıcı süresi dolmuş, süresi dolmak üzere olan ve atanmış kursları görüntüleyebilir.
- Çalışanlar sanal kursları tamamlayabilir ve bunları kendi kendilerine onaylayabilir.

## <a name="set-up-instructor-led-courses"></a>Eğitmen liderliğinde kursları ayarlama

Eğitmen liderliğinde kurslar kullanılmadan önce yapılandırılmalıdır.

Aşağıdaki bilgiler isteğe bağlıdır ve kurslar için belirtilebilir. Bu bilgiler kurslar için girilirse kurs kayıtları oluşturulmadan önce ayarlanması gerekir:

- Kurs türü
- Derslik grupları
- Kurs grupları
- Kurs yerleşimleri
- Derslikler
- Eğitmenler
- Kurs türleri

Yapı ve içeriklerine göre kategorilere ayırmak için *kurs türlerini* kullanabilirsiniz.  **Kurs türleri** sayfasında kurs türlerini oluşturabilirsiniz.

Bir kursa kaydedebileceğiniz minimum ve maksimum katılımcı sayısı **Kurslar** sayfasının **Genel** hızlı sekmesinde tanımlanır.

### <a name="course-setup-type"></a> Kurs kurulum türü 

Kursun yapısını *Ayar türleri* belirler. Kurslar için üç ayar türü vardır.

| Kurulum türü | Açıklama |
|------|--------|
| Standart | Bu ayar türündeki kurslarda günlük ajanda yoktur. Yeni bir kurs oluşturduğunuzda varsayılan ayar türüdür. |
| Ajanda | Birden fazla günde gerçekleşen bir kursun her gününün ayrıntılarını planlamak için bu ayar türünü seçin. |
| Gündem + oturumlar | <p>Daha karmaşık kurslar için bu ayar türünü seçin. Örneğin kursun ajandasını *dersler* ve *oturumlar* olarak ayırabilirsiniz:</p><ul><li>*Dersler*, bir kursun belirli konu alanlarıdır.</li><li>*Oturumlar*, dersleri ayırır ve dersle ilgili işlemlerin veya tekniklerin tanımlanmasına yardımcı olur.</li></ul> |

### <a name="course-tasks"></a> Kurs görevleri

Her kurs için aşağıdaki görevleri gerçekleştirin:

- Katılımcıları kaydedin.
- Kayıt için süre sonu belirleyin.
- Katılımcıların minimum ve maksimum sayısını belirleyin.
- Bir kurs konumu ve sınıfı atayın.
- Kurs katılımcılarına otel önerin.
-  **Personel self servisi**'nde ilan edebileceğiniz bir kurs açıklaması oluşturun.

> [!NOTE]
> Kursu yalnızca kimse kayıt olmadıysa silebilirsiniz.

### <a name="course-statuses"></a>Kurs durumları

Aşağıdaki tabloda, her bir kurs için tamamlanan kurs durumları ve eylemler listelenmiştir.

| Çalıştırma Durumu | Eylemler |
|------|--------|
| Oluşturuldu | <ul><li>Kurs bilgilerini girin ve değiştirin.</li><li>Çalışanların kursa kaydolabilmeleri için kurs durumunu **Açık** olarak değiştirin.</li></ul> | 
| Aç | <ul><li>Kurs için katılımcılar kaydedin.</li><li>Kurstan katılımcı çıkartın.</li><li>Kurs için katılımcılar teyit edin.</li><li>Durumları **Onaylandı** olan katılımcılar için kurs durumunu **Kapalı** veya **İptal Edildi** olarak değiştirin.</li></ul>|
| Kapalı | Kursu yeniden açabilirsiniz. |
| İptal Edildi | Kursu yeniden açabilirsiniz. |

### <a name="course-participants"></a>Kurs katılımcıları

*Kurs katılımcıları*, bir eğitim kursuna veya etkinliğine katılım gösteren çalışanlardır. Katılımcıları yalnızca açık kurslara kaydedebilirsiniz.

### <a name="workflow"></a>İş Akışı

 **Personel self servisi** sayfası üzerinden bir kursa kayıt olan personeller, kayıtlarını onay için iş akışı aracılığıyla yönlendirebilirler.  **Kurslar** sayfasının **Genel** hızlı sekmesinde bir kursu bir iş akışına atayabilirsiniz.
