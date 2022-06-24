---
title: Vergi kodlarını ayarlama
description: Bu makalede, Vergi Hesaplama Hizmetinde vergi kodlarının nasıl ayarlanacağı açıklanmaktadır.
author: wangchen
ms.date: 11/30/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 1bc250716763ce9d8e25c8850c8a3676bf65fb0c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862942"
---
# <a name="set-up-tax-codes"></a>Vergi kodlarını ayarlama

[!include [banner](../includes/banner.md)]

Bu makalede, Vergi Hesaplama hizmetinde vergi kodlarının nasıl ayarlanacağı açıklanmaktadır. Vergi kodunun çalışmasını sağlamak için basit bir senaryo kurulumunu ve karmaşık senaryolar için bazı gelişmiş vergi kodu işlevleri hakkında bilgi içerir.

> [!IMPORTANT]
> Vergi Hesaplama Hizmeti'nde vergi kodları düzeni tüzel kişilikten bağımsızdır. Bu düzeni Regulatory Configuration Service'ten (RCS) yalnızca bir kez tamamlayabilirsiniz. Finance'te seçili bir tüzel kişilik için Vergi Hesaplama hizmetini etkinleştirdiğinizde, vergi kodları otomatik olarak Microsoft Dynamics 365 Finance ile eşitlenir.

## <a name="simple-setup"></a>Basit kurulum

Yalnızca bir vergi oranının olduğu bir senaryo gibi basit bir senaryoda vergi kodu kullanmak için bu adımları izleyin.

1. [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/)'te oturum açın.
2. **Çalışma Alanları** \> **Globalleştirme özellikleri** \> **Vergi hesaplama**'ya gidin.
3. Ayarlamak istediğiniz özellik ve sürümü, ardından **Düzenle**'yi seçin.
4. **Genel** sekmesinde, **Yapılandırma sürümü**'nü seçin.
5. **Vergi kodları** sekmesinde, **Ekle**'yi seçin ve vergi kodunu ve bir açıklama girin.
6.  **Hesaplama kaynağı**'nı seçin. Hesaplama kaynağı, seçtiğiniz vergi yapılandırma sürümünde tanımlanan bir yöntem grubudur. Bu basit senaryo için **Net tutara göre**'yi seçin.
7. **Kaydet**'i seçin. Seçtiğiniz hesaplama kaynağına bağlı olarak daha fazla alan kullanılabilir hale gelir.
8. **Fiyatlar** hızlı sekmesinde, bu vergi koduna bir vergi oranı eklemek için **Ekle**'yi seçin.
9. **Kaydet**'i seçin.

## <a name="calculation-origin"></a>Hesaplama kaynağı

Hesaplama kaynağı, vergi matrahı ve vergi tutarının nasıl hesaplanacağını tanımlar. **Elektronik Raporlama** çalışma alanında vergi yapılandırması tarafından yapılandırılır. Aşağıdaki değerler, **Hesaplama kaynağı** alanında kullanılabilir:

- Net tutara göre
- Brüt tutara göre
- Miktara göre
- Marja göre
- Vergi üzerinden vergi

### <a name="by-net-amount"></a>Net tutara göre

**Hesaplama kaynağı** alanında **Net tutara göre**'yi seçerseniz vergi tutarı diğer vergi kodları hariç olmak üzere satın alma veya satış tutarının yüzdesi olarak hesaplanır.

Örneğin, vergi oranı yüzde 25 olduğunda fatura satırı, her biri 1,00 seviyesinden 10 maddelik bir miktar gösterir ve müşteriye yüzde 10'luk bir satır iskontosu izni verilir. Bu durumda, tutarlar aşağıdaki şekilde hesaplanır.

- **Net tutar:** (10 × 1,00) – yüzde 10 = 9,00 
- **Satış vergisi:** 9,00 × yüzde 25 = 2,25 
- **Toplam fatura tutarı:** 9,00 + 2,25 = 11,25

### <a name="by-gross-amount"></a>Brüt tutara göre

