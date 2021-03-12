---
title: Çağrı merkezi kanalları ayarlama
description: Bu konuda, çağrı merkezleri için siparişlerin Dynamics 365 Commerce kullanarak nasıl işleneceği hakkında bilgi verilmektedir.
author: josaw1
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCROrderParameters, MCRSalesTableOrderHistory, SalesOrderProcessingWorkspace
audience: Application User
ms.reviewer: josaw
ms.custom: 78973
ms.assetid: 09fca083-ac0d-4f30-baf2-bb00a626be12
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: fde831bb08f45623f24805625f76c0a43460562a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985748"
---
# <a name="set-up-call-center-channels"></a>Çağrı merkezi kanalları ayarlama

[!include [banner](includes/banner.md)]

Bir şirket, Dynamics 365 Commerce içinde birden fazla çağrı merkezi kanalı tanımlayabilir. Çağrı merkezi kanalları **Retail ve Commerce** \> **Kanallar** \> **Çağrı merkezleri** \> **Tüm çağrı merkezleri**'nde yapılandırılır ve belirli bir tüzel kişiliğe özeldir.

Yeni bir çağrı merkezi kanalı oluşturulduğunda, sistematik olarak bir çalışma birimi numarası atanır. Çağrı merkezleri işletme birimleri olarak oluşturulduğundan, kullanıcılar çağrı merkezi kanalını ürün çeşitleri, kataloglar ve belirli teslimat şekilleri gibi çeşitli Commerce özelliklerine bağlayabilir.

Varsayılan ambar çağrı merkezi kanalından yapılandırılabilir. Ardından, bu kanalda satış siparişleri oluşturulduğunda, satış siparişi için seçilen müşteride başka bir ambar tanımlanmadığı sürece, varsayılan ambar otomatik olarak satış siparişi başlığına girilir. Bu durumda, müşterinin ambarı varsayılan olarak girilir.

Kullanıcıların çağrı merkezi özelliklerini kullanmak için bir çağrı merkezi kanalına bağlı olması gerekir. Bir kullanıcı tarafından oluşturulan satış siparişi, otomatik olarak bu kullanıcının çağrı merkezi kanalına bağlanır. Şu anda, tek bir kullanıcı birden çok çağrı merkezi kanalına aynı anda bağlanamamaktadır.

Bir e-posta bildirimi profili de çağrı merkezi kanalında yapılandırılabilir. Profil, e-posta siparişleri veren müşterilere çağrı merkezi kanalı üzerinden gönderildiğinde kullanılan e-posta şablonları kümesini tanımlar. E-posta tetikleyicileri sipariş gönderme veya siparişi sevk etme gibi sistem olaylarına karşı yapılandırılabilir.

Satışın bir çağrı merkezi kanalı üzerinden doğru şekilde işlenebilmesi için doğru [ödeme yöntemleri](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-payments) ve teslimat şekilleri kanal için tanımlanmalıdır.

Çağrı merkezi kanalı düzeyinde, kanal tarafından oluşturulan siparişlere bağlanacak mali boyutlar ile ilgili diğer varsayılan değerleri tanımlayabilirsiniz.

## <a name="options-for-order-processing-behavior"></a>Sipariş işleme davranışı seçenekleri

Bir çağrı merkezinin yapılandırmasında üç ayarın çağrı merkezine göre oluşturulan satış siparişleri için kullanılabilen işlevler ve özellikler üzerinde önemli bir etkisi vardır: **Sipariş tamamlamayı etkinleştir**, **Doğrudan satışı etkinleştir** ve **Sipariş fiyat denetimini etkinleştir**.

### <a name="enable-order-completion"></a>Sipariş tamamlamayı etkinleştir

