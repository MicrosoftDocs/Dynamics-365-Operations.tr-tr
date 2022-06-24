---
title: cXML geliştirmeleri satın alma
description: Satın alma cXML geliştirmeleri özelliği, satınalma talepleri için kullanılan harici katalog işlevi olan PunchOut üzerinde oluşturulur.
author: GalynaFedorova
ms.date: 08/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatCXMLParameters, CatCXMLPurchRequest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2020-08-03
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 87dccd19ade1b27db9a6d454659fec6142de4c65
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890929"
---
# <a name="purchasing-cxml-enhancements"></a>cXML geliştirmeleri satın alma

[!include [banner](../includes/banner.md)]

_Satın alma cXML geliştirmeleri_ özelliği, satınalma talepleri için kullanılan [harici katalog işlevi](set-up-external-catalog-for-punchout.md) üzerinde oluşturulur. Var olan bu işlevsellik, _PunchOut_ olarak bilinir. Satınalma siparişinin kaynağı satınalma siparişinden kaynaklanmasa da, satınalma siparişindeki satıcı ile satınalma siparişi belgesini göndermek için kullanılan parametreler arasında bağlantı olmalıdır.

## <a name="turn-on-the-purchasing-cxml-enhancements-feature"></a>cXML geliştirmeleri satın alma özelliğini açma

