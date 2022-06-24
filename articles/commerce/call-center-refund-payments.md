---
title: Çağrı merkezlerinde iade ödemelerini işleme
description: Bu makalede, iadeler oluşturulduğunda veya siparişler veya sipariş satırları iptal edildiğinde iade ödemelerinin çağrı merkezleri aracılığıyla nasıl oluşturulduğu açıklanmaktadır.
author: hhainesms
ms.date: 01/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 330674a31dc59e99ffedb82d0896c64214562eb3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880126"
---
# <a name="refund-payment-processing-in-call-centers"></a>Çağrı merkezlerinde iade ödemelerini işleme

Bu makalede, iadeler oluşturulduğunda veya siparişler veya sipariş satırları iptal edildiğinde iade ödemelerinin çağrı merkezleri aracılığıyla nasıl oluşturulduğu açıklanmaktadır.

Microsoft Dynamics 365 Commerce Headquarters'da çağrı merkezi kullanıcısı olarak bir müşteri için sipariş iadesi oluşturan bir kullanıcı, ilk iade malzemeleri yetkilendirmesini (RMA) oluşturmak için **İade emri** sayfasını kullanır. RMA, müşterinin iade etmek veya değiştirmek istediği ürünleri tanımlar ve iade edilen siparişin sipariş türüne sahip bağlantılı bir **İade satış siparişi** oluşturur. Bu bağlantılı iade siparişi, iade edilen stokun deftere naklini ve deftere nakledilen alacak dekontlarını veya ödeme iadelerini izlemek için kullanılır.

Çağrı merkezi kanalı için **Sipariş tamamlamayı etkinleştir** seçeneği **Evet** olarak ayarlanmışsa, RMA'yı oluşturan çağrı merkezi kullanıcısının **İade siparişi** sayfasında **Tamamlandı**'yı seçerek sipariş tamamlama işleme akışını çalıştırması gerekir. **Tamamla** işlevi, vadesi gelen iade tutarını özetleyen hesaplanmış bir iade özeti sağlar. Ayrıca, doğru şekilde yapılandırıldığında, iade edilen siparişle karşılaştırarak sistematik olarak bir iade satırı oluşturur.

Çağrı merkezi mantığı, orijinal sipariş için kullanılan ödeme yöntemine bağlı olarak iade ödeme hattının ödeme yöntemini belirler. Oluşturulan iade siparişi orijinal bir siparişe bağlı değilse, sistem parametresinden alınan varsayılan bir ödeme yöntemi uygulanır.

## <a name="how-a-call-center-determines-which-payment-method-to-apply-to-a-return-order"></a>Çağrı merkezi iade siparişine hangi ödeme yönteminin uygulanacağını nasıl belirler?

Çağrı merkezi, iade siparişine uygulanması gereken ödeme yöntemini belirlemek için orijinal siparişin ödeme yöntemini kullanır. Bu işlem aşağıdaki orijinal ödeme yöntemleri için şu şekilde çalışır:

