---
title: Kredi yönetimi kurulumu
description: Bu konuda, Kredi yönetimi için gereken kurulum açıklanmaktadır.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 65b1d1a232558efbe05e83d51706a78b12439e47
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124151"
---
# <a name="credit-management-setup"></a>Kredi yönetimi kurulumu 

[!include [banner](../includes/banner.md)]

## <a name="credit-management-workflows"></a>Alacak yönetimi iş akışları

Kredi limiti düzeltmelerini yönetmede kullanılan iş akışlarını tanımlamak için **Alacak ve tahsilatlar \> Kurulum \> Kredi yönetimi iş akışları**'na gidin.

- Tek bir onayla bir kredi limiti düzeltmeleri grubunu onaylamanızı sağlayan bir iş akışı oluşturabilirsiniz.
- Kredi limiti düzeltmelerinin ayrı ayrı onaylanabilmesi için, satır düzeyinde bir iş akışı ekleyebilirsiniz.
- Bekletmeleri bir iş akışı sürecine otomatik olarak yönlendiren bir serbest bırakma iş akışı oluşturabilirsiniz.

## <a name="blocking-rules"></a>Durdurma kuralları

### <a name="ranking-payment-terms"></a>Ödeme koşullarını derecelendirme

Siparişteki ödeme koşulları müşterinin varsayılan ödeme koşullarıyla eşleşmiyorsa bir satış siparişini beklemeye alabilirsiniz. Ancak bazen ödeme koşulları arasında farklılık olsa da siparişi beklemeye almak istemeyeceğiniz kadar benzerdir. Ödeme koşullarını, bazılarının aynı, bazılarının da daha yüksek veya düşük bir derecede olacağı şekilde derecelendirebilirsiniz.

Ödeme koşullarının derecelendirmeleri etkinse, siparişteki ödeme koşullarının müşteri için varsayılan ödeme koşullarına göre daha yüksek bir derecede olması durumunda, satış siparişleri beklemeye alınır.

### <a name="ranking-settlement-discounts"></a>Kapatma iskontolarını derecelendirme

Siparişteki nakit iskontosu müşterinin varsayılan nakit iskontosuyla eşleşmiyorsa bir satış siparişini beklemeye alabilirsiniz. Ancak bazen nakit iskontoları farklı olsa da siparişi beklemeye almak istemeyeceğiniz kadar benzerdir. Nakit iskontolarını, bazılarının aynı, bazılarının da daha yüksek veya düşük bir derecede olacağı şekilde derecelendirebilirsiniz.

Kapatma iskontolarının derecelendirmeleri etkinse, siparişteki nakit iskontusunun müşteri için varsayılan nakit iskontosuna göre daha yüksek bir derecede olması durumunda, satış siparişleri beklemeye alınır.

## <a name="reasons"></a>Nedenler

Kredi yönetiminde çeşitli neden türleri kullanılır:

- Bekletme nedenleri bir satış siparişinin beklemeye neden koyulacağını gösterir.
- Bir sipariş bekletmeden serbest bırakılırken, o siparişe serbest bırakma nedenleri atanır.
- Durum nedenleri, müşteriye bir hesap durumunun neden atandığını gösterir.

**Kredi yönetimi nedenleri** sayfasında (**Kredi yönetimi \> Kurulum \> Kredi yönetimi \> Kredi yönetimi nedenleri**) nedenleri ayarlayabilirsiniz.

1. **Neden türü** alanında nedenin türünü seçin: **Tutuldu**, **Serbest bırak**veya **Durum**.
2. **Neden** alanına neden için bir ad girin.
3. **Açıklama** alanına neden kodu için bir açıklama girin.

## <a name="credit-management-groups"></a>Alacak yönetimi grupları

Kredi yönetimi grupları, aynı kredi yönetimi özelliklerini taşıyan müşterileri veya müşteri gruplarını belirlemek için kullanılır. Örneğin, müşterilerin durdurma ve hariç tutma kredi yönetimi kurallarını belirlemek için kredi yönetimi grupları kullanılabilir.

**Kredi yönetimi grupları** sayfasında (**Kredi yönetimi \> Kurulum > Gruplar kurulumu \> Kredi yönetimi grupları**) kredi yönetimi grupları oluşturabilirsiniz.

