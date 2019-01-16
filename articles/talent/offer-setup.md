---
title: "Teklif yönetimini ayarlayın"
description: "Bu konu Talent'ta tekliflerin nasıl ayarlanacağını açıklar."
author: josaw
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: be66d9f95551066bb8bc25445c652d4fa59066d4
ms.openlocfilehash: bb90f0a3c87c64a74ca63610105abfeb8223900a
ms.contentlocale: tr-tr
ms.lasthandoff: 12/07/2018

---
# <a name="set-up-offer-management"></a>Teklif yönetimini ayarlayın 

[!include [banner](includes/banner.md)]

Bir aday Dynamics 365 for Talent: Attract'ta bir teklif aşamasına geçtiğinde, tekliflerin aday için hızlı bir şekilde oluşturulduğundan, gerektiği gibi onaylandığından ve aday gönderildiğinden emin olmanız gerekir. Çoğu teklif standart olduğu için yeniden kullanılabilir şablonlardan oluşturulabilir. Attract'ta, tüm teklifler, bir veya daha fazla teklif belgesinden oluşan bir teklif paketine toplanır. 

Bu konu, bir Attract yöneticisinin, Attract'taki teklif yönetim özelliklerinin bir parçası olarak farklı teklif paketi şablonları ayarlamak için izleyeceği tüm adımları listeler. Yönetici olmayan rollere sahip kullanıcılar için bu yeteneklerin erişimi olmaz.

>[!NOTE]
> Teklif yönetimi yetenekleri, Kapsamlı İşe aAlma Eklentisi parçası olarak kullanılabilir.

## <a name="offer-data"></a>Teklif verileri 

Teklif verileri, teklif paketi şablonu içindeki en küçük birimdir. Tipik bir teklif standart metin ve bir dizi değerden oluşur. Değer kümesi, teklifler arasında değişebilen tek parçadır. Teklif oluşturma sırasında teklifi oluşturanın odaklanabileceği en önemli yön, teklif paketi şablonunda bluunan teklif veri yer tutucuları listesidir. Teklif verilerini kurmak için aşağıdakileri yapın.

1.  **Teklif yönetimi**'ne gidin.

1.  Sol gezinti bölmesinde **Kitaplığı** genişletin, **Teklif verileri**'ne gidin.

    >[!NOTE]
    > **Teklif verileri** sayfasında, **Aday ayrıntıları** ve **İş ayrıntıları** bölümleri vardır. Attract, sıra dışı birkaç teklif verisi yer tutucusu sağlar.
    
    > Farklı teklif veri yer tutucularını mantıksal gruplar halinde düzenlemek için sayfada bölümler vardır. Bu bölümler, teklif verilerinin bakımı ve verilerin teklif oluşturma işlemi sırasında doldurulmasına yardımcı olur.

1.  Yeni bir teklif veri bölümü oluşturmak için **Bölüm ekle**'ye tıklayın ve bölüm için benzersiz bir ad girin.

1.  Herhangi bir bölüm için teklif verisi yer tutucular eklemek için **Teklif verisi ekle**'ye tıklayın ve yer tutucu için benzersiz bir ad girin.

1.  Her bölümün adını düzenlemek için bölüm adının üzerine getirin ve adı güncelleştirin.

1.  Varolan bir teklif veri yer tutucu adını düzenlemek için önce yer tutucunun zaten bir şablon parçası olmadığından emin olun. Daha sonra teklif veri yer tutucu adına getirin ve adı gerektiği şekilde güncelleştirin.

1. Varolan bir teklif veri yer tutucuyu silmek için önce yer tutucunun başka bir şablon parçası olmadığından emin olun. Daha sonra yer tutucuya getirin ve çöp tenekesi simgesini göründüğü zaman çöp tenekesine tıklayıp teklif veri yer tutucuyu silin.
    >[!NOTE]
    > Bir teklif veri parçası yanında numara göstergesi parçası olarak kaç şablonun bir teklif verisi yer tutucu parçası oldğunu görebilirsiniz. 

