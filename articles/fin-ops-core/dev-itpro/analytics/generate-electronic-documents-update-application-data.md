---
title: ER kullanarak elektronik belgeler oluşturma ve uygulama verilerini güncelleştirme
description: Giden elektronik belgeler oluşturmak için uygulamada kullanılabilen Elektronik raporlama (ER) biçimlerini tasarlayabilirsiniz.
author: kfend
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
ms.openlocfilehash: 1be618d16be2ce9e50c2a43864040dfd23a8ff69
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269676"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a>ER kullanarak elektronik belgeler oluşturma ve uygulama verilerini güncelleştirme

[!include [banner](../includes/banner.md)]

Giden elektronik belgeler oluşturmak için uygulamada kullanılabilen Elektronik raporlama (ER) biçimlerini tasarlayabilirsiniz. Ayrıca gelen elektronik belgeleri ayrıştıran ER biçimleri tasarlayabilir ve bu belgelerdeki içerikleri uygulama verisini güncelleştirmek için kullanabilirsiniz.

Bu işlev ile tek bir ER biçimi giden elektronik belgeleri oluşturmak ve daha sonra uygulama verisini güncelleştirmek için kullanılabilir. Bu özellik aşağıdaki senaryolarda kullanılabilir:

- Uygulama verisinin yinelenen işlemlerde kullanılmasını engellemek için bir uygulamanın verisini elektronik belgeler oluşturmak için kullanıldıktan hemen sonra işaretleyebilirsiniz. Örneğin, ödeme hareketlerini, bir oluşturulan ödeme iletisine dahil edilmelerinden sonra derhal zaten işlendi olarak işaretleyebilirsiniz.
- ER mantığı kullanılarak oluşturulmuş elektronik belgelerin ayrıntılarını depolamak için. Örneğin, ER ifadesi kullanılarak oluşturuluş bir benzersiz ödeme ileti kimlik saptaması. İfade, ER biçimi belgeleri oluşturmak için çalıştırıldığında, ER iletişim kutusunda girilen bilgiye dayanır.

Bu özellik hakkında daha fazla bilgi için Intrastat raporlama ve arşivleme ayrıntıları hakkında sizi bilgilendirecek ER Uygulama veri güncelleştirmesi ile belgeler oluşturma Görev kılavuzlarını (7.5.4.3 Al/Geliş BT hizmeti/çözüm bileşenleri (10677) iş işleminin parçası olarak) oynatın. Aşağıdaki dosyalar, bu Görev kılavuzlarındaki çeşitli adımları tamamlamak için gereklidir. Bu dosyaları yerel makinenize indirin ve kaydedin.

- [ER veri modeli konfigürasyonu: Intrastat (model)](https://download.microsoft.com/download/9/c/e/9ceeacbe-c13e-422e-96f2-594c4a6b45b7/Intrastatmodel.xml)
- [ER model eşleme yapılandırması: Intrastat (eşleme)](https://download.microsoft.com/download/2/1/d/21ddaaeb-64c5-4408-a35f-1ccb922d40a4/Intrastatmapping.xml)
- [ER biçim yapılandırma: Intrastat (biçim)](https://download.microsoft.com/download/8/b/b/8bbb8891-e88d-4739-b92a-2d1d2fffcb79/Intrastatformat.xml)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
