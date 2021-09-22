---
title: Stok tutma birimi için maksimum ondalık birim sayısı 0'dır
description: Bir stok hareketini veya stok rezervasyonunu deftere nakletmeye çalıştığınızda "Stok tutma birimi için maksimum ondalık birim sayısı 0'dır" hatasını alırsınız.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 9dec198e2d77efd2253c80e14d15791cc37f88e1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477887"
---
# <a name="maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a>Stok tutma birimi için maksimum ondalık birim sayısı 0'dır


## <a name="symptoms"></a>Belirtiler

Bir stok hareketini veya stok rezervasyonunu deftere nakletmeye çalıştığınızda aşağıdaki hata iletisini alırsınız:

> Stok tutma birimi için maksimum ondalık birim sayısı 0'dır.

Bu sorun stok hareketi miktarı, alanın desteklediği duyarlık düzeyinin altında olan bir ondalık değer olarak belirtildiğinde oluşur. Örneğin, bir stok hareketi için *0,5* miktarı belirtilmiştir ancak yalnızca tamsayı olan miktarlar desteklenmektedir. Bu nedenle, değer *0,5* yerine *1* olmalıdır.

## <a name="resolution"></a>Çözüm

1. Stok hareketlerindeki miktarları yuvarlamak için SQL Server kurulumunuzda aşağıdaki kodu çalıştırın. Bu kod, **inventTrans** tablosundaki değerleri düzeltecektir.

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. **Sorunu düzelt** seçeneğinin açık olduğu bir eldekiler tutarlılık denetimi çalıştırın. Bu denetim, **inventSum** tablosundaki değerleri düzeltecektir.

> [!IMPORTANT]
> Kodu ortam için gereken şekilde dikkatle düzenlemenizi, test ortamında test etmenizi ve kodu üretim ortamında çalıştırmadan önce sonuçta elde edilen verileri denetlemenizi önemle tavsiye ederiz.
