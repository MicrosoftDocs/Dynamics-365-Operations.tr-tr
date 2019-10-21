---
title: Dağıtılmış sipariş yönetimi (DOM) için maliyet yapılandırması
description: Bu konuda, Dynamics 365 Retail'deki dağıtılmış sipariş yönetimi (DOM) işlevi için maliyet yapılandırması açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 12/05/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-12-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: b5e3e1997f3d3b61b7b3c7486f5531e386293537
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "2019451"
---
# <a name="cost-configuration-for-distributed-order-management-dom"></a>Dağıtılmış sipariş yönetimi (DOM) için maliyet yapılandırması

[!include [banner](../includes/banner.md)]

Kuruluşlar, bir siparişin karşılanması gereken en iyi konumu belirlemek için birden fazla maliyet bileşenini dikkate alır. Bu maliyet bileşenlerinden bazıları sevkiyat maliyeti, işleme maliyeti ve ambalaj maliyetidir. Bu maliyetlerin birleşimi, karşılama konumunun belirlenmesi için hesaplanır.

Dynamics 365 Retail'de dağıtılmış sipariş yönetiminin (DOM) ilk yinelemesi siparişleri karşılama konumlarına atamayı en iyi duruma getirdiğinde, yalnızca mesafe dikkate alınıyordu. Mesafe maliyet ile ilişkili olabilmesine karşın maliyetle aynı değildir. Örneğin, gece sevkiyatı yöntemi aynı mesafeye yapılan üç günlük veya yedi günlük sevkiyattan daha maliyetlidir.

Maliyet yapılandırması özelliği, perakendecilerin sipariş satırlarını karşılamak için en uygun konumu belirlemek üzere hesaplanacak ve dikkate alınacak ek maliyet bileşenlerini tanımlamasına ve yapılandırmasına olanak tanır.

Maliyet bileşenleri yapılandırıldığında DOM çözücü siparişi karşılamak üzere en uygun konumu belirlemek için bu maliyet tanımlarını kullanır. Mesafe bileşenini maliyet olarak dikkate almaz. Bununla birlikte, bileşenler yapılandırılmazsa DOM çözücü siparişi karşılamak üzere en uygun konumu belirlemek için mesafe bileşenini maliyet olarak kullanır.

## <a name="set-up-cost-components"></a>Maliyet bileşenlerini ayarlama

Sistemde iki ana maliyet bileşeni türü tanımlanabilir: **Sevkiyat** ve **Diğer**.

Her iki maliyet bileşeni türü de aşağıdaki tabloda gösterildiği gibi çoklu hesaplama esaslarını destekler.

<table>
<thead>
<tr>
<th>Maliyet bileşeni türü</th>
<th>Hesaplama esası</th>
</tr>
</thead>
<tbody>
<tr>
<td>Sevkiyat</td>
<td>
<ul>
<li>Basit</li>
<li>Katmanlı</li>
</ul>
</td>
</tr>
<tr>
<td>Diğer</td>
<td>
<ul>
<li>Satış siparişi</li>
<li>Satış satırı</li>
<li>Konum</li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="shipping-cost-component-type"></a>Sevkiyat maliyeti bileşeni türü

Bu bölümde, **Sevkiyat** maliyeti bileşeni türü ve sevkiyat maliyetleri için hesaplama esası birleşiminin nasıl ayarlanacağı açıklanmaktadır. Ayrıca, DOM çözücünün her bir birleşimi nasıl kullandığı da açıklanmaktadır.

#### <a name="cost-component-type--shipping-and-calculation-basis--simple"></a>Maliyet bileşeni türü = Sevkiyat ve Hesaplama esası = Basit

**Sevkiyat** maliyeti bileşeni türü ve **Basit** hesaplama esası birlikte kullanılırsa bir teslimat şekline ait sevkiyat maliyeti, sabit maliyeti veya mesafeyi temel alır.

Bu birleşim için aşağıdaki alanları ayarlamanız gerekir:

- **Maliyet faktörü**: Maliyet faktörü için benzersiz bir tanımlayıcı girin.
- **Açıklama**: Maliyet faktörünün adını ve açıklamasını girin.
- **Başlangıç tarihi** ve **Bitiş tarihi**: Bu alanları, maliyet faktörünü belirli bir tarih aralığı için sınırlandırmak amacıyla kullanabilirsiniz. Bu alanları boş bırakırsanız maliyet faktörü belirsiz bir dönem için geçerli olur.
- **Etkin**: Maliyet faktörünün etkin olup olmadığını gösterir. DOM yalnızca karşılama profiliyle ilişkili olan etkin maliyet faktörlerini dikkate alır.
- **Şirket**: Maliyet faktörünün yapılandırıldığı tüzel kişiliği belirtin. Hesaplama ölçütlerinin tüm satırları aynı tüzel kişilik için olmalıdır.
- **Teslimat şekilleri**: Maliyetin yapılandırıldığı teslimat şekillerini belirtin.
- **Hesaplama türü**: Maliyetin belirli bir teslimat şekli için nasıl hesaplanacağını belirtin. İki hesaplama türü desteklenir:

    - **Sabit**: Teslimat şekli olarak düz maliyet kullanılır. Bu hesaplama türünü seçerseniz **Maliyet** alanı düz maliyeti tanımlar.
    - **Mesafe başına birim**: Teslimat şeklinin maliyeti, **Maliyet** alanında belirtilen maliyet değeri ile teslimat adresi ve konumlar arasındaki mesafe çarpılarak hesaplanır.

- **Maliyet**: Teslimat şeklinin maliyetini hesaplamak için **Hesaplama türü** alanıyla birlikte kullanılan maliyet değerini belirtin.

#### <a name="cost-component-type--shipping-and-calculation-basis--tiered"></a>Maliyet bileşeni türü = Sevkiyat ve Hesaplama esası = Katmanlı

**Sevkiyat** maliyeti bileşeni türü ve **Katmanlı** hesaplama esası birlikte kullanılırsa bir teslimat şekline ait sevkiyat maliyeti, sabit maliyeti veya mesafeyi temel alır. Ancak bu birleşimde, mesafe katmanlı bir mesafe aralığını temel alır.

Bu birleşim için aşağıdaki alanları ayarlamanız gerekir:

- **Maliyet faktörü**: Maliyet faktörü için benzersiz bir tanımlayıcı girin.
- **Açıklama**: Maliyet faktörünün adını ve açıklamasını girin.
- **Varsayılan maliyet**: Teslimat adresi ile konum arasındaki mesafe teslimat şekline ilişkin katmanlı mesafelerden herhangi birine denk düşmezse, teslimat şekli için kullanılacak maliyeti belirtin.
- **Başlangıç tarihi** ve **Bitiş tarihi**: Bu alanları, maliyet faktörünü belirli bir tarih aralığı için sınırlandırmak amacıyla kullanabilirsiniz. Bu alanları boş bırakırsanız maliyet faktörü belirsiz bir dönem için geçerli olur.
- **Etkin**: Maliyet faktörünün etkin olup olmadığını gösterir. DOM yalnızca karşılama profiliyle ilişkili olan etkin maliyet faktörlerini dikkate alır.
- **Şirket**: Maliyet faktörünün yapılandırıldığı tüzel kişiliği belirtin. Hesaplama ölçütlerinin tüm satırları aynı tüzel kişilik için olmalıdır.
- **Teslimat şekilleri**: Maliyetin yapılandırıldığı teslimat şekillerini belirtin.
- **Mesafe türü**: Katmanlı mesafe tanımının bir havayolu mesafesi mi yoksa karayolu mesafesi mi olduğunu belirtin.
- **Mesafe birimleri**: Katmanlı mesafenin ölçüldüğü birimi belirtin.
- **Başlangıçtan mesafe**: Katmanlı mesafe için başlangıç aralığını belirtin.
- **Bitişe mesafe**: Katmanlı mesafe için bitiş aralığını belirtin.
- **Hesaplama türü**: Maliyetin belirli bir teslimat şekli ve katmanlı mesafe için nasıl hesaplanacağını belirtin. İki hesaplama türü desteklenir:

    - **Sabit**: Teslimat şekli olarak düz maliyet kullanılır. Bu hesaplama türünü seçerseniz **Maliyet** alanı düz maliyeti tanımlar.
    - **Mesafe başına birim**: Teslimat şeklinin ve katmanlı mesafenin maliyeti, **Maliyet** alanında belirtilen maliyet değeri ile teslimat adresi ve konumlar arasındaki mesafe çarpılarak hesaplanır.

- **Maliyet**: Teslimat şeklinin maliyetini hesaplamak için **Hesaplama türü** alanıyla birlikte kullanılan maliyet değerini belirtin.

> [!NOTE]
> - Katmanlı mesafeler tanımladığınızda, sistem eksik veya çakışan mesafeler olmadığını doğrular.
> - Bir teslimat şekli için kullanılan mesafe türü, tüm katmanlı mesafelerde aynı olmalıdır.

### <a name="other-cost-component-type"></a>Diğer maliyet bileşeni türü

