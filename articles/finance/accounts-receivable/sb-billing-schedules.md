---
title: Faturalama zamanlamasına genel bakış
description: Bu konuda, faturalama zamanlamaları oluşturma, silme ve düzenleme işlemleri açıklanmaktadır.
author: JodiChristiansen
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: e42be3f359e96f0861354ebc8e1e9c87478a5d89
ms.sourcegitcommit: 6102f70d4595d01b90afe5b23dfd8ec2ea030653
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/16/2022
ms.locfileid: "8182703"
---
# <a name="billing-schedule-overview"></a>Faturalama zamanlamasına genel bakış

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

**Faturalama zamanlaması** sayfasında fatura zamanlamaları oluşturabilir, silebilir veya düzenleyebilirsiniz. Ayrıca, faturalama zamanlamaları listesini gözden geçirebilirsiniz. Bir faturalama zamanlaması oluşturduğunuzda, bununla ilgili varsayılan değerler kendisiyle ilişkilendirilmiş faturalama grubu tarafından belirlenir. Ek bilgiler **Yinelenen sözleşme faturalama parametreleri** sayfasında ayarlanır.

## <a name="create-a-billing-schedule"></a>Faturalama zamanlaması oluşturma

Faturalama zamanlaması oluşturmak için aşağıdaki adımları izleyin.

1. **Faturalama zamanlaması** sayfasında **Yeni**'yi seçin.
2. **Faturalama zamanlaması oluştur** iletişim kutusunda **Faturalama zamanlaması grubu** alanında bir faturalama zamanlaması grubu seçin.
3. **Müşteri hesabı** alanından bir müşteri hesabı seçin.
4. **Başlangıç tarihi** alanında başlangıç tarihini seçin ve **Dönem sayısı** alanına dönem sayısını girin. **Bitiş tarihi** alanı, girdiğiniz dönem sayısına göre güncelleştirilir. **Faturalama bitiş tarihi** alanını güncelleştirirseniz **Dönem sayısı** alanı **0** (sıfır) olarak güncelleştirilir.
5. **Tamam**'ı seçin.
6. **Faturalama zamanlaması** sayfasında, **Genel** sekmesinde **Açıklama** alanına faturalandırma zamanlamasının açıklamasını girin.
7. **Kilometre taşı şablonu** alanında, **Aşama bazında faturalama** için bir kilometre taşı şablonu seçin.

**Fatura hesabı** ve **Para birimi kodu** gibi alanlar müşterinin bilgileriyle güncelleştirilir.

**Faturalama sıklığı** ve **Faturalama aralığı** alanları, seçilen faturalama zamanlaması grubuna göre otomatik olarak ayarlanır.

8. Ayrı faturalar oluşturmak için **Ayrı olarak faturala** seçeneğini **Evet** olarak ayarlayın.
9. Son faturalama döneminden sonra bir faturalama zamanlamasını otomatik olarak yenilemek için **Otomatik Yenile** seçeneğini **Evet** olarak ayarlayın ve **Yenileme başına eklenecek satırlar** alanını ayarlayın.

**Parametreler** alanları, **Yinelenen sözleşme fatura parametreleri** sayfasındaki değerlere göre otomatik olarak ayarlanır.

10. Bir fatura zamanlaması tutarını eşit şekilde ayarlamak için **Kısmi dönemleri eşit dağıt** seçeneğini **Evet** olarak ayarlayın.
11. Fatura zamanlaması ayrıntı satırlarını ayın sonuyla uyumlu hale getirmek için **Aya uyumlu hale getir** seçeneğini **Evet** olarak ayarlayın.
12. **Sözleşeme başlangıç tarihi** ve **Sözleşme bitiş tarihi** alanlarına, sözleşmenin başlangıç ve bitiş tarihlerini girin. Bu tarihler yalnızca bilgi amaçlıdır.

**Ödeme** alanı, müşteriden alınan müşteri ödeme bilgilerini gösterir. Bir satır maddesi beklemeye alındıysa veya sonlandırılıysa ödeme bilgileri değiştirilemez.

