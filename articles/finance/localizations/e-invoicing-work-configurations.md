---
title: Yapılandırmalarla çalışma
description: Bu makalede, Genelleştirme özellikleri çalışma alanındaki Elektronik raporlama (ER) yapılandırmalarıyla çalışmaya yönelik ana senaryona dair genel bir bakış sağlanmaktadır.
author: gionoder
ms.date: 01/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: d87559405d2490c314eb2c8b88268af0dc0dfaca
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283070"
---
# <a name="work-with-configurations"></a>Yapılandırmalarla çalışma

[!include [banner](../includes/banner.md)]

Elektronik raporlama (ER) konfigürasyonları, elektronik faturalama özelliklerinin ana bileşen kümelerinden biridir. Bir ER konfigürasyonu, dosya yapısının kurulumunu ve verileri dönüştürmek için iki şekilde bir dizi dönüştürme kuralını içerir:

- **ER biçimi konfigürasyonunu dışa aktarma** – Bu konfigürasyon, birleşik iç yapıdaki (ER model) verileri elektronik dosya biçimine dönüştürür.
- **ER biçimi konfigürasyonunu içe aktarma** – Bu konfigürasyon, elektronik dosya biçiminden birleşik iç yapıya (ER model) verileri dönüştürür.

Ön tanımlı biçimde giden elektronik dosyaları oluşturmaya ek olarak, ER yapılandırmaları gelen iletileri harici bir web servisinden yanıt olarak ayrıştırmak için yaygın olarak kullanılır. Bu işlev, harici kanallarla iletişim sonuçlarını almak, bu sonuçları (kodlar, iletiler ve günlükler) kullanıcı tarafından okunabilen yapıya dönüştürmek ve sonra bu bilgileri istemci uygulamasına geçirmek için yapılandırılabilir mantık oluşturmaya yardımcı olur.

Elektronik faturalama özelliğindeki ER yapılandırmalarını kullanmaya başlamak için, bunları özelliğe bağlamanız ve geçerli özellik sürümü için **Yapılandırmalar** sekmesinde kullanılabilir hale getirmeniz gerekir. **Ekle**, **Sil**, **Düzenle** veya **Görüntüle** seçeneklerini belirleyerek bağlantılı ER yapılandırmasıyla çalışabilirsiniz.

Bir ER yapılandırmasına bağlantı ekleyebilmeniz için, yapılandırmanın mevzuat Regulatory Configuration Service (RCS) deponuzda var olması gerekir. RCS deponuzda bulunan ER yapılandırmalarını gözden geçirmek için, aşağıdaki adımları izleyin.

1. RCS hesabınızda oturum açın.
2. **Elektronik raporlama** çalışma alanı içinde **Yapılandırmalar** bölümünde **Raporlama yapılandırmaları** kutucuğunu seçin.

Yeni bir ER yapılandırması oluşturma veya Genel depodan varolan bir ER yapılandırmasını alma hakkında bilgi için bkz. [Elektronik raporlama](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Bağlı bir ER yapılandırmasını ayarlamak için, geçerli elektronik faturalama özelliğine ait **Konfigürasyonlar** sekmesinde **Düzenle**'yi seçin. Sistem, ER yapılandırmasının bir sürümünü otomatik olarak oluşturur. Geçerli sürüm etkin konfigürasyon sağlayıcısı tarafından oluşturulmamışsa, sistem konfigürasyon sağlayıcınızı kullanan bir türetilmiş sürüm oluşturur. Geçerli sürüm etkin konfigürasyon sağlayıcısı tarafından oluşturulduysa, sistem yeni bir sürüm oluşturur. Her iki durumda da oluşturulan sürümü değiştirebilir ve sonra gerekli tüm güncelleştirmeleri otomatik olarak yapabilirsiniz.
