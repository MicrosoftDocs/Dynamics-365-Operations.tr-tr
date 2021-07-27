---
title: Ertelenen geliri kabul etme
description: Bu konuda, Gelir kabulü özelliğini kullanarak geliri kabul etme hakkında bilgiler verilir.
author: kweekley
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: cafe28e0aa71d623a728829ff1bf71bef5a132b0
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347212"
---
# <a name="recognize-deferred-revenue"></a>Ertelenen geliri kabul etme

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Gelir kabulü özelliği Özellik yönetiminden açılamaz. Şu anda, bu özelliği etkinleştirmek için yapılandırma anahtarları kullanmanız gerekir.

Bu konuda, gelir kabulü planında geliri kabul etme işlemi açıklanmaktadır. Bir faturanın satış siparişi için deftere nakledilmesinin ardından gelir planı olan her satış siparişi satırı için bir gelir kabulü planı oluşturulur. Satırın gelirinin ertelenip ertelenmesi gerektiğini belirlemek için satırdaki gelir planı kullanılır.

## <a name="view-revenue-recognition-schedule-details"></a>Gelir kabulü planı ayrıntılarını görüntüleme

Gelir kabulü planının ayrıntılarına erişmenin iki yolu vardır.

- Gelir kabulü planını, doğrudan bir faturalanan satış siparişinden açabilirsiniz. Bu durumda, gelir planındaki bilgiler yalnızca seçilen satış siparişi için ayrıntıları gösterecek şekilde filtrelenir. Bu yaklaşım, bir satış siparişinin plan ayrıntılarını doğrularken yararlıdır.
- Gelir kabulü planını **Gelir kabulü \> Periyodik görevler** sayfasından açabilirsiniz. Bu yaklaşım genellikle bir dönemin sonunda gelir kabul edildiğinde kullanılır. Sayfa ilk açıldığında hiçbir bilgi gösterilmez. Gösterilmesi gereken plan ayrıntıları için ölçüt tanımlamak üzere kılavuzun üzerindeki filtreleri kullanın. Tarih aralığı, satış siparişi, müşteri, proje kodu veya durum girerek fatura tarihlerine filtre uygulayabilirsiniz.

[![Gelir planları sayfasının resmi.](./media/revenue-recognition-schedule-page.png)](./media/revenue-recognition-schedule-page.png)

Kılavuzun altındaki **Mali boyut** hızlı sekmesi, satış siparişi satırının mali boyutlarını gösterir. Bu boyutlar, ertelenen gelir için deftere nakil işlemi sırasında dikkate alınmıştır. Gelir kabul edildiğinde de dikkate alınırlar. Kullanılan boyut değerleri, gelire atanan hesap yapısına ve ertelenen gelir ana hesaplarına bağlıdır.

## <a name="recognize-revenue"></a>Geliri kabul etme

**Geliri kabul etme** sayfasından **Günlük oluştur** işlemini çalıştırarak geliri kabul edersiniz. Bu sayfayı satış siparişi veya **Periyodik görevler**'den açabilirsiniz. İşlem satış siparişinden çalıştırılırsa gelir yalnızca seçilen satış siparişi için kabul edilir. Genellikle bunun yerine işlem, gelir nakledilen tüm satış siparişi faturaları için kabul edilecek şekilde **Periyodik görevler**'den çalıştırılır.

Gelir seçme ve deftere nakletme amacıyla ölçüt tanımlamak üzere **Günlük oluştur** iletişim kutusunu açmak için **Günlük oluştur**'u seçin.

[![Günlük parametre seçenekleri oluşturma.](./media/revenue-recognition-create-journal.png)](./media/revenue-recognition-create-journal.png)

İletişim kutusunda, gelir kabul edildiğinde kullanılan deftere nakil tarihini tanımlamak için **İşlem tarihi** alan grubundaki seçenekleri kullanın. **Seçilen tarih**'i belirlerseniz **Hareket tarihi** alanına deftere nakil tarihi girebilirsiniz. **Gelir planı tarihi**'ni seçerseniz hareket tarihi kullanılmaz. Bunun yerine, planın her satırında **Kabul etme tarihi** alanının değerleri deftere nakil tarihi olarak kullanılır.

Ardından, **Baz alınacak tarih** alanında gelir kabulü için "baz alınacak" tarihi girin. Kabul etme tarihinin "baz alınacak" tarihte veya öncesinde olduğu plan satırları, beklemede olmadıkları sürece kabul edilir.

Tarihleri tanımladıktan sonra günlük oluşturmak için iletişim kutusunda **Tamam**'ı seçin. Oluşturulan hareketlerin sayısını ve oluşturuldukları günlüğü gösteren bir bilgilendirme iletisi alırsınız. Günlük otomatik olarak deftere nakledilmez. Bu nedenle, gelir kabulü yöneticisinin hangi plan satırlarının kabul edildiğini doğrulamak için zamanı vardır.