1. Herhangi bir bölümü silmek için adın üzerine getirin. Teklif veri yer tutucular bölüm içindeki hiçbir şablonda görünmüyorsa, iletiyi silmek için çöp tenekesi simgesini tıklatabilirsiniz. 
    >[!NOTE]
    > Bölümün silinmesi o bölümün içindeki tüm teklif veri yer tutucuları da siler.

Teklif veri yer tutucuları ayarlandıktan sonra belge şablonlarında kullanabilirsiniz. Teklif veri yer tutucularının belirli bir şablona sınırlama yoktur, aynı grup tüm şablonlarda kullanılabilir.

## <a name="offer-data-rules"></a>Teklif verisi kuralları

Çoğu kuruluş teklifler nasıl oluşturulması gerektiğiyle ilgili kurallara sahiptir. Örneğin, bir organizasyon belirli bir konum ve kıdem düzeyi birleşimi için maksimum yıllık teklifin belirli bir aralıkta olmasını veya yeni işe alım için teklif düzeyi için yalnızca birkaç belirli olası değer olmasını gerektirebilir. Attract, şu anda bir CSV dosyası kullanarak tüm bu gibi verileri kurallarını destekler.

Veri kuralları CSV dosyasını hazırlamak için aşağıdakileri yapın.

1.  Kural kümesi için teklif veri yer tutucuyu belirleyin. Örneğin, **Yıllık Maaş**.

1.  Bağımlı teklif veri yer tutucu değerlerini tanımlayın. Örneğin, **İş Konum** ve **Düzeyi**.

1.  Sütun 1 ve 2'yi **İş Yeri** ve **Düzey** olarak belirtin.

1.  Aralığı değerini yüklemek için , sütun 3 ve 4'ü **Yıllık ücret** yapın. Aralık yerine belirli bir değeri karşıya yüklemek için, yalnızca sütun 3'ü **Yıllık ücret** yapın.

1.  Microsoft Excel dosyasını gerekli rollere göre doldurun.

1.  Her satırın, tüm değerlerin benzersiz birleşimini bir araya getirdiğinden emin olun.

1.  Dosyayı CSV formatında kaydedin.

Teklif veri kuralları dosyasını yüklemek için aşağıdakileri yapın.

1.  **Teklif yönetimi**'ne gidin.

1.  Sol gezinti bölmesinde **Kitaplığı** genişletin, **Teklif verileri kuralları**'na gidin.

1.  **Yeni veri kümesi**'ne tıklayıp **Karşıya yükle** iletişim kutusunu görüntüleyin.

1.  Kural kümesi için benzersiz bir ad belirtin ve kaydedilmiş CSV dosyasını karşıya yükleyin.

1.  **Ekle** seçeneğini tıklatın.
    Kural kümesi arka planda işlenir ve tamamlandıktan sonra uygulama içinde ve e-posta yoluyla bildirilir.

    Karşıya yükleme işlemi sırasında hatalar oluşursa size bildirilir. Daha sonra hata günlüğünü indirip, dosyayı düzeltip yeniden yükleyin.

1.  Üç nokta (**...**) düğmesini, kural kümesini yüklemek ve değerler kümesini güncelleştirmek istiyorsanız kullanın. Güncelleştirmeden sonra dosyayı yeniden yükleyebilirsiniz.

1.  Tanımlanan yer tutucu başka bir belge şablonunda kullanılmıyorsa varolan kural kümesinin karşıya yüklemesini silebilirsiniz.

>[!NOTE]
> - Her bir yer tutucu yalnızca bağımlı olduğu benzersiz sütunlar kümesi olabilir. Örneğin, **Yıllık ücret**, **Şş yeri** ve **Düzey**'e bağlıysa **Yıllık ücret**'in farklı bir sütun kümesine bağlı olduğu başka bir kural kümesine yükleyemezsiniz.

