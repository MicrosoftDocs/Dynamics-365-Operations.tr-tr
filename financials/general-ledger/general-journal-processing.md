---
title: "Yevmiye defteri işlemi"
description: "Bu makaleler, yevmiye işlemlerini daha kolay yapmaya yardımcı olabilecek Microsoft Dynamics 365 for Operations yeteneklerini açıklamaktadır. Bunlar ayrıca doğru verilerin kaydedildiğini ve dahili denetimin hatasız olduğunu da garanti etmeye yardımcı olurlar."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 50cd203025be8857de943e458fc32315e494fb7a
ms.lasthandoff: 03/31/2017


---

# <a name="general-journal-processing"></a>Yevmiye defteri işlemi

[!include[banner](../includes/banner.md)]


Bu makaleler, yevmiye işlemlerini daha kolay yapmaya yardımcı olabilecek Microsoft Dynamics AX yeteneklerini açıklamaktadır. Bunlar ayrıca doğru verilerin kaydedildiğini ve dahili denetimin hatasız olduğunu da garanti etmeye yardımcı olurlar.  

Günlük adları

Ayarlanması gereken en önemli alanlardan biri günlük adlarıdır. Her amaç için belirli günlük adlarını tanımlamak iyi bir fikirdir; örneğin şirketlerarası, tahakkuk ayarlaması ve hata düzeltme gibi. Her günlük adını, her bir amaç için bir veri girişi yapmak için güvenle ve kolayca özelleştirebilirsiniz. 

**Günlük adları** sayfasında aşağıdaki öğeleri ayarlayabilirsiniz.

-   **İş akışı onayı** – İç denetim artırmak için toplam borç tutarı gibi ölçütlere göre gözden geçirme ve onay adımları için maddesellik sınırları kuran günlük iş akışları tanımlayın. Genel günlükler için iş akışlarını ** Genel muhasebe iş akışları** sayfası üzerinde ayarlarsınız.
-   **Varsayılan değerler** – Mahsup hesaplar, para ve mali boyutlar için varsayılan değerleri seçin.
-   **Günlük kontrolü** – Şirket ve hesap türü ve ayrıca segment değerleri üzerindeki kısıtlamaları ayarlayabilirsiniz. 

**Örnekler**

Günlük adı sadece ayarlamalar için kullanılabilir. Bu durumda, yalnızca **defter** hesap türünün tüm şirketler arasında geçerli olduğunu belirtebilirsiniz. [![Günlük kontrol hesap tipleri](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)

Günlük adı yalnızca belirli bir kesim veya ana hesap aralığı için kullanılabilir. [![Günlük kontrol segmenti](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)

**Otomatik ters** seçeneği genel günlüklerde kullanılabilir. Örneğin, aşağıdaki çizimde gösterildiği gibi gerçek belgenin henüz işlenmemiş olduğu tahakkuk ayarlamanız vardır.
[![Yevmiye günlüğü tersine çevirme](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png) 

Günlük girdisi için Microsoft Excel eklentisi, otomasyon ek düzeyi sağlar ve veri girişini kolaylaştırır. **Satırları Excel'de açma **eylemi **yevmiye defteri** ve **günlük fişi** sayfalarında mevcuttur. 

**Periyodik günlüklere** sayfası üzerinde, günlük işlemini otomatikleştirmek için yinelenen günlükler ayarlayabilirsiniz. 

Herhangi bir anda fiş şablonları kullanabilirsiniz. **Yevmiye defterleri** sayfası üzerinde, **Kaydet** ve **Fiş şablonu seç** eylemleri **Günlük fişi** sayfası üzerinde **İşlevler** altında fiş satırları için bulunur.

## <a name="related-setup"></a>İlgili kurulum
Aşağıdaki kurulum genel günlüklere özgü değildir, ancak veri girişinin doğru veri olduğunu ve kolay olduğunu garantilemeye yardımcı olur.

### <a name="main-account"></a>Ana hesap

Ana hesap kurulumu yevmiye defterine işlemek için birçok seçenek sağlar:

-   **DC/CR gereksinimi** – Bir ana hesap borç veya alacak hareketleriyle sınırlandırılmışsa, bu seçeneği kullanın. Kurulum, bir günlük doğrulandığında veya deftere nakledildiğinde doğrulanır.
-   **Varsayılan mahsup hesap**
-   **Askıya alınmış** – Tüm şirketler arasında veya belirli şirket/yasal varlıklar için bir ana hesap veri girişini askıya alma.
-   **El ile girişe izin verme** – Kullanıcıların hesap günlükleri için el ile bir değer girmesini engellemek.
-   **Varsayılan/Para birimi doğrula**
-   **Tüzel kişilik geçersizleştir** – Bu kurulum tanımlanan şirket/yasal varlığa özeldir:
    -   **Varsayılan/Satış vergisini doğrula**
    -   **Varsayılan boyut** – **Sabit olmayan** veya **Sabit değer**. **Sabit değer** bu ana hesap için tüm nakillerin**Sabit** olarak ayarladığınız herhangi bir boyut değeri her zaman kullanmasını garantilemeye yardımcı olur.
-   **Deftere nakli doğrulama**
    -   **Kullanıcı doğrulama** – Bu seçenek, bir ana hesap için deftere nakletmek için hangi kullanıcıların izinli olacağını denetler.
    -   **Deftere gönderme türü doğrulama** – Bu seçenek, bir ana hesap için hangi deftere nakletme türlerinin izinli olacağını denetler.

### <a name="accounting-structures-and-advanced-rules-structures"></a>Hesap yapıları ve gelişmiş kurallar yapıları

Hesap yapıları ve Gelişmiş kurallar yapıları finansal raporlama ve performans izleme için gerekli olan verilerin yevmiye işleme ve belgeleri sırasında yakalandığını güvence altına almak için büyük önem taşımaktadır. Hesap yapıları ve gelişmiş kurallar yapıları veri girişi deneyimini uyarlamanızı sağlar. Veri girişini sadece her durumda ilgili olan mali boyutları için izin verebilirsiniz ve zorunlu ve doğru verileri her zaman yakalanmasını gereksinimini de zorlayabilirsiniz.

Daha fazla bilgi için bkz.: [Planlama: Hesap planı](plan-chart-of-accounts.md). 



