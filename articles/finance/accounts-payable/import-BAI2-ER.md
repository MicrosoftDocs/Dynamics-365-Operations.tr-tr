---
title: Elektronik raporlamayı kullanarak gelişmiş banka mutabakatı içe aktarmayı ayarlama
description: Bu konuda, BAI2 ekstreleri için gelişmiş banka mutabakatı içe aktarma işlemini ayarlamak üzere Elektronik raporlamanın nasıl kullanılacağı açıklanmaktadır.
author: panolte
ms.date: 03/30/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 39f1d8ba561ab0e36346f1dfb4f70df318c92a37
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544530"
---
# <a name="set-up-advanced-bank-reconciliation-import-by-using-electronic-reporting"></a>Elektronik raporlamayı kullanarak gelişmiş banka mutabakatı içe aktarmayı ayarlama

[!include [banner](../includes/banner.md)]

Gelişmiş banka mutabakatı özelliği, elektronik banka ekstrelerini içe aktarmanıza ve bunların Microsoft Dynamics 365 Finance'teki banka hareketleriyle otomatik olarak mutabakat sağlamasına izin verir. Bu konuda, BAI2 banka ekstreleriniz için içe aktarma işlevinin nasıl ayarlanacağı açıklanmaktadır.

## <a name="set-up-the-electronic-reporting-configuration"></a>Elektronik raporlama yapılandırmasını ayarlama

1. Sırasıyla **Çalışma alanları \> Elektronik raporlama**'ya gidin.
2. **Microsoft** yapılandırma sağlayıcısı kutucuğunda **Depolar**'ı seçin.
3. **Genel**'i seçin ve **Aç**'ı seçin.
4. Depoya bir bağlantı kurulması gerekiyorsa, iletişim kutusundaki mavi bağlantıyı seçin.
5. Yapılandırma listesinde, **Banka ekstresi modeli \> BAI2'nin banka ekstresi modeli**'ni bulun.
6. **BAI2** biçimini seçin.
7. **Sürümler** hızlı sekmesinde, en son sürümü ve sonra **İçe aktar**'ı seçin.

## <a name="set-up-the-bank-statement-format"></a>Banka ekstresi biçimini ayarlama

1. **Nakit ve banka yönetimi \> Kurulum \> Gelişmiş banka mutabakatı kurulumu \> Banka ekstresi biçimi**'ne gidin.
2. **Yeni**'yi seçin.
3. **Ekstre biçimi** ve **Ad** alanlarını ayarlayın.
4. **Genel elektronik içe aktarma biçimi** onay kutusunu seçin.
5. **İçe aktarma biçimi yapılandırma** alanını **BAI2** biçimine ayarlayın.

## <a name="set-up-the-bank-account"></a>Banka hesabını ayarlama

1. **Nakit ve banka yönetimi \> Banka hesapları \> Banka hesapları** öğesine gidin.
2. Banka hesabını açın.
3. **Mutabakat** hızlı sekmesinde, **Gelişmiş banka mutabakatı** seçeneğini **Evet** olarak ayarlayın.
4. **Ekstre biçimi** alanını daha önce oluşturulmuş **BAI2** biçimine ayarlayın.

## <a name="import-the-bank-statement"></a>Banka ekstresini içe aktarma

1. **Nakit ve banka yönetimi \> Banka ekstresi mutabakatı \> Banka ekstreleri**'ne gidin.
2. **Banka ekstreleri** sayfasının üst kısmında, **Ekstreyi içe aktar**'ı seçin.
3. **Banka hesabı** alanını ekstredeki banka hesabına ayarlayın.
4. **Ekstre biçimi** alanını daha önce oluşturulmuş **BAI2** biçimine ayarlayın.
5. **Gözat**'ı seçin ve **BAI** dosyasını seçin.
6. **Yükle**'yi seçin.
7. Seçilen dosyayı içe aktarmak için **Tamam**'ı seçin.
