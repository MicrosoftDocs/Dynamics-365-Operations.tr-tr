---
title: Personel ve Yönetici self servisine genel bakış
description: Bu makale, çalışan ve yönetici self servis çalışma alanına genel bir bakış sağlar.
author: andreabichsel
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom:
- "51941"
- intro-internal
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: adb0fc344963b33fe1704a22a35415d9c07b9a08
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/03/2021
ms.locfileid: "6338109"
---
# <a name="employee-and-manager-self-service-overview"></a>Personel ve Yönetici self servisine genel bakış

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makale, çalışan ve yönetici self servis çalışma alanına genel bir bakış sağlar.

## <a name="edit-personal-details"></a>Kişisel ayrıntıları düzenle

Herhangi bir kişisel bilgi eklemeniz veya değiştirmeniz gerekiyorsa, [Kişisel bilgileri düzenleyin](hr-employee-manager-self-service-edit-personal-information.md) inceleyin.

## <a name="user-not-assigned-to-a-worker-record"></a>Kullanıcın çalışan kaydına atanmaması

Kullanıcınızı **Kullanıcılar** sayfasındaki bir **Çalışan** kaydına bağlamadıysanız aşağıdaki ileti görüntülenir:

**Kullanıcı kimliğiniz sistemde personel kaydınızla ilişkili değil. İlişkilendirilene kadar bilgilerinizi görüntüleyemez veya güncelleştiremezsiniz. Yardım için yöneticinizle veya destek ekibiyle iletişime geçin.**

Kullanıcıyı **Çalışan** kaydıyla ilişkilendirmek için **Kullanıcılar**'a gidip kullanıcıyı seçin. **Düzenle**'yi seçin, formdaki **Kişi** alanına ilgili çalışanı ekleyin ve **Kaydet**'i seçin. Artık Personel self servisi'ne erişebiliyor olmanız gerekir.

## <a name="security-requirements-for-employee-and-manager-self-service"></a>Personel ve Yönetici self servisi ile ilgili güvenlik gereksinimleri

Personel ve Yönetici self servisi, iki güvenlik rolü gerektirir:

- Personeller için Personel rolü gereklidir.
- Yöneticiler için hem Personel hem Yönetici rolleri gereklidir.

>[!NOTE]
>Personel ve Yönetici self servisine erişmek için, Personel ve Yönetici çalışma alanlarına erişim izni verildiği sürece özel roller de kullanabilirsiniz.<br>
>Personel bilgilerine yönetici erişimi, Human Resources'ta tanımlanan satır hiyerarşisindeki mevcut konuma bağlıdır.

## <a name="employee-self-service"></a>Personel self servisi

**Bilgilerim** sekmesi, çalışan self servis için aşağıdaki bilgileri görüntüler.  

### <a name="summary"></a>Özet

**Bana atanan iş maddeleri** çalışana atanan tüm onayları ve iş akışı maddelerini görüntüler. Kullanıcıya e-postalar göndermek için iş akışı öğelerini yapılandırabilirsiniz.

**Bana atanan soru formları** doğrudan çalışana veya gruba atanan tüm planlanan soru formlarını görüntüler.

**Şirket dizininin** çalışanları, kuruluştaki kişilerle ilgili bilgileri arayacaktır. Genel kişi bilgileri tüm çalışanlar tarafından kullanılabilir. Şirket dizini, çalışanın oturum açtığı şirketle kısıtlıdır.

**Ekip takvimi** ekibinizin takvim bilgilerini gösterir. Daha fazla bilgi için bkz. [Ekip ve şirket takvimlerini görüntüleyin](hr-employee-self-service-calendar.md).

### <a name="my-career-information"></a>Kariyer bilgilerim

Çalışan self servisinin **kariyer bilgileri** bölümü, bırakma ve devamsızlık, performans yönetimi, yetki, fayda, görev ve eklerle ilgili kartlar içerir.

Bakiyelerde **zaman bakiyesi** kartında herhangi bir kayıtlı plan için bakiye görüntülenir. Bu kart, bakiyenizi tahakkuk yönteminizi temel alarak tahmin edin. Daha sonra onay iş akışı işleminden geçmek için, zaman aşımı istekleri girebilir ve gönderebilirsiniz. İzin ve devamsızlık yönetimi hakkında daha fazla bilgi için bkz. [İzin ve devamsızlık genel bakışı](hr-leave-and-absence-overview.md).

