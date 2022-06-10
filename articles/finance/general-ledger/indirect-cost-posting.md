---
title: Dolaylı maliyet nakli
description: Bu konuda, dolaylı maliyetleri deftere nakletme, maliyet grupları oluşturma ve dolaylı maliyetler için maliyetlendirme tablosuna düğüm ekleme işlemleri açıklanmaktadır.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: CostSheetDesigner, BOMCostGroup, ProjCategory, CostingVersion, CostSheetCalculationFactor
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: d7f4753f69d83d172993e1c9b04be2220fdf253f
ms.sourcegitcommit: 1ea145dc606e243c7f51d91a5c0dd9e385bbda4a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/25/2022
ms.locfileid: "8804629"
---
# <a name="indirect-cost-posting"></a>Dolaylı maliyet nakli

Dolaylı maliyetler, üretim sürecindeki herhangi bir tek faaliyetle doğrudan ilişkili olmayan maliyetlerdir. Örnek olarak çalışan maaşları ve muhasebe departmanı maliyetleri gibi yönetim maliyetleri ile kira, kamu hizmetleri ve makine maliyetleri gibi genel gider maliyetleri verilebilir.

## <a name="calculating-indirect-costs"></a>Dolaylı maliyetleri hesaplama

Microsoft Dynamics 365 Finance, dolaylı maliyetlerin oranını hesaplamak için otomatik bir yöntem içermez. Dolaylı maliyetlerinizi belirlemeniz, dolaylı maliyet kodları oluşturmanız ve maliyetlendirme tablosunda her dolaylı maliyetin oranını ayarlamanız gerekir.

Dolaylı maliyetleri hesaplamak için kullanılan işlem, şirketten şirkete değişiklik gösterebilir. Ancak genel olarak, işlem aşağıdaki temel adımlardan oluşur:

1. Üretimde dikkate alınması gereken dolaylı maliyetlerin listesini oluşturun. Bu listeye kira, yönetim giderleri, muhasebe ücretleri ve yasal ücretler dahil olabilir. Üretim rotalarında dikkate alınan ham madde maliyetlerini veya işçilik maliyetlerini içermemelidir.
2. Tüm dolaylı maliyetleri toplayın. Benzer türdeki dolaylı maliyetleri gruplandırabilir veya bunları birbirinden ayrı tutabilirsiniz. Yapılandırılan her dolaylı maliyet, genel muhasebeye nakletmek için kullanılan farklı ana hesaplara sahip olabilir.
3. Dolaylı maliyetleri bir faktörle karşılaştırın. Bu işlem içe alma temeli olarak da adlandırılır. Faktör, seçtiğiniz her şey olabilir. Burada birkaç genel örnek verilmiştir:

    - Gelir
    - Üretilen toplam miktar
    - Hazırlık süresi
    - Çalıştırma

    Dolaylı maliyetlerinizi hesaplamak istediğiniz dönemi (ör. aylık, üç aylık veya yıllık) seçebilirsiniz. Dolaylı maliyetlerinizin toplamı ve faktörlerinizin toplamı aynı süre için olmalıdır. Dolaylı maliyet oranını hesaplamak için aşağıdaki formül kullanılır:

    *Dolaylı maliyet oranı* = *Toplam dolaylı maliyet giderleri* &divide; *Toplam faktör*

4. Dolaylı maliyet grupları oluşturun.
5. Oranlarınızı kullanarak maliyetlendirme tablosunu yapılandırın.
6. Maliyetlendirme sürümünde dolaylı maliyetlerinizin maliyetini koruyun.

> [!NOTE]
> Maliyetleri biriktirmek ve üretim, projeler ve genel muhasebe gibi farklı kaynaklara ilişkin genel giderinizi belirlemek için **Maliyet muhasebesi** modülünü kullanabilirsiniz. Daha fazla bilgi için bkz. [Maliyet muhasebesi](/cost-accounting/cost-accounting-home-page.md).

> [!IMPORTANT]
> Farklı mevzuat kurumları, mamul malların maliyeti için dolaylı maliyet veya genel gider olarak eklenebilecek maliyet türleriyle ilgili kılavuzlar yayımlamıştır. Dolaylı maliyetleri yapılandırmadan önce kılavuzlara uyum sağlamak için muhasebe departmanınızla ve yerel mevzuat kurumlarıyla görüşmenizi öneririz.

