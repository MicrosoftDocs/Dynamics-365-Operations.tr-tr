---
title: Tahsilat yönetimi temel kavramları
description: Bu konu, tahsilat yönetimiyle ilgili temel kavramları tanımlamaktadır.
author: JodiChristiansen
ms.date: 11/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 508723752ec7ae5f48e52c728b6ef526ec49e4e2
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/06/2022
ms.locfileid: "8723037"
---
# <a name="collections-management-key-concepts"></a>Tahsilat yönetimi temel kavramları

[!include [banner](../includes/banner.md)]

Tahsilatları ayarlamaya veya bunlar üzerinde çalışmaya başlamadan önce aşağıdaki kavramları anlamanız gerekir:

- Müşteri yaşlandırma anlık görüntüsü belirli bir zamandaki yaşlandırılmış bakiye bilgilerini içerir.
- Tahsilat müşteri havuzları işinizi organize etmenize yardımcı olur.
- Tahsilat temsilcilerinin kendi müşteri havuzları olabilir.
- Liste sayfaları tahsilat müşterilerini, etkinlikleri ve vakaları organize eder.
- Bir müşteriyle ilgili tüm tahsilat bilgileri tek bir sayfada bulunur ve bu sayfadan eylem gerçekleştirebilirsiniz.
- Faiz ve ücretlerden feragat etme, bunları eski durumuna getirme veya tersine çevirme işlemi tek bir adımda yapılabilir.
- Silme hareketleri tek bir adımda oluşturulabilir.
- Yetersiz fon (NSF) ödemeleri tek adımda işlenebilir.

Bu konuda her kavram açıklanmaktadır.

## <a name="customer-aging-snapshots"></a>Müşteri yaşlandırma anlık görüntüleri

Bir yaşlandırma anlık görüntüsü, bir müşterinin belirli bir zamandaki hesaplanan yaşlandırılmış bakiyesini içerir. Bu bilgi, **Yaşlandırılmış bakiyeler** listesi sayfası ve **Tahsilatlar** sayfasında gösterilir. Tahsilat listesi sayfalarındaki (**Yaşlandırılmış bakiyeler**, **Tahsilat faaliyetleri** ve **Tahsilat vakaları**) bilgileri görüntüleyebilmeniz için bir yaşlandırma anlık görüntüsünün oluşturulması gerekir.

Her müşteri için, yaşlandırma anlık görüntüsü bir yaşlandırma anlık görüntüsü başlığı ve yaşlandırma dönemi tanımındaki her yaşlandırma dönemine karşılık gelen ayrıntılı kayıtları içerir.

Yaşlandırma anlık görüntüsü başlığı vadesi gelen toplam tutarı, kredi limitini, sevk irsaliyesi tutarını, satış siparişi tutarını, müşteri hesabındaki ihtilaflı hareketlerin toplam tutarını içerir. Müşteriye ilişkin tüm hareketler bu tutarlar hesaplanırken dahil edilir. Vadesi gelen toplam tutar, alacak limiti, sevk irsaliyesi tutar ve satış siparişi tutarı **Tahsilatlar** sayfasındaki **Alacak bilgileri** bilgi kutusunda gösterilir.

Yaşlandırma dönemi tanımındaki her yaşlandırma dönemi için, yaşlandırma anlık görüntüsünde bir ayrıntı kaydı oluşturulur. Her ayrıntı kaydı, yaşlandırma dönemi kodunu ve yaşlandırma döneminde tarihleri olan hareketlerin toplam tutarını içerir. Hareketler bir yaşlandırma dönemine atanabilir (vadesi 30 gün geçmiş gibi). Tarih, yaşlandırma anlık görüntüsünü oluştururken belirttiğiniz **Yaşlandırma başlangıcı** tarih değeriyle ilişkilidir. Bu bilgi, **Yaşlandırılmış bakiyeler** liste sayfasında ve **Tahsilatlar** sayfasındaki **Yaşlandırılmış bakiyeler** bilgi kutusunda gösterilir.

## <a name="collections-customer-pools"></a>Tahsilat müşteri havuzları

Müşteri havuzları, bir grup müşteri kaydını tanımlayan sorgulardır. Bu gruplandırılmış kayıtları, dahil edilen müşteri hesaplarıyla ilgili bilgileri görüntülemek ve bunlar için tahsilatları veya yaşlandırma işlemlerini yönetmek için kullanabilirsiniz. Tahsilat listesi sayfalarındaki bilgileri filtrelemek için müşteri havuzlarını kullanabilirsiniz. Yaşlandırma anlık görüntüsü oluşturulduğunda eklenecek müşteri hesaplarını filtrelemek için de bu müşteri havuzlarını kullanabilirsiniz.

## <a name="collections-agents"></a>Tahsilat temsilcisi

