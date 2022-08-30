---
title: Yerleşim yönergesi stoktan çekme yaşlandırma
description: Bu makalede malzeme çekme sırasında ilk giren ilk çıkar (FIFO) ve son giren ilk çıkar (LIFO) konum yönergesi stratejilerinin nasıl kullanılacağı açıklanmaktadır.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationProfile,WHSWorkTable,WHSWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 4ed1308ea36b731b156b518182846b60a59528d5
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335630"
---
# <a name="location-directive-inventory-picking-aging"></a>Yerleşim yönergesi stoktan çekme yaşlandırma

[!include [banner](../includes/banner.md)]

Bu makalede malzeme çekme sırasında ilk giren ilk çıkar (FIFO) ve son giren ilk çıkar (LIFO) konum yönergesi stratejilerinin nasıl kullanılacağı açıklanmaktadır. Bu stratejiler, stoğun ambara ilk olarak ne zaman girdiğini izlemek üzere yerleşimler için kaydedilen yaşlandırma tarihleriyle birlikte çalışır. *Yerleşim yönergesi stok çekme yaşlandırma* özelliği yaşlandırmayı belirlemek için yerleşimdeki tarihi kullanır. *Ambar yerleşimi durumu* özelliği, plakadaki tarihe göre, yerleşimdeki tarihi güncelleştirir.

Hem toplu olarak izlenen maddeleri, hem de toplu olarak izlenmeyen maddeleri sevk etmek için, stoğun ambara girdiği tarihi temel alan FIFO ve LIFO stratejilerini kullanabilirsiniz. Bu yetenek özellikle, tasnif için bitiş tarihi bulunmayan, toplu olarak izlenmeyen stok için yararlı olabilir.

Stok ambara ilk alındığında veya oluşturulduğunda, sistem ilgili plakayı güncelleştirir ve böylece geçerli tarih yaşlandırma tarihi olarak gösterilir. Bu tarih daha sonra, ambardaki en eski veya en yeni stoğu tanımlamak üzere yerleşim yönergesi stratejileri tarafından kullanılır. Stok, plaka ile izlenmeyen bir konuma taşınırsa, yerleşimin kendisi yaşlandırma bilgileriyle güncelleştirilir ve bu bilgiler daja sonra stratejiler tarafından kullanılır.

## <a name="turn-on-the-feature"></a>Özelliği etkinleştirme