Özelliği etkinleştirmek için, **[Özellik Yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** sayfasını açın ve *cXML Geliştirmeleri Satın Alma* adlı özelliği arayın. Özelliği seçin ve açmak için **Şimdi etkinleştir** düğmesini seçin. (Supply Chain Management sürüm 10.0.21 itibariyle, bu özellik varsayılan olarak açıktır.)

Bu özelliği açtıktan sonra, aşağıdaki üç alanda ayarları yapılandırmalısınız:

- **[cXML parametreleri](#cxml-parameters)**: Satınalma siparişlerini gönderme işleviyle ilgili bazı genel parametreleri ayarlamak için bu ayarları kullanın.
- **[Satıcı kurulumu](#vendor-setup)**: Herhangi bir satıcı için oluşturulan tüm yeni satınalma siparişleri için Commerce Genişletilebilir İşaretleme dili (cXML) varsayılan olarak kullanılacaksa, satıcı için **cXML üzerinden satınalma siparişi gönder** seçeneğini _Evet_ olarak ayarlayın.
- **[Harici kataloglar](#external-catalog-setup)**: Satınalma siparişi belgesinin biçimini ve nasıl gönderildiğini tanımlamak için yeni **Sipariş özellikleri** ayarlarını kullanın.

Aşağıdaki çizim bu yapılandırmayı özetler.

![cXML özelliklerini ayarlamak için alanlar.](media/cxml-settings-areas.png "cXML özelliklerini ayarlamak için alanlar")

Ek olarak, [Satınalma siparişi talebi toplu işini](#po-batch) ayarlamanız gerekir. Bu toplu işlem, teyit edilen satınalma siparişlerini göndermek için kullanılır.

## <a name="set-up-global-cxml-parameters"></a><a name="cxml-parameters"></a>Genel cXML parametrelerini ayarlama

**cXML parametreleri** sayfasını kullanarak satınalma siparişlerini gönderme işleviyle ilgili bazı genel parametreleri ayarlayabilirsiniz.

![cXML parametreleri sayfası.](media/cxml-parameters.png "cXML parametreleri sayfası")

**Satın alma ve kaynak hizmeti \> Kurulum \> cXML yönetimi \> cXML parametreleri** bölümüne gidin ve aşağıdaki parametreleri ayarlayın:

- **cXML test modu**: Bu genel parametre, satınalma siparişlerinin fiziksel olarak toplu işten gönderilme biçimini etkiler. Aşağıdaki değerlerden birini seçin:

    - **Test**: Bu modda, toplu işlem çalışabilir ve ileti için XML belgesi oluşturulur ancak gönderilmez. Bunun yerine, satınalma siparişi talebinde gözden geçirme amacıyla kaydedilir. Bu mod, ilk uygulamayı yapıyorsanız ve verilerin cXML iletisine nasıl girildiğini görmek istediğinizde yararlıdır. İlk doğrulama için satıcılara gönderebileceğiniz örnek iletileri de oluşturmak isteyebilirsiniz.
    - **Canlı**: Bu modda, her belgeyi satıcıya fiziksel olarak aktarmak için özellik [harici katalog ayarlarını](#external-catalog-setup) kullanır.

- **Satınalma talebi güncelleştirmelerini gönder**: Satınalma siparişleri için güncelleştirme iletisi göndermek üzere bu seçeneği *Evet* olarak ayarlayın. İletinin gönderilmesini önlemek için *Hayır* olarak ayarlayın. Satıcıların çoğu güncelleştirme iletilerini almamayı tercih eder. Bunun yerine, bir satınalma siparişinin değiştirilmesi gerekiyorsa, müşterilerin onlara telefon veya e-posta ile başvurmaları istenir. Bu parametre genel bir parametredir ve her satıcı için harici katalogda geçersiz kılma belirtilemez. Satınalma siparişinde ikinci bir onay deftere naklederseniz, ancak ilk onay satıcı tarafından zaten gönderilip onaylanacaksa, bir satınalma siparişi güncelleştirildi olarak işaretlenir. İkinci bir onay işareti varsa, ancak ilk onay gönderilmediyse, ikinci onay yeni bir belge olarak kabul edilir. Bir onay gönderilene kadar bir satınalma siparişini istediğiniz kadar doğrulayabilirsiniz. Sonraki onay daha sonra güncelleştirme iletisi olarak kabul edilecek.
- **Satınalma talebi silme isteği gönder**: Satınalma siparişleri için silme iletisi göndermek üzere bu seçeneği *Evet* olarak ayarlayın. İletinin gönderilmesini önlemek için *Hayır* olarak ayarlayın. Satıcıların çoğu silme iletilerini almamayı tercih eder. Bunun yerine, bir satınalma siparişinin istenmeden gönderildiyse, müşterilerin telefon veya e-posta ile başvurmaları istenir. Bu parametre genel bir parametredir ve her satıcı için harici katalogda geçersiz kılma belirtilemez. Supply Chain Management'ta satınalma siparişini iptal ederseniz, satınalma siparişi silindi olarak işaretlenir.
- **Arşiv dosyası**: Arşivlenen cXML belgelerini dışa aktarmak ve kaydetmek istediğiniz dosya yolunu belirtin. Bu yol, **Satınalma siparişi talep** sayfasından temizleme işlevini çalıştırdığınızda kullanılır.
- **Cadde satırı için maksimum karakter sayısı**: cXML belgesindeki adresler için cadde alanında kullanılabilecek maksimum karakter sayısını girin. Harici katalog özelliklerinde geçersiz kılma belirtilmedikçe, bu genel parametre tüm satıcıları etkiler.

## <a name="set-up-vendor-purchase-orders-to-use-cxml"></a><a name="vendor-setup"></a>cXML kullanmak için satıcı satınalma siparişleri ayarlama

**cXML üzerinden satınalma siparişi gönder** seçeneği _Evet_ olarak ayarlanmış bir satınalma siparişini her onayladığınızda, sistem cXML iletisini otomatik olarak oluşturur ve bunu bu satınalma siparişiyle ilişkilendirilen satıcıya teslim eder. Satınalma siparişleriniz için bu seçeneği kontrol etmenin iki yolu vardır:

- Bir satıcının, bir talepten oluşturulan tüm yeni satınalma siparişleri için cXML 'yi otomatik olarak kullanmasını sağlayacak şekilde ayarlamak için, **Satın alma ve kaynak hizmeti \> Satıcılar \> Tüm Satıcılar** sayfasına gidin ve ayrıntılar sayfasını açmak için satıcı seçin veya oluşturun. Ardından, **Satınalma siparişi varsayılanları** hızlı sekmesinde, **Satınalma siparişini cXML üzerinden gönder** seçeneğini _Evet_ olarak ayarlayın. cXML bir talepten **oluşturulmamış** yeni satınalma siparişleri için otomatik olarak kullanılıyorsa, bu makalede daha sonraki [Sipariş özelliklerini ayarlama](#set-order-properties) bölümünde açıklandığı **ENABLEMANUALPO** sipariş özelliği ilgili harici kataloglar için _True_ olarak ayarlanmalıdır.
- Tek tek satınalma siparişleri için, **Satın alma ve kaynak hizmeti \> Satınalma siparişi \> Tüm satınalma siparişleri** sayfasına gidin ve ayrıntılar sayfasını açmak için bir satınalma siparişi seçin veya oluşturun. **Üst bilgi** görünümüne geçin ve **Kurulum** hızlı sekmesinde, **Satınalma siparişini cXML ile gönder** seçeneğini kullanarak ayarlayın.

![Satıcı satınalma siparişleri için varsayılan ayarlar.](media/cxml-order-defaults.png "Satıcı satınalma siparişleri için varsayılan ayarlar")

## <a name="set-up-an-external-catalog-to-use-cxml"></a><a name="external-catalog-setup"></a>cXML kullanmak için harici bir katalog ayarlama

**Harici kataloglar** sayfasında tüm kataloglarınız için PunchOut işlevlerini ve satınalma siparişi gönderme işlevlerini ayarlayabilirsiniz. İlgili ayarları bulmak için, **Satın alma ve kaynak hizmeti \> Katalogları \> Harici kataloglar** sayfasına gidin. [Her kataloğu her zamanki gibi ayarlamakla](set-up-external-catalog-for-punchout.md) başlayın. Bu süreç, satıcı atamayı, satıcının sağlayabileceği kategorileri seçmeyi ve kataloğu etkinleştirmeyi içerir. Daha sonra bu bölümde açıklanan ek ayarları yapılandırın.

> [!NOTE]
> cXML üzerinden gönderilebilecek bir satınalma siparişini teyit ettiğinizde, sistem satınalma siparişiyle ilişkilendirilmiş olan satıcıyı arar ve o satıcıyla ilişkilendirilmiş olan ilk etkin harici kataloğu bulur. Sistem daha sonra satınalma siparişi göndermek için o harici katalogdaki ayarları kullanır. Birden fazla harici katalog ayarlandıysa, sistem satınalma siparişindeki satıcıyı temel alarak bulduğu ilk harici kataloğu kullanır. Bu nedenle, her satıcı için yalnızca bir harici katalog oluşturmanız önerilir.

![Harici katalog ayarları.](media/cxml-supplier-catalog.png "Harici katalog ayarları")

### <a name="set-the-punchout-protocol-type"></a>PunchOut protokol türünü ayarlama

**Harici kataloglar** sayfasının **Genel** hızlı sekmesinde, **Punchout protokol türü** alanını _cXML_ olarak ayarlayın. Bir ortak işlevi genişletmedikçe ve uzantı içinde ek bir seçenek sağlamadıkça bu seçenek tek kullanılabilir seçenek olacaktır.

Ayrıca, kataloğu PunchOut için kullanıyorsanız, [ileti biçimini de ayarlamanız](set-up-external-catalog-for-punchout.md) gerekir. İleti biçimi, talebin üzerindeki PunchOut hareketi içindeki satıcıya bağlantı kurmak için kullanılır. Bir satınalma siparişi gönderildiğinde, sipariş özellikleri bir satıcıyla bağlantı kurmak için kullanılır.

### <a name="set-the-order-properties"></a><a name="set-order-properties"></a>Sipariş özelliklerini ayarlama

_Satın alma cXML geliştirmeleri_ özelliği, harici kataloglar için yeni bir **Sipariş özellikleri** hızlı sekmesi ekler. Bu hızlı sekme, sipariş özelliklerini tanımlayabileceğiniz bir kılavuz sağlar. Ayrıca bir araç çubuğu da sağlar. Bu araç çubuğu, sipariş özelliklerini yönetmek için kullanabileceğiniz aşağıdaki üç düğmeyi içerir:

- **Varsayılan Özellikler**: Yeni bir katalog kurarken, kılavuza sık kullanılan önceden tanımlanmış bir özellik topluluğu eklemek için bu düğmeyi seçin.
- **Yeni**: Kılavuza yeni bir özellik ekleyin.
- **Sil**: Seçili durumdaki özelliği kılavuzdan silin. Varsayılan bir özelliği yanlışlıkla silerseniz, tüm eksik özellikleri geri yüklemek için **Varsayılan özellikler** ögesini seçin.

Kılavuza bir veya daha fazla özellik eklediğiniz her seferde, her biri için bir değer belirtmek üzere sağ sütunu kullanın.

Varsayılan özellikleri aşağıdaki şekilde kullanın:

- **BUYER\_COOKIE**: Bu izleme alanı, şirketinizle ilgili belirli bilgileri belirtmek için kullanılabilir. Satıcıyla bu özelliğin nasıl kullanıldığı hakkında bir sözleşmeniz yoksa, bir satınalma siparişi gönderirken çok fazla anlamı yoktur. Bu nedenle, bunu basit bir değere ayarlamalısınız.
- **DELIVERTO**: Sevkiyat Adresi belgeye satınalma siparişinden girildiğinde, XML iletisindeki **DeliverTo** alanını ayarlamak için **Dikkat bilgisi** alanı kullanılır. Bu değerin istekte bulunan bir ad olmasını istiyorsanız ve satınalma siparişi başlığında talep edilen alan alanını ayarlayacağından, bu özellik için _REQUESTER_ değerini girin ve böylece talep eden ad XML içindeki **DeliverTo** alanına girilir. Bu durumda, kullanılan birincil e-posta adresi ve telefon numarası sipariş eden yerine istekten bulunandan alınır.
- **DEPLOYMENTMODE**: Bu özelliği satıcının gerektirdiği şekilde ayarlayın. Değerler genellikle _PRODUCTION_ veya _TEST_ olur. Satıcıyla iletişiminizi temel alan değeri ayarlayın. Genellikle, satıcının test veya üretim sistemi olarak gösterdiği **ORDERCHECKURL** değerinin arkasında istenen sistemle eşleşmesi gerekir.
- **FIXEDBILLADDRESSID**: XML iletisindeki **addressID** alanı ayarlandığında, adreste belirtilen konumu seçer. Satıcıyla adreslediğiniz kimlik değeri belirli bir nedenle adres konumundaki değerden farklıysa, değeri burada belirterek geçersiz kılmaya zorlayabilirsiniz. Satıcıyla tek bir adres kullanacağınız gibi, adresin da satıcının sisteminde ayarlandığı bir adres olduğu varsayılmıştır. Fatura adresi, Supply Chain Management'te yasal varlık için belirtilen birincil fatura adresidir.
- **FIXEDSHIPADDRESSID**: XML iletisindeki **addressID** alanı ayarlandığında, adreste belirtilen konumu seçer. Satıcıyla adreslediğiniz kimlik değeri belirli bir nedenle adres konumundaki değerden farklıysa, değeri burada belirterek geçersiz kılmaya zorlayabilirsiniz. Satıcıyla tek bir adres kullanacağınız gibi, adresin da satıcının sisteminde ayarlandığı bir adres olduğu varsayılmıştır. Sevkiyat adresi, satınalma siparişinin başlığında belirtilen adrestir. Satıcıların çoğu satır adreslerini değil, yalnızca başlık adreslerini kabul eder. Satır adresleri için XML içinde alanlar olmasına rağmen, bunlar başlık adresine ayarlanırlar.
- **FROM\_DOMAIN**: Satınalma siparişi belgelerini göndermek için kullanılan değeri girin. Bu değer satıcınız tarafından sağlanır.
- **FROM\_IDENTITY**: Satınalma siparişi belgelerini göndermek için kullanılan değeri girin. Bu değer satıcınız tarafından sağlanır.
- **ORDERCHECKURL**: Satınalma siparişi belgelerinin transfer olduğu URL'yi girin. Bu URL `https://` ile başlar ve satıcınız tarafından sağlanır.
- **PAYLOAD\_ID**: Geçerli satıcı için kullanılan, iş süreçleri için gerekli olduğu şekilde, yük kodu için bir önek değeri girin.
- **SENDER\_DOMAIN**: Satınalma siparişi belgelerini göndermek için kullanılan değeri girin. Bu değer satıcınız tarafından sağlanır.
- **SENDER\_IDENTITY**: Satınalma siparişi belgelerini göndermek için kullanılan değeri girin. Bu değer satıcınız tarafından sağlanır.
- **SHARED\_SECRET**: Satınalma siparişi belgelerini göndermek için kullanılan değeri girin. Bu değer satıcınız tarafından sağlanır.
- **STREETLENGTH**: Satıcının sokak adı olarak kabul edeceği adrese ait maksimum karakter sayısını gösteren bir sayı girin. Buraya bir değer girilirse, **cXML parametreleri** sayfasında belirtilen değer geçersiz kılınır. Sistem, Supply Chain Management uygulamasında standart adrese, burada belirtilen sayıda karaktere sığmaya çalışacak şekilde satır sonlarını ve boşlukları kaldırır. Ek karakterler kesilir.
- **TO\_DOMAIN**: Satınalma siparişi belgelerini göndermek için kullanılan değeri girin. Bu değer satıcınız tarafından sağlanır.
- **TO\_IDENTITY**: Satınalma siparişi belgelerini göndermek için kullanılan değeri girin. Bu değer satıcınız tarafından sağlanır.
- **USERAGENT**: Kullanmakta olduğunuz sistemi tanımlamak için bir değer girin. Örneğin, _Dynamics 365 Supply Chain Management_ girin.
- **VERSION**: Satıcı bu bilgileri istiyorsa, cXML sürüm numarasını girin. Varsayılan sürüm *1.2.008*'dir. Bu sürüm kararlı ve çoğu satıcı tarafından kabul edilir.
- **RESPONSETEXT**: Sipariş gönderildikten sonra satıcının cXML yanıtı iletisinde iade olmasını beklediğiniz tüm özel metni girin. Bu şekilde, sistem iletiyi _Kabul edildi_ olarak işaretleyebilir. Yanıt, buraya girdiğiniz standart metin veya müşteri metniyle eşleşmezse, talep _Hata_ olarak işaretlenir.
- **RESPONSETEXTSUB**: **RESPONSETEXT** alanında belirtilen değerler için satıcı yanıt metninde arama yapmak istiyorsanız bu özelliği _TRUE_ olarak ayarlayın. Örneğin, satıcı yanıtta "OK" içeren bir uzun dize döndürebilir. Bu durumda, yanıtta herhangi bir yerde "OK" aramak için **RESPONSETEXT** alanına _OK_ ve **RESPONSETESTSUB** alanını _TRUE_ olarak ayarlayabilirsiniz. Böylece sipariş _Kabul edildi_ olarak ayarlanabilir.
- **CONTENTTYPE:** Tipik bir katalog kurulumunda bu özelliği ayarlamak zorunda değilsiniz. Bir satın alma siparişi gönderdiğinizde bir satıcının sisteminden sunucu 500 hatası alırsanız, bu özelliği _FALSE_ olarak ayarlayarak test yapabilirsiniz. Bu değer Web isteğindeki bir ayarı değiştirir ve bazı platformlar için iletinin gönderilmesini de sağlayabilir.
- **ENABLEHEADERS**: Başlıkları satınalma siparişiyle birlikte göndermek için bu özelliği _TRUE_ olarak ayarlayın. Bu özelliği yalnızca satıcı gerektiriyorsa ayarlamalısınız. Bu özelliği _TRUE_ olarak ayarlarsanız, satıcının sağladığı adlara göre ek özel özellikler ekleyin ve bunlara _H\__ ön ekini ekleyin. Tipik örnekler arasında **H\_UserID**, **H\_Password**, **H\_RECEIVERID** ve **H\_ActionRequest** sayılabilir. Aşağıdaki özel özellikler varsayılan özelliklere dahil edilmiştir:

    - **H\_USERID**: Ticari ortak, satınalma siparişi göndermek için URL'nin bir parçası olarak kullanıcı kimliği göndermenizi gerektiriyorsa, değeri buraya girin.
    - **H\_PASSWORD**: Ticari ortak, satınalma siparişi göndermek için URL'nin bir parçası olarak parola göndermenizi gerektiriyorsa, değeri buraya girin.

- **ENABLEMANUALPO**: Bu özellik _TRUE_ olarak ayarlanırsa, kullanıcılar satınalma siparişlerini el ile oluştururken (diğer bir deyişle, bir talep ile başlamazlarsa), bu satınalma siparişlerinin ayarları **Satıcıdan cXML aracılığıyla satınalma siparişi gönder** seçeneğinden gelir. Bu özellik ayarlanmamışsa veya _FALSE_ olarak ayarlandıysa, **cXML üzerinden satınalma siparişi gönder** seçeneği el ile oluşturulan satınalma siparişleri için satınalma sipariş başlığında ayarlanmayacaktır. Bir talepten oluşturulan satınalma siparişleri için, **cXML üzerinden satınalma siparişi gönder** seçeneği ayarı, bu özelliğin ayarı ne olursa olsun satıcıdan her zaman devralınır. Daha fazla bilgi için, bu makalenin yukarısındaki [cXML kullanmak için satıcı satınalma siparişleri ayarlama](#vendor-setup) konusuna bakın.
- **PUNCHOUTPOONLY**: Bu özellik _TRUE_ olarak ayarlanırsa, yalnızca PunchOut sürecinden oluşturulan satınalma talep satırları satınalma siparişi başlığındaki **cXML üzerinden satınalma siparişi gönder** seçeneğini ayarlar. Ayrıca, satınalma siparişindeki tüm satırların satınalma talebi satır türü _Harici katalog maddesi_ olmalıdır. Aksi takdirde, cXML satınalma siparişi oluşturulamaz.
- **PUNCHOUTSHIPTO**: Bu özellik _TRUE_ olarak ayarlanırsa, yasal varlığın varsayılan adresi, kullanıcı bir harici kataloğu açtığında, PunchOut kurulum istek iletisine eklenir. Bu adres, **ShipTo** adresi olarak eklenir. Satıcılar şirketin konumunu temel alarak fiyatlandırmayı göstermek için **ShipTo** adresini kullanır.
- **TRACEPUNCHOUT**: Talepten harici bir kataloğa göz atmaya çalıştığınızda bir hata iletisi alırsanız bu özelliği _TRUE_ olarak ayarlayın. Böylece, izleme bilgileri, Supply Chain Management uygulaması ile satıcı sitesi arasında gönderilen **PunchOutSetupRequest** ve **PunchOutResponse** iletileri için doldurulacaktır. Bu bilgileri, sorun yaşadığınız satıcı kataloğu için **Harici katalog kurulum** sayfasından açabileceğiniz **cXML sepeti ileti günlükleri** sayfasında görüntüleyebilirsiniz. Bu özelliği, yalnızca sorun giderme işlemi yapıyorsanız _TRUE_ olarak ayarlamalısınız, çünkü her PunchOut için veritabanında büyük bir performans yükü oluşturur. Daha fazla bilgi için, bu makalenin ilerleyen bölümlerindeki [Harici Katalog PunchOut içindeki cXML sepeti ileti günlüklerini görüntüleme](#message-log) bölümüne bakın.
- **REPLACENEWLINE**: Bir satıcının sistemi, yeni satır karakterleri içeren bir **PunchOutResponse** iletisi gönderdiği için (\\n) sorun yaşıyorsanız, bu özelliği _TRUE_ olarak ayarlayın. Bu sorun, satıcının iletileri ara yazılım veya satınalma hub'ı üzerinden ayrıştırıldığında oluşabilir. Yeni bir satıcı kurulumuyla ilgili sorununuz varsa, **PunchOutResponse** iletisini görüntülemek ve XML etiketlerinin yeni satır karakterleri tarafından bölünmeyeceğini belirlemek için **TRACEPUNCHOUT** özelliğini _TRUE_ olarak ayarlayın.
- **POCOMMENTS**: cXML belgesinin, Supply Chain Management uygulamasında satınalma siparişine iliştirilmiş notları içermesini istiyorsanız bu özelliği _TRUE_ olarak ayarlayın. İliştirilmiş metni, satınalma siparişi iletisindeki başlık açıklamalarına dahil edilir. Sistemin bu ekleri nasıl seçtiği ve işlediği hakkında daha fazla bilgi için, bu makalenin ilerleyen kısımlarında bulunan [Bir satın alma siparişine not ekleme](#attach-po-notes) konusuna bakın.
- **VENDCOMMENTS**: cXML belgesinin, Supply Chain Management uygulamasında satınalma siparişine iliştirilmiş notları içermesini istiyorsanız bu özelliği _TRUE_ olarak ayarlayın. İliştirilmiş metni, satınalma siparişi iletisindeki başlık açıklamalarına dahil edilir. Sistemin bu ekleri nasıl seçtiği ve işlediği hakkında daha fazla bilgi için, [Bir satın alma siparişine not ekleme](#attach-po-notes) konusuna bakın.
- **CLEANAMP**: Bir satıcıda PunchOut işlemini denediğinizde ve satıcının dönüş URL'si yanlış kodlanmış ve işareti (\&) değerini içeriyorsa bir hata iletisi alırsanız bu özelliği _TRUE_ olarak ayarlayın.
- **PUNCHOUTTZ**: Üzerinde çalıştığınız satıcı, PunchOut istek iletisinin tarih/saatine ilişkin belirli bir doğrulama işlemi yapmak üzere Uluslararası Standartlaştırma Örgütü (ISO) 8601 standardını kullanıyorsa, bu özelliği _TRUE_ olarak ayarlayın. Supply Chain Management, **PunchOutSetupRequest** iletisindeki Eşgüdümlü Evrensel Saat (UTC) tarihini kullanır. Bu nedenle, bu özelliği _TRUE_ olarak ayarladığınızda, *+00:00* tarih/saat biçimine eklenir.
- **WMSADDRESSID**: Satıcıya gönderilen satınalma siparişi talebi için **ShipTo** adresindeki **addressID** değeri olarak satınalma siparişi başlığındaki ambar numarasını kullanmak için bu özelliği _TRUE_ olarak ayarlayın. **FIXEDSHIPADDRESSID** özelliği için bir değer ayarlarsanız, bu değer diğer değere göre öncelik kazanır. Bu nedenle, bir özelliği veya diğerini, belgenin **ShipTo** adresindeki **addressID** değerini ayarlamak için kullanmalısınız.
- **PUNCHOUTSHIPTOUSER**: Bu özellik, **PUNCHOUTSHIPTO** özelliği ile birlikte çalışır. **PUNCHOUTSHIPTO** _TRUE_ olarak ayarlanırsa, yasal varlığın adresi çekilir. **PUNCHOUTSHIPTOUSER** _TRUE_ olarak ayarlanırsa, yasal varlık adresi yerine PunchOut kullanıcısının birincil adresi kullanılır.

### <a name="activate-the-external-catalog"></a>Harici kataloğu etkinleştirme

Harici kataloğunuz için tüm özellikleri ayarlamayı ve diğer ayarları yapılandırmayı bitirdiğinizde, **Harici kataloglar** sayfasının **Genel** hızlı sekmesine gidip **Etkin** seçeneğini *Evet* olarak ayarlayın.

### <a name="attach-notes-to-a-purchase-order"></a><a name="attach-po-notes"></a>Bir satın alma siparişine not ekleme

[Sipariş özelliklerini ayarlama](#set-order-properties) bölümünde belirtildiği gibi, sağlanan cXML'nizin ilgili satınalma siparişi ve/veya satıcı kayıtlarına iliştirilmiş notlardan metin içermesini istiyorsanız, harici katalog kurulumunda **POCOMMENTS** ve/veya **VENDCOMMENTS** özelliklerini _TRUE_ olarak ayarlayabilirsiniz. Bu bölümde sistemin, kullanıyorsanız bu ekleri nasıl seçtiği ve işlediği hakkında daha fazla ayrıntı sağlanır.

Sistemin bakacağı not tiplerini ayarlamak için **Satın alma ve kaynak hizmeti \> Kurulum \> Formlar \> Form kurulumu** sayfasına gidin. Daha sonra, **Satınalma siparişi** sekmesinde, **Eklenecek belge türü** alanını, dahil etmek istediğiniz not tipine göre ayarlayın. Belge ekleri değil, yalnızca metin notları dahil edilir.

![Form kurulum sayfası.](media/cxml-form-setup.png "Form kurulum sayfası")

Bir satınalma siparişi yalnızca **Tür** alanları **Eklenecek belge türü** alanında seçtiğiniz değere ayarlanmışsa ve **Sınırlama** alanları _Harici_ olarak ayarlanmışsa, ekler bir satınalma siparişine dahil edilir. Bir satınalma siparişi için ekler oluşturmak, görüntülemek veya düzenlemek için, **Satın alma ve kaynak hizmeti \> Tüm satınalma siparişleri** sayfasına gidin satınalma siparişi seçin veya oluşturun, sonra sağ üst köşedeki **Ekler** düğmesini (ataş simgesi) seçin.

![Satıcıya gönderilmek üzere ayarlanan iliştirilmiş not.](media/cxml-note-to-vendor.png "Satıcıya gönderilmek üzere ayarlanan iliştirilmiş not")

## <a name="view-the-cxml-cart-message-log-for-external-catalog-punchout"></a><a name="message-log"></a>Harici katalog PunchOut işlemi için cXML sepeti ileti günlüğünü görüntüleme

Bir harici katalog için **Punchout protokol türü** alanını _cXML_ olarak ayarladığınızda, sistem satıcılardan geri gelen iadelerin bir ileti günlüğünü yakalar. Bu günlük, sorun giderme ve diğer veri amaçları için kullanılabilir.

Harici bir kataloğun günlüğünü açmak için ilgili kataloğu seçin ve Eylem Bölmesi'nde, **cXML sepet ileti günlüğü** sepetini seçin. **cXML sepet iletisi günlüğü** sayfası iade edilmiş sepetlerin listesini, bu sepetlerle ilgili XML'i ve ilgili satınalma talebinde oluşturulan satırları gösterir.

![cXML sepeti ileti günlükleri sayfası.](media/cxml-cart-message-log.png "cXML sepeti ileti günlükleri sayfası")

## <a name="set-the-extrinsic-elements-for-external-catalog-punchout"></a>Harici katalog PunchOut işlemi için ikincil öğeleri ayarlama

Bir harici katalog için **Punchout protokol türü** alanını *cXML* olarak ayarladığınızda, istek XML iletisinde doğru yere eklenecek özel ikincil öğeler ekleyebilirsiniz.

Bir harici kataloğa ikincil öğeler eklemek için, aşağıdaki adımları izleyin.

1. **Satın alma ve kaynak hizmeti \> Kataloglar \> Harici kataloglar** sayfasına gidin.
1. İlgili kataloğu seçin.
1. **İleti biçimi** hızlı sekmesinde, **Extrinsics** bölümünde, eklemek istediğiniz her bir ikinci öğe için kılavuza satır eklemek üzere **Ekle**'yi seçin. Her satırda, aşağıdaki alanları ayarlayın:

    - **Ad**: Öge için bir ad girin. Bu değer, her bir satır tarafından oluşturulan **Extrinsic** XML öğesinin **ad** özniteliğinin değeri olur. Genellikle, satıcınızla her ikinci öğenin adı konusunda uzlaşmak için birlikte çalışırsınız.
    - **Değer**: Öğe için bir değer seçin. Bu değer, her bir satır tarafından oluşturulan XML öğesinin değeri olur. Aşağıdaki değerler kullanılabilir:

        - **Kullanıcı adı** PunchOut işlemini yapan kullanıcının adını kullanın. Bu ad, Supply Chain Management'ta oturum açılan addır.
        - **Kullanıcı e-posta adresi** PunchOut işlemini yapan kullanıcının e-posta adresini kullanın. Bu adres **Kullanıcı seçenekleri** sayfasının **Hesap** sekmesinde kullanıcının ayarladığı adrestir.
        - **Rasgele değer**: Benzersiz rasgele bir değer kullanın.
        - **Kullanıcının tam adı**: Harici kataloğa erişen kullanıcıyla ilişkili ilgili kişinin tam adını kullanın.
        - **Adı**: Harici kataloğa erişen kullanıcıyla ilişkili ilgili kişinin adını kullanın.
        - **Soyadı**: Harici kataloğa erişen kullanıcıyla ilişkili ilgili kişinin soyadını kullanın.
        - **Telefon numarası**: Harici kataloğa erişen kullanıcıyla ilişkili ilgili kişinin birincil telefon numarasını kullanın.

![Extrinsic öğesi ayarları.](media/cxml-extrinsics.png "Extrinsic öğesi ayarları")

Kullanıcı veya yönetici, ikincil öğeleri göremez ve bu nedenle kullanıcının bir PunchOut işlemi yapana kadar eklenmezler. Bunlar, cXML kurulum isteği iletisindeki **BuyerCookie** ve **BrowserFromPost** öğeleri arasına otomatik olarak eklenecektir. Bu nedenle, harici kataloğu kurarken XML'de el ile kurmanız gerekmez.

![XML'e eklenen extrinsic öğeleri.](media/cxml-extrinsics-xml.png "XML'e eklenen extrinsic öğeler")

## <a name="create-and-process-a-purchase-order"></a><a name="create-po"></a>Satınalma siparişi oluşturma ve işleme

Bir satıcı için satınalma siparişi oluşturduğunuzda, bu satıcıdan alınan **cXML üzerinden satınalma siparişi gönder** seçeneğinin ayarını devralır. Ancak, ayar satınalma siparişinin **Üst bilgi** görünümündeki **Kurulum** hızlı sekmesinde kullanılabilir durumda kalır, böylece daha sonra gerektiği şekilde değişiklik yapabilirsiniz.

![cXML kullanmak için ayarlanan satınalma siparişi.](media/cxml-purchase-order.png "cXML kullanmak için ayarlanan satınalma siparişi")

Bir PunchOut akışından gelen satınalma talebi içinden bir satınalma siparişi oluşturduğunuzda, gerekli tüm satır ayrıntıları doldurulacaktır. Böylece, satınalma sipariş satırlarını el ile ekleyebilir veya diğer satınalma siparişlerinden kopyalayabilirsiniz. Gerekli tüm alanları ayarladığınızdan emin olun. Gerekli bu alanlar, cXML iletisinde kullanılacak satıcı numarası olan harici referans numarasını içerir.

![Harici referans numarası örneği.](media/cxml-line-details.png "Harici referans numarası örneği")

Satınalma siparişi için tüm ayrıntıları doldurmayı bitirdiğinizde, onayladığınızdan emin olun. Satınalma siparişi onaylanmadıkça hiçbir ileti gönderilmez. Eylem Bölmesi'nde, **Satınalma** sekmesinde, **Eylemler** grubunda, satınalma siparişini onaylamak için **Onayla**'yı seçin. 

Satınalma siparişi onaylandıktan sonra, **Satınalma siparişi onayları** günlükleri aracılığıyla onay durumunu görüntüleyebilirsiniz. Eylem Bölmesi'nde, **Satınalma** sekmesinde, **Günlükler** grubunda, **Satınalma siparişi onayları** ögesini seçin.

Her satınalma siparişinde birçok onay olabilir. Her onay, artan bir sayıyla işaretlenmiştir. Aşağıdaki çizimde, satınalma siparişi *00000275*, onay ise *00000275-1* ile işaretlenmiştir. Bu numaralandırma, bir satınalma siparişindeki değişikliklerin bulunduğu standart Supply Chain Management işlevini yansıtır ve bu nedenle satıcıya gönderilmesi gereken cXML iletisi türü onayı temel alarak tanımlanır. Çizimin gösterdiği gibi, **Satınalma siparişi onayları** sayfası **Sipariş gönderme durumu** ve **Sipariş isteği satıcı durumu** alanlarını da içerir. Bu sayfada görebileceğiniz çeşitli durum değerleri hakkında daha fazla bilgi için, bu makalenin ilerleyen kısımlarında [Satın alma siparişi taleplerini izleme](#monitor-po-requests) bölümüne bakın.

![Satınalma sipariş onayları sayfası.](media/cxml-po-confirmations.png "Satınalma sipariş onayları sayfası")

Belgeyle ilgili daha fazla bilgi görüntülemek için kılavuzun üzerindeki **Satınalma siparişi talebi** öğesini seçin.

**Satınalma siparişi talebi** sayfası iki kılavuz içerir. Sayfanın üst kısmındaki kılavuzda, gönderilmek üzere işaretlenmiş her satınalma siparişi için bir kayıt vardır. Sayfanın alt kısmındaki **Satınalma siparişi talep geçmişi** sekmesinde bulunan kılavuz, her bir onayın durumunu göstermek üzere seçili satınalma siparişi için birkaç kayda sahip olabilir. Aşağıdaki şekilde, üst kılavuzda 00000275 numaralı satınalma siparişi ile **Satınalma siparişi talep geçmişi** sekmesindeki kılavuzda 00000275-1 numaralı belge gösterilir.

![Satınalma sipariş talebi sayfası.](media/cxml-po-request.png "Satınalma sipariş talebi sayfası")

Toplu iş ayarlandıysa ve çalışıyorsa, belge gönderilir. Durum değişikliğini belge gönderildikten sonra görüntüleyebilirsiniz. Aşağıdaki çizimde, **Sipariş gönderme durumu** alanı _Gönderildi_ olarak ayarlanır. Satıcının belgeyi teslim aldığını ve bunu okuyup kendi sisteminde depolayabildiğini belirtmek için **Sipariş talebi satıcı durumu** alanı _Kabul edildi_ olarak ayarlanır. **Satınalma siparişi talebi geçmişi** sekmesindeki kılavuz belgenin gönderildiği saati gösterir. Bu sayfada görebileceğiniz çeşitli durum değerleri hakkında daha fazla bilgi için, [Satın alma siparişi taleplerini izleme](#monitor-po-requests) bölümüne bakın.

![Satınalma siparişi talebi sayfasındaki durum iletileri.](media/cxml-po-request-2.png "Satınalma siparişi talebi sayfasındaki durum iletileri")

## <a name="schedule-the-purchase-order-request-batch-job"></a><a name="po-batch"></a>Satınalma siparişi talebi toplu işini planlama

Satınalma siparişi talepleri göndermek üzere toplu işlemi etkinleştirmek için, **Satın alma ve kaynak hizmeti \> Kurulum \> cXML Yönetimi \> Satınalma siparişi talebi** sayfasına gidin ve sonra Eylem Bölmesi'nde, **Satınalma siparişi talebi** sekmesinde, **Toplu iş** grubunda, **Satınalma talebi hazırla ve gönder** iletişim kutusunu açmak için **İşi gönder**'i seçin. Bu iletişim kutusunu, genellikle Supply Chain Management uygulamasında toplu işlerde yaptığınız gibi, tekrarlama ayarlamak için kullanabilirsiniz. Sipariş biriminizi temel alarak bir aralık seçin. Toplu işi her dakika çalıştırabilirsiniz, ancak en iyi yöntem iş günü boyunca satıcılarınızla eşleşen sipariş giriş aralıkları temel alınarak toplu iş gönderimi yapmaktır.

Örneğin, satıcınız öğleden sonra 1'e kadar alınan tüm siparişlerin aynı gün içinde sevk edileceğini belirten bir ilkeye sahiptir. Bu durumda, siparişlerinizi iletmek için toplu işi, sabah yalnızca birkaç kez çalıştırmanız gerekebilir. Kalan siparişler sonraki gün gönderilecektir. Bu karar yalnızca bir iş kararıdır. Bunu gözden geçirebilir ve parametreleri uygun şekilde ayarlayabilirsiniz.

İşlem, *Bekliyor* durumundaki bir satınalma siparişi talebi belgelerini arayacaktır. Bir satıcıya hemen göndermeniz gereken bir siparişiniz varsa, **İşi gönder** ögesini seçebilir ve **Toplu işleme** seçeneğini *Hayır* olarak ayarlayabilirsiniz.

## <a name="monitor-purchase-order-requests"></a><a name="monitor-po-requests"></a>Satınalma siparişi taleplerini izleme

### <a name="view-the-status-of-a-purchase-order"></a>Satınalma siparişinin durumunu görüntüleme

cXML aracılığıyla gönderilebilecek siparişler onaylandıklarında, _Bekleme_ durumuna geçer. [Satınalma siparişi oluştur ve işle](#create-po) bölümünde belirtildiği gibi **Satınalma siparişi talebi** sayfasında satınalma sipariş durumunu görüntüleyebilirsiniz. Her satınalma siparişi talebi, parametrelerine ve verilerine bağlı olarak çeşitli durumlardan birini içerebilir. Bu bölümde, çeşitli durum türleri ve bunların sahip olacakları değerler açıklanmıştır. Bu bilgiler, sorunları yönetmenize ve satınalma siparişlerinizin durumunu anlamanıza yardımcı olabilir.

![Satınalma siparişi talebi sayfasındaki satınalma siparişi durumu iletileri.](media/cxml-monitor-po-request.png "Satınalma siparişi talebi sayfasındaki satınalma siparişi durumu iletileri")

**Satınalma siparişi talebi** sayfasının üst kısmındaki kılavuz, aşağıdaki durum değerlerini gösterebilir:

- **Sipariş gönderme durumu**: Bu alan aşağıdaki değerlerden birini içerebilir:

    - **Bekliyor**: Belge gönderilmek için bekliyor.
    - **Gönderildi**: Belge gönderildi.
    - **Durduruldu**: Belge gönderilmeden önce _Durduruldu_ olarak işaretlendi. (Belgeyi _Durduruldu_ olarak işaretlemek için, **Satınalma talebi** sayfasının Eylem Bölmesi'nde **Durdur** seçeneğini belirleyin.)
    - **Arşiv**: Belge temizlendi. (Belgeyi temizlemek için, **Satınalma talebi** sayfasının Eylem Bölmesi'nde **Temizle** seçeneğini belirleyin.)

- **Sipariş talebi satıcı durumu**: Bu alan aşağıdaki değerlerden birini içerebilir:

    - **Bekliyor**: Belge gönderilmek için bekliyor.
    - **Kabul edildi**: Belge satıcı tarafından alındığı şekilde onaylandı. Satıcının döndürdüğü ayrıntılı XML iletisini, sayfanın alt kısmındaki **Yanıt XML** sekmesini seçerek inceleyebilirsiniz.
    - **Hata**: Belge satıcıya gönderildi, ancak hata oluştu. Hata iletisini, sayfanın alt kısmındaki **Yanıt XML** sekmesini seçerek inceleyebilirsiniz.

**Satınalma siparişi talebi** sayfasının alt kısmındaki **Satınalma siparişi talebi geçmişi** sekmesinde yer alan kılavuz aşağıdaki değerleri gösterebilir:

- **Sipariş talebi türü**: Bu alan aşağıdaki değerlerden birini içerebilir:

    - **Yeni**: Satır, satınalma siparişi onaylandıktan hemen sonra yeni olarak işaretlenir.
    - **Güncelleştir**: Bir onay zaten satıcı tarafından gönderilip kabul edilirse, sonraki onay _Güncelleştir_ olarak işaretlenir. Güncelleştirmeler yalnızca, **Satınalma isteği güncelleştirmelerini gönder** seçeneği [Genel cXML parametreleri](#cxml-parameters) bölümünde *Evet* olarak ayarlandığında gönderilir.
    - **Sil**: Satıcı tarafından bir onay gönderilip kabul edildiğinde, ancak satınalma siparişi iptal edilirse, bekleyen onay _Sil_ olarak işaretlenir. Silme işlemleri yalnızca, **Satınalma talebi silme isteği gönder** seçeneği [Genel cXML parametreleri](#cxml-parameters) bölümünde *Evet* olarak ayarlandığında gönderilir.

- **Talep saati**: Sipariş onayının oluşturulduğu saat. Onay ile satıcı bildirimi arasındaki zamanı belirlemek için talep süresini sipariş durumu ile karşılaştırabilirsiniz.
- **Sipariş gönderme durumu**: Bu alan, sayfanın üst kısmındaki **Sipariş gönderme durumu** alanıyla aynıdır. Onaylama düzeyinde durumu daha kolay görüntülemek için burada tekrarlanabilir. **Sipariş talebi türü** alanı *Yeni* olarak ayarlanmışsa ve bir onay gönderilmeden satınalma siparişi yeniden onaylanırsa, **Sipariş gönderme durumu** alanı *Arşivle* olarak ayarlanır.
- **Sipariş durumu zamanı**: Satınalma sipariş talebi geçmişi kaydının en son güncelleştirildiği saat. (Güncellemeler durum değişikliklerini içerir.)
- **Sipariş talebi satıcı durumu**: Bu alan, sayfanın üst kısmındaki **Sipariş talebi satıcı durumu** alanıyla aynıdır. Onaylama düzeyinde durumu daha kolay görüntülemek için burada tekrarlanabilir.
- **Tekrar gönderme zamanı**: Kaydın yeniden gönderildiği saat.
- **Tekrar gönderme sayısı**: Kaydın yeniden gönderilmesi gereken sayı. Yüksek sayı birçok hata olduğunu gösterir ve bu nedenle veri kurulumunuz veya satıcınızın veri kurulumu ile ilişkili bir sorunu gösterebilir.

### <a name="view-the-xml-for-a-purchase-order-request-message"></a>Satınalma siparişi talebi iletisi için XML'yi görüntüleme

Satınalma siparişi talebi iletisi için XML'yi görüntülemek üzere, **Satınalma siparişi talebi** sayfasının alt kısmında **Talep XML metni** sekmesini seçin. Bu sekmedeki bilgiler test veya hata doğrulaması sırasında yararlı olabilir. Bilgilerin daha kolay okunmasını sağlamak için onu biçimlendirilmiş bir ileti olarak görüntüleyebilirsiniz. Sekmenin içeriğini bir metin dosyasına kopyalayın ve sonra bir XML düzenleyicisinde görüntüleyin.

![Talep XML metni sekmesi.](media/cxml-request-xml-text.png "Talep XML metni sekmesi")

### <a name="view-the-details-of-the-vendor-response"></a>Satıcı yanıtlarının detaylarını görüntüleme

Satıcı onay veya hata yanıtının içeriğini görüntülemek için, **Satınalma siparişi talebi** sayfasının altındaki **Yanıt XML** sekmesini seçin.

![Yanıt XML'si sekmesi.](media/cxml-response-xml.png "Yanıt XML'si sekmesi")

## <a name="additional-resources"></a>Ek kaynaklar

- [PunchOut e-tedariki için harici katalog ayarlama](set-up-external-catalog-for-punchout.md)
- [PunchOut e-procurement için harici katalogları kullanma](use-external-catalogs-for-punchout.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
