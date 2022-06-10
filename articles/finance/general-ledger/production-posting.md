---
title: Üretim emrini deftere nakletme
description: Bu konu, üretim emrini deftere nakletmenin farklı türleri hakkında bilgi sağlar.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup, ProdGroup, WrkCtrTable, WrkCtrResourceGroup, ProjCategory, CostSheetDesigner
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: cd1b6c49e59f9480fd831ad5ff143033ca09792c
ms.sourcegitcommit: 5b55f2913e736d12e40c227bf3ce3a9abec815bd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2022
ms.locfileid: "8803014"
---
# <a name="production-postings"></a>Üretim deftere nakilleri

Bu konu, üretim emri sürecindeki farklı deftere nakil türleri hakkında bilgi sağlar.


## <a name="material-consumption"></a>Malzeme tüketimi

Üretim malzeme çekme listesi defteri nakledildiğinde üretim sırasında malzemeler tüketildi olarak kaydedilir. Bu, eldeki stoğu azaltan hareketler oluşturur. **Üretim parametrelerinde**, kullanılmaya devam eden (süren iş) ham maddelerin değerinin deftere nakledilip nakledilmeyeceğini belirleyebilirsiniz.

Kullanılmaya devam eden ham maddelerin (süren iş) değeri, **Tüketilen malzemelerin tahmini maliyeti** ve **Tüketilen malzemelerin tahmini maliyeti, Süren İş** hesaplarına nakledilir. Üretim emri için malzeme çekme listesi işlemi, üretim emriyle ilgili stok hareketlerindeki fiziksel bir güncelleştirmedir. Bir üretim emri tamamlandı olarak kaydedildiğinde, fiziksel hareketler tersine çevrilir ve ilgili stok hareketleri mali olarak güncelleştirilir. Bitiş günlüğü nakledildiğinde **Tüketilen malzemelerin maliyeti** ve **Tüketilen malzemelerin maliyeti, Süren İş** deftere nakil türleri kullanılır.

**Stok deftere nakil profilleri** sayfasındaki **Üretim** sekmesi, üretim emirlerinin genel muhasebe defterine nasıl nakledileceğini denetler. Bu, **Üretim denetimi parametreleri** sayfasındaki **Genel muhasebe nakli** alanının **Madde ve kaynak** veya **Madde ve kategori** olarak ayarlandığı durumlarda kullanılır. 

Üretim emri için malzeme çekme listesi günlüğünün genel muhasebe defterine nakledilmesi için aşağıdaki koşulların karşılanması gerekir:

-   **Üretim denetimi parametreleri** sayfasında, **Malzeme çekme listesini deftere naklet** onay kutusunun işaretli olması gerekir. Bu ayar, **Tesise göre üretim denetimi parametreleri** sayfasında belirli bir tesis için geçersiz kılınabilir.
-   Satınalma siparişi satırındaki seçili madde için **Madde model grupları** sayfasındaki **Fiziksel stoğu deftere naklet** onay kutusunun seçilmiş olması gerekir.
-   Ana hesaplar **Stok deftere nakil profili** sayfasında aşağıdaki deftere nakil türleri için belirtilmelidir:
    -   **Tüketilen malzemelerin tahmini maliyeti**
    -   **Tüketilen malzemelerin tahmini maliyeti, Süren İş**

## <a name="time-consumption"></a>Zaman tüketimi

Üretim işlerinde çalışanların harcadıkları süre **Rota kartı günlüğü**'nde veya **İş kartı günlüğü**'nde kaydedilir. Bu günlükler nakledildiğinde, kullanılmaya devam eden (süren iş) kaynaklar için özel bir hesaba nakil yapan defter işleme alınır. Bu nakil işlemi, üretim emri için harcanan sürenin değerini temsil eder. Üretim emri sonlandırıldı olarak kaydedildiğinde WIP hesapları kapatılır.

