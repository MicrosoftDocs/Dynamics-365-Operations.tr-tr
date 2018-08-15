---
title: "Çağrı merkezi teslimat şekillerini ve masraflarını yapılandırma"
description: "Bu konu, Microsoft Dynamics 365 for Retail'de çağrı merkezi siparişi için teslimat şekillerinin ve masrafların nasıl ayarlanacağını açıklamaktadır."
author: josaw1
manager: AnnBe
ms.date: 04/26/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: dc2ab66bf6e3195e1ebf394f99182f59c3ee2125
ms.openlocfilehash: ebc8ee52da7d10ca18147684a0190e52a495ad5a
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---

# <a name="configure-call-center-delivery-modes-and-charges"></a>Çağrı merkezi teslimat şekillerini ve masraflarını yapılandırma

[!INCLUDE [banner](includes/banner.md)]

Microsoft Dynamics 365 for Retail'de bir satış siparişi verildiği zaman, satış siparişini giren kişi bir çağrı merkezi kanalına bağlıysa, teslimat şeklini doğrulamak ve sipariş masraflarını hesaplamak için mantık ve kurallar kullanılır.

Bir satış siparişi oluştururken, satış siparişi üst bilgisinde ve satış siparişi satırlarında bir teslimat şekli seçebilirsiniz. Varsayılan olarak, üst bilgide seçtiğiniz teslimat şekli, tüm satış siparişi satırları için kullanılır. Bununla birlikte, gereksinim duyduğunuz takdirde bu varsayılan teslimat şeklini tek tek satış satırlarında değiştirebilirsiniz. Müşteri kaydında da bir teslimat şekli tanımlayabilirsiniz. Bunun üzerine, müşteri için siparişler oluşturulurken o teslimat şekli satış siparişi üst bilgisinde varsayılan olarak kullanılır.

Perakendenin, kullanıcılara bir kanalın kullanabileceği teslimat şekillerini, bir ürün için kullanılabilecek teslimat şekillerini ve belirli sevkiyat hedefleri için geçerli olan teslimat şekillerini sınırlama olanağı veren yetenekleri vardır. Satış siparişi için seçilen teslimat şekillerine ve toplam sipariş değerine göre müşterinin siparişine ek ücretler getirilebilmesi için masraflar da tanımlanabilir.

## <a name="define-delivery-modes"></a>Teslimat şekillerini tanımlama
Çağrı merkezi siparişleri için kullanılabilecek teslimat şekillerini belirleyip ilişkili kurallar ve masraflar tanımlamadan önce teslimat şekillerini tanımlamanız gerekir. **Satış ve pazarlama \> Kurulum \> Dağıtım \> Teslimat şekilleri**'ne gidin. Yeni bir teslimat şekli oluşturmak için **Yeni**'yi seçin. Alternatif olarak, listedeki mevcut bir teslimat şeklini seçin ve ardından değişiklikler yapmak için **Düzenle**'yi seçin.

**Teslimat şekli** alanında, iş gereksiniminize göre bir alfasayısal karakter birleşimi girebilirsiniz. Bunun ardından, **Açıklama** alanını kullanarak ek içerik girebilirsiniz. **Giderler grubu** ve **Hızlandır** alanları isteğe bağlıdır ve bu konunun ilerleyen bölümlerinde daha ayrıntılı açıklanacaktır.

**Perakende kanalları** hızlı sekmesinde, satış hareketleri oluşturulurken teslimat şeklini kullanmasına izin verilecek Perakende kanalını ekleyin.

**Ürünler** hızlı sekmesinde, teslimat şeklinin kullanılabileceği veya kullanılamayacağı ürünleri ve/veya ürün kategorilerini belirtebilirsiniz. Örneğin bir ürün tehlikeli madde kısıtlamaları nedeniyle havayoluyla sevk edilemiyorsa, ürünün veya ürün kategorisinin havayoluyla nakliyat içeren tüm teslimat şekillerinden çıkarıldığından emin olun.

