---
title: Barkod maskesi ayarlama
description: Bu konu, barkod maskesi karakterlerini, barkod maskelerini ve barkod maskelerinin barkodlara nasıl atanacağını açıklamaktadır.
author: BrianShook
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 265994
ms.assetid: 5831c74d-d2a1-4fa5-9a9a-a5aba8848381
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: ddba3ef6c6a1fb1f71198291d5eccd44be737336
ms.sourcegitcommit: f4823a97c856e9a9b4ae14116a43c87f9482dd90
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/09/2021
ms.locfileid: "7779834"
---
# <a name="set-up-bar-code-masks"></a>Barkod maskesi ayarlama

[!include [banner](includes/banner.md)]

Bu konu, barkod maskesi karakterlerini, barkod maskelerini ve barkod maskelerinin barkodlara nasıl atanacağını açıklamaktadır.

## <a name="set-up-bar-code-mask-characters"></a>Barkod maskesi karakterlerini ayarlama

Barkod maskeleri, barkod oluşturmak ve satış noktasına (POS) taranan barkodları hızla tanımlamak için kullanılır. Maskeler, oluşturulacak barkodların biçimini belirten yer tutucuları gibi davranan karakterlerden oluşur. Bir barkod maskesi yapılandırmak için, barkod maskesi karakterleri oluşturmanız gerekir. **Perakende ve Ticaret** &gt; **Stok yönetimi** &gt; **Barkodlar ve etiketler** &gt; **Maske karakterleri**'ne gidin. Barkod maskesi karakterleri oluşturmak için **Yeni**'ye tıklayın. Maske karakterleri aşağıdaki barkod verilerini göstermek için oluşturulabilir.

| Alan            | Açıklama |
|------------------|-------------|
| Ürün          | Ürün kodu için yer tutucu. |
| Herhangi bir sayı       | Barkodlarda sabit kodlanacak bir numarayı belirtmek için kullanılır. |
| Denetleme basamağı      | Bir barkod maskesindeki barkod biçiminin, barkodun geçerliliğini onaylamak için bir denetim basamağı kullandığını belirtir. |
| Boyut basamağı       | Boyutu içeren bir ürün çeşidi için oluşturulan bir barkoddaki boyutu gösterir. |
| Renk basamağı      | Renk içeren bir ürün çeşidi için oluşturulan bir barkoddaki rengi gösterir. |
| Stil basamağı      | Stil içeren bir ürün çeşidi için oluşturulan bir barkoddaki stili gösterir. |
| EAN lisans kodu | EAN lisans kodları için verilen EAN lisansın yer tutucusu. |
| Fiyat            | Fiyat katıştırılmış barkodları için fiyatı belirtir. |
| Miktar         | Miktar/rastgele ağırlık katıştırılmış barkodlardaki miktarı belirtir. |
| Personel         | Barkod POS oturum açma işlemi için kullanılan çalışan kimlik numarasının barkod bölümünü belirtir. |
| Müşteri         | Müşteri kimliği segmentini gösterir. |
| Veri girişi       | *Henüz uygulanmadı.* |
| İskonto kodu    | Dynamics 365 for Retail İlkbahar 2017 sürümünden itibaren *Kaldırıldı*. Önceden: Bir satış noktası hareketine iskonto eklemek için kullanılan barkodun indirim kodunu belirtir. |
| Kupon kodu      | Bir siparişe iskonto eklemek için kullanılan barkoda ilişkin kupon kodunu belirtir. İskonto kodunun yerine geçti. |
| Hediye kartı        | Hediye kartı verirken veya ödeme yaparken bir hediye kartı numarası belirtir. |
| Bağlılık programı kartı     | Harekete bir bağlılık programı müşterisi ekler ve bağlılık programıyla ödeme yapılırken kullanılabilir. |

## <a name="define-bar-code-masks"></a>Barkod maskelerini tanımlama

Gerekli barkod maskeleri için barkod maskesi karakterleri belirtildikten sonra **Perakende ve Ticaret** &gt; **Stok yönetimi** &gt; **Barkodlar ve etiketler** &gt; **Barkod maskesi ayarı**'na gidin. Bu sayfada, daha önce belirtilen karakterleri kullanan barkod maskeleri tanımlayabilirsiniz. Bu barkod maskeleri, barkod oluşturulurken kullanılır ve POS'ta taranan barkodları tanımaya da yardımcı olur.

1. Yeni bir barkod maskesi oluşturmak için **Yeni**'ye tıklayın.
2. **Maske kodu** ve **Açıklama** alanlarına değerleri girin ve **Tür** alanında bir barkod maskesi türü seçin.
3. **Genel** bölümünde, **Barkod standardı** alanındaki bir değeri seçin ve gerekliyse barkod önekini belirtin.
4. **Barkod maske segmenti** bölümünde, oluşturulacak barkodda kullanılacak olan barkod segmentlerini ekleyin.

Örnek olarak, maske kodu "Ürün" olan bir barkod maskesi oluşturmak için aşağıdakileri yaparsınız:

1. Yeni bir barkod maskesi oluşturun ve tür olarak 'Ürün'ü seçin.
2. Bir barkod standardı seçin (örneğin "Kod 39").
3. Barkodu kolayca tanımak için kullanılacak bir önek belirtin. Örneğin, '22'.
4. Bir maske segmenti ekleyin. 'Ürün' maske segmenti seçilecektir.
5. Ürün segmenti için bir uzunluk belirtin (örneğin '10'). Uzunluk, mağazada genel olarak kullanılan bir ürün kodunun uzunluğuyla eşleşmelidir. Maske **Maske** altındaki **Genel** bölümünde bir önizleme olarak görüntülenir.

## <a name="assign-bar-code-masks-to-bar-codes"></a>Barkod maskelerini barkodlara atama

Barkodların kullanılabilmesi için önce barkod maskelerinin barkodlara atanması gerekir. Önceki örnekten devam edersek, bir barkoda barkod maskesi atamak için aşağıdakileri yapın:

1. **Kuruluş yönetimi** &gt; **Kurulum** &gt; **Barkodlar**'a gidin. Yeni bir barkod oluşturmak için **Yeni**'ye tıklayın.
2. **Barkod** **ayarı** ve **Kurulum** alanına değerleri girin.
3. **Genel** bölümündeki **Barkod türü** alanında 'Kod 39'u seçin. **Maske** **kodu** alanında, daha önce oluşturulmuş olan 'Ürün' maskesini seçin.
4. **Boyut** altında '12' girin.
5. **Kaydet**'e tıklayın.

Barkod maskesi şimdi ürünlere ilişkin barkodlar oluşturmak için kullanılabilir. Yukarıdaki adımlar, ürünler için barkod maskeleri oluşturma örneğidir, ancak, desteklenen diğer barkod türleri için barkod maskeleri oluşturma işlemini de gösterir. Barkod maskeleri, türleri ve uzunlukları özel ortamınızda kullanmak için ayarlanmalıdır.


[!INCLUDE[footer-include](../includes/footer-banner.md)]