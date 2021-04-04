---
title: Gelen belgeleri Excel biçiminde ayrıştırma
description: Bu konu, gelen Microsoft Excel dosyalarındaki içeriği ayrıştırmak için Elektronik raporlama (ER) biçimleri tasarlama hakkında bilgi vermektedir.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 847b3309a3e0daf7b341c4ba4a58a8ea0902e61c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564531"
---
# <a name="parse-incoming-documents-in-excel-format"></a>Genel belgeleri Excel biçiminde ayrıştırma

[!include[banner](../includes/banner.md)]

Microsoft Excel çalışma kitaplarındaki (XLSX biçimindeki dosyalar) verileri temsil eden gelen Microsoft Excel dosyalarını ayrıştırmak için Elektronik raporlama (ER) biçimleri tasarlayabilirsiniz. Bunun ardından, uygulama verilerini güncelleştirmek için bu dosyalardaki içeriği kullanabilirsiniz. Bu, şunu yaptığınız zaman size yarar sağlar:

- Yeni bir model ve biçim tasarlamak ve çalıştırma zamanında bunları test etmek. Bu durumda, Excel gerçek uygulama verilerinin benzetimini yapacaktır.
- Uygulamanızın dışında, verileri Excel'de yönetmek ve belirli bir rapor gönderme amacıyla bu verileri içe aktarmak.

Bu özellik hakkında daha fazla bilgi için, **ER - Microsoft Excel dosyasından verileri içe aktarma (Bölüm 1: Biçim tasarlama)** ve **ER - Microsoft Excel dosyasından verileri içe aktarma (Bölüm 2: Verileri içe aktarma)** (7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677) iş sürecinin parçaları). Bu görev kılavuzları, gelen belgelerden bilgileri içe aktarmak ve uygulama verilerini güncelleştirmek için, ER biçimi kullanarak, gelen Excel dosyasının nasıl ayrıştırılabileceği konusunda size yol gösterir. Görev kılavuzu dosyalarını [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684)'dan indirebilirsiniz.

Yukarıda sözü edilen görev kılavuzlarını tamamlamak için aşağıdaki dosyaları indirin:

| İçerik açıklaması                         | Dosya                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| XLSX biçimindeki gelen dosya - şablon    | [1099import-template.xlsx](https://go.microsoft.com/fwlink/?linkid=862266) |
| XLSX biçimindeki gelen dosya - örnek veriler | [1099import-data.xlsx](https://go.microsoft.com/fwlink/?linkid=862266)     |

Finance and Operations uygulamasında henüz [ER - Harici bir dosyadan veri içeri aktarmak için gerekli yapılandırmaları oluşturma](./tasks/er-required-configurations-import-data.md) görev kılavuzunu yürütmediyseniz aşağıdaki dosyayı indirin.

| İçerik açıklaması    | Dosya                                                            |
|------------------------|-----------------------------------------------------------------|
| ER modeli yapılandırması | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=862266) |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]