İşlemin çalıştırıldıktan sonra planda günlüğe aktarılan satırlar **İşlendi** olarak işaretlenir. **İşlendi** bayrağı, satırların günlüğe aktarıldığını gösterir ancak deftere nakledilebilirler veya nakledilemezler. Gelir kabulü günlüğü deftere nakledildikten sonra **İşlendi** bayrağı kalır. Gelir kabulü günlüğü silinirse veya bir satır silinirse **İşlendi** bayrağı kaldırılır. Bu şekilde, **Günlük oluştur** işlemi yeniden çalıştırıldığında satır kabul edilebilir.

[![Gelir kabulü planı sayfası.](./media/revenue-recognition-rev-recog-schedule-02.png)](./media/revenue-recognition-rev-recog-schedule-02.png)

Kabul edilenlerin ayrıntılarını görüntülemek için **Gelir kabulü günlüğü** sayfasında (**Gelir kabulü \> Günlük girişleri \> Gelir kabulü günlüğü**) **Satırlar**'ı açın. Aynı genel muhasebe hesapları kullanılarak tüm satırlar aynı tarihte deftere nakledilse bile kabul edilen her plan satırı için her zaman ayrı bir hareket oluşturulur.

[![Günlük fişi sayfası.](./media/revenue-recognition-journal-voucher.png)](./media/revenue-recognition-journal-voucher.png)

**Hesap** sütunu, ertelenen gelir genel muhasebe hesabını gösterir. Bu genel muhasebe hesabı düzenlenemez. Bu sınırlama, doğru ertelenen gelir muhasebe hesabının serbest bırakılmasını sağlamaya yardımcı olur. Bu genel muhasebe hesabı, başvurulan gelir genel muhasebe hesabına nakil işleminin son gerçekleşmesinden sonra değişmiş olabileceğinden hesap yapısına göre doğrulanmaz.

**Mahsup hesap** sütunu, gelir genel muhasebe hesabını gösterir. Varsayılan olarak gelir genel muhasebe hesabı, Stok deftere nakil profillerinden alınır ve mali boyutlar, satış siparişi satırından alınır. Bu genel muhasebe hesabı, geçerli hesap yapısına göre doğrulanır. Ancak hesap yapısı değişirse ve ek mali boyutlar gerekirse düzenlenebilir.

Varsayılan tutar, planın ilgili satırından alınır ve değiştirilemez.

Varsayılan olarak, satış siparişi birden fazla para birimli bir satış siparişiyse döviz kuru, faturadaki döviz kuru olarak ayarlanır. Bu davranış, muhasebe para birimi ve raporlama para birimi tutarlarının tamamen serbest bırakılmasını sağlamaya yardımcı olur. Yuvarlama nedeniyle, planın son satırındaki döviz kuru, faturadaki kurdan biraz farklı olabilir.

Gelir kabulü günlüğü deftere nakledildikten sonra fiş, plana girilir. Planın aynı satırı için birden fazla fiş varsa satırda bir yıldız işareti (\*) görünür. Bu satır için deftere nakledilen fişleri görüntülemek üzere **Fiş hareketleri**'ni seçin.

## <a name="modify-the-revenue-recognition-schedule-details"></a>Gelir kabulü planı ayrıntılarını değiştirme

Gelir planı ayrıntılarındaki verilerin çoğu düzenlenemez. Plana yeni satırlar eklenemez ve mevcut satırlar silinemez. Zaman içinde bir kuruluşun ertelenen aynı tutarı kabul etmesini sağlamaya yardımcı olmak için tüm satış siparişi satırlarının gelir planı ayrıntıları korunmalıdır.

### <a name="edit-schedule-lines"></a>Plan satırlarını düzenleme

Planın satırlarında bazı düzenlemelere izin verilir. Satırlarda aşağıdaki alanlar değiştirilebilir:

- **Beklemede**: Bu bayrak, satırın işlenmesinden önce ayarlanabilir veya temizlenebilir. Bayrağı temizlemek için satırı seçin ve ardından **Beklemeyi kaldır** seçeneğini belirleyin. Gelir, beklemede olan satırlarda kabul edilemez. Gelir planı otomatik beklemeler için ayarlanırsa satırlar otomatik olarak beklemeye alınabilir.

    [![Gelir planları: plan satırlarını düzenleme.](./media/revenue-recognition-rev-revenue-schedules.png)](./media/revenue-recognition-rev-revenue-schedules.png)

