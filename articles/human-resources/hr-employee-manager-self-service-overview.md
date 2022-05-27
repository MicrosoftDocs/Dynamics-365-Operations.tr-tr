---
title: Personel ve Yönetici self servisine genel bakış
description: Bu makalede, Personel ve Yönetici self servisi çalışma alanına genel bir bakış sağlanmaktadır.
author: twheeloc
ms.date: 08/26/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.custom:
- "51941"
- intro-internal
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 51883730c36a3df2538adbe85ad8ead7d3cf1e98
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694495"
---
# <a name="employee-and-manager-self-service-overview"></a>Personel ve Yönetici self servisine genel bakış


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makalede, Personel ve Yönetici self servisi çalışma alanına genel bir bakış sağlanmaktadır.

## <a name="edit-personal-details"></a>Kişisel ayrıntıları düzenle

Herhangi bir kişisel bilgi eklemeniz veya değiştirmeniz gerekiyorsa, [Kişisel bilgileri düzenleyin](hr-employee-manager-self-service-edit-personal-information.md) inceleyin.

## <a name="user-not-assigned-to-a-worker-record"></a>Kullanıcın çalışan kaydına atanmaması

Kullanıcınızı **Kullanıcılar** sayfasındaki bir **Çalışan** kaydına bağlamadıysanız aşağıdaki ileti görüntülenir:

**Kullanıcı kimliğiniz sistemde personel kaydınızla ilişkili değil. İlişkilendirilene kadar bilgilerinizi görüntüleyemez veya güncelleştiremezsiniz. Yardım için yöneticinizle veya destek ekibiyle iletişime geçin.**

Kullanıcıyı **Çalışan** kaydıyla ilişkilendirmek için **Kullanıcılar**'a gidip kullanıcıyı seçin. **Düzenle**'yi seçin, sayfadaki **Kişi** alanına ilgili çalışanı ekleyin ve **Kaydet**'i seçin. Artık **Personel self servisi**'ne erişebiliyor olmanız gerekir.

## <a name="security-requirements-for-employee-and-manager-self-service"></a>Personel ve Yönetici self servisi ile ilgili güvenlik gereksinimleri

Personel ve Yönetici self servisi, iki güvenlik rolü gerektirir:

- Personeller için Personel rolü gereklidir.
- Yöneticiler için hem Personel hem Yönetici rolleri gereklidir.

>[!NOTE]
>Personel ve Yönetici self servisine erişmek için, Personel ve Yönetici çalışma alanlarına erişim izni verildiği sürece özel roller de kullanabilirsiniz.<br>
>Personel bilgilerine yönetici erişimi, Human Resources'ta tanımlanan satır hiyerarşisindeki mevcut konuma bağlıdır.

## <a name="employee-self-service"></a>Personel self servisi

**Bilgilerim** sekmesi, **Personel self servisi** için aşağıdaki bilgileri görüntüler.  

### <a name="summary"></a>Özet

**Bana atanan iş maddeleri** çalışana atanan tüm onayları ve iş akışı maddelerini görüntüler. Kullanıcıya e-postalar göndermek için iş akışı öğelerini yapılandırabilirsiniz.

**Bana atanan soru formları** doğrudan çalışana veya gruba atanan tüm planlanan soru formlarını görüntüler.

**Şirket dizininin** çalışanları, kuruluştaki kişilerle ilgili bilgileri arayacaktır. Genel kişi bilgileri tüm çalışanlar tarafından kullanılabilir. Şirket dizini, çalışanın oturum açtığı şirketle kısıtlıdır.

**Ekip takvimi** ekibinizin takvim bilgilerini gösterir. Daha fazla bilgi için bkz. [Ekip ve şirket takvimlerini görüntüleyin](hr-employee-self-service-calendar.md).

### <a name="my-career-information"></a>Kariyer bilgilerim

**Personel self servisi**'nin **Kariyer bilgilerim** bölümü İzin ve Devamsızlık, Performans Yönetimi, Yetkinlikler, Kazançlar, Görevler ve Ekler ile ilgili kutucukları görüntüler.

