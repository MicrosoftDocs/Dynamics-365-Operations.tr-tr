---
title: ER kullanarak elektronik belgeler oluşturma ve uygulama verilerini güncelleştirme
description: Giden elektronik belgeler oluşturmak için uygulamada kullanılabilen Elektronik raporlama (ER) biçimlerini tasarlayabilirsiniz. Ayrıca gelen elektronik belgeleri ayrıştıran ER biçimleri tasarlayabilir ve bu belgelerdeki içerikleri uygulama verisini güncelleştirmek için kullanabilirsiniz.
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 333f91cef12b6564ca9bc668732b4cc038f0fa7e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181876"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a>ER kullanarak elektronik belgeler oluşturma ve uygulama verilerini güncelleştirme

[!include [banner](../includes/banner.md)]

Giden elektronik belgeler oluşturmak için uygulamada kullanılabilen Elektronik raporlama (ER) biçimlerini tasarlayabilirsiniz. Ayrıca gelen elektronik belgeleri ayrıştıran ER biçimleri tasarlayabilir ve bu belgelerdeki içerikleri uygulama verisini güncelleştirmek için kullanabilirsiniz.

Bu işlev ile tek bir ER biçimi giden elektronik belgeleri oluşturmak ve daha sonra uygulama verisini güncelleştirmek için kullanılabilir. Bu özellik aşağıdaki senaryolarda kullanılabilir:

- Uygulama verisinin yinelenen işlemlerde kullanılmasını engellemek için bir uygulamanın verisini elektronik belgeler oluşturmak için kullanıldıktan hemen sonra işaretleyebilirsiniz. Örneğin, ödeme hareketlerini, bir oluşturulan ödeme iletisine dahil edilmelerinden sonra derhal zaten işlendi olarak işaretleyebilirsiniz.
- ER mantığı kullanılarak oluşturulmuş elektronik belgelerin ayrıntılarını depolamak için. Örneğin, ER ifadesi kullanılarak oluşturuluş bir benzersiz ödeme ileti kimlik saptaması. İfade, ER biçimi belgeleri oluşturmak için çalıştırıldığında, ER iletişim kutusunda girilen bilgiye dayanır.

Bu özellik hakkında daha fazla bilgi için Intrastat raporlama ve arşivleme ayrıntıları hakkında sizi bilgilendirecek ER Uygulama veri güncelleştirmesi ile belgeler oluşturma Görev kılavuzlarını (7.5.4.3 Al/Geliş BT hizmeti/çözüm bileşenleri (10677) iş işleminin parçası olarak) oynatın. Aşağıdaki dosyalar, bu Görev kılavuzlarındaki çeşitli adımları tamamlamak için gereklidir. Bu dosyaları yerel makinenize indirin ve kaydedin.

- [ER veri modeli konfigürasyonu: Intrastat (model)](https://go.microsoft.com/fwlink/?linkid=849038)
- [ER model eşleme yapılandırması: Intrastat (eşleme)](https://go.microsoft.com/fwlink/?linkid=849038)
- [ER biçim yapılandırma: Intrastat (biçim)](https://go.microsoft.com/fwlink/?linkid=849038)