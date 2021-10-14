---
title: Oluşturmadan başlangıca toplu iş emri yaşam döngüsü
description: Bu yordam, bir toplu iş emrinin yaşam döngüsünün ilk kısmını adım adım açıklar.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7ca259ca8f176cd5bc76081836adcb7d272972b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579268"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a>Oluşturmadan başlangıca toplu iş emri yaşam döngüsü

[!include [banner](../../includes/banner.md)]

Bu yordam, bir toplu iş emrinin yaşam döngüsünün ilk kısmını adım adım açıklar.

Oluşturma, maliyet tahmini işleminden ve üretim işi planlamasından toplu iş emrine kadar tüm adımları içerir.



Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. 



Bu yordamı başka bir veri kümesiyle çalıştırmanın önkoşulları etkin bir formül ve rota sürümü ile sevk edilmiş bir ürün bulunmasıdır.


## <a name="create-a-batch-order"></a>Toplu iş emri oluşturma
1. Tüm üretim emirleri'ne gidin.
2. Yeni toplu iş emri'ni tıklatın.
3. Madde numarası alanında bir değer girin veya seçin.
4. Oluştur'a tıklayın.
5. Üretim alanına bir filtre uygulamak için 'b' değeriyle Hızlı Filtre'yi kullanın.

## <a name="view-production-formula-and-expected-co-products"></a>Üretim formülünü ve beklenen ortak ürünleri görüntüleme
1. Eylem Bölmesinde, Üretim emri öğesine tıklayın.
2. Formül’ü tıklatın.
3. Sayfayı kapatın.
4. Ortak ürünler’i tıklatın.
5. Sayfayı kapatın.

## <a name="estimate-the-batch-order"></a>Toplu iş emrini tahmin etme
1. Tahmin seçeneğine tıklayın.
2. Tamam'a tıklayın.
3. Eylem Bölmesinde Yönet'e tıklayın.
4. Hesaplama ayrıntılarını görüntüle seçeneğine tıklayın.
5. Sayfayı kapatın.

## <a name="release-the-batch-order"></a>Toplu iş emrini sevk etme
1. Eylem Bölmesinde, Üretim emri öğesine tıklayın.
2. Serbest bırak öğesine tıklayın.
3. Tamam'a tıklayın.

## <a name="schedule-production-jobs"></a>Üretim işlerini zamanlama
1. Eylem Bölmesinde, Planla öğesini tıklatın.
2. İşleri planla'ya tıklayın.
3. Sınırlı kapasite alanında Hayır'ı seçin.
4. Sınırlı malzeme alanında Hayır'ı seçin.
5. Tamam'ı tıklatın.
6. Eylem Bölmesinde, Üretim emri öğesine tıklayın.
7. Tüm işleri çalıştır'ı tıklatın.
8. Sayfayı kapatın.

## <a name="start-the-batch-order"></a>Toplu iş emrini başlatma
1. Başlat'a tıklayın.
2. Genel sekmesine tıklayın.
3. Malzeme çekme listesini şimdi naklet alanında Hayır seçeneğini belirleyin.
4. Tamam'a tıklayın.
5. Eylem Bölmesinde, Görüntüle öğesine tıklayın.
6. Malzeme çekme listesi'ni tıklatın.
7. Listede, seçili satırdaki bağlantıya tıklayın.
8. Sayfayı kapatın.
9. Sayfayı kapatın.
10. Rota kartı'nı tıklatın.
11. Listede, seçili satırdaki bağlantıya tıklayın.
12. Sayfayı kapatın.
13. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]