---
title: Genel günlük işleme
description: Bu konu, yevmiye işlemlerini daha kolay yapmaya yardımcı olabilecek Microsoft Dynamics 365 Finance yeteneklerini açıklamaktadır. Bunlar ayrıca doğru verilerin kaydedildiğini ve dahili denetimin hatasız olduğunu da sağlamaya yardımcı olurlar.
author: kweekley
ms.date: 08/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7f9f4019618891909e674c6b936f79778ac84744
ms.sourcegitcommit: 4f8465729d7ae0bf5150a2785a6140c984c7030e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2021
ms.locfileid: "7726789"
---
# <a name="general-journal-processing"></a>Genel günlük işleme

[!include [banner](../includes/banner.md)]

Bu konu, yevmiye işlemlerini daha kolay yapmaya yardımcı olabilecek yetenekleri açıklamaktadır. Bunlar ayrıca doğru verilerin kaydedildiğini ve dahili denetimin hatasız olduğunu da sağlamaya yardımcı olurlar.  

## <a name="journal-names"></a>Günlük adları

Ayarlanması gereken en önemli alanlardan biri günlük adlarıdır. Her amaç için belirli günlük adlarını tanımlamak iyi bir fikirdir; örneğin şirketlerarası, tahakkuk ayarlaması ve hata düzeltme gibi. Her günlük adını, her bir amaç için bir veri girişi yapmak için güvenle ve kolayca özelleştirebilirsiniz. 

**Günlük adları** sayfasında aşağıdaki öğeleri ayarlayabilirsiniz.

-   **İş akışı onayı** – İç denetim artırmak için toplam borç tutarı gibi ölçütlere göre gözden geçirme ve onay adımları için maddesellik sınırları kuran günlük iş akışları tanımlayın. Genel günlükler için iş akışlarını **Genel muhasebe iş akışları** sayfası üzerinde ayarlarsınız.
-   **Varsayılan değerler** – Mahsup hesaplar, para ve mali boyutlar için varsayılan değerleri seçin.
-   **Günlük kontrolü** – Şirket ve hesap türü ve ayrıca segment değerleri üzerindeki kısıtlamaları ayarlayabilirsiniz. 

**Örnekler**

Günlük adı sadece ayarlamalar için kullanılabilir. Bu durumda, yalnızca **defter** hesap türünün tüm şirketler arasında geçerli olduğunu belirtebilirsiniz. 

