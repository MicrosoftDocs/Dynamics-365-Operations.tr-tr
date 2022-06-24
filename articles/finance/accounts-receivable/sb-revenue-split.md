---
title: Abonelik faturalamasında gelir bölme şablonları
description: Bu makale, bir paket olarak satılan maddeler için gelir ayırma şablonlarının nasıl ayarlanacağını açıklar.
author: JodiChristiansen
ms.date: 04/21/2022
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
ms.openlocfilehash: 145ca6e6f0673a5a09fe9a23cf5e163421617fd9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904773"
---
# <a name="revenue-split-templates-in-subscription-billing"></a>Abonelik faturalamasında gelir bölme şablonları

Gelir bölünmesi şablonlarını ayarlamak için **Gelir bölünmesi şablonu** sayfasını kullanın. Gelir bölünmesi, alt maddeleri olan bir ana maddeden oluşur. Bu madde tipi genellikle müşterilere tek bir madde veya paket olarak satılır.

Örneğin, bir bilgisayar öğesi aşağıdaki şekilde oluşturulabilir:

- **Ana öğe:** Abonelik Gümüş
- **Satır (alt öğe) maddeleri:**

    - Destek
    - Bakım
    - Lisans

Bir üst öğe oluşturduğunuzda, aşağıdaki sınırlamaları aklınızda tutun:

- Bir madde, yalnızca bir kez ana madde olarak belirtilebilir.
- Ana madde, aynı şablonda bir alt öğe olarak seçilebilir.
- Geçerli bir şablon en az bir alt öğe gerektiriyor.
- Bir madde, birden fazla paket madde için alt madde olarak belirtilebilir.
- Her bir üst alt ilişkisi benzersiz olmalıdır.

## <a name="create-a-parent-item-that-has-child-items"></a>Alt öğeleri olan bir ana öğe oluştur

Alt öğeleri olan bir ana öğe oluşturmak için aşağıdaki adımları izleyin.

1. **Gelir bölünme şablonu** sayfasında, **Yeni**'yi seçin.
1. **Üst madde** alanında bir ana madde seçin. **Değişken numarası** alanı otomatik olarak güncelleştirilir. Değeri istediğiniz gibi değiştirebilirsiniz.
1. **Tahsisat yöntemi** alanında, bir tahsisat yöntemi seçin.
1. Alt öğe eklemek için **Bileşen maddeleri** listesinde **Ekle**'yi seçin.
1. **Tahsis yöntemi** alanında **Yüzdelik**'i seçtiyseniz, **Yüzdelik** alanında bir yüzde belirletin.

    - **Tahsisat yöntemi** alanında **Eşit miktar**'ı seçtiyseniz **Yüzdelik** alanı otomatik olarak güncelleştirilir, böylece her bir madde eşit yüzdeye sahip olur.
    - **Tahsisat yöntemi** alanında **Değişken tutar** , **Sıfır üst tutarı** veya **Sıfır tutarını** seçtiyseniz , **Yüzde** alanının değeri **0** (sıfır) olarak kalır ve değiştirilemez.

1. **Kaydet**'i seçin.

## <a name="fields"></a>Alanlar

**Gelir bölünmesi şablonu** sayfası, aşağıdaki alanları içerir.

| Alan | Açıklama |
|-------|-------------|
| Ana madde | Madde numarası seçin. Bu madde, oluşturduğunuz paket madde için ana madde olur. |
| Ürün adı | Ürün adı. |
| Tahsisat yöntemi | <p>Tahsisat yöntemini seçin:</p><ul><li>**Eşit tutar**: Tahsisat yüzdeleri otomatik olarak hesaplanır ve şablondaki tüm maddeler arasında eşit olarak bölünür.</li><li>**Yüzde**: Tahsisat için bir yüzde tutarı belirtebilirsiniz. Tüm yüzdelerin toplamı 100 olmalıdır.</li><li>**Değişken tutar** – Eklenen alt maddelerin net tutarı 0'dır (sıfır). Alt maddelerin fiyatı hareket düzeyinde belirtilmelidir.</li><li>**Sıfır tutar** – Üst madde birim fiyatını ve net tutarını tutar. Tüm alt öğelerin net tutarı 0 (sıfır).</li><li>**Sıfır üst tutarı** – Ana maddenin sabit net tutarı 0 (sıfır). Tüm alt öğeler standart öğeler gibi işlem görür. Alt madde tutarlarının toplamının ana madde tutarına eşit olduğunu doğrulamak için doğrulama yapılmaz.</li></ul> |
| **Bileşen maddeleri** | |
| Bileşen maddesi | Madde numarası seçin. Bu madde bir alt öğedir. |
| Çeşit numarası | Maddenin değişken numarasını seçin. |
| Ürün adı | Ürün adı. |
| Yüzde | <p>Kilometre taşı için tahsisat yüzdesi.</p><ul><li>**Tahsisat yöntemi** alanı **Yüzde** olarak ayarlanırsa yüzdeyi belirtebilirsiniz.</li><li>**Tahsisat yöntemi** alanı **Eşit tutar** olarak ayarlanırsa yüzde, şablondaki tüm maddeler eşit yüzdeye sahip olacak şekilde otomatik olarak hesaplanır.</li><li>**Tahsisat yöntemi** alanı **Değişken tutar**, **Sıfır üst tutarı** veya **Sıfır tutar** olarak ayarlanmışsa, yüzde 0 (sıfır) olur ve düzenlenemez.</li></ul><p>Bu alanın değeri 0 (sıfır) ile 100 arasında herhangi bir pozitif sayı olabilir. Tüm yüzdelerin toplamı 100 olmalıdır.</p> |
| Toplam yüzde | <p>**Yüzde** sütunundaki değerlerin toplamı.</p><ul><li>**Tahsisat yöntemi** alanı **Eşit tutar** veya **Yüzde** olarak ayarlanırsa tüm yüzdelerin toplamı 100'e eşit olmalıdır.</li><li>**Tahsisat yöntemi** alanı **Değişken tutar**, **Sıfır üst tutarı** veya **Sıfır tutar** olarak ayarlanmışsa, topla yüzde 0 (sıfır) olur.</li></ul> |

