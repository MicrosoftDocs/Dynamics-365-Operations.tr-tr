---
title: Stok uygunluğu denetleme
description: Bu prosedürde size belirli bir madde numarası için eldeki ve fiziksel stoğun nasıl kontrol edileceği gösterilmektedir.
author: ShylaThompson
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e0c00b2a79ab588ff47c249f73570544d884b79e
ms.sourcegitcommit: 25fe679b73663fda6b5b3c32646026d0993a9f00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/12/2019
ms.locfileid: "1995269"
---
# <a name="check-the-availability-of-stock"></a>Stok uygunluğu denetleme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu prosedürde size belirli bir madde numarası için eldeki ve fiziksel stoğun nasıl kontrol edileceği gösterilmektedir. Ayrıca, bir maddeyle ilgili tedarik bilgilerinin nasıl alınacağı da gösterilmektedir. Eldeki fiziksel stok, eldeki mevcut, yani satın alınmış, teslim alınmış ve kaydedilmiş stoktur. Eldeki stok, eldeki mevcut stoğun yanı sıra, sipariş edilip beklenen ve henüz teslim alınıp kaydedilmemiş stoğu da içerir. Bu yordamı, USMF demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz. USMF kullanıyorsanız, gösterilen örnek değerleri kullanabilirsiniz. Bu görevler genellikle bir ambar çalışanı tarafından yerine getirilir.


## <a name="check-on-hand-inventory-for-an-item"></a>Eldeki stokta bir maddeyi kontrol edin
1. **Gezinti bölmesi > Modüller > Stok yönetimi > Sorgular ve raporlar > Eldeki stok** öğesine gidin.
2. **Madde numarası** satırını seçin. Eldeki stoğu madde numarasına göre sorgulamak için, Tablo ayarının **Eldeki stok** ve Alan ayarının **Madde** numarası olarak ayarlandığı satırı seçin.
3. **Ölçütler**  alanında, sorgulamak istediğiniz maddeyi seçin. USMF demo verileri şirketini kullanıyorsanız "M9201" seçebilirsiniz.  
4. **Tamam**'a tıklayın.
5. **Eylem bölmesinde** **Boyutlar** öğesine tıklayın. **Boyutlar** sekmesi, eldeki stoğunuz hakkında ne kadar ayrıntı görmek istediğinizi seçmenize olanak sağlar. Rezervasyonla ilgili verilere gereksiniminiz varsa, gelişmiş ambar (WHS) işlemlerini kullanan maddeler için tüm stok boyutlarını görüntülemeniz gerekir.
6. **Tamam**'a tıklayın.
7. **Eylem Bölmesinde**, **İlgili bilgiler**'e tıklayın. Bu seçeneği görmüyorsanız, ek eylem bölmesi seçeneklerini görmek için üç nokta düğmesine (...) tıklamanız gerekebilir.
8. **Tedarik özeti**'ne tıklayın. **Tedarik özeti** sekmesinde, belirli bir maddenin eldeki miktar, sağlama süresi ve satıcı bilgileri gibi tedarik bilgileri verilir.  
9. **Eldeki** bölümünü genişletin.
10. **Satıcılar** bölümünü genişletin.
11. Sayfayı kapatın.
12. Sayfayı kapatın.

## <a name="check-physical-on-hand-inventory"></a>Eldeki fiziksel stoğu kontrol edin
1. **Gezinti bölmesi > Modüller > Ambar yönetimi > Sorgular ve raporlar > Fiziksel eldeki stok** öğesine gidin.
2. **Madde numarası** alanına bir değer girin. Maddeler listesini filtre etmek için Tesis ve Ambar alanlarını kullanabilirsiniz. 
3. Sayfayı yenileyin.
4. **Eylem bölmesinde** **Boyutları Görüntüle**'ye tıklayın. Boyutların Görünümü sekmesi, eldeki stoğunuz hakkında ne kadar ayrıntı görmek istediğinizi seçmenize olanak sağlar.
5. **Tamam**'a tıklayın.
6. Sayfayı kapatın.

## <a name="check-on-hand-inventory-by-location"></a>Eldeki stoğu yerleşime göre kontrol edin
1. **Gezinti bölmesi > Modüller > Ambar yönetimi > Sorgular ve raporlar > Yerleşime göre eldeki** öğesine gidin.
2. **Ambar** alanına bir değer yazın. USMF demo veri şirketini kullanıyorsanız, "51" kullanabilirsiniz.  
3. Sayfayı yenileyin.
4. **Boyutları Görüntüle**'ye tıklayın.
5. **Tamam**'a tıklayın.
6. Sayfayı kapatın.