> [!NOTE]
> Faturaları maddeye göre birleştirdiğinizde, **Ödeme koşulları**, **Yöntem** ve **Faturalama zamanlaması** alanları eşleşmelidir. Aksi takdirde, faturalar birleştirilemez.

13. **Adres** sekmesinde, **Teslimat adresi** ve **Fatura adresi** alanlarını gözden geçirebilir ve güncelleştirebilirsiniz.
14. **İlgili kişi bilgileri** sekmesinde, bir son kullanıcı hesabını faturalama zamanlamasıyla ilişkilendirebilirsiniz.
15. **İlgili kişi bilgileri** alanlarına, bir ilgili kişi, e-posta adresi ve internet adresi girebilirsiniz.
16. İş ortağı komisyon bilgilerini izlemek için **İş ortağı hesabı** ve **İş ortağı komisyon oranı** alanlarını ayarlayın. Bu alanlar yalnızca bilgi amaçlıdır.
17. **Toplam** sekmesinde, faturalama zamanlaması için hesaplanan çeşitli toplamları görüntüleyebilirsiniz.
18. **Bekletme** sekmesinde, faturalama zamanlamasının ne zaman beklemeye alındığına ve bekletmenin ne zaman kaldırılığına ilişkin denetim bilgilerini görüntüleyebilirsiniz.
19. **Sonlandırma** sekmesinde, faturalama zamanlamasına uygulanan veya zamanlamadan kaldırılmış olan sonlandırmaların geçmişini görüntüleyebilirsiniz.
20. **Kaydet**'i seçin.
21. **Faturalama zamanlaması satırları** hızlı sekmesinde **Satır ekle**'yi seçin.
22. **Madde numarası** alanında madde numarasını seçin. Eklenen madde gelir bölmedeki bir ana madde ise, satırlar otomatik olarak alt maddelerle güncelleştirilir. Gelir bölmede yalnızca ana maddeyi düzenleyebilirsiniz. Tüm alt öğeler de buna göre güncelleştirilir.
23. **Madde türü** alanında madde türünü seçin.
24. Başlangıç ve bitiş tarihlerini güncelleştirin.
25. Faturalar oluşturulmadan önce, **Faturalama sıklığı** alanını güncelleştirerek faturalama sıklığını değiştirebilirsiniz. Faturalama zamanlamasının ilk faturası oluşturulduktan sonra, faturalama sıklığı değiştirilemez.
26. **Birim** alanında, madde için ölçü birimini seçin.
27. **Fiyatlandırma yöntemi** alanında, maddeyle ilgili fiyatlandırma yöntemini seçin.

**Birim fiyat** alanı otomatik olarak stoktan ayarlanır. Ancak, fiyatlandırma yöntemini **Düz** olarak değiştirirseniz, bunu güncelleştirebilirsiniz.

## <a name="remove-a-line-item"></a>Satır maddesini kaldırma

Bir maddeyi faturalama zamanlamadan kaldırmak için aşağıdaki adımları izleyin.

1. **Faturalama zamanlaması** sayfasında, **Zamanlama numarası** alanında düzenlenecek faturalama zamanlamasının numarasını seçin.
2. **Faturalama zamanlaması satırları** hızlı sekmesinde, silinecek satırı ve **Kaldır**'ı seçin.
3. **Kaydet**'i seçin.

Bu konunun geri kalanında, **Faturalama zamanlaması satırları** hızlı sekmesinde satırlar için kullanılabilir olan eylemler ve ayrıntılar açıklanmaktadır.

## <a name="billing-schedule-line-actions"></a>Faturalama zamanlaması satırı eylemleri

**Faturalama zamanlaması satırları** hızlı sekmesindeki düğmeler, eylemleri ayrı satırlara uygulamanıza olanak sağlar.

