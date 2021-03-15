---
title: Bir ürün modeli için rotayı koruma
description: Bu yordamın çalıştırılması için bir ürün yapılandırma modeli bulunması gerekir.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 90ea3f65284cc97906002015c715d9f071202bdb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966842"
---
# <a name="maintain-route-for-a-product-model"></a>Bir ürün modeli için rotayı koruma

[!include [banner](../../includes/banner.md)]

Bu yordamın çalıştırılması için bir ürün yapılandırma modeli bulunması gerekir. Bu yordam, işlem sırasında yol göstermek için USMF demo şirketindeki son teknoloji hoparlör modelini kullanır.


## <a name="add-a-route-operation"></a>Rota operasyonu ekleme
1. Ürün varyantı model tanımı'na tıklayın.
2. Ürün yapılandırma modelleri'ne tıklayın.
3. Listede, istenen kaydı bulun ve seçin.
    * Bu alıştırma için son teknoloji hoparlör modelini seçin.  
4. Listede, seçili satırdaki bağlantıya tıklayın.
5. Rota operasyonları bölümünü genişletin.
6. Ekle öğesini tıklatın.
7. İsim alanına bir değer yazın.
8. Açıklama alanına bir değer girin.
9. Kaydet'e tıklayın.

## <a name="enter-route-operation-details"></a>Rota operasyonu ayrıntılarını girme
1. Rota operasyonu ayrıntıları'nı tıklatın.
2. Operasyon alanında bir değer girin veya bir değer seçin.
3. Oper. Hayır. bir sayı girin.
    * Operasyon numarası rota sırasını belirler.  
    * Rota operasyonundaki her bir özellik statik bir değer alabilir veya bir öznitelik ile eşleştirilebilir. Bir öznitelik ile eşleme yapılması yapılandırmanın parçası olarak bir değer ayarlanmasına neden olur.  
4. Rota grubu alanında bir değer girin veya bir değer seçin.
    * Rota grubu; maliyetlendirme, tüketim ve ayarlar için temel davranışı belirler.  
5. Kurulum sekmesine tıklayın.
6. Zaman sekmesini tıklatın.
7. İşlem miktarı alanına bir sayı girin.
    * Tek işlem sırasında işlenecek sayıyı belirleyin.  
8. Saatler/zaman alanında bir sayı girin.
    * Zaman oranını girin.  
9. Ayarla onay kutusunu işaretleyin.
10. Çalışma süresi alanında bir sayı girin.
    * Belirttiğiniz miktarın işlenme süresini belirleyin.  
11. Kaynak gereksinimleri sekmesini tıklatın.
12. Ekle öğesini tıklatın.
13. Listede, seçili satırı işaretleyin.
14. Gereksinim türü alanında bir seçenek belirleyin.
    * Sahip olmaları gereken belirli kaynakları veya özellikleri belirtmek isteyip istemediğinize karar verin.  
15. Gerkesinim alanında bir değer girin veya bir değer seçin.
16. Tamam'a tıklayın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]