- **Normal** (nakit) veya **Çek**: Oluşturulan bir iade siparişi, normal (nakit) veya çek ödeme türü kullanılarak ödenen orijinal bir siparişe başvuruyorsa, çağrı merkezi uygulaması **Çağrı merkezi iade yöntemleri** sayfasındaki yapılandırmalara başvurur. Bu sayfa, kuruluşların sipariş para birimine göre, normal veya çek ödeme türü kullanılarak başlangıçta ödenen siparişler için müşterilere nasıl iade yapılacağını tanımlamasını sağlar. **Çağrı merkezi iade yöntemleri** sayfası, kuruluşların sistem tarafından oluşturulan bir iade çekinin müşteriye gönderilip gönderilmeyeceğini seçmesine olanak tanır. Bu senaryolarda, çağrı merkezi mantığı iade siparişinin para birimine başvurur ve iade satış siparişinde bir iade satırı oluşturmak için bu para biriminin **Perakende ödeme yöntemi** değerini kullanır. Daha sonra, eşlenen AR ödeme yöntemini kullanan bir alacak hesapları (AR) müşteri ödeme günlüğü para birimine bağlanır.

    Aşağıdaki resimde, müşterinin USD para birimine bağlı bir satış siparişinden ürünleri iade ettiği ve başlangıçta normal veya çek ödeme türü kullanılarak ödendiği bir senaryonun yapılandırması gösterilmektedir. Bu senaryoda, sistem tarafından oluşturulan bir iade çeki aracılığıyla müşteriye iade yapılacaktır. **REF-CHK** AR ödeme yöntemi, iade çeki ödeme türü olarak yapılandırılmıştır.

    ![Normal ve orijinal ödemeleri denetlemek için çağrı merkezi iade yöntemlerini yapılandırma.](media/callcenterrefundmethods.png)

    > [!NOTE]
    > Müşteri hesabı, nakit veya çek ödemeleri için desteklenen bir iade yöntemi değildir.

- **Kredi kartı**: Oluşturulan bir iade siparişi, kredi kartı kullanılarak ödenen orijinal bir siparişe başvurduğunda, iade ödemeleri için çağrı merkezi mantığı iade siparişine aynı orijinal kredi kartını uygular.
- **Bağlılık programı kartı**: Oluşturulan bir iade siparişi, müşteri bağlılık kartı kullanılarak ödenen orijinal bir siparişe başvurduğunda, iade ödemeleri için çağrı merkezi mantığı para iadesini aynı bağlılık programı kartına uygular.
- **Hediye kartı** (dahili): Oluşturulan bir iade siparişi, Dynamics 365 Commerce'ten verilen bir hediye kartı kullanılarak (dahili hediye kartı işlevselliği) ödenen orijinal bir siparişe başvurduğunda , iade ödemeleri için çağrı merkezi mantığı iadeyi aynı orijinal hediye kartı numarasına uygular.
- **Hediye kartı** (Harici): Oluşturulan bir iade siparişi, harici bir üçüncü taraf hediye kartı kullanılarak ödenen orijinal bir siparişe başvurduğunda, iade ödemeleri için çağrı merkezi mantığı, **Çağrı merkezi parametreleri** sayfasının **RMA/İade** sekmesinde tanımlanan varsayılan iade ödeme yöntemini uygular.

Orijinal sipariş ödeme türü herhangi bir nedenle bilinmiyorsa veya orijinal siparişi ödemek için birden çok ödeme yöntemi kullanılmışsa, çağrı merkezi mantığı, **Çağrı merkezi parametreleri** sayfasının **RMA/İade** sekmesinde tanımlanan varsayılan iade ödeme yöntemini uygular.

Aşağıdaki resimde, **Çağrı merkezi parametreleri** sayfasının **RMA/İade** sekmesindeki **Ödeme yöntemi** alanı gösterilmektedir.

![Çağrı merkezi parametreleri sayfasının RMA/İade sekmesindeki ödeme yöntemi alanı.](media/callcenterrefundparameters.png)

> [!NOTE]
> Daha önce açıklanan iade işleme kuralları, bir çağrı merkezi kullanıcısının Commerce Headquarters'da iptal ettiği siparişler veya sipariş satırları için de geçerlidir. Bir siparişin veya belirli sipariş satırlarının iptali herhangi bir fazla ödemeye neden olursa, iade ödeme satırları oluşturmak için aynı kurallar kullanılır.

Genellikle, iade siparişi, stokun alındığı (veya ıskartaya çıkarıldığı), iade siparişine karşı bir sevk irsaliyesinin nakledildiği ve ardından iade satış siparişi için bir fatura deftere nakil işleminin çalıştırıldığı standart bir işlemden geçer. İade satış siparişi, iade siparişini oluşturma işlemi kapsamında olarak bağlantılı ve sistematik olarak oluşturulur. Tipik senaryolarda, iade satış siparişinin faturası deftere nakledilene kadar müşterilere iade ödeme yapılmaz.