Bu bölümde, **Diğer** maliyeti bileşeni türü ve sevkiyat dışı maliyetler için diğer maliyet türü birleşiminin nasıl ayarlanacağı açıklanmaktadır. Ayrıca, DOM çözücünün her bir birleşimi nasıl kullandığı da açıklanmaktadır.

#### <a name="cost-component-type--other-and-other-cost-type--sales-order"></a>Maliyet bileşeni türü = Diğer ve Diğer maliyet türü = Satış siparişi

**Diğer** maliyet bileşeni türü ile **Satış siparişi** diğer maliyet türü satış siparişi düzeyindeki sevkiyat dışı maliyetlerin tanımlanması için kullanılır.

Bu birleşim için aşağıdaki alanları ayarlamanız gerekir:

- **Maliyet faktörü**: Maliyet faktörü için benzersiz bir tanımlayıcı girin.
- **Açıklama**: Maliyet faktörünün adını ve açıklamasını girin.
- **Başlangıç tarihi** ve **Bitiş tarihi**: Bu alanları, maliyet faktörünü belirli bir tarih aralığı için sınırlandırmak amacıyla kullanabilirsiniz. Bu alanları boş bırakırsanız maliyet faktörü belirsiz bir dönem için geçerli olur.
- **Etkin**: Maliyet faktörünün etkin olup olmadığını gösterir. DOM yalnızca karşılama profiliyle ilişkili olan etkin maliyet faktörlerini dikkate alır.
- **Maliyet**: Satış siparişi düzeyinde sevkiyat dışı bir maliyetin maliyet değerini belirtin.

#### <a name="cost-component-type--other-and-other-cost-type--sales-line"></a>Maliyet bileşeni türü = Diğer ve Diğer maliyet türü = Satış satırı

**Diğer** maliyet bileşeni türü ile **Satış satırı** diğer maliyet türü satış satırı düzeyindeki sevkiyat dışı maliyetlerin tanımlanması için kullanılır.

Bu birleşim için aşağıdaki alanları ayarlamanız gerekir:

- **Maliyet faktörü**: Maliyet faktörü için benzersiz bir tanımlayıcı girin.
- **Açıklama**: Maliyet faktörünün adını ve açıklamasını girin.
- **Başlangıç tarihi** ve **Bitiş tarihi**: Bu alanları, maliyet faktörünü belirli bir tarih aralığı için sınırlandırmak amacıyla kullanabilirsiniz. Bu alanları boş bırakırsanız maliyet faktörü belirsiz bir dönem için geçerli olur.
- **Etkin**: Maliyet faktörünün etkin olup olmadığını gösterir. DOM yalnızca karşılama profiliyle ilişkili olan etkin maliyet faktörlerini dikkate alır.
- **Maliyet**: Satış satırı düzeyinde sevkiyat dışı bir maliyetin maliyet değerini belirtin.

#### <a name="cost-component-type--other-and-other-cost-type--location"></a>Maliyet bileşeni türü = Diğer ve Diğer maliyet türü = Konum

**Diğer** maliyet bileşeni türü ile **Konum** diğer maliyet türünün birleşimi, bir konum grubu veya tek bir konum için sevkiyat dışı maliyetleri tanımlamak amacıyla kullanılır.

Bu birleşim için aşağıdaki alanları ayarlamanız gerekir:

- **Maliyet faktörü**: Maliyet faktörü için benzersiz bir tanımlayıcı girin.
- **Açıklama**: Maliyet faktörünün adını ve açıklamasını girin.
- **Başlangıç tarihi** ve **Bitiş tarihi**: Bu alanları, maliyet faktörünü belirli bir tarih aralığı için sınırlandırmak amacıyla kullanabilirsiniz. Bu alanları boş bırakırsanız maliyet faktörü belirsiz bir dönem için geçerli olur.
- **Etkin**: Maliyet faktörünün etkin olup olmadığını gösterir. DOM yalnızca karşılama profiliyle ilişkili olan etkin maliyet faktörlerini dikkate alır.
- **Karşılama grubu**: Sevkiyat dışı maliyetin tanımlandığı konum gruplarını belirtin.
- **Karşılama konumu**: Sevkiyat dışı maliyetin tanımlandığı konumu belirtin.

    > [!NOTE]
    > Konum tabanlı hesaplama ölçütleri için aynı satırda bir karşılama grubu ve karşılama konumu belirtemezsiniz.

- **Maliyet**: Karşılama grubu düzeyi veya karşılama konumu düzeyinde sevkiyat dışı maliyetin maliyet değerini belirtin.

> [!IMPORTANT]
> DOM'ın çalıştırıldığında bu maliyetleri dikkate alması için maliyet faktörünü ilgili karşılama profiline eklemeniz gerekir.
