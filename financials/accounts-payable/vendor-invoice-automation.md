---
title: "Satıcı faturası otomasyonu"
description: "Bu konu ekler içeren faturalar da dahil olmak üzere satıcı faturalarının uçtan uca otomasyonu için kullanılabilir olan özellikleri açıklar."
author: twheeloc
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: 5bfde00f88a12711c2519aaea19dd7a48196a828
ms.contentlocale: tr-tr
ms.lasthandoff: 06/20/2017

---
# <a name="vendor-invoice-automation"></a>Satıcı faturası otomasyonu

Bu konu ekler içeren faturalar da dahil olmak üzere satıcı faturalarının uçtan uca otomasyonu için kullanılabilir olan özellikleri açıklar.

Borç hesapları (AP) işlemlerini daha verimli kullanmak isteyen kuruluşlar genellikle fatura işlemlerini daha etkin olması gereken işlem alanları içinde ne üst sıralardan birine koyar. Çoğu durumda, bu kuruluşlar kağıt fatura işlemlerini üçüncü taraf bir optik karakter tanıma (OCR) servis sağlayıcısına aktarırlar. Daha sonra her faturanın taranan görüntüsüyle birlikte makine tarafından okunabilir fatura meta verilerini alırlar. Otomasyona yardımcı olmak için "son mil" çözümü faturalama sisteminde bu yapıların kullanımını etkinleştirmek için oluşturulmuştur. Microsoft Dynamics 365 for Finance and Operations, Enterprise sürümü şimdi bu "son mil" otomasyonunu, bir fatura otomasyon çözümüyle kullanıma hazır hale getirmektedir.

## <a name="solution-context"></a>Çözüm bağlamı

Fatura otomasyon çözümü, fatura başlığı ve fatura satırları ve faturayla ilgili ekler için fatura meta verilerini kabul edebilen standart bir arabirim sunar. Bu arabirimle uyumlu yapılar oluşturabilen her dış sistem, fatura ve eklerin otomatik işlenmesi için Finance and Operations'a akış gönderebilir.

Aşağıda Contoso'nun satıcı faturası işleme için bir OCR hizmet sağlayıcısı ile ortaklık kurduğu basit bir tümleştirme senaryosu gösterilmektedir. Contoso satıcıları servis sağlayıcısına faturaları e-posta ile gönderir. OCR işlemi aracılığıyla, hizmet sağlayıcısı fatura meta verilerini (başlığı ve/veya satırlar) ve taranan fatura görüntüsünü oluşturur. Bir tümleştirme katmanı bu yapıları dönüştürür ve böylece Finance and Operations bunları kullanabilir.

![Basit tümleştirme senaryosu](media/vendor_invoice_automation_01.png)

Fatura tümleştirme gerektiğinde önceki senaryonun çeşitli kullanımları mümkün olabilir. Veri geçiş işlemleri, Finance and Operations'da faturaları ve eklerini oluşturmak için bu arabirimin kullanılabileceği başka bir kullanım örneğidir.

### <a name="solution-components"></a>Çözüm bileşenleri

Çözümün temeli aşağıdaki bileşenlerden oluşur:

+ Fatura başlığı, fatura satırları ve fatura ekleri için veri varlıkları
+ Faturalar için özel durum işleme
+ Faturalarda yan yana ek görüntüleyici

Bu konunun kalan kısmında bu çözüm bileşenlerinin ayrıntılı açıklamaları verilmektedir.

## <a name="data-entities"></a>Veri varlıkları

Veri paketi Finance and Operations'a gönderilmesi gereken iş birimidir, böylece fatura başlıkları, fatura satırları ve fatura ekleri oluşturulabilir. Aşağıdaki veri varlıkları veri paketini oluşturan yapılan için kullanılır:

+ Satıcı faturası başlığı
+ Satıcı faturası satırı
+ Satıcı faturası belge eki

Satıcı fatura belgesi eki bu özelliğin bir parçası olarak sunulan yeni bir veri varlığıdır. Satıcı fatura başlığı varlığı ekleri desteleyecek şekilde değiştirilmiştir. Satıcı fatura satırı varlığı bu özellik için değiştirilmiştir.

Bu konu, veri paketiyle ilgili ayrıntılı bir tanımın vermez. Ayrıca veri paketlerinin nasıl oluşturulacağını da açıklamaz. Bu bilgi için bkz. [Veri varlıkları ve paketler çerçevesi](/dynamics365/en-us/unified-operations/dev-itpro/data-entities/data-entities-data-packages).

Faturaları ve ekleri içeren test verilerini hızla oluşturmak için aşağıdaki adımları izleyin.