## <a name="create-cost-groups-for-indirect-costs"></a>Dolaylı maliyetler için maliyet grupları oluşturma

Dolaylı maliyetler için kullanılacak en az bir maliyet grubu oluşturmanız gerekir. Kullanabileceğiniz maliyet grubu sayısında bir sınır yoktur. Maliyetlerinizi nasıl hesaplayacağınızı ve farklı maliyet türleri için farklı oranlar olup olmadığını dikkate alın. Örneğin, kuruluşunuzun gıda ürünleri imal ettiğini varsayalım. Bazı ham madde ve mamul mallar, kuru mallardır ve depolama için bir dolaylı maliyet vardır. Diğer ham madde ve mamul mallar, dondurulmuş durumdadır ve daha yüksek dolaylı maliyete sahiptir. Bu durumda, iki maliyet grubu oluşturmak isteyebilirsiniz: **Kuru malzeme genel gideri** ve **Dondurulmuş malzeme genel gideri**.

Dolaylı maliyetler için maliyet grubu oluşturmak üzere bu adımları izleyin.

1. **Üretim denetimi &gt; Kurulum &gt; Rotalar &gt; Maliyet grupları**'na gidin.
2. Grup oluşturmak için **Yeni**'yi seçin.
3. **Maliyet grubu** alanına, maliyet grubu için benzersiz bir ad (ör. **MATOVH**) girin.
4. **Ad** alanına, maliyet grubunun bir açıklamasını (ör. **Malzeme genel gideri**) girin.
5. **Maliyet grubu türü** alanında, **Dolaylı** seçeneğini belirleyin.
6. İsteğe bağlı: **Davranış** alanında, **Sabit maliyet** veya **Değişken maliyet** seçeneğini belirleyin.

## <a name="configure-the-costing-sheet-for-indirect-costs"></a>Dolaylı maliyetler için maliyetlendirme tablosunu yapılandırma

Bir veya daha fazla maliyet grubu oluşturduktan sonra, maliyetlendirme tablonuzu dolaylı maliyetlerle yapılandırabilir ve hesaplamanızı tanımlayabilirsiniz. Maliyetlendirme tablosunda dolaylı maliyetleri gruplandırmak isteyebilirsiniz. Dolaylı maliyetleri gruplandırmak için, maliyetlendirme tablosunda isteğe bağlı bir üst bilgi oluşturabilirsiniz. Maliyetlendirme tablosunda her maliyet grubu için en az bir düğüm oluşturmanız gerekir. Dolaylı maliyetlere ilişkin her maliyet grubu için bir tane daha dolaylı maliyet hesaplaması ekleyebilirsiniz.

### <a name="indirect-cost-node-types"></a>Dolaylı maliyet düğümü türleri

Bu bölümde, dolaylı maliyetlere ait farklı düğüm türleri açıklanmıştır.

#### <a name="surcharge"></a>Ek maliyet

**Ek maliyet**, dolaylı maliyetlerin en yaygın türlerinden biridir. Maliyet yüzdesini, üretim emrindeki maliyetlerin içe alınması temelinde hesaplar. İçe alma temelini, maliyetlendirme tablosunda malzemenize bağlı maliyet gruplarını veya süre bileşenlerini seçerek tanımlarsınız.

Örneğin, bir üretim emrindeki tüm ham maddeler için üretim maliyetine yüzde 3 ek maliyet eklenebilir.

#### <a name="rate"></a>Ücret

**Oran** türündeki dolay maliyet, üretim emrindeki maliyet içe alma temelinden üretim emrine sabit tutarda maliyet eklemek için kullanılır. Oran, üç alt türden birini temel alabilir:

- **İşlem**: Oran, rotadaki çalışma süresine bağlıdır.
- **Kurulum**: Oran, rotadaki kurulum süresine bağlıdır.
- **Miktar**: Oran, üretilen miktara bağlıdır.

İçe alma temelini, maliyetlendirme tablosunda malzemeye bağlı maliyet gruplarını veya süre bileşenlerini seçerek tanımlarsınız.

