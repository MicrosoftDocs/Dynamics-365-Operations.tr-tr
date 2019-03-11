---
title: Attract'ta güvenlik ve rol yönetimi
description: Bu konu, Microsoft Dynamics 365 for Talent - Attract içindeki rol güvenliği hakkında bilgi sağlar.
author: josaw1
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: josaw1
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 5674df1657b46aa31e2011562f4ebbff2c16fee9
ms.sourcegitcommit: 1e32d78868098fd76124bb41363f15c4ec3ea15a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2019
ms.locfileid: "374792"
---
# <a name="security-and-role-management-in-attract"></a>Attract'te güvenlik ve rol yönetimi

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Talent: Attract rol tabanlı güvenlik kullanır. Başka bir deyişle, erişim bireysel kullanıcılara değil, kullanıcılara atanan güvenlik rollerine verilir. Bir güvenlik rolüne atanmış bir kullanıcı bu rolle ilişkilendirilen ayrıcalıkları kümesine erişebilir.

Attract, beş temel kullanıcı rolleri sağlar:

- Yönetici
- İşe Alım Müdürü
- İşe alma görevlisi
- Görüşmeci
- Salt okunur

Yönetici rolü, diğer kullanıcıları ekleme ve izinlerini değiştirme izni olan tek roldür.

- **Ekle** - Yönetici Merkezi üzerinde **Kullanıcı izinleri** sekmesinde, **Rolleri Ata**'yı seçin, eklenecek kullanıcıyı arayın ve sonra o kullanıcıya izinleri atayın.
- **Düzenle** – Kullanıcı arayın veya kullanıcıyı listede bulun, izinlerini değiştirmek için **Düzenle**'yi seçin.
- **Sil** – Bir kullanıcının izinlerini silmekle kullanıcıyı sistemden kaldırmanızsınız. Bununla birlikte, kullanıcı erişimi ve ayrıcalıklarını Attract'ta sınırlarsınız. Örneğin, Hilda İşe alma yöneticisi rolüne atanmış ve işe alma müdürü olarak bir işe eklenir. İşe alma yöneticisi rolünden Hilda daha sonra kaldırılırsa, işte işe alma müdürü olarak kalır ve yine de bu işi erişebilir. Bununla birlikte, başka iş oluşturamaz.

Aşağıdaki bölümler her rolün üst düzey bir açıklamasını sağlar. Konunun ilerleyen bölümlerindeki tablolar hakkında ayrıntılı bilgi sağlar.

> [!NOTE]
> Bazı özellikler, yalnızca Attract Kapsamlı İşe Alım eklentisinde kullanılabilir.

## <a name="administrator"></a>Yönetici

Yönetici rolüne atanan kullanıcılar Attract'ta tüm verilere erişebilir ve değiştirebilir. Yöneticiler veriler oluşturur, okur, günceller ve siler. Bunlar ayrıca Yönetici Merkezi'ne de erişebilir ve burada Attract uygulama yapılandırabilir ve kullanıcı bilgilerini ayarlar. En az bir kişi Yönetici rolüne atanması önerilir. Varsayılan olarak, Microsoft PowerApps ortam yöneticisi Attract'ta bir yönetici olarak ayarlanır. Attract'ın deneme sürümüne kaydolursanız Yönetici rolü otomatik olarak size atanır. Şu anda işler oluşturmak için Yönetici rolüne sahip kullanıcılar da İşe alan rolü veya İşe alma yöneticisi rolüne sahip olmalıdır.

## <a name="hiring-manager"></a>İşe Alım Müdürü

İşe Alma yöneticisi rolüne atanan kullanıcılar işleri oluşturabilir ve önceden oluşturulmuş işleri güncelleştirebilir. İşe alma yöneticileri, ve bu işle bir işe ve uygulamalar üzerinde yalnızca sınırlı bir dizi eylemi gerçekleştirebilir. Yalnızca İşe alma yöneticisi rolüne atanan kullanıcılar işe alma takımına işe alma müdürleri ekleyebilir.

## <a name="recruiter-role"></a>İşe alan rolü

İşveren rolüne atanan kullanıcıların oluşturdukları işlerde tam okuma, oluşturma, güncelleştirme ve silme ayrıcalıkları vardır. Bunlar aynı zamanda, sahip oldukları işleriyle ilişkili uygulamalar için oluşturma, okuma, güncelleştirme ve silme ayrıcalıklarına sahiptir. Yalnızca İşveren yöneticisi rolüne atanan kullanıcılar işe alma takımına işveren ekleyebilir.

## <a name="interviewer"></a>Görüşmeci

Bir Microsoft Azure Active Directory (Azure AD) hesabına kuruluş içinde sahip olan tüm kullanıcılar, bir işe alma takımına görüşmeci olarak eklenebilir. Görüşmeci rolüne atanan kullanıcılar, iş ayrıntıları ve işler için işe alma takımında oldukları başvurana ait verileri görüntüleyebilir. Bu işler için görüşmeciler işe alma önerileri de yapabilir ve adaylar hakkında görüş bildirir. Bununla birlikte, bunların iş ayrıntılarını veya başvurana ait verileri güncelleştiremez.

