---
title: "Para birimi döviz kurlarını içe aktar"
description: "Bir tüzel kişilik, yabancı para birimlerinde faturalar almışsa, yabancı para birimini yerel para birimine dönüştürmek gereklidir. Başka bir deyişle, farklı para birimlerinin döviz kurlarının güncel olması gereklidir. Bu konu, Avrupa Merkez Bankası ve Rusya Merkez Bankası gibi döviz kuru sağlayıcıları tarafından İnternet üzerinden yayınlanan önemli yabancı referans döviz kurlarını içe aktarmak için gerekli ayarlar ve işlemler hakkında genel bir bakış sağlar."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: bf66a1b1c9314b454223274810a21913d54b702d
ms.lasthandoff: 03/31/2017


---

# <a name="import-currency-exchange-rates"></a>Para birimi döviz kurlarını içe aktar

[!include[banner](../includes/banner.md)]


Bir tüzel kişilik, yabancı para birimlerinde faturalar almışsa, yabancı para birimini yerel para birimine dönüştürmek gereklidir. Başka bir deyişle, farklı para birimlerinin döviz kurlarının güncel olması gereklidir. Bu konu, Avrupa Merkez Bankası ve Rusya Merkez Bankası gibi döviz kuru sağlayıcıları tarafından İnternet üzerinden yayınlanan önemli yabancı referans döviz kurlarını içe aktarmak için gerekli ayarlar ve işlemler hakkında genel bir bakış sağlar.

Aşağıdaki bölümler, yabancı döviz kurlarının içe aktarılmasında kullanılan bilgi akışının ayarlanması ve işlenmesini açıklar.

## <a name="configure-an-exchange-rate-provider"></a>Bir döviz kuru sağlayıcısı yapılandırma
Döviz kurlarını almadan önce, döviz kurlarını sunan sağlayıcılar tarafından gerek duyulan bilgileri ayarlamanız gerekir. **Döviz kuru sağlayıcılarını yapılandır** sayfasını kullanarak döviz kuru sağlayıcılarını seçin. Bazı döviz kuru sağlayıcıları Microsoft Dynamics 365 for Operations içerisindeki örnek veride bulunmaktadır. Aşağıdaki tabloda bu sayfadaki kontrollerle ilgili açıklamalar bulunur.

|           |                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Alan** | **Açıklama**                                                                                                                                                                                                             |
| **Ad**  | Döviz kuru sağlayıcının adı.                                                                                                                                                                                     |
| **Anahtar**   | Sağlayıcının istediği yapılandırma bilgilerinin her parçası için benzersiz kimlik. **Ekle** düğmesine tıkladığınızda her döviz kuru sağlayıcı ekleyişinizde bu bilgiler otomatik olarak eklenir. |
| **Değer** | Her bir anahtar için bilgi. **Ekle** düğmesine tıkladığınızda her döviz kuru sağlayıcı ekleyişinizde bu bilgiler eklenir.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Para birimi döviz kurlarını içe aktar
Döviz kurlarını, döviz kurları sağlayıcı kaynağından alabilirsiniz ve onları **Para birimi döviz kurları** sayfasında ayarlayabilirsiniz. Döviz kurlarını içe aktarmak için **Para birimi döviz kurlarını alma** sayfasını kullanın. Aşağıdaki tablo, alma işlemini başarıyla tamamlamak için gerekli alanların açıklamalarını sağlar.

|                                        |                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Alan**                              | **Açıklama**                                                                                                                                                                                                                                                                                                                                                             |
| **Döviz kuru türü**                 | Bir döviz kuru tipi.                                                                                                                                                                                                                                                                                                                                                      |
| **Döviz kuru sağlayıcı**             | Bir döviz kuru sağlayıcısı.                                                                                                                                                                                                                                                                                                                                                  |
| **Şu tarihten itibaren içe aktar:**                       | Bu parametre, bugünden itibaren veya bir tarih aralığı için almayı yönetir. Bir tarih aralığı kullanmak istiyorsanız, başlangıç ve bitiş tarihlerini seçin.                                                                                                                                                                                                                |
| **Gerekli para birimi çiftlerini oluştur**    | Bu onay kutusu, içe aktarılan para birimi çiftleri mevcut değilse, para birimi çiftlerinin otomatik olarak oluşturulmasını yönetir. Bu seçenek bazı sağlayıcılar için kullanılabilir olmayabilir.                                                                                                                                                                                               |
| **Mevcut döviz kurlarını geçersiz kıl**   | Bu onay kutusu, bir para birimi çifti için mevcut döviz kurunun güncelleştirilmesini yönetir, döviz kuru belirli bir tarih için halihazırda mevcutsa. Bu onay kutusunu seçmezseniz, belirli bir tarih için döviz kuru, başka bir döviz kuru halihazırda mevcutsa, içe aktarılmaz.                                                                                       |
| **Resmi tatilde içe aktarmayı önle** | Bu onay kutusu, resmi bir tatil olan bir tarih için döviz kurunu içe almayı yönetir. Örneğin, bu onay kutusunu seçerseniz ve Avrupa Merkez Bankası'nı döviz kur sağlayıcısı olarak kullanırsanız, sistem, geçerli tüzel kişilik ile ilgili bir resmi tatilde döviz kurunu güncelleştirmez. Bu seçenek bazı sağlayıcılar için kullanılabilir olmayabilir. |






