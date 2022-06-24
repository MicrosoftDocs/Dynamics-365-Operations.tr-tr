---
title: Çağrı merkezi sahtekarlık uyarılarını ayarlama ve bu uyarılarla çalışma
description: Bu makale, siparişler işlendiğinde, müşteri hizmetleri temsilcilerini sahte olması olası bilgilere karşı uyarmak için kuralların nasıl ayarlanacağını açıklar. Siparişleri otomatik olarak veya el ile beklemeye almak için kullanılan belirli kodlar tanımlayabilirsiniz.
author: josaw1
ms.date: 05/14/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesPostingHistory, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 212afd594453d3594fdaef9442a7809e4cafbd07
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885360"
---
# <a name="set-up-and-work-with-call-center-fraud-alerts"></a>Çağrı merkezi sahtekarlık uyarılarını ayarlama ve bu uyarılarla çalışma

[!include [banner](includes/banner.md)]

Bu makalede, potansiyel sahte satış siparişlerini daha fazla incelemek üzere beklemeye almak için nasıl ölçütler ve kurallar ayarlayacağınız açıklanmaktadır. Sahte veri denetimi özelliği, bir satış siparişindeki bilgilerin geçerliliğini belirlemek için kullanılır. Satış siparişindeki bilgiler kuruluşun sahtekarlık ölçütlerine ve kurallarına göre şüpheli görünüyorsa, sipariş incelenmek üzere beklemeye alınabilir. Bu durumda, sipariş, bekleme kaldırılana kadar, işlemlerine devam edilmesi için ambara serbest bırakılamaz.

> [!NOTE]
> Bu özellik yalnızca Commerce çağrı merkezi kanalı için satış siparişi işlemiyle birlikte kullanılabilir.

## <a name="turning-on-the-fraud-check-feature"></a>Sahte veri denetimi özelliğini etkinleştirme

Sahte veri denetimi özelliğini kullanmak için, çağrı merkezi kanalı [tanımlanırken](/dynamics365/unified-operations/retail/set-up-order-processing-options) kanaldaki **Sipariş tamamlamayı etkinleştir** seçeneğini **Evet** yapmanız gerekir. Sipariş tamamlama etkin durumdayken, çağrı merkezi kullanıcıları, oluşturulan tüm satış siparişleri için satış siparişi sayfasında **Tamamla**'yı seçmelidir. Tamamlama eylemi, **Satış siparişi özeti** sayfasının açılmasına neden olur. Kullanıcılar gerekli ödeme verilerini **Satış siparişi özeti** sayfasına girdikten sonra **Gönder**'i seçerek siparişi tamamlarlar. Sipariş gönderilince sahte veri denetimi özelliği tetiklenir ve sistemdeki etkin kuralların tümü otomatik olarak doğrulanır.

Çağrı merkezi kullanıcıları **Gönder**'i seçmeden önce satış siparişlerini sahtekarlık incelemesi için el ile de beklemeye alabilirler. Satış siparişini el ile beklemeye almak için, **Satış siparişi özeti** sayfasında **Durduruldu**\> **El ile sahte tutma**'yı seçin. Bunun ardından, siparişi beklemeye alma nedeninizi açıklayan bir yorum girmeniz istenir. Bu yorum [sipariş tutmalar](/dynamics365/unified-operations/retail/work-with-order-holds) workbench'inde görünerek, siparişin serbest bırakılıp bırakılmayacağını belirlemek üzere beklemedeki siparişleri inceleyen kullanıcıya bilgi verir.

Kanalda **Sipariş tamamlamayı etkinleştir** seçeneğini yapılandırmaya ek olarak, Çağrı merkezi parametrelerinde sahte veri denetimi özelliğini yapılandırmanız gerekir. **Retail ve Commerce** \> **Kanal kurulumu** \> **Çağrı merkezi kurulumu** \> **Çağrı merkezi parametreleri**'ne gidin. **Çağrı merkezi parametreleri** sayfasındaki **Beklemeye alınanlar** sekmesinde **Sahte veri denetimi** seçeneğini **Evet** yapın.

