---
title: Maliyetlendirme parametresi değerleri kurulumu
description: Varış yeri maliyeti modülünü ayarladığınızda, uygulamanın diğer bölümlerinde belirli maliyetlendirme parametresi değerleri türlerini seçtiğinizde kullanılabilecek birkaç ortak değer kümesi tanımlayabilirsiniz. Bu konuda, bu değer kümelerinin nasıl ayarlanacağı açıklanmaktadır.
author: Weijiesa
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMCostTypeTable, ITMCostTypeGroup, ITMCostTransferGroup, ITMCostTemplateTable, ITMVolumetricDivisorTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ed20181201a2f3f84c3dc08549f4f107d46a50a2
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689761"
---
# <a name="costing-parameter-values-setup"></a>Maliyetlendirme parametresi değerleri kurulumu

[!include [banner](../../includes/banner.md)]

**Varış yeri maliyeti** modülünü ayarladığınızda, değer başına birkaç ortak değer kümesi ve ilgili ayarlar tanımlayabilirsiniz. Bu değerler daha sonra uygulamanın diğer bölümlerinde belirli maliyetlendirme parametresi değerleri seçtiğinizde kullanılabilir. Bu konuda, bu değer kümelerinin nasıl ayarlanacağı açıklanmaktadır.

## <a name="set-up-cost-type-codes"></a>Maliyet türü kodlarını ayarlama

Maliyet türü kodları, mallar ambara vardığında oluşan maliyetin türünü veya seyahatin varış yeri maliyetlerini belirler. Genellikle malların değerini artırsalar da tutarları genel muhasebeye tahakkuk ettirmek için de kullanılabilirler. Genel muhasebe ayarlamaları, bir maliyet zaman içinde veya bir dizi seyahat sırasında tahakkuk ettiğinde ve tek bir harekette mahsup edildiğinde kullanılır.

> [!NOTE]
> Maliyet türü tablosu tüzel kişilikler arasında paylaşılıyorsa hesap planının tüzel kişilikler arasında da paylaşılması gerekir. Aksi takdirde, deftere nakil hareketleri düzgün çalışmaz.

Maliyet türü kodlarınızı ayarlamak için **Varış yeri maliyeti \> Maliyetlendirme kurulumu \> Maliyet türü kodları**'na gidin. Yeni maliyet türü kodları oluşturmak, var olan kodları düzenlemek veya seçili maliyet türünü silmek için Eylem Bölmesindeki düğmeleri kullanabilirsiniz.

