---
title: Gelir kabulü yeniden tahsisatı
description: Bu konu başlığında, kuruluşların sözleşmeden doğan satış koşulları değiştirildiğinde gelir fiyatlarını yeniden hesaplamasına olanak tanıyan yeniden tahsisat hakkında bilgi sağlanmaktadır. Birden çok senaryoda gelir kabulünün nasıl gerçekleştiğini açıklayan diğer konu başlıklarına bağlantılar içermektedir.
author: kweekley
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2d961cb4eedda6265b4acd8dbd6f82e8026373fa
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820581"
---
# <a name="revenue-recognition-reallocation"></a>Gelir kabulü yeniden tahsisatı

[!include [banner](../includes/banner.md)]

Yeniden tahsisat, kuruluşların sözleşmeden doğan satış koşulları değiştirildiğinde gelir fiyatlarını yeniden hesaplamasına olanak tanır. Gelir kabulü açısından satış siparişi belgeleri sözleşme olarak kabul edilir.

Kuruluşunuz, yeniden tahsisatın gerekli olup olmadığını kendisi belirlemelidir. Satış siparişine yeni bir satır eklenmesi veya müşteri için yeni bir satış siparişinin eklenmesi sözleşmede bir değişiklik teşkil etmeyebilir. Aşağıdaki senaryolar yeniden tahsisat gerektirebilir:

- Müşterinin, sipariş tamamen veya kısmen faturalandıktan sonra satış siparişine madde eklemesi veya maddeleri satış siparişinden kaldırması.
- Üzerinde anlaşmaya varılan aynı sözleşme için onaylandı veya faturalandı durumunda birden çok satış siparişi girilmesi.
- Müşterinin özgün satış siparişi tamamen veya kısmen faturalandıktan sonra bir madde için kredi iade etmesi veya alması.

Yeniden tahsisat işlemiyle ilgili birkaç önemli sınırlama vardır:

- İşlem yalnızca bir kez çalıştırılabilir. Bu nedenle, yalnızca tüm değişiklikler sonuçlandıktan sonra çalıştırmanız önemlidir.
- İşlem, proje satış siparişlerinde çalıştırılamaz.
- Birden çok satış siparişi söz konusuysa bu siparişler aynı müşteri hesabına ait olmalıdır.
- Yeniden tahsis edilen tüm satış siparişleri aynı hareket para biriminde olmalıdır.
- İşlem çalıştırıldıktan sonra tersine çevrilemez veya geri alınamaz.

## <a name="set-up-reallocation"></a>Yeniden tahsisatı ayarlama

Yeniden tahsisat işlemini bir parametre etkiler.

Yeniden tahsisat kısmen veya tamamen faturalanmış satış siparişlerinde yapılabileceğinden, faturaya yönelik önceki muhasebe girişlerinin yeni, yeniden tahsis edilmiş gelir fiyatları kullanılarak düzeltilmesi gerekir. Bu düzeltme, özgün faturanın muhasebe girişi tersine çevrilerek ve yeniden tahsis edilen gelir fiyatlarına göre yeni bir muhasebe girişi deftere nakledilerek yapılır.