**Beklemeye alınanlar** sekmesinde, sahte veri incelemesi için beklemeye el ile veya otomatik olarak alınan siparişe uygulanacak [tutma kodlarını](/dynamics365/unified-operations/retail/work-with-order-holds) da tanımlamanız gerekir. **El ile sahte tutma kodu** ve **Sahte tutma kodu** alanlarında tutma kodlarını ayarlayın. Beklemeye alınanlar workbench'inde çalışan kullanıcıların kolaylıkla filtre uygulayarak otomatik tutmaları el ile tutmalardan ayırt edebilmelerini sağlamak için iki benzersiz tutma kodu oluşturmayı yararlı bulabilirsiniz.

Sahte veri denetimi özelliğinin etkin bir şekilde çalışması için **Minimum puan** alanını da ayarlamanız gerekir. Sistemde tanımlı her sahtekarlık ölçütünün ve kuralının birer puanı vardır. Bir satış siparişi sahte veri eşleme denetimine girince bir veya daha fazla eşleşme bulunduğu takdirde puanlar toplanarak toplam sahte veri puanını verir. Bir siparişin toplam sahte veri puanı **Minimum puan** alanındaki değeri aşarsa, sipariş otomatik olarak bekleme durumuna alınır. İsterseniz, **Beklemeye alınanlar** sekmesinde puanla ilgili diğer alanları kullanarak, e-posta puanı, telefon puanı, posta kod puanı ve genişletilmiş posta kodu puanı tanımlayabilirsiniz. **Statik sahte veri** sayfasında tanımladığınız statik sahtekarlık ölçütlerinden herhangi biri için, tanımlama sırasında puan belirtmezseniz, sistem, **Çağrı merkezi parametreleri** sayfasının **Beklemeye alınanlar** sekmesinde belirttiğiniz varsayılan puanları kullanarak bunlara puan verecektir.

Son olarak, kullanıcılar bir siparişi sahte veri incelemesi amacıyla el ile beklemeye aldıklarında yorum girerken kullanılması gereken belge türünü belirtmek için **Sahte yorum türü** alanını kullanın. Çoğu zaman bu alan ayarı **Not** yapılır.

## <a name="defining-fraud-criteria-and-rules"></a>Sahtekarlık ölçütlerini ve kurallarını tanımlama

Sistem, bir siparişin sahte veri incelemesi amacıyla beklemeye alınması gerekip gerekmediğini belirlemek için iki tür sahtekarlık ölçütüne başvurur.

- **Statik sahte veri**, engellenmiş numaralar listesine koyulmuş bir telefon numarası veya daha önce sahte işlemlerde kullanıldığı bilindiği için işaretlenmiş e-posta adresi gibi özel bir değer kullanır. Statik sahte verilerin ayarını yapmak için **Retail ve Commerce** \> **Kanal kurulumu** \> **Çağrı merkezi ayarı** \> **Sahte** \> **Statik sahte veri**'ye gidin. **Statik sahte veri** sayfasında, sahtekarlık ölçütlerini el ile veya verileri içe aktararak ekleyebilirsiniz. Puanlar sahtekarlık bilgilerine eklenir. Sahte veri denetimi özelliği etkinse, girilen her satış siparişi, statik verilerle karşılaştırılır. Veriler müşterinin sipariş üst bilgisine bağlı faturalama adresinde veya teslimat adresinde bulunamazsa ya da satış siparişindeki satırlardan herhangi biriyle bağlantılı teslimat adresinde bulunursa, tüm benzersiz eşleşmelerin puanları toplanır ve siparişin beklemeye alınıp alınmayacağını belirlemek için **Minimum puan** değeriyle karşılaştırılır.

- **Sahtekarlık kuralları** kullanıcı tanımlı değişkenlerden ve bu değişkenler için tanımlanmış koşullardan oluşur. Kuralları oluşturmak için **Retail ve Commerce** \> **Kanal kurulumu** \> **Çağrı merkezi ayarı** \> **Sahte** \> **Kurallar**'a gidin. Sahtekarlık kuralları, bir şirketin, birden fazla koşulu değerlendirmek için **VE** ya da **VEYA** deyimlerini içerebilen daha karmaşık kural kümesi yapılandırabilmesine olanak sağlar. Örneğin, bir kullanıcı belirli bir müşteri grubuna dahil olan ve belirli bir ürün sipariş etmiş müşterilere ilişkin tüm siparişleri sahte veri incelemesi amacıyla beklemeye almak istiyor. Bu durumda, müşteriyi ve ürünleri doğrulayacak koşullar **Kurallar** sayfasında bir VE koşulu kullanılarak tanımlanır. Bunun ardından, ancak her iki koşul doğru olduğu ve bu kurala atanan puan değeriyle, varsa, siparişin eşleştiği diğer kuralların puan değerlerinin toplamı, siparişin toplam sahtekarlık puanının **Çağrı merkezi parametreleri** sayfasındaki **Minimum puan** değerini aşmasına neden olduğu takdirde sipariş beklemeye alınır.