Aşağıdaki tabloda, her maliyeti türü kodunda kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Maliyet türü kodu | Maliyet türü kodu için bir ad girin. |
| Tanım | Maliyet türü kodu için açıklama girin. |
| Sevkiyat oranını kullan | Bu maliyetlerin değerini hesaplamak için seyahat döviz kurunun (bazen yönetim oranı olarak da adlandırılır) kullanılması gerekiyorsa bu seçeneği *Evet* olarak ayarlayın. Bu durumda, döviz faturalarını değiştirmek için standart varsayılan veya spot döviz kuru yerine sevkiyat ücreti kullanılır. |
| Raporlama kategorisi | Bu alan, maliyet türü için bir raporlama kategorisi oluşturur. Raporlar, raporlama kategorilerine veya maliyet türüne göre yazdırılabilir. |
| Borç türü | Maliyet türünün maddeyi, genel muhasebe hesabını mı yoksa satıcıyı mı borçlandırması gerektiğini seçin. |
| Deftere borç nakli | **Borç türü** alanı, *Genel muhasebe hesabı* olarak ayarlanmışsa deftere nakil açıklamasını seçin. |
| Borç hesabı | **Borç türü** alanı, *Genel Muhasebe hesabı* olarak ayarlanmışsa kullanılacak genel muhasebe hesabını seçin. |
| Alacak türü | Maliyet türünün maddeyi, genel muhasebe hesabını mı yoksa satıcıyı mı alacaklandırması gerektiğini seçin. |
| Deftere alacak nakli | **Alacak türü** alanı, *Genel muhasebe hesabı* olarak ayarlanmışsa deftere nakil açıklamasını seçin. |
| Alacak hesabı | **Alacak türü** alanı, *Genel Muhasebe hesabı* olarak ayarlanmışsa kullanılacak genel muhasebe hesabını seçin. |
| Kliring hesabı | Maliyet türü için kliring hesabını seçin. Mutabakata yardımcı olmak için maliyet türü başına ayrı bir kliring hesabı belirtmenizi öneririz. |
| Standart maliyet deftere nakil türü | Standart maliyetlendirme kullanıyorsanız deftere nakil açıklamasını seçin. |
| Standart maliyet farkı hesabı | <p>Standart maliyetlendirme kullanıyorsanız burada belirtilen hesap herhangi bir farkı deftere nakletmek için kullanılır. Bu hesap, **Madde fiyatları** sayfasındaki sabitlenmiş maliyet dökümünü kullanır. Bu döküm, fiyatları güncelleştirmek için periyodik düzen kullanılarak oluşturulur.</p><p>Örneğin, bir maddenin standart maliyeti 15,00 TL, FOB 13,00 TL ve navlun 2,00 TL'dir. Fatura stok için alındığında, madde 15,00 TL olarak alınır ancak gerçek FOB 13,00 TL olduğundan, madde için 2,00 TL standart fiyat farkı oluşur. Bu fark, madde deftere nakil profilinde ayarlanan standart fiyat farkı hesabına nakledilir. Tahmini navlun 2,00 TL olduğundan stok faturası deftere nakledildiğinde fark oluşmaz. Ancak navlun faturası alındığında, navlun birim başına 2,50 TL'dir. Bu nedenle, belirtilen maliyete 0,50 TL'lik bir fark nakledilir. |
| Hareketli ortalama fark hesabı | <p>Hareketli ortalama maliyetlendirmesi kullanıyorsanız burada belirtilen hesap herhangi bir farkı deftere nakletmek için kullanılır.</p><p>Örneğin, tahmini navlun 2,00 TL'dir. Ancak navlun faturası alındığında, navlun birim başına 2,50 TL'dir. Bu nedenle, 0,50 TL'lik bir fark deftere nakledilmelidir.</p><p>**Varış yeri maliyeti parametreleri** sayfasında **Ayarlamaları fark olarak deftere naklet** seçeneği *Evet* olarak ayarlandığında, tahmini ve fiili sevkiyat maliyetleri arasındaki tüm farklar burada belirtilen hareketli ortalama fark hesabına nakledilir. **Ayarlamaları fark olarak deftere naklet** seçeneği *Hayır* olarak ayarlandığında, standart işlevsellik kullanılır ve fark, eldeki stoka bağlı olarak stoka veya burada belirtilen hareketli ortalama fark hesabına uygulanır.</p> |
| Masraf tahakkuk hesabı | Satın alma faturası deftere nakledildiğinde maliyet tahminlerinde tahakkuk etmek için kullanılan hesabı seçin. Bu alan yalnızca **Varış yeri maliyeti parametreleri** sayfasının **Genel** sekmesindeki **Maliyetlendirme** hızlı sekmesinde **Maliyet türü masraf tahakkuk hesabını kullan** seçeneği *Evet* olarak ayarlandığında kullanılır. |
| Masraf hesabı | Bir tedarikçi tarafından faturalanan gelen taşıma maliyetlerini yakalamak için kullanılan hesabı seçin. Tutar borç olarak deftere nakledilir. Mahsup hesap, stok farkı hesabıdır. Bu deftere nakil, yalnızca **Borç hesapları parametreleri** sayfasında **Genel muhasebedeki hesabı borçlandırmak için deftere naklet** seçeneği *Evet* olarak ayarlandığında kullanılır. |
| Fark hesabı | Satın alma faturası deftere nakledildiğinde gider tahakkuklarında gideri mahsup etmek için kullanılacak hesap. Bu alan yalnızca **Varış yeri maliyeti parametreleri** sayfasının **Genel** sekmesindeki **Maliyetlendirme** hızlı sekmesinde **Maliyet türü masraf tahakkuk hesabını kullan** seçeneği *Evet* olarak ayarlandığında kullanılır. |

## <a name="vendor-cost-type-groups"></a>Satıcı maliyet türü grupları

Satıcı maliyet türü grupları, *otomatik maliyet* giderlerinin nasıl bulunduğunu ve bir seyahate nasıl uygulandığını belirlemeye yardımcı olun. Benzer ithalat maliyetlerine sahip satıcılar birbirine bağlıdır. Örneğin, gelişmekte olan pazarlardaki tüm satıcılar, yerleşik bir pazardan satın alınan aynı ürün türü için aynı vergi yüzdesini öder.

