---
title: Gelen belgeleri Excel biçiminde ayrıştırma
description: Bu konu, gelen Microsoft Excel dosyalarındaki içeriği ayrıştırmak için Elektronik raporlama (ER) biçimleri tasarlama hakkında bilgi vermektedir.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 490a9325be25908564a40478a1ee29feea67fc02
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "367490"
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

Geçerli Dynamics 365 for Finance and Operation uygulamasında henüz [ER - Harici bir dosyadan veri içe aktarmak için gerekli yapılandırmaları oluşturma](./tasks/er-required-configurations-import-data.md) görev kılavuzunu oynatmadıysanız aşağıdaki dosyayı indirin.

| İçerik açıklaması    | Dosya                                                            |
|------------------------|-----------------------------------------------------------------|
| ER modeli yapılandırması | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=862266) |
