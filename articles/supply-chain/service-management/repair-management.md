---
title: Onarım yönetimi
description: Geçmişte başarılı olmuş önerilen çözümlerle yardım etmek üzere sorunları sistematik olarak gruplayın.
author: sorenva
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAConditionTable, SMASymptomArea, SMADiagnosisArea, SMAResolutionTable, SMARepairStage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 32372a6a54e2adfbf511e2247be4a9baa28b4b53
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015215"
---
# <a name="repair-management"></a>Onarım yönetimi       

[!include [banner](../includes/banner.md)]


Onarım yönetimi için sorunları sistematik olarak gruplandırabilirsiniz. Bu, geçmişte başarılı olmuş önerilen çözümlerle yardımcı olunmasını sağlar.

Belirtileri, tanıları ve çözüm ayarlarını ayarlayın. Onarım için benzer bir madde aldığınızda, bunların tümü daha sonra uygulanabilir. Bir onarım sorununun ilerlemesini takip edebilmek için onarım aşamaları da ayarlayabilirsiniz.

## <a name="setting-up-repair-management"></a>Onarım yönetimi ayarlama

Belirtileri, tanıları ve onarım çözümünü belirtmek için kullanılacak bilgileri girmek için aşağıdaki ayar formlarını kullanılır.

- **Servis yönetimi** \> **Kurulum** \> **Onarım** \> **Durumlar**.
- **Servis yönetimi** \> **Kurulum** \> **Onarım** \> **Belirti alanları**.
-  **Servis yönetimi** \> **Kurulum** \> **Onarım** \> **Tanı alanları**.
- **Servis yönetimi** \> **Kurulum** \> **Onarım** \> **Çözümler**.
- **Servis yönetimi** \> **Kurulum** \> **Onarım** \> **Onarım aşamaları**.

## <a name="symptoms-and-conditions"></a>Belirtiler ve durumlar

Belirtiler, müşterinin sorunu nasıl tanımladığıdır. Belirtiler onarım gerektiğini gösteren müşteri gözlemlerini içerir.

Belirti alanları, belirti kodları ve koşulları ayarlayabilirsiniz. Belirti alanı arıza alanını kapsar ve belirti kodu da arıza belirtisini kapsar. Durum, sorun oluştuğundaki durumu veya ortamı açıklar.

**Örnek**

Bir bilgisayar, uzun süreli kullanımdan sonra sabit disk arızalandığı için onarıma alınır. Sabit disk arızası bir mavi ekran hatasına neden olur. Bilgisayarı alan teknisyen aşağıdaki belirtileri ve durumları girer:

1.  Belirti alanı sabit disktir

2.  Belirti kodu mavi ekran hatasıdır

3.  Durum sabit diskin uzun süreli kullanımı sonrasında arızalanmasıdır

## <a name="diagnosis-and-resolutions"></a>Tanı ve çözümler

Tanı ve çözüm alanları onarım açısından olan ifadelerdir. Bunlar, bir teknisyenin sorunu incelemek için takip ettiği adımlardır.

Tanı alanı, sorunu çözmek için oluşması gereken operasyonu kapsar. Tanı kodu sorunun nasıl ele alındığını ifade eder ve çözüm maddenin onarılması, değiştirilmesi veya siparişin müşteri tarafından iptal edilmesi şeklinde olabilir. Örneğin, bilgisayar onarılmışsa, tanı alanı "arızalı parça", tanı kodu "takılan yeni video kartı" ve çözüm "değiştirildi" olabilir.

## <a name="repair-stages"></a>Onarım aşamaları

Onarım aşamaları onarım sürecinin ilerlemesini belirtir. Onarım aşaması, onarım satırının tamamlandığını ve tamamlanma tarihi ve saatinin kaydedildiğini gösteren bir **Bitti** kapatma parametresi taşır.

## <a name="applying-repair-management"></a>Onarım yönetimini ayarlama

Bir maddeye onarım yönetim uygulamak için maddenin bir servis siparişinde bir servis kapsamındaki parça ilişkisiyle ayarlanması gerekir. Ardından servis siparişinden, geçerli sorun hakkındaki bilgiler içeren bir onarım satırı oluşturabilirsiniz. Onarım satırında, onarımda olan servis kapsamındaki parçayı ve sistem, tanı ve uygulama hakkındaki bilgileri tanımlarsınız. Ayrıca onarım satırı için bir not da oluşturabilirsiniz.

Onarım işlemindeki her adım için onarım satırları oluşturabilirsiniz.

## <a name="create-a-repair-line-on-a-service-order"></a>Bir servis siparişinde onarım satırı oluşturma

1.  **Servis yönetimi** \> **Servis siparişleri** \> **Servis siparişleri**'ne gidin.

2.  Onarım gerektiren servis kapsamındaki parça içeren servis siparişini seçin.

3.  **Onarım** \> **Onarım satırları**'nı seçerek **Onarım satırları** formunu açın.

4.  Yeni bir satır oluşturmak için **Yeni**'yi seçin.

5.  Bir servis kapsamında parça seçin. Servis siparişinde bir parça ilişkisiyle ayarlanmış her türlü servis kapsamındaki parçayı seçebilirsiniz.

6.  Onarım satırında ilişkili olan önayarlı belirti, tanı ve uygulama değerlerinden birini seçin ve gerekirse onarım satırında bir not oluşturmak için **Not** sekmesini seçin.

7.  Yeni onarım satırını kaydetmek için **Kaydet**'i seçin. **Onarım satırları** formunun **Genel** sekmesindeki **Oluşturma tarihi ve saati** alanı formun kaydedildiği saatle güncelleştirilir.

## <a name="tracking-progress-and-resolving-a-repair-issue"></a>İlerlemeyi izleme ve bir onarım sorununu çözümleme

Onarımın ilerlemesini izlemek için bir onarım satırının onarım aşamalarını ayarlayabilirsiniz.

Bir onarım sorunu giderildiğinde, onarım satırını kapatabilirsiniz. Onarım aşamasını **Bitti** özelliği etkinleştirilmiş bir aşamaya ayarlayın. Geçerli tarih ve saat, satırdaki tamamlanma zamanı olarak kaydedilir.

## <a name="close-a-repair-line-for-a-resolved-issue"></a>Çözülen bir sorunun onarım satırını kapatma

1.  **Onarım satırları** formunu açın. Bu makalenin başlarında bir onarım satırı oluşturmak için verilen yordamı takip edin.

2.  Kapatmak istediğiniz onarım sorununu içeren onarım satırını seçin.

3.  **Onarım aşaması** alanından, **Bitti** özelliği etkinleştirilmiş bir aşama seçin.

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]