> - Örnek teklif veri kuralı kümesini **Teklif veri kuralları** sayfasındaki **Örnekler** sekmesinden indirebilirsiniz.

> - Teklifi oluşturan kişi, teklif veri kuralları tarafından önerilen değerleri değiştirdiğinde, teklifi standart olmayan olarak işaretlenir ve teklif onayı iş akışı zorunlu olur.

## <a name="document-templates"></a>Belge şablonları

Teklif belge şablonu, yöneticilerin teklif mektupları oluşturmasına yardımcı olabilir. Teklif belge şablonu, tanımlanan teklif veri yer tutucularının yanı sıra teklifin parçası olan metnin birleşimidir. 

Teklif belge şablonu oluşturmak için aşağıdakileri yapın.

1.  **Teklif yönetimi**'ne gidin.

1.  Sol gezinti bölmesinde **Kitaplığı** genişletin, **Şablonlar**'a gidin.

    **Şablonlar** sayfası, önceden tanımlanmış belge şablonları listesini görüntüler.

1.  Yeni bir belge şablonu oluşturmak için **Yeni Şablon**'a tıklayın.

1.  Şablon için benzersiz bir ad girin ve **Oluştur**'a tıklayın.

1.  Teklif belge içeriğini girmek veya düzenlmek için zengin metin düzenleyici kullanın. Tablolar, resimler ve köprüleri metin düzenleyicisi üstündeki seçenekleri kullanarak ekleyebilirsiniz.

1.  Teklif şablonu belgesinde teklif veri yer tutucuları ekleyebilirsiniz:

    - Sağ bölmeden sürükleyip bırakarak.

    - Teklif veri yer tutucuyu doğrudan konumuna etiketleyin. **\#** yazın ve teklif veri yer tutucu adı yazmaya başlayın. Seçenekler açılan listesinde görünür. Teklif veri yer tutucu eklemek için **Enter**'a tıklatın veya basın.

    >[!NOTE]
    > - Yer tutucuyu teklif belge şablonuyla ilişkilendirmek için, değerini adaya sunmadan, teklif veri yer tutucuya gidin ve  **Sabitle** simgesine tıklayın. Bu, yer tutucuyu teklif belge şablonunun **Sabitlenen teklif verisi** bölümüne gönderir. Bırakmak için aynı adımları uygulayın ancak teklif veri yer tutucular listesinde **Bırak**'a tıklayın.

    > - Etkin teklif beri yer tutucular listesini görüntülemek için sağ bölmede **Etkin** sekmesine geçin.

    > - Teklif veri kuralı kümesi tarafından yönetilen bir yer tutucu eklemek isterseniz, teklif veri yer tutucunun diğer değerlere bağımlılığı görebilirsiniz.

    > - Alternatif olarak, içeriği yerel makinenizdeki bir .docx dosyasından **İçe Aktar** yapabilir ve gerektiği gibi düzenleyin. Böylece, düzenleyicideki tüm içeriği yazmanız gerekmez.

1. Teklif belgesinin önizlemesini yapmak için sayfanın üstündeki **Önizleme** seçeneğini kullanın.

1. Teklifi oluşturan kişiin teklif belge içeriği düzenlemesini kontrol etmek için sayfanın üstündeki **İzni yönet** seçeneğini kullanın. Teklif oluşturanın yalnızca yer tutucu değerlerini eklemesini ve metni düzenlememesini isterseniz izin değerini **Hayır** olarak ayarlayın.

1. İlerlemenizi kaydetmek için **Kaydet**'i tıklatın. Şablon taslak durumunda kaydedilir.

1. Belgeyi son haline getirmek ve yayımlandı olarak işaretlemek için **Bitir**'e tıklayın.

1. Hangi bölge şablonlarının şu anda aktif, hangilerinin taslak modunda ve hangilerinin arşivlendiğini veya artık belge şablonları kitaplığının deneyiminde kullanımda olmadığını görebilirsiniz.