## <a name="revenue-split-on-a-sales-order"></a>Satış siparişinde gelir bölünmesi

Gelir bölünmesi için ayarlanmış bir madde içeren bir satış siparişi oluşturmak için aşağıdaki adımları izleyin.

1. **Satış siparişi** sayfasında bir satış siparişi oluşturun.
2. Gelir bölünmesi için ayarlanan her madde için satırda **Gelir bölünmesi** onay kutusunu seçin. Bu öğe ana madde olur. Şablon önceden ayarlanmışsa, alt öğeler otomatik olarak listede görünür.
3. Daha fazla alt öğe eklemek için, **Gelir bölünmesi alt öğesi ekle**'yi seçin ve eklemek istediğiniz alt öğeyi seçin.
4. Siparişi kaydedin.

## <a name="revenue-split-with-billing-schedules"></a>Faturalama zamanlamalarıyla gelir bölünmesi

Gelir bölünmesi için ayarlanmış bir madde içeren bir faturalama zamanlaması oluşturmak için aşağıdaki adımları izleyin.

1. **Tüm/Etkin faturalama zamanlamaları** sayfasında, bir fatura planı oluşturun.
2. Gelir bölünmesi için ayarlanan her madde için satırda **Gelir bölünmesi** onay kutusunu seçin. Bu öğe ana madde olur. Şablon önceden ayarlanmışsa, alt öğeler otomatik olarak listede görünür.
3. Daha fazla alt öğe eklemek için, **Gelir bölünmesi alt öğesi ekle**'yi seçin ve eklemek istediğiniz alt öğeyi seçin.
4. Ödeme çizelgesiyle ilgili adımlarla devam edin.

> [!NOTE]
> **Gelir bölmeyi otomatik olarak oluştur** seçeneği **Evet** olarak ayarlanmışsa, **Yinelenen sözleşme faturalama parametreleri** sayfasında aşağıdaki eylemler gerçekleşir:
>
> - Gelir bölünmesi şablonunda bir satır maddesi ana madde olarak belirlenmişse, **Gelir bölünmesi** onay kutusu otomatik olarak seçilir.
> - Alt maddeler otomatik olarak satış siparişi veya ödeme çizelgesi satırına girilir.
>
> **Geliri otomatik olarak oluştur** seçeneği **Hayır** olarak ayarlanmışsa, davranış daha önce açıklanmıştır.

## <a name="additional-revenue-split-information"></a>Ek gelir bölme bilgileri

Gelir bölmenin parçası olan bir madde eklediğinizde, aşağıdaki bilgileri göz önünde bulundurun: 

- Üst tutar ertelenemez.
- Alt maddelerin başlangıç tarihi, bitiş tarihi, miktar, birim, tesis ve ambar değerleri üst maddeye bağlıdır. Bu değerler alt maddeler için değiştirilemez. Tüm değişiklikler üst maddede yapılmalıdır. 
- Fiyatlandırma yöntemi **Sabit** yöntemidir ve değiştirilemez.
- Alt maddeler eklenebilir veya çıkarılabilir.
- Üst ve alt maddeler aynı madde grubunu kullanmalıdır. 
- Alt maddeler aşağıdaki kurulumlardan birine sahip olabilir:

    - **Faturalama sıklığı** ve **Faturalama aralıkları** alanları üst maddeyle aynı değere ayarlanır. 
    - **Faturalama sıklığı** alanı **Tek seferlik** olarak ayarlanır. Bu durumda, **Faturalama aralıkları** alanı otomatik olarak **1** değerine ayarlanır. 