- **Kabul etme tarihi**: Kabul etme tarihi, satırın işlenmesinden önce değiştirilebilir. Geliri kabul etmek için günlüğü oluşturan işlem çalıştırıldığında **Geliri kabul etmede baz alınacak tarih** alanına bir tarih girilir. Bu tarih, hangi satırların kabul edilmesi gerektiğini belirlemek için **Kabul etme tarihi** alanındaki tarihle karşılaştırılır.
- **Serbest bırakılacak tutar**: Serbest bırakılacak tutar, satır işlenmeden önce değiştirilebilir. Kabul edilen gelir tutarını azaltabilirsiniz ancak artıramazsınız. Bu alan, kuruluşun kabul etme tarihinde gelirin bir kısmını kabul etmesine olanak tanır. Tutar değiştirilirse **Kalan tutar** alanındaki tutar, daha ne kadar gelirin kabul edilmesi gerektiğini gösterir.
- **Serbest bırakılacak miktar**: Gelir planı bir tekrar veya bir ay için ayarlanırsa **Serbest bırakılacak miktar** alanı, satış siparişi satırının miktarını gösterir. Bu alan da düzenlenebilir ve gelirin bir kısmını kabul etmenin başka bir yolunu sunar. Örneğin, satırdaki miktar 5 ise miktarı 5'ten az olacak şekilde geçersiz kılabilirsiniz. **Serbest bırakılacak tutar** alanındaki miktar, oransal olarak güncelleştirilir.

### <a name="update-contract-terms"></a>Sözleşme şartlarını güncelleştirme

Gelir planı ayrıntıları, fatura deftere nakledildiğinde satış siparişi satırına atanan gelir planına göre oluşturulur. Satış siparişi satırındaki gelir planı yanlışsa bu plan, satış siparişi faturalandıktan sonra satış siparişinde değiştirilemez. Bunun yerine, gelir planını değiştirmek için **Sözleşme şartlarını güncelleştir** düğmesini kullanmanız gerekir. Gelir planı, gelirin kabul edilmesinden önce veya sonra değiştirilebilir.

Planı değiştirmek üzere değiştireceğiniz madde için bir plan satırı seçin. Aşağıdaki resimde, 12 aylık gelir planı kullanılarak deftere nakledilen S0008 maddesi için satır seçilir. **Sözleşme şartlarını güncelleştir**'i seçtiğinizde bir iletişim kutusu, sözleşme başlangıç ve bitiş tarihleriyle gelir planını gösterir.

[![Sözleşme başlangıç ve bitiş tarihleri.](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule.png)](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule.png)

Sözleşme başlangıç ve bitiş tarihlerini, doğru tarih aralığını yansıtacak şekilde değiştirin. Tarih aralığını değiştirdiğinizde **Tekrar sayısı** alanındaki değerin sistemde tanımlanmış bir gelir planıyla eşleşmesi gerekir. Bu örnekte, sözleşme 24 aylık sözleşme olarak değiştirildiğinden 24 aylık gelir planı ayarlanmalıdır. 24 aylık gelir planı mevcut olduğundan varsayılan olarak girilir ve sözleşme değiştirilebilir. Eşleşen sayıda tekrar içeren bir gelir planı yoksa sözleşme değiştirilemez. Sözleşme şartlarını ve gelir planını gerektiği şekilde güncelleştirdikten sonra değişikliklerinizi kaydetmek için iletişim kutusunda **Tamam**'ı seçin.

[![Güncelleştirilmiş sözleşme tarih aralığı.](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule-02.png)](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule-02.png)

Sözleşme değişiklikleri, gelir planı ayrıntıları üzerinde aşağıdaki etkilere sahiptir:

- Ürün için gelir kabul edilmezse önceki tüm plan ayrıntıları kaldırılır ve yeni gelir planı ayrıntılarıyla değiştirilir. Örneğin, başlangıçta S0008 maddesi, plan ayrıntılarında 12 satıra sahipti. Bu 12 satır kaldırılır ve yeni gelir planına göre 24 satırla değiştirilir.
- Ürün için gelir kabul edilirse kabulün yanlış gelir planına göre yapılmasından dolayı bazı gelirler yanlış şekilde kabul edilir. Bu satırlar, tersine çevrilmeli ve yeni plana göre yeniden kabul edilmelidir. Bu senaryoda yeni gelir planı satırları, orijinal kabul etme tarihinde negatif tutarları olacak şekilde oluşturulur. Ardından tutarlar yeni gelir planına göre kabul edilecek şekilde yeni satırlar oluşturulur. Örneğin, 8 Ağustos 2019 tarihinde 10,53 Amerikan doları geliri kabul ettiniz. 8 Eylül 2019 tarihinde de 13,16 Amerikan doları geliri kabul ettiniz. Bu nedenle, aynı tarihlerde iki yeni satır oluşturulur. Bir satır -10,53 Amerikan doları ve diğer satır -13,16 Amerikan doları olur. Ardından yirmi dört yeni satır oluşturulur ve 160,61 Amerikan doları toplam ertelenen gelir bunlar arasında tahsis edilir. **Günlük oluştur** işlemini çalıştırarak ters işlem satırlarını deftere nakledebilirsiniz.

[![Gelir kabulü planı.](./media/revenue-recognition-rev-recog-schedule-03.png)](./media/revenue-recognition-rev-recog-schedule-03.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]