**Üretim denetimi parametreleri** sayfasındaki **Genel muhasebe nakli** alanında belirlenen seçeneğe bağlı olarak harcanan süreyi deftere nakletmenin üç olası yöntemi bulunur.

## <a name="reporting-finished-goods-and-error-quantities"></a>Mamul malların ve hatalı miktarların raporlanması

Bir üretim emri **Tamamlandığı bildirildi** durumuna geçtiğinde, tamamlanan mamul mallar **Tamamlandı olarak raporla** günlüğü aracılığıyla stokta güncelleştirilir. Süren iş muhasebesini kullanıyorsanız, süren iş hesaplarını azaltmak ve mamul mal stoğunu artırmak için bir genel muhasebe günlüğü deftere nakledilir. Defter, ürün için tanımlanan standart maliyeti kullanır. **Üretim denetimi parametreleri** sayfasında **Tahmini maliyet fiyatını kullan** seçeneği işaretliyse, üretim emrindeki tahmini maliyet kullanılır.

Kullanılmaya devam eden ham maddelerin (süren iş) değeri, **Tahmini üretim maliyeti** ve **Tahmini üretim maliyeti, Süren İş** hesaplarına nakledilir. Üretim emri için **Tamamlandı olarak raporla** işlemi, üretim emriyle ilgili stok hareketlerindeki fiziksel bir güncelleştirmedir. Bir üretim emri tamamlandığında, fiziksel hareketler tersine çevrilir ve ilgili stok hareketleri mali olarak güncelleştirilir. Bitiş günlüğü nakledildiğinde **Üretim maliyeti** ve **Üretim maliyeti, Süren İş** deftere nakil türleri kullanılır.

**Stok deftere nakil profilleri** sayfasındaki **Üretim** sekmesi, üretim emirlerinin genel muhasebeye nasıl nakledileceğini denetlemek için kullanılır. Bu, **Üretim denetimi parametreleri** sayfasındaki **Genel muhasebe nakli** alanının **Madde ve kaynak** veya **Madde ve kategori** olarak ayarlandığı durumlarda kullanılır. **Üretim grupları** sayfasındaki **Genel Muhasebe - maddeler** hızlı sekmesi, alanın **Üretim grupları** olarak ayarlanması durumunda üretim emirleri için deftere nakili denetlemek amacıyla da kullanılabilir.

Üretim emri için **Tamamlandı olarak raporla** günlüğünün genel muhasebe defterine nakledilmesi için aşağıdaki koşulların karşılanması gerekir:
-   **Üretim denetimi parametreleri** sayfasında, **Tamamlandı bildirimini genel muhasebeye naklet** onay kutusunun işaretli olması gerekir. Bu ayar, **Tesise göre üretim denetimi parametreleri** sayfasında belirli bir tesis için geçersiz kılınabilir.
-   Satınalma siparişi satırındaki seçili madde için **Madde model grupları** sayfasındaki **Fiziksel stoğu deftere naklet** onay kutusunun seçilmiş olması gerekir.
-   Ana hesaplar **Stok deftere nakil profili** sayfasında aşağıdaki deftere nakil türleri için belirtilmelidir:
    -   **Tahmini üretim maliyeti**
    -   **Tahmini üretim maliyeti, Süren İş**

## <a name="ending-the-production-order"></a>Üretim emrinin sonlandırılması

Bir üretim emri sonlandırılmadan önce fiili maliyetler, üretilen miktar için hesaplanır. Tüm tahmini malzeme, işgücü giderleri ve genel giderler tersine çevrilir ve bunların yerine gerçek maliyetler konur. Mamul ürünün toplam maliyeti için **Üretim maliyeti** hesabı borçlandırılır ve **Üretim maliyeti, Süren İş** hesabı alacaklandırılır. Üretim emri sırasında tüketilen malzemeler için **Tüketilen malzemelerin maliyeti** hesabı alacaklandırılır ve **Malzemelerin maliyeti, Süren İş** hesabı borçlandırılır.

