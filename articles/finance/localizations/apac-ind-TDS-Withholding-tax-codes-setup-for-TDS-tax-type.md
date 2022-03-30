---
title: TDS vergi türü için stopaj vergisi kodlarını ayarlama
description: Bu konu, Kaynakta Kesilen Vergi (TDS) için vergi kodlarının nasıl ayarlanacağını açıklar.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 03d8b7d4992fbb49a873f14e1ce1f0c816cef202
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/12/2022
ms.locfileid: "8407472"
---
# <a name="set-up-withholding-tax-codes-for-the-tds-tax-type"></a>TDS vergi türü için stopaj vergisi kodlarını ayarlama

[!include [banner](../includes/banner.md)]

Bu konu, Kaynakta Kesilen Vergi (TDS) için vergi kodlarının nasıl ayarlanacağını açıklar.

1. **Vergi \> Dolaylı vergiler \> Stopaj vergisi \> Stopaj vergisi kodları**'na gidin.

    [![Stopaj vergisi kodları sayfası.](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)

2. Eylem bölmesinde, TDS için stopaj vergisi kodu oluşturmak üzere **Yeni**'yi seçin ve gerekli ayrıntıları girin.
3. **Genel** hızlı sekmesinde, **Vergi türü** alanında, vergi kodunu TDS vergi kodu olarak sınıflandırmak için **TDS**'yi seçin.
4. **Kapatma dönemi** alanında, TDS vergi kodunun TDS kapatma dönemini seçin.
5. **Ana hesap** alanında, TDS tutarının nakledileceği genel muhasebe hesabını seçin.
6. **Alacak hesabı** alanında, satış hareketlerinde kesilen TDS tutarının nakledileceği alacak hesabını seçin.

    **Kaynak** alanı otomatik olarak **Brüt tutarın yüzdesi** olarak ayarlanır ve değer değiştirilemez.

    > [!NOTE]
    > TDS vergi türünün vergi kodları için kaynak alanını **Net tutar yüzdesi** olarak ayarlayamazsınız.

7. **Stopaj vergisi bileşeni** alanında, TDS vergi kodunun TDS vergi bileşenini seçin.
8. **Stopaj vergisi değerleri** sayfasını açmak için, Eylem Bölmesinde **Değerler**'i seçin.
9. **Başlangıç tarihi** alanında, TDS değerinin başlangıç tarihini girin. **Bitiş tarihi** alanında, bitiş tarihini girin.

    > [!NOTE]
    > **Minimum limit**, **Üst limit** ve **Hariç tutma yüzdesi** alanları, TDS vergi türünün vergi kodlarında kullanılamaz.

10. **Değer** alanına, TDS vergi kodunun TDS yüzdesini girin.
11. **Stopaj vergisi kodları** sayfasına dönmek için **Stopaj vergisi değerleri** sayfasını kapatın.

    > [!NOTE]
    > **Stopaj vergisi kodları** sayfasındaki **Limitler** düğmesi, TDS vergi türüyle ilgili vergi kodları için kullanılamaz.

12. Sayfayı kapatın.