Örneğin, maliyetlendirme tablonuzdaki işçilik maliyeti grubu için rotadaki çalıştırma süresine bağlı olarak her üretim emrine 2,00 ABD doları (USD) değerinde sabit tutar eklenir.

#### <a name="output-unit-based"></a>Çıkış birimi tabanlı

**Çıkış birimi tabanlı** türündeki dolaylı maliyet, maliyetlendirme tablosundaki **Oran** hızlı sekmesinde belirtilen tutarın seçili alt türle çarpımı sonucunda hesaplanır. Dolaylı maliyetin çarpanı olarak mamul malın miktarını, ağırlığını veya hacmini seçebilirsiniz.

Örneğin, üretilen her miktar için 1,50 USD değerinde makine amortismanı hesaplamak için miktarı kullanırsınız. Başka bir örnek olarak, mamul malların soğutma birimlerinizde kapladığı hacim için 2,00 USD değerinde soğutma maliyeti hesaplamak için hacmi kullanırsınız.

#### <a name="input-unit-based"></a>Giriş birimi tabanlı

**Giriş birimi tabanlı** türündeki dolaylı maliyet, bir üretim emrinde tüketilen ham madde miktarıyla belirli bir miktarın çarpılması sonucunda hesaplanır. Toplamı hesaplamak için, üretim emrindeki girişlerin ağırlığını veya hacmini kullanabilirsiniz. Maliyetlendirme tablosunun **İçe alma temeli** hızlı sekmesinde bir veya daha fazla maliyet grubu seçerek hesaplamayı malzemelerin alt kümesiyle sınırlandırabilirsiniz.

Örneğin, bir üretim emrine 1,00 USD eklemek için dondurulmuş ürünlerle bağlantılı belirli bir maliyet grubunun giriş hacmini kullanırsınız.

### <a name="create-a-total-node-for-indirect-costs-in-the-costing-sheet"></a>Maliyetlendirme tablosunda dolaylı maliyetler için toplam düğümü oluşturma

Maliyetlendirme tablosunda dolaylı maliyetlere yönelik bir toplam düğümü oluşturmak için aşağıdaki adımları izleyin.

1. **Maliyet yönetimi &gt; Dolaylı maliyet muhasebesi politikaları kurulumu &gt; Maliyetlendirme tablosu**'na gidin.
2. Ağaçta, üretilen malların maliyetini temsil eden bir düğüm seçin.
3. Düğüm oluşturmak için **Yeni**'yi seçin.
4. **Düğüm türünü seç** alanında, **Toplam**'ı seçin.
5. **Kod** alanında, düğüm için benzersiz bir kimlik (ör. **Üretim Genel Giderleri**) girin.
6. **Üst Bilgi** onay kutusunu seçin.
7. **Toplam** onay kutusunu seçin.
8. **Tamam**'ı seçin.

### <a name="create-an-indirect-cost-group-node-in-the-costing-sheet"></a>Maliyetlendirme tablosunda dolaylı maliyet grubu düğümü oluşturma

Maliyetlendirme tablosunda dolaylı maliyet grubu düğümü oluşturmak için aşağıdaki adımları izleyin.

1. **Maliyet yönetimi &gt; Dolaylı maliyet muhasebesi politikaları kurulumu &gt; Maliyetlendirme tablosu**'na gidin.
2. Ağaçta, dolaylı maliyeti oluşturmak istediğiniz düğümü seçin. Örneğin, **Üretim genel gideri** için toplam düğümünü seçin.
3. Düğüm oluşturmak için **Yeni**'yi seçin.
4. **Düğüm türünü seç** alanında, **Maliyet grubu** seçeneğini belirleyin.
5. **Kod** alanında, düğüm için benzersiz bir kimlik (ör. **TRANSP**) girin.
6. **Açıklama** alanında, **Taşımacılık genel gideri** gibi kısa bir açıklama girin.
7. **Tamam**'ı seçin.
8. **Maliyet grubu** alanında, maliyet grubunu (ör. **OVH1: Taşımacılık genel gideri**) seçin.

### <a name="create-a-surcharge-indirect-cost"></a>Ek masraf dolaylı maliyeti oluşturma