Varsayılan olarak, kullanıcılar tahsilat listesi sayfalarındaki tüm müşteri bilgilerini görebilirler. Tahsilat temsilcisi kayıtları, tahsilat listesi sayfalarındaki ve **Tahsilatlar** sayfasındaki bilgileri filtrelemek için kullanılabilecek müşteri havuzlarını belirlemenize olanak sağlar.

Tahsilat temsilcisi, ödemelerin zamanında tahsil edildiğinden emin olmak için müşterilerle birlikte çalışır. Tahsilat temsilcileri, **Kullanıcı kurulumu** sayfasında kullanıcılara atanan çalışanlardır.

## <a name="collections-list-pages"></a>Tahsilat listesi sayfaları

Aşağıdaki liste sayfaları tahsilat bilgilerini düzenlemenize yardımcı olur:

- **Yaşlandırılmış bakiyeler** – Bu liste sayfasındaki sütunlar yaşlandırma dönemi için müşteri bakiyelerini ve yaşlandırılan tutarları gösterir. Bu bilgiler bir yaşlandırma anlık görüntüsünde depolanır. Yaşlandırma dönemleri, kullanılan yaşlandırma dönemi tanımı tarafından belirlenir. Havuz sorgusu için bir müşteri havuzu belirtildiyse, yaşlandırma dönemi tanımı, müşteri havuzundan alınır. Müşteri havuzunda bir yaşlandırma dönemi tanımı yoksa, **Alacak hesapları parametreleri** sayfasında belirtilmiş varsayılan yaşlandırma dönemi tanımı kullanılır. Hiçbir varsayılan yaşlandırma dönemi tanımı belirtilmemişse, **Yaşlandırma dönemi tanımları** sayfasındaki ilk yaşlandırma dönemi tanımı kullanılır.
- **Tahsilat faaliyetleri** - Bu liste sayfasındaki sütunlar tahsilat etkinlikleri olarak tanımlanan etkinlikleri gösterir. Bu faaliyetler **Tahsilatlar** sayfasında oluşturulur. Tahsilatlarla ilgili olarak yaptığınız işleri izlemek için bu faaliyetleri kullanın.
- **Tahsilat vakaları** – Bu liste sayfasındaki sütunlar, **Tahsilatlar** vaka türündeki bir vaka kategorisine ait vakalarla ilgili bilgileri gösterir.

### <a name="aging-snapshots"></a>Yaşlandırma anlık görüntüleri

Tahsilat listesi sayfalarında bilgileri görebilmeniz için yaşlandırma anlık görüntüsünün oluşturulmuş olması gerekir. Bilgiler yalnızca yaşlandırma anlık görüntüsü oluşturulan müşteriler için gösterilir. Liste sayfasında gösterilen kayıtlara aşağıdaki gibi daha fazla filtre uygulanabilir:

- Varsayılan olarak, kullanıcılar bir yaşlandırma anlık görüntüsü bulunan tüm müşterilere erişebilir.
- Müşteri havuzları varsa, tahsilat liste sayfalarındaki bilgilerin filtreleneceği havuzları kullanmak için kullanıcının tahsilat temsilcisi olarak ayarlanması gerekir. Bilgiler, seçili müşteri havuzuna dahil olan müşterilerle sınırlıdır.
- Bir kullanıcı tahsilat temsilcisi olarak ayarlanırsa, yalnızca bu tahsilat temsilcisi için seçilen havuzlar tahsilat listesi sayfalarında kullanılabilir. Tahsilat temsilcisi için **Tahsilatlar temsilcisi** sayfasında **Temsilcinin tüm müşteri havuzlarını görmesine izin ver** seçeneği belirlenirse, söz konusu temsilci tüm havuzları görebilir.

## <a name="collections-page"></a>Tahsilatlar sayfası

Bir müşteriye ilişkin tahsilat bilgileri, etkinlikleri ve vakaları görüntülemek, yönetmek ve işlem yapmak için **Tahsilatlar** sayfasını kullanabilirsiniz.

Sayfanın üst bölümü seçilen müşteriyle ilgili vakaları, ortadaki bölüm müşteri için hareketleri, alttaki bölüm ise müşteriye ilişkin faaliyetleri gösterilir. Bir veya daha fazla hareket ve etkinlikle ilgili tahsilat bilgilerini izlemek için tahsilat servis talepleri oluşturabilirsiniz. Üst ve alt bölümlerdeki bilgiler vakaya göre filtrelenebilir.

Bilgi kutuları seçili müşteriyle ilgili yaşlandırılmış bakiyeleri ve alacak limiti bilgilerini gösterir. Bu bilgiler yaşlandırma anlık görüntüsünde depolanır. Gereksinim duyarsanız, yaşlandırma anlık görüntüsünü geçerli bilgilerle güncelleştirebilirsiniz.

