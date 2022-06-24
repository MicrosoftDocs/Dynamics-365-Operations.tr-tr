---
title: Otomatik deftere nakil için varsayılan açıklamaları ayarlama
description: Bu makale, otomatik olarak genel muhasebeye nakledilen muhasebe girişlerini açıklamak için kullanılan varsayılan metnin nasıl ayarlanacağını açıklar. Serbest biçimli metni kullanarak veya sabit değişkenleri seçerek, varsayılan açıklama metnini ayarlayabilirsiniz.
author: aprilolson
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 71982a7d5b1bb08d3e238646ea0b15f17260bdcc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904513"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a>Otomatik deftere nakil için varsayılan açıklamaları ayarlama

[!include [banner](../includes/banner.md)]

Bu makale, otomatik olarak genel muhasebeye nakledilen muhasebe girişlerini açıklamak için kullanılan varsayılan metnin nasıl ayarlanacağını açıklar. Serbest biçimli metni kullanarak veya sabit değişkenleri seçerek, varsayılan açıklama metnini ayarlayabilirsiniz.

> [!NOTE]
> Bazı ülke veya bölgelerdeki bazı hareket türleri için, söz konusu hareket türleriyle ilişkili olan alanlardaki metinleri de ekleyebilirsiniz. Hareket türleri ile ülkeler ve bölgeler listesi için bu makalenin ilerleyen kısımlarında bulunan [İsteğe bağlı: Varsayılan açıklamalara başka metin ekleme](#optional-add-other-text-to-default-descriptions) konusuna bakın.

## <a name="set-up-default-descriptions"></a>Varsayılan tanımlar oluşturma

1. **Kuruluş yönetimi** \> **Kurulum** \> **Varsayılan açıklamalar**'a gidin.
2. Eylem Bölmesinde, **Yeni**'yi seçin.
3. **Açıklama** alanında, varsayılan açıklama oluşturmak için hareket türünü seçin.
4. **Dil** alanında, açıklamanın geçerli olduğu dili seçin.
5. **Metin** alanına bir varsayılan açıklama girin. Alana metin yazabilir veya aşağıdaki serbest metin değişkenlerinden birini veya daha fazlasını kullanabilirsiniz:

    - **%1** – Hareket tarihi ekleyin.
    - **%2** – Genel muhasebeye nakledilecek olan belge türüne karşılık gelen bir tanımlayıcı ekleyin. Örneğin, faturalarla ilişkili hareket türleri için **%2** değişkeni fatura numarasını ekler.
    - **%3** – Genel muhasebeye nakledilecek olan belge türüyle ilgili bir tanımlayıcı ekleyin. Örneğin, faturalarla ilişkili hareket türleri için **%3** değişkeni müşteri hesabı numarasını ekler.

## <a name="optional-add-other-text-to-default-descriptions"></a>İsteğe bağlı: Varsayılan açıklamalara başka metin ekleme

Bazı ülke veya bölgelerdeki bazı hareket türleri için, varsayılan açıklamalara hareket türleriyle ilişkili olan verilerinizdeki alanlardan gelen metinleri de ekleyebilirsiniz. Aşağıdaki listelerde, bu seçeneğin kullanılabileceği hareket türleri ile ülkeler ve bölgeler gösterilmektedir.

**Hareket tipleri**

Aşağıdaki belge türleriyle ilişkili hareket türleriyle ilgili varsayılan açıklamalara başka metin ekleyebilirsiniz:

- Müşteri faturaları
- Müşteri alacak dekontları
- Müşteri nakit ödemeleri
- Satıcı ödemeleri
- Satış siparişleri
- Satınalma siparişleri
- Stok günlükleri
- Master planlama (MRP)
- Sabit kıymetler

**Ülkeler ve bölgeler**

Bu seçenek aşağıdaki ülkeler ve bölgeler için kullanılabilir:

- Brezilya
- Çin
- Çek Cumhuriyeti
- Doğu Avrupa
- Macaristan
- Hindistan
- Japonya
- Litvanya
- Letonya
- Polonya
- Rusya

### <a name="add-text-to-default-descriptions"></a>Varsayılan açıklamalara metin ekleme

Bu makalenin önceki kısımlarındaki [Varsayılan açıklamaları ayarlama](#set-up-default-descriptions) bölümünde bulunan adımları tamamladıktan sonra, varsayılan açıklamalara başka metin eklemek için aşağıdaki adımları izleyin.

1. **Parametreler** hızlı sekmesinde, **Ekle**'yi seçin.
2. **Referans tablosu** alanında, açıklamaya parametre verilerinin ekleneceği veritabanı tablosunu seçin.
3. **Referans alanı** alanında, açıklamaya parametre verilerinin ekleneceği alanı seçin.
4. Daha fazla parametre eklemek için 1 ile 3. adımlar arasındaki işlemleri tekrarlayın.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