Maliyet hesabı yürütürken **İşi sonlandır** onay kutusunu işaretlerseniz üretim emrinin durumu **Sonlandırıldı** olarak değişir. Bu durum, tamamlanmış bir üretim emrine istemeden ek maliyetlerin nakledilmesini engeller. Bitti olarak rapor edilen hatalı miktarların değerinin bitti olarak rapor edilen doğru miktarlara tahsis edilmesi gerektiğini belirtebilirsiniz. Alternatif olarak, hatalı miktarların değerinin özel bir hurda hesabına nakledilmesi gerektiğini belirtebilirsiniz. 

Belirli bir hurda hesabı belirtmek için aşağıdaki adımları izleyin:
1.  **Üretim denetimi** > **Kurulum** > **Üretim denetimi parametreleri** öğesine gidin.
2.  **Standart güncelleştirme** sekmesini seçin.
3.  **Hurda yöntemi** alanında **Hurda hesabı**'nı seçin.
4.  **Hurda hesabı** alanında, üretim emri sona erdikten sonra hatalı miktar için hurdanın nakledileceği ana hesabı seçin. Örneğin, 510380: Üretim Iskartası gibi bir Gider hesabı seçin.

Üretim emri için bitiş günlüğünün genel muhasebe defterine nakledilmesi için aşağıdaki koşulların karşılanması gerekir:
-   Ana hesaplar **Stok deftere nakil profili** veya **Üretim grupları** sayfasında aşağıdaki deftere nakil türleri için belirtilmelidir:
    -   **Tüketilen malzemelerin maliyeti**
    -   **Tüketilen malzemelerin maliyeti, Süren İş**
    -   **Üretim maliyeti**
    -   **Üretim maliyeti, Süren İş**
-   Ana hesaplar, aşağıdaki türler için **Maliyet kategorileri**, **Kaynaklar** veya **Kaynak grupları** sayfasında belirtilmelidir.
    -   **Üretim maliyeti içe alındı**
    -   **Tüketilen üretim maliyeti, Süren İş**

## <a name="indirect-costs-for-production-orders"></a>Üretim emirleri için dolaylı maliyetler

Bir üretim emriyle ilgili hareketleri işlediğinizde, genel muhasebe defterinizdeki genel gider maliyetlerini veya ek ücretleri yakalamak için dolaylı maliyetleri yapılandırabilirsiniz. Malzeme çekme listesi günlüğünü veya tamamlandı bildirimi günlüğünü deftere naklettiğinizde dolaylı maliyetlerin fiziksel hareketleri stokta tanınır. Bitiş günlüğünü deftere naklettiğinizde, dolaylı maliyetlerin mali hareketleri stokta tanınır.

**Rota kartı** günlükleriyle veya **İş kartı** günlükleriyle ilişkili süre tüketiminiz için dolaylı maliyetleri tanıyabilirsiniz. Üretim emrini sonlandırdığınızda bu hareketler tersine çevrilir ve mali hesaplara nakledilir. Daha fazla bilgi için [Maliyetlendirme tabloları](/supply-chain/cost-management/costing-sheets.md) konusuna gidin.

## <a name="controlling-the-level-of-ledger-posting"></a>Defter nakil düzeyinin kontrol edilmesi

**Üretim kontrol parametreleri** sayfasında, üretim işlemleri için defter nakil düzeyini ayarlamak üzere **Genel muhasebe nakli** alanını kullanabilirsiniz. 

Aşağıdaki alanlar kullanılabilir:

### <a name="item-and-resource"></a>Madde ve kaynak

