---
title: Maliyet öğesi boyutu üyelerini ortak bir boyut öğeleri kümesine eşleme
description: Farklı maliyet öğesi boyut üyelerini ortak bir maliyet öğesi boyut üyesi kümesine eşleyerek verileri analiz amacıyla ortak bir biçimde birleştirirsiniz.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMDimensionMember, CAMDimensionMapping
audience: Application User
ms.reviewer: twheeloc
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7654f748fb0cfc70d76718f03a235c5d4d13a908
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735478"
---
# <a name="map-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a>Maliyet öğesi boyutu üyelerini ortak bir boyut öğeleri kümesine eşleme

[!include [banner](../includes/banner.md)]

Farklı maliyet öğesi boyut üyelerini ortak bir maliyet öğesi boyut üyesi kümesine eşleyerek verileri analiz amacıyla ortak bir biçimde birleştirirsiniz.

Global bir şirketseniz ve yasal muhasebe gereksinimlerine uymanız gerekiyorsa birden fazla hesap planı kullanabilirsiniz. Farklı hesap planlarından maliyet öğesi boyut üyelerini içe aktardığınızda hesaplar birbirine karışabilir. Ancak bu hesaplar aynı yapıda olabilir ve ortak bir biçim kullanarak tüm hesapların maliyetlerini analiz ve tahsis edebilirsiniz.

## <a name="map-cost-element-dimension-members-to-a-common-format"></a>Maliyet öğesi boyut üyelerini ortak bir biçime eşleme
Aşağıdaki örnekte bir maliyet denetleyicisi olarak, ABD hesap planı yapısından ve Fransız hesap planı yapısından maliyet öğesi boyut üyelerinin ortak bir maliyet öğesi boyut üyesi kümesine eşlendiği bir Maliyet muhasebesinde yeni bir maliyet öğesi boyutunu nasıl oluşturabileceğiniz gösterilmektedir. Bu ortak maliyet öğesi boyut üyesi kümesini iki tüzel kişiliğin maliyet verilerini bir maliyet muhasebesi genel muhasebesinde analiz edebilirsiniz.

| Kaynak: ABD hesap planı          | Kaynak: Fransız hesap planı           | Yeni maliyet öğesi boyut üyeleri ortak kümesi                        |
|------------------------------------|----------------------------------------------|-------------------------------------------------------------------------|
| ABD hesap planından içe aktarılmış maliyet öğesi boyut üyeleri | Fransız hesap planından içe aktarılmış maliyet öğesi boyut üyeleri | ABD ve Fransız maliyet öğesi boyut üyelerini ortak bir kümeye eşleme |
| 5001: Satış                   | 5001: Satış ve reklam                      | 5000: Satış ve reklam                               |
| 5030: Reklam             | 6390: Stok satınalma\*                          | 7000: Temizlik giderleri                                   |
| 7001: Temizlik giderleri              | 7001: Seyahat gideri                     | 7001: Seyahat giderleri                                                   |

\*Stok satınalma Fransız maliyet öğesi boyut üyesi eşlenmedi.

## <a name="currency-conversion"></a>Para birimi dönüştürme
Kullandığınız çeşitli hesap planları farklı para birimlerini kullanmak üzere ayarlanabilir. Bu durumda bir para birimi dönüşümü belirlediğinizden emin olun ve maliyet verilerinin maliyet öğesi boyut üyelerinin kullanıldığı maliyet muhasebesi genel muhasebesinde tanımlanan, doğru para birimini kullanarak işlenmesini sağlayın. Önceki örnekte, maliyet muhasebesi genel muhasebesinde ABD doları (USD) kullanılıyorsa eşlenen maliyet öğesi boyut üyeleri için hareketleri işlemek üzere ABD Doları'ndan (USD) Euro'ya (EUR) para birimi dönüşümü oluşturmanız gerekir.

## <a name="update-mappings-at-any-time"></a>Eşlemeleri herhangi bir anda güncelleştirme
Maliyet öğesi boyutunun eşleme tanımlarını istediğiniz zaman güncelleştirebilirsiniz. Eşlemeler tarihe göre geçerli olmadığından, değişiklikler maliyet hareketlerini bir sonraki işlemenizde veya maliyet hesaplamalarını çalıştırdığınızda uygulanır.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