## <a name="read-only"></a>Salt okunur

Salt okunur rolüne atanan kullanıcıların salt okunur tüm verileri Attract ortamında erişebilir. Bununla birlikte, veri oluşturamaz veya düzenleyemez.

## <a name="delegated-roles"></a>Temsilci olarak atanan roller

İşe alma takımında oldukları her iş için işe alanlar ve işe alma yöneticileri, kendileri için en az bir temsilci atayabilir. Ancak, işe alma takımındaki diğer kişilerin temsilcilerini belirtemez.

Temsilciler, kendilerini belirtilen kişi ile aynı ayrıcalıklara sahip. Örneğin, işe alma müdürü kendisine ait bir iş için temsilci belirlerse temsilci, bu iş için işe alma müdürüyle aynı ayrıcalıklara sahip olur. Temsilciler, işe alma takımından diğer temsilcileri kaldıramaz. Ayrıca kendilerini temsilci olarak atayan kişileri kaldıramazlar.

## <a name="job-details-and-actions"></a>İş ayrıntıları ve eylemleri

İşveren veya işe alma yöneticisi rolüne sahip kullanıcılar işler oluşturabilir. Aşağıdaki ayrıcalıklar, iş ayrıntıları ve işler üzerinde gerçekleştirilebilecek eylemlerde uygulanır.