Eylem Bölmesi, seçili müşteri, vaka, hareket veya etkinlik için ilgili bilgileri görüntülemenizi sağlayan düğmeler içerir. Ayrıca, bir hareketin tahsilat durumunu değiştirme, e-posta sağlayıcınızla tümleştirme yaparak e-posta gönderme, müşterilere para iadesi yapma, NSF ödemelerini işleme koyma ve tahsil edilemeyen bakiyeleri silme gibi ortak işlemleri de gerçekleştirebilirsiniz.

## <a name="waiving-reinstating-or-reversing-interest-and-fees"></a>Faiz ve ücretlerden feragat etme, bunları eski durumuna getirme veya tersine çevirme

Vade farkı dekontlarından veya vade farkı notlarının bir parçası olan ücretler ve hareket faizinden feragat edebilir, bunları eski durumuna getirebilir veya tersine çevirebilirsiniz. **Tüm müşteriler** liste sayfasının eylem bölmesindeki **Tahsil et** sekmesinde **Vade farkı dekontu**, **Hareket vade farkı** veya **Ücret**'i seçebilirsiniz.

Bu ayarlamalar yalnızca vade farkı dekontlarını ve bunların içerdiği faiz ile ücretleri etkiler. Müşterinin borçlu olduğu tüm ücretlerin nasıl silineceği hakkında bilgi için, bu konunun [Silme hareketleri oluşturma](#creating-write-off-transactions) bölümüne bakın.

Daha fazla bilgi için bkz. Bir aralık ile bir faiz kodu oluştur ve Faizi işle.

## <a name="creating-write-off-transactions"></a>Silme hareketleri oluşturma

Ödenmeyen borçları **Tahsilatlar** sayfasında ve tahsilat listesi sayfalarında **Sil**'i seçerek silebilirsiniz.

Bir müşteri için hareketleri sildiğiniz zaman, o müşteriye ilişkin tüm hareketler otomatik olarak kapatma için işaretlenir. Silinen tutar, işaretlenen hareketlerin net tutarına bağlıdır. Silme hareketi yevmiye fişinde oluşturulur ve en fazla üç türde günlük satırı içerebilir:

- İlk günlük satırı türü müşteri silme girişini içerir. İşaretli hareketler birden fazla para birimi kodu, boyut ve deftere nakil profili birleşimleri içeriyorsa, her birleşim için ayrı bir günlük satırı oluşturulur.
- İkinci günlük satırı türü genel muhasebe silme girişini içerir. İşaretli hareketler birden fazla para birimi kodu, boyut ve deftere nakil profili birleşimleri içeriyorsa, her birleşim için ayrı bir günlük satırı oluşturulur.
- Üçüncü günlük satırı türü satış vergileri için genel muhasebe silme bilgileri içerir. Bu günlük satırı yalnızca **Alacak hesapları parametreleri** sayfasında **Ayrı satış vergisi** seçeneği belirlenirse oluşturulur. İşaretlenen hareketler birden fazla satış vergisi borç hesabı, boyut ve satış vergisi kodu birleşimleri içeriyorsa, her birleşim için ayrı bir günlük satırı oluşturulur. Silme hareketi hareket para birimi cinsinden oluşturulur. Daha fazla bilgi için bkz. Bir müşteri için bir silme günlüğü oluştur.

## <a name="process-nsf-payments"></a>NSF ödemelerini işleme

**Tahsilatlar** sayfasındaki **NSF ödemesi**'ni seçerek NSF ödemelerini işleyebilirsiniz. Bu düğmeyi seçtiğiniz zaman ödeme iptal edilir. Müşteriye NSF ücreti uygulanırsa, ödeme günlüğünde gider hareketi oluşturulur. Ücret tutarı, otomatik giderler ayarlarını temel alır. NSF ödemelerine uygulanan otomatik giderler, etkilenen banka hesabı için **Banka hesapları** sayfasında seçilen gider grubu tarafından belirlenir.

## <a name="additional-resources"></a>Ek kaynaklar

[Müşteri kredi yönetimi parametreleri kurulumu](./cm-credit-mgmt-setup.md)

[Müşteri kredi yönetimi kurulum bilgileri](./cm-setup-information.md)

[Müşteri için alacak yönetimi bilgileri ekleme](./cm-add-credit-mgmt-information-customer.md)

[Müşteri alacak grupları](./cm-customer-credit-groups.md)

[Müşteri kredi limiti ayarlamaları](./cm-credit-limit-adjustments.md)

[Satış siparişleri için askıda krediler](./cm-sales-order-credit-holds.md)

[Müşteri kredi yönetimi periyodik görevleri](./cm-periodic-tasks.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
