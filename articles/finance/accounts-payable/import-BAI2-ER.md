---
title: Elektronik raporlamayı kullanarak gelişmiş banka mutabakatı içe aktarmayı ayarlama
description: Bu makalede, gelişmiş banka mutabakatı içeri aktarma işlemini ayarlamak üzere Elektronik raporlamanın nasıl kullanılacağı açıklanmaktadır.
author: angelad116
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
ms.openlocfilehash: 46a50f4b00125656fc185ad569b94eeef00dc3c3
ms.sourcegitcommit: 649f1db26da8f20602f11180fc565b7c59eaf545
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337582"
---
# <a name="set-up-advanced-bank-reconciliation-import-by-using-electronic-reporting"></a>Elektronik raporlamayı kullanarak gelişmiş banka mutabakatı içe aktarmayı ayarlama

[!include [banner](../includes/banner.md)]

Gelişmiş banka mutabakatı özelliği, elektronik banka ekstrelerini içe aktarmanıza ve bunların Microsoft Dynamics 365 Finance'teki banka hareketleriyle otomatik olarak mutabakat sağlamasına izin verir. Bu makalede banka ekstreleriniz için içe aktarma işlevinin nasıl ayarlanacağı açıklanmaktadır. Banka ekstresi içe aktarma işleminin kurulumu elektronik banka ekstrenizin biçimine bağlı olarak değişir. Microsoft Dynamics 365 Finance, üç banka ekstresi biçimini destekler: ISO20022, MT940 ve BAI2. 

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


## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Banka ekstresi biçimleri ve teknik düzenlerine örnekler
Aşağıda gelişmiş banka mutabakatını içe aktarma dosyası teknik düzen tanımları ve ilişkili üç banka ekstresi örnek dosyasına örnekler bulunmaktadır: [İçe aktarma dosyası örnekleri](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Teknik düzen tanımı                             | Banka ekstresi örnek dosya          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)     |
| DynamicsAXISO20022Layout | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)     |

