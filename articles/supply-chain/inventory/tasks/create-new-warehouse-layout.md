---
title: Yeni ambar düzeni oluşturma
description: Bu konu, ambardaki konumlarla ilgili bilgilerin nasıl ayarlanacağını açıklar.
author: perlynne
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 399c87c2e5ad26d5ccc1618cfb6520de3fcdc644
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145675"
---
# <a name="create-a-new-warehouse-layout"></a>Yeni ambar düzeni oluşturma

[!include [banner](../../includes/banner.md)]

Bu konu, ambardaki konumlarla ilgili bilgilerin nasıl ayarlanacağını açıklar. Bu, yalnızca Stok yönetim modülünde "temel depolama" kullanılarak oluşturulan depolar için geçerlidir; Ambar yönetimi modülünde oluşturulan depolara uygulanmaz. Bu yordamı, demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.


## <a name="set-the-default-location-capacity"></a>Varsayılan konum kapasitesini ayarlayın
1. Gezinme bölmesinde **Modüller > Stok yönetimi > Kurulum > Stok ve ambar yönetim parametreleri**'ne gidin.
2. **Yerleşim** sekmesini seçin.
3. **Standart genişlik** alanına bir sayı girin.
4. **Standart derinlik** alanına bir sayı girin.
5. **Standart yükselik** alanına bir sayı girin.
6. **Kaydet**'i seçin.
7. Sayfayı kapatın.

## <a name="define-the-location-name-format"></a>Konum adı biçimini tanımlayın
1. Gezinme bölmesinde **Modüller > Stok yönetimi > Kurulum > Stok dökümü > Ambarlar**'a gidin.
2. **Yeni**'yi seçin.
3. **Ambar** alanına bir değer yazın.
4. **Ad** alanına bir değer yazın.
5. **Tesis** alanında, aramadan istediğiniz kaydı seçin.
6. **Konum adları** bölümünün genişletilmiş görünümüne geçin. Bu bölümdeki seçenekler, konum adları için varsayılan biçimi belirler. Örneğimizde, koridor numarasını, dolap numarasını ve raf numarasını ekleyeceğiz.  
7. **Koridoru dahil et** seçeneğini **Evet** olarak ayarlayın.
8. **Dolabı dahil et** seçeneğini **Evet** olarak ayarlayın. 
9. **Biçim** alanına, dolap için bir değer girin.
10. **Raf dahil et** seçeneğini **Evet** olarak ayarlayın.
11. **Biçim** alanına, raf için bir değer girin.

## <a name="define-warehouse-locations"></a>Ambar konumlarını belirleyin
1. Eylem Bölmesinde, **Ambarlar**'ı seçin.
2. **Konum Sihirbazı**'nı seçin.
3. **Sonraki**'yi seçin.
4. **Çıkış noktaları** seçeneğinin seçimini kaldırın
5. **Toplu konumlar** seçeneğin seçimini kaldırın
6. **Bitiş**' seçeneğine gelene kadar **Sonraki**'yi seçin.
7. Sayfayı kapatın.
8. Sayfayı yenileyin.