Her kuruluş, düzeltmenin yalnızca genel muhasebeyi mi güncelleştireceğine, yoksa alacak hesaplarını da güncelleştirip güncellemeyeceğine karar vermelidir. Verilen karar, **Genel muhasebe parametreleri** (**Gelir kabulü \> Kurulum \> Genel muhasebe parametreleri**) sayfasının **Gelir kabulü** sekmesindeki **Fatura düzeltmelerini Alacak hesaplarına deftere naklet** seçeneğinin doğru ayarını belirler. Uygun ayar senaryoya bağlıdır. Olası senaryolar hakkında daha fazla bilgi için bu konu başlığının ilerleyen bölümlerinde yer alan [Yeniden tahsis için senaryolar](#scenarios-for-reallocation) bölümündeki bağlantıları kullanın.

[![Genel muhasebe parametreleri sayfasındaki Gelir kabulü sekmesi](./media/01_RevRecScenarios.png)](./media/01_RevRecScenarios.png)

**Fatura düzeltmelerini Alacak hesaplarına deftere naklet** seçeneği **Evet** olarak ayarlanırsa yeniden tahsisat işlemi aşağıdaki sonucu üretir:

- Düzeltme gerektiren faturayı tersine çevirmek için Alacak hesaplarında bir alacak belgesi oluşturulur.

    - Alacak belgesi özgün fatura numarasını yeniden kullanır ancak sonuna "-1" eklenir.
    - Alacak belgesi özgün faturaya göre otomatik olarak kapatılır. Özgün fatura zaten başka bir alacak belgesi veya ödemeyle kapatılırsa bu kapatma işlemi otomatik olarak tersine çevrilir.
    - Alacak belgesi, özgün faturada deftere nakledilen muhasebe girişini tersine çevirmek için Genel muhasebeye nakledilir. Ancak, Stok ve Satılan malların maliyeti (COGS) hareketi girişleri geri alınmaz.

- Alacak hesaplarında yeni, yeniden tahsis edilmiş fiyat tutarlarını temel alan yeni bir fatura oluşturulur.

    - Yeni fatura özgün fatura numarasını yeniden kullanır ancak sonuna "-2" eklenir.
    - Yeni fatura, daha önce özgün faturayla kapatılan alacak belgesine veya ödemeye göre otomatik olarak kapatılır.
    - Yeni fatura; yeni, yeniden tahsis edilmiş gelir fiyatı tutarları kullanılarak Genel muhasebeye nakledilir. Bu girişler özgün faturanın muhasebe girişinde tutulduğu için Stok ve COGS hesaplarına yeniden deftere nakledilmez.

**Fatura düzeltmelerini Alacak hesaplarına deftere naklet** seçeneği **Hayır** olarak ayarlanırsa yeniden tahsisat işlemi aşağıdaki sonucu üretir:

- Tersine çeviren bir muhasebe girişi yalnızca Genel muhasebeye nakledilir. Stok ve COGS hesap girişleri hariç olmak üzere özgün faturadaki tüm muhasebe girişleri tersine çevrilir.
- Yeni muhasebe girişi; yeni, yeniden tahsis edilmiş gelir fiyatlarına bağlı olarak yalnızca Genel muhasebeye nakledilir. Bu girişler özgün faturanın muhasebe girişinde tutulduğu için Stok ve COGS hesaplarına yeniden deftere nakledilmez.
- **Müşteri hareketleri** sayfasındaki fatura etkilenmez veya değiştirilmez ancak yine de özgün muhasebe girişini yansıtır. Ters veya yeni muhasebe girişlerine referans bulunmaz.

Belirtildiği gibi, yalnızca Genel muhasebeyi veya hem Genel muhasebeyi hem de Alacak hesaplarını güncelleştirebilirsiniz. Her iki yaklaşımın da artıları ve eksileri vardır. Hangi seçeneği kullanmanız gerektiğini belirlemek için kuruluşunuzun gereksinimlerini değerlendirmenizi öneririz. Hem Genel muhasebeyi hem de Alacak hesaplarını güncelleştirirseniz yeni faturada doğru muhasebe girişleri gösterilir ve **Müşteri hareketleri** sayfasındaki belgeden görüntülenebilir. Ayrıca kapatma işlemi, nakit iskontolarını ve kazançları veya zararları deftere nakletmek için güncelleştirilmiş muhasebe girişlerini kullanır. Diğer taraftan, alacak belgesi ve yeni fatura, diğer alacak belgeleri ve müşteri faturaları gibi müşteri ekstrelerinde ve yaşlandırma raporlarında görünür. Bu belgelerin açıklaması, bunların bir muhasebe düzeltmesi yoluyla oluşturulduğunu gösterir.

## <a name="run-the-reallocation-process"></a>Yeniden tahsisat işlemini çalıştırma

Yeniden tahsisat işlemini başlatmak için yeniden tahsis etmeniz gereken tüm satış siparişlerinde **Fiyatı yeni sipariş satırlarıyla yeniden tahsis et**'i seçin. Alternatif olarak **Gelir tanıma \> Periyodik görevler \> Fiyatı yeni sipariş satırlarıyla yeniden tahsis et**'e gidin ve ardından müşteri hesabı gibi uygun filtreleri girin.

[![Fiyatı yeni sipariş satırlarıyla yeniden tahsis et sayfası](./media/02_RevRecScenarios.png)](./media/02_RevRecScenarios.png)

**Fiyatı yeni sipariş satırlarıyla yeniden tahsis et** sayfasının üst kılavuzu **Satış** olarak adlandırılır. Müşterinin satış siparişlerini listeler. Yeniden tahsis edilmesi gereken satış siparişlerini seçin. Proje satış siparişleri yeniden tahsis edilemediği için proje satış siparişlerini seçemezsiniz. Proje harici satış siparişleri yalnızca bir kez yeniden tahsis edilebildiği için zaten yeniden tahsisat kimliği olan satış siparişlerini de seçemezsiniz. Yeniden tahsisat kimliği olan satış siparişleri başka bir kullanıcı tarafından yeniden tahsisat için işaretlenmiştir.

Sayfadaki alt ızgara **Satırlar** olarak adlandırılır. **Satış** kılavuzunda bir veya daha fazla satış siparişi seçtikten sonra, **Satırlar** kılavuzu satış sipariş satırlarını gösterir. Yeniden tahsis edilmesi gereken satış sipariş satırlarını seçin. Yalnızca bir satış siparişi seçtiyseniz aynı satış siparişindeki satırların yeniden tahsis edilmesi gerekir. Bu durum, satış sipariş satırlarından biri daha önce faturalandığında ve sonra yeni bir satır eklendiğinde veya var olan bir satır kaldırıldığında ya da iptal edildiğinde oluşabilir. Bir satır kaldırıldıysa kılavuzda görünmez. Bu nedenle, seçilemez. Ancak, yeniden tahsisat işlemi çalıştırıldığında yine de dikkate alınır.

Gerekli satış sipariş satırlarını seçtikten sonra, burada açıklandığı gibi Eylem Bölmesindeki düğmeleri kullanın:

- **Yeniden tahsisatı güncelleştir**: Seçili satış sipariş satırlarının yeni gelir fiyatı tutarlarını hesaplayın. Bir satır kaldırıldıysa veya iptal edildiyse yalnızca seçtiğiniz mevcut satırlar için yeniden tahsisat yapılır. Aşağıdaki resimde, yeniden tahsisat güncelleştirilmeden önce satış sipariş satırlarının nasıl göründüğüne dair bir örnek gösterilmektedir.

    [![Yeniden tahsisat güncelleştirilmeden önce satış sipariş satırları](./media/03_RevRecScenarios.png)](./media/03_RevRecScenarios.png)

    Yeni gelir fiyatı tutarları, **Satırlar** kılavuzundaki **Yeniden tahsis edilen tutar** sütununda gösterilir. Bu noktada, yeniden tahsisat işlenmiştir ancak henüz hesaplanmamıştır. Aşağıdaki resimde, yeniden tahsisat güncelleştirildikten sonra satış sipariş satırlarının nasıl göründüğüne dair bir örnek gösterilmektedir.

    [![Yeniden tahsisat güncelleştirildikten sonra satış sipariş satırları](./media/04_RevRecScenarios.png)](./media/04_RevRecScenarios.png)

- **İşlem**: Yeniden tahsis edilen gelir fiyatlarını işleme veya deftere nakletme. Bu düğmeyi seçtikten sonra, yeniden tahsisatı tersine çevirmenin bir yolu yoktur. **İşlem**'i seçmeden önce **Yeniden tahsisatı güncelleştir**'i seçmediyseniz yeniden tahsisat otomatik olarak çalıştırılır.

    - Hiçbir satış sipariş satırı faturalanmadıysa gelir fiyatı tutarları yeniden tahsisat için seçilen satış siparişlerinde güncelleştirilir.
    - Bir veya daha fazla satış sipariş satırı faturalandıysa düzeltilen muhasebe girişleri deftere nakledilir ve faturalanan satış sipariş satırı için oluşturulan gelir çizelgesi ayrıntıları düzeltilir.

- **Beklenen fiş**: Faturalanan tüm satış sipariş satırları için oluşturulan muhasebe girişlerinin önizlemesini gösterir. Hiçbir satır faturalanmadıysa hiçbir şey gösterilmez. **Beklenen fiş**'i seçmeden önce **Yeniden tahsisatı güncelleştir**'i seçmediyseniz yeniden tahsisat otomatik olarak çalıştırılır.
- **Gelir tahsisi**: Seçilen tüm satırlar için gelir fiyatı tahsisatını gösteren bir sayfa açar. Sayfadaki bilgilerin hiçbirini değiştiremezsiniz. Yeniden tahsisat yapmak için kullanılan satır tutarlarını gösterir.

    [![Yeniden tahsisat için kullanılan satır tutarları](./media/05_RevRecScenarios.png)](./media/05_RevRecScenarios.png)

- **Seçilen müşteri için verileri sıfırla**: Yeniden tahsisat işlemi başlatılıp tamamlanmadıysa yalnızca seçilen müşteri için yeniden tahsisat tablosundaki verileri temizleyin. Örneğin, yeniden tahsisat için birden çok satış sipariş satırı işaretlersiniz **İşlem**'i seçmeden sayfayı açık bırakır ve sayfa zaman aşımına uğrar. Bu durumda, satış sipariş satırları işaretli olarak kalır ve başka bir kullanıcı tarafından yeniden tahsisat işlemini tamamlamak için kullanılamaz. Sayfa açıldığında boş olabilir. Bu durumda, başka bir kullanıcının yeniden tahsisat işlemini tamamlayabilmesi için **Seçilen müşteri için verileri sıfırla** düğmesi kullanılarak işlenmemiş satış siparişleri temizlenebilir.

## <a name="scenarios-for-reallocation"></a>Yeniden tahsisat için senaryolar

Aşağıdaki konu başlıklarında gelir kabulü için çeşitli senaryolar ele alınmaktadır:

- [Gelir kabulü yeniden tahsisatı - Senaryo 1](rev-rec-reallocation-scenario-1.md): İki satış siparişi girilir ancak yalnızca onaylanır. İkiden fazla satış siparişi onaylanmış durumdaysa aynı senaryo benzer sonuçlar doğurur.
- [Gelir kabulü yeniden tahsisatı - Senaryo 2](rev-rec-reallocation-scenario-2.md): İki satış siparişi girilir ve ardından müşteri ilk satış siparişi faturalandıktan sonra sözleşmeye bir madde ekler.
- [Gelir kabulü yeniden tahsisatı - Senaryo 3](rev-rec-reallocation-scenario-3.md): Mevcut, faturalanan bir satış siparişine yeni bir satır eklenir.
- [Gelir kabulü yeniden tahsisatı - Senaryo 4](rev-rec-reallocation-scenario-4.md): Mevcut, kısmen faturalanan satış siparişinden bir satır kaldırılır.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]