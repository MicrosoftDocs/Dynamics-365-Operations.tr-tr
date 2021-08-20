---
title: Eksik çekilen madde yeniden tahsisini ayarlama
description: Bu konuda, size, ambar çalışanlarının yönlendirildikleri yerleşimde yeterli stok olmadığında alternatif yerleşimleri hızlı bir şekilde bulmalarının nasıl sağlanacağı gösterilmektedir.
author: ShylaThompson
ms.date: 06/29/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker, WHSLocationWithWorkException
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 84cefe723cff9566ed3004e49f1e829020bc0d416cd0b29258c21222fbeb05ab
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741896"
---
# <a name="set-up-short-picking-item-reallocation"></a>Eksik çekilen madde yeniden tahsisini ayarlama

[!include [banner](../../includes/banner.md)]

Bu yordam, size, ambar çalışanlarının yönlendirildikleri yerleşimde yeterli stok olmadığında alternatif yerleşimleri hızlı bir şekilde bulmalarının nasıl sağlanacağını göstermektedir. 

Yeniden tahsisat işlemi bir **İş özel durumu** ile denetlenir ve ambar **çalışanı** tarafından kullanılır.

Otomatik, El ile veya her iki yeniden tahsisat işlemi kullanılabilir:

- Otomatik yeniden tahsisat - Malların başka bir yerleşimde olup olmadığını belirlemek için yerleşim yönergeleri kullanılır. Mümkünse, iş güncelleştirilecek ve ambar kullanıcısı alternatif yerleşime yönlendirilecektir.
- El ile yeniden tahsisat - Ambar kullanıcısının rezerve edilmemiş mal miktarları olan bir veya daha fazla yerleşimden seçim yapmasına olanak tanır. 
- Otomatik ve el ile - Sistem otomatik yeniden tahsisat gerçekleştiremezse ve rezerve edilmemiş miktarlar bulunan yerleşimler varsa, kullanıcıdan bir yerleşim seçmesi istenir.

## <a name="set-up-work-exceptions"></a>İş özel durumlarını ayarla
Ambar çalışanının işledikleri sevkiyatın ihtiyaçlarına göre bir seçim yapabilmesi için, farklı madde yeniden tahsis ilkelerine sahip birden çok iş özel durumu tanımlamak mümkündür.

Bu yordamı oluşturmak için USMF demo verileri şirketi kullanılmıştır.

1. **Gezinti panosu**'nda, **Ambar yönetimi > Kurulum > İş > İş istisnaları**'na gidin.
2. **Yeni**'ye tıklayın 
3. **İş özel durumu kodu** alanına bir değer yazın. Bu, bu özel durumun başlığı olacaktır. Örneğin, Kısa malzeme çekme kılavuzu.
4. **Tanım** alanına bir değer girin. Bu, bu özel durumun kullanımıyla ilgili kısa bir açıklama olacaktır. Örneğin, Kısa malzeme çekme - madde mevcut değil.
5. **Özel durum** türü alanında, **Kısa çekme**'yi seçin.
6. **Stoğu ayarla** onay kutusunu işaretleyin. Seçilirse, stok kısa malzeme çekme yerleşiminde 0'a otomatik olarak ayarlanır.
7. **Varsayılan ayarlama türü kodu** alanına bir değer girin veya bir değer seçin. Örneğin, USMF'de **Kaynak Kaldırma Ayarlama Devre Dışı**'nı seçebilirsiniz. Her ayarlama türü kodu dört temel özellik içerir: ad, açıklama, stok günlüğü adı ve **Rezervasyonları kaldır**. **Rezervasyonları kaldır** etkinse, kısa çekilen sipariş satırının rezervasyonları kaldırılır.  
8. **Madde yeniden tahsisi** alanında bir değer seçin (örneğin El ile). El ile veya Otomatik ve El ile seçeneklerini belirlerseniz, ambar çalışanının el ile yeniden tahsisi kullanmak için etkinleştirilmesi gerekir.

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>Çalışanı el ile madde yeniden tahsisini kullanmak üzere ayarlama

Bu yordamı oluşturmak için USMF demo verileri şirketi kullanılmıştır.

1. Sayfayı kapatın.
2. **Gezinti panosu**'nda, **Ambar yönetimi > Kurulum > Çalışan**'a gidin.
3. **Düzenle**'yi tıklatın.
4. Listede çalışan seçin. Örneğin Julia Finanderburk.
5. **Kullanıcılar** hızlı sekmesini genişletin.
6. Listede bir **Kullanıcı kodu** seçin. Örneğin, 24.
7. **İş** hızlı sekmesini genişletin.
8. **El ile madde yeniden tahsisine izin ver** alanında **Evet**'i seçin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]