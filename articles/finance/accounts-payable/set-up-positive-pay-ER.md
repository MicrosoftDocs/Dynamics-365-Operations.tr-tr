---
title: Elektronik raporlamayı kullanarak pozitif ödeme dosyalarını ayarlama ve oluşturma
description: Bu konuda, Elektronik raporlama kullanılarak pozitif ödemenin nasıl ayarlanacağı açıklanmıştır.
author: panolte
ms.date: 03/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 43dd1a9cba1fe8df5cff26fe76af7e2957a0d6a4
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544520"
---
# <a name="set-up-positive-pay-files-by-using-electronic-reporting"></a>Elektronik raporlamayı kullanarak pozitif ödeme dosyalarını ayarlama

Bankaya sunulan çeklerin bir elektronik listesini oluşturmak için pozitif ödeme kurun. Ardından, bankaya bir çek sunulduğunda, banka bunu çek listesiyle karşılaştırır. Çek, çek listesindeki bir çekle uyuşuyorsa banka çeki serbest bırakır. Çek, listedeki bir çekle uyuşmuyorsa banka, çeki gözden geçirmek için tutar.

## <a name="set-up-the-electronic-reporting-configuration"></a>Elektronik raporlama yapılandırmasını ayarlama

1. Sırasıyla **Çalışma alanları \> Elektronik raporlama**'ya gidin.
2. **Microsoft** yapılandırma sağlayıcısı kutucuğunda **Depolar**'ı seçin.
3. **Genel**'i seçin ve **Aç**'ı seçin.
4. Depoya bir bağlantı kurulması gerekiyorsa, iletişim kutusundaki mavi bağlantıyı seçin.
5. Yapılandırma listesinde, **Pozitif ödeme modeli \> Pozitif ödeme biçimi**'ni bulup seçin.
6. **Sürümler** hızlı sekmesinde, en son sürümü ve sonra **İçe aktar**'ı seçin.

## <a name="set-up-a-positive-pay-format"></a>Bir pozitif ödeme biçimi kurma

1. **Nakit ve banka yönetimi \> Kurulum \> Pozitif ödeme biçimleri** seçeneğine gidin.
2. **Yeni**'yi seçin.
3. **Ödeme biçimi** ve **Açıklama** alanlarını ayarlayın.
4. **Genel elektronik dışa aktarma biçimi** onay kutusunu seçin.
5. **Dışa aktarma biçimi yapılandırma** alanını **Pozitif ödeme biçimi**'ne ayarlayın.

## <a name="assign-a-positive-pay-format-to-a-bank-account"></a>Pozitif ödeme biçimini bir banka hesabına atama

1. **Nakit ve banka yönetimi \> Banka hesapları \> Banka hesapları** öğesine gidin.
2. Banka hesabını açın.
3. **Genel** hızlı sekmesinde, **Pozitif ödeme biçimi** alanını daha önce oluşturulan biçime ayarlayın.
4. **Pozitif ödeme başlangıç tarihi** alanını mevcut tarih olarak ayarlayın.

## <a name="generate-a-positive-pay-file"></a>Pozitif ödeme dosyası oluştur

1. **Nakit ve banka yönetimi \> Banka Hesapları \> Banka Hesapları** öğesine gidin.
2. Pozitif ödemenin ayarlandığı bir banka hesabını açın.
3. **Ödemeleri yönet \> Pozitif ödeme \> Pozitif ödeme dosyası**'nı seçin.
4. **Kesme tarihi** alanını ayarlayın. Bu tarihten önce oluşturulan çekler dahil edilir.

Elde edilen XML dosyası indirilir.
