---
title: Yeni ambar düzeni oluşturma
description: Bu yordam, ambardaki konumlarla ilgili bilgilerin nasıl ayarlanacağını gösterir.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: f0a52c5d68816a81a94db019387b9ea3ec3efc5a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845534"
---
# <a name="create-a-new-warehouse-layout"></a>Yeni ambar düzeni oluşturma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, ambardaki konumlarla ilgili bilgilerin nasıl ayarlanacağını gösterir. Bu, yalnızca Stok yönetim modülünde "temel depolama" kullanılarak oluşturulan depolar için geçerlidir; Ambar yönetimi modülünde oluşturulan depolara uygulanmaz. Bu yordamı, demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.


## <a name="set-the-default-location-capacity"></a>Varsayılan konum kapasitesini ayarlayın
1. Stokyönetimi > Kurulum > Stok ve ambar yönetim parametreleri'ne gidin.
2. Konumlar sekmesine tıklayın.
3. Standart genişlik alanına bir sayı girin.
4. Standart derinlik alanına bir sayı girin.
5. Standart yükselik alanına bir sayı girin.
6. Kaydet'e tıklayın.
7. Sayfayı kapatın.

## <a name="define-the-location-name-format"></a>Konum adı biçimini tanımlayın
1. Stok yönetimi > Kurulum > Stok dökümü > Ambarlar öğelerini seçin.
2. Yeni'ye tıklayın.
3. Ambar alanına bir değer yazın.
4. İsim alanına bir değer yazın.
5. Tesis alanında, aramayı açmak için açılır menü düğmesine tıklayın.
6. Listede, istenen kaydı bulun ve seçin.
7. Konum adları bölümünün genişletilmiş görünümüne geçin.
    * Bu bölümdeki seçenekler, konum adları için varsayılan biçimi belirler. Örneğimizde, koridor numarasını, dolap numarasını ve raf numarasını ekleyeceğiz.  
8. Koridoru dahil et seçeneğini Evet olarak ayarlayın.
9. Dolabı dahil et seçeneğini Evet olarak ayarlayın. 
10. Biçin alanına, dolap için bir değer girin.
    * Örneğin: -##  
11. Raf dahil et seçeneğini Evet olarak ayarlayın.
12. Biçin alanına, raf için bir değer girin.
    * Örneğin: -##  

## <a name="define-warehouse-locations"></a>Ambar konumlarını belirleyin
1. Eylem Bölmesinde, Ambar öğesine tıklayın.
2. Konum Sihirbazı'na tıklayın.
3. İleri düğmesini tıklatın.
4. Çıkış noktaları seçeneğinin seçimini kaldırın
5. Toplu konumlar seçeneğin seçimini kaldırın
6. İleri düğmesini tıklatın.
7. İleri düğmesini tıklatın.
8. İleri düğmesini tıklatın.
9. İleri düğmesini tıklatın.
10. İleri düğmesini tıklatın.
11. İleri düğmesini tıklatın.
12. İleri düğmesini tıklatın.
    * Bu sayfada gösterilen fiziksel boyutlar, bu yordamın başlangıcında belirlediğiniz boyutlardır.  
13. İleri düğmesini tıklatın.
14. Son düğmesini tıklatın.
15. Sayfayı kapatın.
16. Sayfayı yenileyin.