**İzin Bakiyeleri** kutucuğu, kayıtlı tüm planların bakiyelerini görüntüler. Bu kutucuk, tahakkuk yönteminize göre bakiyenizi tahmin eder. Daha sonra bir onay iş akışı sürecinden geçecek olan izin taleplerini girebilir ve gönderebilirsiniz. İzin ve devamsızlık yönetimi hakkında daha fazla bilgi için bkz. [İzin ve devamsızlık genel bakışı](hr-leave-and-absence-overview.md).

**Görevler** kutucuğu size atanan görevleri görüntüler ve bunları görüntülemenizi ve yönetmenizi sağlar.

**Sonraki Kayıtlı Kurs**, kayıt yaptığınız bir sonraki kursu görüntüler. Açık kursları görüntüleyebilir ve kaydedebilirsiniz. Kayıt yaptırmak üzere açık olan tüm kurslar **Başladı** durumundadır ve personelin kendi kendine kayıt olmasına izin verir. Kuruluşunuzun ayarlarına bağlı olarak, kurs kaydınız bir onay işleminden geçebilir.

**Sertifikalar** kutucuğu, geçerli tarihe en yakın tarihte süresi dolacak olan sertifikayı ve sertifikanın bitiş tarihini görüntüler. Sertifikaları güncelleştirebilir, ekleyebilir veya kaldırabilirsiniz. Kuruluşunuzun ayarlarına bağlı olarak, sertifika güncellemeleri bir onay işleminden geçebilir.

**Sonraki Zamanlanmış İnceleme**, bir sonraki performans incelemenizi görüntüler. Bu kutucuktan yeni bir inceleme başlatabilirsiniz. Yöneticiniz veya İK temsilciniz Ayrıca İnceleme de başlatabilir. Kuruluşunuzun ayarlarına bağlı olarak çıkış incelemelerini de görüntüleyebilir, güncelleştirebilir ve gönderebilirsiniz.

**Performans Hedefleri** ile hedeflerinizi yönetebilirsiniz. Bu kutucuk, her durum için sahip olduğunuz hedef sayısını görüntüler (**Başlatılmadı**, **İzlemede** ve **Geliştirilmesi gerekiyor**). Atanan rol tabanlı güvenliğine bağlı olarak, amaçları oluşturabilir, güncelleştirebilir ve kaldırabilirsiniz. İsterseniz, gruplardan veya şablonlardan yeni hedefler ekleyebilirsiniz. Yöneticiler ve İK ayrıca çalışanlar adına hedefler oluşturabilir ve her hedefin ayrıntılı olarak nasıl yapılacağını belirleyebilir. Yöneticiler ve çalışanlar hedefler üzerinde işbirliği yapabilir ve aktiviteleri, ölçümleri ve durumları güncelleştirebilir. Ayrıca, ekleri dahil edebilirsiniz.

Mevcut becerilerinizi **Toplam Beceriler** kutucuğunda görüntüleyebilirsiniz. Yetenekleri güncelleştirebilir, yenilerini ekleyebilirsiniz veya artık ilgili olmayan olanları kaldırabilirsiniz. Kuruluşunuzun ayarlarına bağlı olarak, becerilerinizdeki değişiklikler bir onay işleminden geçebilir.

Geçerli ücretinizi **Ücret** bölümünde görüntüleyebilirsiniz. Yıllık ödeme ve son artış tutarını görüntülemek için **göster**'i seçin. Birden fazla şirkette çalışıyorsanız her bir yıllık tutar görüntülenir. Ayrıntılı ücret geçmişinizi görüntülemek için **Yıllık maaş** tutarını seçerek **Sabit ve değişken ücret geçmişi** sayfasını açın. Gelecekteki ücret bu sayfada görüntülenmez. Birden fazla yerde çalışıyorsanız her bir şirkete giriş yapmadan ücret geçmişinizi görüntülemek için bu sayfada şirketler arasında geçiş yapabilirsiniz.

**Ekler** kutucuğuyla belgeleri görüntüleyin ve yönetin. Tüm **dış** ekleri yönetebilirsiniz. Hem İK hem de personel, **Personel self servisi** veya **Çalışan** sayfası aracılığıyla ek ekleyebilir. Ekler varsayılan değer olarak **harici** olarak ayarlanır.