**Görev** kartı size atanan görevleri görüntüler ve bunları görüntülemenizi ve yönetmenizi sağlar.

Bir **sonraki kayıtlı kurs** kartında, kayıt yaptığınız bir sonraki kurs görüntülenir. Açık kursları görüntüleyebilir ve kaydedebilirsiniz. Kaydolma için açık olan tüm kursların durumu **başlatıldı** ve çalışanların bu kartta kendi kendine kayda girmesine izin ver. Kuruluşunuzun ayarlarına bağlı olarak, kurs kaydınız bir onay işleminden geçebilir.

**Sertifika** kartı geçerli tarihe en yakın zaman aşımına uğramakta olan sertifikanın sertifikasını ve son kullanım tarihini görüntüler. Sertifikaları güncelleştirebilir, ekleyebilir veya kaldırabilirsiniz. Kuruluşunuzun ayarlarına bağlı olarak, sertifika güncellemeleri bir onay işleminden geçebilir.

Bir **sonraki zamanlanmış İnceleme** kartında sonraki performans incelemeniz görüntülenir. Bu karttan yeni bir gözden geçirme başlatabilirsiniz. Yöneticiniz veya İK temsilciniz Ayrıca İnceleme de başlatabilir. Kuruluşunuzun ayarlarına bağlı olarak, bu karttaki çıkış incelemelerini görüntüleyebilir, güncelleştirebilir ve gönderebilirsiniz.

Hedeflerinizi, **performans hedefleri** kartıyla yönetebilirsiniz. Bu kart, her durumunda sahip olduğunuz hedeflerin sayısını(**başlatılmadı**, **izlemede** ve **gereksinim duyduğu gelişme**) görüntüler. Atanan rol tabanlı güvenliğine bağlı olarak, amaçları oluşturabilir, güncelleştirebilir ve kaldırabilirsiniz. İsterseniz, gruplardan veya şablonlardan yeni hedefler ekleyebilirsiniz. Yöneticiler ve İK ayrıca çalışanlar adına hedefler oluşturabilir ve her hedefin ayrıntılı olarak nasıl yapılacağını belirleyebilir. Yöneticiler ve çalışanlar hedefler üzerinde işbirliği yapabilir ve aktiviteleri, ölçümleri ve durumları güncelleştirebilir. Ayrıca, ekleri dahil edebilirsiniz.

Mevcut becerilerinizi **yetenekler** kartında görüntüleyebilirsiniz. Yetenekleri güncelleştirebilir, yenilerini ekleyebilirsiniz veya artık ilgili olmayan olanları kaldırabilirsiniz. Kuruluşunuzun ayarlarına bağlı olarak, becerilerinizdeki değişiklikler bir onay işleminden geçebilir.

Geçerli maaşınızı **ücret** kartı üzerinden görüntüleyebilirsiniz. Yıllık ödeme ve son artış tutarını görüntülemek için **göster**'i seçin. Birden fazla şirket içinde çalışıyorsanız, her yıllık tutar kart üzerinde görüntülenir. Ayrıntılı maaş geçmişinizi görüntülemek için **sabit ve değişken maaş geçmişi** formunu açmak üzere yıllık maaş tutarını seçin. Gelecekteki ücret bu formda görüntülenmiyor. Birden fazla işiniz varsa her bir şirkette oturum açmadan maaş geçmişinizi görüntülemek için bu form içindeki şirketler arasında geçiş yapabilirsiniz.

**Ekleri** kartla belgeleri görüntüleyin ve yönetin. Tüm **dış** ekleri yönetebilirsiniz. Hem İK hem de Çalışanlar Çalışan Self servis ile veya **çalışan** formu üzerinden ek ekleyebilirler. Ekler varsayılan değer olarak **harici** olarak ayarlanır.

### <a name="additional-information"></a>Ek bilgiler

Bu bölüm, **kariyer bilgileri** bölümüne benzer şekilde, diğer çalışan self servis alanlarına bağlantılar sağlar.

**Sosyal haklar** bağlantısı üzerinden daha fazla yararlanmak için kaydolun. Sosyal haklar yönetimi hakkında daha fazla bilgi için [Sosyal Haklara genel bakış](hr-benefits-management-overview.md)'a bakın.