**Varış yeri maliyeti \> Maliyet kurulumu \> Satıcı maliyet türü grupları**'na giderek satıcı maliyet türü gruplarını koruyabilirsiniz. **Satıcı maliyet türü grupları** sayfası, var olan tüm satıcı maliyet türü gruplarını listeleyen bir kılavuz sağlar. Kılavuza satır eklemek, kaldırmak ve düzenlemek için Eylem Bölmesindeki düğmeleri kullanabilirsiniz.

Aşağıdaki tabloda, kılavuzdaki her satırda kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Satıcı maliyet türü grupları | Satıcı maliyet türü grubu için benzersiz bir ad girin (*Gelişmekte olan pazarlar* gibi). |
| Tanım | Satıcı maliyet türü grubu için açıklama girin. Bu açıklama, satıcı grubuyla ilişkili gider düzeyi veya türü hakkında ayrıntılı bilgi sağlayabilir. |

## <a name="item-cost-type-groups"></a>Madde maliyet türü grupları

Madde maliyet türü grupları, *otomatik maliyet* giderlerinin nasıl bulunduğunu ve bir seyahate nasıl uygulandığını belirlemeye yardımcı olun. Benzer öğeler birbirine bağlanır. Örneğin, vergi oranı yüzde 5 olan tüm maddeler belirli bir maliyet türü grubuna ait olabilir.

**Varış yeri maliyeti \> Maliyet kurulumu \> Madde maliyet türü grupları**'na giderek madde maliyet türü gruplarını koruyabilirsiniz. **Madde maliyet türü grupları** sayfası, var olan tüm madde maliyet türü gruplarını listeleyen bir kılavuz sağlar. Kılavuza satır eklemek, kaldırmak ve düzenlemek için Eylem Bölmesindeki düğmeleri kullanabilirsiniz.

Aşağıdaki tabloda, kılavuzdaki her satırda kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Madde maliyet türü grupları | Madde maliyet türü grubu için benzersiz bir ad girin (*%5 Vergi* gibi). |
| Tanım | Madde maliyet türü grubu için açıklama girin. Bu açıklama, madde grubuyla ilişkili gider düzeyi veya türü hakkında ayrıntılı bilgi sağlayabilir. |

> [!NOTE]
> Madde maliyet türü, maddenin **Piyasaya sürülen ürün** sayfasının **Satın alma** hızlı sekmesindeki **Maliyet türü grubu** alanı aracılığıyla maddeye bağlanır.

## <a name="transfer-order-cost-type-groups"></a>Transfer emri maliyet türü grupları

Transfer emri maliyet türü grupları, *otomatik maliyet* giderlerinin nasıl bulunduğunu belirlemeye yardımcı olun. Benzer öğeler birbirine bağlanır. Örneğin, vergi oranı yüzde 7 olan tüm maddeler belirli bir maliyet türü grubuna ait olabilir.

**Varış yeri maliyeti \> Maliyet kurulumu \> Transfer emri maliyet türü grupları**'na giderek transfer emri maliyet türü gruplarını koruyabilirsiniz. **Transfer emri maliyet türü grupları** sayfası, var olan tüm transfer emri maliyet türü gruplarını listeleyen bir kılavuz sağlar. Kılavuza satır eklemek, kaldırmak ve düzenlemek için Eylem Bölmesindeki düğmeleri kullanabilirsiniz.

Aşağıdaki tabloda, kılavuzdaki her satırda kullanılabilecek ayarlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Transfer emri maliyet türü grupları | Transfer emri maliyet türü grubu için benzersiz bir ad girin (*%7 Vergi* gibi). |
| Tanım | Transfer emri maliyet türü grubu için açıklama girin. Bu açıklama, transfer emri maliyet türü grubuyla ilişkili gider düzeyi veya türü hakkında ayrıntılı bilgi sağlayabilir. |

> [!NOTE]
> Transfer emri maliyet türü, maddenin **Piyasaya sürülen ürün** sayfasının **Satın alma** hızlı sekmesindeki **Transfer emri maliyet grubu** alanı aracılığıyla maddeye bağlanır.

## <a name="cost-templates"></a>Maliyet şablonları

Maliyet tahminini alan kullanıcıların bilmeyebileceği ayarların varsayılan değerlerini ayarlamak için maliyet şablonlarını kullanabilirsiniz. Maliyet şablonları, kullanıcıların doğru bir tahmin elde etmek için yapması gereken seçimleri en aza indirerek tahmin sürecindeki karmaşıklığı azaltmaya yardımcı olabilir.