### <a name="additional-information"></a>Ek bilgiler

Bu bölüm, **Kariyer Bilgilerim** bölümüne benzer şekilde diğer **Personel self servisi** alanlarına bağlantılar sağlar.

**Sosyal haklar** bağlantısı üzerinden daha fazla yararlanmak için kaydolun. Sosyal haklar yönetimi hakkında daha fazla bilgi için [Sosyal Haklara genel bakış](hr-benefits-management-overview.md)'a bakın.

**Performans** altında, hem performans hedeflerinde hem de incelemelerde kullanılacak performans günlüğü girişleri oluşturmak için **Performans günlüğü**'nü seçebilirsiniz. Kuruluşunuzdaki diğer çalışanlarla ilgili geribildirim sağlamak için **geri bildirim gönder**'i seçebilirsiniz. Kuruluşunuzun ayarlarına bağlı olarak, e-postalar alıcıya, gönderene ve yöneticilere gönderilebilir. Organizasyon içindeki tüm çalışanlara geri bildirim gönderebilirsiniz. Geri bildirim gönderme şirket tarafından kısıtlanmıyor.

**Yetki** altında **kurslar**, **eğitim**, **güven** gerektiren pozisyonlar ve **mesleki deneyimlerin** üzerinde değişiklikler yapabilirsiniz. Kuruluşunuzun ayarlarına bağlı olarak, sertifika güncellemeleri bir onay işleminden geçebilir.

İş ayrıntılarını **organizasyon** altında görüntüleyebilirsiniz. İş ayrıntıları, birincil konumunuz için yetenekler, sertifikalar ve sorumluluk alanları içerir. Ayrıca, kullanımınıza aldığınız herhangi bir ödünç verilen donanımı de görebilirsiniz. Kuruluşunuzun ayarlarına bağlı olarak, yüklenen ekipmandaki değişiklikler bir onay işleminden geçebilir.

**Soru formu** altında, tamamlanan soru formlarını görebilirsiniz. Tamamlanmamış şirket çapındaki soru formları da görebilirsiniz. Soru formunu istediğiniz zaman tamamlayabilirsiniz. Soru formunun yazarı, zaman çerçevesini ve soru formunun hangi sırada uygulanabilir olduğunu belirleyebilir.

**İnsan kaynakları parametreleri**'nde kullanıcı tanımlı bağlantıları yapılandırabilirsiniz. Örneğin, ödeme ekstrelerinin, yıl sonu belgelerinin veya harici çözümlerin bağlantılarını tanımlayabilirsiniz. Bu bağlantılar bu bölümün en altında yer alabilir, ancak onları kişiselleştirme kullanarak taşıyabilirsiniz.

**Personel self servisi** çalışma alanına Power Apps uygulamasını katıştırarak ek sekmeler de oluşturabilirsiniz. Sayfayı herhangi bir Power Apps ile kişiselleştirmek için **ayarlar** menüsünü kullanın. **Ayarlar** menüsünde bir güç uygulaması eklemeyi, ayrıntıları tamamlamak ve uygulamayı eklemeyi seçebilirsiniz. Varsayılan olarak, Power Apps dizideki ilk sekme olarak görünür. Standart kişiselleştirme kullanarak sırayı değiştirebilirsiniz.

## <a name="my-team"></a>Ekibim

**Takımım** sekmesi, **Yönetici self servisi** için aşağıdaki bilgileri görüntüler. **Ekibim** sekmesine yalnızca yöneticiler erişebilir.

### <a name="personnel-actions"></a>Personel eylemleri

Personel eylemleri **insan kaynakları paylaşılan parametreleri** ve **insan kaynakları parametreleri** içindeki Konfigürasyon seçeneklerine göre görüntüler. **Çalışanlar** için etkinleştirildiğinde, personel eylemleri yeni menü seçeneklerini etkinleştirir:

- **Yeni personel talep et**
- **Yeni yüklenici talep et**
- **Çalışan yeniden ataması talep et**
- **İşten çıkarma talep et**
- **Ücret değişikliği talep et**