Çağrı merkezi kanalındaki **Sipariş tamamlamayı etkinleştir** ayarının bu kanal için girilen satış siparişlerinin sipariş işleme akışı üzerinde önemli bir etkisi vardır. Bu ayar etkinleştirildiğinde, tüm satış siparişlerinin onaylanabilmesi için önce bir doğrulama kural kümesinden geçmesi gerekir. Bu kuralları satış siparişi sayfasının Eylem Bölmesine eklenen **Tamamla** düğmesini seçerek çalıştırın. **Sipariş tamamlamayı etkinleştir** ayarı açık olduğunda oluşturulan tüm siparişlerin sipariş tamamlama işleminden geçmesi gerekir. Bu işlem, ödeme ve ödeme doğrulama mantığının yakalanmasını zorunlu kılar. Ödeme uygulama yanı sıra, sipariş gönderme işlemi sistemde yapılandırdığınız [sahtekarlık denetimlerini](https://docs.microsoft.com/dynamics365/unified-operations/retail/set-up-fraud-alerts) tetikleyebilir. Ödemesi yapılmayan veya sahtekarlık doğrulamalarını geçemeyen siparişler beklemeye alınır ve beklemeye alınma nedeni çözülene kadar başka bir işlem (malzeme çekme veya sevkiyat gibi) yapılamaz.

**Sipariş tamamlamayı etkinleştir** ayarı çağrı merkezi kanalı için açık olduğunda, satır maddeleri bir satış siparişine girilirse ve kanal kullanıcısı **Tamamla** 'yı seçmeden satış siparişi formunu kapatmayı veya formdan ayrılmayı denerse, sistem satış siparişi özet sayfasını açarak ve kullanıcıdan siparişi doğru şekilde göndermesini isteyerek satışı tamamlama işlemini zorunlu kılar. Sipariş ödeme ile birlikte sipariş doğru şekilde gönderilemiyorsa, kullanıcı siparişi beklemeye almak için [sipariş tutmalar](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds) işlevini kullanabilir. Kullanıcı siparişi iptal etmeye çalışırsa, siparişi kullanıcı güvenlik ayarlarının izin verdiği işleve bağlı olarak İptal et veya Sil işlevini kullanarak doğru şekilde iptal etmesi gerekir.

**Sipariş tamamlamayı etkinleştir** ayarı çağrı merkezi kanalı için açılırsa **Ödeme durumu** alanı siparişte izlenir. Sistem satış siparişi gönderildiğinde **Ödeme durumu**'nu hesaplar. Yalnızca onaylanan ödeme durumundaki siparişlerin malzeme çekme ve sevkiyat gibi ek sipariş işleme adımları için sistem üzerinde ilerlemesine izin verilir. Ödemeler reddedilirse **işleme** bayrağı ayrıntılı sipariş durumunda etkin hale gelir ve bu, ödeme sorunu çözülene kadar siparişin beklemede kalmasını sağlar.

Ayrıca, **Sipariş tamamlamayı etkinleştir** ayarı açık olursa, kullanıcılar satış siparişleri oluşturduğunda ve satır maddesi giriş modunda olduğunda **Kaynak** alanı ana satış siparişi başlığında kullanılabilir olacaktır. **Kaynak** alanı bir doğrudan pazarlama satış senaryosunda [katalog kaynak kodunu](https://docs.microsoft.com/dynamics365/unified-operations/retail/call-center-catalogs) yakalamak için kullanılır. Bu kod promosyonlar ve özel fiyatlar sağlar.

**Sipariş tamamlamayı etkinleştir** ayarı kapalı olsa bile, kullanıcılar hala satış siparişine bir kaynak kodu uygulayabilir. Bununla birlikte, önce **Kaynak** alanına erişmek için satış siparişi başlığı ayrıntılarını açmaları gerekir. Başka bir deyişle, bazı ek tıklamalar gereklidir. Aynı davranış sevki tamamlanan ve öncelikli siparişler gibi özellikler için de geçerlidir. Bu özellikler, çağrı merkezinde oluşturulan tüm siparişler için kullanılabilir. Bununla birlikte, **Sipariş tamamlamayı etkinleştir** ayarı açık olduğunda, kullanıcılar bu özelliklerin yapılandırmasını satış giriş görünümündeyken satış başlığında görebilir. Uygun ayarları ve alanları bulmak için satış siparişi başlığı ayrıntılarına gitmeleri gerekmez.

### <a name="enable-direct-selling"></a>Doğrudan satışı etkinleştir

**Doğrudan satışı etkinleştir** ayarı çağrı merkezi kanalı için açık olduğunda, kullanıcılar Commerce'in yukarı satış ve çapraz satış özelliklerinden yararlanabilirler. Bu durumda, açılır pencereler sipariş girişi sırasında görüntülenir ve müşteriye çağrı merkezi kullanıcısının teklif edebileceği diğer ürünleri önerir. Önerilen ürünler, yalnızca satış siparişi satırında sipariş edilen ürünü temel alır. Şu anda yukarı satış ve çapraz satış önerileri ürünlerde veya kataloglarda madde düzeyinde yapılandırılabilir. **Doğrudan satışı etkinleştir** ayarı çağrı merkezi kanalı için devre dışı olduğunda, sipariş edilen madde için tanımlanmış bir çapraz satış veya yukarı satış olsa bile açılır pencereler sipariş girişi sırasında görünmez.

**Doğrudan satışı etkinleştir** ayarı açık olduğunda, satış siparişi giriş sayfasının komut dosyaları ve resimler özellikleri de açılır. Bu durumda, bir bilgi bölmesi sipariş girişi sırasında sayfanın sağında kullanılabilir olacaktır. Bu panel, genel sipariş girişi işlemiyle ilgili komut dosyalarını, uygulanan katalog kaynak kodunu ve sipariş edilen maddelerle ilgili komut dosyalarını gösterir. Ayrıca, ürün kurulumunda madde için bir resim tanımlandıysa, resimler paneli sipariş edilen maddeler için bir ürün resmi gösterebilir.

### <a name="enable-order-price-control"></a>Sipariş fiyatı denetimini etkinleştir

**Sipariş fiyatı denetimini etkinleştir** ayarı açık olduğunda, yalnızca yetkili kullanıcılar sipariş girişi sırasında bir maddenin satış fiyatını değiştirebilir. Değişiklikleri tanımlanan tolerans içinde olmalıdır. Uygun yetkiye sahip olmayan kullanıcıların fiyat değişikliği isteği göndermesi gerekir. İstek daha sonra gözden geçirme ve onay için sistem iş akışları aracılığıyla işlenir.

## <a name="channel-users"></a>Kanal kullanıcıları

Çağrı merkezi kanalını tanımlarken, kanal kullanıcılarını çağrı merkezine bağlamanız gerekir. Aksi takdirde, çağrı merkezi sistemde kullanılamaz. Kullanıcılar Commerce'de oturum açtığında ve satış siparişlerini veya iade siparişlerini sipariş girişiyle ilgili sayfaya girdiklerinde, kullanıcı kimliği çağrı merkezi kanalının yapılandırmasına karşı doğrulanır. Bir kullanıcı belirli bir çağrı merkezi kanalına bağlıysa, kullanıcı tarafından oluşturulan siparişler bu kanalın niteliklerini ve varsayılan değerlerini alır.

Varsayılan olarak, satış siparişi başlığındaki **satış** bayrağı çağrı merkezi kullanıcılarının oluşturduğu tüm siparişler için açıktır. Siparişler sistemin ticarete özel fiyat ve promosyon özelliklerinden yararlanabilir.


Bir çağrı merkezi kanalına bağlı olmayan kullanıcılar, Microsoft Dynamics 365 Finance'in standart sipariş girişi özelliklerini kullanır. Bu kullanıcıların satış siparişi giriş formu aracılığıyla girdikleri siparişler sistematik olarak Commerce siparişi olarak tanımlanmaz. Ayrıca, bu kullanıcılar tarafından girilen bu siparişler sipariş tamamlama işlemi kurallarına, fiyatlandırma mantığına ya da çağrı merkezi kanal yapılandırması veya çağrı merkezi sistem parametrelerinde tanımlanabilecek diğer sipariş doğrulamalarına tabi olmazlar.

Çağrı merkezi parametrelerini yapılandırmayı ve kanal kullanıcılarını tanımlamayı tamamladıktan sonra, istenen sistem davranışının sağlanmasına yardımcı olmak için tüm gerekli Çağrı merkezi parametrelerinin **Retail ve Commerce** \> **Kanal kurulum** \> **Çağrı merkezi kurulumu** \> **Çağrı merkezi parametreleri** altından tanımlandığından emin olun. İlgili numara serilerinin de tanımlandığından emin olun.

> [!NOTE]
> Çağrı merkezi işlevlerini kullanabilmeniz için **çoklu sevk edilecek** konfigürasyon anahtarının etkinleştirilmesi gerekir. Bu konfigürasyon anahtarı, **Sistem yönetimi** \> **Kurulum** \> **Lisans konfigürasyonu** altındaki **ticaret konfigürasyon** anahtarlarında bulunabilir. Bu, satış siparişi satırı düzeyinde konfigüre edilen teslimat adresine dayalı olarak çeşitli doğrulamaları gerçekleştiren çağrı merkezi işlevselliğe bağlı olarak gereklidir. 

