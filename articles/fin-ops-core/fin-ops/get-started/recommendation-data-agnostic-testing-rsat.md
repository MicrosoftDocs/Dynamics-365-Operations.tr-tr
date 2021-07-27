---
title: Regression Suite Automation Tool kullanarak veri belirsiz test
description: Bu konu altında, Regression Suite Automation Tool kullanarak veri belirsiz test yapma önerileri tartışılmaktadır.
author: kfend
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2019-09-11
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: e4795d11ac370003e48dc845c86ec8a5ba22aa86
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6348667"
---
# <a name="data-agnostic-testing-using-the-regression-suite-automation-tool"></a>Regression Suite Automation Tool kullanarak veri belirsiz test

[!include [banner](../includes/banner.md)]

Bir ERP uygulamasının işlevsel doğrulaması tam veri belirsiz olamaz; test etmek için birden çok aşama ve yaklaşım vardır. Bu test aşamaları şunları içerir:  

- SysTest çerçevesi
- ATL çerçevesi
- Regression Suite Automation Tool (RSAT)

[![Test sınıflandırması piramidi.](./media/rsat-data-agnostic-testing-01.PNG)](./media/rsat-data-agnostic-testing-01.PNG)

## <a name="overview"></a>Genel bakış
-   **SysTest çerçevesi** – SysTest çerçevesi, birim testleri yazmak için güvenilirdir. Birim testleri genellikle bir yöntem veya işlevi test ettiğinden, her zaman veri belirsiz olmaları ve yalnızca testin parçası olarak sağlanan giriş verilerine bağlı olmaları gerekir.
-   **ATL çerçevesi** – Microsoft, SysTest çerçevesi üzerinde bir soyutlama olan bir ATL çerçevesine sahiptir ve işlevsel test yazmayı çok daha basit ve güvenilir hale getirir. Bu çerçeve, bileşen testleri veya basit tümleştirme testleri yazmak için kullanılmalıdır.
-   **RSAT** – RSAT, tümleştirme testleri ve iş döngüsü testleri için kullanılır. Regresyon doğrulama testleri olarak da adlandırılan iş döngüsü testleri varolan verilere bağlıdır. Ancak, ek faktörleri dikkate alırsanız, bu testler veri belirsiz hale gelebilir. 

    - Birim testleri ve bileşen testleri düşük düzeydeyse ve tamamen veri belirsiz olabiliyorsa (varolan bir veri kümesine bağlı değilse), iş döngüsü veya regresyon doğrulama testleri, mevcut bazı verilere bağlıdır. Bu veriler kurulumu, yapılandırma ayarlarını (parametreler) ve ana verileri (müşteri, satıcılar, maddeler vb.) içerir ancak hiçbir zaman hareket verisi içermez. Test sırasında bunların herhangi biri değiştiriliyorsa, son testin bir parçası olarak, değişen verilerin eski hallerine geri döndürüldüğünden emin olun.
    - Belirli bir kaydı seçmek yerine, belirli ölçütlere göre ana verileri seçin. Örneğin, boyut değerlerine ve stok kullanılabilirliğine göre bir madde seçmek istiyorsanız, ürün listesini bu değerlerle filtreleyin, ilk maddeyi seçin ve gelecekteki testler için kullanmak üzere numarayı kopyalayın. Müşteri, satıcı veya madde gibi basit bir ana veri satırıysa, otomasyonun bir parçası olarak oluşturulabilir ve zincirleme aracılığıyla gelecekteki testlerde kullanılabilir. 
    - Fatura numarası gibi benzersiz kimlik tanımlayıcıları numara sırasına göre veya =TEXT(NOW(),"yyyymmddhhmm") gibi Microsoft Excel işlevlerini kullanarak girin. Bu işlev, her dakika, bu eylemin ne zaman gerçekleştiğini izlemenize olanak sağlayan benzersiz bir numara sağlayacaktır. Bu, ürün giriş numaraları ve satıcı fatura numaraları gibi değişkenler için kullanılabilir. Bu testler, geri yükleme gerektirmeden, aynı veritabanı üzerinde tekrar tekrar çalışmaya devam eder.
    - Varsayılan seçenek **Otomatik** olduğundan, ortamın **Düzenleme modu** ayarını ilk test olayı olarak **Oku** veya **Düzenle** yapın. **Otomatik** seçenekleri her zaman önceki ayarı kullanır ve güvenilmez testlere neden olabilir. 
 
    [![Seçenekler sayfası, Performans sekmesi.](./media/rsat-data-agnostic-testing-02.PNG)](./media/rsat-data-agnostic-testing-02.PNG)
 
    - Genel doğrulama yerine yalnızca belirli bir harekete filtre uyguladıktan sonra doğrulayın. Örneğin kayıt numarası için hareket numarasına veya hareket tarihine filtre uygulayarak, doğrulamanın tüm diğer hareketleri hariç tutmasını sağlayın. 
    - Bir müşteri bakiyesini veya bütçe kontrolünü denetliyorsanız, önce değeri kaydedin ve ardından, sabit beklenen değeri doğrulamak yerine, beklenen sonucu doğrulamak için hareket değerini ekleyin. 
 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]