---
title: Çağrı merkezi sipariş bekletmelerini yapılandırma ve bunlarla çalışma
description: Bu konu, siparişlerdeki tutma durumuyla Dynamics 365 Commerce kullanarak nasıl çalışılacağını açıklamaktadır.
author: josaw1
manager: AnnBe
ms.date: 05/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCRHoldCodeTable, MCRSalesTableOrderHistory, MCRHoldCodeTrans, MCROrderEventSetup, MCROrderEventTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b11dd48ac629910a82b4d5bfdf9889809b0d829d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416442"
---
# <a name="configure-and-work-with-call-center-order-holds"></a>Çağrı merkezi sipariş tutmalarını yapılandırma ve bunlarla çalışma

[!include [banner](includes/banner.md)]

Bu konu, çağrı merkezi siparişleri için Dynamics 365 Commerce'de bulunan sipariş tutma özelliklerini açıklamaktadır.

## <a name="configuring-call-center-order-holds"></a>Çağrı merkezi sipariş tutmalarını yapılandırma

Çağrı merkezi sipariş tutma özelliklerini kullanmak için önce durdurma kodları tanımlamalısınız. İş gereksinimlerinize göre bir kullanıcı tanımlı tutma kodları kümesi oluşturmak için **Satış ve pazarlama** \> **Kurulum** \> **Satış siparişleri** \> **Sipariş tutma kodları**'na gidin. İsterseniz **Satış siparişi için varsayılan** seçeneğini **Evet** yaparak, tutma kodlarından birini varsayılan tutma kodu olarak işaretleyebilirsiniz. Bir satış siparişi beklemeye alındığı her zaman bu tutma kodu kullanılacaktır. Bir satış siparişinde rezerve edilmiş stok varsa ve sipariş belirli bir nedenle beklemeye alındığında rezervasyonların otomatik olarak kaldırılması gerekiyorsa, neden kodlarına ilişkin **Stok rezervasyonlarını kaldır** seçeneğini **Evet** yapın.

Satış siparişini beklemeye alan kullanıcılar isteğe bağlı notlar girdiği zaman alınacak notun türünü belirtmek için **Alacak hesapları** \> **Kurulum** \> **Alacak hesapları parametreleri**'ne gidin ve **Satış kurulumu** hızlı sekmesinde, **Genel** sekmesindeki **Not türü** alanını ayarlayın. Beklemeye alınan satış siparişlerini **Müşteri hizmeti** sayfasında görüntülenirken vurgulamada kullanılacak rengi tanımlamak için **Beklemede satış siparişi durumu** alanını kullanın.

İsteğe bağlı bir tutma nedeni kodları kümesi oluşturmak için **Retail ve Commerce** \> **Kanal kurulumu** \> **Bilgi kodları**'na gidin. Bu bilgi kodları, ana tutma kodunu daha fazla tanımlamak için ikinci neden kodu olarak kullanılabilir. **Yeni**'yi seçerek bir neden kodu kümesi oluşturduktan sonra ek nedenler listesini tanımlamak için **Alt kodlar**'ı seçin. Tanımladığınız herhangi bir bilgi kodunu çağrı merkezi kanalına bağlamak için **Retail ve Commerce** \> **Kanallar** \> **Çağrı merkezleri** \> **Tüm çağrı merkezleri**'ne gidin. **Genel** hızlı sekmesinde **Tutma kodu** alanını ayarlayın.

## <a name="putting-orders-on-hold"></a>Siparişleri beklemeye alma

Çağrı merkezi kullanıcılarının arka ofis Commerce programında oluşturduğu siparişler belirli durumlarda el ile veya otomatik olarak beklemeye alınabilir.

Sipariş girişi sırasında ancak sipariş gönderilmeden ve onaylanmadan önce çağrı merkezi kullanıcıları bir siparişi el ile beklemeye alarak diğer işlemler için ambara serbest bırakılmasını önlemek isteyebilirler. Örneğin, siparişi veren müşteri siparişin taahhüdünü vermeye hazır olmayabilir veya işlem için gereken kritik veriler eksik olabilir.

Sipariş giriş sayfasında, çağrı merkezi kullanıcısı, sipariş giriş menüsünün **Satış siparişi** sekmesindeki **Sipariş tutmalar** seçeneğini kullanarak bir siparişi beklemeye alabilir. Alternatif olarak, kullanıcı, bir çağrı merkezi satış siparişinde **Tamamla**'yı seçtiği zaman görünen **Satış siparişi özeti** sayfasındaki **Tut** menü öğesini seçebilir.

Her iki durumda da **Sipariş tutmalar** sayfası açılır. Bunun ardından kullanıcı **Yeni**'yi seçerek sipariş için tutma oluşturabilir. **Tutma kodu** alanında kullanıcının tutma nedenini en iyi açıklayan kodu seçmesi gerekir. **Neden kodu** alanında, kullanıcı isteğe bağlı olarak ek bir kod seçip tutma işlemi için ikinci düzeyde bir açıklama yapabilir.

