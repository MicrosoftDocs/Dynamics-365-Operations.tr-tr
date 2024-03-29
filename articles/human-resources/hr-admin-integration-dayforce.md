---
title: Dayforce ile tümleştirmeyi yapılandırma
description: Bu makalede, Microsoft Dynamics 365 Human Resources ile Ceridian Dayforce arasındaki tümleştirme için gereken yapılandırma adımları açıklanmaktadır.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PersonnelIntegrationConfiguration
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5a5d296dd4c1b09065fc47673dd540d8c122c482
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896148"
---
# <a name="configure-integration-with-dayforce"></a>Dayforce ile tümleştirmeyi yapılandırma


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources ile Ceridian Dayforce arasındaki tümleştirme, bu makalede açıklanan çeşitli yapılandırma adımlarına dayanır. Ödeme işlemini işlemeden önce tümleştirmeyi hem Human Resources'ta hem de Dayforce'ta yapılandırmanız gerekir.

Ödeme işlemlerini tamamlamak için Dayforce gibi bir hizmet kullandığınızda tümleştirmeyi Human Resources'ta etkinleştirmeniz gerekir. Tümleştirme için Human Resources'tan özel veriler gerekir. Bu nedenle, Dayforce ile eşlenmiş verilerin Human Resources'ta tümleştirmeyi destekleyecek şekilde yapılandırıldığını doğrulamanız gerekir. Tümleştirme, aşağıdaki geniş veri kategorilerini kullanır:

- İnsan kaynakları verileri
- Ücret verileri
- Ödeme döngüleri, ödeme dönemleri ve kazanç kodları gibi bordro verileri
- Çalışan verileri

Bu makalede, tümleştirmeyi etkinleştirmek için izlemeniz gereken adımlar ve tümleştirmenin gerektirdiği veri türleri ve yapılandırma ayrıntıları açıklanmaktadır.

## <a name="enable-the-integration"></a>Tümleştirmeyi etkinleştirme

Human Resources'ta yapılandırmayı açmanız ve Dayforce'a bağlanmak için yapılandırma bilgilerini girmeniz gerekir. Microsoft Dynamics 365 Finance'e aktarılmak üzere oluşturulan genel muhasebe hareketini istiyorsanız ayrıca bir Microsoft Azure depolama hesabı oluşturmanız ve Finance'te Azure Depolama bağlantı dizesini de girmeniz gerekir.

Human Resources'ta tümleştirmeyi açmak için aşağıdaki adımları izleyin.

1. **Sistem yönetimi** sayfasında **Tümleştirme yapılandırması**'nı seçin.
2. Güvenli Dosya Aktarım Protokolü (FTP) uç noktasını ve güvenli FTP klasörü yolunu girin.
3. Güvenli FTP uç noktasına ve klasör yoluna erişecek kullanıcının kullanıcı adını ve parolasını girin.
4. Bağlantıyı gerektiği gibi test edin ve **Bordro tümleştirmesini etkinleştir** seçeneğini **Evet** olarak ayarlayın.

Tümleştirme açıldığında veri dışa aktarma paketi ve dosyalar oluşturulur ve sıklık ayarlanır. Bu sıklığı ihtiyaç duyduğunuz şekilde değiştirebilirsiniz.

Azure depolama hesapları ve Azure Depolama bağlantı dizeleri hakkında daha fazla bilgi için aşağıdaki Azure konularına bakın:

- [Azure depolama hesapları hakkında](/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [Azure Depolama bağlantı dizelerini yapılandırma](/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a>Bordro tümleştirmesinin etkinleştirilmesinin teknik ayrıntıları

Bordro tümleştirmesinin açılmasının iki temel etkisi vardır:

- "Bordro tümleştirmesini dışa aktar" adlı dışa veri aktarma projesi oluşturulur. Bu proje, bordro tümleştirmesi için gerekli olan varlıkları ve alanları içerir. Projeyi incelemek için **Sistem yönetimi**'ne gidin, **Veri yönetimi** kutucuğunu seçin ve ardından projeler listesinden veri projesini açın.
- Bu toplu iş, veri dışa aktarma projesini yürütür, sonuçta elde edilen veri paketini şifreler ve veri paketi dosyasını **Tümleştirme Yapılandırması** ekranında yapılandırılan SFTP son noktasına aktarır.

> [!NOTE]
> SFTP son noktasına aktarılan veri paketi, pakette benzersiz bir anahtar kullanılarak şifrelenir. Anahtar yalnızca Ceridian tarafından erişilebilen bir Azure Key Vault'ta yer alır. Veri paketi içeriğinin şifresini çözmek ve içeriği incelemek mümkün değildir. Veri paketinin içeriğini incelemeniz gerekiyorsa "Bordro tümleştirmesini dışa aktar" veri projesini el ile dışa aktarmanız, indirmeniz ve sonra açmanız gerekir. El ile dışa aktarmada şifreleme uygulanmaz veya paket transfer edilmez.

## <a name="configure-your-data"></a>Verilerinizi yapılandırma 

Bordro işlemek için Human Resources'ta insan kaynağı verilerini yapılandırmanız gerekir. Kazanç ve ücret bilgileriyle birlikte işler ve pozisyonlar gibi kurumsal verileri ayarlamanız gerekir. Bu bilgiler personel ödemesi oluşturmak için gerekli olan istihdam, ödeme ve kesinti bilgilerini sağlar.

### <a name="human-resource-data"></a>İnsan kaynağı verileri

#### <a name="benefits"></a>Kazançlar 

İnsan kaynakları, bir kuruluşun çalışanları için sunduğu veya işlediği kazançları, kesintileri ve çalışan ücret planlarını ayarlamak ve bunları yönetmek için kullanılan araçları sağlar.

Kazançları oluştururken Dayforce'ta kullanılan aşağıdaki verileri ve yapılandırmaları göz önünde bulundurun.

##### <a name="benefit-plans"></a>Kazanç planları

- Plan (gerekli)
- Tür (gerekli)
- Bordro etkisi (gerekli)
- Borçları kurtar
- Kesinti yöntemi
- Kesinti önceliği
- Dönemi sınırla
- Sınır tutar

##### <a name="benefits"></a>Kazançlar

- Plan (gerekli)
- Tür (gerekli)
- Seçenek (gerekli)
- Kazanç Kodu (gerekli)
- Sıklık
- Temel
- Tutar veya oran
- Kazanç kodu

##### <a name="supported-frequencies"></a>Desteklenen sıklıklar 

- Haftalık
- İki haftada bir
- Yarım aylık
- Aylık

##### <a name="supported-bases"></a>Desteklenen tabanlar 

- Sabit tutar
- Kazançların yüzdesi
- Üretime yönelik saatler

Dayforce, kazanç planında tanımlanan bordro etkisine göre aşağıdaki kesintileri oluşturur.

| Human Resources'ta seçim        | Dayforce'ta sonuç                            |
|----------------------------|-----------------------------------------------|
| Hiçbiri                       | Kesinti oluşturulmaz.                      |
| Yalnızca kesinti             | Personel kesintisi oluşturulur.             |
| Yalnızca katkı          | İşveren kesintisi oluşturulur.             |
| Kesinti ve katkı | Personel ve işveren kesintileri oluşturulur. |

Kazanç programı tanımlama ve yönetme hakkında daha fazla bilgi için aşağıdaki konulara bakın:

- [Personel kazançları programı oluşturma](/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [Yeni kazanç oluşturma](/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [Kazanç uygunluk kurallarını ve ilkelerini tanımlama](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [Çalışanlara kazanç kaydetme ve çalışanlardan kazanç kaldırma](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a>Ücret 

Ücret yönetimi, temel maaş ve ikramiyelerin teslimatının denetimi için kullanılır. Bir personelin sabit temel maaşı ve başarı artışı, sabit ücret planları aracılığıyla denetlenir. İkramiyelerin ödemesi, örneğin prim ödemeleri, performans ödülleri, hisseler, hibeler ve ayrıca da tek seferlik ödüller, değişken ücret planları tarafından denetlenir.

Dayforce personelin saatlik veya yıllık ücretlerini hesaplamak için ücret bilgilerini kullanır. Sabit ücret planları ve ödeme oranı dönüştürmeleri gereklidir. Personelin bir sabit ücret planıyla ilişkilendirilmeleri gerekir.

Ücret planları hakkında daha fazla bilgi için aşağıdaki konulara bakın:

- [Sabit ücret planları oluşturma](/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [Değişken ücret planları oluşturma](/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [Maaş/ücret yapısı ve planları geliştirme](/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [İşlem ücreti](/dynamics365/unified-operations/talent/process-compensation)
- [Ücret işlemini tanımlama ve sonuçları hesaplama](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [Personeli sabit ücret planına kaydetme](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [Personeli değişken ücret planına kaydetme](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a>İşler 

Bir iş, işi gerçekleştiren kişiden beklenen görev ve sorumlulukların toplamıdır. Daha fazla bilgi için aşağıdaki konulara bakın:

- [İşin bileşenlerini ayarlama](/dynamics365/unified-operations/talent/create-job)
- [Yeni işler tanımlama](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a>Pozisyonlar

Bir pozisyon, bir işin bireysel eşdüşümüdür. Örneğin, "Satış yöneticisi (Doğu)" pozisyonu, "Satış yöneticisi" işiyle ilişkilendirilmiş pozisyonlardan biridir. Bir pozisyon, bir departmanda bulunur. Her pozisyonla yalnızca bir çalışan ilişkilendirilebilir.

Pozisyonları ayarlarken aşağıdaki verileri ve yapılandırmayı göz önünde bulundurun:

- Pozisyon (gerekli)
- Açıklama (gerekli)
- İş (gerekli)
- Departman (gerekli)
- Pozisyon türü (gerekli)
- Tam zamanlı eşdeğeri
- Yıllık mesai saatleri (gerekli)
- Tüzel kişilik tarafından ödenen (gerekli)
- Ödeme döngüsü (gerekli)
- Varsayılan mali boyut – Maliyet merkezi (gerekli)
- Çalışan ataması: Çalışan, atama başlangıç tarihi, atama bitiş tarihi, neden kodu

Aynı departmanda birden fazla pozisyon aynı işle ilişkilendirilmişse bunlar Dayforce'ta tek bir pozisyonda konsolide edilir.

Daha fazla bilgi için aşağıdaki konulara bakın:

- [Departmanlar, işler ve pozisyonları kullanarak iş gücünüzü düzenleme](/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [Pozisyonları ayarlama](/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a>Departmanlar

Bir bölüm bir kuruluşun bir kategori veya işlevsel alanını temsil eden işletme bir birimdir. Departman satış, muhasebe veya İnsan kaynakları gibi kuruluşun belirli bir alanından sorumludur. İşlevsel alanlara bildirmek için bölümleri kullanabilirsiniz. Departmanların kâr ve zarar sorumluluğu olabilir.

Daha fazla bilgi için aşağıdaki konulara bakın:

- [Departman oluşturma ve departman hiyerarşisi ile ilişkilendirme](/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [Yeni departmanlar tanımlama](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a>Ödeme döngüleri ve ödeme dönemleri

Ödeme döngüsü, bordronun ne sıklıkta çalıştırıldığını ve çalışanlara ödeme yapılan belirli günleri belirler. Örneğin, bir ödeme döngüsü aylık olabilir ve personele ayın son günü ödeme yapılabilir. Alternatif olarak, bir ödeme döngüsü haftalık olabilir ve personele ödeme döneminin bitişinden sonraki Salı günü ödeme yapılabilir. Ödeme döngüleri, bu pozisyonlardaki çalışanlara ne zaman ödeme yapıldığını kontrol etmek için pozisyonlara atanır.

Ödeme döngülerini oluşturduktan sonra her döngü için ödeme dönemleri oluşturabilirsiniz. Her ödeme dönemi, sağladığınız bilgilere göre varsayılan bir ödeme tarihi içerir. Ancak ödeme döneminin bir tatil gününe denk gelmesi gibi istisnalara izin vermek için ödeme döneminde varsayılan ödeme tarihini değiştirebilirsiniz.

Dayforce'ta aşağıdaki bilgiler kullanılır:

- Ödeme döngüsü (gerekli)
- Ödeme döngüsü sıklığı (gerekli)
- Dönem başlangıç tarihi (ilk ödeme dönemi gerekir)
- Varsayılan ödeme tarihi (ilk ödeme dönemi gerekir)

Bu bilgiler ödeme grupları olarak Dayforce ile tümleştirilir ve her ödeme döngüsü için ülke veya bölgeye göre ayrılır. Tümleştirmeden önce en az bir ödeme dönemi oluşturulmalıdır. Dayforce, ilk ödeme döneminin başlangıç tarihine ve Human Resources'ta ayarlanan varsayılan ödeme tarihine bağlı olarak ödeme grubu takvimlerini ve ödeme tarihlerini oluşturur.

#### <a name="earning-codes"></a>Kazanç kodları

Kazanç kodları, çalışanların aldığı her tür kazancı benzersiz olarak tanımlar. Kodlar, muhasebe kuralları, vergi kanunları, raporlama gereksinimleri ve brütleştirme özelliği gibi kazançlarla ilgili çeşitli parametrelere sahiptir.

Dayforce'ta aşağıdaki bilgiler kullanılır:

- Kazanç Kodu (gerekli)
- Tanım
- Ölçü birimi
- Üretken

### <a name="worker-data"></a>Çalışan verileri

Sahip olduğunuz çeşitli çalışan türlerine ilişkin kayıtlar, insan kaynaklarınız ve bordro sistemleriniz için önemlidir. Girdiğiniz bilgiler çalışanları ve kişisel bilgileri izlemek için kullanılabilir.

Çalışanlar hakkında aşağıdaki bilgileri koruyabilirsiniz:

- **Temel**: İletişim bilgileri, demografik bilgiler, kimlik bilgileri, aile bilgileri, askerlik hizmeti durumu, göçmenlik bilgileri ile kişisel ve acil durum iletişim kişileri gibi temel bilgileri tutun.
- **İstihdam**: Şirket veya kuruluş ilişkisi, pozisyon ataması, başlangıç ve bitiş tarihleri, iş uygunluğu, istihdam koşulları, emeklilik, tatil ve tayin bilgileri gibi bir çalışanın istihdamıyla ilgili bilgileri tutun.
- **İzin ve devamsızlık**: Çalışma takvimleri, devamsızlık işlemleri ve devamsızlık ayarı gibi bir çalışanın devamsızlığıyla ilgili bilgileri tutun.
- **Ücret ve bordro**: Plan kaydı, ödüller, performans, komisyon, vergi bilgileri, emeklilik ve maaş kesintileri gibi bir çalışanın ücret planlarıyla ilgili bilgileri ve bordro bilgilerini tutun.

Çalışan bilgilerini girerken Dayforce'ta kullanılan aşağıdaki verileri ve yapılandırmaları göz önünde bulundurun.

#### <a name="general-information"></a>Genel bilgiler

- Personel numarası (gerekli)
- Ad (gerekli)
- Soyadı (gerekli)
- İkinci adı
- Kıdem tarihi
- Bilinen hali

#### <a name="personal-information"></a>Kişisel bilgiler

- Medeni durum (gerekli)
- Doğum tarihi (gerekli)
- Cinsiyet (gerekli)
- Engelli kişi
- Uyruğu ülkesi bölgesi (yalnızca Meksika için)

#### <a name="address-information"></a>Adres bilgileri

- Birincil (gerekli)
- Ülke/bölge (gerekli)
- Posta kodu (gerekli)
- Cadde Numarası (gerekli) (Yalnızca Meksika için)
- Bina Tamamlayıcı (yalnızca Meksika için)
- Şehir (gerekli)
- İl (gerekli)
- Ülke (gerekli)

#### <a name="contact-information"></a>İletişim bilgileri 

- Birincil (gerekli)
- İlgili kişi numarası (gerekli)
- Dahili

#### <a name="payroll-information-and-earning-codes"></a>Bordro bilgileri ve kazanç kodları

Personele belirli bir ödeme sıklığında özel kazançlar atanabilir ve çalışanlar, tercih edilen bir ödeme yöntemine sahip olabilir. Bu tercihlerin ve ayarların kullanıldığının sağlanmasına yardımcı olmak için Dayforce'ta aşağıdaki alanlar kullanılır.

##### <a name="earning-codes"></a>Kazanç kodları

- Pozisyon (gerekli)
- Kazanç Kodu (gerekli)
- Sıklık (gerekli)
- Tutar (gerekli)

##### <a name="payroll-information"></a>Bordro bilgileri

- Ödeme Yöntemi
- Ekonomik Bölge (gerekli)
- Personel Kazanç Kodu
- Ulusal Kimlik Numarası (gerekli)
- Askerlik Hizmet Numarası
- Vardiya Kodu (gerekli)
- Vergi Numarası (gerekli)
- Sendika Kodu (gerekli)
- İş Günü Kodu (gerekli)
- Çalışma İzni Numarası

> [!NOTE]
> Meksika'da ödeme yöntemleri olarak **Nakit**, **Çek** (şirketin fiziksel çeki) ve **Elektronik Ödeme** desteklenir. Hiçbir ödeme yöntemi belirtilmemişse varsayılan olarak **Çek** kullanılır.

#### <a name="employment-details"></a>İstihdam ayrıntıları

İstihdam ayrıntıları geçmişi, personelin Dayforce'ta işe alma, işten çıkarma ve yeniden işe alma durumlarını oluşturmada temel bilgi olarak kullanılır. Dayforce, bir defada yalnızca bir etkin istihdam kaydını destekler.

- İşe başlama tarihi (gerekli)
- İş bitiş tarihi
- Başlangıç tarihi
- Ayarlanan başlama tarihi
- İşten çıkarma tarihi (işten çıkarma halinde gereklidir)
- İşten çıkarma nedeni (işten çıkarma halinde gereklidir)

Personelin önemli tarihleri aşağıdaki bilgiler kullanılarak türetilir.

| İnsan Kaynakları                | Dayforce                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| En son işe alma tarihi | Geçerli sonlandırılmamış işe başlama tarihi istihdam geçmişi kaydı                                 |
| İşten çıkarma tarihi      | Geçerli sonlandırılmamış işten çıkış tarihi istihdam geçmişi kaydı                                 |
| Başlangıç tarihi            | Ayarlanan başlama tarihi, başlama tarihi veya geçerli etkin olmayan işe başlama tarihi istihdam geçmişi kaydı |
| Orijinal işe alma tarihi    | En erken işe başlama tarihi istihdam geçmişi kaydı                                               |

#### <a name="compensation"></a>Ücret

Bir istihdam dönemi boyunca her personelin birincil pozisyonu ile sabit ücret planı ilişkilendirilmelidir. Bu dönem personelin işe alındığı (veya işe başlama tarihi) tarihte başlar ve işten çıkış tarihine kadar devam eder.

- Yürürlük Tarihi (gerekli)
- Son kullanma tarihi
- Ödeme Oranı (gerekli)
- Ödeme Oranı Dönüştürmeleri (gerekli)
- Yıllık eşdeğer (gerekli)
- Saatlik eşdeğer (gerekli)

Saatlik personelin birden fazla pozisyonu varsa birincil pozisyonun sabit ücreti, personel düzeyinde taban oranı/maaş olarak Dayforce'ta içe aktarılır. Birincil olmayan pozisyonlar için saatlik oran Dayforce'ta ilgili pozisyona kaydedilir.

Maaşlı personelin birden fazla pozisyonu varsa tüm etkin pozisyonlar için kümülatif saat oranı ve yıllık maaş oluşturulur ve personel düzeyinde taban oranı/maaş olarak türetilir.

#### <a name="identification-numbers"></a>Kimlik numaraları

##### <a name="social-security-identifier"></a>Sosyal Güvenlik Kimlik Tanımlayıcı 

Her personelin bir birincil kimlik tanımlayıcısı olması gerekir. Bu kimlik tanımlayıcı **SSK** kimlik türünde olmalıdır. Dayforce'ta bu, personelin işe alınması için gereken Sosyal Güvenlik kimlik tanımlayıcı olarak otomatik türetilir.

- Birincil (gerekli)
- Kimlik Türü = "SSN"
- Verildiği Tarih
- Bitiş Tarihi

Personel, **SSN** kimlik türü için birden fazla kimlik numarası bildirebilir. Ancak numaranın etkin veya süresinin dolmuş olup olmadığına bakılmaksızın yalnızca **Birincil** olarak işaretlenen kayıt Dayforce'a tümleştirilir.

#### <a name="bank-accounts-and-disbursements"></a>Banka hesapları ve tahsilatlar

Banka hesabı transferleri aracılığıyla ödeme yapılmasını tercih eden personel için geçerli banka hesap bilgileri girilmelidir.

| İnsan Kaynakları                         | Dayforce                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| Banka hesap numarası (gerekli) |                                                                                                             |
| SWIFT kodu (gerekli)          | Meksika'da bordro işlemleri için **Banka Kodu** alanı kullanılır.                                                             |
| Şube numarası (gerekli)       |                                                                                                             |
| Banka hesabı türü (gerekli)   | Meksika'da bordro işlemleri için **Hesap türü** alanı kullanılır. Desteklenen değerler **Cari** ve **Bordro**'yu içerir. |

> [!NOTE]
> Banka hesabı transferleri aracılığıyla ödeme yapılmasını tercih eden personel, birincil adresi Meksika'da olan ve bir Meksika bankasındaki geçerli bir banka hesabıyla ilişkilendirilmiş tüzel kişilik altında bulunan bir bakiye hesabına bağlantı sağlamalıdır. Bakiye hesabı olmayan diğer hesaplar dikkate alınmaz.

#### <a name="address-information"></a>Adres bilgileri

Her personelin bir birincil konumu olması gerekir. Dayforce'ta bu konum, personelin vergiye esas birincil ikamet yerini belirlemek için kullanılır.

- Birincil (gerekli)
- Ülke/bölge (gerekli)
- Posta kodu (gerekli)
- Cadde (gerekli)
- Cadde Numarası (gerekli)
- Bina Tamamlayıcı
- Şehir (gerekli)
- İl (gerekli)
- Ülke (gerekli)

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a>Amerika Birleşik Devletleri ve Kanada’da bordro oluşturmak için verilerinizi yapılandırma

Amerika Birleşik Devletleri ve Kanada’daki personel için ödeme oluşturuyorsanız aşağıdaki öğeler yapılandırılmalıdır:

- Pozisyonlarda departmanların olması gerekir.
- Maliyet merkezleri mali boyut olarak ayarlanmalı ve varsayılan mali boyut dizesindeki ilk öğe olmalıdır.

> [!NOTE] 
> Human Resources'ı Pozisyonların bir Departman belirtmesini zorunlu kılacak şekilde yapılandırabilirsiniz. Bunu yapmak için **İnsan Kaynakları Paylaşılan Pozisyonlar > Pozisyonlar > Pozisyonlarda departmanlar gerektir**'e gidin. Bu ayarın tümleştirme için zorunlu olmasını öneririz.

### <a name="job-types"></a>İş türleri

Benzer işleri kategorilere gruplamak için iş türleri kullanılır. Amerika Birleşik Devletleri ve Kanada'da bordro işlemek için iş türleri gereklidir. İş türü örnekleri arasında tam zamanlı ve yarı zamanlı veya maaş ve saatlik ödeme yer alır. İş türleri, personelin saatlik veya maaşlı olduğunu belirten ödeme türleri olarak Dayforce'a eşlenir.

Aşağıdaki iş türleri ve açıklamalar gereklidir.

| İş türü   | Tanım |
|------------|-------------|
| Saatlik     | Saatlik      |
| Maaşlı   | Maaşlı    |

### <a name="position-types"></a>Pozisyon türleri 

Pozisyonun tam zamanlı, yarı zamanlı veya başka bir pozisyon olduğunu tanımlamak için pozisyon türlerini kullanırsınız. Pozisyon türleri, personelin tam zamanlı veya yarı zamanlı olduğunu belirten ödeme sınıfları olarak Dayforce'a eşlenir.

Aşağıdaki pozisyon türleri ve açıklamalar gereklidir.

| Pozisyon türü   | Tanım        |
|-----------------|--------------------|
| Tam zamanlı       | Tam zamanlı personel |
| Yarı zamanlı       | Yarı zamanlı personel |

### <a name="reason-codes"></a>Neden kodları

Neden kodları personelin durumu hakkında bilgiler sağlar. Neden kodları, personelin pozisyonunda veya istihdam durumundaki değişikliklerin nedenini belirten durum nedenleri olarak Dayforce'a eşlenir.

Aşağıdaki neden kodları ve açıklamalar gereklidir.

| Neden kodu    | Tanım      | Uygulanabilir senaryolar |
|----------------|------------------|----------------------|
| RESIGNATION    | İstifa      | Çalışanı işten çıkar     |
| TERMINATION    | Bitiş      | Çalışanı işten çıkar     |
| RETIREMENT     | Emeklilik       | Çalışanı işten çıkar     |
| OTHER          | Diğer Nedenler    | Çalışanı işten çıkar     |
| DEATH          | Ölüm            | Çalışanı işten çıkar     |
| LEAVEOFABSENCE | İzin | Çalışanı işten çıkar     |
| CONTRACTEND    | Sözleşme Bitişi  | Çalışanı işten çıkar     |
| SALARYCHANGE   | Maaş Değişikliği | Ücret         |

### <a name="marital-status"></a>Medeni durum

Medeni durum değerleri Dayforce'a eşlenir ve tümleştirme işleminden sonra uygunsa kabul edilen değerlere dönüştürülür.

Aşağıdaki tabloda medeni durum değerlerinin Dayforce'a nasıl eşlendiği gösterilmektedir.

| İnsan Kaynakları                 | Dayforce             |
|------------------------|----------------------|
| Evli                | Evli              |
| Tekli                 | Tekli               |
| Dul                | Dul              |
| Boşanmış               | Boşanmış             |
| Tescilli Birliktelik | Medeni Birliktelik |
| Hiçbiri                   | Hiçbiri                 |
| Birlikte yaşıyor             | Birlikte yaşıyor           |

### <a name="gender"></a>Cinsiyet

Cinsiyet gösterimleri Dayforce'a eşlenir ve tümleştirme işleminden sonra uygunsa kabul edilen değerlere dönüştürülür.

Aşağıdaki tabloda cinsiyet gösterimlerinin Dayforce'a nasıl eşlendiği gösterilmektedir.

| İnsan Kaynakları       | Dayforce        |
|--------------|-----------------|
| Erkek         | Erkek            |
| Kadın       | Kadın          |
| Özgün değil | *Desteklenmez* |

### <a name="earning-codes"></a>Kazanç kodları

Kazanç kodları, çalışanların aldığı her tür kazancı benzersiz olarak tanımlar. Kodlar, muhasebe kuralları, vergi kanunları, raporlama gereksinimleri ve brütleştirme özelliği gibi kazançlarla ilgili çeşitli parametreleri içerir. Desteklenmeyen bir sıklık kullanılıyorsa hesaplama için **Her Ödeme** sıklığı varsayılan olarak kullanılır.

#### <a name="supported-frequencies"></a>Desteklenen sıklıklar

- Tümü
- EVERYPAY
- EACHPAYPERIOD
- EVRYOTHRPAYODD
- EVRYOTHRPAYEVN
- 1OFMTH
- LASTOFMTH
- 2OFMTH
- 3OFMTH
- 4OFMTH
- 5OFMTH
- 1N2OFMTH
- 3N4OFMTH
- 1N3OFMTH
- 1N4OFMTH
- 2N3OFMTH
- 2N4OFMTH
- 1N2N3OFMTH
- 1N2N4OFMTH
- 1N3N4OFMTH
- 2N3N4OFMTH
- 1N2N3N4OFMTH - 1N2N3N4OFMTH
- 2N3N4N5OFMth - 2N3N4N5OFMth
- 1OFQTR - 1OFQTR
- LASTOFQTR – LASTOFQTR
- LASTMTHOFQTR – LASTMTHOFQTR
- 1OFYEAR - 1OFYEAR
- LASTOFYEAR – LASTOFYEAR
- NOVNDECOFYEAR - NOVNDECOFYEAR

### <a name="addresses"></a>Adresler

Belirli ülke veya bölge, il ve ilçe (belediye) kodlarının tanımlanması için Dayforce'un ve ülke içi/bölge içi sağlayıcıların tanıyabileceği belirli biçimler gerekir. Şehirlere ilişkin biçim esnek olmasına rağmen, her şehir bir ille ilişkilendirilmelidir.

| İnsan Kaynakları          | Dayforce              |
|-----------------|-----------------------|
| Ülke/Bölge  | Ülke Kodu          |
| Posta Kodu | Posta Kodu           |
| İl           | İl Kodu            |
| Şehir            | Şehir                  |
| İlçe          | İlçe (Belediye) |
| Sokak          | Adres Satırı 1        |

### <a name="tax-regions"></a>Vergi bölgeleri

Vergi bölgeleri, bordro oluşturma sırasında uygulanması gereken uygun vergiyi belirlemek için kullanılır. Vergi bölgeleri, Dayforce'a konum adresleri olarak eşlenir. Varsayılan vergi bölgesi, çalışanın etkin konumuyla ilişkilendirilmelidir. 

- Vergi bölgesi (gerekli)
- Ülke/Bölge (gerekli)
- İl (gerekli)
- İlçe 
- Şehir (gerekli)

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a>Meksika'da bordro oluşturmak için verilerinizi yapılandırma

Meksika'da personel için ödeme oluşturuyorsanız aşağıdaki öğeler yapılandırılmalıdır:

- Pozisyonlarda departmanların olması gerekir.
- Maliyet merkezleri mali boyut olarak ayarlanmalı ve Varsayılan Mali Boyut dizesindeki ilk öğe olmalıdır.

### <a name="job-types"></a>İş tipleri

Benzer işleri kategorilere gruplamak için iş türleri kullanılır. Meksika'da bordro işlemek için iş türleri gereklidir. İş türü örnekleri arasında tam zamanlı ve yarı zamanlı veya maaş ve saatlik ödeme yer alır. İş türleri, personelin saatlik veya maaşlı olduğunu belirten ödeme türleri olarak Dayforce'a eşlenir.

Aşağıdaki iş türleri ve açıklamalar gereklidir.

| İş türü   | Tanım |
|------------|-------------|
| Saatlik     | MX Saatlik   |
| Maaşlı   | MX Maaşlı |

### <a name="position-types"></a>Pozisyon türleri 

Pozisyonun tam zamanlı, yarı zamanlı veya başka bir pozisyon olduğunu tanımlamak için pozisyon türlerini kullanırsınız. Pozisyon türleri, personelin tam zamanlı veya yarı zamanlı olduğunu belirten ödeme sınıfları olarak Dayforce'a eşlenir.

Aşağıdaki pozisyon türleri ve açıklamalar gereklidir.

| Pozisyon türü   | Tanım        |
|-----------------|--------------------|
| Tam zamanlı       | Tam zamanlı personel |
| Yarı zamanlı       | Yarı zamanlı personel |

### <a name="reason-codes"></a>Neden kodları

Neden kodları personelin durumu hakkında bilgiler sağlar. Neden kodları, personelin pozisyonunda veya istihdam durumundaki değişikliklerin nedenini belirten durum nedenleri olarak Dayforce'a eşlenir.

Aşağıdaki neden kodları ve açıklamalar gereklidir.

| Neden kodu            | Tanım                    | Uygulanabilir senaryolar |
|------------------------|--------------------------------|----------------------|
| DEPARTUREBEFOREPAYMENT | İlk bordrodan önce ayrılma | Çalışanı işten çıkar     |
| RESIGNATION            | İstifa                    | Çalışanı işten çıkar     |
| PENSION                | Emeklilik                        | Çalışanı işten çıkar     |
| TERMINATION            | Bitiş                    | Çalışanı işten çıkar     |
| RETIREMENT             | Emeklilik                     | Çalışanı işten çıkar     |
| ABSENTEE               | Devamsızlık                       | Çalışanı işten çıkar     |
| OTHER                  | Diğer Nedenler                  | Çalışanı işten çıkar     |
| CLOSURE                | İşletmenin Kapanması               | Çalışanı işten çıkar     |
| DEATH                  | Ölüm                          | Çalışanı işten çıkar     |
| LEAVEOFABSENCE         | İzin               | Çalışanı işten çıkar     |
| CONTRACTEND            | Sözleşme Bitişi                | Çalışanı işten çıkar     |
| SALARYCHANGE           | Maaş Değişikliği               | Ücret         |

### <a name="terms-of-employment"></a>Çalışma koşulları

İstihdam koşulları, istihdam koşullarının kategorilerini oluşturmak için kullanılır. Koşullar, istihdam göstergesi değerleri olarak Dayforce'a eşlenir.

Aşağıdaki istihdam koşulları ve açıklamalar gereklidir.

| Çalışma koşulları   | Tanım |
|-----------------------|-------------|
| Normal               | Normal     |
| Doğrudan                | Doğrudan      |
| Stajyerlik            | Stajyerlik  |
| Kalıcı             | Kalıcı   |

### <a name="marital-status"></a>Medeni durum

Medeni durum değerleri Dayforce'a eşlenir ve tümleştirme işleminden sonra uygunsa kabul edilen değerlere dönüştürülür.

Aşağıdaki tabloda medeni durum değerlerinin Dayforce'a nasıl eşlendiği gösterilmektedir.

| İnsan Kaynakları                 | Dayforce                  |
|------------------------|---------------------------|
| Evli                | Evli                   |
| Tekli                 | Tekli                    |
| Dul                | Dul                   |
| Boşanmış               | Boşanmış                  |
| Tescilli Birliktelik | Medeni Birliktelik      |
| Hiçbiri                   | *Meksika'da desteklenmez* |
| Birlikte yaşıyor             | *Meksika'da desteklenmez* |

### <a name="gender"></a>Cinsiyet

Cinsiyet gösterimleri Dayforce'a eşlenir ve tümleştirme işleminden sonra uygunsa kabul edilen değerlere dönüştürülür.

Aşağıdaki tabloda cinsiyet gösterimlerinin Dayforce'a nasıl eşlendiği gösterilmektedir.

| İnsan Kaynakları       | Dayforce                  |
|--------------|---------------------------|
| Erkek         | Erkek                      |
| Kadın       | Kadın                    |
| Özgün değil | *Meksika'da desteklenmez* |

### <a name="payment-method"></a>Ödeme yöntemi

Ödeme yöntemleri, personele ve şirkete çalışanlara nasıl ödeme yapılacağını tanımlamak için bir yol sağlar. Ödeme yöntemleri Dayforce'a eşlenir ve tümleştirme işleminden sonra uygunsa kabul edilen değerlere dönüştürülür.

Aşağıdaki tabloda ödeme yöntemlerinin Dayforce'a nasıl eşlendiği gösterilmektedir.

| İnsan Kaynakları             | Dayforce                  |
|--------------------|---------------------------|
| Nakit               | Nakit                      |
| Elektronik Ödeme | Transfer et                  |
| Denetle              | Çek                    |
| Banka Ödeme Emri         | *Meksika'da desteklenmez* |
| Diğer              | *Meksika'da desteklenmez* |

### <a name="bank-account-type"></a>Banka hesabı türü

Banka hesap türleri, personele elektronik ödeme yapmak için kullanılır. Banka hesap türleri, transfer hesabı bilgileri olarak Dayforce'a eşlenir. Banka hesap türleri, uygunsa tümleştirme işleminden sonra kabul edilen değerlere dönüştürülür.

| İnsan Kaynakları            | Dayforce                  |
|-------------------|---------------------------|
| Cari Hesap  | CheckingAccount           |
| Bordro Hesabı   | PayrollAccount            |
| Tasarruf Hesabı   | *Meksika'da desteklenmez* |
| BankGirot hesabı | *Meksika'da desteklenmez* |
| PlusGirot hesabı | *Meksika'da desteklenmez* |

### <a name="earning-codes"></a>Kazanç kodları

Kazanç kodları, çalışanların aldığı her tür kazancı benzersiz olarak tanımlar. Kodlar, muhasebe kuralları, vergi kanunları, raporlama gereksinimleri ve brütleştirme özelliği gibi kazançlarla ilgili çeşitli parametreleri içerir. Desteklenmeyen bir sıklık kullanılıyorsa hesaplama için **Her Ödeme** sıklığı varsayılan olarak kullanılır.

#### <a name="supported-frequencies"></a>Desteklenen sıklıklar

- Tümü
- EVERYPAY
- EACHPAYPERIOD
- EVRYOTHRPAYODD
- EVRYOTHRPAYEVN
- 1OFMTH
- LASTOFMTH
- 2OFMTH
- 3OFMTH
- 4OFMTH
- 5OFMTH
- 1N2OFMTH
- 3N4OFMTH
- 1N3OFMTH
- 1N4OFMTH
- 2N3OFMTH
- 2N4OFMTH
- 1N2N3OFMTH
- 1N2N4OFMTH
- 1N3N4OFMTH
- 2N3N4OFMTH
- 1N2N3N4OFMTH - 1N2N3N4OFMTH
- 2N3N4N5OFMth - 2N3N4N5OFMth
- 1OFQTR - 1OFQTR
- LASTOFQTR – LASTOFQTR
- LASTMTHOFQTR – LASTMTHOFQTR
- 1OFYEAR - 1OFYEAR
- LASTOFYEAR – LASTOFYEAR
- NOVNDECOFYEAR - NOVNDECOFYEAR

### <a name="addresses"></a>Adresler

Belirli ülke veya bölge, il ve ilçe (belediye) kodlarının tanımlanması için Dayforce'un ve ülke içi/bölge içi sağlayıcıların tanıyabileceği belirli biçimler gerekir. Şehirlere ilişkin biçim esnek olmasına rağmen, her şehir bir ille ilişkilendirilmelidir.

| İnsan Kaynakları              | Dayforce              |
|---------------------|-----------------------|
| Ülke/Bölge      | Ülke Kodu          |
| Posta Kodu     | Posta Kodu           |
| İl               | İl Kodu            |
| Şehir                | Şehir                  |
| İlçe              | İlçe (Belediye) |
| Sokak              | Adres Satırı 1        |
| Cadde Numarası       | Adres Satırı 2        |
| Bina Tamamlayıcı | Adres Satırı 5        |

### <a name="passport-number"></a>Pasaport numarası

Personel pasaport bilgilerini bildirebilir. Bu bilgiler, **Pasaport** kimlik türünü içerir ve Meksika'ya özel personel bilgilerinin bir parçası olarak Dayforce'a tümleştirilir.

- Kimlik Türü = "Pasaport"
- Verildiği Tarih
- Bitiş Tarihi

Personel, **Pasaport** kimlik türü için birden fazla kimlik numarası bildirebilir. Ancak yalnızca geçerli etkin pasaport girişi Dayforce'a tümleştirilir. Tüm pasaport girişlerinin süresi dolmuşsa en son verilen pasaport Dayforce'a tümleştirilir.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
