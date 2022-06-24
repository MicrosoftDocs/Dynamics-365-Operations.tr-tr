---
title: Fazla/eksik hareketleri
description: Bu makale, sistemin alındıktan sonra malların aşırı işlenmesini ve eksik işlenmesini nasıl yöneteceğini belirleyebilmesi için fazla/eksik hareketleri için ilkelerin ayrıntılarını ayarlamanıza yardımcı olacak bilgiler sağlar.
author: Weijiesa
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMOverUnderTrans, ITMOverUnderToleranceTable, ITMOverUnderReasonTable, ITMOverUnderToleranceGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 79ce18a462f9c2f93dceec82da7ee0209ab61f78
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845011"
---
# <a name="overunder-transactions"></a>Fazla/eksik hareketleri

[!include [banner](../../includes/banner.md)]

Bir seyahatteki siparişler işlendiğinde, sistem tüketim için son hedef ambarda alınan madde miktarının, seyahatle ilişkili satın alma siparişi satırlarında belirtilen miktarla eşleşmesini bekler. Ancak satın alma siparişi satırlarındaki tam miktar her zaman ambarda alınmadığı için **Varış yeri maliyeti** modülü, malların fazla ve eksik teslim alınmasını işlemek için kullanılan bir kurallar kümesi tanımlar. Orijinal satın alma siparişi faturalandığı ve artık değiştirilemediği için bu kurallar özellikle önemlidir. Fazla/eksik hareketi ilkelerinin ayrıntılarını ayarlayarak sistemin malların giriş anında fazla işlenmesini ve eksik işlenmesini nasıl yöneteceğini belirlemesini sağlarsınız. Ayrıca, **Fazla/eksik hareketleri** sayfasını kullanarak fazla ve eksik stoku el ile yönetebilirsiniz.

## <a name="overunder-tolerances"></a>Fazla/eksik toleransları

Bir hataya neden olmadan bir seyahatte işlenebilecek fazla ve eksik miktarları veya hacimleri belirtmek için fazla teslimat ve eksik teslimat toleransları ayarlarsınız. Seyahat satırı girişi bu toleransların dışındaysa daha fazla işlem için seyahat satırı kapatılmadan önce değiştirilmesi ve çözümlenmesi gerekir.

Toleransları yapılandırmak için **Varış yeri maliyeti \> Fazla/eksik kurulumu \> Fazla/eksik toleransları**'na gidin. Burada tolerans kayıtlarını görüntüleyebilir, düzenleyebilir, ekleyebilir ve kaldırabilirsiniz. Aşağıdaki tabloda, her kayıtta kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Hesap kodu | <p>Aşağıdaki değerlerden birini seçerek toleransın uygulanacağı satıcıların kapsamını tanımlayın:</p><ul><li>**Tablo**: Fazla/eksik toleransı yalnızca satır için seçilen satıcı için geçerlidir.</li><li>**Grup**: Fazla/eksik toleransı, satır için seçilen satıcı tolerans grubundaki tüm satıcılar için geçerlidir.</li><li>**Tümü**: Fazla/eksik toleransı tüm satıcılar için geçerlidir.</li></ul> |
| Hesap ilişkisi | **Hesap kodu** alanında seçtiğiniz değere bağlı olarak fazla/eksik toleransın uygulandığı satıcı veya satıcı grubunu seçin. |
| Madde kodu | <p>Aşağıdaki değerlerden birini seçerek toleransın uygulanacağı maddelerin kapsamını tanımlayın:</p><ul><li>**Tablo**: Fazla/eksik toleransı yalnızca satır için seçilen madde için geçerlidir.</li><li>**Grup**: Fazla/eksik toleransı, satır için seçilen madde tolerans grubundaki tüm maddeler için geçerlidir.</li><li>**Tümü**: Fazla/eksik toleransı tüm maddeler için geçerlidir.</li></ul> |
| Madde ilişkisi | **Madde kodu** alanında seçtiğiniz değere bağlı olarak fazla/eksik toleransın uygulandığı madde veya madde grubunu seçin. |
| Tolerans miktarı | Tüm satın alma siparişine uygulanması gereken tutar toleransını girin. |
| Yüzde toleransı | Ayrı bir satın alma siparişine uygulanması gereken yüzde toleransını girin. |