**Performans** altında, performans hedefleri ve gözden geçirmeleri üzerinde kullanılacak performans günlüğü girişleri oluşturmak için **performans günlükleri**'ni seçebilirsiniz. Kuruluşunuzdaki diğer çalışanlarla ilgili geribildirim sağlamak için **geri bildirim gönder**'i seçebilirsiniz. Kuruluşunuzun ayarlarına bağlı olarak, e-postalar alıcıya, gönderene ve yöneticilere gönderilebilir. Organizasyon içindeki tüm çalışanlara geri bildirim gönderebilirsiniz. Geri bildirim gönderme şirket tarafından kısıtlanmıyor.

**Yetki** altında **kurslar**, **eğitim**, **güven** gerektiren pozisyonlar ve **mesleki deneyimlerin** üzerinde değişiklikler yapabilirsiniz. Kuruluşunuzun ayarlarına bağlı olarak, sertifika güncellemeleri bir onay işleminden geçebilir.

İş ayrıntılarını **organizasyon** altında görüntüleyebilirsiniz. İş ayrıntıları, birincil konumunuz için yetenekler, sertifikalar ve sorumluluk alanları içerir. Ayrıca, kullanımınıza aldığınız herhangi bir ödünç verilen donanımı de görebilirsiniz. Kuruluşunuzun ayarlarına bağlı olarak, yüklenen ekipmandaki değişiklikler bir onay işleminden geçebilir.

**Soru formu** altında, tamamlanan soru formlarını görebilirsiniz. Tamamlanmamış şirket çapındaki soru formları da görebilirsiniz. Soru formunu istediğiniz zaman tamamlayabilirsiniz. Soru formunun yazarı, zaman çerçevesini ve soru formunun hangi sırada uygulanabilir olduğunu belirleyebilir.

Kullanıcı tanımlı bağlantıları **insan kaynakları parametrelerinde** konfigüre edebilirsiniz. Örneğin, ödeme ekstrelerinin, yıl sonu belgelerinin veya harici çözümlerin bağlantılarını tanımlayabilirsiniz. Bu bağlantılar bu bölümün en altında yer alabilir, ancak onları kişiselleştirme kullanarak taşıyabilirsiniz.

Ayrıca, çalışan self servis çalışma alanı içine Power Apps katıştırarak ek sekmeler oluşturabilirsiniz. Sayfayı herhangi bir Power Apps ile kişiselleştirmek için **ayarlar** menüsünü kullanın. **Ayarlar** menüsünde bir güç uygulaması eklemeyi, ayrıntıları tamamlamak ve uygulamayı eklemeyi seçebilirsiniz. Varsayılan olarak, Power Apps dizideki ilk sekme olarak görünür. Standart kişiselleştirme kullanarak sırayı değiştirebilirsiniz.

## <a name="my-team"></a>Ekibim

**Ekibim** sekmesi, Yönetici self servis için aşağıdaki bilgileri görüntüler. **Ekibim** sekmesine yalnızca yöneticiler erişebilir.

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

**Özet** bölümündeki bilgiler, **insan kaynakları parametrelerinde** HR seçeneği belirlenmiş olan seçeneklere bağlıdır. **İnsan Kaynakları parametreleri** sayfasının **Yönetim Self servis** sekmesinde, süresi dolan kayıtları ve açık pozisyonları görüntüleme seçeneklerini yapılandırabilirsiniz.  Bu seçeneklerin etkinleştirilmesi, **Özet** bölümünde hangi yöneticilerin görebileceğini belirler.

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

Ekibim bilgileri, yöneticilerin doğrudan ve genişletilmiş raporları görüntülemesine ve güncelleştirmesine olanak tanır. Genişletilmiş raporlara erişmek için, yönlendirir raporunu alan çalışanı seçin ve sonra kart üzerinde **Ekibi görüntüle**'yi seçin. Aynı seçeneklerin tümü, genişletilmiş raporlar için doğrudan rapor olarak uygulanır. 

#### <a name="summary-tab"></a>Özet sekmesi

**Özet** sekmesi, doğrudan raporlarınızın hızlı görünümünü sağlar. Bir doğrudan raporda çalışan da kendilerine rapor edilen çalışanlar varsa, kart, **ekip göster** düğmesiyle birlikte üst bölümdeki doğrudan rapor sayısını görüntüler. Her kartın üzerindeki seçenekler seçili çalışana uygulanır. Örneğin, bir çalışan adına bir bırakma talebi girmek istiyorsanız, çalışanı seçer ve sonra da kartların üstünde **İzin isye**'yi seçersiniz. 

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