| Düğme | Açıklama |
|--------|-------------|
| Satır ekle | Faturalama zamanlamasına bir satır ekleyin. |
| Madde listesinden ekle | Listeden seçerek faturalama zamanlamasına birden fazla madde ekleyin. |
| Kaldır | <p>Seçili satırı üst faturalama zamanlamasından kaldırın.</p><p>Gelir bölmenin bir parçası olan maddeler için yalnızca ana maddeyi kaldırabilirsiniz. İlişkili tüm alt öğeler otomatik olarak kaldırılır.</p> |
| Fatura ayrıntısını görüntüle | Faturalama ayrıntılarını görüntüleyin. |
| Sonlandır | <p>Seçili satırları sonlandırın. Bu düğme yalnızca seçili satırların durumu **Etkin** olduğunda kullanılabilir.</p><p>Gelir bölmenin bir parçası olan maddeler için yalnızca ana maddeyi sonlandırabilirsiniz.</p> |
| Sonlandırmayı kaldır | <p>Seçili satırlardan sonlandırmayı kaldırın. Bu düğme yalnızca seçili satırların durumu **Sonlandırıldı** olduğunda kullanılabilir.</p><p>Gelir bölmenin bir parçası olan maddeler için sonlandırmayı yalnızca ana maddeden kaldırabilirsiniz.</p> |
| Bekletme uygula | <p>Seçili satırı bekleme durumuna almak için ayrıntılarını seçin.</p><p>Gelir bölmenin bir parçası olan maddeler için yalnızca ana maddeyi beklemeye alabilirsiniz.</p> |
| Bekletmeyi kaldır | <p>Seçili satırından beklemeyi kaldırın.</p><p>Gelir bölmenin bir parçası olan maddeler için bekletmeyi yalnızca ana maddeden kaldırabilirsiniz.</p> |
| İlerletme ve iskonto | Bu düğme gelir bölme işleminin parçası olan maddeler için kullanılamaz, ancak gelir bölmenin **Sıfır tutar** tahsisat yönetimini kullandığı ana maddeler bunun dışındadır. |
| Ertelemeler | <p>Seçili satır için erteleme seçeneklerini girin.</p><p>Bu düğme, gelir bölmedeki üst maddeler için kullanılamaz.</p> |
| Kilometre taşı tahsisatı | <p>Seçili satır için kilometre taşı tahsisat bilgilerini gözden geçirin ve güncelleştirin.</p><p>Bu düğme yalnızca, faturalama zamanlaması satır maddesi bir kilometre taşı maddesi olduğunda kullanılabilir.</p> |
| Destek ve yenileme | <p>Seçili satır için destek ve yenileme bilgilerini gözden geçirin ve güncelleştirin.</p><p>Bu düğme yalnızca, faturalama zamanlaması satır maddesi bir destek veya yenileme maddesi olduğunda kullanılabilir.</p> |
| Boyutları görüntüle | **Faturalama zamanlaması satırları** kılavuzunda görüntülenen boyut sütunlarını gösterin veya gizleyin. |
| Birim fiyatı hesapla | <p>Müşterinin sözleşme tutarını taksitli olarak ödeyebilmesi için (örneğin günlük, aylık, üç aylık, altı aylık veya yıllık), maddenin birim fiyatını hesaplayın. Sözleşme fiyatını ve fiyat sıklığını seçebilirsiniz.</p><p>Değişikliklerin denetim kaydını görüntüleyebilirsiniz: eski sözleşme fiyatı ve sıklığı, yeni sözleşme fiyatı ve sıklığı, değişikliği yapan kullanıcı ve değişikliğin tarihi ve saati.</p> |
| Sıralama tarihi | <p>Yenileme maddeleri için uyumlu hale getirme tarihini belirtin.</p><p>**Madde grubu** alanında bir madde grubu seçerseniz tüm maddeler, faturalama zamanlamasındaki madde grubundaki ilk maddenin uyumlu hale getirme tarihini kullanır. **Madde grubu** alanı boşsa, tüm maddeler için kullanılacak bir uyumlu hale getirme tarihi belirtebilirsiniz.</p><p>Bu düğme, yalnızca **Faturalama sıklığı** alanı **Yıllık** olarak ayarlandığında kullanılabilir.</p> |
| Faturalanmamış gelir | <p>Faturalanmamış gelir özelliğini kullanmak üzere maddeyi ayarlayın. Böylece, madde için faturalandırılmamış gelir ve faturalandırılmamış iskonto hesaplarını belirtebilirsiniz.</p><p>Bu düğme yalnızca **Madde türü** alanının **Standart** olarak ayarlandığı maddeler için kullanılabilir. Mevcut faturalama zamanlamaları veya faturanın önceden oluşturulmuş olduğu faturalama zamanlaması satırları için kullanılamaz.</p> |
| Gelir bölme alt maddesi ekle | <p>Satış siparişibe eklemek için bir alt öğe seçin.</p><p>Bu düğme yalnızca gelir bölme işlemindeki üst maddeler için kullanılabilir.</p> |
| Gelişmiş fiyatlandırma seçenekleri | Maddenin fiyatlandırma seçeneklerini düzenleyin. |

