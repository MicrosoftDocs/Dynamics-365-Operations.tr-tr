---
title: TDS vergi türü için vergi bileşenlerini ayarlama
description: Bu makalede, Kaynakta Kesilen Vergi (TDS) türü için stopaj vergisi bileşenlerinin nasıl ayarlanacağı açıklanmaktadır. Ayrıca her TDS bileşeni için TDS'yi hesaplama amacıyla kullanılan eşik sınırının nasıl tanımlanacağını açıklar.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: df2eb10ce9e372bb1e984f6ae1a2e889bbd90ad0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871171"
---
# <a name="set-up-tax-components-for-the-tds-tax-type"></a>TDS vergi türü için vergi bileşenlerini ayarlama

[!include [banner](../includes/banner.md)]

Bu makalede, Kaynakta Kesilen Vergi (TDS) türü için stopaj vergisi bileşenlerinin nasıl ayarlanacağı açıklanmaktadır. TDS bileşenleri şunlardır: TDS, ek talep, PE-Cess ve SHE Cess. Bu makalede, her TDS bileşeni için TDS'yi hesaplama amacıyla kullanılan eşiğin nasıl tanımlanacağını da açıklanmaktadır. Ek olarak, her TDS bileşeni için TDS'yi hesaplamak üzere kullanılan bir istisna eşiği tanımlayabilirsiniz.

TDS bileşenlerini ayarlamak için aşağıdaki adımları izleyin.

1. **Vergi \> Kurulum \> Stopaj vergisi \> Stopaj vergisi bileşenleri**'ne gidin.

    [![Stopaj vergisi bileşenleri sayfası.](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)

2. TDS vergi türü için stopaj vergisi bileşenlerini ayarlamak üzere **Vergi türü** alanında **TDS**'yi seçin.
3. Eylem bölmesinde, bir satır oluşturmak için **Yeni**'yi seçin.
4. **Stopaj vergisi bileşeni** alanında, TDS bileşeni için bir ad girin.
5. **Stopaj vergisi bileşen grubu** alanında, TDS bileşeninin ekleneceği TDS stopaj vergisi bileşen grubunu seçin.
6. **Genel** hızlı sekmesinde, **Açıklama** alanına TDS bileşeninin açıklamasını girin.
7. Eylem Bölmesinde, **Eşik** sayfasını açmak için **Eşik** seçeneğini belirleyin; böylece TDS bileşeni için TDS'yi hesaplamak üzere kullanılacak eşiği tanımlayabilirsiniz.
8. Eşiğin uygulanabileceği dönemi tanımlamak için **Başlangıç tarihi** ve **Bitiş tarihi** alanlarını kullanın.
9. **Genel** hızlı sekmesinde, **Eşik** alanına TDS bileşeni için TDS hesaplamasında kullanılacak eşik tutarını girin. Vergi yalnızca, kümülatif fatura tutarı eşiği aştığında kaynakta kesilecektir.

    Örneğin, eşik tutarı 10.000 ise kümülatif fatura tutarı 10.000'i aştığında (yani 10.001 veya daha fazla olduğunda) TDS hesaplanır.

10. **İstisna eşik** alanında, TDS bileşeni için TDS hesaplamasında kullanılacak istisna eşik tutarını girin. Bir fatura satırında vergi yalnızca, tutar istisna eşiği aştığında kaynakta kesilecektir.

    Örneğin, istisna eşik tutarı 5.000 ise, fatura satır tutarı 5.000 değerini aştığında (yani 5.001 veya daha fazla) TDS belirli bir fatura satırında hesaplanır.

    [![Eşik sayfası.](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)

    > [!NOTE]
    > İstisna eşik tutarı, eşik tutarına eşit veya tutardan daha az olmalıdır.
    >
    > Kümülatif fatura tutarı, **Eşik** alanında belirtilen eşiği aşmasa bile, hareket tutarı istisna eşiği aşarsa vergi, bir hareket için kesilir.

11. **Stopaj vergisi bileşenleri** sayfasına dönmek için **Eşik** sayfasını kapatın.
12. Eylem Bölmesinde, **Stopaj vergisi bileşenlerini kopyala** iletişim kutusunu açmak için **Kopyala**'yı seçerek bir TDS bileşen grubu için ayarlanmış olan TDS bileşenlerini başka bir TDS bileşen grubuna kopyalayabilirsiniz.
13. **Kaynak** alanında, TDS bileşenlerinin kopyalanmak için alınacağı TDS bileşen grubunu seçin. **Hedef** alanında, TDS bileşenlerinin kopyalanacağı stopaj vergisi bileşen grubunu seçin.

    > [!NOTE]
    > Her iki TDS bileşen grubuna eklenen ortak TDS bileşenleri kopyalanmaz.

14. **Stopaj vergisi bileşenleri** sayfasında diğer TDS bileşen grubu için TDS bileşenlerini kopyalamak ve oluşturmak için **Tamam**'ı seçin.

    [![Stopaj vergisi bileşenlerini kopyala iletişim kutusu.](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)

15. Sayfayı kapatın.