**Hesaplama kaynağı** alanında **Brüt tutara göre**'yi seçerseniz vergi tutarı brüt satış tutarının yüzdesi olarak hesaplanır. Brüt tutar, satır net tutarı artı satır için tüm vergi ve harçlar (**Hesaplama kaynağı** alanının **Brüt tutara göre** olarak ayarlandığı vergi hariç) olarak hesaplanır.

Örneğin, vergi dairesi bir maddeye özel vergi uygulamaktadır. Vergi tutarları, vergi hesaplanmadan önce net tutara eklenir. Aşağıdaki vergi kodları kullanılır:

- **Vergi 1** – Oran yüzde 10'dur ve **Net tutara göre** hesaplama yöntemi kullanılır.
- **Vergi 2** – Oran yüzde 20'dir ve **Net tutara göre** hesaplama yöntemi kullanılır.
- **Vergi oranı** – Oran yüzde 25'tir ve **Brüt tutara göre** hesaplama yöntemi kullanılır.

Net tutar 10,00 ise Harç 1, 1,00 (10,00 x yüzde 10) ve Harç 2 = 2,00'dir (10,00 x yüzde 20). Bu durumda, tutarlar aşağıdaki şekilde hesaplanır. 

- **Brüt tutar:** Net tutar + Harç 1 tutarı + Harç 2 tutarı = 10,00 + 1,00 + 2,00 = 13,00 
- **Vergi tutarı:** 13,00 × yüzde 25 = 3,25 
- **Toplam vergi ve harç:** 1,00 + 2,00 + 3,25 = 6,25 
- **Toplam fatura tutarı:** 10,00 + 6,25 = 16,25

### <a name="by-quantity"></a>Miktara göre

**Hesaplama kaynağı** alanında **Miktara göre**'yi seçerseniz vergi tutarı belge satırına girilen miktarla çarpılan sabit bir birim başına tutar şeklinde hesaplanır. Birim başına tutar, **Ücretler** hızlı sekmesinde belirtilir.

Örneğin, vergi kodu birim başına 1,20 olarak ayarlanır. Satış faturası satırında, bir maddeden 25 birim satılmıştır. Bu durumda, veri tutarı 25 x 1,20 = 30,00 olur.

### <a name="by-margin"></a>Marja göre

**Hesaplama kaynağı** alanında **Marja göre**'yi seçerseniz vergi tutarı satış marjının yüzdesi olarak hesaplanır. Satış marjı, maliyet tutarı eksi satış tutarıdır. Bu hesaplama yöntemi yalnızca satış hareketleri için geçerlidir.

Örneğin, vergi oranı yüzde 25'tir, fatura satırı her biri 10,00'dan 10 maddelik bir miktar gösterir ve madde başına maliyet 6'dır. Bu durumda, tutarlar aşağıdaki şekilde hesaplanır.

- **Satış marjı:** 10 × (10,00 – 6,00) = 40,00
- **Vergi tutarı:** 40,00 × yüzde 25 = 10,00
- **Toplam fatura tutarı:** 100,00 + 10,00 = 110,00

### <a name="tax-on-tax"></a>Vergi üzerinden vergi

**Hesaplama kaynağı** alanında **Verginin vergisi**'ni seçerseniz satış vergisi aynı belge satırındaki diğer tüm vergi tutarlarının yüzdesi olarak hesaplanır.

Örneğin, aşağıdaki vergi kodları kullanılır:

- **Vergi 1** – Oran yüzde 10'dur ve **Net tutara göre** hesaplama yöntemi kullanılır.
- **Vergi 2** – Oran yüzde 20'dir ve **Net tutara göre** hesaplama yöntemi kullanılır.
- **Harç üzerinden vergi** – Oran yüzde 25'tir ve **Vergi üzerinden vergi** hesaplama yöntemi kullanılır.

Bu durumda, tutarlar aşağıdaki şekilde hesaplanır.

- **Net tutar:** 10,00 
- **Harç 1:** 10,00 × yüzde 10 = 1,00 
- **Harç 2:** 10,00 × yüzde 20 = 2,00 
- **Harç üzerinden vergi:** 3,00 × yüzde 25 = 0,75
- **Toplam vergi:** 1,00 + 2,00 + 0,75 = 3,75 
- **Toplam fatura tutarı:** 10,00 + 3,75 = 13,75

