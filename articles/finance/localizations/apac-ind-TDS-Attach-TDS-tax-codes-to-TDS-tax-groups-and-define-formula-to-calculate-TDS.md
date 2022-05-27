---
title: TDS vergi kodlarını, TDS vergi gruplarına ekle ve TDS hesaplama formülünü belirle
description: Bu konu, Kaynakta Kesilen Vergi (TDS) gruplarının nasıl kurulduğunu ve TDS vergi kodlarını TDS vergi gruplarına ilişkilendirmeyi açıklamaktadır. Bir TDS vergi grubu için TDS'yi hesaplamak için, gruba iliştirilen TDS vergi kodlarının formülünü belirlemeniz gerekir.
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
ms.openlocfilehash: f1326f95c297887213ecfb572a2437867d964925
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711250"
---
# <a name="attach-tds-tax-codes-to-tds-tax-groups-and-define-the-formula-for-calculating-tds"></a>TDS vergi kodlarını, TDS vergi gruplarına ekle ve TDS hesaplama formülünü belirle

[!include [banner](../includes/banner.md)]

Bu konu, Kaynakta Kesilen Vergi (TDS) gruplarının nasıl kurulduğunu ve TDS vergi kodlarını TDS vergi gruplarına ilişkilendirmeyi açıklamaktadır. Bir TDS vergi grubu için TDS'yi hesaplamak için, gruba iliştirilen TDS vergi kodlarının formülünü belirlemeniz gerekir.

TDS vergi grubunu ayarlamak, TDS vergi kodlarını gruba iliştirmek ve TDS'yi hesaplama formülünü belirlemek için aşağıdaki adımları izleyin.

1. **Vergi \> Dolaylı vergiler \> Stopaj vergisi \> Stopaj vergisi grupları**'na gidin.

    [![Stopaj vergisi grupları sayfası.](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)

2. Eylem bölmesinde, TDS için stopaj vergisi grubu oluşturmak üzere **Yeni**'yi seçin ve gerekli ayrıntıları girin.
3. **Vergi türü** alanında **TDS**'yi seçin.
4. **Kurulum** hızlı sekmesinde satır oluşturmak için **Ekle**'yi seçin.
5. **Stopaj vergisi kodu** alanında TDS vergi grubu için TDS vergi kodunu seçin. **Stopaj vergisi adı** alanı, TDS vergi kodunun adını ve **Değer** alanı değeri gösterir.
6. TDS hareketlerinde TDS vergi koduna iliştirilmiş TDS vergi bileşeni için tanımlanan eşik sınırını ve istisna eşik sınırını yok saymak için **Eşiği dikkate alma** onay kutusunu seçin.
7. Vergi grubunun hareketlerde hesaplanmasını önlemek için, **Muaf** onay kutusunu seçin.
8. Eylem bölmesinde, bu TDS vergi grubunun TDS hesaplama formülünü belirleyebilmek için formül tasarımcısını açmak üzere **Tasarımcı**'yı seçin. **Tasarımcı** sayfasında, **Vergiler** sekmesi, TDS vergi grubu için seçilen TDS vergi kodlarını gösterir.

    [![Tasarımcı sayfası.](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)

9. Bir satır oluşturmak için, **Hesaplama** sekmesinde **Alt+N**'yi seçin. **Kimlik** alanı, TDS hesaplaması için otomatik olarak oluşturulan öncelik kimliğini gösterir.
10. **Vergi kodu** alanında formül için belirlenecek TDS vergi kodunu seçin. TDS vergi grubu için seçilen tüm TDS vergisi kodları, bu alanda seçilebilir.
11. **Vergilendirilebilir esas** alanında, TDS hesaplamasının esasını seçin:

    - **Brüt tutar** – TDS'yi, vergi kodu için belirlenen hesaplama ifadesini kullanarak, brüt hareket tutarına (yani fatura tutarı) göre hesaplayın.
    - **Brüt tutar hariç** – TDS'yi, vergi kodu için tanımlanan hesaplama ifadesine göre hesaplayın.

    > [!NOTE]
    > Öncelik kimliği **1** olan TDS vergi kodlarının **Vergilendirilebilir esas** alanı, **Brüt tutar hariç** olarak ayarlanamaz.

12. TDS hesaplaması, TDS vergi grubuna iliştirilmiş her vergi kodu için **Hesaplama ifadesi** alanında belirlenen formüle dayanır. **Hesaplama ifadesi** alanında seçili TDS vergi koduna ait hesaplama ifadesini girmek için artı işareti (+), eksi işareti (-), çarpma işareti (\*) veya bölme işareti (/) düğmesini seçin.

    > [!NOTE]
    > Öncelik kodu **1** olan TDS vergi kodu için herhangi bir hesaplama ifadesi tanımlanamaz.

13. Bu TDS vergi kodu için **Hesaplama ifadesi** alanında hesaplama ifadesini tanımlamak için, **Vergiler** sekmesinde mevcut olan TDS vergi kodlarını ekleyin. **Hesaplama ifadesi** alanında TDS vergi kodlarını eklemek için aşağıdaki yöntemlerden birini kullanabilirsiniz:

    - Gerekli vergi kodunu **Vergiler** sekmesinden **Hesaplama ifadesi** alanına sürükleyin.
    - **Vergiler** sekmesinde gerekli vergi koduna çift dokunun (veya çift tıklayın).
    - **Vergiler** sekmesinde gerekli vergi kodunu seçin ve basılı tutun (veya sağ tıklayın) ve sonra **Vergi kodu ekle**'yi seçin.

    > [!NOTE]
    > Her TDS vergi kodundan önce bir hesaplama ifadesi ekleyin. Hesaplama ifadesine eklenen TDS vergi kodları köşeli ayraç (\[...\]) içinde görünür.

14. **Hesaplama ifadesi** alanında vergi kodu için tanımlanan hesaplama ifadesini temizlemek için **C** düğmesini seçin.
15. **Hesaplama** sekmesindeki bir kaydı silmek için , **Sil**'i seçin.
16. Sayfayı kapatın.
