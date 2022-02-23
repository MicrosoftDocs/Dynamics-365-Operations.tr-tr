---
title: İşe alma verilerindeki değişiklikleri izleme
description: İşlem denetimi özelliği adayların, açılan işlerin veya iş başvurularında raporlama veya uyumluluk nedenleriyle yapılan değişiklikleri izlemenize olanak sağlar.
author: tracykeya
manager: AnnBe
ms.date: 04/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2019 update
ms.openlocfilehash: c009f82e69bff0e4ea540514de8f9e60eca1e466
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462870"
---
# <a name="track-changes-in-recruiting-data"></a>İşe alma verilerindeki değişiklikleri izleme

[!include [banner](includes/banner.md)]

Denetim işlemeyi kullanarak adaylar, açılan işler veya iş başvurularında yapılan değişiklikleri izleyebilirsiniz. Raporlama veya uyumluluk açısından faydalıdır.

OData bağlayıcısını kullanarak Power BI'de izlenen verileri görüntüleyebilirsiniz. Daha fazla bilgi için bkz. [Power BI Desktop'ta OData akışlarına bağlanma](https://docs.microsoft.com/power-bi/desktop-connect-odata).

## <a name="track-changes"></a>Değişiklikleri izle
İşe alma verilerinde değişiklikleri izlemeyi ayarlamak için şu adımları uygulayın:

1. [Power Apps](https://web.powerapps.com)'ta uygun ortamı seçin.

2. **Ayarlar**'ı (dişli simgesi), **Gelişmiş özelleştirmeler**'i seçin ve sonra **Geliştirici kaynakları** altından **Kaynaklar**'ı seçin. 

3. **Geliştirici Kaynakları** sayfasında **Örnek Web API değeri** alanındaki değeri kopyalayın. Örneğin, değer şöyle görünebilir: https://yourorgname.api.crm.dynamics.com/api/data/v9.1/.

4. Daha sonra, aşağıdaki varlıkların birinden veri sorgulayabilirsiniz:
  - Açılan iş geçmişi (msdyn_jobopeninghistories)
  - İş başvurusu geçmişi (msdyn_jobapplicationhistories) 
  - Aday geçmişi (msdyn_candidatehistories)

## <a name="data-reported"></a>Raporlanan veri

Aşağıdaki veriler işlem denetiminde kullanılabilir.

| Raporlanan veri | Tanım |
| --- | --- |
| Değiştiren (msdyn_ChangedbyId) | Kullanıcıya referans |
| Oluşturma tarihi (createdon) |  Değişikliğin gerçekleştiği sıradaki UTC olarak tarih ve saat |
| Değişiklik türü (msdyn_changetype) | Hangi değişiklik oldu |
| Adaylara, açılan işlere <br></br>ve iş başvurularına ait ortak değerler | Oluşturulma tarihi<br></br>Güncelleştirildi |
| İş başvurusu geçmişi | Eklenen yapı <br></br>Kaldırılan yapı |
| Açılan iş geçmişi | YAPILACAK İŞ: gönderi eklendi <br></br>YAPILACAK İŞ: gönderi kaldırıldı <br></br>YAPILACAK İŞ: gönderi güncelleştirildi <br></br>YAPILACAK İŞ: katılımcı eklendi <br></br>YAPILACAK İŞ: katılımcı kaldırıldı |
| Aday geçmişi | Yapı eklendi <br></br>Yapı kaldırıldı <br></br>İş deneyimi eklendi <br></br>İş deneyimi kaldırıldı <br></br>Eğitim eklendi <br></br>Eğitim kaldırıldı <br></br>Yetenek eklendi <br></br>Yetenek kaldırıldı <br></br>Etiket eklendi <br></br>Etiket kaldırıldı <br></br>Sosyal ağ eklendi <br></br>Sosyal ağ kaldırıldı <br></br>Kişisel ayrıntılar eklendi <br></br>Kişisel ayrıntılar güncelleştirildi<br></br> |
| Değiştirilen alanlar (msdyn_changedfields) | JSON nesne listesi değiştirilen alanları tüm alanlar için değerleri depolamayabilir.<br></br><br></br>"Oluşturulan" ve "Güncelleştirilmiş" değişiklikler için, oluşturulan veya değiştirilen kayıttaki alanları listeler.<br></br><br></br>"Eklenen" değişiklik türleri için alt kayıttaki alanları listeler.<br></br><br></br>**Örnek:**<br></br><br></br>{<br></br>  "msdyn_applyurl": { "newValue": "" },<br></br>  "msdyn_description": { "valueOmitted": true } <br></br>} |
|İş başvurusu geçmişi | İş başvurusu (msdyn_JobapplicatonId)<br></br>Durum (msdyn_status) <br></br>Durum açıklaması (msdyn_statusreason) <br></br>Ret nedeni (msdyn_rejectionreason) |
| Açılan iş geçmişi | Açılan iş (msdyn_JobopeningId) <br></br>Durum (msdyn_jobopeningstatus) <br></br>Durum açıklaması (msdyn_jobopeningstatusreason) |
| Aday geçmişi | Aday (msdyn_CandidateId) |