İsteğe bağlı İnceleme ve onay iş akışı üzerinden geçmek için bu seçenekleri yapılandırabilirsiniz.

**Pozisyon eylemlerini** etkinleştirme aşağıdaki seçenekleri etkinleştirin:

- **Yeni pozisyon talep et**
- **Pozisyon ayrıntılarında değişiklik talep et**

İsteğe bağlı İnceleme ve onay iş akışı üzerinden geçmek için bu seçenekleri yapılandırabilirsiniz.

### <a name="summary"></a>Özet

**Özet** bölümündeki bilgiler, İnsan Kaynakları'nın **İnsan kaynakları parametreleri**'nde belirlediği seçeneklere bağlıdır. **İnsan kaynakları parametreleri** sayfasının **Yönetici self servisi** sekmesinde, süresi dolan kayıtları ve açık pozisyonları görüntüleme seçeneklerini yapılandırabilirsiniz. Bu seçeneklerin etkinleştirilmesi, **Özet** bölümünde hangi yöneticilerin görebileceğini belirler.

Yöneticiler için aşağıdaki kutucukları konfigüre edebilirsiniz:

- **Ekibim için sona eren sertifikalar**
- **Takımım için süresi dolmak üzere olan kimlik numaraları**
- **Takımım için süresi dolmak üzere olan denemeler**
- **Takımım için süresi dolmak üzere olan ön elemeler**
- **Takımım için süresi dolmak üzere olan testler**
- **Doğrudan ve/veya genişletilmiş raporlar için açık pozisyonlar**
- **Ekibimde kapalı bekleme süresi istekleri**
- **Takım yetenekleri değerlendirmesi**
- **Yetenek eksikliği analizi**
- **Takım performans günlükleri**
- **Takım performans hedefleri**
- **Takım performansı gözden geçirmeleri**
- **Çıkış yapan çalışanlar**

Yöneticilerin, doğrudan raporları adına değişiklikler yapmak veya istekleri izin eklemek için aşağıdaki seçenekleri yapılandırabilirsiniz:

- Sertifikalar
- Kurslar
- Ödünç verilen maddeler
- Yetenekler
- İzin ve devamsızlık istekleri

### <a name="my-team-information"></a>Takımımın bilgileri

**Takımım**, yöneticilerin doğrudan ve genişletilmiş raporları görüntülemesine ve güncelleştirmesine olanak tanır. Genişletilmiş raporlara erişmek için bağlı çalışanları olan personeli seçin ve ardından kutucuktan **Takımı görüntüle**'yi seçin. Aynı seçeneklerin tümü, genişletilmiş raporlar için doğrudan rapor olarak uygulanır. 

#### <a name="summary-tab"></a>Özet sekmesi

**Özet** sekmesi, doğrudan raporlarınızın hızlı görünümünü sağlar. Bir doğrudan raporda çalışan da kendilerine rapor edilen çalışanlar varsa, kart, **ekip göster** düğmesiyle birlikte üst bölümdeki doğrudan rapor sayısını görüntüler. Her kutucuğun üzerinde bulunan seçenekler, seçilen personel için uygulanır. Örneğin, bir personel adına izin talebi girmek istiyorsanız personeli seçin ve ardından **İzin iste**'yi seçin. 

Bir çalışan seçtikten sonra **Ayrıntılar** düğmesini seçerseniz, aşağıdaki seçenekler görüntülenecektir:

- **Sertifikalar**
- **Maaş**
- **Kurslar**
- **İncelemeler**
- **İzin süresi**
- **Ödünç verilen maddeler**
- **Performans hedefleri**
- **Kayıtlı kurslar**
- **Yetenekler**
- **Geribildirim gönder**

Kuruluşunuzun ayarlarına bağlı olarak, yalnızca değişiklik veya yalnızca görünümü yapabilirsiniz.

#### <a name="position-tab"></a>Pozisyon sekmesi

**Pozisyon** sekmesi, personelin birincil pozisyonundaki özet görünümünü sağlar. Her kutucuğun başlık alanında ad, kutucuk ve bölüm görüntülenir. Bu kutucuk şunları içerir:

- **Kıdem tarihi**: **Çalışan** sayfasının çalışan özeti bölümünden görüntülenir.
- **Hizmet yılı**: Personelin işe başlama tarihi esas alınarak hesaplanır.
- **Önceki pozisyonların sayısı**: Pozisyon geçmişine bağlı olarak bu sayının seçilmesi önceden bulunulan tüm pozisyonların ayrıntılı görünümünü açar.
- **Doğum tarihi**: Personelin ay ve gün şeklinde belirtilen doğum tarihi.

Hem doğrudan hem de genişletilmiş raporların konum verilerini görüntüleyebilirsiniz.

#### <a name="compensation-tab"></a>Ücret sekmesi

**Ücret** sekmesi çalışanın yıllık maaşını görüntüler. Bir şirket tanımlayıcısı maaş tutarının altında görüntülenir. Bir çalışan birden fazla işe sahip ise ve çoklu tüzel kişiliklerden ödeme alıyorsa çalışanın birden çok ücret planı olacaktır. Şirket değiştirmeden tüzel kişiliklerdeki tüm ücret planlarını görmek için **İnsan kaynakları > Paylaşılan parametreler > Gelişmiş erişim > Şirketler arası ücreti etkinleştir** altında şirketler arası ücreti etkinleştirmeniz gerekir.

Ücret geçmişini görüntülemek için **Maaş tutarı**'nı seçerek **Ayrıntılar** sayfasını açın. **Ücret** sayfasında yalnızca geçerli ve geçmiş sabit ve değişken ücret kayıtları görüntülenir. Personel birden fazla yerde çalışıyorsa her şirketteki ücret geçmişini görüntülemek için şirketler arasında geçiş yapabilir veya tüm ücret planlarını görüntülemek için **Paylaşılan insan kaynakları parametreleri**'nde şirketler arası ücreti etkinleştirebilir.

Hem doğrudan hem de genişletilmiş raporların ücreti görüntüleyebilirsiniz.

#### <a name="leave-and-absence-tab"></a>İzin ve devamsızlık sekmesi

**İzin ve devamsızlık** sekmesi, faaliyeti olan çalışanların en üst bakiyelerini görüntüler. Eylem yapmak veya tam faaliyet listesini görmek için, **Ayrıntılar** 'ı seçin ve sonra **İzin**'ı seçin. **İzin** sayfasında, personelin zamanını daha iyi yönetmesine yardımcı olmak için bakiyeleri, istekleri, onaylanan izinleri ve tahmini bakiyeleri görüntüleyebilirsiniz. Organizasyonunuzun ayarlarına bağlı olarak, iş, sizin veya genişletilmiş raporlarınız için zaman kapalı da isteyebilirsiniz.

#### <a name="performance-goals-tab"></a>Performans hedefleri sekmesi

**Performans hedefleri** sekmesi, performans hedeflerini duruma göre özetler. Bir çalışanın tüm hedeflerini görmek için durum için bir sayı seçin veya **Ayrıntılardan** performans hedeflerini seçin. Yöneticiler ve çalışanlar hedefleri hedef süresine göre güncelleştirebilir.

Yöneticiler , **ekibimin** **Özet** bölümünde **ekip performans hedefleri** döşemesi aracılığıyla takımlarına ait tüm hedefleri görebilir.

#### <a name="reviews-tab"></a>İncelemeler sekmesi

**İncelemeler** sekmesi, çalışanın her durumunda sahip olduğu İncelemeleri özetler: **Devam ediyor**, **gözdengeçirilmek üzere hazır** ve **Son İnceleme**. Bir çalışanın incelemesine erişmek için, **Ayrıntılar** düğmesini seçin ve üzerinde işbirliği yapılacak İncelemeleri seçin. Gözden geçirme işleminin iş akışı sürecinde olduğu yere göre, incelemenin güncelleştirme için kullanılabilir olup olmadığını görebilirsiniz. 

Yöneticiler , **ekibimin** **Özet** bölümünde **ekip performans incelemeleri** döşemesi aracılığıyla takımlarına ait tüm incelemeleri görebilir.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