**Genel muhasebe nakli** alanında **Madde ve kaynak** seçeneğini belirlediğinizde, deftere nakil hesapları rotadaki işlemin kaynak veya kaynak grubundan gelir. Belirli bir kaynaktaki hesaplar ilk deftere nakil seçeneği olacaktır. Hesap belirtilmezse kaynak grubunda belirtilen hesaplar kullanılır. Bir rotadaki her operasyon satırının **Maliyetlendirme kaynağı** olarak belirtilen bir kaynağı olabilir. Bu kaynak kullanılacak hesabı belirlemede kullanılır. Bu seçenek genellikle bir kuruluşun kaynaklara işletim maliyetleri atadığı durumlarda kullanılır. Maliyetler, genellikle kaynaklar için daha yüksektir ve "üret veya satın al" kararları almanıza yardımcı olmak için kullanılır. Bu, en ayrıntılı deftere nakil yapılandırmasıdır ve deftere nakillere ilişkin en ayrıntılı denetimin yanı sıra üretim işlemlerine dair ayrıntılı analizler sunar.

### <a name="item-and-category"></a>Madde ve kategori

**Genel muhasebe nakli** alanında **Madde ve kategori** seçeneğini belirlediğinizde, deftere nakil hesapları rotadaki her satırla ilgili **Maliyet kategorisi** sayfasından gelir. Rotadaki her işlem satırının üç maliyet kategorisi olabilir: **Hazırlık** süresi, **Çalıştırma** süresi ve **Miktar**. Bu seçenek genellikle kuruluşunuzun ana odağı, işlem verimliliği ve etkinlik süresi olduğunda kullanılır. Bu seçenek, deftere nakil işleminin özet halidir yine de maliyetleri kategorilere ayırma yöntemi sunar.

### <a name="production-group"></a>Üretim Grubu

**Genel muhasebe nakli** alanındaki **Üretim grupları** seçeneğini belirlediğinizde, deftere nakil hesapları **Üretim grupları** sayfasından gelir. **Üretim grupları** genellikle, birden fazla üretim satırının benzer ürünleri çalıştırdığı veya benzer ekipmanlara sahip olduğu durumlarda kullanılır. İki farklı üretim grubu arasındaki maliyetleri karşılaştırmak için bu seçeneği kullanabilirsiniz.  
  
> [!NOTE]
> Mamul maddenin maliyetini hesaplamak için standart yöntem kullanılmışsa, nihai hareketler bu durumu yansıtır. Fiili maliyetler ve standart yöntemle hesaplanan maliyetler arasında fark oluşursa, bu farklar kar ya da zararı gösteren hesaba nakledilir.

### <a name="route-groups-and-ledger-posting"></a>Rota grupları ve genel muhasebe defterine nakil

Bir rotadaki her işlem satırının belirtilen bir **Rota grubu** bulunur. **Tahmin ve maliyetlendirme** grubunda yer alan **Rota grubu**'ndaki **Hazırlık süresi**, **Çalıştırma süresi** ve **Miktar** alanları, üretim emrinde bir **İş kartı** veya **Rota kartı günlüğü** deftere nakledilirken sürenin maliyetlendirme için kullanılıp kullanılmayacağını denetler. Seçenekler devre dışı bırakılmışsa, genel muhasebe defterinde süre tüketimi için fiş oluşturulmaz.

Üretim emri için **Rota kartı** veya **İş kartı günlüğünün** genel muhasebe defterine nakledilmesi için aşağıdaki koşulların karşılanması gerekir:

-   **Rota grubu** sayfasındaki **Tahmin ve maliyetlendirme** grubunda **Hazırlık süresi**, **Çalıştırma süresi** veya **Miktar** alanı seçilmelidir.
-   Ana hesaplar, **Maliyet kategorisi**, **Rota**, **Rota grubu** veya **Üretim grupları** sayfasında aşağıdaki deftere nakil türleri için belirtilmelidir:
    -   Mahsup edilen tahmini üretim maliyeti
    -   Tüketilen tahmini üretim maliyeti, Süren İş