Maliyetlendirme tablonuzda ek masraf dolaylı maliyeti oluşturmak için aşağıdaki adımları izleyin.

1. **Maliyet yönetimi &gt; Dolaylı maliyet muhasebesi politikaları kurulumu &gt; Maliyetlendirme tablosu**'na gidin.
2. Ağaçta, dolaylı maliyeti oluşturmak istediğiniz dolaylı maliyet grubu düğümünü seçin. Örneğin, **TRANSP - Taşımacılık Genel Gideri** için toplam düğümünü seçin.
3. Düğüm oluşturmak için **Yeni**'yi seçin.
4. **Düğüm türünü seç** alanında, **Ek maliyet**'i seçin.
5. **Kod** alanında, düğüm için benzersiz bir kimlik (ör. **Taşımacılık Ek Maliyeti**) girin.
6. **Tamam**'ı seçin.
7. **Alt tür** alanında, **Toplam**'ı seçin.
8. **İçe alma temeli** hızlı sekmesinde yeni bir maliyet kodu oluşturmak için **Yeni**'yi seçin.
9. **Kod** alanında, ek maliyeti hesaplamak için kullanılacak bir maliyet grubu seçin.
10. İsteğe bağlı: Hesaplamada kullanmak istediğiniz her ek maliyet grubu için 8-9 arasındaki adımları yineleyin.
11. **Ek maliyet** hızlı sekmesinde oran oluşturmak için **Yeni**'yi seçin.
12. **Sürüm** alanında, ek maliyetin ekleneceği maliyetlendirme sürümünü seçin.
13. İsteğe bağlı: **Tesis** alanında, ek maliyetin uygulanacağı tesisi girin.
14. **Yüzde** alanında, **İçe alma temeli** hızlı sekmesinde tanımlanan maliyet gruplarından üretim emirlerini hesaplamak için yüzdeyi girin.
15. **Genel muhasebe nakilleri** hızlı sekmesinde; **Mahsup edilen tahmini dolaylı maliyet**, **Tüketilen dolaylı maliyetin tahmini maliyeti, Süren İş**, **Mahsup edilen dolaylı maliyet** ve **Tüketilen dolaylı maliyetin maliyeti, Süren İş** alanları için kullanılacak ana hesabı seçin.
16. İsteğe bağlı: **Mali boyutlar** hızlı sekmesinde, genel muhasebeye nakledildiklerinde hareketler için varsayılan olarak girilecek mali boyutları belirtin.

Önceki yordamda, **Ek maliyet** türünde dolaylı maliyetin nasıl oluşturulacağı gösterilmektedir. Diğer dolaylı maliyet türlerini oluşturmak için benzer adımlar kullanılır. Aşağıdaki bölümlerde her bir türe ilişkin farklılıklar açıklanmaktadır.

#### <a name="rate"></a>Ücret

- 4. adımda, **Ek maliyet** yerine **Oran**'ı seçin.
- 7. adımda, **Toplam** yerine **İşlem**, **Kurulum** veya **Miktar** seçin.
- 11. adımda, **Ek maliyet** hızlı sekmesi yerine **Oran** hızlı sekmesini kullanın.
- 14. adımda, **Yüzde** alanına yüzde oranı girmek içine **Tutar** alanına tutar girin.

#### <a name="output-unit-based"></a>Çıkış birimi tabanlı

- 4. adımda, **Ek maliyet** yerine **Çıkış birimi tabanlı**'yı seçin.
- 7. adımda, **Toplam** yerine **Miktar**, **Ağırlık** veya **Hacim** seçin.
- 8 ile 10 arasındaki adımları atlayın.
- 11. adımda, **Ek maliyet** hızlı sekmesi yerine **Oran** hızlı sekmesini kullanın.

#### <a name="input-unit-based"></a>Giriş birimi tabanlı

- 4. adımda, **Ek maliyet** yerine **Giriş birimi tabanlı**'yı seçin.
- 7. adımda, **Toplam** yerine **Ağırlık** veya **Hacim** seçin.
- 11. adımda, **Ek maliyet** hızlı sekmesi yerine **Oran** hızlı sekmesini kullanın.