| Veri veya eylem    | İşe alma görevlisi | İşe Alım Müdürü | Görüşmeci |
|-------------------|-----------|----------------|-------------|
| İş ayrıntıları       | O kullanıcının işe alma takımında olduğu işleri oluşturma, okuma, güncelleştirme ve silme | O kullanıcının işe alma takımında olduğu işleri oluşturma, okuma, güncelleştirme ve silme | Salt okunur |
| İşe alım takımı       | O kullanıcının işe alma takımında olduğu işleri oluşturma, okuma, güncelleştirme ve silme | O kullanıcının işe alma takımında olduğu işleri oluşturma, okuma, güncelleştirme ve silme | Salt okunur |
| İş İlanı Yayımlama       | O kullanıcının işe alma takımında olduğu işleri oluşturma, okuma, güncelleştirme ve silme | Salt okunur | Salt okunur |
| İşlem           | O kullanıcının işe alma takımında olduğu işleri oluşturma, okuma, güncelleştirme ve silme | O kullanıcının işe alma takımında olduğu işleri oluşturma, okuma, güncelleştirme ve silme | Salt okunur |
| Başvuran Ekle    | Kullanıcının işe alma takımında olduğu işler için başvuran ekle | Kullanıcının işe alma takımında olduğu işler için başvuran ekle | İzin verilmiyor |
| Aday Ekle     | Kullanıcının işe alma takımında olduğu işler için adaylar ekle | Bir yapılandırma seçeneği, [Aday müşteri faaliyet kurulumu](./activities-attract.md#prospect-activity), görüşmecilerin müşteri adayı ekleyip görüntüleyebileceğini kontrol eder. | İzin verilmiyor |
| İş etkinleştir      | Kullanıcının işe alma takımında olduğu işleri etkinleştirin | Kullanıcının işe alma takımında olduğu işleri etkinleştirin | İzin verilmiyor |
| İşi kapat         | Kullanıcının işe alma takımında olduğu işleri kapatın | İzin verilmiyor | İzin verilmiyor |
| İşi sil        | Kullanıcının işe alma takımında olduğu işleri silin | Yalnızca işe hiçbir başvuranları eklenmediyse | İzin verilmiyor |
| Başvuranları sil | Kullanıcının işe alma takımında olduğu başvuranları silin | İzin verilmiyor | İzin verilmiyor |

## <a name="application-details-and-actions"></a>Başvuru ayrıntıları ve eylemleri

Aşağıdaki ayrıcalıklar, başvuranların işle ilgili verileri ve başvurular üzerinde gerçekleştirilebilecek eylemlerde uygulanır.

| Veri veya eylem          | İşe alma görevlisi | İşe Alım Müdürü | Görüşmeci |
|-------------------------|-----------|----------------|-------------|
| Başvuru belgeleri   | O kullanıcının işe alma takımında olduğu işleri oluşturma, okuma, güncelleştirme ve silme | O kullanıcının işe alma takımında olduğu işleri oluşturma, okuma, güncelleştirme ve silme | Salt okunur |
| Uygulama Notları       | O kullanıcının işe alma takımında olduğu işleri oluşturma, okuma, güncelleştirme ve silme | O kullanıcının işe alma takımında olduğu işleri oluşturma, okuma, güncelleştirme ve silme | Oluştur |
| Başvuru Faaliyeti    | Kullanıcı işe alma takımındaysa görüntüle | Kullanıcı işe alma takımındaysa görüntüle | Salt okunur |
| Başvuru geri bildirimi    | Kullanıcı işe alma takımdaysa tüm geri bildirimleri ekle ve görüntüle | Kullanıcı işe alma takımdaysa tüm geri bildirimleri ekle ve görüntüle | Geribildirim ekleyebilirsiniz\*\* |
| Başvuruyu reddet      | Kullanıcı işe alma takımındaysa reddedebilir | İzin verilmiyor | İzin verilmiyor |
| Aşamayı ilerlet           | Kullanıcı işe alma takımındaysa reddedebilir | Kullanıcı işe alma takımındaysa ilerleyebilir | İzin verilmiyor |
| Teklif yönetimi başlat | Teklif yönetimini başlatabilir | Teklif faaliyeti üzerinde bir yapılandırma seçeneği vardır. | İzin verilmiyor |

\*\*[Geri bildirim faaliyet kurulumu](activities-attract.md#feedback-activity) içindeki yapılandırma seçeneği, görüşmecilerin birbirinin geribildirimini görüp görmediğini denetler.

## <a name="process-templates"></a>Süreç şablonları

Aşağıdaki ayrıcalıklar işe alma işlem şablonları için geçerlidir. Ekip üyelerinin şablonları oluşturma ve düzenleme yetenekleri Yönetici merkezindeki **Şablon yönetiminde** yapılandırılmıştır. Şablon yönetimi etkinse, işe alanlar ve işe alma müdürleri kendi işlem şablonlarını oluşturup düzenleyebilir. Şablon yönetimi devre dışı bırakılırsa, yalnızca yöneticiler şablonlar oluşturabilir ve düzenleyebilir. Aşağıdaki tabloda şablon yönetiminin açık durumda olduğunu kabul eder.

| Veriler              | İşe alma görevlisi                                           | İşe Alım Müdürü                                      | Görüşmeci |
|-------------------|-----------------------------------------------------|-----------------------------------------------------|-------------|
| Süreç şablonları | Kullanıcının oluşturduğu şablonlara tam ayrıcalık | Kullanıcının oluşturduğu şablonlara tam ayrıcalık | Erişim yok   |

## <a name="email-and-email-templates"></a>E-posta ve e-posta şablonları

Aşağıdaki ayrıcalıklar, e-posta şablonları ve e-postalar üzerinde gerçekleştirilebilecek eylemlerde uygulanır. Yalnızca yöneticiler e-posta şablonları oluşturabilir ve düzenleyebilir.

| Veri veya eylem     | İşe alma görevlisi          | İşe Alım Müdürü     | Görüşmeci |
|--------------------|--------------------|--------------------|-------------|
| E-posta şablonları    | Salt okunur erişim   | Salt okunur erişim   | Erişim yok   |
| E-posta gönder         | Etkinlik başına gönder  | Etkinlik başına gönder  | Erişim yok   |
| E-posta içeriği düzenle | E-posta içeriği düzenle | E-posta içeriği düzenle | Erişim yok   |

## <a name="talent-pools"></a>Yetenek havuzları

Beceri havuzlarında aşağıdaki ayrıcalıkları geçerlidir. Oluşturan kişi paylaşmayı seçmedikçe beceri havuzları, yalnızca oluşturan kişi tarafından görülebilir. Aday araması, adlandırılmış bir havuza eklenmemiş adayları aramak için kullanılabilir.

| Veri veya eylem   | İşe alma görevlisi                                       | İşe Alım Müdürü                                  | Görüşmeci |
|------------------|-------------------------------------------------|-------------------------------------------------|-------------|
| Adlandırılmış havuz       | Kullanıcının oluşturduğu havuzlara tam ayrıcalık | Kullanıcının oluşturduğu havuzlara tam ayrıcalık | Erişim yok   |
| Havuzu paylaş       | Yalnızca kullanıcı tarafından oluşturulan havuzları                | Yalnızca kullanıcı tarafından oluşturulan havuzları                | Erişim yok   |
| Aday arama | Tam arama yetenekleri                        | Tam arama yetenekleri                        | Erişim yok   |

## <a name="candidates"></a>Adaylar

Adaylar, beceri havuza eklenen ancak bir işle ilişkili olmayan kişilerdir.

| Veriler                        | İşe alma görevlisi                        | İşe Alım Müdürü                   | Görüşmeci |
|-----------------------------|----------------------------------|----------------------------------|-------------|
| Profil - aday ayrıntıları | Oluşturma, okuma, güncelleştirme ve silme | Oluşturma, okuma, güncelleştirme ve silme | Erişim yok   |
| Belgeler                   | Oluşturma, okuma, güncelleştirme ve silme | Oluşturma, okuma, güncelleştirme ve silme | Erişim yok   |