1. Finance ve Operations kurulumunuzda oturum açın.
1. **Borç hesapları** > **Faturalar** > **Bekleyen satıcı faturaları**'na gidin.
1. Satırları ve ekleri olan faturalar oluşturun.

    > [!NOTE]
    > Ekler başlık ekleri olmalıdır. Şu anda Satıcı faturası belge eki varlığı satır eklerini desteklememektedir.

1. **Veri yönetimi** çalışma alanını açın.
1. Satıcı faturası başlığı, Satıcı faturası satırı ve Satıcı faturası belge eki varlıkları içeren bir dışa aktarma işi oluşturun.
1. Verileri dışa aktarın.
1. Dışa aktarılan verileri paket olarak indirin. Şimdi paketi test amacıyla verileri hedef kurulumlara aktarmak için kullanabilirsiniz.

### <a name="determining-the-legal-entity-for-an-invoice"></a>Bir fatura için tüzel kişilik belirleme

Veri paketleriyle içe aktarılan faturalar ait oldukları tüzel kişilikle iki şekilde ilişkilendirilebilir:

+ Faturayı işleyen içe aktarma işlemi faturayı işin **Veri yönetimi** çalışma alanında planlandığı aynı şirkete aktarır. Başka bir deyişle, işin şirketi faturanın ait olduğu şirketi belirler.
+ Faturaları içeren veri paketi Finance and Operations'a gönderdiğinde, arayan (Finance and Operations dışında çalışan tümleştirme uygulaması) HTTP isteğinde şirket kodunu açık şekilde belirtebilir. Bu durumda, Finance and Operations'da işleme işinin çalıştığı şirket bağlamı geçersiz kılınır ve faturalar HTTP isteğiyle geçirilen şirket için içe aktarılır.

> [!NOTE]
> Bu davranış standart veri yönetimi davranışıdır. Burada, faturalar bağlamında, yalnızca bütünlük açısından açıklanmıştır.

## <a name="exception-processing"></a>Özel durum işleme

Satıcı faturalarının Finance and Operations'a tümleştirme yoluyla geldiği senaryolarda, Borç hesapları ekibi üyesinin özel durumları veya başarısız olan faturaları işlemesi ve başarısız faturalardan bekleyen faturalar oluşturması için kolay bir yol olması gerekir. Satıcı faturaları için bu özel durum işleme özelliği artık Finance and Operations'ın bir parçasıdır.

### <a name="exceptions-list-page"></a>Özel durumlar listesi sayfası

Özel durumlar için yeni liste sayfası **Borç hesapları** > **Faturalar** > **İçe aktarma hataları** > **İçe aktarılamayan satıcı faturaları**'nda bulunur. Bu sayfa, Satıcı fatura başlık verileri varlığının aşamalandırma tablosundaki tüm satıcı faturası başlığı kayıtlarını gösterir. Aynı kayıtları **Veri yönetimi** çalışma alanından da görebilirsiniz ve burada özel durum işleme özelliğinde sunulan eylemlerin aynılarını gerçekleştirebilirsiniz. Ancak, özel durum işleme özelliği arabirimi işlevsel kullanıcı için optimize edilmiştir.

![Özel durumlar listesi sayfası](media/vendor_invoice_automation_02.png)

Bu liste sayfası akış ile gelen aşağıdaki alanları içerir:

+ **Şirket** – Faturanın ait olduğu şirket
+ **Hata iletisi** – Faturanın neden oluşturulamadığını açıklayan veri yönetimi çerçevesi sorunlarına ilişkin hata iletisi
+ **Numara** – Fatura numarası
+ **Fatura hesabı**
+ **Ad** - Satıcının adı
+ **Satıcı hesabı**
+ **Satınalma siparişi** - Fatura için satın alma siparişi (PO) numarası
+ **Deftere nakil tarihi**
+ **Fatura tarihi**
+ **Fatura açıklaması**
+ **Para birimi**
+ **Günlük**
+ **Satır referansı** – Dış sistemden gelen tanımlayıcı

    > [!NOTE]
    > Referans satırı fatura kodu değildir.

Bu liste sayfasında aşağıdaki şekillerde kullanabileceğiniz bir önizleme bölmesi de vardır:

+ Tam hata iletisini görmek - Böylece ızgaradaki **Kata iletisi** sütununu genişletmeniz gerekmez.
+ Faturayla birlikte gelen ek varsa, faturanın eklerinin tam listesini görmek.

Liste sayfası aşağıdaki eylemleri destekler:

+ **Düzenle** – Sorunları gidermek için özel durum kaydını düzenleme modunda açın.
+ **Seçenekler** – Liste sayfalarında kullanılabilir olan standart seçeneklere erişin. Özel durumlar liste sayfasını çalışma alanınıza liste veya kutucuk olarak sabitlemek için **Çalışma alanına ekle** seçeneğini kullanabilirsiniz.

