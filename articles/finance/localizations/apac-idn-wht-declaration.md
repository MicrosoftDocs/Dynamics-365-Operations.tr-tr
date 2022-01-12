---
title: Endonezya için stopaj vergisi raporu
description: Bu konuda, Endonezya için stopaj vergisi raporunun nasıl yapılandırılacağı ve oluşturulacağı açıklanmaktadır.
author: sndray
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: sndray
ms.search.validFrom: 2021-12-02
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6cf2f9240ea747054578c52343af34b15c250f38
ms.sourcegitcommit: f51e74ee9162fe2b63c6ce236e514840795acfe1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/21/2021
ms.locfileid: "7943668"
---
# <a name="withholding-tax-report-for-indonesia-id-00005"></a>Endonezya için stopaj vergisi raporu (ID-00005)

[!include [banner](../includes/banner.md)]

Bu konuda, Endonezya içindeki tüzel kişiliklerin e-Bupot uygulamasındaki stopaj hareketlerini raporlamak için kullandığı PPH stopaj vergisi dosyasının nasıl ayarlanacağı ve oluşturulacağı açıklanmaktadır.

Endonezya vergi dairesi (DGT), gelir vergisi (PPh) kanununun 23. ve/veya 26. maddesi kapsamında stopaj vergisini düşen veya tahsil eden ve KPP Pratama'ya kayıtlı olan vergiye tabi girişimcilerin (PKP), e-Bupot uygulamasını kullanarak 23. ve 26. madde kapsamındaki Gelir Vergisi Beyannamesini elektronik olarak raporlaması gerektiğini belirlemiştir. 

- **Madde 23** – Rapor, birincil adresin ülke/bölge kodunun Endonezya kodu olduğu satıcılardan gelen tüm stopaj hareketlerini içerir.
- **Madde 26** – Rapor, birincil adresin ülke/bölge kodunun Endonezya kodu olmadığı satıcılardan gelen tüm stopaj hareketlerini içerir.

## <a name="prerequisites"></a>Önkoşullar

- Tüzel kişiliğin birincil adresi Endonezya'da olmalıdır.
- **Özellik yönetimi** çalışma alanında **Genel stopaj vergisi** özelliği etkinleştirilmelidir. Özellikleri etkinleştirme hakkında daha fazla bilgi için [Özellik yönetimine genel bakış](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'a bakın

### <a name="download-electronic-reporting-configurations"></a>Elektronik raporlama yapılandırmalarını indirme

İçe aktarma dosyasının oluşturulması, Elektronik raporlama (ER) yapılandırmalarına bağlıdır. Yapılandırılabilir raporlamanın özellikleri ve kavramları hakkında daha fazla bilgi için [Elektronik raporlama](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md) konusuna bakın.

Üretim ve kullanıcı kabul sınamaları (UAT) ortamları için [Elektronik raporlama yapılandırmalarını Lifecycle Services'tan indirme](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md) konusundaki yönergeleri izleyin.

İçe aktarma dosyası oluşturmak için aşağıdaki yapılandırmaları depodan yükleyin:

- **Tax declaration model.version.93.xml** veya sonraki bir sürüm
- **Tax declaration model mapping.version.93.153.xml** veya sonraki bir sürüm
- **WHT PPh schema import (ID).version.93.14** veya sonraki bir sürüm

## <a name="set-up-general-ledger-parameters"></a>Genel kayıt defteri parametreleri ayarlama

1. **Vergi** \> **Kurulum** \> **Genel muhasebe parametreleri**'ne gidin.
2. **Stopaj vergisi** sekmesindeki **WHT beyan biçimi eşlemesi** alanında, **WHT PPh şemasını içe aktarma (ID)**'yi seçin. 
3. **Kode Bukti Potong** stopaj vergisi gelir türünü ayarlamak için **Vergi** \> **Kurulum** \> **Stopaj vergisi** \> **Stopaj vergisi gelir türleri**'ne gidin ve ardından kodları ilgili madde stopaj vergisi gruplarına atayın. Kodlar, e-Bupot uygulamasını kullanarak tümleştirme dosyası oluşturmak için gereklidir. 

## <a name="generate-the-withholding-import-file"></a>Stopaj içe aktarma dosyasını oluşturma

e-Bupot dosyasının belirli bir dönem için hazırlanması ve gönderilmesi işlemi, ödeme vergisini kapatma veya deftere nakletme işi sırasında deftere nakledilen stopaj vergisi hareketlerine dayanır.

Dosyayı oluşturmak için aşağıdaki adımları izleyin.

1. **Vergi** \> **Beyanlar** \> **Stopaj vergisi** \> **PPH içe aktarma dosyası e-bupot 23 ve 26**'ya gidin.
2. Raporun "başlangıç" ve "bitiş" tarihini seçin, ardından kapatma dönemini belirleyin.
3. Hareket tarihini girin ve ardından **Tamam**'ı seçin.
4. Dili seçin. Tüm raporlar ABD İngilizcesi (**en-us**) ve Endonezce (**id**) dillerine çevrilir.
5. İş türünü seçin ve sonra çek ve belge numaralarını girin. 
6. Raporun yönetici tarafından imzalanıp imzalanmadığını kontrol edin. Bu bilgi dosyada raporlanır. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