Maliyet şablonlarıyla çalışmak için **Varış yeri maliyeti \> Maliyetlendirme kurulumu \> Maliyet şablonları**'na gidin. **Maliyet şablonları** sayfasında, soldaki liste bölmesi tüm geçerli maliyet şablonlarını gösterir. Şablon eklemek, kaldırmak ve düzenlemek için Eylem Bölmesindeki düğmeleri kullanabilirsiniz.

Aşağıdaki tabloda, her şablonda kullanılabilecek ayarlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Maliyet şablonu | Maliyet şablonu için benzersiz bir ad girin. Ad genellikle şablonun faktörünü veya maliyet çarpanını açıklar. |
| Tanım | Maliyet şablonu için açıklama girin. |
| Sevkiyat şirketi | Maliyet şablonuyla ilişkilendirilecek sevkiyat şirketinin satıcı hesabını seçin. |
| Teslimat şekli | Bir maddenin tahmini maliyeti hesaplandığında maliyet şablonunun kullanması gereken teslimat şeklini seçin. Bu alan, maliyet tahmininde mallarla ilişkili otomatik maliyetlerin belirlenmesine yardımcı olur. |
| Sevkiyat konteyneri türü | Maliyet şablonuyla ilişkilendirilecek sevkiyat konteyneri türünü seçin. Bu alan, maliyet tahmininde mallarla ilişkili otomatik maliyetlerin belirlenmesine yardımcı olur. |
| Gümrük müşaviri | Maliyet şablonuyla ilişkilendirilecek gümrük müşavirini (satıcı) seçin. Bu alan, maliyet tahminiyle ilişkili otomatik maliyetlerin belirlenmesine yardımcı olur. |
| Faktör | Malların son maliyet tahminine uygulanacak bir faktör girin. Örneğin, hesaplanan maliyet tahminine yüzde 10 eklemek için *1,10* girin. |

## <a name="volumetric-divisors"></a>Hacimsel bölenler

Hacimsel ağırlığı hesaplamak için hacimsel bölenler kullanılır. Her sevkiyat/sevkiyat şirketi kendi hacimsel bölenlerini belirler. Buna ek olarak, bir şirketin bölenleri genellikle teslimat şekline bağlı olarak değişir. Örneğin, hava ve deniz genellikle çok farklı bölenlere sahiptir. Bir şirket, sevkiyatın nereden yapıldığına bağlı olarak kurallarını daha karmaşık hale getirebilir. Sistem, volümetrik ağırlığını bulmak için aşağıdaki formülü kullanır: VolumetricWeight = Hacim ÷ VolumetricDivisor.

Örneğin, hava yoluyla gönderilen bir paket 3 metreküp (m³) hacme sahiptir. Şirket hacimsel ağırlıkla ücret alır ve 6 hacimsel bölenini uygular. Bu bölen, hacimsel ağırlığı belirlemek için hacimle bölünür. Bu nedenle, bu örnek için hacimsel ağırlık 3 ÷ 6 = 0.5 kilogramdır (kg).

Hacimsel bölenleri ayarlamak için **Varış yeri maliyeti \> Maliyetlendirme kurulumu \> Hacimsel bölenler**'e gidin. **Hacimsel bölenler** sayfası, var olan tüm hacimsel bölenleri listeleyen bir kılavuz sağlar. Kılavuza satır eklemek, kaldırmak ve düzenlemek için Eylem Bölmesindeki düğmeleri kullanabilirsiniz.

Aşağıdaki tabloda, kılavuzdaki her satırda kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Sevkiyat şirketi | Hacimsel bölenle ilişkili sevkiyat şirketinin satıcı hesabını seçin. |
| Maliyet türü kodu | Hacimsel bölenle ilişkili maliyet türü kodunu seçin. Maliyet türlerini raporlama paketlerine koymak için bu alanı kullanın. Raporlar, raporlama kategorilerine veya maliyet türüne göre yazdırılabilir. |
| Çıkış limanı | Hacimsel bölenin uygulandığı "çıkış" limanını seçin. |
| Hacimsel bölen | Satıra uygulanan hacimsel bölen değerini girin. Her bir paketin hacmi, paketin hacimsel ağırlığını belirlemek için buraya girdiğiniz değere bölünür. |

> [!NOTE]
> Sistem **fiili ağırlık** ve **hacimsel ağırlık** arasındaki maksimum değeri kullanır.