### <a name="what-happens-when-an-invoice-is-posted-on-a-return-sales-order"></a>İade satış siparişinde bir fatura deftere nakledildiğinde ne olur?

Aşağıdaki senaryolarda, bir fatura iade satış siparişine nakledildiğinde ne olacağı açıklanmaktadır:

- İade siparişinde para iadesi ödemesi bir kredi kartı içinse fatura deftere nakledildiğinde ek mantık çağrılır. Bu mantık, ödeme işlemcisini müşterinin kredi kartına ödemeyi iade etmeye çağırır. İade müşteri ödeme fişi de oluşturulur ve müşterinin hesabına sistematik olarak nakledilir. Bu ödeme günlüğü iade siparişi alacak dekontu fişine göre kapatılır.
- Yapılması gereken iade ödeme çek ödeme türü içinse, AR ödeme yöntemini kullanan bir müşteri ödeme fişi oluşturulur ve ödeme fişinin müşteri hesabına nakledilebilmesi için el ile deftere nakledilmesi veya yazdırılması gerekir. Geri ödeme denetimini işlemek için kullanıcılar alacak hesaplarındaki **Müşteri ödeme günlüğü** sayfasını veya Perakende ve Ticaret'teki özel **İade çeki işleme** sayfasını kullanabilir.
- Yapılması gereken iade ödeme dahili hediye kartı veya bağlılık programı kartı ödeme türü içinse, iade siparişi faturalandığında, geri ödeme ödeme fişi oluşturulur ve müşteri hesabına nakledilir. Bu faturalama adımı, iade tutarını müşterinin dahili olarak izlenen hediye kartı bakiyesine veya bağlılık puanı bakiyesine de ekler.
- **Müşteri** işlevini kullanan bir ödeme yöntemi (örneğin, müşteri hesabı) iade satış siparişine bağlıysa ödeme işlendiğinde kredi limiti doğrulamaları yok sayılır. Bu bağlamda hiçbir ödeme fişi oluşturulmaz veya deftere nakledilmez. İade siparişinde bir müşteri ödeme türü kullanıldığında, fatura deftere nakil işleminin oluşturduğu alacak dekontu fişi müşteri kredi fişi görevi görür ve müşterinin AR bakiyesine para iadesi olduğunu gösterir.

## <a name="advance-credit"></a>Avans kredisi

Bir kullanıcı **Sipariş tamamlamayı etkinleştir** seçeneğinin **Evet** olarak ayarlandığı bir çağrı merkezinde çağrı merkezi kullanıcısı olarak iade siparişlerini işlediğinde, iade siparişini oluşturan çağrı merkezi kullanıcısı, **Çağrı merkezi parametreleri** sayfasının **RMA/İade** sekmesinde **Avans kredisi** seçeneğini **Evet** olarak ayarlarsa, iade ödemesi deftere naklinde önceden açıklanan işlem için bir istisna oluşabilir. Bu durumda, ödeme iadesi, iade siparişinin **İade özeti** sayfasındaki **Gönder** işlevi kullanılarak başarıyla gönderilmesinden hemen sonra gerçekleşir. İade satış siparişinin kendisi henüz faturalanmamış olsa da, sistem iade değeri için hemen bir ön ödeme müşteri ödemesi fişi oluşturur. Bu yaklaşım, bir kuruluşun müşteri hizmetleri sorunları nedeniyle müşterilere önceden para iadesi yapması gereken durumlarda kullanılabilir ve iadeler yapılmadan önce iade edilen stokun alınmasını gerektirmez.

## <a name="replacement-orders"></a>Değiştirme siparişleri