>[!NOTE]
> Varolan bir teklif paketi şablonunun parçası olmayan teklif belgesi şablonlarını silebilirsiniz.


## <a name="offer-package-templates"></a>Teklif paketi şablonları

Teklif paketleri, adayla paylaşılan ve bir veya daha falza teklik belge şablonu birleşiminden oluşan teklif parçalarıdır. Teklif paketi oluşturmak için aşağıdakileri yapın.

1.  **Teklif yönetimi**'ne gidin.

1.  Sol gezinti bölgesinden **Paketler**'e gidin.

    Teklif oluşturanlar için kullanılabilir olan etkin paket şablonları listesi görüntülenir.

1.  Yeni bir teklif paketi oluşturmak için **Yeni Paket**'e tıklayın.

1.  Benzersiz bir ad girin ve **Oluştur**'a tıklayın.

1.  **Şablon ekle**’yi tıklatın.

    >[!NOTE]
    > - Yeni bir şablon oluşturmayı veya mevcut bir modelden seçmeyi seçebilirsiniz.

    > - Varolan bir şablonu eklemek isterseniz, teklif belge şablonunun kaydedilmiş, sonlandırılmış ve etkin olarak işaretlenmiş olduğundan emin olmak gerekir.
    
    > - İstediğiniz sayıda belge şablonu seçebilirsiniz. 
    
1.  **Paket yönetimi**'ne dönmek için **Bitti**'ye tıklatın.

    Belge sırasını yapılandırın ve belirli teklif belgesinin tekli oluşturma sırasında gerekip gerekmediğini de işaretleyin. Teklif oluşturan, **Gereksiz** olarak işaretlenen belgeleri silme seçeneğine sahiptir.

1. Teklif paketi şablonunun tüm teklif oluşturan kullanıcılar tarafından kullanılabilir olması için **Kaydet ve yayınla**'ya tıklayın.

   Taslak teklif paketi şablonlarını görüntülemek için **Taslaklar** sekmesine gidin. Teklif paket şablonuna değişiklik yapılırsa, kaydedilmesi ve yeniden yayınlanması gerekir.

## <a name="configure-an-offer-process"></a>Teklif sürecini yapılandırma

Attract yöneticisi tarafından yapılandırılabilir teklif oluşturma işleminin birden çok bölümü vardır.

- **Teklif onayları** - Teklif onaylarının, teklifini adaya gönderilebilmesi için gerekip gerekmediğini belirleyin. Yönetici olarak, tüm teklif onaylarının sıralı bir şekilde veya paralel onay iş akışıyla olacağını belirleyebilirsiniz. Teklif onaylayanların, teklifi onaylarının yanı sıra bir açıklama eklemesini gerektirebilirsiniz. Teklif onayları, standart olmayan teklifler için zorunludur.

- **Adayın teklif deneyimi** - Yönetici olarak, tüm tekliflerin bitiş tarihi olmasını seçebilirsiniz, bu durumda bitiş tarihinin varsayılan mahsubunun ne olması gerektiğini de seçmelisiniz. Adayların bir teklif reddedip reddemeyeceğini de yapılandırabilirsiniz.

- **e-İmzalar** - Bir yönetici olarak, adayların tekliflere imza atabilecekleri yöntemleri seçebilirsiniz.
    - Adobe Sign - Tüm teklif paketleri Adobe Sign ile gönderilir. Teklifi yayınlayan her teklif oluşturucusunun kendi Adobe Sign lisansını Attract'e bağlamış olması gerekir. 

    - ESign - Bu varsayılan seçenektir, kullanıma hazırdır, kullanıcı kendi adını ve baş harflerini yazarak imza atabilir.

Teklif oluşturma işlemi hakkında daha fazla bilgi için bkz: [Teklif oluşturma, onaylama ve imzalama](./creating-offers.md).