1. Bir satır oluşturmak için **Yeni**'yi seçin.
2. Grup için bir kimlik girin. Kimlik en fazla 10 karakter olabilir.
3. **Açıklama** alanına grup için bir ad girin. Ad en fazla 60 karakter olabilir.

Kredi yönetimi grubu, **Tüm müşteriler** sayfasının (**Alacak hesabı \> Müşteriler \> Tüm müşteriler**) **Alacak ve tahsilatlar** hızlı sekmesinde bir müşteriye atanır.

## <a name="account-statuses"></a>Hesap durumları

Müşteri hesabının kredi beklemesini belirlemek için hesap durumları oluşturabilirsiniz. Bir durum ve o durumun faturalama ve teslim bekletme işlemlerine etkilerini tanımlayabilirsiniz. Hesap durumları, bir müşteriyle ilgili durdurma kurallarını belirlemek için de kullanılabilir.

Hesap durumlarını **Hesap durumları** sayfasında (**Kredi yönetimi \> Kurulum > Gruplar kurulumu \> Hesap durumları**) oluşturabilirsiniz.

1. Bir hesap durumu ekleyin ve müşterinin kredi bekletme durumunu temsil eden bir açıklama girin. Örneğin, bir müşterinin iyi durumda olduğunu ve açık siparişlerin standart kredi yönetimi işlemine tabi olduğunu göstermek için **Normal**'i kullanın.
2. **Faturalama** ve **Beklemedeki Teslimat** alanlarında, bu hesap durumundaki müşteriler için gerçekleşecek bekletme türünü seçin. Kredi limiti kuralları uygulandığında, tüm işlemleri veya yalnızca fatura işlemeyi beklemeye alabilir ya da hiçbir işleme bekletme uygulamayabilirsiniz.

## <a name="scoring-groups"></a>Puanlama grupları

Risk faktörleri ve risk faktörlerini ölçmek için kullanılacak ölçütleri tanımlamak için Puanlama grupları ayarlayabilirsiniz. Bir müşteri hakkındaki bilgiler bir puanlama grubuna uygulandığı zaman, her risk faktörü için bir puan hesaplanır ve müşteriyi bir risk grubuna koymak için kullanılır. Risk grubu, kredi tutarını belirlemek ve otomatik kredi limitlerini hesaplamak için kullanılabilir.

Puanlama gruplarını **Puanlama grupları** sayfasında (**Kredi yönetimi \> Kurulum \> Risk kurulumu \> Puanlama grupları**) oluşturabilirsiniz.

1. Bir puanlama grubu oluşturun ve grup için bir ad girin.
2. Puanlama grubunu daha ayrıntılı açıklamak için bir açıklama girin.
3. Bir grup türü seçin. Önceden tanımlanmış sekiz tür vardır. **Kullanıcı tanımlı**'yı seçerek, kuruluşunuza daha uygun bir grup türü de tanımlayabilirsiniz.
4. Puanlama grubunun, risk puanını nasıl hesaplayacağını tanımlamak için bir puan türü seçin. Aşağıdaki seçenekler bulunur:

    - **Aralık** – Bir puanı hesaplamada kullanılacak bir değer aralığı tanımlamak için bu seçeneği kullanın.
    - **Kullanıcı tanımlı** – Puan için kullanılacak bir değer listesini el ile tanımlamak için bu seçeneği kullanın.

5. Puan türü olarak **Aralık**'ı seçtiyseniz, değer aralığını ve karşılık gelen puanları tanımlamak için satırlar ekleyin.

    1. **Başlangıç değeri** alanında, aralıktaki en düşük değeri belirtin.
    2. **Bitiş değeri** alanında, aralıktaki en yüksek değeri belirtin.
    3. **Puan** alanında, girilen değer "başlangıç"/"bitiş" aralığı içinde olduğu zaman atanması gereken puanı girin.

    Puan türü olarak **Kullanıcı tanımlı**'yı seçtiyseniz, kullanıcı tanımlı değerleri ve bunlara karşılık gelen puanları tanımlamak için satırlar ekleyin.

    1. **Değer** alanına, müşteri bilgilerinden alınacak kullanıcı tanımlı değeri girin.
    2. **Puan** alanında, girilen değer "başlangıç"/"bitiş" aralığı içinde olduğu zaman atanması gereken puanı girin.

## <a name="risk-assessments"></a>Risk değerlendirmeleri