## <a name="overunder-reasons"></a>Fazla/eksik nedenleri

Fazla veya eksik miktar, alınan bir seyahat satırıyla ilişkilendirildiğinde, miktarın üzerinde veya altında olmasının nedenini tanımlamanız gerekebilir. Bu durumda, mallar alındığında teslim alma satırındaki fazla teslimat veya eksik teslimat nedenini seçebilirsiniz.

Fazla teslimat ve eksik teslimat nedenlerini ayarlamak için **Varış yeri maliyeti \> Fazla/eksik kurulumu \> Fazla/eksik nedenleri**'ne gidin. Burada, kullanılabilir fazla teslimat ve eksik teslimat nedenlerini görüntüleyebilir, düzenleyebilir, ekleyebilir ve kaldırabilirsiniz. Aşağıdaki tabloda, her nedende kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Fazla/eksik nedeni | Fazla alma veya eksik alma hareketinin nedeni için benzersiz bir ad girin. |
| Tanım | Fazla/eksik nedeni açıklaması girin. |
| Hareket | Fazla/eksik nedeni ile ilişkili taşıma günlüğünü seçin. Bu alanda, **Stok günlüğü adları** sayfasında (**Stok yönetimi kurulumu \> Günlük adları \> Stok**) bir *Taşıma* günlüğü türünün ilişkili olduğu tüm kullanılabilir günlükler listelenmektedir. |

## <a name="item-overunder-tolerance-groups"></a>Madde fazla/eksik toleransı grupları

Benzer toleranslara sahip maddeler birlikte gruplandırılabilir. Bu şekilde, bu gruptaki tüm maddeler için aynı anda fazla/eksik toleransı ayarlayabilirsiniz.

Madde fazla/eksik tolerans gruplarını ayarlamak için **Varış yeri maliyeti \> Fazla/eksik kurulumu \> Madde fazla/eksik tolerans grupları**'na gidin. Burada, fazla/eksik toleransı grubu kayıtlarını görüntüleyebilir, düzenleyebilir, ekleyebilir ve kaldırabilirsiniz. Aşağıdaki tabloda, her kayıtta kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Fazla/eksik toleransı grubu | Grup için benzersiz bir ad girin. Toleransı açıklayan *%1 Var* gibi bir ad seçin. |
| Tanım | Grubun açıklamasını girin. |

## <a name="vendor-overunder-tolerance-groups"></a>Satıcı fazla/eksik toleransı grupları

Düzenli olarak fazla veya eksik teslimat yapan satıcıları gruplandırabilirsiniz. Daha sonra grup başına fazla/eksik toleransı ayarlayabilirsiniz.

Satıcı fazla/eksik tolerans gruplarını ayarlamak için **Varış yeri maliyeti \> Fazla/eksik kurulumu \> Satıcı fazla/eksik tolerans grupları**'na gidin. Burada, fazla/eksik toleransı grubu kayıtlarını görüntüleyebilir, düzenleyebilir, ekleyebilir ve kaldırabilirsiniz. Aşağıdaki tabloda, her kayıtta kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Fazla/eksik teslimat grupları | Grup için benzersiz bir ad girin. Gruba ait satıcıların türünü açıklayan bir ad seçin. |
| Tanım | Grubun açıklamasını girin. |

## <a name="view-and-process-overunder-transactions"></a>Fazla/eksik hareketlerini görüntüleme ve işleme

Yerine konulan mal miktarı başlatılan miktarla eşleşmediğinde, fazla ve eksik hareketleri oluşturulur. Varış günlüğündeki miktar yalnızca yerine koyulan miktarla güncelleştirilmelidir.