**Notlar** hızlı sekmesinde, **Tutma Notları** alanında, kullanıcı serbest biçimli ek notlar girerek, tutma işlemi hakkında ek bağlam veya bilgiler verebilir. Bu notlar daha sonra tutma emrini inceleyen veya emrin üzerinde çalışan diğer kullanıcılara yardımcı olabilir.

Tutma bilgileri girilip kaydedildikten sonra kullanıcı **Sipariş tutmalar** sayfasını kapatabilir. Bunun ardından kullanıcı satış siparişi giriş sayfasına döndürülür. Satış siparişinde başka eylem gerekmiyorsa, kullanıcı satış siparişi giriş sayfasını kapatabilir.

**Sipariş tamamlamayı etkinleştir** bayrağı etkinleştirildiyse, çağrı merkezi kanalında bekleme durumundaki bir siparişe ödeme uygulanması zorunlu değildir. Bunun tersine, beklemeye alınmamış bir satış siparişi için, kullanıcılar ödeme uygulanana kadar satış siparişi giriş sayfasından ayrılamaz. Kuşkusuz, sipariş tutma kaldırılmadan önce ödeme yapılması gerekecektir.

Ek olarak, çağrı merkezi kullanıcıları herhangi bir nedenle şüpheli görülen siparişlere el ile bir sahte tutma ekleyebilirler. Siparişler etkin sahtekarlık ölçütleri ve kurallarıyla eşleştikleri zaman otomatik olarak da beklemeye alınabilir. Bu tür sipariş tutma hakkında daha fazla bilgi için bkz. [Sahtekarlık uyarılarını ayarlama](https://docs.microsoft.com/dynamics365/unified-operations/retail/set-up-fraud-alerts).

## <a name="viewing-and-managing-orders-that-are-on-hold"></a>Beklemeye alınan siparişleri görüntüleme ve yönetme

### <a name="viewing-hold-information-for-a-single-sales-order"></a>Tek bir satış siparişinin tutma bilgilerini görüntüleme

**Müşteri hizmeti** sayfasında sipariş satırları belirli bir renkle vurgulandığı için, kullanıcılar beklemede olan siparişleri görsel olarak tanıyabilirler. Bu renk, **Alacak hesapları parametreleri** sayfasındaki **Beklemede satış siparişi durumu** alanıyla tanımlanır.

> [!NOTE]
> Satır sayfada seçildiği zaman vurgu rengi görünmez.

Kullanıcılar bir satış siparişinin beklemede olup olmadığını öğrenmek için o siparişin ayrıntılı durum bilgilerini de görüntüleyebilirler. Ayrıntılı durum bilgilerine **Tüm satış siparişleri** veya **Müşteri hizmeti** sayfasından erişilebilir. Bir sipariş beklemedeyse, **İşleme** bayrağı koyulur ve **Ayrıntılı durum** alanı, senaryoya bağlı olarak **Beklemede** veya **Sahte Tutma** durumu gösterir.

Kullanıcılar tek bir sipariş tutmanın ayrıntılarını görüntülemek için, seçilen siparişin **Seçenekler** menüsünü kullanarak **Müşteri hizmeti** sayfasından **Sipariş tutma** sayfasının ayrıntılı bir görünümünü açabilirler. Kullanıcılar bu görünüme **Tüm satış siparişi** sayfasından **Satış siparişi** sekmesindeki **Sipariş tutmalar** menü öğesini seçerek de erişebilirler.

### <a name="viewing-all-orders-that-are-on-hold"></a>Beklemeye alınan tüm siparişleri görüntüleme

El ile veya otomatik olarak bekleme durumuna alınmış tüm siparişleri görüntülemek için **Retail ve Commerce** \> **Müşteriler** \> **Sipariş tutmalar**'a gidin.

**Sipariş tutmalar** workbench'i, el ile veya sahtekarlıkla ilgili tutma eylemleri nedeniyle beklemeye alınan tüm siparişlerin liste halinde bir görünümünü verir. Kullanıcılar sayfada standart filtreleme ve sıralama seçeneklerinden yararlanarak, incelemekle sorumlu oldukları belirli tutma kodlarının üzerinde çalışmalarına veya bu kodları yönetmelerine olanak sağlayan görünümler oluşturabilirler. **Sipariş tutmalar** workbench'i, bir sipariş beklemede tutulduğu gün sayısını da gösterir. Bu bilgiler, kullanıcıların kuyrukta öncelik sırasını belirlemelerine yardımcı olabilir.

Kullanıcılar, bekletilen siparişlerin daha ayrıntılı bir görünümünü elde etmek için menüdeki **Sipariş tutma** seçeneğine tıklayabilirler. Bu görünüm müşteri hakkında bilgilerin yanı sıra, siparişe, müşteriye veya tutma eylemine uygulanmış notları verir. Sipariş bir sahtekarlık kuralıyla eşleştiği için beklemeye alındıysa, bu görünüm, otomatik tutma nedeni hakkında ayrıntılar da verir.

Kullanıcılar **Sipariş tutmalar** sayfasının hem liste görünümünden hem de ayrıntılı görünümünden, ödeme, toplamlar, notlar gibi, siparişle ilgili ek bilgileri görüntüleyebilir veya düzenleyebilirler.

Şirketinizde birden fazla kullanıcı tutma kuyruğu üzerinde aynı anda çalışıyorsa **Kullanıma almayı askıya al** sekmesindeki seçenekler yararlı olabilir. Kullanıcılar **Kullanıma alma** seçeneğini belirleyerek, sipariş tutmayı incelemek ve araştırmak için çalıştıklarını belirtebilirler. Bu sayede, diğer kullanıcılar aynı işi yapmaya çalışarak zaman kaybetmez. Kullanıcılar **Sipariş tutmalar** sayfasının ayrıntılı görünümünden, kullanıma alma tarih-saati ve tutma kaydını işleme alan kullanıcı hakkında bilgiler görüntüleyebilirler.

Bir tutma kaydı kullanıma alındıktan sonra yalnızca kullanıma alan kullanıcı o kullanıma almayı temizleyebilir. Bu kısıtlamanın amacı, kullanıcıların başka kullanıcıların zaten üzerinde çalışmakta olduğu kayıtları almalarını önlemektir. Bir siparişi diğer kullanıcıların üzerinde çalışabilmesi için kuyruğa geri bırakmak için, kaydı işleme alan kullanıcı **Kullanıma almayı temizle** seçeneğini belirler.

> [!NOTE]
> Kullanıma alma temizlenince tutma serbest bırakılmaz.

Bir kullanıcının hastalık veya şirketten ayrılma gibi nedenlerle bulunmadığı bazı durumlarda, o kullanıcının kullanıma aldığı kayıtların başka bir kullanıcıya yeniden atanması gerekebilir. Bir yönetici **kullanıma almayı geçersiz kıl** seçeneğini kullanarak kayıtları yeniden atayabilir.

## <a name="releasing-orders-that-are-on-hold"></a>Beklemeye alınan siparişleri serbest bırakma

**Sipariş tutmalar** sayfasının hem liste görünümünde hem de ayrıntılı görünümünde **Beklemeyi sil** sekmesi, sipariş tutmayı serbest bırakmak için kullanılan seçenekleri içerir. Bir siparişi, seçilen tutma kodundan serbest bırakmak için **Tutmaları temizle** seçeneğini kullanın.

Çağrı merkezi siparişleri için ödeme gerekir. Bu nedenle, siparişe ödeme uygulanmadıysa bir tutma tamamen temizlenemez. **Çağrı merkezi parametreleri** sayfasındaki **Tutmalar** sekmesinde **Temizlendiğinde gönder** parametresinin açıldığından emin olun. Bu ayar, temizlenen durdurma emrinin doğrulanmak ve ödeme yetkilerini vermek üzere uygun sipariş gönderme mantığından geçmesini garanti altına almaya yardımcı olur. Ödemeler eksikse, kullanıcı bir hata iletisi alır ve tutma kodu temizlenmez.

**Temizlendiğinde gönder** parametresi ayarlanmadıysa, kullanıcıların siparişin tüm gerekli ödeme doğrulamalarından geçmesini garantilemeye yardımcı olarak, **Beklemeyi sil** menüsündeki **Temizle ve gönder** seçeneğini belirlemeleri gerekir. Çağrı merkezi kanalında **Sipariş tamamlamayı etkinleştir** bayrağı etkin durumdayken sipariş gönderme başarısız olursa, sipariş tutma durumundan serbest bırakılır ancak **İşleme** işareti kaldırılmaz. Bu nedenle, ilgili ödemeler uygulanıp doğrulanana kadar sipariş ambara serbest bırakılmaz.

Kullanıcılar tutmayı temizlemek istedikleri bir siparişte sonraki işlemler için serbest bırakılmadan ek değişiklikler yapmak isterlerse **Temizle ve değiştir** seçeneğini belirleyebilirler. Bu seçenek tutma kodunu kaldırıp satış siparişi ayrıntılarını açarak kullanıcıların siparişte ek değişiklikler yapabilmelerine olanak sağlar. Kullanıcılar, ayrıca, çağrı merkezi kanalında **Sipariş tamamlamayı etkinleştir** bayrağı açıkken ödeme uygulayıp satış siparişini ödeme doğrulama mantığından geçirerek gönderebilirler.

## <a name="reporting-options"></a>Raporlama seçenekleri

Sipariş tutmalarla ilgili tarih aralığı, tutma kodu veya diğer ilgili ölçütler bazında rapor çalıştırmak için **Retail ve Commerce** \> **Sorgular ve raporlar** \> **Çağrı merkezi raporları** \> **Sipariş tutma raporu**'na gidin.


[!INCLUDE[footer-include](../includes/footer-banner.md)]