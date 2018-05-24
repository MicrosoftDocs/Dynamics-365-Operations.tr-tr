---
title: "Onarım yönetimi"
description: "Geçmişte başarılı olmuş önerilen çözümlerle yardım etmek üzere sorunları sistematik olarak gruplayın."
author: YuyuScheller
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAConditionTable, SMASymptomArea, SMADiagnosisArea, SMAResolutionTable, SMARepairStage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 937571968c6956ce3dba1427082b298983540f59
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---

# <a name="repair-management"></a>Onarım yönetimi       

[!include [banner](../includes/banner.md)]


Onarım yönetimi için sorunları sistematik olarak gruplandırabilirsiniz. Bu, geçmişte başarılı olmuş önerilen çözümlerle yardımcı olunmasını sağlar.

Belirtileri, tanıları ve çözüm ayarlarını ayarlayın. Onarım için benzer bir madde aldığınızda, bunların tümü daha sonra uygulanabilir. Bir onarım sorununun ilerlemesini takip edebilmek için onarım aşamaları da ayarlayabilirsiniz.

## <a name="setting-up-repair-management"></a>Onarım yönetimi ayarlama

Belirtileri, tanıları ve onarım çözümünü belirtmek için kullanılacak bilgileri girmek için aşağıdaki ayar formlarını kullanılır.

1.  **Servis yönetimi** \> **Kurulum** \> **Onarım** \> **Durumlar**'a tıklayın.

2.  **Servis yönetimi** \> **Kurulum** \> **Onarım** \> **Belirti alanları**'na tıklayın.

3.  **Servis yönetimi** \> **Kurulum** \> **Onarım** \> **Tanı alanları**'na tıklayın.

4.  **Servis yönetimi** \> **Kurulum** \> **Onarım** \> **Çözümler**'e tıklayın.

5.  **Servis yönetimi** \> **Kurulum** \> **Onarım** \> **Onarım aşamaları**'na tıklayın.

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

1.  **Servis yönetimi** \> **Ortak** \> **Servis siparişleri** \> **Servis siparişleri**'ne tıklayın.

2.  Onarım gerektiren servis kapsamındaki parça içeren servis siparişini seçin.

3.  **Onarım** \> **Onarım satırları**'nı tıklayarak **Onarım satırları** formunu açın.

4.  Yeni bir satır oluşturmak için Ctrl+N tuşlarına basın.

5.  Bir servis kapsamında parça seçin. Servis siparişinde bir parça ilişkisiyle ayarlanmış her türlü servis kapsamındaki parçayı seçebilirsiniz.

6.  Onarım satırında ilişkili olan önayarlı belirti, tanı ve uygulama değerlerinden birini seçin ve gerekirse onarım satırında bir not oluşturmak için **Not** sekmesini tıklatın.

7.  Yeni onarım satırını kaydetmek için CTRL+S tuşlarına basın. **Onarım satırları** formunun **Genel** sekmesindeki **Oluşturma tarihi ve saati** alanı formun kaydedildiği saatle güncelleştirilir.

## <a name="tracking-progress-and-resolving-a-repair-issue"></a>İlerlemeyi izleme ve bir onarım sorununu çözümleme

Onarımın ilerlemesini izlemek için bir onarım satırının onarım aşamalarını ayarlayabilirsiniz.

Bir onarım sorunu giderildiğinde, onarım satırını kapatabilirsiniz. Onarım aşamasını **Bitti** özelliği etkinleştirilmiş bir aşamaya ayarlayın. Geçerli tarih ve saat, satırdaki tamamlanma zamanı olarak kaydedilir.

## <a name="close-a-repair-line-for-a-resolved-issue"></a>Çözülen bir sorunun onarım satırını kapatma

1.  **Onarım satırları** formunu açın. Bu konunun başlarında bir onarım satırı oluşturmak için verilen yordamı takip edin.

2.  Kapatmak istediğiniz onarım sorununu içeren onarım satırını seçin.

3.  **Onarım aşaması** alanından, **Bitti** özelliği etkinleştirilmiş bir aşama seçin.

  