**Adresler** hızlı sekmesinde, teslimat şeklinin kullanılabileceği veya kullanılamayacağı ülkeleri, bölgeleri veya eyaletleri belirtebilirsiniz. Örneğin, Hawaii veya Alaska'ya sevk edilen siparişler karayoluyla teslimata uygun değil. Bu nedenle, bu eyaletlerin karayoluyla teslim hizmetiyle ilişkili tüm teslimat şekillerinden çıkarılması ancak bir havayoluyla teslim hizmetiyle ilişkili tüm teslimat şekillerine dahil edilmesi gerekir.

## <a name="validate-delivery-modes-for-a-call-center-order"></a>Çağrı merkezi siparişi için teslimat şekillerini doğrulama
Teslimat şekilleri tanımlandıktan sonra **Teslimat şekillerini işle** toplu işini çalıştırmalısınız. Bu iş, Perakende kanalları için satış siparişi işlemlerinde teslimat şekillerini kullanılabilir hale getirir. **Teslimat şekillerini işle** işini çalıştırmak için **Perakende \> Perakende BT'si \> Teslimat şekillerini işle**'ye gidin. Bu iş, bir perakende kanalına yeni teslimat şekilleri eklendiği veya mevcut teslimat şekli/kanal ilişkilerinde değişiklik yapıldığı zaman çalıştırılmalıdır.

**Teslimat şekillerini işle** toplu işini çalıştırdıktan sonra **Perakende \> Kanallar \> Çağrı merkezleri \> Tüm çağrı merkezleri**'ne gidebilirsiniz. **Tüm çağrı merkezleri** sayfasındaki Eylem Bölmesinde, **Ayarla** sekmesinde **Teslimat şekilleri**'ni seçin. **Teslimat şekilleri** sayfasında, seçilen çağrı merkezi kanalı için tüm geçerli teslimat şekilleri listelenir. Mevcut teslimat şekillerini düzenlemek veya yeni teslimat şekilleri eklemek için **Teslimat şekillerini yönet**'i seçin. **Teslimat şekillerini işle** işinin her değişiklik yapıldığında çalıştırılması gerektiğini unutmayın.

## <a name="define-charges-for-delivery-services"></a>Teslimat hizmetleri için masrafları tanımlama
Müşteriler için satış siparişleri oluşturulduğunda, şirket sipariş için seçilen teslimat şekillerine göre otomatik olarak hesaplanan masraflar eklemek isteyebilir. Bu masraflar tüm müşteriler ve teslimat şekilleri için aynı olacak şekilde yapılandırılabilir. Alternatif olarak, masraflar, müşteriye ve/veya satış siparişi için seçilen teslimat şekillerine bağlı olarak değişebilir.

Masrafları tanımlamak için **Perakende \> Kanal kurulumu \> Giderler \> Otomatik masraflar**'a gidin. Yeni masraflar eklemek için **Yeni**'yi seçin. Alternatif olarak, mevcut bir girişi ve ardından **Düzenle**'yi seçin.

Masraflar sipariş üst bilgisi veya sipariş satırları düzeyinde hesaplanabilecek şekilde tanımlanabilir. İstediğiniz düzeyi seçmek için **Düzey** alanını seçin.

Masraflar belirli bir müşteri, bir grup müşteri veya tüm müşteriler için tanımlanabilir. Yalnızca belirli bir müşteriye uygulanan masrafları tanımlamak için **Hesap kodu** alanında **Tablo**'yu seçin. Belirli bir müşteri grubuna yönelik masrafları tanımlamak için **Grup**'u seçin. İlgili teslimat şeklini kullanan bir satış siparişini veren her müşteriye masrafları uygulamak için **Tümü**'nü seçin. **Hesap kodu** alanında **Tablo**'yu veya **Grup**'u seçtiyseniz, **Hesap ilişkisi** alanında müşteriyi veya müşteri grubunu seçin.