Risk puanlarına göre müşterilere atanabilecek risk değerlendirmeleri tanımlayabilirsiniz. Bir risk puanı, müşteri bilgileri her bir puanlama grubuyla karşılaştırılarak hesaplanır. Müşterinin ait olduğu risk grubunu belirlemek için puanlar toplanır ve toplam puan, risk grubu kurulumundaki değerlerle karşılaştırılır. Risk grubu puanı, bunun ardından, müşteri için kredi yönetimi durdurma ve hariç tutma kurallarını tanımlamak için kullanılır.

Risk gruplarını **Risk değerlendirmeleri** sayfasında (**Kredi yönetimi \> Kurulum \> Risk kurulumu \>Risk değerlendirmeleri**) ayarlayabilirsiniz.

1. Bir risk grubu kimliği girin.
2. Risk grubunu daha ayrıntılı açıklamak için bir açıklama girin.
3. Risk grubuna hangi müşterilerin dahil olduğunu belirlemek için kullanılacak bir puan aralığı girin.
4. Risk grubunu temsil eden simgeyi belirtmek için bir risk grubu göstergesi seçin.

## <a name="guaranteeinsurance-types"></a>Garanti/sigorta türleri

Garanti/sigorta türlerini **Garanti/sigorta türleri** sayfasında (**Kredi yönetimi \> Kurulum \> Garanti/sigorta kurulumu \> Garanti/sigorta türleri**) ayarlayabilirsiniz.

1. Kefilin veya sigorta aracısının adını tanımlayan bir garanti veya sigorta türü girin.
2. Kefili/sigorta aracısını açıklamak için bir açıklama girin.

## <a name="coverage-types"></a>Karşılama türleri

Kapsam türleri, sigorta poliçelerini daha ayrıntılı sınıflandırmak için kullanılabilir. Bunlar garantilerle kullanılamaz.

Kapsam türlerini **Kapsam türleri** sayfasında (**Kredi yönetimi \> Kurulum \> Garanti/sigorta kurulumu \> Kapsam türleri**) ekleyebilirsiniz.

1. Sigorta veya garanti olarak eklenecek kapsam türünü belirlemek için bir kapsam türü girin.
2. Kapsam türünü açıklamak için bir açıklama girin.

## <a name="automatic-credit-limits"></a>Otomatik alacak limitleri

Otomatik kredi limitleri için ölçütleri **Otomatik kredi limitleri**sayfasında (**Kredi yönetimi \> Kurulum \> Risk kurulumu \> Otomatik kredi limitleri**) oluşturabilirsiniz.

1. Otomatik kredi limitinin atanacağı bir risk grubu seçin.
2. Otomatik kredi limiti için para birimini seçin. Aynı risk grubu için farklı para birimlerinde birden fazla otomatik kredi limiti oluşturabilirsiniz.
3. Bu otomatik kredi limiti için kullanılabilecek maksimum şirket gelirini temsil eden gelir tutarını girin. Kredi limitleri oluşturulurken, gelir tutarı, **Finansal öğeler** sayfasında (**Alacak hesapları \> Tüm müşteriler \> Müşteri seçin \> Genel \> İstatistikler \> Mali**) bulunan bir gelir değeriyle karşılaştırılır. Sistem **Genel bakış** bölümündeki en son değeri kullanır.

Seçilen ölçütlere göre oluşturulacak kredi limitini temsil eden satırları eklemek için bu adımları izleyin.

1. Kredi limitini hesaplamak için kullanılacak müşteri bilgilerini tanımlayan puanlama grubunu seçin.
2. Puanlama grubu bilgilerinin nasıl değerlendirileceğini tanımlayan karşılaştırma işlecini seçin.
3. Puanlama grubu için belirtilen değerle karşılaştırılacak değeri girin.
4. Müşteri bilgileri, puanlama grubu için belirtilen değerle eşleştiği zaman atanacak kredi limitini girin. Örneğin **Düşük** puanlama grubu için bir otomatik kredi limiti oluşturursunuz. Puanlama gruplarından biri Sektörde geçen yıl sayısı ise, müşterinin sektörde bulunduğu süre beş yılsa 100.000 kredi limiti atayan bir satır, ve müşterinin sektörde bulunduğu süre on yılsa 200.000 kredi limiti atayan başka bir satır tanımlayabilirsiniz.