Seyahat satırlarının girişi işlendiğinde, satıcı için fazla/eksik toleransları ayarlanabilir. Maddeler daha sonra gözden geçirilecek ve doğrulanacaktır. Tolerans yüzde, yerel tutar veya her ikisi olarak ayarlanabilir.

Teslim alınan bir madde toleransın içindeyse sistem bir hareket günlüğü oluşturur. Bu günlük, seyahat parametreleri sayfasında belirtilebilir. Ayrıca, bir fazla/eksik teslimat hareketi oluşturulur. Örneğin, sipariş değeri 100 TL, giriş değeri 99 TL ise bu değerler tolerans kurallarını karşılar. Bu durumda, eksik teslim alınan miktar için negatif taşıma günlüğü oluşturulur.

Alınan bir madde toleransın dışındaysa sistem miktar farkı için bir fazla/eksik hareketi oluşturur.

Fazla/eksik hareketlerini görüntülemek ve işlemek için **Varış yeri maliyeti \> Sorgular \> Fazla/eksik hareketleri**'ne gidin. Burada, bir fazla/eksik hareketi, fazla veya eksik alınan bir yolculuktaki tüm maddelerle ilişkilendirilir. Seyahatlerle ilişkili tüm fazla/eksik hareketlerini çözmek için **Fazla/eksik hareketleri** sayfasını kullanmanızı öneririz. Ayrıca, eksik teslimat ambar hareketlerini el ile çözümlemek için taşıma veya sayım günlükleri **kullanmamanızı** öneririz. Bunun yerine, eksik teslimat ambarı miktarlarını yönetmek için **Fazla/eksik hareketleri** sayfasını kullanmalısınız.

### <a name="upper-overview-tab"></a>Üst Genel Bakış sekmesi

Fazle/eksik hareketlerinizi görüntülemek için **Fazla/eksik hareketleri** sayfasının üst kısmındaki **Genel Bakış** sekmesini seçin. Aşağıdaki tabloda, kılavuzda kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Fazla/eksik hareket numarası | Varış günlüğü işlendiğinde otomatik olarak oluşturulan fazla/eksik hareketi kaydının benzersiz adı. |
| Seyahat | Satın alma satırının bağlı olduğu seyahat. |
| Sevkiyat konteyneri | Satın alma satırının bağlı olduğu konteyner. |
| Varış günlüğü | Fazla/eksik satırının oluşturulduğu varış günlüğü. |
| Referans | Satın alma siparişine veya fazla/eksik hareketiyle ilişkili transfer emrine yapılan başvuru. |
| Sayı | Fazla/eksik hareketinde başvurulan satın alma siparişi. |
| Satıcı hesabı | Fazla veya eksik teslimatın ilişkili olduğu satıcı. |
| Transitteki malların numarası | Varsa transitteki mal numarası. |
| Madde kodu | Fazla veya eksik teslimatın ilişkili olduğu madde numarası. |
| Orijinal miktar | Sevkiyata eklenen satın alma siparişi satırının orijinal miktarı. |
| Teslim alınan miktar | Gerçekte teslim alınan miktar. |
| Fark | Beklenen varış günlüğü tutarı ile varış günlüğüne nakledilen tutar arasındaki fark. Negatif değer, malların fazla teslim edildiğini gösterir. |
| Kalan miktar | Varış günlüğü satırında kalan miktar. |
| Fazla/eksik teslimat | Teslim alınan miktarın fazla veya eksik olduğunu gösteren bir değer. |
| Durum | Fazla/eksik hareketinin durumu. **[Varış yeri maliyeti parametreleri](landed-cost-parameters.md)** sayfasındaki ayarlara bağlı olarak fazla teslimat otomatik olarak fazla teslimat tutarı için bir taşıma günlüğü oluşturabilir ve günlüğü deftere nakledebilir. Bu durumda, fazla/eksik hareketinin durumu *Tamamlandı* olur. Malları eksik teslimat ambarının dışına taşımak için eylem gerekiyorsa kaydın durumu *Devam ediyor* olur. |
| Fazla/eksik nedeni | Fazla/eksik hareketiyle ilişkili neden. |
| Diğer stok boyutları | Kılavuzda ek boyutlar için sütunları istediğiniz gibi gösterebilirsiniz. Bu boyutlar arasında toplu iş numarası, stok durumu ve ambar bulunur. Eylem bölmesinde, dahil edilecek boyutları seçebileceğiniz bir iletişim kutusu açmak için **Stok \> Boyutları görüntüle**'yi seçin. |