## <a name="advanced-functionality"></a>Gelişmiş işlevsellik

Bu bölümde, karmaşık senaryolar için vergi kodu kurulumunun bazı gelişmiş işlevleri açıklanmaktadır.

### <a name="tax-exemption"></a>Vergi muafiyeti

**Genel** hızlı sekmesinde **Muaf** seçeneğini **Evet** olarak ayarlarsanız gerçek vergi oranına bakılmaksızın vergi tutarı her zaman 0 (sıfır) olarak geçersiz kılınacaktır.

Muafiyetin nedenini belirtmek için **Muafiyet Kodu** alanını ayarlayabilirsiniz. 

**Muafiyet Kodu** alanı için ana veri aramasını etkinleştirebilirsiniz. Bu şekilde, Finance'te tanımlanan muafiyet kodu değerleri arasından seçim yapabilirsiniz. Ana veri aramasını etkinleştirme hakkında bilgi için bkz. [Vergi hesaplama yapılandırması için ana veri aramasını etkinleştirme](tax-service-set-up-environment-master-data-lookup.md).

Örneğin, vergi oranı yüzde 25'tir ve vergi kodunda **Muaf** seçeneği **Evet** olarak ayarlanmıştır. Fatura satırı, her biri 1,00 seviyesinden 10 maddelik bir miktar gösterir ve müşteriye yüzde 10'luk bir satır iskontosu izni verilir. Bu durumda, tutarlar aşağıdaki şekilde hesaplanır.

- **Net tutar:** (10 × 1,00) – yüzde 10 = 9,00 
- **Satış vergisi:** 0,00 
- **Toplam fatura tutarı:** 9,00 + 0,00 = 9,00

### <a name="use-tax"></a>Kullanım vergisi

**Genel** Hızlı Sekmesinde **Kullanım Vergisi** seçeneğini **Evet** olarak ayarlarsanız vergi tutarı **Satıcı özeti** hesabı yerine **Vergi borcunu kullan** hesabına nakledilir.

Örneğin, vergi oranı yüzde 25'tir ve vergi kodunda **Kullanım Vergisi** seçeneği **Evet** olarak ayarlanmıştır. Fatura satırı, her biri 1,00 seviyesinden 10 maddelik bir miktar gösterir ve müşteriye yüzde 10'luk bir satır iskontosu izni verilir. Bu durumda, tutarlar aşağıdaki şekilde hesaplanır.

- **Net tutar:** (10 × 1,00) – yüzde 10 = 9,00 
- **Kullanım vergisi:** 9,00 × yüzde 25 = 2,25
- **Toplam fatura tutarı:** 9,00 + 0,00 = 9,00

> [!IMPORTANT]
> Vergi kodunda hem **Muaf** seçeneği hem de **Kullanım Vergisi** seçeneği **Evet** olarak ayarlanırsa kod satış hareketleri için vergiden muaf olarak tanınır ve satın alma hareketleri için vergi kullanır.

### <a name="reverse-charges"></a>Ters giderler

**Genel** Hızlı Sekmesinde **Ters Gider** seçeneğini **Evet** olarak ayarlarsanız vergi oranı eksi olarak yapılandırılabilir. Ters gider senaryosu için iki vergi kodu ayarlamanızı öneririz: biri artı vergi oranına sahip, diğeri eksi vergi oranına sahip. Her iki vergi kodu da aynı oran değerine sahip olmalı ve eksi vergi oranına sahip vergi kodunda **Ters Gider** seçeneği **Evet** olarak ayarlanmalıdır. Finance'te karşı ödeme çözümü hakkında daha fazla bilgi için [KDV/GST düzenine ilişkin karşı ödeme mekanizmasına](emea-reverse-charge.md) bakın.

Örneğin, bir fatura satırında iki vergi kodu belirlenir. Bir vergi oranı yüzde 25. Diğer vergi oranı yüzde -25'tir ve ikinci vergi kodunda **Ters Gider** seçeneği **Evet** olarak ayarlanmıştır. Fatura satırı, her biri 1,00 üzerinden 10 maddeden oluşan bir miktar gösterir. Bu durumda, tutarlar aşağıdaki şekilde hesaplanır.