> [!NOTE]
> Çok sayıda kural veya fazla karmaşık kurallar, satış siparişleri gönderilirken sistem performansını olumsuz etkiler. Sahte veri denetimi özelliği, büyük hacimli statik sahtekarlık verilerini ve çok fazla etkin kuralı işleyecek şekilde optimize edilmemiştir. Çağrı merkezi kullanıcıları satış siparişi girişi sırasında **Gönder**'i seçtiği zaman her kuralın değerlendirileceğini unutmayın. Kurallar satış siparişi başlıklarında ve tüm sipariş satırlarında değerlendirilir. Ne kadar çok kural olursa o kadar karmaşık kural deyimi olacak ve dolayısıyla işlem o kadar uzun sürecektir. Siparişte çok sayıda satır maddesi ve çok sayıda etkin kural ile statik veri girişi varsa, tüm verilerin otomatik olarak incelenip doğrulanması ve sahtekarlık puanının hesaplanması performansa ciddi şekilde olumsuz etkide bulunabilir. Bu özelliği kullanan kuruluşların, kurallarda veya statik sahtekarlık ölçütünde değişiklik yapmadan önce daima sipariş gönderme işlemi süresinin kabul edilebilir olduğunu üretim ortamında test etmesi ve onaylaması gerekir.

## <a name="identifying-orders-that-are-on-hold-for-fraud-review"></a>Sahte veri incelemesi için beklemeye alınmış siparişleri belirleme

Çağrı merkezi kullanıcıları bir satış siparişi gönderirken sipariş sahtekarlık ölçütleriyle veya kurallarıyla eşleşirse ve puan minimum değeri aşarsa, kullanıcılar, siparişin beklemeye alındığını bildiren bir uyarı iletisi alır. Kullanıcılar, yalnızca bilgi amaçlı olduğundan, bu iletiyi kapatabilir. Kullanıcılar isteğe bağlı olarak bu bilgileri müşteriye iletebilir. İşletme, bu durumda kullanıcıların izleyeceği protokolü belirlemelidir.

Sipariş kaydedilir ancak üzerine **İşleme** bayrağı koyulur. Bu bayrak, siparişin ambara serbest bırakılmamasını garantilemeye yardımcı olur. Kullanıcılar istedikleri zaman bir satış siparişinin **İşleme** bayrağı ayarını **Ayrntılı durum** sayfasında görüntüleyebilirler. Bu sayfa **Tüm satış siparişi** ve **Müşteri hizmeti** sayfalarından açılabilir. Sistem, ayrıca, siparişin **Ayrıntılı durum** alanının değerini **Sahte tutma**'ya güncelleştirebilir.

Sahte veri incelemesi için beklemeye alınmış siparişleri görüntülemek ve yönetmek için **Retail ve Commerce** \> **Müşteriler** \> **Sipariş tutmalar**'a gidin. Tutma nedeni hakkında bilgiler içeren daha ayrıntılı bir görünümü görmek için **Sipariş tutmalar** sayfasında, listeden bir giriş seçin ve ardından **Sipariş tutma**'ya tıklayın. **Sahtekarlık ayrıntıları** hızlı sekmesinde, sipariş için bir eşleşme olduğu saptanan sistematik sahtekarlık ölçütlerini ve uygulanan puanları görüntüleyebilirsiniz. Sipariş el ile tutulursa, siparişi beklemeye alan kullanıcının girdiği yorumları, **Notlar** hızlı sekmesindeki **Sahtecilik notları** bölümüne bakarak inceleyebilirsiniz.

Tutma emirleriyle nasıl çalışılacağı hakkında daha fazla bilgi için bkz. [Sipariş tutmalar](/dynamics365/unified-operations/retail/work-with-order-holds).


[!INCLUDE[footer-include](../includes/footer-banner.md)]