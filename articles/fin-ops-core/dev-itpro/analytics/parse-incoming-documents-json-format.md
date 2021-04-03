---
title: Gelen belgeleri JSON biçiminde ayrıştırma
description: Bu konu, gelen belgeleri JavaScript Nesne Gösterimi (JSON) biçiminde ayrıştırmak için Elektronik raporlama (ER) biçimlerinin nasıl ayarlanacağını açıklamaktadır.
author: kfend
manager: AnnBe
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: d39a697876641b4c9647dc1a55243ac2ca7cb9e7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564507"
---
# <a name="parse-incoming-documents-in-json-format"></a>Gelen belgeleri JSON biçiminde ayrıştırma

[!include[banner](../includes/banner.md)]

JavaScript (başka bir deyişle JavaScript Nesne Gösterimi \[JSON\] biçimindeki dosyalar) tabanlı bir metin biçiminde verileri temsil eden elektronik belgeleri ayrıştırmak için Elektronik raporlama (ER) biçimleri tasarlayabilirsiniz.

Bu özellik hakkında daha fazla bilgi edinmek için, aşağıdaki tabloda bulunan dosyaları yükleyin ve sonra da bir harici JSON dosyası görev kılavuzundaki verileri içe aktarmak üzere bir biçim yapılandırması oluşturun. Bu görev kılavuzu, bir ER biçiminin uygulama verilerini güncelleştirmek üzere gelen bir JSON dosyasını ayrıştırmak için nasıl kullanılabileceğini göstermektedir.

| Ünvan                                  | Dosya adı |
|----------------------------------------|-----------|
| ER biçim yapılandırması                | [Satıcıların hareketlerini içe aktarma biçimi trans_JSON.xml](https://go.microsoft.com/fwlink/?linkid=874111) |
| .cvs biçimindeki gelen dosya örneği | [1099entries_JSON.txt](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a>Gereksinimler

Bir ER biçim yapılandırması tamamlanmadan önce harici bir JSON dosyası görev kılavuzundan veri içe aktarmak için aşağıdaki gereksinimin karşılanması gerekir:

- JSON dosyasındaki üst öğeler yalnızca nesne öğeleri olabilir.
- Bir nesnenin iç içe yerleştirilmiş öğeleri özellik öğeleri olmalıdır ve böylece geçerli bir JSON yapısı oluşturulur.
- JSON dizileri, bir nesnenin özellik öğelerinin yalnızca iç içe yerleştirilmiş öğelerdir.
- JSON dizileri yalnızca JSON nesnelerini içerebilir. Doğrudan dize/sayısal değerler ve iç içe diziler içeremez. Bu dizilerde bulunan öğeler, (biçiminde belirtildiği gibi) sıralı olarak ayrıştırılacaktır. Her JSON nesnesindeki çokluluk ayarları dikkate alınır.

Ek olarak, henüz tamamlamadıysanız [ER Harici bir dosyadan veri almak için gerekli olan yapılandırmaları oluşturma](tasks/er-required-configurations-import-data.md) görev kılavuzunu tamamlamanız gerekir. Görev kılavuzunu tamamlamak için aşağıdaki dosyayı indirin.

| Ünvan                  | Dosya adı |
|------------------------|-----------|
| ER modeli yapılandırması | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=874111) |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]