Aşağıdaki diyagramda, belirli bir rotadaki rota grubunun her işlem (rota satırı) için toplam maliyet hesaplamasıyla ilişkisi gösterilmektedir. Her rota satırının bir rota grubu vardır. Rota grubu, hazırlık süresi, çalıştırma süresi ve miktar parametrelerini denetler. **Maliyet kategorisi** sekmesinde, **Hazırlık**, **Çalıştırma** ve **Miktar** için rota grupları ayarına göre etkinleştirilen üç seçenek bulunur. **Zamanlamalar** hızlı sekmesi, rota grubunu esas alan üç alana sahiptir.

Kullanılan formül, rota grubunda seçeneğin etkin olup olmamasına bağlıdır. Seçilen maliyet kategorisindeki maliyet, toplam maliyeti hesaplamak için zamanlamalarda girilen miktarla çarpılır.

:::image type="complex" source="media/RouteGroupRelationship.png" alt-text="Rota gruplarının toplam hesaplanan maliyetle ilişkisi.":::
Rota gruplarının toplam hesaplanan maliyetle ilişkisi. Her rota satırının bir rota grubu vardır. Rota grubu, hazırlık süresi, çalıştırma süresi ve miktar parametrelerini denetler. Maliyet kategorisi sekmesinde, Hazırlık, Çalıştırma ve Miktar için rota grupları ayarına göre etkinleştirilen üç seçenek bulunur. Zamanlamalar hızlı sekmesi, rota grubuna göre etkinleştirilen ve maliyetlendirilen üç alana sahiptir. Kullanılan formül, rota grubunda seçeneğin etkin olup olmamasına bağlıdır. Seçilen maliyet kategorisindeki maliyet, toplam maliyeti hesaplamak için zamanlamalarda girilen miktarla çarpılır.
:::image-end:::

## <a name="sample-posting-profile-configuration"></a>Örnek deftere nakil profili yapılandırması

Aşağıdaki tabloda örnek ana hesapları ve açıklamaları olan varsayılan deftere nakil türleri örnekleri gösterilmiştir. 

 - **Borç/Alacak** sütunu, hareketin genel olarak Borç veya Alacak olduğu ya da bazı durumlarda deftere nakledilebileceği anlamına gelir. 
 - **Kliring hesabı** sütunu, deftere nakil türünün bir kliring hesabı olduğunu belirtir. Sonraki bir hareket deftere nakledildiğinde, bu hesapta deftere nakledilen tutar için otomatik olarak ters işlem uygulanır. 
 - **P/F** sütunu fiziksel deftere nakil için **P** ve mali deftere nakil için **F**'yi belirtir. 
 - **İzle** sütunu, belirli bir deftere nakil türü ana hesabının genellikle başka bir deftere nakil türüyle aynı olup olmadığını gösterir. Sütundaki değer genellikle takip edilen deftere nakil türünü gösterir.

> [!NOTE]
> Önerilen ana hesaplar ve ana hesap adları yalnızca önerilerdir. İş gereksinimleriniz için en iyi yapılandırmayı belirlemek amacıyla muhasebeciniz ile çalışmanızı öneririz.