Bu özelliği kullanılabilir hale getirmek için, [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aşağıdaki özellikleri bu sırayla etkinleştirin:

1. *Ambar yerleşimi durumu* (Sürüm 10.0.29 itibariyle bu özellik zorunludur ve kapatılamaz. Daha fazla bilgi için bkz. [Ambar yerleşimi durumu](warehouse-location-status.md)).
1. *Yerleşim yönergesi stoktan çekme yaşlandırma*

## <a name="feature-requirements"></a>Özellik gereksinimleri

Bu özelliği kullanmak için stoğu depolamak üzere kullanılan her [yerleşim profili](tasks/create-location-profile.md) için **Yerleşim durumunu etkinleştir** seçeneğini *Evet* olarak ayarlamanız gerekir. Bir yerleşim profili için bu seçeneği ayarlamak üzere **Ambar yönetimi \> Kurulum \> Ambar \> Yerleşim profilleri**'ne gidin ve yerleşim profilini seçin. Seçeneği **Genel** hızlı sekmesinde bulabilirsiniz.

## <a name="feature-scenarios"></a>Özellik senaryoları

Bu bölüm, FIFO ve LIFO stratejilerinin nasıl ayarlanacağını ve kullanılacağını gösteren örnekler içerir.

> [!TIP]
> Bu bölümde, bir FIFO ve bir LIFO olmak üzere iki senaryo sunulmaktadır. Sağlanan yordamlar, her iki senaryoyu da sırasıyla yapacağınız varsayılır. Her iki senaryoyu da yapmanız önerilir, böylece iki strateji arasındaki farkları öğrenebilirsiniz.

### <a name="make-sample-data-available"></a>Örnek verilerini kullanılabilir hale getirme

Burada belirtilen örnek kayıtları ve değerleri kullanarak bu senaryolar üzerinden çalışmak için, standart [tanıtım verilerinin](../../fin-ops-core/fin-ops/get-started/demo-data.md) yüklenmiş olduğu bir sistemde olmanız gerekir. Ek olarak, başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.

Bu senaryoları, özelliği üretim sisteminde kullanmaya yönelik bir kılavuz olarak da kullanabilirsiniz. Ancak, bu durumda, burada açıklanan her ayar için kendi değerlerinizi kullanmanız gerekir.

### <a name="set-up-the-scenarios"></a><a name="demo-set-up"></a>Senaryoları ayarlama

Demo verileri, senaryoları desteklemek için kurulum ve stok ayarlamaları gerektirir. FIFO ve LIFO senaryolarıya çalışmak için gerekli olan stok verilerini oluşturmak için bu adımları izleyin.

1. Demo verilerinin yüklü olduğu bir sistemde oturum açın ve **USMF** tüzel kişiliğini seçin.
1. **Ambar yönetimi \> Kurulum \> Ambar \> Konum profilleri**'ne gidin.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. Yerleşim profilleri listesinde **FLOOR-05**'i seçin.
1. **Genel** hızlı sekmesinde, **Yerleşim durumunu etkinleştir** seçeneğini *Evet* olarak ayarlayın.
1. **Kaydet**'i seçin.
1. **Ambar Yönetimi \> Kurulum \> Konum yönergeleri** seçeneğine gidin.
1. Konum yönergeleri listesinde, **63 Çekme konteyner kullanımı**'nı seçin.
1. Sayfayı düzenleme moduna sokmak için **Düzenle**'yi seçin.
1. **Konum yönergesi eylemleri** hızlı sekmesinde, **Sıra numarası** alanının *1* olarak ayarlandığı satırı bulun ve aşağıdaki adımlardan birini izleyin:

    - Bir FIFO senaryosu ayarlıyorsanız, **Strateji** alanı değerini *Yerleşim yaşlandırma FIFO* olarak değiştirin.
    - Bir LIFO senaryosu ayarlıyorsanız, **Strateji** alanı değerini *Yerleşim yaşlandırma LIFO* olarak değiştirin.

1. **Yerleşim yönergesi eylemleri** hızlı sekmesinde **Sorguyu düzenle**'yi seçin.
1. Sorgu iletişim kutusunda, **Aralık** sekmesinde bir satır eklemek için **Ekle**'yi seçin ve sonra aşağıdaki değerleri ayarlayın:

    - **Tablo:** *Yerleşimler*
    - **Türetilmiş tablo:** *Yerleşimler*
    - **Alan:** *Bölge Kodu*
    - **Ölçütler:** *Kat*

1. Ayarlarınızı uygulayıp sorgu iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Yerleşim yönergenizde yaptığınız değişiklikleri kaydetmek için **Kaydet**'i seçin.
1. Bir mobil cihazda veya bilgisayarınızdaki *Dynamics 365 Supply Chain Management - Ambarlama* uygulamasında, senaryoları desteklemek üzere mevcut stoğu ambar yerleşiminden kaldırmak için aşağıdaki adımları izleyin:

    1. Ambar *63* için uygun bir kullanıcı kimliği ve parola kullanarak oturum açın.
    1. Ana menüde **Kalite**'yi seçin.
    1. **Kalite yönetimi** menüsünde, **Iskarta**'yı seçin.
    1. **Iskarta** sayfasında, **YER/Plaka** alanını seçin ve *63\_1* değerini girin.
    1. **Giriş** veya **Tamam**'ı seçin.
    1. **Enter** veya **Tamam**'ı seçerek **Ayarlama** için **Iskarta** ayrıntılarını onaylayın.

    Plaka stoğu ayarlandığında, İş Tamamlandı" iletisi alırsınız.

    Bu adımlar, demo verilerinde iki yerleşimde stok bırakır. Her yerleşim farklı bir yaşlandırma tarihine sahiptir. *FL-001* yerleşiminin yaşladırma tarihi 15 Nisan 2017, *FL-002* konumunun yaşlandırma tarihi 29 Ocak 2017'dir. Her iki yerleşimde de *A0001* maddesi bulunur.

    Bu verileri görüntülemek için **Stok Yönetimi \> Sorgular ve raporlar \> Eldeki stok listesi**'ne gidin ve ambar *63* *A0001* maddesi için filtre uygulayın. **Yerleşim** alanının *FL-001* veya *FL-002* olarak ayarlandığı satırlarda pozitif **Fiziksel stok** değerine sahip bir satır seçin ve ardından Eylem Bölmesinde **Hareketler**'i seçin. **Fiziksel tarih** alanı, daha önce sözü edilen yaşlandırma tarihlerinden birine karşılık gelen bir tarih gösterir.

### <a name="scenario-1-set-up-and-use-fifo-location-aging"></a><a name="fifo-demo"></a>Senaryo 1: FIFO yerleşim yaşlandırması ayarlama ve kullanma

FIFO stratejisi, en eski yaşlandırma tarihini içeren konumu bulur ve bu yaşlandırma tarihine göre malzeme çekme işlemini tahsis eder.

1. Henüz yapmadıysanız, bu senaryo için gerekli [örnek verileri hazırlayın](#demo-set-up).
1. **Satış ve pazarlama \> Satış siparişi \> Tüm satış siparişleri**'ne gidin.
1. **Yeni**'yi seçin.
1. **Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Müşteri** hızlı sekmesinde, **Müşteri hesabı** alanını *ABD-001* olarak ayarlayın.
    - **Genel** hızlı sekmesinde, **Ambar** alanının ayarını *63* yapın.

1. Satış siparişi oluşturmak ve iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Yeni satış siparişi açılır. **Satış siparişi satırları** hızlı sekmesindeki kılavuzda yeni, boş bir satır dahil eder. Bu sipariş satırı için, **Madde numarası** alanını *A0001* olarak ve **Miktar** alanını *1* olarak ayarlayın.
1. Kılavuzun üzerindeki **stok** menüsünde **rezervasyon**'yı seçin.
1. **Rezervasyon** sayfasında, seçili ambardaki stoktan bu madde için sipariş edilen miktarı rezerve etmek için **Lot ayır**'ı seçin.
1. **Rezervasyon** sayfasını kapatın.
1. **Satış siparişi** sayfasında, Eylem Bölmesinde, **Ambar** sekmesindeki **Eylemler** grubunda **Ambara serbest bırak**'ı seçin. Bilgi iletileri alırsınız. Sistem bir sevkiyat oluşturur, bunu yeni bir yüklemeye ekler ve gerekli işi oluşturur.
1. **Satış siparişi satırları** hızlı sekmesinde, **Ambar** menüsünde, bu satış siparişi için oluşturulan işi açmak için **İş ayrıntıları**'nı seçin. **İş türü** değerinin *Çekme* olduğu satırın *FL-002* değerine sahip bir **Yerleşim** gösterdiğine dikkat edin. Bu yerleşim, en eski yaşlandırma tarihine sahip (FIFO) plakayı içerir.
1. **Ambar \> Sevkiyat ayrıntıları**'nı seçin.
1. **Genel** hızlı sekmesinde, senaryo 2'de kullanabilmek için dalga kodunu not edin.

### <a name="scenario-2-set-up-and-use-lifo-location-aging"></a>Senaryo 2: LIFO yerleşim yaşlandırması ayarlama ve kullanma

LIFO stratejisi, en yeni yaşlandırma tarihini içeren konumu bulur ve bu yaşlandırma tarihine göre malzeme çekme işlemini tahsis eder. Senaryo 2'de, senaryo 1'in ayarını düzenleyecek (FIFO) ve bu senaryo sırasında oluşturulan satış siparişi ve dalgayı yeniden kullanacaksınız.

1. Bu senaryoya başlamadan önce, [önceki bölümde](#fifo-demo) açıklandığı şekilde tam FIFO senaryosunu ayarlayın ve tamamlayın. Bu senaryoda, o senaryo için oluşturulan dalgayı ve kurulumun büyük bir bölümünü yeniden kullanacaksınız.
1. **63 Çekme konteyner kullanımı** yerleşim yönergesini, [Senaryoları ayarlama](#demo-set-up) yordamının ilk bölümünde açıklanan şekilde *Yerleşim yaşlandır LIFO* stratejisini kullanacak şekilde düzenleyin.

    Ardından, senaryo 1'de satış siparişi için oluşturulan dalgayı  *Yerleşim yaşlandırma LIFO* stratejisini kullacak şekilde değiştireceksiniz.

1. **Ambar yönetimi \> Giden dalgalar \> Sevkiyat dalgaları \> Tüm dalgalar**'a gidin.
1. FIFO senaryosu için oluşturduğunuz siparişi içeren dalgayı seçin ve açın.
1. Eylem Bölmesinde, **İş** sekmesinde, FIFO senaryosu için oluşturduğunuz işi iptal etmek için **İptal**'i seçin.
1. Eylem Bölmesinde, **Dalga** sekmesindeki **Dalga** gurubunda **İşle**'yi seçin.
1. İşlem tamamlandığında, Eylem Bölmesinde, **Dalga** sekmesinde, **İlgili bilgi** grubunda, bu dalga için oluşturulan işi açmak için **İş**'i seçin.
1. **İş** sayfasında, **Genel bakış** sekmesinde, iki satır olmalıdır. **İş durumu** alanının *Açık* olarak ayarlandığı satırı seçin.
1. **İş türü** değerinin *Çekme* olduğu satırın *FL-001* değerine sahip bir **Yerleşim** gösterdiğine dikkat edin. Bu yerleşim, en yeni yaşlandırma tarihine sahip (LIFO) plakayı içerir.

Bu senaryolarda, seçilen stratejiye bağlı olarak, yerleşim yaşlandırma stratejisinin işi en eski stoğa veya en yeni stoğa sahip stok yerleşimine nasıl yönlendirdiğini gördünüz.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