**Pozisyonlar** sekmesi, çalışanların birincil pozisyonlarındaki Özet görünümünü sağlar. Ad, döşeme ve departman, her kartın başlık alanında görüntülenir. Bu kart şunları içerir:

- **Kıdem tarihi** -çalışan formunun alt Özet bölümünden görüntülenir
- **Hizmet yılları** - Çalışanın istihdam başlangıç tarihine göre hesaplanan yılları
- **Önceki pozisyonların sayısı** - pozisyon geçmişine göre bu sayıyı seçmek, daha önce tutulan tüm pozisyonların ayrıntılı görünümünü açar
- **Doğum tarihi** - çalışanın Doğum tarihinin ay ve günü

Hem doğrudan hem de genişletilmiş raporların konum verilerini görüntüleyebilirsiniz.

#### <a name="compensation-tab"></a>Ücret sekmesi

**Ücret** sekmesi çalışanın yıllık maaşını görüntüler. Bir şirket tanımlayıcısı maaş tutarının altında görüntülenir. Bir çalışan birden fazla işe sahip ise ve çoklu tüzel kişiliklerden ödeme alıyorsa çalışanın birden çok ücret planı olacaktır. Şirketler arasında geçiş yapmadan tüzel kişiliklerdeki tüm maaş planlarını görmek için, **İnsan Kaynakları > Paylaşılan parametreler > Gelişmiş erişim > Şirketler arası ücretlendirmeyi etkinleştir**'in altında çapraz ücretlendirmeyi etkinleştirmeniz gerekir.

Maaş geçmişini görüntülemek için, **Ayrıntılar** formunun açılacağı maaş tutarını seçin. **Ücret** formunda yalnızca geçerli ve geçmişe ait sabit ve değişken maaş kayıtları görüntülenebilir. Bir çalışan birden fazla işe sahip ise, şirketler arasında geçiş yaparak her bir şirketteki maaş geçmişini görüntüleyebilir veya İnsan Kaynakları Paylaşılan parametrelerde şirketler arası ücreti etkinleştirerek tüm ücret planlarını görüntüleyebilirsiniz.

Hem doğrudan hem de genişletilmiş raporların ücreti görüntüleyebilirsiniz.

#### <a name="leave-and-absence-tab"></a>İzin ve devamsızlık sekmesi

**İzin ve devamsızlık** sekmesi, faaliyeti olan çalışanların en üst bakiyelerini görüntüler. Eylem yapmak veya tam faaliyet listesini görmek için, **Ayrıntılar** 'ı seçin ve sonra **İzin**'ı seçin. **İzin** formundan, çalışanların zamandan daha iyi yönetilmesini sağlamak için bakiyeleri, istekleri, onaylanan zamanı ve tahmin bakiyelerini görüntüleyebilirsiniz. Organizasyonunuzun ayarlarına bağlı olarak, iş, sizin veya genişletilmiş raporlarınız için zaman kapalı da isteyebilirsiniz.

#### <a name="performance-goals-tab"></a>Performans hedefleri sekmesi

**Performans hedefleri** sekmesi, performans hedeflerini duruma göre özetler. Bir çalışanın tüm hedeflerini görmek için durum için bir sayı seçin veya **Ayrıntılardan** performans hedeflerini seçin. Yöneticiler ve çalışanlar hedefleri hedef süresine göre güncelleştirebilir.

Yöneticiler , **ekibimin** **Özet** bölümünde **ekip performans hedefleri** döşemesi aracılığıyla takımlarına ait tüm hedefleri görebilir.

#### <a name="reviews-tab"></a>İncelemeler sekmesi

**İncelemeler** sekmesi, çalışanın her durumunda sahip olduğu İncelemeleri özetler: **Devam ediyor**, **gözdengeçirilmek üzere hazır** ve **Son İnceleme**. Bir çalışanın incelemesine erişmek için, **Ayrıntılar** düğmesini seçin ve üzerinde işbirliği yapılacak İncelemeleri seçin. Gözden geçirme işleminin iş akışı sürecinde olduğu yere göre, incelemenin güncelleştirme için kullanılabilir olup olmadığını görebilirsiniz. 

Yöneticiler , **ekibimin** **Özet** bölümünde **ekip performans incelemeleri** döşemesi aracılığıyla takımlarına ait tüm incelemeleri görebilir.

[!INCLUDE[footer-include](../includes/footer-banner.md)]