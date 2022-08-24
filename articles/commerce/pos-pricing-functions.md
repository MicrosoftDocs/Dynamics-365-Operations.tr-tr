---
title: POS'taki fiyatlandırma işlevleri
description: Bu makalede, Microsoft Dynamics 365 Commerce satış noktası (POS) uygulamasındaki çeşitli fiyat ve iskonto işlevleri açıklanmaktadır.
author: boycez
ms.date: 08/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2022-07-14
ms.openlocfilehash: 92bbc3b81b889f106dc113528afbdc37d1106ff3
ms.sourcegitcommit: 924dbcdc6b03f6a7ae3a07378ec405fd15c7e359
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2022
ms.locfileid: "9294136"
---
# <a name="pricing-functions-in-pos"></a>POS'taki fiyatlandırma işlevleri

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce satış noktası (POS) uygulamasındaki çeşitli fiyat ve iskonto işlevleri açıklanmaktadır.

Dynamics 365 Commerce POS uygulaması, ön saflarda çalışanların Store Commerce işlemlerini gerçekleştirmesini sağlayan zengin yetenekler sağlar. Aşağıdaki tablo, uygulamada şu anda kullanılabilir olan fiyat ve iskonto işlevlerini gösterir.

| İşlev                       | POS işlemleri |
|--------------------------------|----------------|
| Fiyatları görüntüle                    | [Fiyat denetimi](#price-check) |
| İskontoları görüntüle                 | [Tüm iskontoları görüntüle](#view-all-discounts)<br>[Kullanılabilir iskontoları görüntüle](#view-available-discounts) |
| Fiyatları geçersiz kıl                | [Fiyat geçersiz kılma](#price-override) |
| İskontoları uygula veya kaldır      | [Satır iskonto tutarı](#line-discount-amount)<br>[Satır iskonto yüzdesi](#line-discount-percent)<br>[Toplam iskonto tutarı](#total-discount-amount)<br>[Toplam iskonto yüzdesi](#total-discount-percent)<br>[Sistem iskontolarını hareketten kaldır](#remove-system-discounts-from-transaction)<br>[Sistem iskontolarını yeniden uygula](#reapply-system-discounts) |
| Kuponları uygula veya kaldır        | [Kupon kodunu ekle](#add-coupon-code)<br>[Kupon kodunu kaldır](#remove-coupon-code) |
| Fiyatları ve indirimleri hesapla | [Yeniden hesapla](#recalculate) |

Önceki operasyonların POS uygulamasında nasıl yapılandırılabileceği ve çevrimdışı modu destekleyip desteklemedikleri hakkında bilgi için bkz. [Çevrimiçi ve çevrimdışı satış noktası (POS) operasyonları](pos-operations.md).

## <a name="price-check"></a>Fiyat denetimi

**Fiyat denetimi** işlemi, POS kullanıcılarının belirli bir ürünle ilgili önceden yapılandırılmış fiyatlara bakmasına olanak tanır.

## <a name="view-all-discounts"></a>Tüm iskontoları görüntüle

**Tüm indirimleri görüntüle** işlemi, POS kullanıcılarının, o anda mağaza kanalında çalışan tüm geçerli yükseltmeleri aramasına olanak tanır. Bu operasyon özellikle aşağıdaki koşullardan herhangi biriyle eşleşen tüm iskontoları listeler:

- İskontonun fiyat grubu, mağazanın fiyat grubuyla eşleşir.
- İskontonun fiyat grubu bir ilişki veya bağlılık programıyla eşlenir.
- İskontonun fiyat grubu, mağaza ile ilişkilendirilmiş bir katalogla eşlenir.

**Tüm iskontoları görüntüle** sayfası yalnızca halihazırda uygulanan indirimlerle rekabet etmeyen iskontoları gösterir. Bu davranış, bir satış görevlisinin müşteriyi bir iskontoyla ilgili bilgilendirmesi ve müşterinin gerekli eylemi yapması durumunda (örneğin, müşterinin yüzde 10 indirim almak için bir ürün daha satın alması), iskontonun harekete uygulanmasını sağlar. Kupon tabanlı iskontolar yalnızca **Kupon kodu olmadan uygula** parametresi açık olduğunda görüntülenir.

**Tüm iskontoları görüntüle** operasyonunda, POS kullanıcıları iskontoları ada ve açıklamaya göre arayabilir ve iskontoları kupon gerektirip gerektirmediklerine göre filtreleyebilir.

## <a name="view-available-discounts"></a>Kullanılabilir iskontoları görüntüle

**Kullanılabilir iskontoları görüntüle** işlemi, POS kullanıcılarının bir hareketteki seçili bir satıra veya tüm harekete uygun tüm indirimleri görüntülemesine olanak sağlar. Seçili bir satıra uygulanabilen iskontolar zaten uygulanmış olan iskontoları ve henüz uygulanmamış olan iskontoları içerir (örneğin, ek maddeler gerektiren karıştır ve eşle iskontoları). Geçerli bir iskonto **Kupon kodu olmadan uygula** parametresinin açık olduğu bir kupona bağlıysa POS kullanıcısı, kupon kodları veya kupon barkodları girmek veya taramak zorunda kalmadan, kuponu doğrudan kullanmak için bu operasyonun içinde **Kupon uygula** işlevini de kullanabilir.

## <a name="price-override"></a>Fiyat geçersiz kılma

**Fiyat geçersiz kılma** işlemi, POS kullanıcılarının bir hareketteki ürünün satış fiyatını geçersiz kılmasına olanak tanır. Bu işlem yalnızca fiyat geçersiz kılmalara izin vermek üzere yapılandırılan ürünler için geçerlidir.

## <a name="line-discount-amount"></a>Satır iskonto tutarı

**Satır iskonto tutarı** işlemi, POS kullanıcılarının bir hareketteki satır maddesi için indirim tutarı girmesini sağlar. Bu operasyon yalnızca, iskonto uygulanabilir maddelere uygulanır ve kullanıcı için POS izin grubunda belirtilen **Maksimum satır indirimi tutarı** değerine uyar.

## <a name="line-discount-percent"></a>Satır iskonto yüzdesi

**Satır iskonto yüzdesi** işlemi, POS kullanıcılarının bir hareketteki satır maddesi için indirim yüzdesi girmesini sağlar. Bu operasyon yalnızca, iskonto uygulanabilir maddelere uygulanır ve kullanıcı için POS izin grubunda belirtilen **Maksimum satır indirimi yüzdesi** değerine uyar.

## <a name="total-discount-amount"></a>Toplam iskonto tutarı

**Toplam iskonto tutarı** işlemi, POS kullanıcılarının bir hareket için indirim tutarı girmesini sağlar. Bu operasyon yalnızca, iskonto uygulanabilir maddelere uygulanır ve kullanıcı için POS izin grubunda belirtilen **Maksimum toplam indirim tutarı** değerine uyar. Girilen iskonto tutarı maksimum toplam iskonto tutarını aşarsa, operasyon bloke edilir ve izin geçersiz kılma akışı tetiklenmez. Şu anda, satış maddeleri ve iade maddeleri içeren karışık bir sepete toplam indirim tutarı uygulanamaz.

## <a name="total-discount-percent"></a>Toplam iskonto yüzdesi

**Toplam iskonto yüzdesi** işlemi, POS kullanıcılarının bir hareket için indirim yüzdesi girmesini sağlar. Bu operasyon yalnızca, iskonto uygulanabilir maddelere uygulanır ve kullanıcı için POS izin grubunda belirtilen **Maksimum toplam indirim yüzdesi** değerine uyar. Girilen iskonto yüzdesi maksimum toplam iskonto yüzdesini aşarsa, operasyon bloke edilir ve izin geçersiz kılma akışı tetiklenmez. Şu anda, satış maddeleri ve iade maddeleri içeren karışık bir sepete toplam indirim yüzdesi uygulanamaz.

## <a name="remove-system-discounts-from-transaction"></a>Sistem iskontolarını hareketten kaldır

**Sistem iskontolarını hareketten kaldır** işlemi, POS kullanıcılarının uygulanan tüm sistem iskontolarını (kupon tabanlı iskontolar dahil) hareketten temizlemesine olanak tanır. Bu operasyon gerçekleştirildikten sonra fiyatlandırma altyapısı, indirim hesaplama kapsamından sistem iskontolarını hariç tutmak üzere başlatılır. **Sistem iskontolarını hareketten kaldır** işlemi el ile iskontoları kaldırmaz.

## <a name="reapply-system-discounts"></a>Sistem iskontolarını yeniden uygula

**Sistem iskontolarını yeniden uygula** işlemi, iskontoların **Sistem iskontolarını hareketten kaldır** işlemi kullanılarak kaldırılmış olması halinde, POS kullanıcılarının bir harekete sistem tarafından hesaplanan iskontoları yeniden uygulamasına olanak tanır. Bu operasyon gerçekleştirildikten sonra fiyatlandırma altyapısı, indirim hesaplama kapsamında tüm sistem iskontolarını dahil etmek üzere başlatılır.

## <a name="add-coupon-code"></a>Kupon kodunu ekle

**Kupon kodu ekle** işlemi, POS kullanıcılarının bir harekete kupon kodu girerek bir kupon eklemesine olanak sağlar. Alternatif olarak POS kullanıcıları, kupon barkodunu tarayabilir veya **Hareket** ekranındaki sayısal klavyeyi kullanarak barkodu girin.

## <a name="remove-coupon-code"></a>Kupon kodunu kaldır

**Kupon kodunu kaldır** işlemi, POS kullanıcılarının bir harekete uygulanmış olan bir veya daha fazla kuponu seçmesini ve kaldırmasını sağlar.

## <a name="recalculate"></a>Yeniden hesapla

**Yeniden hesaplama** işlemi, POS kullanıcılarının isteğe bağlı fiyatlandırma hesaplamasını tetiklemesini sağlar. Fiyat kilitleme ve/veya gecikmeli fiyat hesaplaması etkinleştirildiğinde bu operasyon gereklidir ve POS kullanıcısı, sepet veya sipariş değişikliklerinden sonra fiyatları ve iskontoları yeniden hesaplamak istediğinde kullanılır. **Yeniden hesaplama** işlemi her zaman siparişin tamamını tekrar hesaplar. Seçili satış satırlarını yeniden hesaplamak için kullanılamaz. POS'ta kilitli bir satış satırına el ile iskonto uygulamak için, POS kullanıcılarının tüm satış satırlarının kilidini açmak için öncelikle **Yeniden hesaplama** işlemini kullanmaları gerekir.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