| Deftere nakil türü  | Temel hesap örneği | Temel hesap adı örneği| Hesap türü | Borç/Alacak? | Kliring hesabı | Fiziksel veya Mali | İzle | Açıklama |
|---------------|----------------------|--------------------------|--------------|----------------|------------------|-----------------------|--------|------------|
| Tüketilen malzemelerin tahmini maliyeti      | 140100               | Malzeme Stoğu        | Varlık        | Kredi         | Y                | P                     | Tüketilen malzemelerin maliyeti                | Bu hesap, bir üretim emri için malzeme çekme listesi günlüğünü deftere naklettiğinizde kullanılır. Bu hesaba mahsup, Malzemelerin tahmini maliyeti, Süren İş hesabıdır. Üretim emri sonlandırıldığında bu hesaptaki tutar için otomatik olarak ters işlem uygulanır. Bu hesap bilançodaki stok hesabını temsil eder.       |
| Tüketilen malzemelerin tahmini maliyeti, Süren İş | 150150               | Üretim süren iş - Malzemeler | Varlık        | Borç          | Y                | P                     | Tahmini üretim maliyeti, Süren İş          | Bu hesap, bir üretim emri için malzeme çekme listesi günlüğünü deftere naklettiğinizde kullanılır. Bu hesaba mahsup, Tüketilen malzemelerin tahmini maliyeti hesabıdır. Üretim emri sonlandırıldığında bu hesaptaki tutar için otomatik olarak ters işlem uygulanır. Bu hesap bilançonuzdaki süren işi temsil eder.                  |
| Tahmini üretim maliyeti               | 140200               | Mamul Mallar Stoğu   | Varlık        | Borç          | Y                | P                     | Üretim maliyeti                         | Bu hesap, bir üretim emri için tamamlandı bildirimi günlüğünü deftere naklettiğinizde kullanılır. Bu hesaba mahsup, Tahmini üretim maliyeti, Süren İş hesabıdır. Üretim emri sonlandırıldığında bu hesaptaki tutar için otomatik olarak ters işlem uygulanır. Bu hesap bilançodaki stok hesabını temsil eder. |
| Tahmini üretim maliyeti, Süren İş          | 150150               | Üretim süren iş - Malzemeler | Varlık        | Kredi         | Y                | P                     | Üretim maliyeti, Süren İş                    | Bu hesap, bir üretim emri için tamamlandı bildirimi günlüğünü deftere naklettiğinizde kullanılır. Bu hesaba mahsup, Tahmini üretim maliyeti hesabıdır. Üretim emri sonlandırıldığında bu hesaptaki tutar için otomatik olarak ters işlem uygulanır. Bu hesap bilançonuzdaki süren işi temsil eder.                     |
| Tüketilen malzemelerin maliyeti                | 140100               | Malzeme Stoğu        | Varlık        | Kredi         | N                 | C                     | Tüketilen malzemelerin tahmini maliyeti      | Bu hesap, sonlandırma işlemi sırasında üretim emrinde tüketilen malzemeleri tanımak için kullanılır. Bu hesaba mahsup, Tüketilen malzemelerin maliyeti, Süren İş hesabıdır.                                                                                                    |
| Tüketilen malzemelerin maliyeti, Süren İş           | 150150               | Üretim süren iş - Malzemeler | Varlık        | Borç          | N                 | C                     | Tüketilen malzemelerin tahmini maliyeti, Süren İş | Bu hesap, sonlandırma işlemi sırasında üretim emrinde tüketilen süren işteki malzemeleri tanımak için kullanılır. Bu hesaba mahsup, Tüketilen malzemelerin maliyeti hesabıdır.                                                |
| Üretim maliyeti                         | 140200               | Mamul Mallar Stoğu   | Varlık        | Borç          | N                 | C                     | Tahmini üretim maliyeti               | Bu hesap, üretim emrini sonlandırdığınızda üretim emri tarafından üretilen mamul malın maliyetini tanımak için kullanılır. Bu hesaba mahsup, Üretim maliyeti, Süren İş hesabıdır.                                                                  |
| Üretim maliyeti, Süren İş                    | 150150               | Üretim süren iş - Malzemeler | Varlık        | Kredi         | N                 | C                     | Tahmini üretim maliyeti, Süren İş          | Bu hesap, üretim emrini sonlandırdığınızda üretim emri tarafından üretilen süren işteki mamul malın maliyetini tanımak için kullanılır. Bu hesaba mahsup, Üretim maliyeti hesabıdır.                                     |

> [!NOTE]
> **Yalın hizmet süren iş girişi** ve **Yalın hizmet süren iş kliring hesabı**, yalın imalat için geriye dönük maliyetlendirmede kullanılır. Daha fazla bilgi için [Geriye dönük maliyetlendirme](/supply-chain/cost-management/backflush-costing.md) konusuna gidin.