Masraflar belirli bir teslimat şekline, bir teslimat şekli grubuna veya tüm teslimat şekillerine uygulanacak şekilde yapılandırılabilir. **Teslimat şekli kodu** alanında **Tablo**'yu seçerseniz, **Teslimat şekli ilişkisi** alanında belirli bir teslimat şekli seçmeniz gerekir. **Grup**'u seçerseniz, **Teslimat şekli ilişkisi** alanında bir teslimat şekli grubu seçmeniz gerekir. Teslimat şekli grupları **Perakende \> Kanal kurulumu \> Giderler \> Teslimat masrafları grubu**'nda tanımlanır. Bunlar daha sonra **Teslimat şekilleri** sayfasında bir veya daha fazla teslimat şekline bağlanabilir. Masrafları tanımlarken bir grup seçerseniz, seçilen teslimat grubuna bağlanan teslimat şekilleri bu masrafları kullanır. Son olarak, **Teslimat şekli kodu** alanında **Tümü**'nü seçerseniz, masraflar tüm teslimat şekilleri tarafından kullanılır. Bu nedenle, **Teslimat şekli ilişkisi** alanında bir değer seçmezsiniz.

**Satırlar** bölümünde, gereksiniminize göre bir veya daha fazla masrafı para birimiyle tanımlayabilirsiniz. Masraflar, masrafa ilişkin mali nakil kurallarını tanımlayan bir masraflar koduna bağlanmalıdır. **Kategori** alanı, masrafların nasıl hesaplanacağını tanımlamak için kullanılır. Örneğin, müşteriler bir siparişlerini belirli bir teslimat şekliyle vermek için 9,95 lira sabit bir ücret ödeyecekse **Sabit** kategorisini kullanın. İşletme, teslimat masraflarını karşılamak için müşterilerinden sipariş toplamının belirli bir yüzdesi kadar masraf almaya karar verirse **Yüzde** kategorisini kullanın. Müşterilerin ödeyeceği gerçek ücret **Masraf değeri** alanında tanımlanır.

Perakende şirketleri genellikle katmanlı masraflar yapılandırır. Bu durumda, müşterinin teslimat için ödeyeceği tutar için, sipariş değeri baz alınır. Katmanlı masrafları yapılandırmak için, **Masraf değeri** alanında masrafın kendisini tanımlamaya ek olarak, **Başlangıç tutarı** ve **Bitiş tutarı** alanlarına değerler girin. Örneğin 50 liradan daha düşük değerli siparişlerde, satıcı, karayoluyla sevkiyat için 5,95 lira masraf alır. Değeri 50 lira ve üzerinde olan ama 100 liradan düşük siparişlerde satıcı 7,95 lira masraf alır. Son olarak, değeri 100 lira ve üzerinde olan siparişlerde satıcı ücretsiz sevkiyat sunar. Aşağıdaki çizimde bu masrafların yapılandırması gösterilmektedir.

![Sabit katmanlı masraflar örneği](media/fixedtieredcharges.png)

İş gereksinimlerinize bağlı olarak, masraflar için bir kategoriler karışımı kullanabilirsiniz. Örneğin değeri 100 liranın altında olan tüm siparişlerde sevkiyat için sabit 9,95 lira masraf vardır. Bu durumda değeri 100 liranın üzerindeki siparişlerde teslimat masrafları, sipariş değerinin yüzde 5'i oranıyla hesaplanır. Aşağıdaki çizimde bu masrafların yapılandırması gösterilmektedir.

![Karma katmanlı masraflar örneği](media/mixedtieredcharges.png)

## <a name="apply-delivery-modes-during-order-entry-in-a-call-center"></a>Bir çağrı merkezinde sipariş girişi sırasında teslimat şekillerini uygulama
Yeni bir satış siparişi oluşturulurken, satış siparişi üst bilgisinin **Teslimat** hızlı sekmesindeki **Teslimat şekli** alanında bir değer belirtilmelidir. Bu alan müşteri kaydından alınan varsayılan değerlere göre otomatik olarak doldurulabilir.

Sipariş üst bilgisinde tanımlanan teslimat şekli, oluşturulan satış siparişi satırlarına otomatik olarak kopyalanır. Bununla birlikte, belirli bir satır maddesinin teslimat şekli kurulumunu, satış siparişi giriş sayfasının **Satır ayrıntıları** bölümündeki **Teslimat** sekmesinde değiştirebilirsiniz.

Seçilen teslimat şekli sipariş veya sipariş satırı için tanımlanmış ürün veya teslimat adresi için geçerli değilse bir hata iletisi alırsınız. Bu durumda, o ürün veya adres yapılandırmasını desteklemek üzere tanımlanmış bir teslimat şekli seçmeniz gerekir.

