---
title: Üretim emri oluşturma
description: Bu prosedür, bir üretim emrinin nasıl oluşturulacağını gösterir.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdTable, ProdBOM, ProdRoute, ProdJournalCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ce08532b8281d730cd5fae4ebd634a08c5baeedd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439013"
---
# <a name="create-a-production-order"></a>Üretim emri oluşturma

[!include [banner](../../includes/banner.md)]

Bu prosedür, bir üretim emrinin nasıl oluşturulacağını gösterir. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu, üretim emri ömrünü açıklayan yedi yordamın birincisidir.


## <a name="create-a-production-order"></a>Üretim emri oluşturma
1. Üretim denetimi > Üretim emirleri > Tüm üretim emirleri'ne gidin.
2. Yeni üretim emri'ne tıklayın.
3. Madde numarası alanına 'D0001' girin.
4. Teslimat alanına bir tarih girin.
    * Teslim tarihi, zamanında teslimat yapılabilmesi için bir üretim emrinin ne zaman bitmesi gerektiğini belirtir. Bu tarih planlama işleminde kullanılabilir. Örneğin, emri teslim tarihinden geriye doğru planlayabilirsiniz.  
5. Miktarı '20' olarak ayarlayın.
    * Not: Ürün reçetesi numarası alanı, geçerli madde için etkin olan herhangi bir ürün reçetesi numarasını gösterir ancak onaylanan ürün reçetesi sürümlerinin listesinden etkin bir ürün reçetesi seçerek üretim emri için ürün reçetesini değiştirebilirsiniz.    Not: Rota numarası alanı, geçerli madde için etkin olan herhangi bir Rota numarasını gösterir ancak onaylanan Rota sürümlerinin listesinden etkin bir Rota seçerek üretim emri için Rotayı değiştirebilirsiniz.  
6. Oluştur'a tıklayın.

## <a name="validate-the-production-order"></a>Üretim emrini doğrulama
1. Listede, seçili satırdaki bağlantıya tıklayın.
    * Yeni oluşturduğunuz üretim emri numarası bağlantısına tıklayın. Bu, siparişle ilgili ayrıntılar sayfasını açar.  
2. Düzenle öğesine tıklayın.
3. Teslimat alanına bir tarih girin.
    * Örneğin, üretim emrinin teslim tarihini değiştirebilirsiniz.  
4. Kaydet'e tıklayın.
5. Sayfayı kapatın.

## <a name="update-the-bom"></a>Ürün reçetesini güncelleştirme
1. Eylem Bölmesinde, Üretim emri öğesine tıklayın.
2. Ürün reçetesine tıklayın.
    * Üretim emri oluşturulurken varsayılan verilerden kopyalanan ürün reçetesi verilerini doğrulamak için ürün reçetesi sayfasını açın. Bu yordamda, bir ürün reçetesi için miktarı güncelleştirmeniz gerekir.  
3. Düzenle öğesine tıklayın.
4. Miktar alanına bir sayı girin.
    * Ürün reçetesi satırındaki miktarı değiştirmek, üretim emrine ilişkin malzeme tüketiminin maliyet tahminini etkiler.  
5. Kaydet'e tıklayın.
6. Sayfayı kapatın.

## <a name="update-the-production-route"></a>Üretim rotasını güncelleştirme
1. Eylem Bölmesinde, Üretim emri öğesine tıklayın.
2. Rota'ya tıklayın.
    * Üretim emri oluşturulurken varsayılan verilerden kopyalanan ürün rotası verilerini doğrulamak için Rota sayfasını açın. Bu yordamda, bir üretim rotasındaki operasyonlardan biri için miktarı güncelleştirmeniz gerekir.  
3. Listede, istenen kaydı bulun ve seçin.
4. Düzenle öğesine tıklayın.
5. İşlem miktarı alanına bir sayı girin.
    * İşlem süresini değiştirmek tahmini rota tüketimini ve üretim emri maliyetini etkiler.  
6. Kaydet'e tıklayın.
7. Sayfayı kapatın.

