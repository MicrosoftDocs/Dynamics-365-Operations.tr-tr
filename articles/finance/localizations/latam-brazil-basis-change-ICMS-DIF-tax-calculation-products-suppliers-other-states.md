---
title: Diğer eyaletlerdeki tedarikçilere ait ürünlerin ICMS-DIF vergisi hesaplamalarında temel değişiklik
description: Bu konu, Brezliyanın Rio Grande do Sul (RS) veya São Paulo (SP) eyaletlerinde mali bir belge alındığında ICMS-DIF vergi türü hesaplamalarına dair konfigürasyonu açıklar.
author: Kai-Cloud
ms.date: 1/20/2022
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
ms.openlocfilehash: 63e3cbaaf77456b55f08ea91831ba9d49cb57185
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689170"
---
# <a name="basis-change-in-icms-dif-tax-calculations-for-products-from-suppliers-in-other-states"></a>Diğer eyaletlerdeki tedarikçilere ait ürünlerin ICMS-DIF vergisi hesaplamalarında temel değişiklik

Bu konu, Brezliyanın Rio Grande do Sul (RS) veya São Paulo (SP) eyaletlerinde mali bir belge alındığında **ICMS-DIF** vergi türü hesaplamalarına dair konfigürasyonu açıklar.

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
    - **Marjinal taban** alanında, **Satır başına net tutar** veya **Fatura bakiyesinin net tutarı**'nı seçin.
    - Vergilendirme kodunu **3** mali değeri olacak şekilde tanımlayın. Bu şekilde, **Mali defterler** modülü etkinleştirildiğinde ayarlama hareketi otomatik olarak oluşturulur.
    - Satış vergisi grubunun konfigürasyonlarında, **ICMS-DIF** satış vergisi kodu için **Vergi kullan** seçeneğini belirleyin.
