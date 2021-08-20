---
title: TDS hesaplamaları için formül tasarımcısı
description: Bu konu, hareketle ilişkilendirilmiş TDS grubundaki her bir TDS vergi kodu için belirlenen formüle dayalı olarak Kaynakta Kesilen Verginin (TDS) nasıl hesaplandığını gösteren bir örnek sağlar.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: e9c97982233b1f3dc3924fa42954b5cb8d09ffcaa07d19a3892b25737a6c29c5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778881"
---
# <a name="formula-designer-for-tds-calculations"></a>TDS hesaplamaları için formül tasarımcısı

[!include [banner](../includes/banner.md)]

Bu konu, her bir TDS vergi kodu için belirlenen formüle göre Kaynakta Kesilen Verginin (TDS) nasıl hesaplandığıyla ilgili bir örnek sağlar. TDS vergi kodları, harekete iliştirilen TDS grubunda tanımlanır. TDS formüllerini tasarlamadan önce, aşağıdaki adımlarda listelendiği şekilde TDS için gerekli temel kurulumu tamamlayın. 

- **Stopaj vergisi bileşeni grupları** sayfasını kullanarak TDS bileşeni gruplarını ayarlayın. 
- **Stopaj vergisi bileşenleri** sayfasını kullanarak TDS bileşenlerini ayarlayın ve TDS bileşeni grubunu TDS bileşenleriyle ilişkilendirin. 
- **Stopaj vergisi kodları** sayfasını kullanarak TDS vergi kodlarını ayarlayın ve TDS bileşenlerini vergi kodlarıyla ilişkilendirin. 
- **Stopaj vergisi grupları** sayfasını kullanarak TDS vergi gruplarını ayarlayın. Ardından TDS vergi kodlarını vergi grubuna iliştirin ve **Formül tasarımcısı** sayfasını kullanarak formülü tanımlayın. 

**Örnek formül**

Bu örnekte; Kira TDS grubu, A satıcısı için oluşturulan satınalma faturasına bağlıdır. Fatura tutarı $100.000'dır. Faturanın TDS hesaplamasını görüntülemek için aşağıdaki tabloyu inceleyin.

| TDS grubu                                                   | TDS grubuna iliştirilen TDS vergi kodları | Değer              | Vergilendirilebilir esas  (Formül tasarımcısı) | Hesaplama ifadesi  (Formül tasarımcısı) | Matrah | Hesaplanan TDS tutarı |
| ------------------------------------------------------------ | --------------------------------------- | ------------------ | --------------------------------- | :----------------------------------------: | ----------- | --------------------- |
| Kira                                                         | TDS  (TDS bileşeni-TDS)                | %10                | Brüt tutar                      |                                            | 100,000      | 10,000                 |
| Ek talep  (TDS bileşeni-Ek talep)                         | %10                                     | Brüt tutar hariç | +TDS                              |                   10000                    | 1,000        |                       |
| PE-Cess  (TDS bileşeni- PE-Cess)                            | %2                                      | Brüt tutar hariç | +TDS+Ek talep                    |                   11000                    | 220         |                       |
| SHE Cess  (TDS bileşeni- SHE Cess)                          | %1                                      | Brüt tutar hariç | +TDS+Ek talep                    |                   11000                    | 110         |                       |
| **Fatura** **için** **hesaplanan** **toplam** **TDS** **değeri** | **11,330**                               |                    |                                   |                                            |             |                       |

Fiş girişleri aşağıdaki şekilde oluşturulur.

| Hesap           | Borç  | Kredi |
| ----------------- | ------ | ------ |
| Kira              | 100,000 |        |
| Satıcı A          |        | 100,000 |
| Satıcı A          | 11,330  |        |
| Ödenecek TDS       |        | 10,000  |
| Ödenecek ek talep |        | 1,000   |
| Ödenecek PE-Cess   |        | 220    |
| Ödenecek SHE Cess  |        | 110    |
