---
title: Perakende hareketi tutarlılık denetleyicisi
description: Bu konuda, Dynamics 365 Commerce'te bulunan hareket tutarlılık denetleyicisi açıklanmaktadır.
author: josaw1
ms.date: 10/07/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 38386087a74a0881867df89bbe26453dff740be3
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350316"
---
# <a name="retail-transaction-consistency-checker"></a>Perakende hareketi tutarlılık denetleyicisi

[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'ta bulunan hareket tutarlılık denetleyicisi açıklanmaktadır. Tutarlılık denetleyicisi, tutarsız hareketleri ekstre deftere nakil işlemi tarafından alınmadan önce tanımlar ve ayırır.

Bir ekstre deftere nakledildiğinde deftere nakil işlemi, ticari hareket tablolarında tutarsız verilerin bulunması nedeniyle başarısız olabilir. Veri sorunu, satış noktası (POS) uygulamasında öngörülemeyen aksaklıklardan veya hareketlerin üçüncü taraf POS sistemleri tarafından yanlış aktarılmasından kaynaklanabilir. Bu tutarsızlıkların nasıl görünebileceğine ilişkin örnekler şunlardır: 

- Üstbilgi tablosundaki işlem toplamı, satırlardaki işlem toplamıyla eşleşmiyordur.
- Üstbilgi tablosundaki satır sayısı, işlem tablosundaki satır sayısıyla eşleşmiyordur.
- Üstbilgi tablosundaki vergiler, satırlardaki vergi tutarıyla eşleşmiyordur. 

Ekstre deftere nakil işlemi tarafından tutarsız işlemler seçildiğinde tutarsız satış faturaları ve ödeme günlükleri oluşturulur ve bunun sonucunda tüm ekstre deftere nakil işlemi başarısız olur. Ekstrelerin bu durumdan kurtarılması, birden fazla işlem tablosu arasında karmaşık veri düzeltmelerini içerir. Hareket tutarlılık denetleyicisi bu tür sorunları önler.

Aşağıdaki çizelgede, işlem tutarlılık denetleyicisi ile gerçekleştirilen deftere nakil işlemi gösterilmektedir.

![Hareket tutarlılık denetleyicisi ile gerçekleştirilen ekstre deftere nakil işlemi.](./media/validchecker.png "Perakende hareketi tutarlılık denetleyicisi ile gerçekleştirilen deftere nakil işlemi")

**Mağaza hareketlerini doğrula** toplu işlemi, aşağıdaki senaryolar için ticari hareket tablolarının tutarlılığını denetler.

- **Müşteri hesabı**: Hareket tablolarındaki müşteri hesabının Genel Merkez müşteri yöneticisinde de bulunduğunu doğrular.
- **Satır sayısı**: Hareket başlığı tablosundan alındığı şekilde satır sayısının satış hareket tablolarındaki satır sayısıyla eşleştiğini doğrular.
- **Fiyata vergi dahildir**: **Fiyata vergi dahildir** parametresinin hareket satırları arasında tutarlı olduğunu ve satış satırındaki fiyatın vergi dahil fiyat ve vergi muafiyeti yapılandırmasına uygun olduğunu doğrular.
- **Ödeme tutarı**: Genel Muhasebedeki kuruş yuvarlama yapılandırmasını da dikkate alarak ödeme kayıtlarının üst bilgideki ödeme tutarıyla eşleştiğini doğrular.
- **Brüt tutar**: Genel Muhasebedeki kuruş yuvarlama yapılandırmasını da dikkate alarak üst bilgideki brüt tutarın, satırdaki net tutarların toplamına vergi tutarının eklenmesiyle elde edilen toplam olduğunu doğrular.
- **Net tutar**: Genel Muhasebedeki kuruş yuvarlama yapılandırmasını da dikkate alarak üst bilgideki net tutarın, satırdaki net tutarların toplamına vergi tutarının eklenmesiyle elde edilen toplam olduğunu doğrular.
- **Eksik/Fazla ödeme**: Genel Muhasebedeki kuruş yuvarlama yapılandırmasını da dikkate alarak üst bilgideki brüt tutar ile ödeme tutarı arasındaki farkın maksimum eksik ödeme/fazla ödeme yapılandırmasını aşmadığını doğrular.
- **İskonto tutarı**: Genel Muhasebedeki kuruş yuvarlama yapılandırmasını da dikkate alarak iskonto tablolarındaki iskonto tutarının ve hareket satırı tablolarındaki iskonto tutarının tutarlı olduğunu ve başlıktaki iskonto tutarının satırlardaki iskonto tutarlarının toplamı olduğunu doğrular.
- **Satır iskontosu**: Hareket satırındaki satır iskontosunun, iskonto tablosunda hareket satırına karşılık gelen tüm satırların toplamı olduğunu doğrular.
- **Hediye kartı maddesi**: Commerce, hediye kartı maddelerinin iadesini desteklemez. Ancak bir hediye kartının bakiyesi nakde çevrilebilir. Nakde çevirme satırı yerine iade satırı olarak işlenen bir hediye kartı maddesi için ekstre deftere nakil işlemi başarısız olur. Hediye kartı maddeleri için doğrulama işlemi, hareket tablolarındaki yalnızca hediye kartı satır maddelerinin hediye kartı nakde çevirme satırları olmasını sağlamaya yardımcı olur.
- **Negatif fiyat**: Negatif fiyat hareketi satırı olmadığını doğrular.
- **Madde ve Ürün Çeşidi**: Hareket satırlarındaki maddelerin ve ürün çeşitlerinin madde ve ürün çeşidi ana dosyasında bulunduğunu doğrular.
- **Vergi tutarı**: Vergi kayıtlarının satırlardaki vergi tutarlarıyla eşleştiğini doğrular.
- **Seri numarası**: Seri numarasıyla kontrol edilen maddelere ait hareket satırlarında seri numarasının bulunduğunu doğrular.
- **İşaret**: Miktar ve net tutardaki işaretin tüm hareket satırlarında aynı olduğunu doğrular.
- **İş tarihi**: Hareketlere ilişkin tüm iş tarihleri için mali dönemlerin açık olduğunu doğrular.
- **Masraflar**: Üst bilgi ve satır masrafı tutarının vergi ve vergi muafiyeti yapılandırması dahil olacak şekilde fiyata uygun olduğunu doğrular.

## <a name="set-up-the-consistency-checker"></a>Tutarlılık denetleyicisini ayarlama

**Retail ve Commerce \> Retail ve Commerce BT \> POS deftere nakli** altından "Mağaza hareketlerini doğrula" toplu işini periyodik olarak çalışmak üzere yapılandırın. Toplu iş, "Ekstreleri toplu işle hesapla" ve "Ekstreleri toplu işle deftere naklet" işlemlerinin ayarlanmasına benzer şekilde, mağaza organizasyon hiyerarşisine göre zamanlanabilir. Bu toplu işlemi günde birden fazla kez yürütülecek şekilde yapılandırmanızı ve her P işi uygulamasının sonunda çalıştırılacak şekilde zamanlamanızı öneririz.

## <a name="results-of-validation-process"></a>Doğrulama işleminin sonuçları

Toplu iş olarak gerçekleştirilen doğrulama denetiminin sonuçları, uygun harekette işaretlenir. Hareket kaydındaki **Doğrulama durumu** alanı **Başarılı** veya **Hata** olarak ayarlanabilir ve son doğrulama çalıştırma tarihi, **Son doğrulama saati** alanında görünür.

Doğrulama hatası ile ilgili daha fazla hata açıklaması görmek için ilgili mağaza işlem kaydını seçip **Doğrulama hataları** düğmesine tıklayın.

Doğrulama denetlemesinden geçemeyen işlemler ve henüz doğrulanmamış olan işlemler ekstrelere eklenmez. "Ekstre hesaplama" işlemi sırasında ekstreye eklenebilecek, ancak eklenmemiş olan işlemlerin olması durumunda kullanıcılar bilgilendirilir.

Bir doğrulama hatası bulunursa hatayı düzeltmenin tek yolu, Microsoft Desteği ile iletişime geçmektir. Bir sonraki sürümde kullanıcıların kullanıcı arabiriminde başarısız olan kayıtları düzeltmelerine olanak tanıyan özellik eklenecektir. Değişiklik geçmişini takip etmek için günlüğe kaydetme ve denetleme özellikleri de kullanıma sunulacaktır.

> [!NOTE]
> Bir sonraki sürümde daha fazla senaryoyu desteklemek için ek doğrulama kuralları da eklenecektir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]