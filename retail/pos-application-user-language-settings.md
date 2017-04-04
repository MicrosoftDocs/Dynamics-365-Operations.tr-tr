---
title: "POS uygulaması ve kullanıcı dil ayarları"
description: "Bu konu, perakende Modern POS (MPOS) ve bulut POS dil ayarlarının nasıl değiştirileceğini açıklar."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: bf5b75572529bb497d3079752de187f30aa59294
ms.lasthandoff: 03/31/2017


---

# <a name="pos-application-and-user-language-settings"></a>POS uygulaması ve kullanıcı dil ayarları

Bu konu, perakende Modern POS (MPOS) ve bulut POS dil ayarlarının nasıl değiştirileceğini açıklar.

<a name="overview"></a>Özet
========

Perakende Modern POS (MPOS) ve bulut POS nerede dil ayarları ve çevirileri mağaza ve kullanıcı ayarları arasında değişebilir ortamları destekler. Örneğin, burada İngilizce müşterileri için yaygın olarak kullanılır, ancak uygulamanın Fransızca çevirileri ile kullanmak bazı çalışanlar tercih bir bölge deposu konumlanabilir.

## <a name="data-language"></a>Veri dili
Kullanıcının ayarları ne olursa olsun, MPOS ve bulut POS her zaman mağazanın dil ayarları veri için kullanılan çevirileri belirlemek için kullanır. Bu, tüm kullanıcılar ve müşterilere tutarlı bir deneyim olacaktır garanti eder.  Veri örnekleridir:

-   Ürünler
-   Öznitelikler ve değerler
-   Kategori adları
-   Yazdırılan veya e-postayla gönderilen hareket girişleri
-   Ödeme yöntemi adları
-   Satır görüntüleme iletileri

Kullanıcı oturum açma önce bilinmez bu yana mağazanın dil ana POS oturum açma ekranı için de kullanılır. Çeviri mağazanın dil için kullanılabilir durumda değilse, POS şirketin diline döner.

### <a name="configuring-the-stores-language-setting"></a>Mağazanın dil ayarını yapılandırma

Mağazanın dil ayarı kümeden **tüm perakende mağazalar** üzerinde **perakende mağaza** altında sayfa ** genel &gt;bölgesel ayarlar &gt;dili. ** Bırak aşağı her mağaza için bir dil seçmek için kullanın.

## <a name="user-interface-language"></a>Kullanıcı arabirimi dili
POS kullanıcının dil ayarı uygulama kullanıcı arabiriminde kullanılan çevirileri belirler. Bu, tüm etiketleri, menüler ve veri kabul edilmez listeleri içerir. Bunun tek istisnası POS düğme grupları üzerinde görüntülenen metindir. Bunlar her zaman metin düğmesinde tanımlanan gösterir şekilde Çevirileri, düğme grupları desteklemez. Çevrilen düğme desteklemek için kopyalayıp korumak ayrı düğme grupları ve kullanıcıları uygun olarak atamanız gerekir.

### <a name="configuring-the-users-language-setting"></a>Kullanıcının dil ayarını yapılandırma

POS kullanıcının dil ayarı kümeden **tüm çalışanların** üzerinde **alt** altında sayfa **perakende &gt;dil**.  Ana profil sekmesinde ayarlı değil.  Bu ayar, POS tarafından kullanılmaz. Kullanıcının dili ayarlanmamışsa veya çevirilerin mevcut olmadığı bir dile ayarlanmışsa, POS mağazanın diline döner.  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| ** **       | **Kullanıcı Arabirimi dili** ** **      | **Veri dili (ürünler, makbuz biçimleri, satır görüntüleme, vs.)** |
| **Şirket** | Varsayılan Değer                    | Varsayılan Değer                                                           |
| **Mağaza**   | Şirketi geçersiz kılar          | Şirketi geçersiz kılar                                                 |
| **User**    | Mağazayı veya şirketi geçersiz kılar | Hiçbir Zaman                                                             |




