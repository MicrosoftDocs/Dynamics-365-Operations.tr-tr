---
title: "Dynamics 365 for Talent sistem gereksinimleri ve güncelleştirme ilkesi"
description: "Bu konu Dynamics 365 for Talent için gereksinimleri listeler. Güncelleştirme ilkesi de açıklanmaktadır."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-talent
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7bcc8464d34c35423e86c963c6b493fc09db4472
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="microsoft-dynamics-365-for-talent-system-requirements-and-update-policy"></a>Microsoft Dynamics 365 for Talent sistem gereksinimleri ve güncelleştirme ilkesi

[!include[banner](includes/banner.md)]


Bu konu Microsoft Dynamics 365 for Talent için gereksinimleri listeler. Güncelleştirme ilkesi de açıklanmaktadır.

## <a name="supported-web-browsers"></a>Desteklenen web tarayıcıları

Microsoft Dynamics 365 for Talent web uygulamasını belirtilen işletim sistemleri üzerinde çalışan aşağıdaki web tarayıcılarından birinde çalıştırabilirsiniz: 

*   Windows 10 üzerinde Microsoft Edge (son genel olarak yayımlanmış sürüm)
*   Windows 10, Windows 8.1 veya Windows 7 üzerinde Internet Explorer 11
*   Windows 10, Windows 8.1, Windows 8, Windows 7 veya Google Nexus 10 tablet üzerinde Google Chrome (son genel olarak yayımlanan sürümü)
*   Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) ve 10.12 (Sierra) veya Apple iPad üzerinde Apple Safari (son genel olarak yayınlanmış sürüm)

Her web tarayıcısı için en son sürümü bulmak için, yazılım üreticisinin web sitesine gidin. 

> [!NOTE]
> * Görev Kaydedici'den oluşturulmuş görüntüleri yakalamak ve bunları Microsoft Word belgelerine eklemek için bir Chrome eklentisinin yüklü olması gerekir. 
> * İş Akışı Düzenleyicisi bir ClickOnce uygulaması olarak başlatılır. ClickOnce uygulamalarını yalnızca Microsoft Edge ve Internet Explorer (Microsoft Windows'un desteklenen bir sürümünde) destekler. İş Akışı Düzenleyicisi ClickOnce uygulaması için 64-bit uyumlu bir işletim sistemi gereklidir.
> * PDF dosyalarının önizlemesini yapmak için (en son sürüm genel kullanıma açık) Windows 10 üzerinde, Microsoft Edge veya (en son sürüm genel kullanıma açık) Windows 10, Windows 8.1, Windows 8, Windows 7 veya Google Nexus 10 tablet üzerinde Google Chrome gibi modern tarayıcıları kullanmanızı öneririz.
Ağ gereksinimleri
> * Dynamics 365 for Talent 250-300 milisaniye (ms) veya daha az gecikmeli ağlar için tasarlanmıştır. Bu gecikme, bir tarayıcı istemcisinden Dynamics 365 for Talent'ı barındıran Microsoft Azure veri merkezine iletim süresidir. Ağ bağlantı gecikmesini [www.azurespeed.com] (http://www.azurespeed.com "Azure Latency Test") adresinden test etmenizi öneririz.
> * Dynamics 365 for Talent için bant genişliği gereksinimleri senaryoya bağlıdır. En tipik senaryolar 50 kilobayt/saniye (KBps) üzerinde bir bant genişliği gerektirir.

> [!WARNING]
> Kullanıcı sayısıyla minimum bant genişliği gereksinimlerini çarpıp bir müşteri konumundan bant genişliği gereksinimlerini hesaplamayın. Belirli bir konumun eşzamanlı kullanımını hesaplamak çok zordur. Bant genişliği gereksinimleri konusunda kaygıları olan müşteriler Dynamics 365 for Talent'ın bir deneme sürümünü kullanabilir.

## <a name="supported-microsoft-office-applications"></a>Desteklenen Microsoft Office uygulamaları

*   Microsoft Excel ve Word eklentilerini çalıştırmak için Windows veya Mac için Microsoft Office 2016'yı yüklemiş olmanız gerekir. Sürüm gereksinimleri hakkında ayrıntılar için bkz. [Office tümleştirme sorun giderme] (../dev-itpro/office-integration/office-integration-troubleshooting.md "Office integration troubleshooting").
*   Excel'e Aktar veya Word'e Aktar işleviyle oluşturulan belgeleri görüntülemek için Microsoft Office 2007 veya sonraki bir sürümü yüklemiş olmanız gerekir.

## <a name="update-policy"></a>Güncelleştirme ilkesi

Microsoft Dynamics 365 for Talent bir bulut servisi olarak sunulur. Dynamics 365 for Talent güncelleştirmeleri süreklidir ve Microsoft tarafından otomatik olarak uygulanır.

Güncelleştirmeler düzenli aralıklarla yayımlanır ve güncelleştirmeler tüm ortamlar için yapılır.  Dynamics 365 for Talent, ürün destek kullanılabilirliği hakkında düzenli ve öngörülebilir kılavuzlar sunan [Microsoft Support Lifecycle policy] (https://support.microsoft.com/en-us/gp/lifecycle#gp/OSSLpolicy "Microsoft Support Lifecycle") ile uygun olarak desteklenir.