## <a name="calculation-of-delivery-charges-during-entry-of-order"></a>Sipariş girişi sırasında teslimat masraflarını hesaplama
Çağrı merkezi kanalınız için **Sipariş tamamlamayı etkinleştir** ayarı açılırsa, kullanıcılar **Tamamla**'yı seçtiği zaman satış siparişleri için sevkiyat masrafları otomatik olarak hesaplanır. **Satış siparişi özeti** sayfasının üst kısmında şu mesaj görünür: "Katmanlı masraflar hesaplandı." Hesaplanan masraflar, **Toplam satış** alanının değerine eklenir. **Tutar** hızlı sekmesinde, **Giderler** alanı, sipariş ve satırlar için hesaplanan tüm masrafların toplam tutarını gösterir. Masrafların daha ayrıntılı bir dökümünü görmek için **Satış siparişi özeti** sayfasında **Sipariş**'i seçin ve ardından masrafları görüntülemek, eklemek veya düzenlemek için **Giderler** seçeneğini belirleyin. Sipariş üst bilgisindeki teslimat masraflarının hesaplanmasında üst bilgiyle bağlantılı teslimat şeklinin baz alındığına dikkat edin. Satır düzeyinde teslimat masrafları, satış satırı için yapılandırılan teslimat şekline göre hesaplanır. Farklı satırlarda birden fazla teslimat şekli kullanılıyorsa, birden çok masraf uygulanıp toplanabilir. Bunun ardından, toplam tutar **Satış siparişi özeti** sayfasındaki **Giderler** sayfasında gösterilir.

**Sipariş tamamlamayı etkinleştir** ayarı kapatılırsa, kullanıcıların, masrafları hesaplamayı el ile tetiklemesi gerekir. **Satış siparişi** sayfasındaki Eylem Bölmesinde, **Satış** sekmesinin **Hesapla** grubunda **Katmanlı masraflar**'ı seçin. "Katmanlı masraflar hesaplandı" iletisi görünür. Bunun ardından, hesaplanan masrafları görüntülemek, düzenlemek veya silmek için, **Satış** sekmesinde **Giderler** seçeneğini belirleyin.

## <a name="use-expedited-delivery-modes-on-call-center-orders"></a>Çağrı merkezi siparişlerinde hızlandırılmış teslimat şekillerini kullanma
İsterseniz, yapılandırdığınız teslimat şekline bir hızlandırma kodu bağlayabilirsiniz. Bu kod bir öncelik sıralama ve raporlama aracı olarak kullanılır. Şu anda siparişe ek ücretler uygulanmasına neden olmamaktadır. Hızlandırma kodlarını ayarlamak için **Satış ve pazarlama \> Kurulum \> Dağıtım \> Hızlandırma kodları**'na gidin.

Örneğin ertesi gün havayoluyla sevk edilecek siparişler için, ambardan malzeme çekme işleminin her gün 13:00'a kadar yapılması gerekir. Bu durumda, bir hızlandırma kodu oluşturulabilir ve bu kod, sistemde yapılandırılmış herhangi bir ertesi gün teslimat şekline bağlanabilir. Ambar, çekme dalgasını oluştururken, **Hızlandır** alanındaki ilgili hızlandırma kodu bir filtre olarak kullanılıp, malzeme çekme işleminin, teslimat şekilleri yalnızca o kodla bağlantılı siparişler için çalıştırılması sağlanabilir.

Ek olarak, bir çağrı merkezi siparişi girilirken ya satış siparişi üst bilgisine veya tek bir satış sipariş satırına el ile bir hızlandırma kodu uygulanabilir. Yine, bu kod, sıralama veya raporlama amacıyla kullanılabilir. Bazı durumlarda, bir müşteri hizmeti sorunu nedeniyle bir siparişin dikkatle ele alınması gerekir. Böyle durumlarda, sipariş karşılama sürecinde siparişin saptanıp öncelik kazanmasına yardımcı olmak için sipariş üst bilgisine veya satırlarına belirli bir hızlandırma kodu uygulanabilir.