- Alt maddelere ait net tutarların toplamı üst tutara eşittir. Tahsisat yönteminin **Sıfır tutarlar** olması durumunda, hem alt madde tutarlarının toplamı hem de üst tutar 0 (sıfır) değerindedir. 

    > [!NOTE]
    > Tahsisat yönteminin **Sıfır üst tutarı** olması durumunda, alt maddelerin (sıfır olmayan) toplamı 0 (sıfır) olan üst tutara eşit değildir. Bu tahsisat yöntemi, çalışanların alt maddeleri görebilmesi için şirket içi amaçlar doğrultusunda kullanılır. Ancak, müşteriler yalnızca üst maddeyi görebilir.

- Satış siparişinin çoklu öğe düzenleme (MEA) türü **Tek** ise ilgili çoklu öğe gelir tahsisatı hareket satırı üst ve alt maddeler eklendiğinde oluşturulur. 
- Gelir bölme tahsisat yönteminin **Eşit tutarlar** olması ve üst tutarın değiştirilmesi durumunda, tüm alt satırların tutarları yeniden hesaplanır. 
- Tahsisat yönteminin **Değişken tutar** olduğu bir gelir bölme işleminde aşağıdaki davranış gerçekleşir:

    - Üst maddenin net tutarı **Üst tutar** sütununda görünür. Bu değer düzenlenebilir. Ancak birim fiyat, net tutar ve iskonto 0 (sıfır) değerindedir ve düzenlenemez.
    - Alt maddelerin birim fiyatı 0 (sıfır) değerindedir. Birim fiyatı veya net tutarı düzenleyebilirsiniz. Bir değeri düzenlediğinizde, diğer değer otomatik olarak güncelleştirilir.

- Tahsisat yönteminin **Yüzde** olduğu bir gelir bölme işleminde aşağıdaki davranış gerçekleşir:

    - Üst maddenin net tutarı **Üst tutar** sütununda görünür. Bu değer düzenlenebilir. Ancak birim fiyat, net tutar ve iskonto 0 (sıfır) değerindedir ve düzenlenemez. 
    - Alt maddelerin net tutarı, *Yüzde* &times; *Üst tutar* şeklinde hesaplanır.

- Tahsisat yönteminin **Eşit tutar** olduğu bir gelir bölme işleminde aşağıdaki davranış gerçekleşir:

    - Üst maddenin net tutarı **Üst tutar** sütununda görünür. Bu değer düzenlenebilir. Ancak birim fiyat, net tutar ve iskonto 0 (sıfır) değerindedir ve düzenlenemez. 
    - Alt maddelerin net tutarı, üst tutarın tüm alt maddeler arasında eşit olarak bölünmesiyle hesaplanır. 
    - Alt maddeler kaldırılır veya eklenirse, tüm alt satırların eşit tutarlara sahip olması için net tutar ve birim fiyatları yeniden hesaplanır. 
    - Üst tutar eşit olarak bölünemezse son alt maddenin net tutarı ve birim fiyatı, diğer alt maddelerin net tutarından ve birim fiyatından biraz daha az veya fazla olabilir. 

- Tahsisat yönteminin **Sıfır tutarlı** olduğu bir gelir bölme işleminde aşağıdaki davranış gerçekleşir:

    - Birim fiyatı, net tutar ve iskonto düzenlenebilir. Üst tutar 0 (sıfır) değerindedir ve düzenlenemez. 
    - Alt maddelerin miktarı, birimi, tesisi ve ambar değerleri üst öğeye bağlıdır. Alt maddeler için bu değerleri değiştiremezsiniz. Tüm değişiklikler üst maddede yapılmalıdır. 
    - Alt maddelerin birim fiyatı ve net fiyatı 0 (sıfır) değerindedir ve düzenlenemez. 

- Tahsisat yönteminin **Sıfır üst tutarı** olduğu bir gelir bölme işleminde aşağıdaki davranış gerçekleşir:

    - Üst öğenin birim fiyatı, üst tutarı ve net tutarı 0 (sıfır) değerindedir.
    - Fatura planında, alt satırlar el ile eklenmiş gibi görünür ve tüm değerler seçili fatura planı grubuna göre güncelleştirilir. Bu değerler düzenlenebilir. Alt maddeler için **Fatura ayrıntılarını görüntüle** sayfasındaki **Girilen miktar**, **Birim fiyatı**, **İskonto** ve **Net tutar** alanlarını kullanarak **İlerletme ve iskonto** ve **Gelişmiş fiyatlandırma** seçeneklerine erişebilirsiniz. 
    - Bir satış siparişinde, alt satırlarda iskonto ve iskonto yüzdesi 0 (sıfır) değerindedir. 
    - Üst ve alt maddelerin faturalama sıklığı değiştirilebilir ve her maddenin farklı bir sıklık değeri olabilir. Ancak üst madde, alt maddeleri arasında en kısa sıklık değerine sahip olanın sıklık değerini kullanması için otomatik olarak güncelleştirilir. Örneğin, bir gelir bölme işleminde iki alt madde vardır ve bunlardan biri **Aylık** faturalama sıklığını, diğeri ise **Yıllık** faturalama sıklığını kullanmaktadır. Bu durumda, üst maddenin faturalama sıklığı **Aylık** olarak güncelleştirilir.