İade siparişi oluşturulduğunda, müşteri için yeni bir satış siparişi oluşturmak üzere **Değiştirme siparişi** işlevi kullanılabilir. Bu yaklaşım değişim senaryolarında kullanılabilir. **Değiştirme siparişi** işlevi gönderilmesi gereken yeni maddeler için başka bir satış siparişi oluşturur ancak **Çağrı merkezi parametreleri** sayfasının **RMA/İade** sekmesindeki çapraz referans bağlantısı değiştirme siparişini, RMA'yı ve iade edilen satış siparişini birbirine bağlar.

Değiştirme siparişlerindeki ödemeler işlendiğinde, kuruluşların iki seçeneği olur:

- İade siparişi için müşteriye orijinal ödeme yöntemine göre para iadesi yapma ve ardından değiştirme siparişi için ayrı bir ödeme alma. Bu seçeneği kullanmak için herhangi bir ek kurulum gerekmez.
- **Çağrı merkezi parametreleri** sayfasının **RMA/İade** sekmesinde **Kredi uygula** seçeneğini **Evet** olarak ayarlayın. Bu durumda, hem iade siparişine hem de değiştirme siparişine sistematik olarak bir müşteri ödeme yöntemi uygulanır. Bu seçenek, herhangi bir harici iade ödemesinin düzenlenmesini önlemeye yardımcı olabilir. Ayrıca hareket üzerinde herhangi bir ödemenin işlenmesini önlemeye yardımcı olur. Eşit bir değişimin işlendiği durumlarda faydalı olabilir ve kuruluş, iade siparişi faturalandığında oluşturulan alacak fişini, değiştirme siparişi tarafından oluşturulan faturayı ödemek için kullanmayı tercih eder. **Kredi uygula** seçeneği **Evet** olarak ayarlandığında, kuruluşun alacak dekontunu her iki mali belge oluşturulduktan sonra değiştirme siparişinin faturasına karşılık olarak el ile kapatması gerekir.

**Kredi uygula** seçeneği için **Evet** ayarı yalnızca iade siparişi yeni bir siparişe bağlandığında geçerlidir. Bu durumda, iade ve değişim siparişi için sistematik olarak ödeme yapmak üzere kullanılacak müşteri ödeme yöntemi, **Çağrı merkezi parametreleri** sayfasının **RMA/İade** sekmesindeki **Kredi ödeme yöntemi uygula** alanı tarafından tanımlanır. Bu alanda yalnızca **Müşteri** işlevi ödeme türünün bir ödemesi seçilebilir.

> [!NOTE]
> Bağlantılı değiştirme emri olmayan bir iade siparişi için, **Kredi uygula** seçeneği için **Evet** ayarı iade siparişi ödeme mantığı üzerinde hiçbir etkiye sahip olmayacaktır çünkü bu ayar yalnızca değiştirme siparişleri için geçerlidir.

![Çağrı merkezi parametreleri sayfasının RMA/İade sekmesindeki Kredi ödeme yöntemi uygula alanı.](media/callcenterrefundparameters1.png)

> [!IMPORTANT]
> Değiştirme siparişleri oluşturan kullanıcılar **Kredi uygula** seçeneğini kullanmayı planlıyorsa, **Kredi uygula** seçeneğini **Evet** olarak ayarlamadan önce iade siparişinde **Tamamla** işlevini çalıştırmamalıdır. **Tamamla** işlevi çalıştırıldıktan sonra, geri ödeme hesaplanır ve iade satış siparişine uygulanır. İade ödemesi zaten hesaplandıktan ve uygulandıktan sonra **Kredi uygula** seçeneğini **Evet** olarak ayarlama girişimi, iade ödemesinin yeniden hesaplanmasını tetiklemez ve **Kredi ödeme yöntemini uygula** alanında seçilen ödeme yöntemi uygulanmaz. Bu bağlamda **Kredi uygula** seçeneğinin kullanılması gerekiyorsa, kullanıcının değiştirme siparişini ve RMA'yı silmesi ve ardından baştan başlayıp yeni bir RMA oluşturması gerekir. Bu kez, kullanıcının **Tamamla** işlevini çalıştırılmadan önce **Kredi uygula** seçeneğinin **Evet** olarak ayarlandığından emin olması gerekir.