### <a name="exception-details-page"></a>Özel durum ayrıntıları sayfası

Düzenleme modunu çalıştırdığınızda, sorunları bulunan fatura için özel durum ayrıntıları sayfası görüntülenir. Ekler varsa, fatura ve varsayılan ek özel durum ayrıntıları sayfasında yan yana görünür.

![Özel durum ayrıntıları sayfası](media/vendor_invoice_automation_03.png)

Önceki örnekte, gelen satıcı faturası başlığı için satırlar yoktu. Bu nedenle, satırlar bölümü boştu.

Özel durum ayrıntıları sayfası aşağıdaki işlemi destekler:

+ **Bekleyen fatura oluştur** – Özel durum işlemenin bir parçası olarak faturadaki sorunları giderdikten sonra, bekleyen fatura oluşturmak için bu düğmeye tıklayabilirsiniz. Bekleyen faturalar oluşturma (zaman uyumsuz işlem) arka planda gerçekleşir.

### <a name="shared-service-vs-organization-based-exception-processing"></a>Paylaşılan hizmetler ile kuruluş tabanlı özel durum işleme karşılaştırması

Özel durumlar listesi sayfası **Veri yönetimi** çalışma alanının aşamalandırma kayıtlarını işlemek için desteklediği standart güvenlik yapılarını destekler. Fatura içe aktarma işi aşağıdaki şekillerde güvenlik altına alınabilir:

+ Kullanıcı rolüne göre
+ Kullanıcıya göre
+ Tüzel kişiliğe göre

![Kullanıcı rolüne ve tüzel kişiliğe göre güvenlik altına alınan içer aktarma işlemi](media/vendor_invoice_automation_04.png)

Fatura içe aktarma işi için güvenlik yapılandırıldıysa, özel durumlar listesi bu ayarları kabul eder. Kullanıcılar, yalnızca bu kurulumun görmelerine izin verdiği fatura özel durumu kayıtlarını görebilir.

Örneğin, Contoso fatura özel durumlarını tüzel kişiliğe göre işleme kararı verir. Bu nedenle, güvenlik fatura içe aktarma işleminde A tüzel kişiliğindeki kullanıcının yalnızca A tüzel kişiliğindeki fatura özel durumlarını görmesine, B tüzel kişiliğindeki kullanıcının yalnızca B tüzel kişiliğindeki fatura özel durumlarını görmesine izin verecek şekilde yapılandırılır. Bu ayar, fatura özel durumlarının yönetimi için görev ayrımına olanak tanır.

Conotoso herhangi bir güvenlik uygulamamaya da karar verebilirdi; bu durumda aynı kullanıcılar tüm tüzel kişiliklere ait fatura özel durumlarıyla işlem yapabilirdi. Bu ayar, fatura özel durumlarının yönetimi için paylaşılan hizmetler senaryosuna olanak tanır.

## <a name="side-by-side-attachment-viewer"></a>Yan yana ek görüntüleyici

Satıcı faturalarındaki ekleri kolaylıkla görebilmeniz için, faturalama işleminde kullanılan aşağıdaki sayfalarda artık bir fatura görüntüleyici sunulmaktadır:

+ **Özel durumları işleme**
+ **Bekleyen satıcı faturaları** sayfası (fatura gözden geçirme işleminde de kullanılabilir)
+ **Fatura günlüğü** sorgu sayfası (deftere nakledilen faturalar için)

Ek görüntüleyicinin sağladığı ana işlevler:

