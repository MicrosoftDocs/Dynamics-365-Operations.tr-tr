---
title: Dynamics 365 genelleştirme hizmetleri
description: Bu konu, Microsoft Dynamics 365 genelleştirme hizmetlerine genel bir bakış sağlar.
author: JaneA07
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 8fa82f741471a8314d01972b3ae3393eea4fd6b47bde647bf4ecdaebfea814a3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775082"
---
# <a name="dynamics-365-globalization-services"></a>Dynamics 365 genelleştirme hizmetleri

[!include [banner](../includes/banner.md)]

Aşağıdaki genelleştirme hizmetleri, bazı Microsoft Dynamics 365 çevrimiçi hizmetlerinde bulunan özellikleri genişletmek için yapılandırılabilir:

- **Regulatory Configuration Service (RCS)**, farklı türdeki elektronik belge ve raporların yapılandırılmasını destekler. RCS, Elektronik raporlama (ER) tasarımcısının, yapılandırma deposunun bağımsız bir hizmet olduğu gelişmiş bir sürümünü sağlar. Daha fazla bilgi için, bkz. [Regulatory Configuration Service](rcs-overview.md).
- **Elektronik Faturalama** dönüştürmeleri, dijital imzaları ve sertifika ve yanıt işleme dahil olmak üzere harici web hizmetleriyle bağlantı için yapılandırılabilen tümleştirmeleri bir araya getirir. Daha fazla bilgi için bkz. [Elektronik Faturalama](e-invoicing-service-overview.md).
- **Vergi Hesaplama** çoklu vergi kodlarını, vergi kodu belirlemeyi, vergi hesaplama tasarımcısını ve dünya çapında karmaşık vergi düzenlemelerine uymak amacıyla bir çalışma zamanı altyapısını destekleyerek gelişmiş esneklik sağlar. Daha fazla bilgi için bkz. [Vergi Hesaplama](global-tax-calcuation-service-overview.md).

Bu genelleştirme hizmetleri, aşağıdaki Dynamics 365 çevrimiçi hizmetleriyle kullanıma hazır tümleştirme sağlar.

| Çevrimiçi hizmet | DYH | Elektronik Faturalama | Vergi Hesaplama (Önizleme) |
|----------------|-----|----------------------|---------------------------|
| Dynamics 365 Finance | Evet | Evet | Evet | 
| Dynamics 365 Supply Chain Management | Evet | Evet | Evet | 
| Dynamics 365 Project Operations | Evet | Evet | Geçerli değil | 
| Dynamics 365 Commerce | Evet | Geçerli değil | Geçerli değil | 

> [!NOTE]
> Azure coğrafi konumlarının (coğrafi bölgeler) RCS için kullanılabilirliğine ilişkin farklılıklar nedeniyle, bu hizmetin yapılandırması müşteri verilerinin geçerli Dynamics 365 çevrimiçi hizmeti için seçilen coğrafi bölge dışına aktarılmasına neden olabilir. Daha fazla bilgi için bkz. [Dynamics 365 ve Power Platform: Kullanılabilirlik, veri konumu, dil ve yerelleştirme](https://aka.ms/rcs/D365Productavailabilityguide).