### <a name="upper-general-tab"></a>Üst Genel sekmesi

Üstteki **Genel Bakış** sekmesinde seçili olan satır hakkında daha fazla bilgi görüntülemek için **Fazla/eksik teslimat hareketleri** sayfasının üst kısmındaki **Genel** sekmesini seçin. Bu sekmedeki bilgiler, kullanılabilir tüm boyutların değerlerini içerir. Bu bilgiler kaynak satın alma siparişinden çekilir.

### <a name="lower-overview-tab"></a>Aşağıdaki Genel Bakış sekmesi

Üst **Genel Bakış** sekmesinde seçili satırın belge türünü görüntülemek için **Fazla/eksik teslimat hareketleri** sayfasının alt kısmındaki **Genel Bakış** sekmesini seçin. Aşağıdaki tabloda, kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Yeni belge türü | Bu alan, seçili fazla/eksik teslimat hareketi satırında gösterilen eyleme bağlı olarak *Taşıma günlüğü* veya *Satın alma siparişi* olarak ayarlanır. |
| Sayı | Seçili fazla/eksik teslimat hareketi satırıyla ilişkili satın alma siparişine veya taşıma günlüğüne başvuru ve bağlantı. |
| Fazla/eksik nedeni | Seçili fazla/eksik hareket, satırıyla ilişkili neden. |
| Miktar | Seçili fazla/eksik hareketi satırıyla ilişkili satın alma siparişi veya taşıma günlüğü için seçtiğiniz miktar. |

### <a name="lower-general-tab"></a>Alt Genel sekmesi

Seçili fazla/eksik teslimat hareketi satırıyla ilişkili fazla/eksik teslimat hareketi numarasını, lot numarasını ve boyut numarasını görüntülemek için **Fazla eksik teslimat hareketleri** sayfasının alt kısmındaki **Genel** sekmesini seçin. 

### <a name="process-overunder-transactions"></a>Fazla/eksik teslimat hareketlerini işleme

**Fazla/eksik teslimat hareketleri** sayfasındaki Eylem Bölmesi, sayfada seçilen hareketleri işlemek için aşağıdaki komutları sağlar. Her komut, her işlemin nasıl işleneceğini seçmenizi sağlar.

- **Oluştur \> Taşıma**: Seçili hareket için bir taşıma günlüğü oluşturun ve deftere nakledin. Hareketler altında, beklenen ve gerçek alınan miktar arasındaki fark için otomatik olarak bir taşıma günlüğü oluşturulur ve deftere nakledilir. Satıcının maliyet farkını dikkate almasını istiyorsanız fazla teslimat hareketleri için bu komutu seçin.
- **Oluştur \> Satın alma siparişi**: Seçili hareketin beklenen ve gerçek alınan miktarı arasındaki fark için bir satın alma siparişi oluşturun. Kuruluşunuz maliyet farkını dikkate alacaksa fazla teslimat hareketleri için bu komutu seçin.
- **Oluştur \> Hedefe transfer et**: Bu komut yalnızca transfer emirleri için geçerlidir. Fazla veya eksik miktarı hedef ambara transfer etmek istiyorsanız seçin.
- **Oluştur \> Çıkış noktasına transfer et**: Bu komut yalnızca transfer emirleri için geçerlidir. Fazla/eksik miktarı çıkış noktası ambarına transfer etmek istiyorsanız seçin.