+ Belge yönetiminin desteklediği tümek türlerini görün (dosyalar, görüntüler, URL'ler ve notlar).
+ Çok sayfalı TIFF dosyalarını görüntüleyin.
+ Görüntü dosyalarında aşağıdaki eylemleri gerçekleştirin:
  + Resmin bölümlerini vurgulayın.
  + Resmin bölümlerini engelleyin.
  + Resme ek açıklama ekleyin.
  + Resmi yakınlaştırın ve uzaklaştırın.
  + Görüntüyü kaydırın.
  + Geri al ve yinele eylemleri.
  + Resmin boyutuna sığdır.

> [!NOTE]
> Bu eylemler yalnızca resim dosyaları için (JPEG, TIFF, PNG vb.) kullanılabilir. Bu eylemleri kullanarak resimde yaptığınız tüm değişiklikler resim dosyasına kaydedilir. Şu anda, ek görüntüleyici sürüm veya denetim özellikleri içermez.

### <a name="default-attachment"></a>Varsayılan ek

Bir satıcı faturasında bir veya daha fazla ek varsa, belgelerden birini **Ekler** sayfasında varsayılan ek olarak ayarlayabilirsiniz. **Varsayılan ektir** seçeneği bu özelliğin bir parçası olarak eklenmiş olan yeni bir seçenektir. Bu seçenek aynı zamanda Satıcı faturası belge eki veri varlığı için de ortaya çıkar. Bu nedenle, varsayılan ek tümleştirmeler aracılığıyla ayarlanabilir.

Yalnızca tek bir belge varsayılan ek olarak ayarlanabilir. Bir belgeyi varsayılan ek olarak ayarladıktan sonra, bu belge fatura açıldığında otomatik olarak ek görüntüleyicide görüntülenir. Varsayılan ek olarak bir belge ayarlamazsanız, görüntüleyicisi fatura açıldığında otomatik olarak herhangi bir ek görüntülemez.

### <a name="showhide-invoice-attachments"></a>Fatura eklerini göster/gizle

**Özel durum işleme**, **Bekleyen fatura** ve **Fatura günlüğü** sorgu sayfalarında, ek görüntüleyiciyi gizlemenizi veya göstermenizi sağlayan yeni bir düğme bulunur.

### <a name="security"></a>Güvenlik

Ek görüntüleyicideki aşağıdaki eylemler rol tabanlı güvenlikle denetlenir:

+ Vurgulama
+ Engelle
+ Ek açıklama

### <a name="pending-vendor-invoices-page"></a>Beklemedeki satıcı faturaları sayfası

Aşağıdaki ayrıcalıklar vurgulama, engelleme veya ek açıklama ekleme işlemleri için ek görüntüleyiciye salt okuma erişimi veya okuma/yazma erişimi sağlar:

+ **Satıcı fatura resmini koru** – Bu ayrıcalık, okuma/yazma erişimi sağlar.
+ **Satıcı fatura resmini görüntüle** – Bu ayrıcalık, salt okuma erişimi sağlar.

Aşağıdaki görevler, şu eylemler için ek görüntüleyiciye salt okuma veya okuma/yazma erişimi sağlar:

+ **Satıcı faturalarını koru** – Satıcı fatura resmini koru ayrıcalığı bu göreve atanır.
+ **Satıcı fatura durumunu sorgula** – Satıcı fatura resmini görüntüle ayrıcalığı bu göreve atanır.

Aşağıdaki roller, şu eylemler için ek görüntüleyiciye salt okuma veya okuma/yazma erişimi sağlar:

+ **Borç hesapları memuru** ve **Borç Hesapları yöneticisi** – Bu rollere Satıcı faturalarını koru görevi atanır.
+ **Borç hesapları memuru**, **Borç Hesapları yöneticisi**, **Borç hesapları merkezi ödeme memuru** ve **Borç hesapları ödemeler memuru** – Bu rollere satıcı faturası durumunu sorgula görevi atanır.

### <a name="invoice-exception-details-page"></a>Fatura özel durum ayrıntıları sayfası

Aşağıdaki ayrıcalıklar vurgulama, engelleme veya ek açıklama ekleme işlemleri için ek görüntüleyiciye salt okuma erişimi veya okuma/yazma erişimi sağlar.

> [!NOTE]
> Bu bölümde söz edilen bu roller, ek görüntüleyicideki fatura resimlerine salt okuma erişimi sağlar. Bir rolün resimler için yazma erişimi de olması gerekiyorsa, bu role yazma erişimini burada açıklanan ayrıcalığı ve görevi vererek sağlayabilirsiniz.

+ **Satıcı fatura başlığı varlığı resmini koru** – Bu ayrıcalık, ek görüntüleyicideki fatura resimlerine okuma/yazma erişimi sağlar.
+ **Satıcı fatura başlığı varlığı resmini görüntüle** – Bu ayrıcalık, ek görüntüleyicideki fatura resimlerine salt okuma erişimi sağlar.

Aşağıdaki görevler, şu eylemler için ek görüntüleyiciye salt okuma erişimi sağlar:

+ **Satıcı faturalarını koru** – Satıcı fatura başlığı varlığı resmini koru ayrıcalığı bu göreve atanır.

Aşağıdaki roller, şu eylemler için ek görüntüleyiciye salt okuma erişimi sağlar:

+ **Borç hesapları memuru** ve **Borç Hesapları yöneticisi** – Bu rollere Satıcı faturalarını koru görevi atanır.

Varsayılan olarak, kullanıcı rolü herhangi bir sayfada düzenleme hakları sağlıyorsa, kullanıcı ek görüntüleyicide de vurgulama, engelleme ve not ekleme eylemleri için düzenleme hakkında sahip olur. Bununla birlikte, belirli bir rolün sayfada düzenleme haklarına sahipken ek görüntüleyicide bu haklara sahip olmaması gereken senaryolar varsa, önceki listedeki uygun ayrıcalıklar bu kullanım örneğini karşılamak üzere kullanılabilir.