## <a name="billing-schedule-line-details"></a>Faturalama zamanlaması satırı ayrıntıları

**Faturalama zamanlaması satırları** hızlı sekmesinde bir satır seçtiğinizde, o satırla ilgili belirli ayrıntıları görebilirsiniz. Bu ayrıntılar farklı sekmeler arasında bölünür.

### <a name="general-tab"></a>Genel sekmesi

**Genel** sekmesinde aşağıdaki bilgiler bulunur.

| Alan veya bölüm | Açıklama |
|------------------|-------------|
| Kullanım | <p>Bu bölümde kullanım maddeleri hakkında bilgi sağlanmaktadır: Aşağıdaki alanları içerir:</p><ul><li>**Kullanım tanımlayıcısı**: Ölçüm veya kullanım maddesinin tanımlayıcısı.</li><li>**Okuma seçeneği**: Kullanım okuma seçeneği: **Okuma** veya **Tüketim**.</li><li>**Tahmini tüketim**: Faturanın oluşturulmadığı dönemler içeren bir kullanım maddesi için tahmini tüketimi belirtin. **Faturalama ayrıntıları** sayfasında, tahmini tüketim için fatura ayrıntı satırlarını gözden geçirebilirsiniz.</li></ul> |
| Harici referanslar\* | Bu bölüm harici referans bilgilerini belirtebileceğiniz **Harici** ve **Satır numarası** alanlarını içerir. |
| Kilometre taşı | <p>Bu bölümde kilometre taşı maddeleri hakkında bilgi sağlanmaktadır: Madde tamamlanma tarihini gösteren **Tahmini tamamlanma tarihi** alanını içerir.</li></ul> |
| Metin | Satır için açıklama. Metin, müşterinin veya tüzel kişiliğin varsayılan diline çevrilir. |
| Madde grubu | Satır maddesi için madde grubu. |
| Sıralama tarihi | Faturalama zamanlaması için uyumlu hale getirme tarihi. |

\* **Fatura oluştur** sayfasında faturaları maddeye göre birleştirdiğinizde **Harici başvuru** alanlarının eşleşmesi gerekir. Bir karakter farklı olsa bile maddeler faturada birleştirilmez. **Harici başvuru** bölümündeki bölümündeki her iki alan için de doğrulama denetimi yapılmaz ve **Satır numarası** alanındaki değer pozitif bir tamsayı olmalıdır.

### <a name="address-tab"></a>Adres sekmesi

**Adres** sekmesinde aşağıdaki bilgiler bulunur.