[![Günlük kontrol hesap tipleri.](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)

Günlük adı yalnızca belirli bir kesim veya ana hesap aralığı için kullanılabilir. 

[![Günlük kontrol segmenti.](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)

**Otomatik ters** seçeneği genel günlüklerde kullanılabilir. Örneğin, aşağıdaki çizimde gösterildiği gibi gerçek belgenin henüz işlenmemiş olduğu tahakkuk ayarlamanız vardır.
[![Yevmiye günlüğü tersine çevirme.](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png) 

Günlük girdisi için Microsoft Excel eklentisi, otomasyon ek düzeyi sağlar ve veri girişini kolaylaştırır. **Satırları Excel'de açma** eylemi **yevmiye defteri** ve **günlük fişi** sayfalarında mevcuttur. 

**Periyodik günlüklere** sayfası üzerinde, günlük işlemini otomatikleştirmek için yinelenen günlükler ayarlayabilirsiniz. 

Herhangi bir anda fiş şablonları kullanabilirsiniz. **Yevmiye defterleri** sayfası üzerinde, **Kaydet** ve **Fiş şablonu seç** eylemleri **Günlük fişi** sayfası üzerinde **İşlevler** altında fiş satırları için bulunur.

## <a name="related-setup"></a>İlgili kurulum
Aşağıdaki kurulum genel günlüklere özgü değildir, ancak veri girişinin doğru veri olduğunu ve kolay olduğunu sağlamaya yardımcı olur.

### <a name="main-account"></a>Ana hesap

Ana hesap kurulumu yevmiye defterine işlemek için birçok seçenek sağlar:

-   **DC/CR gereksinimi** – Bir ana hesap borç veya alacak hareketleriyle sınırlandırılmışsa, bu seçeneği kullanın. Kurulum, bir günlük doğrulandığında veya deftere nakledildiğinde doğrulanır.

-   **Varsayılan mahsup hesap**
-   **Askıya alınmış** – Tüm şirketler arasında veya belirli şirket/yasal varlık için bir ana hesap veri girişini askıya alma.
-   **El ile girişe izin verme** – Kullanıcıların hesap günlükleri için el ile bir değer girmesini engellemek.
-   **Varsayılan/Para birimi doğrula**
-   **Tüzel kişilik geçersizleştir** – Bu kurulum tanımlanan şirket/yasal varlığa özeldir:
    -   **Varsayılan/Satış vergisini doğrula**
    -   **Varsayılan boyut** – **Sabit olmayan** veya **Sabit değer**. **Sabit değer** bu ana hesap için tüm nakillerin **Sabit** olarak ayarladığınız herhangi bir boyut değeri her zaman kullanmasını sağlamaya yardımcı olur.
-   **Deftere nakli doğrulama**
    -   **Kullanıcı doğrulama** – Bu seçenek, bir ana hesap için deftere nakletmek için hangi kullanıcıların izinli olacağını denetler.
    -   **Deftere gönderme türü doğrulama** – Bu seçenek, bir ana hesap için hangi deftere nakletme türlerinin izinli olacağını denetler.

### <a name="accounting-structures-and-advanced-rules-structures"></a>Hesap yapıları ve gelişmiş kurallar yapıları

Hesap yapıları ve Gelişmiş kurallar yapıları finansal raporlama ve performans izleme için gerekli olan verilerin yevmiye işleme ve belgeleri sırasında yakalandığını sağlamak için büyük önem taşımaktadır. Hesap yapıları ve gelişmiş kurallar yapıları veri girişi deneyimini uyarlamanızı sağlar. Veri girişini sadece her durumda ilgili olan mali boyutları için izin verebilirsiniz ve gerekli ve doğru verileri her zaman yakalanmasını gereksinimini de zorlayabilirsiniz.

Daha fazla bilgi edinmek için aşağıdaki konulara bakın:
- [Hesap planınızı planlama](plan-chart-of-accounts.md) 
- [Günlükler için gelişmiş kurallar oluşturma](tasks/create-advanced-rules-journals.md)
- [Şablon kullanarak yevmiye defteri girişi oluşturun](tasks/create-journal-entry-template.md)
- [Günlükler oluşturma ve doğrulama](tasks/create-validate-journals.md)
- [Periyodik günlükleri deftere nakletme](tasks/post-periodic-journals.md)
- [Genel muhasebe tahsisat günlüğünü işleme](tasks/process-ledger-allocation-journal.md)

## <a name="simulate-posting"></a>Deftere nakil benzetimi gerçekleştir
**Deftere nakletmeyi simüle et**'i çoğu günlük için **Doğrula** menüsünde bulabilirsiniz. Bir günlüğü **Doğrula** işlevini kullanarak doğruladığınızda, sistem günlüğü belirli hata koşullarına karşı test eder. **Deftere nakletmeyi simüle et** işlevini kullanırsanız, sistem, deftere nakil sırasında çalıştırılacak tüm işlemleri günlüğü deftere gerçekte nakletmeden yapar. Daha sonra görüntülenen deftere nakil mesajlarını gözden geçirebilir, bulduğunuz hataları düzeltebilir ve daha sonra günlüğü deftere nakletmek için **Deftere naklet** menüsünü açabilirsiniz. 

**Deftere nakletmeyi simüle et**, toplu işlem için kullanılamaz. Ancak, deftere nakli toplu iş için simüle etme kodu mevcuttur ve geliştiriciler bu kodu bu özelliğe eklemek üzere genişletebilir.  

## <a name="journal-unlock"></a>Günlüğün kilidini açma
Günlük sayfasında, "sistem tarafından kilitlendi" durumunda olan bir günlüğün kilidini açmak için Evet olarak ayarlanmış bir düğme vardır. Bu kilit açma işlemi, yürütülmekte olan toplu işleri analiz eden ve bu günlüğün artık etkin bir şekilde bir toplu işlem tarafından işlenmediğini onaylayan Sistem Yöneticisi tarafından gerçekleştirilebilir. Bu düğme,**Özellik Yönetimi** sayfasındaki **Günlük kilidini aç düğmesi** adlı özellik tarafından etkinleştirilir. 

## <a name="workflow-recall"></a>İş akışı geri çağırma 
Durumu "kurtarılamaz" olan bir iş akışındaki günlüğü geri çağırma özelliği, bir günlükteki ve **İş akışı geçmişi** sayfasındaki **İş akışı** düğmesi kullanılarak etkinleştirilir. Bu, **Özellik Yönetimi** sayfasındaki **Günlükler için iş akışı durumunu sıfırlama** adlı özellik tarafından etkinleştirilir.

## <a name="delete-journal-lines"></a>Günlük Satırlarını Silme
Tüm günlük satırlarını hızlı bir şekilde silme özelliği, **İşlevler** > **Günlük Satırlarını Sil** altındaki bir günlükte etkinleştirilir. Bu özelliği etkinleştirmek için, **Özellik yönetimi**'nde, **Günlük performansı iyileştirmelerini sil**'i seçin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