## <a name="payment-overrides-for-call-center-returns"></a>Çağrı merkezi iadeleri için ödeme geçersiz kılmaları

Çağrı merkezi mantığı, iade ödemesi yöntemini bu makalede daha önce açıklanan şekilde sistematik olarak belirlese de, kullanıcılar bazen bu ödemeleri geçersiz kılmak isteyebilir. Örneğin, bir kullanıcı mevcut iade ödeme satırlarını düzenleyebilir veya kaldırabilir ve yeni ödeme satırları uygulayabilir. Sistem tarafından hesaplanan iade ödemeleri yalnızca doğru geçersiz kılma izinlerine sahip kullanıcılar tarafından değiştirilebilir. Bu izinler Perakende ve Ticaret'teki **Geçersi kılma izinleri** sayfasında yapılandırılabilir. İade ödemesini geçersiz kılmak için kullanıcının **Geçersiz kılma izinleri** sayfasında **Alternatif ödemeye izin ver** seçeneğinin **Evet** olarak ayarlandığı bir güvenlik rolüne bağlanması gerekir.

![Geçersiz kılma izinleri sayfasında alternatif ödemeye izin ver seçeneği.](media/overridepermissions.png)

Alternatif olarak, bir kuruluş **Çağrı merkezi parametreleri** sayfasının **RMA/İade** sekmesinde **Ödeme geçersiz kılmaya izin ver** seçeneğini **Evet** olarak ayarlayabilir. Bu durumda, **Güvenlik Geçersiz Kılma Kodu** alanında bir güvenlik geçersiz kılma kodu seçilmelidir. Güvenlik geçersiz kılma kodu, kullanıcılar ayarlandıktan sonra Commerce Headquarters'da görüntüleyemediğinden, dışarıdan yönetilmesi gereken alfasayısal bir koddur. Güvenlik geçersiz kılma kodu, bir kuruluştaki yalnızca birkaç önemli, güvenilir kişi tarafından bilinmelidir. **Ödeme geçersiz kılmaya izin ver** seçeneği **Evet** olarak ayarlandığında, doğru rol izinlerine sahip olmayan kullanıcılar iade siparişinde ödeme yöntemini değiştirmeye çalışırsa güvenlik geçersiz kılma kodunu girme seçeneğine sahip olurlar. Bu kodu bilmiyorlarsa veya bir yönetici veya süpervizör onlar adına kodu sayfaya giremezse iade ödeme yöntemini geçersiz kılamazlar.

> [!NOTE]
> Güvenlik geçersiz kılma kodu kaybolur veya unutulursa kuruluş, **Çağrı merkezi parametreleri** sayfasının **RMA/İade** sekmesindeki **Güvenlik Geçersiz Kılma Kodu** alanında yeni bir güvenlik geçersiz kılma kodu tanımlayarak kodu sıfırlamak zorunda kalır.

![Çağrı merkezi parametreleri sayfasının RMA/İade sekmesindeki Ödeme geçersiz kılma parametreleri.](media/overridepaymentparameter.png)

> [!IMPORTANT]
> Kuruluşlar, kredi kartı ödeme türlerini kullanan iade ödemelerini geçersiz kılmaya çalışmadan önce, kredi kartı işlemcilerinin bağlantısız iadelere izin verdiğini doğrulamalıdır. Birçok işlemci, geri ödemelerin orijinal karta geri nakledilmesini gerektirir. Daha önce yakalaması olmayan bir karta para iadesi yapma girişimi, işlemcide deftere nakil hatalarına neden olabilir.

## <a name="additional-resources"></a>Ek kaynaklar

[Çağrı merkezlerinde ödeme yöntemleri](work-with-payments.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]