- **Net tutar:** (10 × 1,00) = 10,00 
- **Vergi kodu 1:** 10,00 × yüzde 25 = 2,50
- **Vergi kodu 2:** 10 × yüzde -25 = -2,50
- **Toplam fatura tutarı:** 10,00 + 2,50 -2,50 = 10,00

### <a name="exclusion-from-base-amount-calculations"></a>Matrah hesaplamalarından hariç tutma

**Genel** Hızlı Sekmesinde **Matrah hesaplamasından hariç tut** seçeneğini **Evet** olarak ayarlarsanız vergi kodunun hesaplanan vergi tutarı, fiyat dahil senaryodaki diğer vergi kodu hesaplamaları için vergi matrahından hariç tutulur.

Daha fazla bilgi için bkz. [Fiyatlara vergi dahildir seçeneği etkinleştirildiğinde fiyatlardaki vergiyi hesaplama](global-exclude-from-tax-base-amount-calculation.md).

### <a name="rates"></a>Oranlar

**Oran** Hızlı Sekmesinde, farklı vergi matrahı aralıkları için farklı vergi oranları tanımlayabilirsiniz. Vergi tutarını hesaplamak için Vergi Hesaplama hizmeti her zaman vergi matrahı ile eşleşen oranı kullanır.

Örneğin, vergi oranları aşağıdaki resimde gösterildiği gibi yapılandırılabilir.

| Minimum tutar | Maksimum tutar | Vergi oranı   |
| -------------- | -------------- | ---------- |
| 0              | 1,000          | Yüzde 10 |
| 1,000          | 5.000          | Yüzde 15 |
| 5.000          | 10,000         | Yüzde 20 |
| 10,000         | 0              | Yüzde 30 |

Bu durumda, vergi tutarı aşağıdaki şekilde hesaplanır.

- Vergi matrahı 300,00, vergi oranı yüzde 10 ise vergi tutarı yüzde 10 = 30,00 × 300,00'dür.
- Vergi matrahı 3.000,00, vergi oranı yüzde 15 ise vergi tutarı yüzde 15 = 450,00 × 3.000,00'dir.
- Vergi matrahı 6.000,00, vergi oranı yüzde 20 ise vergi tutarı yüzde 10 = 1.200,00 × 6.000,00'dir.
- Vergi matrahı 20.000,00, vergi oranı yüzde 30 ise vergi tutarı yüzde 30 = 6.000,00 × 20.000,00'dir.

> [!NOTE]
> Vergi matrahı hem bir satırdaki maksimum tutarla hem de diğer satırdaki minimum tutarla eşleşebiliyorsa matrah minimum matrahla eşleşen vergi oranını kullanır. Örneğin, vergi matrahı 1.000,00, vergi oranı yüzde 15 ise vergi tutarı yüzde 15 = 150,00 × 1.000,00'dir.

### <a name="limits"></a>Limitler

**Sınırlar** Hızlı Sekmesinde, vergi tutarı minimum/maksimum aralığa girerse hesaplanan vergi tutarını geçersiz kılmak için vergi sınırları tanımlayabilirsiniz.

- Hesaplanan vergi tutarı, **Sınırlar** Hızlı Sekmesinde yapılandırılan maksimum vergi tutarından fazla veya buna eşitse son vergi tutarı maksimum vergi tutarına eşittir.
- Hesaplanan vergi tutarı **Sınırlar** Hızlı Sekmesinde yapılandırılan minimum vergi tutarından küçükse son vergi tutarı 0'dır (sıfır).

Örneğin, vergi sınırları aşağıdaki şekilde yapılandırılır:

- **Minimum vergi tutarı:** 100 
- **Maksimum vergi tutarı:** 1.000

Hesaplanan vergi tutarı 2.000 ise nihai vergi tutarı 1.000'dir.

Hesaplanan vergi tutarı 500 ise nihai vergi tutarı 500'dir.

Hesaplanan vergi tutarı 80 ise nihai vergi tutarı 0'dır (sıfır).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
