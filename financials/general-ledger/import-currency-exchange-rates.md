---
title: "Para birimi döviz kurlarını içe aktar"
description: "Tüzel kişilik, yabancı para birimlerinde faturası almışsa, yabancı para birimi, yerel para birimine dönüştürmek gereklidir. Başka bir deyişle, farklı para birimlerinin döviz kurları güncel gereklidir. Bu konu gerekli ayarları ve döviz başvuru oranları Avrupa merkez bankası ve Merkez Bankası, Rusya gibi döviz kuru sağlayıcıları tarafından Internet üzerinden yayınlanan alma işlemi genel bir bakış sağlar."
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

Tüzel kişilik, yabancı para birimlerinde faturası almışsa, yabancı para birimi, yerel para birimine dönüştürmek gereklidir. Başka bir deyişle, farklı para birimlerinin döviz kurları güncel gereklidir. Bu konu gerekli ayarları ve döviz başvuru oranları Avrupa merkez bankası ve Merkez Bankası, Rusya gibi döviz kuru sağlayıcıları tarafından Internet üzerinden yayınlanan alma işlemi genel bir bakış sağlar.

Ayarlama ve döviz kurları alma için kullanılan bilgi akışını aşağıdaki bölümlerde açıklanmaktadır.

## <a name="configure-an-exchange-rate-provider"></a>Döviz kuru sağlayıcısı yapılandırma
Döviz Kurlarını almadan önce döviz kurları sunan sağlayıcıları tarafından gerekli olan bilgileri ayarlamanız gerekir. Kullanım **döviz kuru sağlayıcılarını yapılandırmak** döviz kuru sağlayıcı seçmek için sayfa. Bazı döviz kuru sağlayıcıları Microsoft Dynamics 365 işlemleri için örnek veride bulunmaktadır. Aşağıdaki tabloda, bu sayfadaki denetimler için açıklamalar sağlar.

|           |                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field** | **Description**                                                                                                                                                                                                             |
| **Name**  | Döviz kuru sağlayıcının adı.                                                                                                                                                                                     |
| **Key**   | Sağlayıcının istediği yapılandırma bilgilerinin her parçası için benzersiz kimlik. Bu bilgileri tıklattığınızda, eklediğiniz her döviz kuru sağlayıcısı için otomatik olarak eklenen **Ekle** düğmesi. |
| **Value** | Her bir anahtar için bilgi. Bu bilgileri tıklattığınızda eklemek için her bir döviz kuru sağlayıcısı eklenir **Ekle** düğmesi.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Para birimi döviz kurlarını içe aktar
Döviz kurları Döviz kuru sağlayıcıları kaynağından almak ve kısmında ayarlanan **döviz kurları** sayfa. Kullanım **alma döviz kurları** döviz kurlarını almak için sayfa. Aşağıdaki tabloda alma işlemini başarıyla tamamlamak için gerekli alanları açıklamalar sağlar.

|                                        |                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field**                              | **Description**                                                                                                                                                                                                                                                                                                                                                             |
| **Exchange rate type**                 | Bir döviz kuru türü.                                                                                                                                                                                                                                                                                                                                                      |
| **Exchange rate provider**             | Bir döviz kuru sağlayıcısı.                                                                                                                                                                                                                                                                                                                                                  |
| **Import as of**                       | Bu parametre, bugünün tarihi itibariyle veya tarih aralığı için alıp almamayı yönetir. Tarih aralığını kullanmak istiyorsanız, başlangıç ve bitiş tarihlerini seçin ya da girin.                                                                                                                                                                                                                |
| **Create necessary currency pairs**    | Bu onay kutusunu, alınan para çifti yoksa döviz çiftleri otomatik olarak oluşturulmasını yönetir. Bu seçenek, bazı sağlayıcılar için kullanılabilir olmayabilir.                                                                                                                                                                                               |
| **Override existing exchange rates**   | Bu onay kutusu zaten belirli bir tarih için döviz kuru varsa, güncelleştirme varolan döviz kurunun Döviz çifti için yönetir. Başka bir döviz kuru zaten varsa, bu onay kutusunu seçmezseniz, belirli tarihler için döviz kuru alınmaz.                                                                                       |
| **Prevent import on national holiday** | Bu onay kutusunu, döviz kurunun alma tarihi ortak bir tatil için yönetir. Bu onay kutusunu seçerseniz ve Avrupa merkez bankası döviz kuru sağlayıcısı olarak kullanın, örneğin, sistem döviz kuru geçerli yasal varlığıyla ilgili ortak bir tatil üzerinde güncelleştirmez. Bu seçenek, bazı sağlayıcılar için kullanılabilir olmayabilir. |