| Alan | Açıklama |
|-------|-------------|
| Teslimat adresi | <p>Satır maddesi için teslimat adresini seçin. Varsayılan teslimat adresi, **Adres** hızlı sekmesindeki birincil teslimat adresidir.</p><p>Adresi değiştirdiğinizde, aşağıdaki adres seçeneklerini belirleyebilirsiniz:</p><ul><li>**Adresler**: Geçerli müşteri için bir adres seçin.</li><li>**Kullanımda**: Geçerli müşteri için kullanılmakta olan bir adres seçin.</li><li>**Diğer adres**: Herhangi bir müşteri kaydı için bir adres seçin.</li></ul><p>Gelir bölme kullanan maddeler için, yalnızca ana maddenin adresi düzenlenebilir. Alt öğelerin adresi üst öğenin adresiyle eşleşir ve ayrı olarak düzenlenemez.</p> |
| Fatura adresi | <p>Satır maddesi için fatura adresini seçin. Varsayılan teslimat adresi, **Adres** hızlı sekmesindeki birincil teslimat adresidir. Adresi, mevcut adreslerin amacına göre istediğiniz şekilde değiştirebilirsiniz:</p><ul><li>Adreslerin hiçbirinde **Fatura** amacı yoksa, varsayılan fatura adresi amacı ne olursa olsun müşterinin birincil adresi olur.</li><li>Bir veya daha fazla adres **Fatura** amacına sahipse, varsayılan fatura adresi en son girilen adrestir.</li><li>Bir veya daha fazla adres **Fatura** amacına sahipse ve fatura adreslerinden biri birincil adres olarak ayarlanmışsa, varsayılan fatura adresi **Fatura** amacı içeren ve birincil adres olarak ayarlanan adrestir.</li><li>Gelir bölme kullanan maddeler için, yalnızca ana maddenin adresi düzenlenebilir. Alt öğelerin adresi üst öğenin adresiyle eşleşir ve ayrı olarak düzenlenemez.</li></ul> |

### <a name="product-tab"></a>Ürün sekmesi

**Ürün** sekmesinde aşağıdaki bilgiler bulunur.

| Alan veya bölüm | Açıklama |
|------------------|-------------|
| Depolama boyutları | <p>Bu bölüm, maddeyle ilgili depolama bilgilerini gösterir. Maddenin seri numarasını gösteren **Seri numarası** alanını içerir.</p><p>Seri numarası, destek ve yenileme işlemi sırasında başlangıçtaki satış siparişinden kopyalanır. Gelir bölme kullanan maddeler için, üst maddenin seri numarası tüm alt maddelere kopyalanır. Seri numarası, **Yinelenen sözleşme faturalama parametreleri** sayfasında **Seri numarasını kopyala** seçeneği **Evet** olarak ayarlandığında kopyalanır.</li></ul> |
| Ürün boyutları | Maddenin ürün ayrıntıları ve değerleri, faturalama zamanlaması satırı için seçilen **Varyant numarası** değeri temel alınarak otomatik olarak güncelleştirilir. |

### <a name="account-tab"></a>Hesap sekmesi

**Hesap** sekmesinde aşağıdaki bilgiler bulunur.

| Alan | Açıklama |
|-------|-------------|
| Ana hesap | Satış satırında oluşturulan ana hesap. Varsayılan değer, satış siparişinden alınır. Bu alan boş olabilir. |
| Madde mali boyutları | <p>Müşteri ve madde kaydına dayalı olarak varsayılan mali boyut değerleri.</p><p>Gelir bölme kullanan maddeler için, alt maddeler daha önce açıklandığı gibi, müşteri ve madde kayıtlarının mali boyut değerlerini kullanır. Alt öğelerin mali boyut değerlerini güncelleştirmeniz gerekiyorsa, veri varlığını içe aktarabilirsiniz.</p> |

### <a name="renewals-tab"></a>Yenilemeler sekmesi

**Yenilemeler** sekmesinde aşağıdaki bilgiler bulunur.

| Alan | Açıklama |
|-------|-------------|
| Otomatik olarak yenile | <p>Faturalama zamanlaması satırının sonraki faturalama dönemi için otomatik olarak yenilenip yenilenmediğini belirten bir değer:</p><ul><li>**Evet**: Faturalama zamanlaması satırı bir fatura oluşturduğunuzda sonraki faturalama dönemi için otomatik olarak yenilenir.</li><li>**Hayır**: Faturalama zamanlaması satırı otomatik olarak yenilenmez. Faturalama zamanlamasını el ile yenilemeniz gerekir.</li></ul> |
| Yenileme başına eklenecek satır sayısı | Faturalama zamanlaması yenilemeye eklenecek satır sayısı. |

Ayrıca, **Yenilemeler** sekmesinde aşağıdaki düğmeler bulunur.

