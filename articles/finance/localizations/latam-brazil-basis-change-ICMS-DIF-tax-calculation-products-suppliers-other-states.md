---
title: Diğer eyaletlerdeki tedarikçilere ait ürünlerin ICMS-DIF vergisi hesaplamalarında temel değişiklik
description: Bu makalede, Brezilya'nın Rio Grande do Sul (RS) veya São Paulo (SP) eyaletlerinde mali bir belge alındığında ICMS-DIF vergi türü hesaplamalarına dair yapılandırma açıklanmaktadır.
author: Kai-Cloud
ms.date: 06/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-1-17
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 1bd9982a3804778a27203b4311682ee8bc3c4841
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218665"
---
# <a name="basis-change-dual-base-in-icms-dif-tax-calculations-for-products-from-suppliers-in-other-states"></a>Diğer eyaletlerdeki tedarikçilere ait ürünlerin ICMS-DIF vergisi hesaplamalarında temel değişiklik (ikili baz)

Bu makalede, Brezilya'nın Rio Grande do Sul (RS) veya São Paulo (SP) eyaletlerinde mali bir belge alındığında **ICMS-DIF** vergi türü hesaplamalarına dair yapılandırma açıklanmaktadır.

Eyalet yasasına göre, toplanan Imposto sobre Circulação de Mercadorias e Serviços (ICMS) şu kurala uymalıdır:

*Toplanacak ICMS* = ([(*Operasyon tutarı* – *Kaynaktan ICMS*) ÷ (1 – *ICMS % dahili*)] × *ICMS % dahili*) – *Kaynaktan ICMS tutarı*

## <a name="example"></a>Örnek

RS eyaletindeki bir Brezilya şirketi, SP eyaletindeki bir satıcıdan satınalmaya dair bir mali belge alır. Şirket, RS eyaleti (yüzde 18) ve SP eyaleti (yüzde 12) arasındaki ICMS'nin fark yüzdesini toplamalıdır. Ancak, taban ise önceki kurala göre hesaplanmalıdır.

- **Operasyon tutarı:** 1.000,00 Brezilya reali (R$ 1.000,00)
- **ICMS eyaletler arası:** R$ 120,00
- **RS eyaletinde ICMS yüzdesi:** yüzde 18
- **RS eyaletinde toplanacak ICMS:** (\[(1.000 – 120) ÷ (1 – 0,18)\] × 0,18 ) – 120 = R$ 73,17 

## <a name="resolution"></a>Çözüm

RS eyaletinin kurallarına göre ICMS farkını (ICMS-DIF) hesaplamak için satış vergisi kodları ve satış vergisi grubunu aşağıdaki şekilde ayarlamalısınız:

1. Yüzde 12 ICMS'yi (diğer eyalete) almak için satış kodu oluşturun. Bu kod, satıcıdan vergi alacak tutarı kaydetmek için kullanılır.
2. ICMS-DIF'i toplamak için bir satış vergisi kodu oluşturun. Bu satış vergisi kodunun yüzde 18 oranında (kendi eyaletiniz için) bir yüzde tutarı olmalıdır, yüzde 18 ve yüzde 12 arasındaki farkı belirlemek için. Vergi türünü **ICMS-DIF** olarak belirleyin. Bu satış vergisi kodu, hesaplama parametrelerinde aşağıdaki şekilde tanımlanmalıdır:

    - **Orijin** bölümünde **Brüt tutarın yüzdesi**'ni seçin.
    - **Marjinal taban** alanında, **Satır başına net tutar**'ı seçin.
    - Vergilendirme kodunu **3** mali değeri olacak şekilde tanımlayın. Bu şekilde, **Mali defterler** modülü etkinleştirildiğinde ayarlama hareketi otomatik olarak oluşturulur.
    - Satış vergisi grubunun konfigürasyonlarında, **ICMS-DIF** satış vergisi kodu için **Vergi kullan** seçeneğini belirleyin.

### <a name="use-the-delta-tax-rate-in-the-configuration-of-dual-base-icms-dif-sales-tax-codes"></a>ICMS-DIF satış vergisi kodlarının yapılandırmasında değişken vergi oranını kullanma

Daha önce açıklanan ayarlar kullanıldığında, **ICMS-DIF** satış vergisi kodu ikili baz kuralıyla hesaplanır. Ancak, nominal vergi oranı yüzde 18 olur ve basit baz kuralındaki yüzde 6 oranıyla farklılık gösterir. Bu farklılık, mali belge ve vergi raporlamasında tutarsızlık sorunlarına neden olur. Microsoft Dynamics 365 Finance sürüm 10.0.29 itibariyle, tutarsızlığı kaldırmak için **Özellik yönetimi**'ndeki **(Brezilya) İkili baz durum için ICMS-DIF vergi kodunda değişken vergi oranını yapılandır** özelliğini etkinleştirebilirsiniz.

- Önceki bölümdeki adımları tamamlamaya ek olarak, **Satış vergisi üzerinde satış vergisi** alanındaki **ICMS 12** satış vergisi kodunu seçin.
- **ICMS-DIF** satış vergisi kodunun vergi oranını yüzde 18 olarak ayarlayın. **Yüzde/Tutar** alanı nominal vergi oranını yüzde 6 oranında gösterir.

> [!NOTE]
> **ICMS-DIF** ve **ICMS 12** satış vergisi kodlarının aynı satış vergisi grubunda atanması gerekir.

## <a name="basis-change-dual-base-in-icms-dif-tax-calculations-for-products-to-non-taxpayer-consumers-difal-in-other-states"></a>Diğer eyaletlerdeki vergi mükellefi olmayan tüketicilere satılan ürünlerin ICMS-DIF vergisi hesaplamalarında temel değişiklik (ikili baz)

Vergi mükellefi olmayan tüketicilerle yapılan ticari işlemlerde ICMS-DIF vergisi baz değişikliğini desteklemek için **Özellik yönetimi**'nde bulunan **(Brezilya) Satış hareketlerinde ICMS-DIFAL için ikili baz hesaplama** özelliğini etkinleştirin. Örnek ICMS-DIF satış vergisi kodu, satış siparişinde ve serbest metin fatura hareketlerinde geçerli olur.

Başka bir eyaletteki vergi mükellefi olmayan tüketicilerle yapılan ticaretin Imposto sobre Produtos Industrializados (IPI) vergisine da tabi olduğu senaryoları desteklemek için **Özellik yönetimi**'nde **(Brezilya) IPI vakalarıyla ilgili olarak ICMS-DIFAL için ikili baz hesaplaması** özelliğini etkinleştirin. IPI satış vergisi kodunun vergi tutarı algılanır ve ICMS-DIAL vergi matrahına uygulanır.

- Satış siparişinin veya serbest metin faturasının üstbilgisinde, **Mali bilgiler** hızlı sekmesinde, **Son Kullanıcı** seçeneğinin **Evet** olarak ayarlanması gerekir.
- Satın alma siparişinin veya satıcı faturasının üstbilgisinde, **Mali bilgiler** hızlı sekmesinde, **Kullanım ve tüketim** seçeneğinin **Evet** olarak ayarlanması gerekir.