| Düğme | Açıklama |
|--------|-------------|
| Faturalanmamış gelir günlük girişi denetimi | Faturalanmamış gelir özelliğini kullanan tüm maddeler için yapılan tüm değişiklikleri görüntüleyin. |
| Yenileme dönemi ekle | Madde için yenileme süresi ekleyin. Yeni yenileme süresinin başlangıç tarihi, önceki sürenin bitiş tarihinden bir sonraki tarihtir. **Yenileme bitiş tarihi**, **Erteleme başlangıç tarihi**, **Erteleme bitiş tarihi**, **Madde miktarı** ve **Birim fiyat** alanları güncelleştirilebilir. |
| Yenileme dönemini değiştir | <p>Yenileme süresini değiştirin. İlk süre için, ilk günlük girişi oluşturulmadan önce erteleme başlangıç ve bitiş tarihlerini değiştirebilirsiniz. Sonraki süreler için başlangıç tarihi değiştirilemez. Bu, her zaman önceki sürenin sona ermesinden bir sonraki tarihtir.</p><p>Değiştirdiğiniz süreden sonra bir yenileme süresi varsa, sürenin tarihleri değiştirilemez. Bu durumda, yalnızca yenileme maddesiyle ilgili **Miktar** ve **Birim Fiyat** alanları güncelleştirilebilir.</p><p>Örneğin, üç süre mevcuttur. <ul><li>İlk süre zaten başlatıldığından değiştirilemez.</li><li>İkinci süre için yalnızca miktar ve birim fiyat değiştirilebilir.</li><li>Üçüncü süre için, başlangıç tarihi dışındaki tüm değerler değiştirilebilir. Ayrıca, **Şablondan zamanlama** seçeneği faturalandırılmamış gelir maddesi için şablonu esas alan bir erteleme zamanlaması oluşturmanıza olanak tanır. Bu seçenek **Evet** olarak ayarlandığında, **Şablon** alanında erteleme şablonunu seçin ve gereksinim duyduğunuz şekilde erteleme başlangıç ve bitiş tarihlerini değiştirin. Sonraki yenileme süreleri aynı erteleme şablonunu kullanır. Ancak erteleme şablonu değiştirilebilir.</p></li></ul> |

### <a name="termination-tab"></a>Sonlandırma sekmesi

**Sonlandırma** sekmesinde aşağıdaki bilgiler bulunur.

| Alan | Açıklama |
|-------|-------------|
| Ayrılma tarihi | Faturalama zamanlaması satırının sonlandırıldığı tarih. Varsayılan değer, başlıktaki **Sonlandırma tarihi** alanından alınır. Değeri istediğiniz gibi değiştirebilirsiniz. |
| Sonlandırma türü | Sonlandırma türü. Varsayılan değer, başlıktaki **Sonlandırma türü** alanından alınır. |

### <a name="hold-tab"></a>Bekletme sekmesi

Gelir ve gider ertlemeleri kullanılıyorsa, **Bekletme** sekmesinde erteleme tarihi gösterilir.

### <a name="escalation-and-discount-tab"></a>Aktarma ve iskonto sekmesi

**Aktarma ve iskonto** sekmesinde aşağıdaki bilgiler bulunur.

| Alan | Açıklama |
|-------|-------------|
| İlerletme | <p>Faturalama zamanlaması satırı için aktarmalara izin verilip verilmediğini seçin. Başlıktaki herhangi bir aktarma satırı, faturalama zamanlaması satırı oluşturulduğunda uygulanır.</p><ul><li>**Evet**: Aktarmalar satıra uygulanabilir. Bu seçenek işaretlendiğinde, **Aktarma ve iskonto** sayfasında faturalama zamanlaması satırları için aktarmaları ayarlayabilirsiniz.</li><li>**Hayır**: Aktarmalar satıra uygulanamaz.</li></ul><p>Varsayılan ayar, seçilen **Faturalama zamanlaması grubu**'nu temel alır.</p> |

### <a name="price-changes-tab"></a>Fiyat değişiklikleri sekmesi

**Standart** fiyat yerine **Düz** fiyat olarak değiştirilen satırlar için **Fiyat değişiklikleri** sekmesindeki kılavuz aşağıdaki sütunları içerir:

- Tarihi değiştir
- Değiştiren kullanıcı
- Standart fiyat
- Düz fiyat
- Fiyat güncelleştirme
